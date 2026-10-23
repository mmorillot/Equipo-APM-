# Estudio de Factibilidad Financiera: Celda Robotizada de Fin de Línea e Inspección en Línea

* **Proyecto:** Automatización del Fin de Línea y Control Metrológico de Empaque
* **Empresa Beneficiaria:** Planta Láctea (Modelo Lácteos San Mateo)
* **Preparado por:** Equipo de Ingeniería y Finanzas de Proyectos de Automatización
* **Fecha de Evaluación:** Octubre de 2026
* **Horizonte de Evaluación:** 5 años
* **Moneda Base:** Pesos Colombianos (COP) | **Tasa de Cambio (TRM):** $1\text{ USD} = \$3.192,73\text{ COP}$

---

## 1. Resumen Ejecutivo de la Propuesta Financiera

El presente estudio evalúa la viabilidad técnica y financiera para la implementación de una **Celda Compacta de Fin de Línea 3 en 1** dentro de la cámara de conservación a **8°C**. El sistema integra el aseguramiento de calidad en continuo mediante **Báscula Dinámica (Checkweigher)** y **Sistema de Visión Artificial**, vinculados a una estación de paletizado automático con manipulador robótico industrial **Yaskawa Motoman PL80**, herramienta de succión por espuma **Schmalz FXP** y central de aire comprimido **Atlas Copco G 7P-10 FF**.

### Principales Conclusiones Financieras (Escenario Actualizado)
* **Inversión Inicial Total (CAPEX):** **$\$492.190.531\text{ COP}$** ($\$154.159,77\text{ USD}$), que comprende equipamiento de paletizado, instrumentación de calidad, periféricos neumáticos, cerramientos normativos, logística de importación, servicios integrales de ingeniería y la nómina directa de los 6 ingenieros asociados al proyecto.
* **Costo Operativo Anual (OPEX):** **$\$25.835.040\text{ COP/año}$**, incluyendo consumo eléctrico regulado bajo un régimen operativo de 4 días/semana ($208\text{ días/año}$), repuestos de desgaste, consumibles neumáticos, calibraciones metrológicas anuales y póliza de soporte técnico.
* **Beneficios y Ahorros Anuales Brutos:** **$\$210.991.800\text{ COP/año}$**, impulsados por la recuperación de materia prima al controlar el sobrepeso (*giveaway* de $13\text{ g/unidad}$ en $1.911\text{ unidades/día}$), eliminación de rechazos comerciales por empaque defectuoso, optimización de mano de obra en frío y supresión de caídas de producto.
* **Flujo de Caja Libre Operativo (FCLO):** **$\$154.805.231\text{ COP/año}$** durante los años 1 al 4, y **$\$194.805.231\text{ COP}$** en el año 5 al liquidar el valor de salvamento residual.
* **Valor Presente Neto (VPN):** **$+\$66.954.202\text{ COP}$**, descontado a una TIO exigida del **13,50% E.A.**
* **Tasa Interna de Retorno (TIR):** **18,82% E.A.**, superando la tasa de corte corporativa (**+5,32%** de margen de seguridad financiera).
* **Período de Recuperación de Capital (Payback):** **3,18 años** en términos nominales (3 años y 2 meses) y **4,39 años** en términos descontados (4 años y 4 meses, recuperado dentro del ciclo de depreciación fiscal de 5 años).
* **Retorno sobre la Inversión (ROI):** **31,45% anual** y **65,39% acumulado a 5 años**.

---

## 2. Registro de Cambios frente al Modelo Base

En esta versión del modelo financiero (`Modelo_Financiero.xlsx`) se incorporaron cinco ajustes estructurales respecto a la línea base inicial:

