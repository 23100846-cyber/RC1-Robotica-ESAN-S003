# RC-1 — Control PID: del simulador al robot real

**Universidad:** Universidad ESAN  
**Curso:** Robótica RC-1  
**Sección:** S003  
Andy vasquez Sarmiento
**Entorno:** ROS 2 Humble, Ubuntu 22.04, WSL2 y simulador YahboomCar

## Objetivo

Analizar el comportamiento de distintos controladores de movimiento mediante experimentos de seguimiento de trayectoria, giros y recorridos cuadrados, comparando la odometría y la posición real del robot.

## Evidencias del proyecto

| Parte | Descripción | Estado |
|---|---|---|
| A | Simulador, odometría y frenado | Completada |
| B - 1A | Control Bang-bang | Completada |
| B - 1B | Control proporcional | Completada |
| B - 1C | Control proporcional-derivativo | Completada |
| B - 1D | Control PID completo | Completada |
| C | Experimentos de giro de 90° | Completada |
| D | Recorrido cuadrado de 2 × 2 metros | Completada |
| E | Experimentos con robot físico | Pendiente |
| F | Consolidación de evidencias | Pendiente |

## Resultados destacados

- **Parte B - 1D:** error lateral final de 0.17 cm con Kp=3.0, Ki=0.5 y Kd=4.0.
- **Parte C:** la configuración de giro seleccionada fue Kp_yaw=10.0, Ki_yaw=0.0 y Kd_yaw=1.2.
- **Parte D:** la prueba 3C logró un cierre real promedio de 38.39 cm con ruido bajo.

## Organización

Las evidencias se incluyen en archivos ZIP independientes para cada prueba o parte. Cada paquete contiene los datos, las métricas, las gráficas y los scripts correspondientes.

## Estado actual

Las pruebas virtuales A, B, C y D están completadas. La siguiente etapa será trabajar con el robot físico y preparar la entrega final.
