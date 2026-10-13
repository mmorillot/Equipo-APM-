<div align="center">
  <h1>Gestión y Evaluación de la Producción</h1>
  <h3><i>Línea de Quesos Frescos (Pasta Hilada) — OwlTech Automation</i></h3>
</div>

---

## 🎯 Objetivo del Módulo
Este documento consolida el análisis operativo de la línea de quesos frescos. A través de la aplicación de herramientas de manufactura esbelta (*Lean Manufacturing*) y simulación de eventos discretos (Siemens Tecnomatix Plant Simulation), evaluamos el desempeño actual del sistema productivo, identificamos restricciones (cuellos de botella) y cuantificamos el impacto técnico-económico de nuestra propuesta de Transformación Digital Industrial.

---

## 1. Parámetros Operativos y de Producción

El modelo se basa en un esquema de producción por lotes ("días de campaña") con una asignación específica de materia prima.

### 1.1 Capacidad y Demanda Diaria
* **Materia prima diaria:** 4.200 L/día (equivalente a 105 cantinas).
* **Rendimiento quesero:** 10% (Se requieren 10 L de leche para obtener 1 kg de queso de masa base).
* **Masa base disponible:** 420 kg/día.
* **Tiempo Disponible de Turno ($T_D$):** 480 minutos - 30 minutos (inactividad planeada) = **450 minutos/día**.

Con la masa base de 420 kg, la demanda diaria ($D$) varía según la referencia a producir en la campaña:
* **Mozzarella (250 g):** 1.680 unidades/día.
* **Quesillo (300 g):** 1.400 unidades/día.
* **Siete Cueros (200 g):** 2.100 unidades/día.

### 1.2 Cálculo de Takt Time y Cuello de Botella
Tomando como base la producción de la **Referencia 1 (Mozzarella)**:

$$Takt = \frac{T_D}{D} = \frac{450 \text{ min}}{1680 \text{ und}} = 0.267 \text{ min/und (16 segundos)}$$

**Análisis de Restricciones:**
1. **Coagulación (Proceso Batch):** La tina quesera procesa el lote en 35 minutos. 
   * $T_c \text{ Coagulación} = 35 \text{ min} / 1680 \text{ und} = 0.02 \text{ min/und}$.
2. **Empaque (Proceso Discreto):** La empacadora opera a un ritmo de 10 unidades por minuto.
   * $T_c \text{ Empaque} = 0.10 \text{ min/und}$ (6 segundos).

**Conclusión:** Dado que $T_c \text{ Empaque} (0.10) < Takt Time (0.267)$, la línea cuenta con la capacidad instalada para absorber la demanda. El cuello de botella en el flujo discreto es la empacadora, pero el sistema general está condicionado a la liberación del lote en la etapa de coagulación.

---

## 2. Análisis de Manufactura Esbelta (Lean)

Para visualizar el flujo de materiales e información, y eliminar los desperdicios (*Mudas*), desarrollamos los siguientes diagramas.

### 2.1 Diagrama de Operaciones de Proceso (DOP)
Mapeo de la secuencia lógica de manufactura utilizando simbología estándar ASME. Se ilustra la entrada de leche, las adiciones (cuajo, fermentos) y el balance de masa (extracción de lactosuero).

<div align="center">
  <!-- Reemplaza la ruta con la ubicación real de tu imagen -->
  <img src="Images/Diagrama_de_operaciones_de_proceso.png" alt="Diagrama de Operaciones de Proceso" width="800"/>
  <p><i>Figura 1: Flow Process Chart de la línea de Quesos Frescos.</i></p>
</div>

### 2.2 Diagrama de Espagueti (Spaghetti Diagram)
Representación del flujo físico de materiales y personas sobre el Layout de la planta. 

<div align="center">
  <!-- Reemplaza la ruta con la ubicación real de tu imagen -->
  <img src="./img/espagueti_actual.png" alt="Diagrama de Espagueti Antes" width="400"/>
  <img src="./img/espagueti_futuro.png" alt="Diagrama de Espagueti Después" width="400"/>
  <p><i>Figura 2: Optimización de rutas (Antes vs. Después) para reducción de transportes.</i></p>
</div>

### 2.3 Value Stream Mapping (VSM)
El VSM contrasta el tiempo de valor agregado frente al Lead Time total.

**Estado Actual (Push):** Evidencia altos niveles de inventario en proceso (WIP) debido a tiempos de espera manuales en la medición de pH y formatos de papel.
<div align="center">
  <!-- Reemplaza la ruta con la ubicación real de tu imagen -->
  <img src="./img/vsm_actual.png" alt="VSM Actual" width="800"/>
</div>

**Estado Futuro (Pull + Automatización):** Propuesta con sensores en línea (pH ISFET), integración a SCADA/MES y control automatizado de la hiladora.
<div align="center">
  <!-- Reemplaza la ruta con la ubicación real de tu imagen -->
  <img src="./img/vsm_futuro.png" alt="VSM Futuro" width="800"/>
</div>

---

## 3. Indicadores de Desempeño (KPIs)

La automatización de la planta está diseñada para impactar directamente en las siguientes métricas:

* **OEE (Overall Equipment Effectiveness):** $Disponibilidad \times Eficiencia \times Calidad$. 
  La implementación del sistema SCADA/MES reduce los tiempos inactivos no planeados y garantiza un control estricto del pH de hilado (5.1 para Mozzarella, 4.9 para Quesillo), disminuyendo drásticamente la tasa de rechazo.
* **MLT (Manufacturing Lead Time):** 
  $$MLT = Tsu_{max} + \sum (Tc_i + Tno_i) + (Q-1)Tc_n$$
  Calculado en 183 minutos para el lote diario de Mozzarella. La automatización del lavado (CIP) mediante secuencias Grafcet reduce el $Tsu_{max}$ (Setup).

---

## 4. Simulación de Eventos Discretos (Tecnomatix)

Para validar nuestra propuesta, se construyó un Gemelo Digital del proceso utilizando **Siemens Tecnomatix Plant Simulation**. El modelo emula la transición entre el flujo continuo (leche), el procesamiento por lotes (tinas) y la salida discreta (bloques de queso).

### 4.1 Modelo del Sistema
Se modeló la recepción (4.200 L) mediante objetos `Source`, el tratamiento térmico en `ParallelProc`, la acumulación de lotes en `Buffer` y las operaciones secuenciales con `SingleProc`.

<div align="center">
  <!-- Reemplaza la ruta con la ubicación real de tu imagen -->
  <img src="./img/plant_simulation_layout.png" alt="Layout en Plant Simulation" width="800"/>
  <p><i>Figura 3: Entorno de simulación de la línea en Tecnomatix.</i></p>
</div>

### 4.2 Resultados y Dashboard Comparativo
El experimento de simulación compara el rendimiento de la planta con control manual vs. control automatizado (TDI).

<div align="center">
  <!-- Reemplaza la ruta con la ubicación real de tu imagen -->
  <img src="./img/dashboard_tecnomatix.png" alt="Dashboard de Resultados" width="800"/>
  <p><i>Figura 4: Estadísticas de utilización, Throughput y OEE extraídas del modelo.</i></p>
</div>

**Conclusiones de la Simulación:**
* La automatización de los parámetros térmicos en la hiladora elimina el cuello de botella virtual generado por paradas no programadas.
* El *Throughput* simulado alcanza las metas establecidas por el Takt Time, garantizando el cumplimiento de la orden de producción del ERP.**
