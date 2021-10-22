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
- [Buenas prácticas y herramientas](#buenas-prácticas-y-herramientas)
  - [Combinar actividades con código](#combinar-actividades-con-código)
  - [Modo depuración y puntos de ruptura](#modo-depuración-y-puntos-de-ruptura)
  - [Control de versiones Git](#control-de-versiones-git)
  - [Manage Packages o Administrador de Paquetes](#manage-packages-o-administrador-de-paquetes)
- [Descubriendo actividades](#descubriendo-actividades)
  - [Leer datos de PDF e imagen](#leer-datos-de-pdf-e-imagen)
    - [Texto de PDF a Bloc de notas](#texto-de-pdf-a-bloc-de-notas)
    - [Leer texto de una imagen en PDF a Bloc de notas](#leer-texto-de-una-imagen-en-pdf-a-bloc-de-notas)
    - [Exportar PDF como imagen](#exportar-pdf-como-imagen)
    - [Leer imagen y registrar mensaje](#leer-imagen-y-registrar-mensaje)
  - [Utilizar decisiones](#utilizar-decisiones)
    - [Si / If](#si--if)
    - [Cambiar / Switch](#cambiar--switch) 
  - [Ciclos](#ciclos)
    - [For each / Para cada](#for-each--para-cada)
    - [While / Mientras](#while--mientras)
    - [Do-While / Hacer mientras](#do-while--hacer-mientras)
  - [Interacción con navegador web](#interacción-con-navegador-web)
  - [Extraer datos con Data Scrapting](#extraer-datos-con-data-scrapting)
  - [Manejar DataTable](#manejar-datatable)
  - [Interactuar con Excel](#interactuar-con-excel)
  - [Configuración Gmail](#configuración-gmail)
  - [Interactuar con Correo](#interactuar-con-correo)
- [Robotic Enterprise Framework – REF](#robotic-enterprise-framework--ref)
  - [Introducción REF](#introducción-ref)
  - [Conocer el Orquestador](#conocer-el-orquestador)
  - [Analizar el archivo Config](#analizar-el-archivo-config)
  - [Sincronizar robot con Orchestrator](#sincronizar-robot-con-orchestrator)
  - [Creación de colas](#creación-de-colas)
  - [Crear un Asset en el Orquestador](#crear-un-asset-en-el-orquestador)
  - [Inicialización del proyecto REF](#inicialización-del-proyecto-ref)
  - [Etapa de procesamiento de datos](#etapa-de-procesamiento-de-datos)
  - [Finalizando nuestro proyecto REF](#finalizando-nuestro-proyecto-ref)
- [Arquitectura de Software](#arquitectura-de-software)
  - [Proyecto final](#proyecto-final)
  - [Arquitectura para los proyectos](#arquitectura-para-los-proyectos)
    - [1. Solución estándar](#1-solución-estándar)
    - [2. Solución de Alta Disponibilidad](#2-solución-de-alta-disponibilidad)
  - [La arquitectura de nuestro proyecto](#la-arquitectura-de-nuestro-proyecto)
  - [Modulando un proceso Automatizado](#modulando-un-proceso-automatizado)
  - [Solución del proyecto final](#solución-del-proyecto-final)
  - [Centro de Excelencia](#centro-de-excelencia)
  
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

## Interacción con navegador web

- Uso muy frecuente.
- Requiere plugin complementario.
- Selectores.
- Extracción de datos
- Interacción con interfaz.

Entrando en **Herramientas** se puede descargar Plugin del navegador que utilizamos, se confirma **extensión** dentro de este y se puede verificar en chrome://extensions/

[![84](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/84.png "84")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/84.png "84")

Se utiliza actividad **Abrir navegador** donde se configura en Propiedades el **BrowserType** y escribimos como parámetro “google.com”. Dentro irá una secuencia `Do / Hacer` la actividad Ir a donde buscará en el navegador elegido hacia la dirección “platzi.com”:

[![85](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/85.png "85")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/85.png "85")

Después de Ir a “platzi.com” utilizamos la función **Clic** para seleccionar la secuencia para iniciar la sesión.

[![86](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/86.png "86")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/86.png "86")

Se crean variables `inUsuario` e `inContraseña` (Contiene String con user y password) para el ejercicio y se utilizan en las actividades **Escribir** en para autenticar en la pagina.

Luego al probar esta secuencia `Do / Hacer` damos clic derecho y la **Extraemos como flujo de trabajo,** un .xaml que podremos usar en cualquier momento para Autenticar en Platzi:

[![87](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/87.png "87")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/87.png "87")

Al correr la secuencia se rompe debido al error que no se seleccionó el browser en la secuencia de **Hacer,** entonces se selecciona como salida de **Abrir navegador** la nueva variable `BrowserAbierto` y en la entrada de la actividad **Ir a** se pone como navegador el argumento `in_Browser` . Esto con el fin de enlazar la entrada a Chrome y la búsqueda de la página de Platzi:

[![88](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/88.png "88")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/88.png "88")

[![89](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/89.png "89")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/89.png "89")

Como argumentos dentro del flujo de trabajo se configuran de la siguiente manera para que corra el robot:

[![90](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/90.png "90")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/90.png "90")

> Con la anterior configuración ya debe funcionar el robot y dejar la sesión iniciada. Pero, ¿Qué pasa cuando la sesión ya estaba iniciada?

Para esto cortaremos el Ir a “platzi.com” del flujo de trabajo **AutenticarEnPlatzi** y lo pegaremos en el inicio ante del flujo que invocamos. Esto lo convertirá en una secuencia la cual enlazaremos con la salida de **Abrir navegador** , por lo que de entrada en el **Navegador** pondremos la variable `BrowserAbierto.`

[![91](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/91.png "91")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/91.png "91")

Se agrega **Elemento existente** con el fin de validar un objeto en la interfaz en este caso es el contador de puntos de Platzi, clic derecho y damos en **Selector de edición:**

[![92](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/92.png "92")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/92.png "92")

En la ventana emergente damos en **Indicar elemento** y seleccionamos el contador de puntos en la página Google que se abrió la sesión Platzi. A continuación, se configura la edición de texto de la siguiente manera para que seleccione con la expresión * xxx que significa todo lo que contenga la siguiente expresión xxx. Se valida y se aceptan los cambios realizados.

[![93](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/93.png "93")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/93.png "93") 

[![94](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/94.png "94")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/94.png "94")

Ahora requerimos crear una variable llamada `varBanderaAutenticacion` en las propiedades de salida, la cual nos servirá como condición en el siguiente paso:

[![95](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/95.png "95")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/95.png "95")

Se agrega actividad de control **Si** donde evalúa que, si es correcto que hay valores en el contador de puntos en Platzi registra mensaje de “La sesión ya está abierta”, si no realiza el workflow para autenticar usuario y contraseña:

[![96](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/96.png "96")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/96.png "96")

Salida donde verificó que estaba abierta la sesión:

[![97](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/97.png "97")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/97.png "97")

Salida para cuando llega a opción de utilizar workflow:

[![98](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/98.png "98")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/98.png "98")

## Extraer datos con Data Scrapting

- Leer datos estructurados.
- Guardar datos de un DataTable.
- Altamente organizada.
- Patrón predecible.

Ya con la ventana abierta en el buscador de Platzi sobre los cursos de **Python** seleccionamos la opción de `Extracción de datos` , lo cual traerá esta ventana para configurar:

[![99](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/99.png "99")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/99.png "99")

Se selecciona **Sig.** y elegimos el primer elemento o primer curso en este caso, después nos pedirá elegir el siguiente dato o curso para identificarlos en la **Data Table.** Permite configurar las columnas que se extraerán donde se elige las opciones de `Extraer texto` y `Extraer URL` (Para este momento ya aparecen subrayados todos los datos elegidos).

[![100](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/100.png "100")]([![101](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/101.png "101")

Se da una vista previa de esa tabla con todos los datos extraídos de la página en la que estamos trabajando con o sin límite y también pregunta si la selección de datos aplica para otra página (En este caso NO).

[![101](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/101.png "101")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/101.png "101")

[![102](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/102.png "102")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/102.png "102")

Se corta la actividad de **Extraer datos estructurados "URL"** y se organiza después del **Ir a** como se ve en la imagen, como dato de salida creamos la variable `dtCursosEncontrados` que guarde los datos y se realiza el mensaje con los comandos `.Rows.Count.ToString` para que nos arroje la cantidad de datos obtenidos (100):

[![103](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/103.png "103")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/103.png "103")

## Manejar DataTable

Organizar información.

Interacción de datos mediante filas y comlumnas.

Se unen en actividades como:

- Consulta a Base de Datos.

- Lectura de Exceles.

- Almacenar información estructurada.

Como primer paso configuramos la variable `dtCursosEncontrados` para que la podamos ver en todo el ejercicio:

[![104](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/104.png "104")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/104.png "104")

Agregamos secuencia de Tabla de datos donde se utiliza la actividad **Para cada fila de la tabla de datos,** para cada `row/fila` en la variable que nos guarda los datos extraídos nos va a imprimir de salida el nombre de cada uno de los Cursos que están en la columna **NombreCurso.**

[![105](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/105.png "105")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/105.png "105") [![106](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/106.png "106")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/106.png "106")

Ahora utilizaremos la actividad **Agregar columna de datos** para la cual creamos **EstatusCurso** donde dirá el estado actual del curso ejem. “Pendiente”:

[![107](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/107.png "107")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/107.png "107")

Seguido de esto utilizaremos de nuevo actividad **Para cada fila de la tabla de datos** para que en cada fila se asigne un “Pendiente”. Como mensaje de salida configuramos el nombre y el estado con los siguientes comandos: `CurrentRow(0).ToString + " - " + CurrentRow("EstatusCurso").ToString`

[![108](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/108.png "108")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/108.png "108") [![109](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/109.png "109")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/109.png "109")

Ahora comentamos los anteriores **Registrar mensajes** para que nos permita visualizar mejor la salida. Vamos a trabajar con la actividad **Tabla de datos de salida** para extraer la información en texto plano separando columnas por comas. En esta se crea la variable `varTextodelDT` que nos almacenará todo el texto de la Data Table.

[![110](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/110.png "110")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/110.png "110")

## Interactuar con Excel

- Leer Exceles.
- Guardar en Excel en DataTable.
- Escribir en Excel.
- Eliminar filas.
- Insertar filas.
- Entre otras acciones.

Primero se trabajará sobre leer un data table y escribir su contenido en una hoja de Excel. Se abre la actividad **Ámbito de aplicación de Excel** la cual nos permite hacer algo con un archivo .xlsx de acuerdo a su ruta. Al final de la ruta se escribe el nombre del nuevo archivo `\CursoPlatzi.xlsx`

[![111](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/111.png "111")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/111.png "111")

[![112](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/112.png "112")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/112.png "112")

Dentro de la secuencia de hacer se utiliza actividad **Escribir rango** donde se especifica el nombre de la primera hoja y la celda donde empezar. La variable de entrada v`arCursosEncontrados` era donde en la secuencia Tabla de datos guardamos toda la información en un data table.

[![113](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/113.png "113")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/113.png "113")

Al revisar el archivo Excel que se creó se puede evidenciar como organizó el data table en la primera hoja del nuevo Excel y cada columna con su encabezado correspondiente.

[![114](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/114.png "114")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/114.png "114")

Ahora, vamos a leer el archivo Excel y vamos a extraer la información en una variable para mostrar en salida. Para esto cambiamos la dirección en que se ejecutará el flujo, comentamos el **Ámbito de aplicación de Excel** anterior y agregamos uno nuevo. Dentro de la secuencia hacer agregamos actividad **Leer rango** especificando la hoja y la celda (Si se deja “” leerá toda la hoja). Como variable de salida recolectamos la info en `dtCursosEncontrados.`

[![115](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/115.png "115")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/115.png "115")

[![116](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/116.png "116")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/116.png "116")

Luego ponemos la **Tabla de datos de salida** para que tome la información del data table `dtCursosEncontrados` y la almacene en la variable `varTextoAEscribir` . Luego con un mensaje realizamos la salida.

[![117](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/117.png "117")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/117.png "117")

[![118](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/118.png "118")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/118.png "118")

También podemos leer una celda con actividad **Leer celda.** De igual manera se puede explorar todas las actividades que se pueden utilizar al escribir Excel.

## Configuración Gmail

Primero navegamos a Administración de Cuenta de Google ( https://myaccount.google.com )

[![119](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/119.png "119")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/119.png "119")

Pantalla principal de Administración de Cuenta de Google.

Luego en el menú de Seguridad, ubicado de lado izquierdo de la pantalla, damos clic.

[![120](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/120.png "120")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/120.png "120")

Una vez en la sección de Seguridad debemos modificar lo siguiente:

[![121](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/121.png "121")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/121.png "121")

Desactivar la autenticación por teléfono y la verificación de 2 pasos.

[![122](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/122.png "122")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/122.png "122")

Activar el acceso de aplicaciones menos seguras.
Con estos pasos cubiertos, Gmail permitirá que UiPath interactúe con la bandeja de entrada y salida (para recibir y enviar correos).

## Interactuar con Correo

- Comunicación (del robot).
- Leer correos.
- Enviar correos nuevos o responder anteriores.
- Guardar archivos adjuntos.

Primero se probará el envío de mensajes por correo para lo cual utilizaremos actividad **Enviar mensaje de correo SMTP** (System Mail Transfer Protocol). Para esto requerimos configurar el puerto a **465** y el servidor **smtp.gmail.com,** también llenar la información de correo y contraseña de donde saldrá el mensaje.

[![123](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/123.png "123")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/123.png "123")

[![124](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/124.png "124")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/124.png "124")

Ahora, vamos a obtener mensajes no leídos en el correo que tenemos. Para esto vamos a utilizar actividad **Obtener mensajes de correo IMAP** (Internet Message Access Protocol), configurando el puerto a **993** y el servidor imap.gmail.com, también llenar la información de correo y contraseña de donde saldrá el mensaje.

[![125](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/125.png "125")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/125.png "125")

[![126](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/126.png "126")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/126.png "126")

También debemos configurar en propiedades las opciones **Arriba** para saber cuántos correos como máximo queremos traer, habilitar `SoloMensajesNoLeidos` y creamos en salida la variable de tipo lista `lstCorreosEncontrados` para que almacene la info extraída. Se agrega mensaje con el comando `"Correos encontrados: " + lstCorreosEncontrados.Count.ToString` para cuente los correos y de respuesta a manera de String.

[![127](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/127.png "127")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/127.png "127")

Sin embargo, queremos verificar que la información que trajo es correcta así que vamos a imprimir mensaje por cada uno de los correos, con la información del título, cuerpo y fecha. Para facilidad de lectura configure para que solo traiga 5 correos.

Para esto traemos la actividad **Paralelo Para cada,** donde para cada ítem “Correo” en nuestra lista `lstCorreosEncontrados` va registrando el mensaje: `Correo.Subject + Environment.NewLine + Correo.Body + Environment.NewLine + Correo.Headers("Date")`

- `Environment.NewLine` = Salto de línea

Para que nos reconozca la variable de lista de correos tenemos que cambiar el tipo de argumento a `System.Net.Mail.MailMessage` :

[![128](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/128.png "128")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/128.png "128")

[![129](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/129.png "129")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/129.png "129")

[![130](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/130.png "130")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/130.png "130")

Como ejemplo de responder mensajes traemos la actividad **Enviar mensaje de correo SMTP** que habíamos hecho y la editamos para responder, se configura en propiedades la opción **Avanzar: MensajeDeCorreo** con el ítem **Correo** para cada mensaje se enviará una respuesta con un archivo adjunto:

[![131](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/131.png "131")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/131.png "131")

[![132](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/132.png "132")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/132.png "132")

[![133](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/133.png "133")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/133.png "133")

# Robotic Enterprise Framework – REF

## Introducción REF

¿Que hemos aprendido?

- Que son los selectores.
- Interactuar con aplicaciones y páginas web.
- Conexión a Base de Datos.
- Manejo de Correos.

REF

- Robotic Enterprise Framework.
- Plantilla de proyecto.
- Integrada a Orquestador.
- Basada en estados.
- Basado en als mejores práticas.

Framework = Entorno de trabajo

Para crear un Proyecto en REF debemos abrir Studio y elegir la plantilla REF.

[![134](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/134.png "134")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/134.png "134")

Proporcionamos el nombre del proyecto, la ruta donde lo vamos a almacenar y opcionalmente una descripción de para qué es este proyecto.

[![135](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/135.png "135")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/135.png "135")

Al abrir el proyecto se verá de la siguiente forma.

[![136](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/136.png "136")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/136.png "136")

#### Estructura del Proyecto
El proyecto cuenta con 3 partes importantes, veamos una introducción a ellas:

**Cuadro Verde:**

El proyecto REF contiene una carpeta Data que es la carpeta que el Framework recomienda para colocar los archivos de entrada (input), salida (output), temporales (temp) y el archivo Config.xlsx (el cual analizaremos la próxima clase).

**Cuadro Amarillo:**

Es una carpeta con el nombre Framework, contiene los archivos XAML recomendados cómo los mínimos requeridos en el Framework.
Estos archivos son una recomendación, algunos son requeridos y otros son opcionales, todo depende del tipo de implementación que generarán.

**Cuadro Rojo:**

El archivo **Main.XAML** que ya conocemos, para esta versión en el Framework, es una máquina de estados, lo que nos muestra en su diseño es la máquina de estados completa con sus 4 estados.

- Initialization (Inicialización): En este estado o fase, realizamos la configuración previa para nuestro proceso, abrir páginas web, abrir programas, iniciar sesión en donde se requiera, leer archivos como el Config, Assets, etc).

- Get Transaction Data (Obtener datos de transacción): Esta es el segundo estado o fase, aquí obtendremos un registro de la cola del Orquestador, asignamos ese registro a nuestra variable de transacción y pasamos a Process Transaction, si no hay más datos para transaccionar procedemos a navegar a End Process.

- Process Transaction (Procesar transacción): Esta es el tercer estado o fase, aquí realizamos las tareas que requiere el proceso, validar reglas de negocio, navegar a ciertos sitios, insertar los datos en algún sistema, generar archivos, etc.

- End Process (Finalizar proceso): El último estado o fase, aquí realizamos un cierre de todas las aplicaciones que abrimos. De ser requerido, realizamos la notificación por correo con un resumen de lo realizado. Dependiendo de sus proyectos, también es la etapa donde hacemos un cambio de estado dentro de la base de datos operativos.

#### Comunicación entre estados

REF al ser una máquina de estados, se validan parámetros para identificar cual es el próximo paso a ejecutar.
En el caso de REF, en la primera transición es de Inicialización hacía “A o B”, donde:

– A) Finalizar Proceso
– B) Obtener datos.

La pregunta es ¿Cómo sabe a dónde ir?

Para descubrirlo, podemos dar clic en cualquiera de los 2 campos marcados en Rojo.

Pantalla del REF_1

[![137](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/137.png "137")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/137.png "137")

[![138](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/138.png "138")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/138.png "138")

Al hacer el doble clic, se mostrará la vista de Transición del Estado Iniciación.

En la pantalla con los detalles de Transición veremos las reglas de transición en base a validación de datos; en el caso de **Inicialización** se valida la variable SystemException, existiendo 2 casos de validación:

1. Succesful: para indicar qué fue satisfactoria la iniciación, se valida que SystemException no contenga valores, ya que esta variable aloja los errores detectados durante la ejecución. Al no haber errores, se cumple la condición y envía ejecuta la siguiente transición: Obtener Datos (Get Transaction Data).

2. System Exception (Failed): en el caso de que SystemException tenga valor, la validación de condición de Transición para System Exception (Failed) se vuelve verdadera, por lo que redirige el proceso a su estado de Finalizar Proceso (End Process).

[![139](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/139.png "139")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/139.png "139")

Si hacemos clic en cualquiera de los 2 campos marcados en Rojo veremos las validaciones de transacción de Obtener Datos.

[![140](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/140.png "140")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/140.png "140")

Al hacer el doble clic, se mostrará la vista de Transición del Estado Obtener datos de Transacción.

En la pantalla con los detalles de Transición veremos las reglas de transición en base a validación de datos; en el caso de Obtener Datos se valida la variable TransactionItem, existiendo 2 casos de validación:

1. New Transaction: para indicar que fue satisfactoria la obtención de datos, se valida que TransactionItem contenga valores, ya que esta variable aloja la información que trataremos en el Procesado. Al existir información, se cumple la condición y envía ejecuta la siguiente transición: Procesar Transacción (Process Transaction).

2. No Data: en el caso de que TransactionItem no tenga valores, la validación de condición de Transición para No Data se vuelve verdadera, por lo que redirige el proceso a su estado de Finalizar Proceso (End Process).

[![141](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/141.png "141")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/141.png "141")

Si hacemos clic en cualquiera de los 2 campos marcados en Rojo veremos las validaciones de transacción de Procesar Transacción.

[![142](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/142.png "142")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/142.png "142")

Al hacer el doble clic, se mostrará la vista de Transición del Estado Procesar Transacción.

En la pantalla con los detalles de Transición veremos las reglas de transición en base a validación de datos; en el caso de Procesar Transacción se validan 2 variables SystemException y BusinessException:

1. Success: para indicar que el procesamiento de los datos de la transacción fue correcto, se valida que SystemException y BussinesException no contengan valores, de ser así, se detona el SetTransactionStatus.xaml y colocamos el registro en el Orquestador como Finalizado (Success); posteriormente viajamos al Obtener Datos (Get Transaction Data) para solicitar un nuevo registro.

2. Business Rule Exception: cuando la variable BussinesException contiene valores, significa que durante el procesamiento de la información no se cumplió una regla de negocio (ej. El valor de un monto a pagar es superior al permitido por el sistema.). De ser este el caso que nos ocurra, se detona el SetTransactionStatus.xaml y colocamos el registro en el Orquestador como Error (Error); posteriormente viajamos al Obtener Datos (Get Transaction Data) para solicitar un nuevo registro.

3. System Exception: cuando la variable SystemException contiene valores, significa que durante el procesamiento de la información hubo un error en el sistema que no es derivado de una regla de negocio, (ej. El sitio web donde registramos la información cambió de visible a 404 not found) (ej2. Cambiaron las credenciales del correo, no fueron actualizadas en el Asset del Robot y esto no permite la comunicación con la descarga/envío de correos).

[![143](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/143.png "143")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/143.png "143")

[![144](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/144.png "144")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/144.png "144")

[![145](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/145.png "145")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/145.png "145")

Así mismo, posterior a la ejecución del proceso se Ejecuta el XAML llamado SetTransactionStatus.xaml.

[![146](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/146.png "146")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/146.png "146")

En dicho flujo de trabajo tenemos distintas acciones según los resultados de nuestro Process Transaction.

SetTransactionStatus.XAML contiene 3 flujos para las 3 posibles situaciones que se mencionaron anteriormente en el Procesado de la Transacción, Success, Business Rules Exception y System Error.

Por lo general, este XAML no lo modificamos, a menos que sea una situación muy particular, pero es importante conocer cómo funciona.
Este flujo realiza en el registro del orquestador (el TransactionItem) que procesamos un cambio de estado, siendo Successful o Failed según la situación. Veamos cómo se hace.

Primero el flujo pregunta (en la Decisión “Success”) “¿BusinessException y SystemException contienen información?” si estas variables no contienen valor, navegamos a la Secuencia de Success.

Si la pregunta anterior es positiva, alguna de las variables tiene valores, preguntamos “¿BussinesException tiene valor?” si se determina que es correcto, el flujo se mueve a la Secuencia de “Business Exception”, en caso de que BussinesException no contenga valores navegamos a la Secuencia de SystemException.

[![147](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/147.png "147")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/147.png "147")

[![148](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/148.png "148")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/148.png "148") [![149](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/149.png "149")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/149.png "149")

Una vez que comprendimos cómo se decide cual es la situación resultante, veamos un poco qué acciones realiza cada Secuencia, en general realizan la misma acción, pero cambian los datos que escriben.

La siguiente pantalla es la Secuencia de Success, se realiza un *Set Transaction Status con la Propiedad de Status en Successful.

[![150](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/150.png "150")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/150.png "150")

La siguiente pantalla es la Secuencia de Business Exception, se realiza un *Set Transaction Status con la Propiedad de Status en Failed y el ErrorType como Business.

[![151](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/151.png "151")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/151.png "151")

La siguiente pantalla es la Secuencia de System Exception, se realiza un *Set Transaction Status con la Propiedad de Status en Failed y el ErrorType como Application.

[![152](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/152.png "152")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/152.png "152")

Con esto finalizamos la lectura acerca de REF, en la siguiente clase veremos cómo se configura el archivo Config.xlsx y cómo el robot lo lee (en el estado de Inicialización) y cómo lo consumimos en nuestro proyecto.

## Conocer el Orquestador

Una vez autenticados en la página navegamos a Services y verificamos que exista un Servicio.

[![154](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/154.png "154")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/154.png "154")

Esperamos a que cargue y nos encontraremos en la vista principal del Orquestador.

Antes de comenzar con las funciones técnicas del Orquestador, vamos a navegar a la sección de My Profile, para esto damos clic en el icono superior derecho con nuestras siglas. Aquí se mostrará una pantalla con sus datos, Selector de Temas y lenguaje.

[![155](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/155.png "155")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/155.png "155")

#### Los menús y sus funciones

El orquestador contiene muchas funcionalidades, algunas de ellas son nuevas, liberadas en las nuevas actualizaciones.

[![156](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/156.png "156")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/156.png "156")

- Robots: aquí podemos monitorear los Robots que tengamos registrados, su estado (conectado o no, disponible u ocupado). No se preocupen si no ven Robots en su Orquestador, los configuraremos la próxima video clase.

- Las Carpetas (Folders): antes eran llamadas Tenants, estas cumplen la función de separar información para distintos roles. Por ejemplo, puedes crear una Carpeta con Robots exclusivos para el área de Recursos Humanos y otra carpeta exclusiva para los Robots del área de Finanzas y Pagos.
Damos clic en Añadir Carpeta
Se mostrará una ventana, donde debemos colocar el nombre de la Carpeta. El tipo de carpeta indica cómo obtendrá los robots y datos para su funcionamiento, por recomendación la mejor opción es clásica, ya que así solo se añade lo que deseamos y no hereda nada de otra Carpeta. Esto nos permite un control puntual de que hay en cada carpeta.

[![157](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/157.png "157")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/157.png "157")

- Usuarios (Users): aquí podremos administrar los Usuarios que pueden acceder a nuestro Orquestador y nuestras Carpetas.

- Roles: donde podemos Editar los permisos de los Roles o Añadir Roles (dando clic en el signo de más (+)).
- Según los roles que configures puedes crear usuarios para personal administrativo que no tengan permiso de modificar Assets (así te proteges de alteraciones no controladas).

- Robots, aquí podemos monitorear los Robots que tengamos registrados, su estado (conectado o no, disponible u ocupado). También cuenta con una pestaña llamada Entorno (Environments), donde podemos añadir Entornos de Trabajo (Realizaremos la configuración en la próxima clase).

- Máquinas (Machine): en esta sección se registran Equipos virtuales basados en nuestro nombre de Equipo físico, esto nos proporcionará una Machine Key que usaremos para vincular el Orquestador con el Robot de nuestro PC, esto lo realizaremos en la próxima vídeo clase.

- Paquetes (Packages): en este apartado, se muestran los proyectos que cargamos a orquestador sea desde el estudio o manualmente (haremos carga de proyectos más adelanta cuando finalicemos el desarrollo).

Ahora les explicaré el grupo de 	, en este grupo están contempladas las funciones usadas para hacer funcionar un proceso automatizado desde el Orquestador (que va de la mano con algunas de las funciones vistas en Administración).

[![158](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/158.png "158")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/158.png "158")

- Procesos(Process): en esta sección, creamos un registro de proceso, donde se asignar el Paquete que cargamos al Orquestador y este es Proceso es el que usamos para crear trabajos. En las siguientes clases veremos a fondo cómo crear el proceso, vincularlo a los paquetes y probarlos en el Robot.

- Colas (Queue): Aquí podemos ver las colas existentes y crearlas, ver los registros de las transacciones que tienen. En las siguientes clases veremos a fondo cómo crear la cola que usaremos en nuestro proyecto.

- Desencadenadores (Triggers): anteriormente se llamaba Programación (Schedule), Aquí realizaremos configuraciones para que un proceso se ejecute en el horario deseado las veces deseadas (ej. Todos los días a las 19 hrs, ejecuta el Proceso 1). Una nueva funcionalidad en el Orquestador que detonó el cambio del nombre, es la sección de Detonación por Cola, que solicita la ejecución de un Proceso cuando una Cola en particular reciba nuevos registros.

- Variables globales (Assets): la última de las pantallas a explicar, pero no por ello la menos importante, de hecho, todo lo contrario, una de las más importantes y utilizadas.
 
La función principal de esta sección es crear variables o recursos que el Robot consumirá durante su ejecución. Estos recursos o Assets pueden ser modificados en cualquier momento, teniendo en cuenta que afectará al Robot hasta su siguiente ejecución (que los leerá de nuevo).

Aquí podemos añadir y editar Assets, que son de distintos tipos. Los campos en rojo son requeridos. Los demás campos son opcionales. En las siguientes clases configuraremos todos los Assets que usaremos durante nuestro Proyecto REF.

[![159](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/159.png "159")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/159.png "159")

El tipo de Valor Global significa que el valor colocado en este Asset será el que leerán todos los Robots, si desactivamos este marcador, el Asset va a requerir que se proporcione el Robot que lo puede consumir y el valor que dicho Robot recibirá.

Esto es práctico cuando por ejemplo cada Robot fuera a usar una credencial distinta para el mismo sistema.

## Analizar el archivo Config

La clase pasada creamos un proyecto REF, en su estructura de proyectos vimos que había un archivo llamado Config.xlsx, un Excel.

[![160](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/160.png "160")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/160.png "160")

### Estructura del archivo

Nuestro Config de Excel, cuenta con 3 hojas y 3 columnas en cada hoja, las hojas son las siguientes:

**Settings:** Esta hoja se utiliza para colocar valores de configuración que por lo general no cambian una vez definidos, por ejemplo, nombre de archivos a generar, rutas de archivos, páginas web de sistemas a utilizar (más adelante configuraremos algunos valores para ejemplificar mejor); esta hoja contiene las 3 columnas siguientes:

- Name: Colocamos aquí el nombre con el que llamaremos en código el valor contenido en Value.
- Value: Colocamos aquí el valor que se proporcionará al código al ser llamado.
- Description: Una breve descripción acerca del nombre y el valor del registro.

**Constants:** Esta sección contiene variables constantes, generalmente se utiliza para colocar nombre de Logs, contadores de reintentos y funciones similares.

- Name: Colocamos aquí el nombre con el que llamaremos en código el valor contenido en Value.
- Value: Colocamos aquí el valor que se proporcionará al código al ser llamado.
- Description: Una breve descripción acerca del nombre y el valor del registro.

**Assets:** Esta hoja se utiliza para colocar valores de configuración que pueden cambiar y afectan al robot directamente, por ejemplo, credenciales, rutas dinámicas, correos destinatarios, etc (más adelante configuraremos algunos valores para ejemplificar mejor); esta hoja contiene las 3 columnas siguientes:

- Name: Colocamos aquí el nombre con el que llamaremos en código el nombre del Asset.
- Asset: Es el nombre del Asset como está registrado en el Orquestador.
- Description: Una breve descripción acerca del Nombre y el Asset del registro.

### Configurando variables en el archivo

A continuación, te mostraré la lista de valores en Setting y en Assets, que serán las configuraciones que usaremos en el desarrollo del proyecto REF en las siguientes clases.

### Replicarlas en tu archivo

Para Settings deben añadir todas las variables del cuadro rojo y modificar los valores de las 2 variables preexistentes.

[![161](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/161.png "161")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/161.png "161")

Para Constants Modificar los campos en rojo, para el segundo campo, tengan en cuenta que la ruta que yo coloqué es la ruta donde está mi proyecto guardado.

[![162](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/162.png "162")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/162.png "162")

Para Assets Añadir los siguientes registros. Estos en la clase siguiente los vamos a crear en el Orquestador.

[![163](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/163.png "163")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/163.png "163")

### ¿Cómo leemos el Config en el Proyecto REF?

Dentro de nuestro proyecto REF, en el estado de Inicialización, tenemos una validación de si el archivo de Config es vacío. Cuando ésta condición se cumple, se ejecutará entre las múltiples acciones un XAML llamado InitAllSettings.

[![164](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/164.png "164")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/164.png "164")

Dentro de InitAllSettings.xaml tenemos las siguientes acciones:

- Assing out_Config, la función de esta asignación es inicializar el diccionario de datos.

[![165](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/165.png "165")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/165.png "165")

- For Each Configuration Sheet, aquí se realiza una lectura de todos los datos encontrados en la hoja Setting y Constants.
Primero en el Read Range activity se leen las hojas Settings y Constants.
Luego en el foreach row interno, leemos cada registro de las hojas leídas y guardamos en el diccionario “out_Config” la llave (que corresponde a la columna Name) y el valor (que corresponde a la columna Value).

[![166](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/166.png "166")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/166.png "166")

- Try Initializing Assets, En esta secuencia, se realiza una lectura de la hoja de Assets.
Primero en el Read Range activity se lee la hoja Assets.
Luego en el foreach row interno, leemos cada registro de las hojas leídas, posteriormente en el Get Orchestrator Asset, consultamos en el Orquestador el Asset que escribimos en la columna Asset.
Guardamos en el diccionario “out_Config” la llave (que corresponde a la columna Name) y el valor (que viene del Asset que leímos el paso anterior).

[![167](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/167.png "167")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/167.png "167")

### ¿Cómo utilizar los datos leídos?

Hasta ahora, hemos creado los registros en el archivo Config y hemos aprendido como el Robot los lee, pero nos falta saber utilizar los datos que el robot leyó y guardó en el diccionario llamado “config”.

Para leer los valores de nuestro diccionario debemos invocar la variable Config, abrir paréntesis, colocar entre comillas la palabra clave que registramos en la columna Name y añadir al final un `.ToString`

`Config(“<PalabraClave>”).ToString`

En la siguiente pantalla podemos ver como se invoca el Config (cuadros rojos) y el resultado (cuadros amarillos).

[![168](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/168.png "168")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/168.png "168")

## Sincronizar robot con Orchestrator

Requerimientos para sincronizar:

- Machine key
- URL Orquestador
- Datos del ordenador (Usuario y contraseña)
- UiPath Studio instalado y cuenta

Se utilizó este tutorial como guía para el desarrollo de la sincronización:

🤖 Unattended Robots in Uipath Orchestrator (Full Tutorial)
https://www.youtube.com/watch?v=5ixkFVEPCAU 

El nombre de la máquina que se está usando se puede conseguir en **Preferences / Orchestrator settings del UiPath Assistant.**

[![169](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/169.png "169")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/169.png "169")

Dentro del perfil del usuario Inquilino se crea la máquina con su respectivo nombre. Se deja sin ninguna de las licencias de tiempo de ejecución.

[![170](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/170.png "170")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/170.png "170")

En nuestro UiPath Studio dentro del **Main** del proyecto REF que se trabaja, se busca la opción de **Publicar:**

[![171](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/171.png "171")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/171.png "171")

Se nombra el paquete en su primera versión 1.0.1 y se procede a publicar la información.

[![172](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/172.png "172")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/172.png "172")

En el **Orchestrator** dentro de la pestaña **Usuarios** se puede visualizar el correo relacionado con el nombre de usuario, seleccionamos opciones y **Editar.**

[![173](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/173.png "173")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/173.png "173")

En la pestaña de **Ajustes de usuario** seleccionamos **Allow to be Automation user (Permitir ser usuario de automatización).**

[![174](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/174.png "174")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/174.png "174")

En la segunda pestaña **Robot desatendido** se habilita la opción de **Crear automáticamente robot desatendido,** el nombre de dominio de usuario se obtiene en la terminal de Windows escribiendo “whoami”. Se introduce una contraseña y dejan las demás opciones como están, luego se Actualiza la información de usuario.

[![175](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/175.png "175")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/175.png "175")

Al revisar en la pestaña de **Robots** se observa el robot desatendido recién creado y ligado con nuestro usuario.

[![176](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/176.png "176")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/176.png "176")

## Creación de colas

Las colas se utilizan para organizar las transacciones a ejecutar.

Dentro de la carpeta principal **PlatziTenant** se busca la pestaña Colas y se crea una nueva, con una descripción y las opciones que tiene para añadir:

[![177](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/177.png "177")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/177.png "177")

Al regresar al **Assistant** en el **Orchestrator settings** se agrega la información restante, la URL del Orchestrator está en el link como muestra la imagen:

[![178](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/178.png "178")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/178.png "178")

La **Machine key (Llave de la máquina)** se puede copiar de la pestaña de Máquinas en el portapapeles:

[![179](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/179.png "179")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/179.png "179")

Una vez llena la información se puede conectar y licenciar con nuestro **Orchestrator.**

[![180](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/180.png "180")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/180.png "180")

### Crear un Asset en el Orquestador

- Contenedores de datos.
- Pueden ser manipulados.
- Proporciónan información al Robot.

Para crear estos activos se debe ingresar en la carpeta principal **PlatziTenant** y en la pestaña de **Variables globales** se crea una nueva. De acuerdo con nuestro archivo **Config.xlsx** podemos ingresar el nombre de cada Asset empezando con la primera **RutaCarpetaInsumos** donde están los archivos de entrada del proceso, esta variable es de tipo Texto y se habilita como Variable Global. La ruta la encontramos por medio de **Orchestrator** en la carpeta **Data / Input:**

[![181](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/181.png "181")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/181.png "181")

Se realiza el mismo procedimiento con el activo **RutaCarpetaSalida** la ruta de la carpeta sería **Data / Output.**

Para el Asset de **EnviarCorreoA** se pone como texto la dirección de correo del destinatario:

[![182](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/182.png "182")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/182.png "182")

Hace falta otro activo que nos de las credenciales necesarias para poder identificarse, ingresar y enviar el correo necesario. Este activo **AssetCredencialCorreos** de tipo Credencial permite ingresar la dirección de correo y contraseña del remitente.

[![183](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/183.png "183")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/183.png "183")

Al final del ejercicio se pueden evidenciar los cuatro Assets con su respectiva información y valor:

[![184](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/184.png "184")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/184.png "184")

Dentro del Studio se debe configurar las credenciales con el proceso:

[![185](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/185.png "185")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/185.png "185")

## Inicialización del proyecto REF

Actividades del Proyecto: 

- Inicialización: Leer archivo y crear lista de palabras.
- Procesar Transacción: Leer palabra clave y registrar en Excel.
- Finalizar Proceso: Enviar generado por correo.

Para la Inicialización del proyecto REF entramos en el proceso de **Initialization** y abrimos el flujo de trabajo de iniciar el proceso:

[![186](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/186.png "186")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/186.png "186")

Una vez dentro se empieza a configurar un Log Message como Trace para informar que se ha iniciado a leer el texto, luego se agrega actividad Leer archivo de texto y se escribe el siguiente código para mostrar donde y que se está leyendo:

`in_Config("RutaCarpetaInsumos").ToString+"\"+in_Config("NombreArchivoInsumo").ToString`

Se crea la variable tipo String de salida `varTextoLeido` para almacenar todo lo que se esta procesando.

[![187](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/187.png "187")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/187.png "187")

Se agrega la actividad **Asignar** donde se crea un Array de palabras clave `arrayPalabrasClave` el cual se debe poner como tipo de variable `System.String[]`

Su valor será el comando `Split(varTextoLeido, ",")` para organizar cada palabra leída en el Array delimitadas por comas. Para esto el archivo de texto dentro de la carpeta `Data / Input` se modifica para contener las palabras a leer delimitadas.

[![188](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/188.png "188")](https://raw.githubusercontent.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/main/img/188.png "188")

Seguido de esto se agrega la actividad Paralelo Para cada dónde para cada ítem en el `arrayPalabrasClave` se realiza lo que contiene su body. Para este se agrega actividad **Añadir elemento de la cola** y se configura su NombreDeCola con el código `in_Config("OrchestratorQueueName").ToString`

[![189](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/189.png?raw=true "189")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/189.png?raw=true "189")

Antes de **Añadir elemento de la cola** se agrega otra actividad de Asignar donde se crea variable `varContador` que se encargará de sumar 1 cada vez que se lea un ítem del Array. En la InformaciónDeElemento se configura de la siguiente manera las variables de entrada de **PalabrasClave** y **Fila,** de tipo String y Número entero respectivamente con su valor:

[![190](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/190.png?raw=true "190")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/190.png?raw=true "190")

Para no generar error se configura la actividad **Paralelo Para cada** con el fin de que el Tipo de argumento de entrada es un String:

[![191](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/191.png?raw=true "191")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/191.png?raw=true "191")

## Etapa de procesamiento de datos

Dentro del proceso **Process Transaction** abrimos el flujo de trabajo que se observa:

[![192](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/192.png?raw=true "192")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/192.png?raw=true "192")

[![193](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/193.png?raw=true "193")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/193.png?raw=true "193")

Se agrega actividad **Ámbito de aplicación de Excel** para trabajar con el software y se escribe el código `in_Config("RutaCarpetaSalida").ToString+"\"+in_Config("NombreReporteGenerar").ToString` para especificar la carpeta donde estará el archivo Excel, si no existe se crea.

Dentro de este se agrega secuencia **Hacer** y dentro la actividad Escribir celda donde se configura la hoja, la celda y el mensaje a escribir:

[![194](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/194.png?raw=true "194")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/194.png?raw=true "194")

Luego se agrega actividad **Asignar** donde se crea variable `varFila` de tipo String y su valor es el código `in_TransactionItem.SpecificContent("Fila").ToString` para que nos indique el valor de la fila.

En otro **Asignar** se crea un contador `varContadorFila` para que agregue 1 a la variable VarFila y se pueda seguir escribiendo una fila después con el comando `1+int32.Parse(varFila)`

Se agrega actividad Escribir celda especificando la Hoja, la celda de acuerdo con el contador que se lleva `“A"+varContadorFila.ToString` y el valor que se quiere escribir es la palabra clave como un string con el siguiente comando `in_TransactionItem.SpecificContent("PalabrasClave").ToString`

[![195](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/195.png?raw=true "195")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/195.png?raw=true "195")

## Finalizando nuestro proyecto REF

Se ingresa en proceso **End Process** se observa dentro de actividad **Try** que por defecto **CloseAllApps.xaml** se utiliza para cerrar pero en nuestro caso no utilizamos aplicaciones, así que lo borramos.

[![196](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/196.png?raw=true "196")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/196.png?raw=true "196")

Se agrega secuencia **Envío de Correo** la cual extraemos como un Flujo de trabajo y guardamos en la carpeta **ImplementacionProceso / Finalizacion:**

[![197](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/197.png?raw=true "197")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/197.png?raw=true "197")

[![198](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/198.png?raw=true "198")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/198.png?raw=true "198")

Una vez creado se crea variable **in_Config** se configura su Tipo buscando como Dictionary< String,Object >

[![199](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/199.png?raw=true "199")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/199.png?raw=true "199")

Se agrega actividad **Obtener credencial** en la cual como entrada se utiliza comando con relación con Asset creado `in_Config("AssetCredencialCorreos").ToString`

Como salida se crea variables **varUsuario** y **varContraseña** la cual queda guardada como **SecureString.** Para la RutaDeCarpetaDeOrchestrator se configura lo siguiente `in_Config("OrchestratorFolderName").ToString`

[![200](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/200.png?raw=true "200")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/200.png?raw=true "200")

Como requerimos utilizar funciones de correo se requiere tener instalado el paquete `UiPath.Mail.Acivities`

[![201](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/201.png?raw=true "201")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/201.png?raw=true "201")

Seguido se adiciona actividad **Enviar mensaje de correo SMTP** en el que escribimos para quien va relacionado con el Asset creado anteriormente `in_Config("EnviarCorreoA").ToString`

Como asunto el mensaje y la fecha corta `"Reporte de resultado del proceso "+DateTime.Now.ToShortDateString`  acompañado del mensaje del cuerpo del correo.

Para el **Puerto** escribimos el comando `int32.Parse(in_Config("SMTP_Puerto").ToString)` que lee lo que ya configuramos en Settings en archivo Config.  Lo mismo funciona para el Servidor previamente escrito en el archivo `in_Config("SMTP_Servidor").ToString`

Para el inicio de sesión se utiliza el siguiente comando para manejar las credenciales del correo guardado 

`New System.Net.NetworkCredential(String.Empty, varContrasena).Password`

[![202](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/202.png?raw=true "202")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/202.png?raw=true "202")

Una vez terminado el **Try** se selecciona como Exception la opción **System.Exception,** y se le adiciona un mensaje de tipo Fatal con el mensaje de error, un salto de línea y el mensaje de Exception

`"Ha ocurrido un error en el envío del correo. "+Environment.NewLine+exception.Message`

[![203](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/203.png?raw=true "203")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/203.png?raw=true "203")

[![204](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/204.png?raw=true "204")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/204.png?raw=true "204")

# Arquitectura de Software

## Proyecto final

Las próximas 2 clases, utilizaremos esta solicitud de proyecto para trabajar las actividades de la clase, les recomiendo copiar el texto de la propuesta a un bloc de notas para tenerlo a la mano cuando realicemos las actividades de las clases.

**Situación actual:**

Actualmente Celis está creando en archivos de Excel con la lista de los cursos que encuentra al realizar ciertas búsquedas basadas en palabras claves. Después de 2 horas genera una lista con los siguientes datos:

- Nombre del Curso
- Página Web del Curso
- Nombre del Profesor (si son varios profesores se marca como “múltiples profesores”)

Ya con el archivo generado, se realiza un análisis de la información obtenida desde el buscador para optimizar sus resultados.

**Solicitud:**

Freddy considera que se invierte mucho tiempo en la extracción de la información, por lo que busca un desarrollador RPA que le dé una propuesta de la arquitectura (de hardware) requerida para automatizar este proceso, una propuesta de proyecto y una estimación del tiempo que tardará el robot en realizar la extracción de los datos.

- El archivo de palabras claves es proporcionado por un archivo de texto, las palabras claves estarán separadas por coma. Si hay 2 palabras seguidas sin coma, por ejemplo, “Programación Avanzada” se debe utilizar la búsqueda de las dos palabras al mismo tiempo en el buscador.
- El Excel generado debe contener 1 hoja por cada palabra clave usada en el buscador.
- Se requiere un solo Excel con todos los resultados.
- El Excel debe contener 3 columnas, Nombre del Curso, Página Web y Profesor (si son varios, colocar “Múltiples profesores”).
- Se requiere que la página web sea completa (ej. https://platzi.com/clases/programacion-basica/ ) 
- El Excel debe ser enviado por correo diariamente.
- Se requiere el Excel en la bandeja de correo antes de las 9:30am.
- Se busca que el proyecto sea funcional sin importar el costo, pero se dará mayor prioridad a las propuestas más económicas.

**Información adicional:**

Se cuenta actualmente con la siguiente infraestructura:

- Se cuenta con un Windows Server con espacio disponible para montar más sitios web en el IIS.
- Se cuenta con una Instancia de Base de Datos con espacio para almacenar más bases de datos de ser requerido.
- Hay dos equipos Laptop Windows 10 que quedan desocupados de 19hrs a 21hrs posteriormente se apagan por políticas de la empresa. Dichos equipos no cuentan con acceso al repositorio donde se aloja el insumo de “palabra_claves.txt”. Se puede revisar con infraestructura dar acceso de ser necesario.

**Propuesta:**

La propuesta entregada por el desarrollador que desea participar en la licitación debe contener.

- Propuesta de Arquitectura
  ¿Cuántos equipos requieren?
  ¿Requieren que sean nuevos?

- Propuesta de Solución
  ¿Cómo funcionará el proyecto?
  ¿Estructura del proyecto (modulación)?
  ¿Tiempo estimado de desarrollo?
  ¿Tiempo estimado de ejecución del proceso?

## Arquitectura para los proyectos

Las soluciones RPA tienen 2 tipos de soluciones, que varían según las necesidades del proyecto.

Los dos tipos de soluciones son las siguientes:

### 1. Solución estándar

UiPath recomienda la siguiente configuración como estándar, sin Alta disponibilidad; la estructura cuenta con los siguientes miembros:

- Robots: Es quien ejecuta las tareas desarrolladas, generalmente en un equipo independiente.
- Orquestador: Servidor Windows Server qué debe tener comunicación hacía SQL Server y hacía los Robots.
- SQL Server: Es un Servidor (o servicio, según la infraestructura) que aloja la base de datos del Orquestador.
- (Opcional) Elasticsearch: Servicio opcional, ElasticSearch es utilizado por el Orquestador para alojar los Logs de ejecuciones, de control, de fallos, esto es recomendado para:

  - No saturar la base de datos SQL con logs.
  - Elasticsearch puede ser combinado con otros softwares (como Kibana) para una explotación de los LOGS, generación de reportes, visualización gráfica, etc.

[![205](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/205.png?raw=true "205")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/205.png?raw=true "205")

[![206](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/206.png?raw=true "206")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/206.png?raw=true "206")

### 2. Solución de Alta Disponibilidad

La estructura de Alta Disponibilidad que UiPath recomienda es la siguiente:

- Robots: Deben estar conectados por un balanceador a los orquestadores.
- 2 orquestadores: Conectador por Redis, un orquestador funciona como activo y el otro como pasivo. Solo el activo opera, si el que opera falla, entra el pasivo a seguir dando soporte a los robots.
- 2 SQL Server: Ambos balanceados por instancia, funcionan de manera activa – pasiva igual que los orquestadores.
- 3 Redis: Mantienen un monitoreo de comunicación entre los Orquestadores, si el activo cae, son los Redis los encargados de activar el Orquestador en “espera” para operar
- (Opcional) 2 o más Elasticsearch: Ambos balanceados por instancia, funcionan de manera activa – pasiva igual que los orquestadores.

## La arquitectura de nuestro proyecto

Propuesta de Diagrama del proyecto:

[![207](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/207.png?raw=true "207")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/207.png?raw=true "207")

## Modulando un proceso Automatizado

Partir los procesos en pequeños subprocesos.

- Hacer una propuesta de solución de software para el proceso de Platzi.

¿Para qué nos sirve modular?

- Darle mantenimiento al código fácil y rápido.
- En mi experiencia: +2 módulos usando bases de datos para controlar los estados de los registros.
- Facilita la comunicación y el control de la información.

[![208](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/208.png?raw=true  "208")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/208.png?raw=true  "208")

Archivo Bizagi 

Propuesta de Proceso Global:

[![209](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/209.png?raw=true "209")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/209.png?raw=true "209")

Módulos de la propuesta de Proceso Global:

[![210](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/210.png?raw=true "210")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/210.png?raw=true "210")

## Solución del proyecto final

La solución al Proyecto final se encuentra en GitHub de Profesor Jorge Falcon, divida en dos partes de acuerdo con los módulos planteados: https://github.com/JFEspanolito?tab=repositories

## Centro de Excelencia

Documentación completa del Proceso Automatizado.

- Manuales de instalación.
- Manuales de Confuración.

Capacitar los usuarios.

- ¿Como funciona el Orchestador?
- ¿Como desarrollar sus propias automatizaciones?

Como guía se puede utilizar el Pase QA del Proyecto Final planteado por Falcón, que es la documentación oficial del proyecto que abarca desde su alcance, requisitos, configuración de robot, queues y assets utilizados, anexos y referencias, entre otras.

Archivo

[![211](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/211.png?raw=true "211")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/211.png?raw=true "211")

“Truco” de documentación:

[![212](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/212.png?raw=true "212")](https://github.com/hackmilo/Notas---Automatizacion-de-Procesos-RPA-con-UiPath/blob/main/img/212.png?raw=true "212")