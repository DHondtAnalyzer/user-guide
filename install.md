# Manual de instalación y despliegue

Este manual contiene la información paso a paso para instalar la aplicación D'Hont Analyzer y desplegarla en un servidor para su posterior uso.

## Requisitos

Son necesarias las siguientes precondiciones:

- Disponer del código fuente de la aplicación que acompaña a este manual.
- Disponer de una cuenta en Firebase, necesaria para la Base de datos y la gestión de la autenticación.

## Instalación

- Instalar node.js usando el instalador correspondiente a su Sistema Operativo que puede encontrar en [este enlace](https://nodejs.org/en/download/ "Node js download"). Puede comprobar si la instalación fue satisfactoria ejecutando en un terminal la instrucción `node -v`.
- Extraiga el código fuente de la aplicación en un directorio y situése en el directorio raíz. Ejecute en un terminal el comando `npm install`, y de este modo se instalarán las dependencias necesarias para ejecutar la aplicación.
- Para enlazar la aplicación con su base de datos de Firebase, ha de editar el fichero `DirectorioApp/src/environments/firebase.config.ts`, he introducir la siguiente información:
	+ apiKey
    + authDomain
    + databaseURL
    + storageBucket
    + messagingSenderId

## Despliegue

- Para ejecutar la aplicación, ejecute en el directorio ráiz de la aplicación el comando `npm start` desde una terminal.