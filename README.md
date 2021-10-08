# Notas - Automatizacion de Procesos RPA con UiPath

![](https://static.platzi.com/media/avatars/Platzi-f730e65b-e92b-44d3-81c0-5c59c4dc4658.png) ![](https://static.platzi.com/media/learningpath/badges/46.png) ![](https://static.platzi.com/media/achievements/mesa-de-trabajo-484-d124a2a2-d266-44ba-a797-6728efdc635e.png)

## Tabla de Contenidos

- [Introducción](#introducción)
  - [¿Quiénes participan en un proyecto RPA?](#quiénes-participan-en-un-proyecto-rpa)
  - [Descargar e instalar UIPath](#descargar-e-instalar-uipath) 
- [Primera automatización](#primera-automatización)
  - [Sequences and Flowcharts](#sequences-and-flowcharts)
  - [Variables y archivos XAML](#variables-y-archivos-xaml)
  - [Programar actividades: Open Application and Type Into](#programar-actividades-open-application-and-type-into)
  - [Programar actividades: Attach Windows y uso de selectores](#programar-actividades-attach-windows-y-uso-de-selectores)
  - [Descargar e instalar UIPath](#descargar-e-instalar-uipath)
  - [Descargar e instalar UIPath](#descargar-e-instalar-uipath)
  - [Descargar e instalar UIPath](#descargar-e-instalar-uipath)
  - [Descargar e instalar UIPath](#descargar-e-instalar-uipath)
  - [Descargar e instalar UIPath](#descargar-e-instalar-uipath)


# Introducción

**RPA = Robotic Process Automation**

La Automatización Robótica de Procesos es una tecnología de software que disminuye las tareas digitales repetitivas de alto volumen por medio de robots programados. Requiere que sean tareas repetitivas que consumen mucho tiempo del trabajador y que sea un proceso estandarizado por la empresa con reglas de negocio definidas.

Es una gran representación de la **4ta Revolución Industrial,** la cual estamos viviendo en la actualidad a nivel mundial.

Reglas para su uso:

- Entradas digitales.
- Proceso estandarizado.
- Proceso con reglas de negocio definidas.
- Tareas repetitivas.
- Consumen mucho tiempo.

Esta tecnología tiene muchos beneficios, algunos de estos son:

- Permite al talento de las empresas realizar otros trabajos de más valor para la organización.
- Mejoran la productividad en el flujo de trabajo haciéndola más rápida y eficiente.
- Al estar automatizado un proceso brinda seguridad y precisión en el desarrollo de las tareas, evitando una revisión permanente.
- Disminuye en gran porcentaje los costos de implementación RPA con respecto al valor del **FTE (Full Time Equivalent)** que realiza la tarea manualmente.
- Se obtiene un **ROI (Return on Investment)** mucho más rápido.
- En general las plataformas para RPA (UiPath, Automation Anywhere, Rocketbot, etc) son de uso fácil y se integran muy bien con distintas plataformas como las del paquete de Office, bases de datos, navegadores, entre otras aplicaciones de trabajo.
- Permite relacionarse con otras tecnologías como la Inteligencia Artificial para aprovechar de mejor manera la data de los procesos de la empresa.

## ¿Quiénes participan en un proyecto RPA?

Para realizar una automatización de un proceso, existen múltiples involucrados, cada uno con una función específica, así mismo hay una relación muy estrecha entre los participantes. Ya que al ser una automatización de un proceso la mayor parte del desarrollo conlleva interactuar directamente con el dueño del proceso.

Los participantes se pueden dividir en 2 grupos:

**1. Solicitante de la Automatización:**

- Infraestructura de TI.
- Soporte de TI.
- Seguridad de la Información.
- Dueño del Proceso.

**2. Equipo de Desarrollo:**

- Desarrollador RPA.
- Arquitecto RPA.
- Analista de Negocio RPA.
- Ingeniero de Infraestructura RPA.

A continuación, una breve descripción de las funciones principales de los participantes.

### Infraestructura de TI:

- Despliegan la infraestructura para los robots.
- Administran la infraestructura.
- Administran las redes de la infraestructura.
- Refrescan la información para las pruebas.
- Instalan las aplicaciones de la automatización.

### Soporte de TI:

- Administración de credenciales.
- Dar permisos de acceso.
- Monitoreo de robots y procesos.
- Atención de incidentes.
- Solucionar problemas de la Aplicación.

### Seguridad de la Información:

- Certificación de la plataforma ¿Funciona como deseamos?

### Dueño del Proceso:

- Son los solicitantes de una automatización.
- Quienes proporcionan toda la información del proceso (catálogo de datos, reglas de negocio, etc).
- Proporcionan demostración en vivo del proceso (se recomienda grabarla) al Arquitecto, Analista y Ing. de Infraestructura RPA. (muchas veces es recomendable llevar al Desarrollador a esta demostración).

### Desarrollador RPA:

- Desarrollador de la solución RPA.
- Trabaja de manera muy cercana al Analista y al Arquitecto.
- Mueve los procesos de etapa: de Desarrollo a Pruebas de Calidad cuando el desarrollo es finalizado.
- Provee asistencia nivel 1 al soporte de la aplicación durante las etapas de Prueba de Calidad.

### Arquitecto RPA:

- El encargado de definir la solución ¿Cuántos módulos crearemos por proceso? ¿Cuál será la dependencia de ejecución de estos módulos?
- Trabaja en conjunto con el Analista de Negocio.

### Analista de Negocio RPA:

- ¿El proceso deseado cumple los requerimientos para ser automatizado? ¿Cuáles son los riegos de automatizar este proceso? ¿Robots atendidos o desatendidos?

### Ingeniero de Infraestructura RPA:

- Definir la infraestructura para el robot ¿Cuántos robots necesitamos? ¿Cuántos orquestadores? ¿Equipos físicos o Servidores AWS?

## Descargar e instalar UIPath

Ahora es necesario conocer la interfaz del **IDE (entorno de desarrollo integrado),** previo a esto y el resto del curso, si se desea practicar las actividades y cumplir los retos, van a requerir instalar **UiPath Studio,** versión **Community.** Adicional se requiere que guardes tu usuario y contraseña, en temas avanzados los utilizaremos nuevamente.

Es necesario navegar a UiPath Platform y de forma automática nos redirigirá a la pantalla de autenticación, donde debemos dar en la opción de **“Sign up”** para crear una cuenta.

Una vez autenticados, entramos al portal, de lado derecho veremos la opción de **“Descargar el Studio”.**

[![1](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/1.png?raw=true "1")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/1.png?raw=true "1")

#  Primera automatización

## Sequences and Flowcharts

Sequences & Flowcharts son los nombres en inglés de los agrupadores de actividades que UiPath permite utilizar. Durante esta lectura hay ejemplos del uso de estas actividades por su nombre en español, Secuencias y Diagramas de Flujo respectivamente.

**¿Dónde se encuentran?**

Se encuentran dentro de la lista de Actividades por su nombre en inglés. (Esto es así, aunque cambies el idioma del Studio).

[![2](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/2.png?raw=true "2")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/2.png?raw=true "2") [![3](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/3.png?raw=true "3")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/3.png?raw=true "3")

**¿Cómo se usan?**

Estos contenedores, se pueden incrustar dentro del archivo del proyecto “Main.xaml” y cualquier otro archivo XAML. Los contenedores de Secuencia y Diagramas de Flujo, pueden contener dentro de ellos múltiples contenedores de Secuencias y Diagramas de Flujo.

[![4](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/4.png?raw=true "4")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/4.png?raw=true "4")

[![5](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/5.png?raw=true "5")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/5.png?raw=true "5")

Las pantallas anteriores son una pequeña demostración de cómo puedes añadir múltiples Secuencias y Diagramas de Flujo. A continuación, un ejemplo de Diagrama de Flujo que contiene múltiples Secuencias para realizar autenticación en un portal web que requiere certificados.

[![6](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/6.png?raw=true "6")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/6.png?raw=true "6")

Las secuencias del flujo anterior, contienen acciones específicas, como ejemplo podemos ver la Secuencia de Abrir e Ingresar Credenciales.

[![7](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/7.png?raw=true "7")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/7.png?raw=true "7")

**Renombrar actividades**

Para cambiar el nombre de un Diagrama de Flujo (Flowchart), una Secuencia (Sequence) o cualquier Actividad (Activity), solo deben dar doble clic sobre el nombre por defecto que se encuentra en la barra azul/gris.

Otra forma de realizar esta edición es presionar F2 con el objeto previamente seleccionado.

[![8](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/8.png?raw=true "8")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/8.png?raw=true "8")

A manera de práctica se crea estructura con la clases que se verán en el curso de la siguente manera:

[![9](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/9.png?raw=true "9")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/9.png?raw=true "9")

## Variables y archivos XAML

Una **Variable** es:

- Contenedor de información.
- Tienen alcance definido.
- Tipos específicos para cada función.

Se unen `Start` y la secuencia de `Variables` que queremos se ejecute:

[![10](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/10.png?raw=true "10")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/10.png?raw=true "10")

Dentro de `Variables` creamos objetos como `Asignar` y `Registrar mensaje` para crear las siguientes variables:

[![11](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/11.png?raw=true "11")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/11.png?raw=true "11")

> Se guarda con `Ctrl+S` y se `Depura` para verificar la Salida.

> Con `Crtl + K` se puede Establecer Variable:..

[![12](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/12.png?raw=true "12")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/12.png?raw=true "12")

Un **Archivo XAML** es: Contendor de actividades que nos permite mandar a llamar el flujo de actividades.

Se crea nueva carpeta en la principal y se agrega nuevo **EscribirHolaMundo.xaml**

[![13](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/13.png?raw=true "13")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/13.png?raw=true "13")

Se une el nuevo **XAML** con la secuencia anterior.

[![14](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/14.png?raw=true "14")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/14.png?raw=true "14")

[![15](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/15.png?raw=true "15")]([![16](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/16.png?raw=true "15")

Nueva variable **in_VarTextoEscribir** es Argumento.

Dentro de **Invoke EscribirHolaMundo** se importa argumento anterior:

[![16](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/16.png?raw=true "16")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/16.png?raw=true "16")

Se guarda con `Ctrl+S` y se depura para verificar Salida.

[![17](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/17.png?raw=true "17")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/17.png?raw=true "17")

Archivo **XAML** sirve para:

- Ordenar código.
- Segmentar funcionalidad.
- Reutilizar código / funciones.

## Programar actividades: Open Application and Type Into

`Open Application (Abrir aplicación)` Permite abrir aplicaciones.

`Type into (Escribir texto)` Permite escribir texto plano.

Para el ejercicio se reutiliza el ultimo **XAML** y se cambia nombre a **EscribirTextoEnNotePad.xaml,** se utiliza primero el objeto `Abrir Aplicación` donde se abre Notepad y se escoge en la aplicación. Luego se agrega en `Do` a el objeto `Escribir texto`, lo cual al depurar proceso muestra la salida:

[![19](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/19.png?raw=true "19")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/19.png?raw=true "19")

[![18](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/18.png?raw=true "18")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/18.png?raw=true "18")

## Programar actividades: Attach Windows y uso de selectores

**Attach Windows / Asociar ventana**

Se crea una nueva secuencia `Enfocar aplicación` y se une a al anterior `Invoke`:

[![20](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/20.png?raw=true "20")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/20.png?raw=true "20")

Dentro de la secuencia se crea `Asociar ventana` y `Escribir en`, donde se asociará una ventana de Notepad y se escribirá el nuevo mensaje desde la secuencia `Asociar Aplicación` respectivamente, adicional, se marca Campovacio a la derecha para 

[![21](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/21.png?raw=true "21")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/21.png?raw=true "21")

Al guardar y depurar muestra error por el título del Notepad que se crea en la anterior secuencia, este se cambia con el Selector de edición y se corrige la diferencia "*"

[![22](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/22.png?raw=true "22")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/22.png?raw=true "22") 

[![23](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/23.png?raw=true "23")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/23.png?raw=true "23")

Luego de **Validar** y guardar esta configuración, se depura y ejecuta correctamente:

[![24](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/24.png?raw=true "24")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/24.png?raw=true "24")

[![25](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/25.png?raw=true "25")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/25.png?raw=true "25")

# Buenas prácticas y herramientas

## Combinar actividades con código

- Lenguaje Soportado: Visual Basic
- Se está buscando integración con C# y Java
- Integración de forma nativa
- Fácil de combinar

Para empezar, se reutilizará la parte de Variables pero con unos cambios internos, se agrega las palabras “Automation, Python, Ubuntu”:

[![26](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/26.png?raw=true "26")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/26.png?raw=true "26") [![27](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/27.png?raw=true "27")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/27.png?raw=true "27")

Luego se crea nueva secuencia **Codificación** y se une a **Variables,** se crea objeto Asignar, una variable nueva `arrayPalabrasClaves` y `Registrar mensaje`, sus valores son:

`arrayPalabrasClaves `= `Split(VarTextoAEscribir, ",")`

`Mensaje` = `"Encontré " + arrayPalabrasClaves.Length().ToString + " palabras clave"`

[![28](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/28.png?raw=true "28")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/28.png?raw=true "28")[![29](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/29.png?raw=true "29")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/29.png?raw=true "29")

Esto devolverá de salida las palabras clave escritas y la cantidad de palabras.

`Split` -> Es una función para dividir texto en el caso anterior separados por “,”

`Lenght()` -> Se utiliza para saber longitud o contar lo que está en el array

`ToString` -> Para volver String o texto el resultado del Lenght

Se crea la carpeta **Archivos** y se crea archivo .txt con palabras clave, se crea variable `varCantidadArchivos` y se utilizan las siguientes entradas de código en los valores:

`varCantidadArchivos` = `Directory.GetFiles("C:\Users\andre\Desktop\Class book\Robotic process automation\CursoRPA_Platzi\Archivos", "*").Count() `

`Mensaje` = `"Encontré " + varCantidadArchivos.ToString + " archivos"`

[![30](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/30.png?raw=true "30")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/30.png?raw=true "30")

La salida correspondiente para este flujo seria la siguiente:

[![31](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/31.png?raw=true "31")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/31.png?raw=true "31")

## Modo depuración y puntos de ruptura

- Permite pausar las ejecuciones.
- Ver errores durante la ejecución.
- Mostrar ventanas complementarias.

Se activa con un clic los **Puntos de interrupción** (Doble clic para desactivar) y se selecciona la parte en donde empezará (Asignar), luego se depura el archivo y aparecerá ventana en la izquierda con la información de las Variables y propiedades:

[![32](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/32.png?raw=true "32")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/32.png?raw=true "32")

Selecciona **Entre** en para continuar con la siguiente secuencia y obtener la información relevante del paso dado, **Continuar** para que siga depurando sin detenerse.

[![33](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/33.png?raw=true "33")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/33.png?raw=true "33")

**Puntos de interrupción:** Pausa la depuración por partes donde se obtendrá ventana con información de las variables, propiedades y salidas.

**Paso lento:** Se pueden usar hasta 4 niveles de lentitud para monitorear cada paso del flujo de ejecución.

**Tasa o seguimiento de Ejecución:**  Marcar que actividades se marcan de manera correcta.

**Actividades de registro:** Va permitir ver de manera detallada y puntual que está ejecutando el robot en cada ejecución.

**Elementos destacados:** Elementos de interfaz con los que se esta interactuando.

[![34](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/34.png?raw=true "34")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/34.png?raw=true "34")

## Control de versiones Git

Para poder utilizarlo, debemos tener un proyecto existente, para esta demostración utilizaremos el proyecto generado para el curso. 

Primero cree repositorio en **GitHub** con el nombre de la carpeta del curso para poder realizar control de versión con **UiPath:**

[![35](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/35.png?raw=true "35")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/35.png?raw=true "35")

Navegaremos al menú de **INICIO** y luego al menú izquierdo que dice **Team / Equipo.**

[![36](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/36.png?raw=true  "36")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/36.png?raw=true  "36") [![37](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/37.png?raw=true  "37")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/37.png?raw=true  "37")

De lado derecho se mostrarán las opciones para integrar nuestro proyecto a un Controlador de Versiones (GIT, TFS, SVN). Para este curso usaremos en particular, el sistema de **GIT** y **GitHub.**

Vamos a realizar un `Git Init / Iniciación en Git` en nuestro proyecto, para crear el repositorio local. Para esto solo debemos dar clic en Git Init.

Se mostrará una ventana que nos dará la lista de archivos que serán incluidos en el control de versiones.

[![38](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/38.png?raw=true "38")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/38.png?raw=true "38")

Debemos colocar un mensaje de inicialización en el cuadro inferior y luego dar clic en `Commit.`

[![39](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/39.png?raw=true "39")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/39.png?raw=true "39")

Validar que **Git** se implementó con el control de versiones, para esto damos clic derecho sobre el proyecto en la pestaña de **Project.**

[![40](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/40.png?raw=true "40")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/40.png?raw=true "40") [![41](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/41.png?raw=true "41")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/41.png?raw=true "41")

Vamos a dar clic sobre `Push / Insertar` para subir nuestro proyecto al repositorio de GitHub.

[![42](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/42.png?raw=true "42")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/42.png?raw=true "42")

 > URL termina en .git

 Mensaje de confirmación de actualización:

[![43](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/43.png?raw=true "43")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/43.png?raw=true "43")

Para comparar cambios realizados podemos utilizar las siguientes opciones:

[![44](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/44.png?raw=true "44")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/44.png?raw=true "44") [![45](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/45.png?raw=true "45")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/45.png?raw=true "45")

Insertar cambios nuevos:

[![46](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/46.png?raw=true "46")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/46.png?raw=true "46") [![47](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/47.png?raw=true "47")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/47.png?raw=true "47")

## Manage Packages o Administrador de Paquetes

Es una poderosa herramienta de UiPath que nos permite buscar, instalar, actualizar o quitar **Paquetes de Actividades** de nuestro proyecto. Esto nos sirve para obtener funcionalidades oficiales o de algún desarrollador que se dio a la tarea de crear un paquete de actividades con funciones específicas.

Nuestro Administrador de Paquetes se encuentra en la pestaña de **Design:**

[![48](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/48.png?raw=true "48")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/48.png?raw=true "48")

Se pueden actualizar dependencias actuales en **Project Dependencies** e instalar nuevas en **All Packages:**

[![49](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/49.png?raw=true "49")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/47.png?raw=true "49")

[![50](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/50.png?raw=true "50")](http://https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/50.png?raw=true "50")

Se guardan los cambios y se realizarán los cambios en el proyecto:

[![51](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/51.png?raw=true "51")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/51.png?raw=true "51") [![52](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/52.png?raw=true "52")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/52.png?raw=true "52")

# Descubriendo actividades

## Leer datos de PDF e imagen

- Extraer texto de un archivo.
- Generar una imagen JPG del archivo.
- Requiere un paquete de actividades.

### Texto de PDF a Bloc de notas:

Se utiliza la actividad **Leer texto de PDF** seleccionando el archivo .pdf a utilizar, luego se invoca el **.xaml** que utilizamos para escribir en **Bloc de notas**. Para esto se crea la variable `varTextoPDF` y se configura como argumento:

[![53](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/53.png?raw=true "53")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/53.png?raw=true "53")

[![54](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/54.png?raw=true "54")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/54.png?raw=true "54")

### Leer texto de una imagen en PDF a Bloc de notas:

Para esto se utiliza la actividad **Leer PDF con OCR** (OCR es un motor que tiene la función de leer texto de imágenes, en este caso **Microsoft OCR** ) seleccionando de nuevo el archivo .pdf a utilizar, utilizamos de nuevo la variable `varTextoPDF` y se configura como argumento, luego se invoca el **.xaml** que utilizamos para escribir en Bloc de notas: 

[![55](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/55.png?raw=true "55")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/55.png?raw=true "55")

[![56](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/56.png?raw=true "56")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/56.png?raw=true "56")

Para poder **Depurarlo** tenemos que **comentar o inhabilitar** la actividad anterior **Leer texto en PDF,** esto se hace con `Ctrl + D` :

[![56](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/57.png?raw=true "56")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/56.png?raw=true "56")

### Exportar PDF como imagen:

Iniciaremos comentando las anteriores actividades para que no interfieran con el nuevo proceso, se utiliza la actividad **Exportar página en PDF** como imagen donde se selecciona el archivo .pdf, la ruta donde se alojará la imagen (Se le agrega a lo último de la ruta el nombre y la extensión deseada .jpg).  Se configura en **Propiedades** que Numero de página a utilizar y se depura:

[![58](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/58.png?raw=true "58")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/58.png?raw=true "58")

[![59](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/59.png?raw=true "59")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/59.png?raw=true "59")

## Leer imagen y registrar mensaje:

Se agrega la nueva actividad **Cargar** imagen donde se selecciona el archivo .jpg y se crea como salida la variable `varImagen` :

[![60](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/60.png?raw=true "60")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/60.png?raw=true "60")

Luego se enlaza con el motor **Microsoft OCR** donde configuramos en **Propiedades**  que de entrada sea la variable `varImagen` y de salida reutilizamos la variable `varTextoPDF` con el fin de Registrar mensaje en panel de salida:

[![61](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/61.png?raw=true "61")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/61.png?raw=true "61")

[![62](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/62.png?raw=true "62")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/62.png?raw=true "62")

## Utilizar decisiones

Hay tipos de decisiones.

- `If` -> Basado en True or False.

- `Switch` -> Basado en datos estáticos.

- `Ordenar acciones` -> Ordenar acciones.

### Si / If:

Primero para entender el ciclo **Si** se crea cuadro de entrada para preguntar edad de la persona, esta se almacenará en la nueva variable `varRespuestaUsuario` :

[![63](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/63.png?raw=true "63")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/63.png?raw=true "63")

Se agrega la actividad **Si** en donde se escribe la condición de que la variable que almacena la edad sea mayor o igual a 18, como de entrada la variable es de tipo **String** cambiamos esto a número entero con el comando `int32.Parse()` . En caso de que sea correcto **Entonces** se crea **Bandeja de Mensajes** con **Eres mayor de edad** y en caso contrario **Si no** se crea **Bandeja de Mensajes** con **Eres menor de edad.**

[![64](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/64.png?raw=true "64")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/64.png?raw=true "64")

[![65](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/65.png?raw=true "65")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/65.png?raw=true "65")

[![66](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/66.png?raw=true "66")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/66.png?raw=true "66")

[![67](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/67.png?raw=true "67")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/67.png?raw=true "67")

[![68](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/68.png?raw=true "68")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/68.png?raw=true "68")

### Cambiar / Switch:

A diferencia de **Si** esta actividad permite generar una opción **Default o de error,** junto con varias opciones de respuesta **Case** que la persona puede elegir. Utilizamos el cuadro de dialogo anterior y se agrega la actividad **Cambiar** donde se puede configurar para **Default** con todas las opciones un `LogMessage / Registrar mensaje` :

[![69](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/69.png?raw=true "69")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/69.png?raw=true "69")

[![70](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/70.png?raw=true "70")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/70.png?raw=true "70")

[![71](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/71.png?raw=true "71")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/71.png?raw=true "71")

Default:

[![72](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/72.png?raw=true "72")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/72.png?raw=true "72")

Como alternativa a este flujo tambien podemos usar las Flow decisions que funcionan de la misma manera pero resulta ser mejor visualmente, utilizando **Flow Decision** es binario y reemplaza el `Si / If` . El **Flow Switch** tiene el funcionamiento de` Cambiar / Switch` con opción Default y varios Case para utilizar:

[![73](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/73.png?raw=true "73")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/73.png?raw=true "73")

[![74](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/74.png?raw=true "74")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/74.png?raw=true "74")

## Ciclos

Existen 4 tipos de ciclos:

- `For each / Para cada` -> Exclusivo  para Listas y Arreglos.

- `For each row / Para cada fila de Tabla de datos` -> Exclusivo para DataTable.

- `While / Mientras` -> Primero verifica la condición y luego se ejecuta.

- `Do-While / Hacer mientras` -> Ejecuta y luego verifica la condición.

### For each / Para cada:

Se inicia con crear la variable `lstMensaje` la cual se le debe asignar un tipo de variable de Lista como se ve en las imágenes, y se agregan actividades **Añadir colección** para escribir en la lista un mensaje de tipo String tres veces:

[![75](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/75.png?raw=true "75")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/75.png?raw=true "75")

[![76](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/76.png?raw=true "76")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/76.png?raw=true "76")

Primero se crea mensaje para escribir la variable de tipo lista vacía, para luego insertar actividad **Para cada** dónde se establece que `itemMensaje` guardara el mensaje añadido. Entonces para cada **itemMensaje** en la lstMensaje el robot escribira en salida cada uno de los mensajes escritos en los **Anadir colección:**

[![77](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/77.png?raw=true "77")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/77.png?raw=true "77")

[![78](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/78.png?raw=true "78")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/78.png?raw=true "78")

### While / Mientras:

Se registra mensaje indicando que empieza salida de ciclo while, se asigna la nueva variable `varContador` de tipo **int32** con valor inicial a cero. Al ingresar la actividad de control **Mientras** como condición ponemos que la variable deba ser menor a 10 y que cada vez se escriba un mensaje de salida con el valor actual de la variable y luego se le sume 1.

[![79](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/79.png?raw=true "79")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/79.png?raw=true "79")

[![80](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/80.png?raw=true "80")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/80.png?raw=true "80")

[![81](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/81.png?raw=true "81")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/81.png?raw=true "81")

### Do-While / Hacer mientras:

Esta actividad funciona primero haciendo el proceso de escribir el valor de la variable, sumarle 1 a esta y después verifica que si la variable actual es menor a 20 continua a la siguiente:

[![82](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/82.png?raw=true "82")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/82.png?raw=true "82")

[![83](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/83.png?raw=true "83")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/83.png?raw=true "83")