| Parámetro / Rubro Modificado | Modelo Base Inicial | Modelo Actualizado (`Modelo_Financiero.xlsx`) | Impacto Técnico y Financiero |
| :--- | :--- | :--- | :--- |
| **Tasa de Cambio (TRM)** | $\$4.124,50\text{ COP/USD}$ | **$\$3.192,73\text{ COP/USD}$** | Reduce el costo en COP del equipamiento importado en un 22,59%. |
| **Ítem 4.6: Sueldo Ingenieros (CAPEX)** | No desglosado aparte | **$\$84.000.000\text{ COP}$** ($\$26.309,77\text{ USD}$) | Incorpora el salario de los 6 ingenieros asociados al proyecto (salario base de $\$3.500.000\text{ COP}$), elevando la participación de Integración al 30,69% del CAPEX. |
| **Régimen Operativo Anual** | $312\text{ días/año}$ ($2.496\text{ h/año}$) | **$208\text{ días/año}$ ($1.664\text{ h/año}$)** | Operación de 4 días/semana en turno de $8\text{ h/día}$; disminuye el consumo eléctrico anual a $10.982,4\text{ kWh/año}$ ($\$9.335.040\text{ COP/año}$). |
| **Producción Diaria Empacada** | $3.000\text{ unidades/día}$ | **$1.911\text{ unidades/día}$** | Ajuste al volumen real de bloques de queso empacados al vacío por turno diario. |
| **Recuperación de Sobrepeso (*Giveaway*)** | $10\text{ g/unidad}$ ($0,010\text{ kg}$) | **$13\text{ g/unidad}$ ($0,013\text{ kg}$)** | Recupera $24,843\text{ kg/día}$ ($\approx 25\text{ kg/día}$), generando un ahorro metrológico anual de $\$64.591.800\text{ COP/año}$. |

---

## 3. Presupuesto Detallado de Inversión Inicial (CAPEX)

La estructura presupuestal desglosa el costo de adquisición de hardware importado liquidado a una TRM de **$\$3.192,73\text{ COP/USD}$**, los sistemas de inspección de calidad y los honorarios profesionales e ingeniería asociada de la firma integradora.

