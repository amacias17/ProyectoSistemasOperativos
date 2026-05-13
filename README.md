# Proyecto Sistemas Operativos

## INTRODUCCIÓN

Los sistemas operativos modernos requieren mecanismos robustos de sincronización y comunicación entre procesos para resolver problemas complejos de manera concurrente. Este proyecto implementa un sistema meteorológico distribuido que demuestra el uso práctico de:

- Named pipes (FIFO) para comunicación entre procesos
- Semáforos POSIX para control de acceso a recursos compartidos
- Hilos (pthreads) para procesamiento concurrente
- Buffers circulares para almacenamiento eficiente de datos

El proyecto implementa un sistema que captura, filtra y categoriza mediciones meteorológicas de tres estaciones en Bogotá:

- Kennedy
- Usaquén
- Teusaquillo

---

# Contexto

El Instituto Distrital de Gestión de Riesgos y Cambio Climático necesita un sistema que centralice y procese datos meteorológicos de múltiples estaciones en tiempo real.

---

# Objetivos Generales

1. Implementar un sistema distribuido que demuestre el uso correcto de primitivas de sincronización en sistemas operativos.

2. Aplicar patrones de concurrencia (productor/consumidor) de forma práctica.

3. Implementar IPC mediante named pipes de forma eficiente.

---

# Objetivos Específicos

- Crear un agente (`agenteM`) que lea archivos CSV y envíe datos válidos por un pipe.

- Implementar un monitor que sincronice múltiples agentes usando buffers circulares.

- Usar semáforos POSIX para evitar *race conditions*.

- Procesar datos con hilos consumidores dedicados por estación.

- Generar un archivo consolidado y un reporte final de categorización.
