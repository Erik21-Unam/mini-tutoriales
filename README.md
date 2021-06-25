## Git

**Más usados**

- ``git pull`` (bajar los cambios)
- [``git add .``] ó [``git add -A``] (agregar todos los cambios)
- ``git commit -m 'Mensaje'`` (descripción de los cambios que creamos)
- ``git push`` (subir los cambios)
- ``git status`` (ver el estado de los cambios)
- ``git checkout nombre_rama`` (cambiarse de rama)


**Otros comandos**

- ``git init`` (inicializar un repositorio)
- ``git config user.email "email@dom.com"`` (agregar tu correo al repositorio)
- ``git config user.name "User"`` (agregar tu usuario al repositorio)
- ``git clone [tu.repositorio]`` (clonar el proyecto)
- ``git branch -a`` (mostrar todas las ramas locales)
- ``git config --list`` (mostrar la configuración del repositorio)


---
## Comandos utiles en Linux

1. ``touch mi_archivo.txt`` (podemos crear nuevos archivos)
2. ``ls`` (listar los archivos y directorios de la carpeta actual)
3. ``ls -a`` (listar los archivos y directorios ocultos de la carpeta actual)
4. ``ls -l`` (listar los archivos y directorios de la carpeta actual y mostrar su información detallada)
5. ``pwd`` (mostrar la ruta del directorio actual)
6. ``mv mi_archivo.txt ./mi_carpeta/mi_archivo.txt`` (cambiar archivos de ubicación)
7. ``mv mi_archivo.txt usuarios.txt`` (sirve para renombrar archivos)
8. ``cp usuarios.txt usuarios_copia.txt`` (copiamos archivos)
9. ``cp -r cursos/ cursos_copia/`` (copiar directorios)
10. ``cat notas.txt`` (leer el contenido de un archivo)
11. ``uname -a`` (muestra información del equipo)
12. ``lsb_release -a`` (muestra información del equipo | solo para distribuciones basadas en debian)
13. ``grep -i búsqueda archivo`` (buscar palabra en archivo | no distingue mayúsculas y minúsculas)
14. ``grep -c búsqueda archivo`` (número de veces que aparece una palabra en un archivo)
15. ``grep búsqueda1 archivo | grep búsqueda2 archivo`` (buscar múltiples palabras en archivo)

---

## Mercurial

**Más usados**

- ``hg pull`` (bajar los cambios)
- ``hg update`` (agregar los cambios bajados)
- ``hg addremove`` (solo si creamos algún archivo)
- ``hg commit -m 'Mensaje' -u usuario`` (descripción de los cambios que creamos)
- ``hg push`` (subir los cambios)
- ``hg status`` (ver el estado de los cambios)

**Otros comandos**

- ``hg log -l 4 -b default -G`` (ver los últimos commits creados)
- ``hg up nombre_rama`` (cambiarse de rama)
- ``hg graft 1024`` (pasar un commit a otra rama)

---

## Configuración Personal de Visual Studio Code
```
{
    "editor.fontFamily": "'Courier New', monospace",
    "editor.wordWrap": "on",
    "editor.fontSize": 16,
    "workbench.colorCustomizations": {
        "tab.activeBorder": "#eba946",
        "tab.unfocusedActiveBorder": "#000"
    }
}
```
**Mis extensiones de uso**
```
- Angular 8 and TypeScript/HTML VS Code Snippets
- Beautify
- Bracket Pair Colorizer
- CodeSanbox Theme
- Color Picker
- Git History
- GitLens -- Git supercharged
- Laravel Snippets
- Live Sass Compiler
- vscode-icons
- Awesome Flutter Snippets
- Dart
- Flutter
```

---
## Instalación local de LAMP en Ubuntu
```
- sudo apt install -y apache2 apache2-utils (para instalar apache)
- sudo service apache2 status (verificamos que el proceso se este ejecutando)
- sudo chown www-data:www-data /var/www/html/ -R (cambiamos el usuario del directorio html)
- sudo chmod -R 777 /var/www/html/ (le damos permisos al directorio)
- sudo apt install mysql-server mysql-client (instalamos mariadb)
- sudo service mariadb status (verificamos que el proceso se este ejecutando)
- sudo mysql_secure_installation (iniciamos la instalación segura)
- sudo apt install php7.4 libapache2-mod-php7.4 php7.4-mysql php-common php7.4-cli php7.4-common php7.4-json php7.4-opcache php7.4-readline php7.4-mbstring php7.4-curl (instalamos php)
- sudo a2enmod php7.4 (habilitamos el modulo de php)
- sudo service apache2 restart (reiniciamos el servidor)
- sudo nano /var/www/html/info.php (escribimos la siguiente línea: <?php phpinfo(); ?>)
- sudo apt install phpmyadmin (instalamos phpmyadmin)
- sudo nano /etc/apache2/apache2.conf (hasta el final del archivo colocamos lo siguiente: Include /etc/phpmyadmin/apache.conf)
- sudo mysql -u root -p (entramos a la base de datos)
- CREATE USER 'user'@'localhost' IDENTIFIED BY 'password'; (creamos un usuario)
- GRANT ALL PRIVILEGES ON * . * TO 'user'@'localhost'; (con esto tendra todos los privilegios)
- FLUSH PRIVILEGES; (cargamos los valores de la BD)
- sudo service apache2 restart (reiniciamos el servidor)

Opcional:
- sudo systemctl disable apache2 (desactivamos el proceso)
- sudo systemctl disable mariadb (desactivamos el proceso)
```

---

## Configuraciones para .htaccess

**Quitar la extensión .html de la url**
```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME}.html -f
RewriteRule ^(.*)$ $1.html
```

**Quitar la extensión .php de la url**
```
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME}.php -f
RewriteRule ^(.*)$ $1.php
```

**Denegar la vista de archivos de un directorio**
```
Options All -Indexes
```
