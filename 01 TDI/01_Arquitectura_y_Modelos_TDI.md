# Arquitectura y Modelos TDI - Línea de Quesos

## Introducción
Este documento consolida la arquitectura de control y los modelos operativos para la modernización de la planta láctea. El diseño se enmarca bajo los principios de la **Transformación Digital Industrial (TDI)**, la cual se define como la integración holística y creciente de las tecnologías digitales con los procesos industriales[cite: 51]. La TDI va más allá de la simple automatización; busca empoderar a las personas, optimizar los procesos y transformar cómo opera la fábrica para fortalecer la estrategia de negocio y generar mayor valor para el cliente[cite: 51].

Mediante la aplicación de estándares internacionales (ISA-88 e ISA-95), este documento estructura la planta física, define las recetas de producción y detalla la instrumentación necesaria para asegurar el flujo correcto de la información desde el proceso hasta la toma de decisiones.

## Tabla de Contenido
1. [Introducción](#introducción)
2. [Modelo físico ISA-88 · Línea de quesos](#modelo-físico-isa-88--línea-de-quesos)
3. [Modelo procedimental ISA-88 · Línea de quesos](#modelo-procedimental-isa-88--línea-de-quesos)
4. [Instrumentación, variables y comunicaciones · Línea de quesos](#instrumentación-variables-y-comunicaciones--línea-de-quesos)

---

## Modelo físico ISA-88 · Línea de quesos
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

*(Las áreas de yogures (A2) y UHT (A4) se reservan en la numeración, sin detalle).*

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

## Modelo procedimental ISA-88 · Línea de quesos
Procedimiento → Procedimiento de unidad → Operación → Fase.
Un solo procedimiento para las tres referencias; cada receta (Q1-Q3) cambia los parámetros.

| Procedimiento de unidad | Operaciones (de los diagramas de proceso) | Fases de ejemplo (PLC) |
|---|---|---|
| UP-301 Acondicionar leche | Tratamiento térmico en marmita, estandarizar grasa, atemperar | Calentar al SP de receta; mantener; enfriar a temperatura de atemperado |
| UP-302 Cuajada | Activar cultivo, diluir cuajo y CaCl₂, adicionar insumos, coagular, cortar, agitar y desuerar, acidificar | Dosificar; reposo con PID activo hasta firmeza; corte a tamaño de grano; desuerado a T y tiempo; vaciado |
| UP-303 Hilar y moldear | Trocear cuajada, hilar y amasar, moldear | Hilar hasta pH crítico con agua a T de receta; moldear bloque |
| UP-304 Salmuera | Preparar salmuera, enfriar y salmuerar | Mantener T de salmuera; inmersión temporizada; extraer |
| UP-305 Empacar | Escurrir y secar, empacar, codificar lote, inspeccionar, armar caja, encajonar, paletizar | Vacío y sellado; codificar fecha y lote; verificar sello y metales |

**Puntos de inspección:** pH, temperatura de leche, bolsas, vacío y sellado, producto terminado.

*Pendientes:* Unificar el nombre de Q3 (quesillo o quesadillo; el diagrama incluye bocadillo, la tabla de recetas no) y confirmar si Q2 pasa por salmuera (la tabla sí, el diagrama dice "hilado y salado").

---

## Instrumentación, variables y comunicaciones · Línea de quesos

| Unidad | Variables críticas | Sensores | Actuadores | Control |
|---|---|---|---|---|
| UN-301 Marmita | Temperatura, nivel | PT100, nivel | Válvula de vapor | Grafcet + PID |
| UN-302 Tina | Temperatura, firmeza, pH, caudal, nivel | PT100, firmeza, pH, caudalímetro | Válvulas vapor/agua helada, variador de liras, bomba lobular | PID de camisa + Grafcet de tina |
| UN-303 Hiladora | Temperatura de agua y pasta, pH | PT100, pH ISFET | Calentamiento, variador | PID + control de velocidad |
| UN-304 Moldeadora | Conteo de bloques | Sensor de conteo | Motor | Lógica discreta |
| UN-305 Salmuera | Temperatura, tiempo, nivel | PT100, nivel | Grúa, enfriamiento | Temporizador + PID |
| UN-306 Empacadora | Vacío, temperatura de sello, conteo, metales | Vacío, óptico, detector de metales | Sellado, codificador | Ladder |
| UN-502 Paletizado | Posición, presencia | Sensores ópticos | Robot | Ladder + robot |

**Comunicaciones:** N1-N2 cableado y EtherNet/IP · N2-N3 OPC · N3-N4 OPC UA/API · N4-N5 B2MML/servicios web.