| Ítem | Componente / Subsistema | Fabricante y Referencia | Especificaciones Técnicas | Costo (USD) | Costo (COP) | % Part. |
| :---: | :--- | :--- | :--- | :---: | :---: | :---: |
| **A** | **Hardware de Paletizado y Fuerza** | | | | | |
| 1.1 | Manipulador Robótico Industrial | Yaskawa Motoman PL80 | 4 ejes, carga máx. 80 kg, alcance 2.061 mm, muñeca IP67 apta para frío. | $\$39.500,00$ | $\$126.112.835$ | 25,62% |
| 1.2 | Gabinete Controlador de Celda | Yaskawa YRC1000 | Controlador compacto con buses de campo PROFINET y Ethernet/IP. | $\$8.000,00$ | $\$25.541.840$ | 5,19% |
| 1.3 | Teach Pendant de Operación | Yaskawa JZRCR-YPP21-1 | Consola táctil ergonómica con cable flexible apantallado de 8 m. | $\$3.200,00$ | $\$10.216.736$ | 2,08% |
| 1.4 | Mazo de Cables Extendidos | Yaskawa Kit 15 m | Potencia y encoders de 15 m para situar el gabinete fuera del cuarto frío. | $\$1.800,00$ | $\$5.746.914$ | 1,17% |
| 1.5 | Gripper (Placa de Vacío) | Schmalz FXP-440-3R36-O10-F | Placa de esponja EPDM con eyectores neumáticos multi-etapa integrados. | $\$5.800,00$ | $\$18.517.834$ | 3,76% |
| 1.6 | Brida de Acople Mecánico | Schmalz FLA-FXP-ISO-9409-1 | Acople normalizado ISO al vástago del eje 4 del manipulador PL80. | $\$450,00$ | $\$1.436.729$ | 0,29% |
| 1.7 | Compresor de Tornillo Rotativo | Atlas Copco G 7P-10 FF | 7,5 kW (10 HP), 38 CFM @ 10 bar, secador frigorífico integrado (+3°C). | $\$8.200,00$ | $\$26.180.386$ | 5,32% |
| 1.8 | Tanque Pulmón y Filtración | Vertical 500 L + Filtro UD 15+ | Acumulador 11 bar, purga automática y filtración coalescente 0,01 µm. | $\$2.050,00$ | $\$6.545.097$ | 1,33% |
| 1.9 | Transportador Infeed Motorizado | Interroll MDR Serie 24V | Rodillos RollerDrive EC5000 (2,5 m), acumulación cero presión y topes Festo. | $\$6.700,00$ | $\$21.391.291$ | 4,35% |
| 1.10 | Seguridad Física y Perimetral | Troax Smart Fix + SICK deTec4 | Cerramiento metálico h=2.050 mm, cortina óptica con muting y enclavamiento Euchner. | $\$7.550,00$ | $\$24.105.112$ | 4,90% |
| 1.11 | Tablero Eléctrico y Pasamuros | Siemens S7-1214FC + Roxtec | PLC Fail-safe, HMI KTP700 7", gabinete Rittal y pasamuros térmico hermético. | $\$8.400,00$ | $\$26.818.932$ | 5,45% |
| | **Subtotal A** | **Hardware de Paletizado y Fuerza** | | **$\$91.650,00$** | **$\$292.613.705$** | **59,45%** |
| **B** | **Inspección de Calidad en Línea** | | | | | |
| 2.1 | Báscula Dinámica (Checkweigher) | Cinta pesadora AISI 304L | Celda digital de pesaje en continuo ($\pm 0,5\text{ g}$), banda de descarte y brazo neumático. | $\$6.500,00$ | $\$20.752.745$ | 4,22% |
| 2.2 | Sistema de Visión Artificial | Cámara matricial IP67 industrial | Domo polarizado, software OCR/OCV para inspección de sellos, lote y fecha. | $\$7.500,00$ | $\$23.945.475$ | 4,87% |
| | **Subtotal B** | **Inspección de Calidad en Línea** | | **$\$14.000,00$** | **$\$44.698.220$** | **9,08%** |
| **C** | **Comercio Exterior y Aduana** | | | | | |
| 3.1 | Flete Internacional y Arancel | Nacionalización consolidada | Transporte marítimo/aéreo multimodal, seguros y arancel aduanero DIAN. | $\$1.200,00$ | $\$3.831.276$ | 0,78% |
| | **Subtotal C** | **Comercio Exterior y Aduana** | | **$\$1.200,00$** | **$\$3.831.276$** | **0,78%** |
| **D** | **Servicios de Integración** | | | | | |
| 4.1 | Ingeniería de Detalle y Planos | EPLAN / Simulación cinemática | Ingeniería eléctrica, mecánica 3D, arquitectura de seguridad ISO 10218. | $\$5.500,00$ | $\$17.560.015$ | 3,57% |
| 4.2 | Montaje Electromecánico | Obra civil y mecánica a 8°C | Canalización conduit sanitaria en acero inoxidable AISI 304 y neumática. | $\$4.000,00$ | $\$12.770.920$ | 2,59% |
| 4.3 | Programación y Software | MotoPallet + TIA Portal + Visión | Algoritmos de estibado, parametrización de visión y recetas ISA-88 en HMI. | $\$5.500,00$ | $\$17.560.015$ | 3,57% |
| 4.4 | Puesta en Marcha (FAT / SAT) | Comisionamiento y calibración | Sintonización de báscula dinámica, calibración cinemática y pruebas SAT. | $\$3.500,00$ | $\$11.174.555$ | 2,27% |
| 4.5 | Capacitación Técnica Certificada | Nivel 1 (Operación) / Nivel 2 | Formación de operarios de celda y técnicos de mantenimiento de planta. | $\$2.500,00$ | $\$7.981.825$ | 1,62% |
| 4.6 | Sueldo Ingenieros | Salario para 6 ingenieros asociados | Salario base de $\$3.500.000\text{ COP}$ para los 6 ingenieros del proyecto. | $\$26.309,77$ | $\$84.000.000$ | 17,07% |
| | **Subtotal D** | **Servicios de Integración** | | **$\$47.309,77$** | **$\$151.047.330$** | **30,69%** |
| **TOTAL** | **INVERSIÓN INICIAL ($I_0$)** | **Solución Llave en Mano** | **69,31% Activos e Instrumentación / 30,69% Integración** | **$\$154.159,77$** | **$\$492.190.531$** | **100,00%** |

---

## 4. Costos Operativos Anuales (OPEX)

Los costos operativos proyectados corresponden a un régimen de **208 días laborales al año** (4 días/semana) en un turno continuo de 8 horas diarias (**$1.664\text{ horas/año}$**):

