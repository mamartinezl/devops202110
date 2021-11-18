# JOBS

1. Crear job1
    1. Crear proyecto del estilo libre.
        * Nombre: job01
        * Description: Primer job
        * Build --> Execute shell --> echo "hola mundo"

1. Editar job1
    1. Crear proyecto del estilo libre.
        * Nombre: job01
        * Description: Primer job
        * Build --> Execute shell --> echo "La fecha del sistema es $(date)"

1. Crear job2
    1. Crear proyecto del estilo libre.
        * Nombre: job02
        * Description: Segundo job
        * Build --> Execute shell --> 
        ```console
        NOMBRE="AUTO"
        echo "La fecha del sistema es $(date) - $NOMBRE" >> /tmp/demo.txt
        ```        
        * Verificar
        ```console
        docker exec -it jenkins bash
        ls -lt /tmp
        cat /tmp/demo.txt
        ``` 
        
1. Crear job3

    1. Copiar archivos

    ```console
    cd ~/devops202110/Lab02
    docker cp script.sh jenkins:/opt/script.sh
    docker exec -it jenkins bash
    ls -lt /opt
    ``` 
    
    ```console
    NOMBRE="DEV"
    APELLIDO="OPS"
    MOSTRAR=1

    /opt/script.sh $NOMBRE $APELLIDO $MOSTRAR
    ``` 

1. Crear job4 con parámtros
    1. En la sección **General**, seleccionar _"This project is parameterized"_
    1. Agregar 3 parámetros:
        | NAME        | TYPE           | Value  |
        | ------------- |:-------------:|:-----|
        | NOMBRE        | String        | DEV |
        | APELLIDO      | String        | OPS |
        | MOSTRAR       | Boolean       | GO |
