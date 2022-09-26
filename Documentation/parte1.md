# A brief history of Virtual Machines

El concepto de trabajar con máquinas virtuales, no es reciente, data de 1960 en mainframes de IBM. El concepto de la máquina virtual, fue creado para compartir mainframes IBM muy caras, entre múltiples empresas o organizaciones (como un método mucho más avanzado de Time-Sharing - Tiempo Compartido). Recordemos que el método de Time-Sharing original, es de compartir el tiempo de ejecución de CPU entre distintos usuarios. Pero en este caso ya no se comparte solo la CPU, si no, todos los recursos de la máquina física se particionan/reparten en cada máquina virtual. 

El problema original es el siguiente: Tenemos una máquina muy cara, que debe compartirse entre varias empresas para poder reducir el TCO(Total Cost Ownership). Se crea a nivel de hardware una capa de abstracción, donde se cargan instancias de Máquina Virtual de un Sistema Operativo, donde la empresa puede trabajar sobre el sin conocer si el mainframe está siendo compartido con otra, sin influenciarle nada el otro software que se esté ejecutando.

Actualmente, las máquinas virtuales, en los sistemas que tenemos, no se usan para usarlos como Time-Sharing con otras personas, si no que son utilizados para poder trabajar con distintos sistemas operativos disponibles en el mercado, para desarrollar productos para ellos sin tener que comprar hardware distinto.

Estas máquinas ejecutaban un sistema llamado Hipervisor (Originalmente llamado VMM - Virtual Machine Monitor), cuya función es atrapar las instrucciones que lancen los sistemas operativos desde sus máquinas virtuales, para poder ejecutarlas en el hardware real que estos no conocen. __Esto es la virtualización Tipo 1__.

## Las máquinas virtuales en sistemas x86 o AMD64.

Los sistemas que tenemos a fecha de 2022, son en su mayoría x86-64 (Mejor conocido como AMD64), estos sistemas datan de 1970, pero no fueron pensados para trabajar con Virtualización a nivel de hardware por motivos obvios, esta arquitectura de CPU originalmente, es lo que sería en su tiempo lo que hoy en día sería la de las CPU de smartphones, si quieren vender una CPU para un sistema monopuesto, no van a incluir a nivel de hardware instrucciones complejas que compliquen el diseño de una CPU pensada para ejecutar un usuario y un sistema operativo. Que haga su fabricación, mucho más cara. Como simil: No van a incluir una gráfica para juegos en un smartphone, es un desperdicio de dinero, de recursos y tendría poca utilidad para lo que normalmente se usa un smartphone, chatear, ver vídeos, etc...

¿Cómo surge la virtualización? Los sistemas x86 en 1990 evolucionaron mucho a lo que serían hoy en día, incluyeron instrucciones de SIMD que permiten ejecución de Vídeo, Imágenes, el primer 3D, ... En resumen se hicieron muy potentes a un bajo precio, entonces una empresa llamada VMware, inventa lo que sería la __virtualización Tipo 2__, porque a pesar de la potencia que iba creciendo, no tenían todavía soporte a nivel de instrucción (o hardware), de la virtualización nativa, las instrucciones que se ejecutaban en una MV, se atrapan a nivel de Aplicación y luego a continuación se pasa al Sistema Operativo.