1. **Consumo de Energía Eléctrica (36,13% del OPEX):**
   * **Potencia promedio demandada:** Robot PL80 ($1,8\text{ kW}$) + compresor Atlas Copco ciclando bajo demanda de vacío ($3,2\text{ kW}$) + rodillos e indexadores ($0,8\text{ kW}$) + báscula dinámica y visión artificial ($0,8\text{ kW}$) = **$6,60\text{ kW}$**.
   * **Consumo anual efectivo:** $1.664\text{ h/año} \times 6,60\text{ kW} = 10.982,4\text{ kWh/año}$.
   * **Tarifa media industrial regulada:** $\$850\text{ COP/kWh}$.
   * **Costo energético anual:** $10.982,4\text{ kWh} \times \$850\text{ COP} = \mathbf{\$9.335.040\text{ COP/año}}$.
2. **Consumibles de Vacío y Desgaste Mecánico (9,29% del OPEX):**
   * Repuesto semestral de la esponja EPDM Schmalz (2 recambios al año por desgaste mecánico y humedad en frío): **$\$2.400.000\text{ COP/año}$**.
3. **Mantenimiento del Sistema de Compresión de Aire (13,93% del OPEX):**
   * Kit de mantenimiento preventivo para compresor Atlas Copco (cambio de aceite sintético, elemento separador, filtros de aire y purgas): **$\$3.600.000\text{ COP/año}$**.
4. **Mantenimiento Preventivo del Robot (9,68% del OPEX):**
   * Servicio técnico anual certificado (engrase de reductores de 4 ejes con grasa apta para frío, ajuste cinemático y reemplazo de baterías de encoders): **$\$2.500.000\text{ COP/año}$**.
5. **Calibración y Certificación Metrológica (13,55% del OPEX):**
   * Calibración metrológica semestral con masas patrón certificadas, reemplazo preventivo de luminarias y limpieza de lentes ópticos: **$\$3.500.000\text{ COP/año}$**.
6. **Póliza de Soporte Técnico y Licenciamiento (17,42% del OPEX):**
   * Soporte semestral programado por la firma integradora, optimización de trayectorias, respaldo de recetas ISA-88 y soporte remoto: **$\$4.500.000\text{ COP/año}$**.

$$\mathbf{\text{OPEX Total Anual}} = 9.335.040 + 2.400.000 + 3.600.000 + 2.500.000 + 3.500.000 + 4.500.000 = \mathbf{\$25.835.040\text{ COP/año}}$$

---

## 5. Beneficios y Ahorros Anuales Estimados

Los ahorros económicos brutos reflejan los cinco pilares de eficiencia operativa proyectados en planta:

1. **Ahorro por Mitigación de Sobrepeso (*Giveaway* - Báscula Dinámica) [30,61% del ahorro]:**
   * La báscula dinámica sincronizada permite ajustar los cabezales de porcionado a una tolerancia controlada de $\pm 1\text{ g}$, recuperando un promedio de **$13\text{ g}$ ($0,013\text{ kg}$) de queso terminado por unidad**.
   * **Queso recuperado por día:** $1.911\text{ unidades/día} \times 0,013\text{ kg/unidad} = 24,843\text{ kg/día}$ ($\approx 25\text{ kg/día}$).
   * **Costo de materia prima de queso:** $\$12.500\text{ COP/kg}$.
   * **Ahorro anual ($24,843\text{ kg/día} \times \$12.500\text{ COP/kg} \times 208\text{ días/año}$):** **$\$64.591.800\text{ COP/año}$**.
2. **Supresión de Pérdidas por Fugas de Vacío y Defectos de Marcaje (Visión Artificial) [11,37% del ahorro]:**
   * Inspección automática del 100% de los envases termoformados, detectando microarrugas en la ceja de sellado, atrapamiento de grasa y defectos en la impresión de lote y fecha (OCR/OCV): **$\$24.000.000\text{ COP/año}$**.
3. **Optimización de Mano de Obra Directa (MOD) en Cuarto Frío [29,57% del ahorro]:**
   * Ahorro/reasignación de 2 operarios de estiba manual en cuarto frío a 8°C con un costo mensual consolidado por operario de $\$2.600.000\text{ COP/mes}$ (SMMLV + auxilio de transporte + 52% de factor prestacional y dotación térmica).
   * **Ahorro anual ($2\text{ operarios} \times \$2.600.000\text{ COP/mes} \times 12\text{ meses}$):** **$\$62.400.000\text{ COP/año}$**.
