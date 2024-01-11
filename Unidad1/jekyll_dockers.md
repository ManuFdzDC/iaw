# JEKYLL EN DOCKERS
## 1. Instalar en docker una imagen de Jekyll.
```docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll```

![image](https://github.com/ManuFdzDC/iaw/assets/144890528/40dad30c-c32a-43be-b9b1-ceff920f4c18)


## 2. Crear una pagina de jekyll.
```docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll new blog```
Con este comando crearemos la estructura de archivos de un proyecto jekyll.

![image](https://github.com/ManuFdzDC/iaw/assets/144890528/9c2a9ce4-324b-4b8c-8b7e-a013f872d901)

## 3. Editar el archivo Gemfiles.
Nos moveremos a la carpeta del blog que ha creado Jekyll para poder editar el archivo Gemfiles.
```cd blog``` 

![image](https://github.com/ManuFdzDC/iaw/assets/144890528/8e9bcbba-b51b-4b01-b570-89aa7d3d433a)

En este directorio ejecutaremos el comando

```nano Gemfile```

y al final del archivo escribiremos

```gem "webrick"```

![image](https://github.com/ManuFdzDC/iaw/assets/144890528/8bda4206-c0f4-4ff2-aa81-84fa350b804d)

## 4. Ejecutar de forma local el sitio HTML generado por Jekyll.

```docker run -it --rm -p 4000:4000 -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll serve --force_polling```

El comando habra que ejecutarlo en el directorio blog y la pagina se abrira en el puerto 4000.
![image](https://github.com/ManuFdzDC/iaw/assets/144890528/7cc9af44-5957-4a42-8d6c-62679c947162)

## 5. Visualizar la pagina en el navegador web.
Escribiremos en el buscador la ip de la maquina virtual en que la que se esta ejecutando seguido del puerto donde se ejecuta la pagina web.

![image](https://github.com/ManuFdzDC/iaw/assets/144890528/464fc260-38d1-4631-b877-1a105b624e92)

