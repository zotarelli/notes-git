# Test Git
Sistema de control de versinoes para el mantenimiento efectivo y confiable de archivos.

## Zonas de Git
1. Directorio de trabajo
2. Area de preparación
3. Directorio Git

## Flujo de trabajo básico en Git

1. Modificar una serie de archivos en el directorio de trabajo.
2. Preparar los archivos, añadiéndolos al área de preparación.
3. Confirmar los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en el directorio de Git.

## Configurando Git por primera vez
```
git config --global user.name "Valeria Zotarelli"
git config --global user.email "valeriazotarelli@gmail.com"
git config --global core.editor nano
git config --list
```
## Configuración SSH en Linux
Desde la terminal seguimos los siguientes pasos.

1. Ejecutamos el comando `ssh-keygen -t rsa -b 4096 -C "email@ejemplo.com"`
El correo debe ser el mismo con el que nos registramos en Github.
Cuando nos pida la ruta escribimos `/home/[usuario]/.ssh/github_rsa`

2. Iniciamos ssh-agent en background ejecutando el comando `eval "$(ssh-agent -s)"`

3. Agregamos la clave SSH generada a ssh-agent ejecutando el comando `ssh-add ~/.ssh/github_rsa`

4. Desde ahora podemos hacer pull y push sin que Github nos esté pidiendo los datos de acceso.
