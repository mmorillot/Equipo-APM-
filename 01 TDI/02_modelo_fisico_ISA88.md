# Modelo físico ISA-88 · Línea de quesos
Jerarquía: Área → Celda → Unidad → Módulo de equipo (EM) → Módulo de control (CM).
Los tags son propuestos y se confirman con el P&ID.

## Estructura
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

Las áreas de yogures (A2) y UHT (A4) se reservan en la numeración, sin detalle.

## Módulos de equipo y de control
| Unidad | Módulos de equipo | Módulos de control |
|---|---|---|
| UN-301 Marmita | Calentamiento (vapor), llenado/vaciado | TE-301 PT100, LT-301 nivel, FV-301 válvula de vapor |
| UN-302 Tina | Camisa térmica; liras de corte y agitación; dosificación de cuajo y CaCl₂; llenado/vaciado | TE-302 PT100, AT-302 firmeza, AT-303 pH, FIT-302 caudal, LT-302 nivel, FV-302 vapor, FV-303 agua helada, M-302 variador de liras, PU-302 bomba lobular |
| UN-303 Hiladora | Calentamiento de agua; tornillos de amasado | TE-304 agua, TE-305 pasta, AT-304 pH ISFET, M-303 variador, FV-304 calentamiento |
| UN-304 Moldeadora | Rodillos de moldeo | ZS-304 conteo, M-304 motor |
| UN-305 Salmuera | Enfriamiento, manipulador de jaulas | TE-306 temperatura, LT-306 nivel, M-305 grúa |
| UN-306 Empacadora | Vacío, sellado, codificador de lote | PT-306 vacío, TE-307 temperatura de sello, ZS-306 conteo óptico, XA-306 detector de metales |
| UN-307 Lactosuero | Transferencia a silo | LT-307 nivel, PU-307 bomba |
