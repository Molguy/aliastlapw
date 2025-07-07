# Como llamar a abrir un programa EXE desde la terminal WSL 

Pasos para agregar un alias en bash de ubuntu para abrir desde la terminal WSL un programa perteneciente al diseño del sistema windows.

Para aquellos que desen abrir un porgrama de forma sencilla que no es de linux y no esten familiarizados o se esten adentrando a este tipo de trabajos en Ubuntu.


Abre la terminal escribiendo _WSL_ en el buscador de aplicaciones, o en el escritorio presiona _Shift_ + _Click Derecho_ y despues presiona **L** 

*Se usara como ejemplo el programa **Ovito** nativo para windows* 

# Paso 1

*1. Copia la ruta de la ubicacion de su programa, ejemplo:*

    C:\Program Files\OVITO Basic\ovito.exe

*2. Escribe la ruta de su porgrama entre el espacio de las comillas inglesas en esta forma:*

    alias ovitow='cmd.exe /c " "'

Valiendo la redundancia, _ovitow_ es un alias de porgrama original "Ovito", en donde se puede remplazar por cualquier otra palabra o por su mismo nombre, es a conveniencia del usuario.

# Paso 2

Escriba en la terminal de WSL:

    nano ~/.bashrc
    
A pulso de teclas direccionales, encuentra un espacio para escribir o pegar su linea completa, *ejemplo:* 

    alias ovitow='cmd.exe /c "C:\Program Files\OVITO Basic\ovito.exe"'

Para Guardar y salir presione _Control_ + **X**, presione **Y**, y _Enter_ para confirmar.

# Paso 3

_Para este paso ya deberiamos de estar fuera del editor nano y estar de vuelta en la linea de comando_

Actualize escribiendo en la terminal:

    source ~/.bashrc 

# Listo

A este punto ya puede abrir un porgrama .EXE desde la terminal en cualquier lado de WSL como si fuese un programa nativo de linux, e incluso abrir un archivo con formato compatible desde la ruta en la que se encuentre trabajando, *ejemplo:*

        ovitow dump_0.7.nvt

aclarando que _dump_0.7.nvt_ es un archivo que se puede abrir con ese porgrama y que ya se encontraba en la ruta en donde se esta trabajando.
