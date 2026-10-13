# Arquitectura y Modelos TDI - Planta Láctea

## Introducción a la Transformación Digital Industrial (TDI)
La Transformación Digital Industrial (TDI) es la integración holística de las tecnologías digitales con los procesos físicos de manufactura. Su objetivo principal trasciende la simple instalación de hardware automatizado; busca conectar el piso de planta (OT) con los sistemas de gestión empresarial (IT). Mediante la adopción de tecnologías de medición, control y plataformas como SCADA, MES y ERP, la TDI convierte los datos operativos en información estratégica para optimizar la rentabilidad, garantizar la calidad y respaldar la toma de decisiones del negocio en tiempo real.

### ¿Por qué elegimos la Línea de Quesos de Pasta Hilada?
Para desarrollar la ingeniería de detalle, seleccionamos la línea de quesos de pasta hilada debido a que representa el desafío mecatrónico e informático más completo de la planta:
1. **Naturaleza Híbrida:** Exige gobernar la transición perfecta entre procesos por lotes rígidos (coagulación de la cuajada en tinas durante 30-40 min), procesos continuos (hilado y amasado termomecánico) y procesos discretos rápidos (moldeo y empaque)[cite: 214].
2. **Impacto en Seguridad (Operacional):** La automatización de la hiladora elimina la necesidad de que los operarios manipulen manualmente la masa en agua a altas temperaturas (75 °C - 85 °C), reduciendo el riesgo de accidentes laborales.
3. **Control Crítico de Calidad (Económico):** El éxito de la pasta hilada depende de alcanzar un pH exacto (4.9 a 5.1). Implementar sensores ISFET en línea integrados al SCADA evita el error humano en la medición, reduciendo drásticamente las mermas térmicas y los rechazos de producto.
4. **Flexibilidad (ISA-88):** Permite demostrar cómo el sistema MES descarga recetas específicas a los mismos equipos físicos para producir referencias con variables muy distintas (Mozzarella, Quesillo y 7 Cueros).

---

