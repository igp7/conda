# CHEAT SHEET

## Conda
|COMANDO|DESCRIPCIÓN|
|---|---|
|conda info|Verifica que Conda está instalado, comprueba el número de versión.|
|conda update -n base conda| Actualiza Conda a la versión actual.|
|conda update anaconda|Actualiza todos los paquetes a la última versión de Anaconda. Instalará versiones estables y compatibles, no necesariamente la más reciente.|
|conda clean --all|Elimina los archivos en caché no utilizados, incluyendo los paquetes no utilizados.|
|conda config --show conda config --show-sources|Examinar la configuración de Conda y los servicios de configuración.|


## Creacion de entornos
|COMANDO|DESCRIPCIÓN|
|---|---|
|conda info --envs|Listado de todos los entornos creados|
|conda create --name ENVNAME python=3.6 "PKG1>7.6" PKG2|Crea un nuevo entorno llamado ENVNAME con la versión específica de Python y los paquetes instalados.|
|conda create --name NEWENV --file pkgs.txt|Crear un entorno basado en las versiones exactas de los paquetes.|
|conda env create|Crea un entorno a partir del archivo llamado environment.yml en el directorio actual.|
|conda env create --file envname.yml|Crear un entorno a partir de un archivo YAML.|


## Activacion de entornos
|COMANDO|DESCRIPCIÓN|
|---|---|
|conda activate ENVNAME|Activar un entorno Conda con nombre.|
|conda activate /path/to/environment-dir|Activar un entorno Conda en una ubicación concreta del disco.|
|conda deactivate|Desactivar el entorno actual.|


## Eliminacion de entornos
|COMANDO|DESCRIPCIÓN|
|---|---|
|conda remove --name ENVNAME --all|Eliminar un entorno completo.|


## Configuracion de entornos
|COMANDO|DESCRIPCIÓN|
|---|---|
|conda env config vars set <name_var>=<value_var>|Añade una variable de entorno al entorno activado|
|conda env config vars unset <name_var>|Elimina una variable de entorno del entorno activado|
|conda env config vars list|Lista las variables de entorno del entorno activado|


## Compartir entornos
|COMANDO|DESCRIPCIÓN|
|---|---|
|create --clone ENVNAME --name NEWENV|Hacer una copia exacta de un entorno conda.|
|conda env export --name ENVNAME > envname.yml o conda env export > envname.yml|Exporte un entorno a un archivo YAML que pueda ser leído en Windows, macOS y Linux.|
|conda list [--explicit|-e] > requirements.txt|Exportar un entorno con versiones exactas de paquetes para un sistema operativo.|


## Administracion de entornos
|COMANDO|DESCRIPCIÓN|
|---|---|
|conda list --revisions|Enumerar todas las revisiones realizadas en el entorno activo.|
|conda list --name ENVNAME --revisions|Enumerar todas las revisiones realizadas en un entorno determinado.|
|conda install --name ENVNAME --revision REV_NUMBER|Restaurar un entorno a una revisión anterior determinada.|


## Packages 
|COMANDO|DESCRIPCIÓN|
|---|---|
|conda list|Enumerar todos los paquetes y versiones en el entorno activo.|
|conda list --name ENVNAME|Enumera todos los paquetes y versiones de un entorno determinado con la opcion --name.|
|conda search PKGNAME=3.1 "PKGNAME [version='>=3.1.0,<3.2']"|Buscar un paquete en los canales actualmente configurados con un rango de versiones >=3.1.0, <3.2".|
|anaconda search FUZZYNAME|Encuentre un paquete en todos los canales utilizando el Cliente Anaconda.|
|conda search PKGNAME --info|Información detallada sobre las versiones de los paquetes.|
|conda install conda-forge::PKGNAME|Instalar el paquete desde un canal específico.|
|conda install PKGNAME==3.1.4|Instalar un paquete por número de versión exacto (3.1.4).|
|conda install "PKGNAME[version='3.1.2|3.1.4']"|Instale una de las versiones de la lista (OR).|
|conda install "PKGNAME>2.5,<3.2"|Instale las siguientes restricciones (AND).|
|conda install --yes PKG1 PKG2|Ejecuta la mayoría de los comandos sin requerir un prompt de usuario. Útil para los scripts.|
|conda uninstall PKGNAME --name ENVNAME|Eliminar un paquete de un entorno.|
|conda update --all --name ENVNAME|Actualizar todos los paquetes de un entorno.|


## Channels
|COMANDO|DESCRIPCIÓN|
|---|---|
|conda config --add channels CHANNELNAME|Añade un canal a tu configuración de Conda.|


## Referencias
- [Conda command reference](https://docs.conda.io/projects/conda/en/latest/commands/index.html)
