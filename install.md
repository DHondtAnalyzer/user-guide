# Manual de instalación y despliegue

Este manual contiene la información paso a paso para instalar la aplicación D'Hont Analyzer y desplegarla en un servidor para su posterior uso.

## Requisitos

Son necesarias las siguientes precondiciones:

- Disponer del código fuente de la aplicación que acompaña a este manual.

- Disponer de una cuenta en Firebase, necesaria para la Base de datos y la gestión de la autenticación.

- Su sistema operativo se encuentra actualizado.

## Instalación

- Instalar `node.js` versión LTS 6.9.4. y el gestor de paquetes `npm`. Para ello, puede usar el instalador correspondiente a su Sistema Operativo que puede encontrar en [este enlace](https://nodejs.org/en/download/ "Node js download"). Puede comprobar si la instalación fue satisfactoria ejecutando en un terminal la instrucción `node -v`.

- Opcionalmente, si su SO no es Windows, puede instalar `node.js` y `npm` a través del gestor de versiones [nvm](https://github.com/creationix/nvm#install-script). Una vez haya instalado `nvm`, ejecute en un terminal el comando `nvm install 6`.

- Extraiga el código fuente de la aplicación en un directorio y situése en el directorio raíz. Ejecute en un terminal el comando `npm install`, y de este modo se instalarán las dependencias necesarias para ejecutar la aplicación.

- Para la configuración del módulo externo `AngularFireModule` es necesario que se dirija en la consola de Firebase al apartado _Authentication_ pulsando el siguiente botón:<br>![imagen](https://cloud.githubusercontent.com/assets/9568287/20773142/b4551b18-b750-11e6-9c89-e4d7fe89e2a8.png)<br> A continuación, modifique la plantilla localizada en el directorio `src/environments` llamada `firebase.config.ts.template` (**consejo**: no borrar esta plantilla para hacer más rápida la configuración). Copie dicho fichero a uno llamado `firebase.config.ts` en el mismo directorio, y rellene los valores con los que se muestra en la consola de firebase.
```json
{
  "apiKey": "<your-key>",
  "authDomain": "<your-project-authdomain>",
  "databaseURL": "<your-database-URL>",
  "storageBucket": "<your-storage-bucket>"
}
```

## Despliegue

- Para ejecutar la aplicación, ejecute en el directorio ráiz de la aplicación el comando `npm start` desde una terminal.