4. **Reducción de Mermas por Desplome y Aplastamiento de Cajas [21,33% del ahorro]:**
   * El mosaico cruzado de MotoPallet y el agarre plano de la garra Schmalz eliminan el daño mecánico en las cajas basales de 15 kg: **$\$45.000.000\text{ COP/año}$**.
5. **Disminución de Costos Ocultos por Incapacidades y Ausentismo (ARL) [7,11% del ahorro]:**
   * Erradicación de levantamiento repetitivo de cargas pesadas en ambientes fríos, reduciendo el ausentismo laboral y riesgo osteomuscular: **$\$15.000.000\text{ COP/año}$**.

### Consolidación de Márgenes Operativos

$$\text{Ahorro Bruto Anual} = 64.591.800 + 24.000.000 + 62.400.000 + 45.000.000 + 15.000.000 = \mathbf{\$210.991.800\text{ COP/año}}$$

$$\text{EBITDA Anual de la Celda} = \text{Ahorro Bruto} - \text{OPEX} = 210.991.800 - 25.835.040 = \mathbf{\$185.156.760\text{ COP/año}}\ (87,76\%)$$

---

## 6. Proyección del Flujo de Caja Libre (FCLO a 5 Años)

### Premisas Financieras y Tributarias
* **Método de Depreciación:** Línea recta a 5 años sin valor residual contable intermedio:
  $$\text{Depreciación Anual} = \frac{\$492.190.531}{5} = \mathbf{\$98.438.106\text{ COP/año}}$$
* **Impuesto sobre la Renta Corporativa:** **35%** (tarifa estatutaria vigente en Colombia).
* **Valor de Salvamento de Mercado ($V_s$):** En el año 5 se proyecta un valor de salvamento conservador equivalente a **$\$40.000.000\text{ COP}$**.

### Estado de Flujos de Efectivo Proyectado y Análisis de Descuento

| Rubro Financiero (COP) | Año 0 | Año 1 | Año 2 | Año 3 | Año 4 | Año 5 | Total Acumulado (1-5) |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Inversión Inicial ($I_0$)** | $-\$492.190.531$ | – | – | – | – | – | $-\$492.190.531$ |
| (+) Ahorros Brutos Operativos | – | $\$210.991.800$ | $\$210.991.800$ | $\$210.991.800$ | $\$210.991.800$ | $\$210.991.800$ | $\$1.054.959.000$ |
| (-) Costos Operativos (OPEX) | – | $-\$25.835.040$ | $-\$25.835.040$ | $-\$25.835.040$ | $-\$25.835.040$ | $-\$25.835.040$ | $-\$129.175.200$ |
| **(=) EBITDA** | – | **$\$185.156.760$** | **$\$185.156.760$** | **$\$185.156.760$** | **$\$185.156.760$** | **$\$185.156.760$** | **$\$925.783.800$** |
| (-) Depreciación Fiscal | – | $-\$98.438.106$ | $-\$98.438.106$ | $-\$98.438.106$ | $-\$98.438.106$ | $-\$98.438.106$ | $-\$492.190.531$ |
| **(=) Utilidad Antes de Impuestos (EBIT)** | – | **$\$86.718.654$** | **$\$86.718.654$** | **$\$86.718.654$** | **$\$86.718.654$** | **$\$86.718.654$** | **$\$433.593.270$** |
| (-) Impuesto de Renta (35%) | – | $-\$30.351.529$ | $-\$30.351.529$ | $-\$30.351.529$ | $-\$30.351.529$ | $-\$30.351.529$ | $-\$151.757.644$ |
| **(=) Utilidad Neta del Proyecto** | – | **$\$56.367.125$** | **$\$56.367.125$** | **$\$56.367.125$** | **$\$56.367.125$** | **$\$56.367.125$** | **$\$281.835.625$** |
| (+) Reversión de Depreciación | – | $+\$98.438.106$ | $+\$98.438.106$ | $+\$98.438.106$ | $+\$98.438.106$ | $+\$98.438.106$ | $+\$492.190.531$ |
| (+) Valor de Salvamento ($V_s$) | – | – | – | – | – | $+\$40.000.000$ | $+\$40.000.000$ |
| **(=) Flujo de Caja Libre (FCLO)** | **$-\$492.190.531$** | **$\$154.805.231$** | **$\$154.805.231$** | **$\$154.805.231$** | **$\$154.805.231$** | **$\$194.805.231$** | **$\$814.026.156$** |
| Factor de Descuento ($13,50\%$) | $1,0000$ | $0,8811$ | $0,7763$ | $0,6839$ | $0,6026$ | $0,5309$ | N/A |
| **Flujo Nominal Acumulado** | $-\$492.190.531$ | $-\$337.385.299$ | $-\$182.580.068$ | $-\$27.774.837$ | $+\$127.030.394$ | $+\$321.835.625$ | $+\$321.835.625$ |
| **Flujo de Caja Descontado** | $-\$492.190.531$ | $\$136.392.274$ | $\$120.169.405$ | $\$105.876.127$ | $\$93.282.932$ | $\$103.423.994$ | $\$559.144.732$ |
| **Flujo Descontado Acumulado** | $-\$492.190.531$ | $-\$355.798.256$ | $-\$235.628.852$ | $-\$129.752.725$ | $-\$36.469.793$ | **$+\$66.954.202$** | **$+\$66.954.202$** |

