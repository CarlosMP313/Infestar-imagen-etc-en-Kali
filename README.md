# Cómo Ocultar Archivos Detrás de una Imagen (Ejemplo con Scripts Automáticos)

Este método te permitirá ocultar cualquier archivo, como un script o texto, dentro de una imagen. A continuación, te explico los pasos para hacerlo:

## Pasos:

1. **Obtener una imagen:** Descarga o utiliza cualquier imagen que tengas. Para este ejemplo, usaremos una imagen llamada `perrito.jpg`.

2. **Crear un archivo para ocultar:** Para fines demostrativos, usaremos un archivo de texto. Sin embargo, puedes ocultar cualquier tipo de archivo, incluyendo scripts automáticos o incluso malware (esto último solo con fines educativos y nunca con intenciones maliciosas).

    - Abre una terminal y crea un archivo de texto:
      ```bash
      nano hacker.txt
      ```
    - Escribe algún contenido en el archivo, por ejemplo:
      ```
      ¡Has sido hackeado!
      ```
    - Guarda y cierra el archivo (`Ctrl + O` para guardar, `Ctrl + X` para salir).

3. **Comprimir el archivo en formato ZIP:** Comprime el archivo que deseas ocultar. En este caso, convertiremos el archivo de texto a formato ZIP, pero podrías usar cualquier nombre para el archivo ZIP.

    ```bash
    zip hacker.zip hacker.txt
    ```
    Aquí, `hacker.zip` es el nombre del archivo comprimido y `hacker.txt` es el archivo que estás ocultando.

4. **Fusionar el archivo comprimido con la imagen:** Usaremos el comando `cat` para fusionar el archivo ZIP con la imagen.

    ```bash
    cat hacker.zip >> perrito.jpg
    ```
    Este comando añade el contenido del archivo ZIP al final de la imagen, ocultando efectivamente el archivo dentro de la imagen `perrito.jpg`.

5. **Verificar la presencia del archivo oculto:** Para verificar que el archivo se encuentra dentro de la imagen, puedes usar el siguiente comando:

    ```bash
    cat perrito.jpg
    ```
    Esto mostrará el contenido binario de la imagen, incluyendo el archivo oculto.

6. **Extraer el archivo oculto:** Si deseas extraer el archivo oculto, simplemente descomprime la imagen utilizando el comando `unzip`:

    ```bash
    unzip perrito.jpg
    ```
    Esto descomprimirá el archivo `hacker.txt` (o cualquier otro archivo oculto) que fusionaste con la imagen.

## Importante:

Esta información es únicamente con fines educativos. No me hago responsable por el uso indebido de esta información. Ocultar archivos detrás de imágenes puede ser utilizado para propósitos legítimos, como proteger información sensible, pero también puede ser utilizado de forma maliciosa. Usa este conocimiento de manera ética y legal.
