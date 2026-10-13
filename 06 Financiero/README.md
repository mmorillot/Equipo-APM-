# Evaluación financiera – Celda robotizada de fin de línea e inspección en línea

Estudio de factibilidad financiera para la automatización del fin de línea y el control metrológico de empaque en una planta láctea (modelo Lácteos San Mateo), con una celda 3 en 1: báscula dinámica (*checkweigher*), visión artificial y paletizado robotizado (Yaskawa Motoman PL80, gripper Schmalz FXP, compresor Atlas Copco G 7P-10 FF) dentro de la cámara de conservación a 8 °C.

- **Fecha de evaluación:** octubre de 2026
- **Horizonte:** 5 años
- **Moneda base:** COP (1 USD = 4.124,50 COP)
- **TIO (tasa de descuento):** 13,50 % E.A.

---

## 1. Corrección aplicada al presupuesto

El estudio original reportaba una inversión total de **$494.115.100 COP (USD 119.800)**, pero la suma de sus ítems da **$527.317.325 COP (USD 127.850)**, una diferencia de $33.202.225 COP. Cada ítem está bien convertido a la TRM, así que se corrigió el total. **Todos los archivos usan $527.317.325 COP.**

Si en cambio $494.115.100 fuera un presupuesto fijo, habría que recortar USD 8.050 de algún ítem y recalcular.

---

## 2. Presupuesto de inversión (CAPEX)

| Subsistema | USD | COP |
|---|---:|---:|
| A. Hardware de paletizado y fuerza | 91.650 | 378.010.425 |
| B. Inspección de calidad en línea | 14.000 | 57.743.000 |
| C. Comercio exterior y aduana | 1.200 | 4.949.400 |
| D. Servicios de integración | 21.000 | 86.614.500 |
| **Total** | **127.850** | **527.317.325** |

## 3. Costos operativos anuales (OPEX)

Régimen de 312 días al año, un turno de 8 h (2.496 h/año).

| Concepto | COP / año |
|---|---:|
| Energía eléctrica (6,6 kW × 2.496 h × $850/kWh) | 14.002.560 |
| Consumibles de vacío (esponja EPDM) | 2.400.000 |
| Mantenimiento del sistema de aire comprimido | 3.600.000 |
| Mantenimiento preventivo del robot | 2.500.000 |
| Calibración y certificación (báscula y visión) | 3.500.000 |
| Póliza de soporte técnico y licenciamiento | 4.500.000 |
| **OPEX total** | **30.502.560** |

## 4. Beneficios y ahorros anuales

| Concepto | COP / año |
|---|---:|
| Mitigación de sobrepeso (30 kg/día × $12.500/kg × 312 días) | 117.000.000 |
| Pérdidas por fugas de vacío y defectos de marcaje | 24.000.000 |
| Mano de obra directa (2 operarios × $2.600.000 × 12) | 62.400.000 |
| Mermas por desplome y aplastamiento de cajas | 45.000.000 |
| Incapacidades y ausentismo (ARL) | 15.000.000 |
| **Ahorro bruto anual** | **263.400.000** |

**EBITDA anual** = 263.400.000 − 30.502.560 = **$232.897.440**

---

## 5. Premisas del flujo de caja

- **Depreciación:** línea recta a 5 años, sin valor residual contable. $527.317.325 / 5 = **$105.463.465 por año**.
- **Impuesto de renta:** **35 %** sobre el EBIT (EBITDA − depreciación), tarifa estatutaria usada en el estudio original. Es un supuesto no contrastado con una fuente actual; si aplica otro régimen o incentivo, hay que recalcular.
- **Valor de salvamento (año 5):** $40.000.000, sin impuesto.
- **FCLO** = EBITDA − impuesto (la depreciación solo reduce el impuesto, no es un egreso de caja).

## 6. Flujo de caja libre operativo (COP)

