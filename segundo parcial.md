
# 1.1 Git Commit

![1.1](https://1drv.ms/i/s!AgoFM0fcAFp6gW1ilLYP5DIzUujx?e=evTLVY)

Un commit es una copia de tus archivos en el directorio del repositorio y cuando sea necesario lo comprime entre versiones del repositorio.

# 1.2 Branch

Los Branch o ramas son referencias a un commit en específico.

Git Checkout

Checkout sirve para seleccionar un commit en especifico.

![1.2](https://1drv.ms/i/s!AgoFM0fcAFp6gW45mzn--dIFnQFS?e=enriEu)

# 1.3 Merge

Merge crea un commit que enlaza dos ramas por lo que tiene dos padres.

![1.3](https://1drv.ms/i/s!AgoFM0fcAFp6gW8lTG2Vzl0mMndV?e=W7C3gA)

# 1.4 Rebase

Este commando copia los commits y los pega a otro lado

![1.4](https://1drv.ms/i/s!AgoFM0fcAFp6gW8lTG2Vzl0mMndV?e=W7C3gA)

# 2.1 Detach

Este concepto se basa en cambiar el commit que esta seleccionado en base a un nombre clave EJ: "HEAD".

![2.1](https://1drv.ms/i/s!AgoFM0fcAFp6gXE4iwvPSJgP_Y_M?e=MVqIML)

# 2.2Referencias relativas

Este commando envía hacia atrás el nombre simbólico de un commit hacia cuantas veces sea usado el operador ^.

![2.2](https://1drv.ms/i/s!AgoFM0fcAFp6gXJ2QAwpOL5OpmrU?e=8JvLH7)

# 2.3Referencias relativas #2

Operador ~

Este comando es igual al anterior solo que se usa el operador (~) y se le asigna el número directamente de commits que se moverá hacia atrás.

Forzar ramas

Este usa la opción -f para mover una rama x cantidad de veces atrás del nombre simbólico.

![2.3](https://1drv.ms/i/s!AgoFM0fcAFp6gXN9MHlgwG4co_WY?e=JkuXoh)

# 2.4Revertir cambios

Git reset

Este regresa una rama hacia el punto donde se creó un commit anterior, aunque solo funciona de manera local.

Git revert

Este crea un commit nuevo que realiza los cambios necesarios para revertir el commit y los comparte con cualquiera que este trabajando con el repositorio.

![2.4](https://1drv.ms/i/s!AgoFM0fcAFp6gXT1xBk115zxhQFW?e=zbBTLt)

# 3.1 Cherry pick

Este copia de manera directa varios commits y los mueve a la rama que este referenciándose al momento del comando.

![3.1](https://1drv.ms/i/s!AgoFM0fcAFp6gXVau9OBzSmhmO2L?e=lOUCgi)

# 3.2 Rebase interactivo

Este commando sirve para reordenar commits y usando la opción -i te facilita una UI para seleccionar cuales commits va a ser elegidos con su orden y cuales se van a omitir, además de una opción para juntar varios commits en uno.

![3.2](https://1drv.ms/i/s!AgoFM0fcAFp6gXbpLIr-xYxoVXBh?e=VjeVnG)

# 4.1 Unico commit.

Aquí usando los conceptos anteriores tome la rama main e hice un Cherry pick al commit C4 para mover solo ese commit.

![4.1](https://1drv.ms/i/s!AgoFM0fcAFp6gXeGhJk9xbnYm3Vg?e=uIJflH)

# 4.2 Malabareando commits

![4.2](https://1drv.ms/i/s!AgoFM0fcAFp6gXhD1S9721NA8QpT?e=agrd3Y)

En este use el rebase 2 veces para copiar los 2 commits y que quedaran ambos separados como se muestra en el objetivo.

Luego del primer rebase hice un commit y le agrege la opción amend que modifica el ultimo commit seleccionado.

Y por último use un Branch para mover la rama main donde estaba la rama caption.

# 4.3 Malabareando Commits #2

![4.3](https://1drv.ms/i/s!AgoFM0fcAFp6gXmjlRyLdtE25r2I?e=yddreT)

Primero seleccione la rama main.

Luego hice un Cherry-pick para copiar el commit C2

Después un commit con un amend para que modifique el ultimo commit seleccionado.

Y otro Cherry-pick para copiar el commit C3.

# 4.4 Git Tags

![4.4](https://1drv.ms/i/s!AgoFM0fcAFp6gXrdHHKBUTvAlnUq?e=pySQbD)

Primero le hago un tag llamado v0 al commit C1

Luego le hago un tag llamado v1 al commit C2

Y selecciono el commit C2

# 4.5 Git Describe

![4.5](https://1drv.ms/i/s!AgoFM0fcAFp6gXt4USyJsgLp0tWv?e=2v6MLx)

Básicamente se hizo un describe para describir las ramas main, side y bugfix.

Para finalizar el nivel se hizo un commit para completar el objetivo.

# 5.1 Rebaseando múltiples ramas

![5.1](https://1drv.ms/i/s!AgoFM0fcAFp6gXzJJHj6sv3D6G8B?e=l2gP39)

El primer comando es un rebase para la rama bugFix para que se copie debajo de main.

El segundo comando es para tomar todos los commits de side debajo de bugFix.

El tercer comando es para tomar todos los commits de another debajo de side.

Y por ultimo se actualiza main con un rebase.

# 5.2 Varios Padres

![5.2](https://1drv.ms/i/s!AgoFM0fcAFp6gX2iwRY6f5ixpMgi?e=UwLr0t)

En este comando uso un Branch creando la rama bugwork y le asigno la posición de el segundo padre a dos posiciones de HEAD.

# 5.3 Ensalada de branches

![5.3](https://1drv.ms/i/s!AgoFM0fcAFp6gX5mtM-9V7Y310Rw?e=BtyLMz)

Primero selecciono one y hago un Cherry-pick para que copie los commits C4, C3 y C2 a la rama one.

Repito lo mismo con la rama two agregándole un commit nuevo llamado C5.

Y por último hago un Branch para move a la rama three de forma forzada al commit C2.
