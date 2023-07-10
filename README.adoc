# AntoraBundle pack editor

En este repo de github tenemos todo lo necesario para editar el bundle de Antora. El bundle seria como el 'theme' o el tema que se muestra con la documentación. 

El contenido que nos importa es el que se encuentra dentro del **SRC** el resto de ficheros y carpetas nos permiten construir una documentación "falsa" para ir previsualizando el **theme**

## Levantar el proyecto en local

1. Lo primero que tendremos que hacer es clonar el proyecto. 
2. Realizamos un 'npm i' dentro del proyecto clonado
3. Ejecutamos gulp preview
4. Accedemos al localhost especificado en consola para ver el proyecto de prueba con el tema. 

> Es importante destacar que en ocasiones el comando gulp preview falla, si eso ocurre probaremos a abrir un cmd, accederemos a la ruta del proyecto y lo lanzaremos desde el cmd. 

## Pasar el theme a nuestra doc de Antora

Una vez que tengamos el **theme** como nos interesa solo queda pasarlo a la documentación de **Antora**, para ello seleccionaremos todo lo que este dentro de la carpeta **src** y lo comprimiremos como .zip 

Una vez que tenemos el fichero comprimido accederemos a nuestra documentación de **Antora**y pegaremos el **.zip** en el directorio raiz. Luego abriremos el fichero 'antora-playbook.yml' y dentro de este especificaremos la ruta del **.zip** como se muestra en este código:

```yml
ui:
  bundle:
    url: ./prueba2.zip
    snapshot: true
```
Con esto automaticamente nuestra documentacion de **Antora** usara el template diseñado.

