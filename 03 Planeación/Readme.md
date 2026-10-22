# Estructura de Desglose del Trabajo (EDT)

## Proyecto integrador — Automatización de Procesos de Manufactura (APM) 2026-2

---

<details>
<summary><h2>1.0. Planeación y dirección del proyecto</h2></summary>
  
### 1.1. Definición del proyecto

- [ ] **1.1.1.** Identificación del problema de ingeniería y las necesidades del cliente.
- [ ] **1.1.2.** Definición de los objetivos general y específicos.
- [ ] **1.1.3.** Definición del alcance y las limitaciones del proyecto.
- [ ] **1.1.4.** Identificación de los entregables del proyecto.

### 1.2. Planeación del trabajo

- [ ] **1.2.1.** Elaboración de la estructura de desglose del trabajo (EDT).
- [ ] **1.2.2.** Elaboración del cronograma.
- [ ] **1.2.3.** Seguimiento del avance y registro de compromisos del equipo.

</details>
<details>
<summary><h2>2.0. Análisis del proceso productivo y gestión de la producción</h2></summary>
### 2.1. Caracterización de la planta

- [ ] **2.1.1.** Identificación de las tres líneas de producción: yogures, quesos y leche UHT o bebidas lácteas.
- [ ] **2.1.2.** Identificación de maquinaria, equipos y recursos compartidos.
- [ ] **2.1.3.** Caracterización de las etapas del proceso productivo.
- [ ] **2.1.4.** Identificación de productos, referencias, materias primas y requerimientos de producción.
- [ ] **2.1.5.** Elaboración de diagramas de flujo de los procesos productivos.

### 2.2. Análisis de tiempos y capacidades

- [ ] **2.2.1.** Estimación de tiempos de proceso por operación.
- [ ] **2.2.2.** Determinación de capacidades de producción y utilización de recursos.
- [ ] **2.2.3.** Identificación de tiempos de cambio de producto, receta y formato.
- [ ] **2.2.4.** Identificación de paradas programadas y no programadas.
- [ ] **2.2.5.** Estimación de tiempos de falla y reparación para el análisis de MTBF y MTTR.

### 2.3. Análisis de la situación actual

- [ ] **2.3.1.** Elaboración del mapa de flujo de valor actual (VSM).
- [ ] **2.3.2.** Determinación del OEE y sus componentes.
- [ ] **2.3.3.** Determinación del Takt Time y Throughput.
- [ ] **2.3.4.** Determinación del MLT y la utilización de recursos.

### 2.4. Simulación y mejora de la producción

- [ ] **2.4.1.** Construcción del modelo de simulación en Siemens Tecnomatix, incorporando las tres líneas, los recursos compartidos y sus parámetros operativos.
- [ ] **2.4.2.** Ejecución de escenarios de simulación e identificación de cuellos de botella y oportunidades de mejora.
- [ ] **2.4.3.** Evaluación de escenarios de mejora, elaboración del VSM futuro y comparación de indicadores antes y después.

### 2.5. Gestión de la producción y mantenimiento

- [ ] **2.5.1.** Organización de la información requerida para la gestión de órdenes, lotes, recetas, cantidades, calidad, paradas y trazabilidad.
- [ ] **2.5.2.** Definición conceptual del intercambio de información entre producción, MES y ERP.
- [ ] **2.5.3.** Definición de estrategias de mantenimiento preventivo.
- [ ] **2.5.4.** Definición de procedimientos de mantenimiento correctivo.
- [ ] **2.5.5.** Evaluación de alternativas de mantenimiento predictivo y sus requerimientos de información y sensórica.

</details>

<details>
<summary><h2>3.0. Transformación Digital Industrial y arquitectura de automatización</h2></summary>


### 3.1. Modelado ISA-88

- [ ] **3.1.1.** Elaboración del modelo físico ISA-88.
- [ ] **3.1.2.** Elaboración del modelo procedimental ISA-88.
- [ ] **3.1.3.** Definición de recetas y referencias de producto.
- [ ] **3.1.4.** Definición de lotes, parámetros y condiciones de producción.

### 3.2. Arquitectura ISA-95

- [ ] **3.2.1.** Definición de la arquitectura integral de automatización.
- [ ] **3.2.2.** Ubicación de los sistemas de proceso, control, supervisión, gestión de producción y gestión empresarial en la arquitectura.
- [ ] **3.2.3.** Definición del flujo de información entre proceso, control, SCADA, MES y ERP, incluyendo las órdenes de producción y la información de ejecución.

### 3.3. Instrumentación y comunicaciones

- [ ] **3.3.1.** Identificación de las variables del proceso.
- [ ] **3.3.2.** Selección conceptual de sensores y actuadores.
- [ ] **3.3.3.** Definición de la arquitectura de comunicaciones requerida para la integración de equipos y sistemas.