---

## 7. Evaluación de Indicadores Financieros

### 1. Valor Presente Neto (VPN)
Descontando los flujos futuros de efectivo a la tasa $\text{TIO} = 13,50\%\text{ E.A.}$:
$$\sum_{t=1}^{5} \frac{\text{FCLO}_t}{(1 + 0,135)^t} = 136.392.274 + 120.169.405 + 105.876.127 + 93.282.932 + 103.423.994 = \$559.144.732\text{ COP}$$
$$\text{VPN} = \$559.144.732 - \$492.190.531 = \mathbf{+\$66.954.202\text{ COP}}$$

### 2. Tasa Interna de Retorno (TIR)
Calculada igualando el VPN a cero:
$$-492.190.531 + \sum_{t=1}^{4} \frac{154.805.231}{(1 + \text{TIR})^t} + \frac{194.805.231}{(1 + \text{TIR})^5} = 0 \implies \mathbf{\text{TIR} = 18,82\%\text{ E.A.}}$$
Dado que $\text{TIR}\ (18,82\%) > \text{TIO}\ (13,50\%)$, el proyecto entrega un margen de seguridad (*spread*) de **$+5,32\text{ puntos porcentuales}$**.

### 3. Período de Recuperación (Payback)
* **Payback Simple (Nominal):**
  $$\text{Payback Simple} = \frac{492.190.531}{154.805.231} = \mathbf{3,18\text{ años}}\quad (3\text{ años y } 2\text{ meses})$$
* **Payback Descontado (al 13,50% E.A.):**
  * Saldo descontado por recuperar al cierre del Año 4: $\$36.469.793\text{ COP}$.
  * Recuperación real considerando el valor del dinero en el tiempo: **$\mathbf{4,39\text{ años}}$** ($4\text{ años y } 4\text{ meses}$).

### 4. Retorno sobre la Inversión (ROI)
* **ROI Anual sobre Flujo Neto:**
  $$\text{ROI}_{\text{Anual}} = \frac{154.805.231}{492.190.531} \times 100\% = \mathbf{31,45\%\text{ anual}}$$
* **ROI Total Acumulado (5 Años):**
  $$\text{ROI}_{\text{5 Años}} = \frac{814.026.156 - 492.190.531}{492.190.531} \times 100\% = \mathbf{65,39\%}$$

---

## 8. Matriz Consolidada de Decisión Financiera

