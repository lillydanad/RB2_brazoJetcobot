# Reto del Brazo 2: El Turno del Brazo
**Curso:** Robótica (08079) - Universidad ESAN

## Equipo 4
* Daniela Valeria Ricapa Adrian
* Cielo Camyla Valle Cristobal
* Hugo Javier Barboza
* Italo Alejandro Navarrete Pinedo

## Descripción
Este repositorio contiene la implementación de un sistema de acceso concurrente para el JetCobot utilizando ROS 2. El objetivo principal es gestionar las peticiones simultáneas de 4 clientes hacia un único brazo robótico mediante un broker, garantizando exclusión mutua, manejando una cola de prioridades y validando la admisión mediante cinemática directa. 

## Estructura del Repositorio
* `arm_broker`: Contiene la lógica del servidor de acción, la cola de prioridades, el filtro de admisión y los nodos clientes.
* `arm_broker_interfaces`: Contiene las interfaces personalizadas necesarias para la comunicación entre los nodos.
* `evidencia`: Almacena el `ros2 bag` de las ejecuciones bajo contención, los archivos `.csv` exportados y la figura comparativa de las métricas obtenidas[cite: 2].

## Instrucciones de Ejecución

### 1. Configuración del entorno
Asegúrese de establecer el dominio de red correspondiente al robot asignado (72) y deshabilitar la restricción de localhost antes de ejecutar los nodos:
```bash
export ROS_DOMAIN_ID=72
export ROS_LOCALHOST_ONLY=0
