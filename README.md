# Priority Scheduler

Este script permite controlar la ejecución de los scripts en entornos de procesado de datos. Cuenta con estas funcionalidades:
- Evita las doble ejecuciones: Con la opción --lock evita que un script se pueda ejecutar más de una vez al mismo tiempo.
- Permite definir la prioridad: Con la opción --priority permite configurar la prioridad del comando que se va a ejecutar. Siendo 0 el menos prioritario y 2 el más prioritario.
- Puede asignar timeouts a los comandos ejecutados: Con la opción --timeout podemos lanzar un comando con un tiempo máximo de ejecución.
- Permite denegar nuevas ejecuciones cuando el equipo está cargado: Con la opción --load podemos establecer un umbral de carga de CPU para que, cuando el equipo supere ese umbral, no permita nuevas ejecuciones.


<h2>Usar ./prisch [params] -c "comando"</h2>


    -l / --lock        Evitar dobles ejecuciones
    -L / --load        Abortar ejecucion si la sonda supera una determinada carga
    -t / --timeout     Establecer un timeout. Si se supera se mata el proceso
    -p / --priority    Establece una prioridad. Va desde 0 (minima prioridad) hasta 2 (maxima prioridad)
    -v / --verbose     Informacion extendida
    -h / --help        Ayuda
