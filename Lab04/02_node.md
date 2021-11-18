# Node
## Settings

1. Instalar plugins Node
    1. Login
    1. Manage Jenkins
    1. Manage Plugins
    1. Clic Avialable
    1. Buscar Plugin: "NodeJS"

1. Instalar nodejs
    1. Manage Jenkins
    1. Global Tool Configuration
    1. Ir a la sección: "NodeJS"
    1. Clic en "Add NodeJS"
        * Name: node-default
        * Install automatically: Check
        * Version: 16.11.1

## JOBS
1. Crear job6-build-nodejs
    * Crear proyecto del estilo libre.
        * Nombre: job6-nodejs
        * Description: Node demo
        * Build Environment: Provide Node & npm bin/ folder to PATH
        * Build --> add execute shell --> 
        ```shell         
        npm version
        ```        

1. Crear job6-script-nodejs
    * Crear proyecto del estilo libre.
        * Nombre: job6-nodejs
        * Description: Node demo
        * Build --> Execute NodeJS script --> 
        ```shell         
        console.log("ok");
        console.log(process.version);
        ```  