| Parámetro / Indicador Financiero | Valor Proyectado | Unidad | Criterio de Decisión | Dictamen Financiero | Estado |
| :--- | :---: | :---: | :---: | :--- | :---: |
| **Inversión Inicial Total ($\text{CAPEX} - I_0$)** | $\$492.190.531$ | COP | Presupuesto integral | 69,31% Activos y Calidad / 30,69% Integración | **APROBADO** |
| **Inversión en Moneda Extranjera** | $\$154.159,77$ | USD | TRM: $\$3.192,73\text{ COP/USD}$ | Equipamiento importado + ingeniería local | **APROBADO** |
| **Costo Operativo Anual (OPEX Celda)** | $\$25.835.040$ | COP/año | Sostenibilidad de planta | Representa solo el 12,24% del ahorro bruto anual | **ÓPTIMO** |
| **Ahorro Bruto Anual Estimado** | $\$210.991.800$ | COP/año | Alto impacto operativo | Impulsado en 30,61% por *giveaway* y 29,57% por nómina | **ALTO IMPACTO** |
| **Margen Operativo Bruto (EBITDA)** | $\$185.156.760$ | COP/año | Margen $> 80\%$ sobre ahorro | Generación operativa neta del 87,76% | **ROBUSTO** |
| **Flujo de Caja Libre (Años 1 a 4)** | $\$154.805.231$ | COP/año | Flujo neto post-impuestos | Incluye escudo fiscal por depreciación lineal | **POSITIVO** |
| **Flujo de Caja Libre (Año 5 + $V_s$)** | $\$194.805.231$ | COP | Liquidación residual | Incluye recuperación de $\$40.000.000$ de salvamento | **POSITIVO** |
| **Tasa de Descuento (TIO / WACC)** | $13,50\%$ | % E.A. | Referencia sectorial | Costo de oportunidad ajustado al perfil de riesgo | **BASE** |
| **Suma de Flujos Descontados (1-5)** | $\$559.144.732$ | COP | $\text{VP de flujos} > I_0$ | Valor presente bruto generado por la operación | **SUPERÁVIT** |
| **Valor Presente Neto (VPN)** | **$+\$66.954.202$** | COP | $\text{VPN} > \$0\text{ COP}$ | Viable: Agrega valor neto al patrimonio de la empresa | **VIABLE** |
| **Tasa Interna de Retorno (TIR)** | **$18,82\%$** | % E.A. | $\text{TIR} > \text{TIO}\ (13,50\%)$ | Rentable: Rentabilidad robusta con $+5,32\%$ sobre la TIO | **RENTABLE** |
| **Margen de Seguridad (*Spread*)** | **$5,32\%$** | % | $\text{Spread} > 5,00\%$ | Tolera sobrecostos o alzas de tasas de hasta $5,32\text{ pp}$ | **HOLGADO** |
| **Payback Simple (Nominal)** | **$3,18$** | Años | $< 3,5\text{ años}$ | Recuperación nominal en 3 años y 2 meses | **CUMPLE** |
| **Payback Descontado (Real)** | **$4,39$** | Años | $< 4,5\text{ años}$ | Recuperación real en 4 años y 4 meses (dentro de vida fiscal) | **CUMPLE** |
| **ROI Anual Promedio** | **$31,45\%$** | % / año | $> 25,0\%\text{ anual}$ | Retorno operativo anual medio sobre capital invertido | **VIABLE** |
| **ROI Acumulado (5 Años)** | **$65,39\%$** | % (5 años) | $> 50,0\%\text{ acumulado}$ | El proyecto retorna dos terceras partes adicionales de su capital neto | **EXCELENTE** |

---

## 9. Guía de Uso de la Hoja de Cálculo (`Modelo_Financiero.xlsx`)

El libro de Excel está estructurado en **5 hojas interactivas**:
1. **`1_Parametros_y_Supuestos`**: Celdas de entrada para modificar la TRM (`B6`), días laborales al año (`B13`), horas por turno (`B14`), producción diaria (`B23`), gramos de *giveaway* recuperados (`B24`) y costo mensual por operario (`B28`).
2. **`2_CAPEX_Inversion`**: Desglose de los 20 ítems de inversión (incluyendo el ítem `4.6 Sueldo Ingenieros` por $\$84.000.000\text{ COP}$). Los montos en COP y USD están vinculados mediante la TRM de la hoja 1.
3. **`3_OPEX_y_Beneficios`**: Cálculo automatizado del gasto eléctrico anual según las horas operativas efectivas ($1.664\text{ h/año}$) y de los ahorros metrológicos y laborales, consolidando el margen EBITDA.
4. **`4_Flujo_de_Caja_y_VPN`**: Estado de Resultados proyectado a 5 años, cálculo de depreciación lineal, impuesto de renta (35%) y vectores de descuento para obtener el flujo acumulado nominal y descontado.
5. **`5_Dashboard_Ejecutivo`**: Tablero de control con las funciones financieras (`NPV`, `IRR`), dictámenes de viabilidad y gráficos comparativos de evolución de caja y composición de ahorros.