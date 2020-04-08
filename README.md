# Introducción a Integración Continua y Despliegue Continuo en Jenkins

En esta sesión vamos a aprender las diferentes maneras de configurar un pipeline en Jenkins a través de código,
de manera que nuestros cambios queden siempre reflejados en nuestro sistema de control de versiones.

En Jenkins hay dos maneras de describir pipelines con código (previa instalación del plugin correspondiente):

 * Jenkins DSL: más completo pero más complejo, describiremos nuestros pipelines usando sintaxis de _groovy_.
 * Jenkinsfile: más limitado pero más sencillo, es una abstracción del anterior donde los métodos están predefinidos. Se basa en un fichero _Jenkinsfile_ donde se describen los pasos del pipeline de manera declarativa, aunque también se permite código _groovy_.

Para el ejemplo de esta clase, usaremos un Jenkinsfile. Para ello necesitamos un servidor de jenkins funcionando (ver
sección **Primeros pasos**.

## Primeros pasos

Antes de nada necesitamos una instalación de Jenkins en nuestro local. Para ello, ejecutaremos el siguiente comando:

`docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts`

Esto nos arrancará en nuestro local un contenedor de Jenkins con un maestro y dos esclavos en el puerto 8080 de nuestra
máquina.

Una vez se termine la descarga y empiece la ejecución del contenedor, lo primero que tenemos que hacer es copiar la
contraseña de administrador para desbloquear la interfaz administrativa. Una vez desbloqueada, crearemos nuestro usuario
e instalaremos los plugins necesarios (también se pueden instalar por defecto). Como la imagen de Jenkins viene
preconfigurada con dos esclavos y python preinstalado, es suficiente para nuestro siguiente paso.

## Crear nuestro primer pipeline

Crearemos un pipeline nuevo con nombre `cicd_introduction` para configurar seguidamente el repositorio y el Jenkinsfile
de nuestro usuario de github.

## Ejecutar por primera vez

Para verificar que todo funcionó correctamente, podemos darle a `Build` y ver el resultado de los logs de la ejecución!

## Siguientes pasos

Crear el código de la librería, los tests y definir los pasos de nuestro pipeline (análisis de código, tests, generación
de artefacto, publicación, etc).

## Presentación

Puede visualizar las transparencias usadas en la presentación en el siguiente enlace [keepcoding](https://docs.google.com/presentation/d/1_C4MIO2r2F7JSWLegVo3gHJJFU5RlOBoZwoMz9BOZD4/edit?usp=sharing)
