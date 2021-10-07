# Notas - Automatizacion de Procesos RPA con UiPath

![](https://static.platzi.com/media/avatars/Platzi-f730e65b-e92b-44d3-81c0-5c59c4dc4658.png) ![](https://static.platzi.com/media/learningpath/badges/46.png) ![](https://static.platzi.com/media/achievements/mesa-de-trabajo-484-d124a2a2-d266-44ba-a797-6728efdc635e.png)

## Tabla de Contenidos

- [Introducción](#introducción)
  - [¿Quiénes participan en un proyecto RPA?](#quiénes-participan-en-un-proyecto-rpa)
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

## Sequences & Flowcharts

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

## Programar actividades: Open Application & Type Into

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

