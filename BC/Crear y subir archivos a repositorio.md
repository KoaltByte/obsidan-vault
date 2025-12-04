1. Crear un nuevo repositorio remoto en `GitHub`.
2. Iniciar en `git` con la cuenta de `Github` 
   ```git
   git config --global user.email
   git config --global user.name
   ```
3. En git navegar hasta el directorio que se desea subir
   ```git
   cd /ruta/a/tu/vault
   ```
4. Convertir la carpeta normal en un repositorio de git
   Se crea una carpeta oculta `.git/` en donde git guarda el historial de cambios, los commits, las ramas y las configuraciones del repo.
   ```git
   git init
   ```
5. Añadir los archivos y prepararlos para el commit
   ```git
   git add .
   ```
6. Crear una versión actualizada del proyecto
   El comit guarda los archivos añadidos o modificados, asigna un mensaje de "Initial commit" el cual queda en el historial del repositorio.
   ```git
   git commit -m "Initial commit"
   ```
   El texto entre comillas se puede cambiar y debe de ser una descripción pequeña sobre los cambios que se hicieron en ese commit.
7. Renombrar la rama actual a main.
   Prepara la rama principal para subirla al repositorio remoto
   ```git
   git branch -M main
   ```
8. Indicar el repositorio remoto en donde se subiran los archivos
   ```git
   git remote add origin https://github.com/usuario/repo.git
   ```
9. Subir el repositorio local a GitHub por primera vez.
   ```git
   git push -u origin main
   ```
   - push envía los commits a GitHub
   - origin es el repositorio remoto
   - main es la rama que se sube
   - -u establece que main local seguirá a origin/main

## Resumen 

|**Comando**|**Qué hace**|**Para qué sirve en tu repositorio de Obsidian**|
|---|---|---|
|`git init`|Inicializa un repositorio Git en la carpeta actual.|Le dice a Git que empiece a rastrear cambios en tu carpeta del vault.|
|`git add .`|Agrega **todos los archivos y carpetas** al área de preparación (staging).|Indica qué archivos quieres incluir en el primer commit (tu vault completo).|
|`git commit -m "Initial commit"`|Crea un commit con los archivos agregados y un mensaje.|Guarda una “foto inicial” de tu vault en Git.|
|`git branch -M main`|Crea o renombra la rama principal a **main**.|Asegura que tu rama principal se llame _main_, que es el estándar actual de GitHub.|
|`git remote add origin https://github.com/tu-usuario/obsidian-vault.git`|Conecta tu repositorio local con un repositorio remoto en GitHub.|Permite sincronizar tu vault entre tu computadora y GitHub.|
|`git push -u origin main`|Envía tu rama **main** al repositorio remoto y la establece como predeterminada.|Sube t|
# Comandos útiles después de crear el repo 
|**Comando**|**Qué hace**|**Para qué sirve en tu repositorio de Obsidian**|
|---|---|---|
|`git status`|Muestra el estado del repositorio: archivos modificados, nuevos, eliminados y si hay commits pendientes.|Para ver qué notas o archivos de tu vault han cambiado y si ya están preparados para hacer commit.|
|`git pull`|Descarga los cambios del repositorio remoto y los fusiona con tu repositorio local.|Para actualizar tu vault local con lo que tengas en GitHub (útil si usas dos computadoras).|
|`git push`|Sube tus commits locales al repositorio remoto.|Para sincronizar tus cambios de Obsidian hacia GitHub.|
|`git log`|Muestra el historial de commits.|Para ver qué cambios has hecho antes, cuándo y con qué mensaje (útil para volver en el tiempo).|
|`git restore`|Permite restaurar archivos a un estado anterior o deshacer cambios no confirmados.|Para recuperar una nota si la arruinaste o revertir un cambio antes de hacer commit.|
|`git checkout`|Cambia entre ramas o restaura archivos individuales.|Para trabajar en otra versión de tu vault o revisar una nota tal como estaba en un commit pasado.|
|`git merge`|Combina los cambios de una rama con otra.|Para integrar trabajo que hiciste en otra rama (por ejemplo, experimentos o reorganización de notas).|
# Guardar cambios en un repo
1. Preparar los cambios para el commit
   ```git
   git add .
   ```
2. Hacer el commit
   Hace una "captura" de todas las modificaciones
   ```git
   git commit -m "Descripción de los cambios"
   ```
3. Enviar los archivos a GitHub
   ```git
   git push
   ```