</details>

<details>
<summary><h2>4.0. Diseño de planta, instrumentación y celda robotizada</h2></summary>


### 4.1. Distribución de planta

- [ ] **4.1.1.** Elaboración del layout general de la planta.
- [ ] **4.1.2.** Distribución de las tres líneas de producción y los recursos compartidos.
- [ ] **4.1.3.** Representación de los flujos de materiales mediante diagramas de recorrido o espagueti.

### 4.2. Diagramas técnicos de instrumentación

- [ ] **4.2.1.** Elaboración de los diagramas de tuberías e instrumentación (P&ID) correspondientes a la solución detallada.

### 4.3. Diseño de la celda robotizada

- [ ] **4.3.1.** Identificación y justificación de la operación que se robotizará.
- [ ] **4.3.2.** Diseño de la distribución de la celda y del flujo de materiales.
- [ ] **4.3.3.** Definición de los elementos de seguridad de la celda.
- [ ] **4.3.4.** Identificación de riesgos y medidas de mitigación.
- [ ] **4.3.5.** Simulación funcional de la celda en RobotStudio.

</details>

<details>
<summary><h2>5.0. Automatización, control y supervisión de la línea seleccionada</h2></summary>

### 5.1. Diseño del control secuencial

- [ ] **5.1.1.** Definición de las secuencias de operación de la línea seleccionada.
- [ ] **5.1.2.** Elaboración del GRAFCET.
- [ ] **5.1.3.** Implementación de la lógica de control en Ladder mediante Logix Emulate.
- [ ] **5.1.4.** Configuración de parámetros de producción según la receta seleccionada.
- [ ] **5.1.5.** Pruebas de la lógica de control con diferentes recetas y lotes.

### 5.2. Desarrollo del gemelo digital

- [ ] **5.2.1.** Construcción del modelo digital de la línea seleccionada.
- [ ] **5.2.2.** Incorporación de sensores y actuadores virtuales.
- [ ] **5.2.3.** Configuración de variables y secuencias del proceso.
- [ ] **5.2.4.** Integración con Logix Emulate.
- [ ] **5.2.5.** Simulación de la ejecución de diferentes lotes y recetas.

### 5.3. Sistema SCADA y HMI

- [ ] **5.3.1.** Diseño de la interfaz HMI según los principios de ISA-101.
- [ ] **5.3.2.** Configuración de la visualización de estados, variables, alarmas y tendencias.
- [ ] **5.3.3.** Visualización de la receta seleccionada y el estado del lote.
- [ ] **5.3.4.** Configuración de la comunicación OPC.
- [ ] **5.3.5.** Integración del SCADA con el gemelo digital.
- [ ] **5.3.6.** Validación funcional de la supervisión y operación del proceso.

### 5.4. Integración funcional

- [ ] **5.4.1.** Integración del modelo de proceso con el control lógico-secuencial.
- [ ] **5.4.2.** Integración del control con la supervisión SCADA.
- [ ] **5.4.3.** Validación de la interacción entre el proceso simulado, la celda robotizada y el gemelo digital.
- [ ] **5.4.4.** Registro de resultados y evidencias de las pruebas.

</details>

<details>
<summary><h2>6.0. Evaluación técnico-económica y presentación de la propuesta</h2></summary>


### 6.1. Evaluación económica

- [ ] **6.1.1.** Identificación de equipos, licencias, materiales y servicios requeridos.
- [ ] **6.1.2.** Recopilación de cotizaciones y elaboración del presupuesto.
- [ ] **6.1.3.** Estimación de costos de implementación y operación.
- [ ] **6.1.4.** Cuantificación de beneficios económicos esperados por las mejoras productivas.
- [ ] **6.1.5.** Elaboración del flujo de caja proyectado.
- [ ] **6.1.6.** Cálculo del VAN, la TIR y el periodo de recuperación de la inversión.
- [ ] **6.1.7.** Evaluación de la viabilidad financiera de la propuesta.

### 6.2. Consolidación de resultados

- [ ] **6.2.1.** Comparación de indicadores productivos de la situación actual y la propuesta.
- [ ] **6.2.2.** Elaboración del resumen ejecutivo de la solución.
- [ ] **6.2.3.** Formulación de la propuesta de valor y oferta comercial.

### 6.3. Documentación y presentación

- [ ] **6.3.1.** Organización del repositorio GitHub y sus evidencias técnicas.
- [ ] **6.3.2.** Elaboración de la página web del proyecto.
- [ ] **6.3.3.** Preparación del video de sustentación de 30 a 45 minutos.
- [ ] **6.3.4.** Documentación del trabajo en equipo y del proceso de aprendizaje.

</details>
