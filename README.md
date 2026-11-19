# RC-1 — Control PID: del simulador al robot real

**Universidad ESAN · Robótica 2026-2 · Sección S003**  
**Fecha de consolidación:** 18 de noviembre de 2026.  
**Estado:** laboratorio cerrado; evidencia consolidada con limitaciones documentadas, **no aprobado automáticamente**.

## Resumen medido

- **E5 — Giro real:** 87° con transportador; error físico de 3° frente a 90° (cumple el límite de ±3°).
- **E6 — Rectas:** tres corridas con CSV/ROS bag, desvíos físicos de **9, 5 y 6 cm**. Solo E6-02 cumple el límite ≤5 cm. No alterar estos valores ni sustituirlos por `e_line`.
- **E7 — Cuadrado 3A:** una corrida real completada; cierre físico informado como **aproximadamente 37 cm**; no es medición precisa verificada en fuente.
- **E7 — 3B:** corridas seleccionadas **01, 04 y 08**, cierres físicos de **25, 12 y 15 cm**; promedio **17.33 cm**. No fueron corridas consecutivas con parámetros idénticos. Existen al menos 02/03 como ensayos de ajuste (archivados). Aceptación de selección a confirmar con el docente.
- **Odómetro real:** `/odom_raw`; en simulación `/odom`; **ROS_DOMAIN_ID real: 20**.

## Organización

- `partes_virtuales/A/`, `C/`, `D/`: evidencias completas localizadas.
- `partes_virtuales/B/plots_disponibles/`: imágenes; faltan **CSV y ZIP original de B** para considerar el repositorio completamente sustentado.
- `robot_real/E5_giro/`: CSV, bag, scripts modificados; giro físico de 87°.
- `robot_real/E6_rectas/`: CSV, bags y PNG de las 3 corridas.
- `robot_real/E7_3A/`: 3A real con CSV + bag.
- `robot_real/E7_3B/`: tres corridas seleccionadas y ensayos intermedios 02/03.
- `csv/`: hoja de resultados del Anexo E, mediciones físicas, comparación simulador/robot.
- `plots/`: figuras de diagnóstico y mediciones consolidadas.
- `config/rc1_pid.yaml`: registro de ganancias por planta y corrida.
- `informe.pdf`: informe de **1 página**, con mediciones reales y límites declarados.
- `scripts_profesor/`: copia de los códigos utilizados.

## Integrantes y responsabilidades

Distribución del trabajo declarada por los integrantes:

| Integrante | Actividades realizadas |
|---|---|
| **Vásquez Sarmiento, Andy Angelo** | Desarrollo de las actividades del proyecto, incluyendo las partes virtuales **excepto 1A y 1D**, y el trabajo experimental y la preparación de evidencias del robot real. **No se le atribuye la elaboración del informe final.** |
| **Morveli Córdova, Mathias Vladimir** | Desarrollo de las actividades virtuales **1A y 1D**, y elaboración del **informe final**. |

Las etiquetas de roles de la rúbrica (integración, control, planificación y percepción) pueden registrarse por tarea en la presentación o defensa, sin adjudicar participación no informada. Los datos de autoría no modifican las mediciones ni el historial de ensayos.

## Estado de la rúbrica

- **E1-E4:** A/C/D localizadas; B necesita recuperar CSV originales para auditoría. Mantener los archivos de simulación.
- **E5:** cumple con medición física de 87° (error 3°), condicionado a aceptación de evidencia.
- **E6:** tres corridas ejecutadas, pero **no cumple plenamente** precisión ≤5 cm en dos de ellas.
- **E7:** promedio de **corridas seleccionadas** 17.33 cm, pero no consecutivas y con variación 0.10/0.09 m/s. El profesor decide si admite la selección.
- **E8:** comparativa y PNG generados; verificar que todas las pruebas virtuales cuenten con PNG y CSV de origen.
- **DEF / entrega:** preparación de defensa, publicar repositorio del grupo, agregar `README.md`, confirmar tag `v1.0-rc1`. No se realizó push ni se creó el tag desde este paquete.

## Limitaciones de calidad

1. No atribuir precisión física a los valores `/odom_raw`.
2. El desvío de E6 proviene de cinta. `e_line` es una señal de control con un desplazamiento virtual de 10 cm.
3. La nota de E7 depende de la política del docente sobre selección de corridas y reajustes; no descartar evidencias desfavorables.
4. Las fechas internas del reloj del robot pueden ser incorrectas; se preservan archivos originales sin editar tiempos.
5. Las predicciones preprueba sólo se presentan cuando aparecen explícitamente en los archivos de la Parte D/C; no se reconstruyen predicciones no guardadas.