## Tabla de Contenido
1. [Introducción y Justificación](#introducción-a-la-transformación-digital-industrial-tdi)
2. [Modelo físico ISA-88 · Línea de quesos](#1-modelo-físico-isa-88--línea-de-quesos)
3. [Modelo procedimental ISA-88 · Línea de quesos](#2-modelo-procedimental-isa-88--línea-de-quesos)
4. [Instrumentación, variables y comunicaciones](#3-instrumentación-variables-y-comunicaciones--línea-de-quesos)
5. [Referencias adicionales de planta (Yogures y UHT)](#4-referencias-adicionales-de-planta-yogures-y-uht)
6. [Fuentes y Bibliografía](#5-fuentes-y-bibliografía)

---

## 1. Modelo físico ISA-88 · Línea de quesos
Jerarquía: Área → Celda → Unidad → Módulo de equipo (EM) → Módulo de control (CM).
Los tags son propuestos y se confirman con el P&ID.

### Estructura
| Área | Celda | Unidad |
|---|---|---|
| A1 Recepción y acondicionamiento (compartida) | C1.1 Recepción y filtrado | UN-101 tanque de recepción; UN-102 filtro y enfriador (4 °C) |
| | C1.2 Estandarización y pasteurización | UN-103 estandarizador; UN-104 pasteurizador de placas (72 °C, 15 s); UN-105 silos |
| A3 Quesos | C3.1 Tratamiento y cuajada | UN-301 marmita 4.800 L; UN-302 tina quesera |
| | C3.2 Hilado y moldeo | UN-303 hiladora; UN-304 moldeadora |
| | C3.3 Salmuera | UN-305 tanques de salmuera |
| | C3.4 Empaque | UN-306 empacadora al vacío; UN-307 manejo de lactosuero |
| A5 Producto terminado | — | UN-501 encajonado; UN-502 celda robotizada de paletizado; UN-503 cuarto frío |
| A6 Servicios | — | UN-601 CIP; UN-602 vapor; UN-603 agua helada |

*Nota: Las áreas de yogures (A2) y UHT (A4) se reservan en la numeración, sin detalle profundo en ISA-88.*

### Módulos de equipo y de control
| Unidad | Módulos de equipo | Módulos de control |
|---|---|---|
| UN-301 Marmita | Calentamiento (vapor), llenado/vaciado | TE-301 PT100, LT-301 nivel, FV-301 válvula de vapor |
| UN-302 Tina | Camisa térmica; liras de corte y agitación; dosificación de cuajo y CaCl₂; llenado/vaciado | TE-302 PT100, AT-302 firmeza, AT-303 pH, FIT-302 caudal, LT-302 nivel, FV-302 vapor, FV-303 agua helada, M-302 variador de liras, PU-302 bomba lobular |
| UN-303 Hiladora | Calentamiento de agua; tornillos de amasado | TE-304 agua, TE-305 pasta, AT-304 pH ISFET, M-303 variador, FV-304 calentamiento |
| UN-304 Moldeadora | Rodillos de moldeo | ZS-304 conteo, M-304 motor |
| UN-305 Salmuera | Enfriamiento, manipulador de jaulas | TE-306 temperatura, LT-306 nivel, M-305 grúa |
| UN-306 Empacadora | Vacío, sellado, codificador de lote | PT-306 vacío, TE-307 temperatura de sello, ZS-306 conteo óptico, XA-306 detector de metales |
| UN-307 Lactosuero | Transferencia a silo | LT-307 nivel, PU-307 bomba |

---

## 2. Modelo procedimental ISA-88 · Línea de quesos
Procedimiento → Procedimiento de unidad → Operación → Fase.
Un solo procedimiento maestro para las tres referencias; cada receta (Q1-Q3) altera los parámetros de ejecución.

| Procedimiento de unidad | Operaciones (de los diagramas de proceso) | Fases de ejemplo (PLC) |
|---|---|---|
| UP-301 Acondicionar leche | Tratamiento térmico en marmita, estandarizar grasa, atemperar | Calentar al SP de receta; mantener; enfriar a temperatura de atemperado |
| UP-302 Cuajada | Activar cultivo, diluir cuajo y CaCl₂, adicionar insumos, coagular, cortar, agitar y desuerar, acidificar | Dosificar; reposo con PID activo hasta firmeza; corte a tamaño de grano; desuerado a T y tiempo; vaciado |
| UP-303 Hilar y moldear | Trocear cuajada, hilar y amasar, moldear | Hilar hasta pH crítico con agua a T de receta; moldear bloque |
| UP-304 Salmuera | Preparar salmuera, enfriar y salmuerar | Mantener T de salmuera; inmersión temporizada; extraer |
| UP-305 Empacar | Escurrir y secar, empacar, codificar lote, inspeccionar, armar caja, encajonar, paletizar | Vacío y sellado; codificar fecha y lote; verificar sello y metales |

**Puntos de inspección clave:** pH en mesa de desuerado, temperatura de leche, integridad de bolsas, vacío/sellado y detección de metales en producto terminado.

---

## 3. Instrumentación, variables y comunicaciones · Línea de quesos

| Unidad | Variables críticas | Sensores | Actuadores | Control |
|---|---|---|---|---|
| UN-301 Marmita | Temperatura, nivel | PT100, nivel | Válvula de vapor | Grafcet + PID |
| UN-302 Tina | Temperatura, firmeza, pH, caudal, nivel | PT100, firmeza, pH, caudalímetro | Válvulas vapor/agua helada, variador de liras, bomba lobular | PID de camisa + Grafcet de tina |
| UN-303 Hiladora | Temperatura de agua y pasta, pH | PT100, pH ISFET | Calentamiento, variador | PID + control de velocidad |
| UN-304 Moldeadora | Conteo de bloques | Sensor de conteo | Motor | Lógica discreta |
| UN-305 Salmuera | Temperatura, tiempo, nivel | PT100, nivel | Grúa, enfriamiento | Temporizador + PID |
| UN-306 Empacadora | Vacío, temperatura de sello, conteo, metales | Vacío, óptico, detector de metales | Sellado, codificador | Ladder |
| UN-502 Paletizado | Posición, presencia | Sensores ópticos | Robot | Ladder + robot |

**Comunicaciones (Arquitectura ISA-95):** 
* N1-N2: Cableado duro y EtherNet/IP
* N2-N3: Protocolo OPC
* N3-N4: OPC UA / API Rest
* N4-N5: Estándar B2MML / Servicios Web

---

## 4. Referencias adicionales de planta (Yogures y UHT)
Aunque el enfoque de automatización recae sobre los quesos, la planta procesa las siguientes referencias en paralelo compartiendo los recursos de Nivel A1.

### Yogures
| Parámetro | Y1 Firme | Y2 Batido | Y3 Bebible (propuesta) |
|---|---|---|---|
| **Fermentación** | En el envase[cite: 214] | En tanque[cite: 214] | En tanque |
| **Después de fermentar** | Enfriar y almacenar a 4 °C | Enfriar; inyección de fruta[cite: 214] | Homogeneizar, enfriar |
| **Fase Común** | Tratamiento 85 °C por 20-30 min o 90-95 °C por 3-5 min[cite: 214]; incubación 40-43 °C hasta pH 4,5-4,6 (4-5 h)[cite: 214]; homogeneización 138-172 bar | *(Comparte parámetros base)* | *(Comparte parámetros base)* |

### Leche UHT y bebidas
| Parámetro | L1 Entera | L2 Deslactosada | L3 Saborizada chocolate (propuesta) |
|---|---|---|---|
| **Tratamiento UHT** | 135-140 °C, 2-4 s | Igual | Igual |
| **Adición en línea** | Ninguna | Lactasa aséptica después del UHT, ~0,3 g/L | Cacao, azúcar, estabilizante |

---

## 5. Fuentes y Bibliografía
* Teagasc, ficha *Production of Yoghurt*: [https://teagasc.ie/wp-content/uploads/media/website/rural-economy/rural-development/diversification/1-Production-of-Yoghurt.pdf](https://teagasc.ie/wp-content/uploads/media/website/rural-economy/rural-development/diversification/1-Production-of-Yoghurt.pdf)
* SPX FLOW, boletín técnico de homogeneización y UHT: [https://www.spxflow.com/assets/pdf/apv-homogenizer-used-with-uht-us.pdf](https://www.spxflow.com/assets/pdf/apv-homogenizer-used-with-uht-us.pdf)
* Tetra Pak, leche deslactosada: [https://www.tetrapak.com/solutions/categories/dairy/white-milk/lactose-free-milk-drinks](https://www.tetrapak.com/solutions/categories/dairy/white-milk/lactose-free-milk-drinks)
* GEA, dosificación aséptica: [https://www.packaginginsights.com/news/aseptic-dosing-station-from-gea-tds.html](https://www.packaginginsights.com/news/aseptic-dosing-station-from-gea-tds.html)
* Tetra Pak, *Dairy Processing Handbook* (Referencia general de procesos lácteos).
