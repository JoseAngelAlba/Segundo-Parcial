
# 1.1 Git Commit

![Texto

1.1](https://1drv.ms/i/s!AgoFM0fcAFp6gW1ilLYP5DIzUujx?e=evTLVY)

Un commit es una copia de tus archivos en el directorio del repositorio y cuando sea necesario lo comprime entre versiones del repositorio.

# 1.2 Branch

Los Branch o ramas son referencias a un commit en específico.

Git Checkout

Checkout sirve para seleccionar un commit en especifico.

![Gráfico

1.2](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image004.png)

# 1.3 Merge

Merge crea un commit que enlaza dos ramas por lo que tiene dos padres.

![Gráfico

1.3](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

# 1.4 Rebase

Este commando copia los commits y los pega a otro lado

![Texto

1.4](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image007.png)

# 2.1 Detach

Este concepto se basa en cambiar el commit que esta seleccionado en base a un nombre clave EJ: "HEAD".

![Imagen que contiene Texto

2.1](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image009.png)

# 2.2Referencias relativas

Este commando envía hacia atrás el nombre simbólico de un commit hacia cuantas veces sea usado el operador ^.

![Forma

2.2](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image011.png)

# 2.3Referencias relativas #2

Operador ~

Este comando es igual al anterior solo que se usa el operador (~) y se le asigna el número directamente de commits que se moverá hacia atrás.

Forzar ramas

Este usa la opción -f para mover una rama x cantidad de veces atrás del nombre simbólico.

![Interfaz de usuario gráfica, Texto

2.3](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image012.png)

# 2.4Revertir cambios

Git reset

Este regresa una rama hacia el punto donde se creó un commit anterior, aunque solo funciona de manera local.

Git revert

Este crea un commit nuevo que realiza los cambios necesarios para revertir el commit y los comparte con cualquiera que este trabajando con el repositorio.

![Imagen que contiene Texto

2.4](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)

# 3.1 Cherry pick

Este copia de manera directa varios commits y los mueve a la rama que este referenciándose al momento del comando.

![Imagen que contiene Forma

Descripción generada automáticamente](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image016.png)

# 3.2 Rebase interactivo

Este commando sirve para reordenar commits y usando la opción -i te facilita una UI para seleccionar cuales commits va a ser elegidos con su orden y cuales se van a omitir, además de una opción para juntar varios commits en uno.

![Interfaz de usuario gráfica, Texto, Chat o mensaje de texto

Descripción generada automáticamente](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image017.png)

# 4.1 Unico commit.

Aquí usando los conceptos anteriores tome la rama main e hice un Cherry pick al commit C4 para mover solo ese commit.

![Imagen que contiene Forma

Descripción generada automáticamente](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image019.png)

# 4.2 Malabareando commits

![Interfaz de usuario gráfica, Texto

Descripción generada automáticamente](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png)

En este use el rebase 2 veces para copiar los 2 commits y que quedaran ambos separados como se muestra en el objetivo.

Luego del primer rebase hice un commit y le agrege la opción amend que modifica el ultimo commit seleccionado.

Y por último use un Branch para mover la rama main donde estaba la rama caption.

# 4.3 Malabareando Commits #2

![Imagen que contiene Interfaz de usuario gráfica

Descripción generada automáticamente](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image022.png)

Primero seleccione la rama main.

Luego hice un Cherry-pick para copiar el commit C2

Después un commit con un amend para que modifique el ultimo commit seleccionado.

Y otro Cherry-pick para copiar el commit C3.

# 4.4 Git Tags

![](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image024.png)

Primero le hago un tag llamado v0 al commit C1

Luego le hago un tag llamado v1 al commit C2

Y selecciono el commit C2

# 4.5 Git Describe

![Interfaz de usuario gráfica, Texto

Descripción generada automáticamente](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image025.png)

Básicamente se hizo un describe para describir las ramas main, side y bugfix.

Para finalizar el nivel se hizo un commit para completar el objetivo.

# 5.1 Rebaseando múltiples ramas

![Interfaz de usuario gráfica, Texto

Descripción generada automáticamente](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image026.png)

El primer comando es un rebase para la rama bugFix para que se copie debajo de main.

El segundo comando es para tomar todos los commits de side debajo de bugFix.

El tercer comando es para tomar todos los commits de another debajo de side.

Y por ultimo se actualiza main con un rebase.

# 5.2 Varios Padres

![Forma

Descripción generada automáticamente con confianza media](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image028.png)

En este comando uso un Branch creando la rama bugwork y le asigno la posición de el segundo padre a dos posiciones de HEAD.

# 5.3 Ensalada de branches

![Interfaz de usuario gráfica, Texto

Descripción generada automáticamente con confianza media](file:///C:/Users/jose/AppData/Local/Temp/msohtmlclip1/01/clip_image030.png)

Primero selecciono one y hago un Cherry-pick para que copie los commits C4, C3 y C2 a la rama one.

Repito lo mismo con la rama two agregándole un commit nuevo llamado C5.

Y por último hago un Branch para move a la rama three de forma forzada al commit C2.
