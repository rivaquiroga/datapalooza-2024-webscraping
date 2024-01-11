# Configuración de un entorno virtual en Visual Studio Code

## Instalaciones previas

Para utilizar Visual Studio Code como nuestro editor de código necesitamos instalar tres cosas: [Python](https://www.python.org/downloads/), [Visual Studio Code](https://code.visualstudio.com/download) y la extensión de Python en Visual Studio Code. 

## Configuración de un entorno virtual

Para trabajar en clases crearemos un _entorno virtual_. Hacemos esto para evitar conflictos entre el código que escribirmos y las distintas versiones de Python o de las librerías que vamos instalando en nuestro computador. Esto nos asegura que el código que ejecutamos en este proyecto en particular seguirá funcionando en el futuro, independiente de que actualicemos la versión de Python o que instalemos una versión más reciente de alguna librería para trabajar en otro proyecto. 


### Paso 1: Abrir nuestra carpeta de trabajo en VS Code

El entorno virtual se crea dentro de la carpeta principal de nuestro proyecto. Para ello, entonces, lo primero es tenerla abierta en VS Code. Puedes abrirla desde el explorador que está al lado izquierdo de la ventana, desde el menú **Archivo** > **Abrir carpeta**, o con el atajo `Ctrl/Cmd + K + Ctrl/Cmd + O`. 

![](img/vscode-abrir-carpeta-1.png)

### Paso 2: Buscar en la paleta de comandos la opción para crear el entorno

Puedes abrir la paleta de comandos con `Ctrl/Cmd + Shift + P` o desde el ícono :gear: abajo a la izquierda. Una vez abierta escribe "entorno" (o "environment", si es que tienes la interfaz en inglés). Elige la opción **Python: Crear entorno**.

![](img/vscode-crear-entorno.png)

### Paso 3: Selecciona el entorno

VS Code te ofrecerá dos opciones para crear el entorno: Venv y Conda. Para este ejemplo seleccionaremos Venv, que es la opción por defecto si es que instalaste Python desde <https://www.python.org>. Para ocupar la opción de crear el entorno con Conda tienes que haber instalado Conda (o miniconda) primero. Si estás en Windows e instalaste Python por primera vez con conda o miniconda, entonces elige esta opción.

![](img/vscode-seleccionar-venv.png)

### Paso 4: Seleccionar la versión de Python

Probablemente solo te aparezca una versión si tu sistema operativo es Windows y recién estás empezando a usar Python. Mac y Linux traen una versión pre-instalada, así que es probable que en ese caso te aparezcan dos versiones: la que venía en el sistema y la que instalaste tú cuando comenzaste el Diplomado. Elige la más reciente. 

![](img/vscode-seleccionar-python.png)

Si elegiste como entorno Venv y no te aparece ninguna versión de Python, intenta creando el ambiente con Conda. 

Una vez que seleccionas la versión de Python, el entorno comienza a crearse. Te aparecerá un mensaje como este en la esquina inferior izquierda de la ventana:

![](img/vscode-creando-entorno.png)

¡Listo! En el explorador deberías ver ahora un nuevo directorio dentro de tu carpeta principal que se llama `.venv` (o `.conda`, si es que elegiste esa opción).

### Paso 5: instalar librerías

Abre un nuevo terminal desde el menú **Terminal** > **Nuevo terminal**:

![](img/vscode-instalar-librerias.png)

Si te fijas, antes de la ruta de la carpeta aparece `(.venv)`, lo que nos confirma que estamos dentro del entorno virtual. Si creaste el entorno con Conda, entonces aparecerá `.conda`

Para instalar las librerías, debes escribir ahí directamente el código para hacerlo. Las que utilizamos durante el taller se instalan así: 

```
pip install beautifulsoup4
pip install requests
pip install pandas
pip install lxml
```