| Rubro | Año 0 | Año 1 | Año 2 | Año 3 | Año 4 | Año 5 |
|---|---:|---:|---:|---:|---:|---:|
| Inversión inicial | -527.317.325 | – | – | – | – | – |
| Ahorros brutos | – | 263.400.000 | 263.400.000 | 263.400.000 | 263.400.000 | 263.400.000 |
| (−) OPEX | – | -30.502.560 | -30.502.560 | -30.502.560 | -30.502.560 | -30.502.560 |
| EBITDA | – | 232.897.440 | 232.897.440 | 232.897.440 | 232.897.440 | 232.897.440 |
| (−) Depreciación | – | -105.463.465 | -105.463.465 | -105.463.465 | -105.463.465 | -105.463.465 |
| EBIT | – | 127.433.975 | 127.433.975 | 127.433.975 | 127.433.975 | 127.433.975 |
| (−) Impuesto (35 %) | – | -44.601.891 | -44.601.891 | -44.601.891 | -44.601.891 | -44.601.891 |
| Utilidad neta | – | 82.832.084 | 82.832.084 | 82.832.084 | 82.832.084 | 82.832.084 |
| (+) Reversión de depreciación | – | 105.463.465 | 105.463.465 | 105.463.465 | 105.463.465 | 105.463.465 |
| (+) Valor de salvamento | – | – | – | – | – | 40.000.000 |
| **FCLO** | **-527.317.325** | **188.295.549** | **188.295.549** | **188.295.549** | **188.295.549** | **228.295.549** |
| FCLO acumulado | -527.317.325 | -339.021.776 | -150.726.227 | 37.569.322 | 225.864.871 | 454.160.420 |

## 7. Flujos descontados a la TIO (13,50 %)

| Año | FCLO | Factor 1/(1+i)^t | Flujo descontado | Acumulado descontado |
|---:|---:|---:|---:|---:|
| 0 | -527.317.325 | 1,0000 | -527.317.325 | -527.317.325 |
| 1 | 188.295.549 | 0,8811 | 165.899.162 | -361.418.163 |
| 2 | 188.295.549 | 0,7763 | 146.166.663 | -215.251.500 |
| 3 | 188.295.549 | 0,6839 | 128.781.201 | -86.470.299 |
| 4 | 188.295.549 | 0,6026 | 113.463.613 | 26.993.314 |
| 5 | 228.295.549 | 0,5309 | 121.204.330 | 148.197.644 |

---

## 8. Indicadores financieros

| Indicador | Fórmula | Resultado | Criterio | Dictamen |
|---|---|---:|---|---|
| **VPN** | Σ FCLO_t / (1+i)^t − I₀ | **+$148.197.644** | > 0 | Viable |
| **TIR** | Tasa que hace VPN = 0 | **24,29 %** | > 13,50 % | Rentable (+10,79 pp sobre la TIO) |
| **Payback simple** | Año en que el FCLO acumulado llega a I₀ | **2,80 años** (2 años y 10 meses) | < 3,0 años | Cumple |
| **Payback descontado** | Igual, con flujos descontados | **3,76 años** (3 años y 9 meses) | < 4,0 años | Cumple |
| **ROI anual** | FCLO / I₀ | **35,71 %** | – | – |
| **ROI a 5 años** | (Σ FCLO − I₀) / I₀ | **86,13 %** | > 50 % | Cumple |

### Comparación con el estudio original

| Indicador | Original ($494.115.100) | Corregido ($527.317.325) |
|---|---:|---:|
| FCLO años 1 a 4 | 185.971.393 | 188.295.549 |
| FCLO año 5 | 225.971.393 | 228.295.549 |
| VPN | +173.324.025 | +148.197.644 |
| TIR | 26,84 % | 24,29 % |
| Payback simple | 2,66 años | 2,80 años |
| Payback descontado | 3,52 años | 3,76 años |
| ROI a 5 años | 96,28 % | 86,13 % |

El FCLO sube un poco con la inversión mayor porque la depreciación más alta reduce el impuesto.

---

## 9. Gráficas

![FCLO por año](Imagenes/Finanzas/g1_fclo.png)

![Flujo acumulado nominal y descontado](Imagenes/Finanzas/g2_acumulado.png)

![Flujo con beneficios, costos y flujo neto](Imagenes/Finanzas/g3_flujo_componentes.png)

---

## 10. Conclusión

Con la inversión corregida el proyecto sigue siendo viable: VPN positivo, TIR 10,79 puntos porcentuales por encima de la TIO y recuperación de la inversión en menos de 4 años, incluso descontando los flujos. El OPEX equivale al 11,6 % del ahorro bruto anual, y el sobrepeso (44 %) y la mano de obra (24 %) explican la mayor parte del beneficio.

## 11. Limitaciones

- Los beneficios y costos provienen del estudio original y no se validaron con datos de planta.
- Los ahorros se mantienen constantes durante los 5 años, sin inflación ni crecimiento de producción.
- No se considera financiamiento: los flujos son del proyecto, sin deuda.
- La TRM se asume fija en 4.124,50 COP/USD.
- El valor de salvamento de $40.000.000 era el 8,1 % de la inversión original y con el total corregido equivale al 7,6 %; se mantuvo el monto sin cambios.
