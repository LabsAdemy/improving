# Git

Buenas prácticas con GIT

## Primeros pasos

### Configuración

https://gitforwindows.org/
https://git-scm.com/downloads

```bash
git config --global user.name "[firstname lastname]"
git config --global user.email "[valid-email]"
git config --global credential.helper wincred
git config --global --list
```

### Inicialización

```bash
mkdir improving
cd improving
git init
git status
```

### Edición de ficheros y staging area

```bash
# crear y modificar fichero curso.md
git add ./curso.md # incorporar fichero al control de código
git status
# modificar fichero curso.md
git status
git add ./curso.md # incorporar cambios del fichero al control de código
git status
# modificar con un error
git status
git checkout -- ./curso.md # deshacer cambios en curso.md
git status
git reset ./curso.md # sacar de git el fichero curso.md
git status
git add * # volver a añadir el fichero y cualquier otro
git diff # ver cambios no incorporados
:q # para salir
```

### Ignorar ficheros

`.gitignore`

```txt
node_modules/
logs/
.vscode/
```

### Cometer, comprometer, guardar los cambios

```bash
git commit -m "feat: primeros pasos" # Guardar cambio con un mensaje que indique propósito
git log # ver historial de cambios comprometidos
git show curso.md # ver cambios de un fichero
```
> Cada commit tiene un identificador único

```bash
git rev-parse HEAD # Obtenr id del útlimo commit
```

### Convenio de Mensajes

[conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)


fix: Para arreglos de errores (avanza versión patch) #issueID

feat: Para agregar funcionalidad (avanza versión minor) #issueID

fix|feat!: Cambios rupturistas (avanza versión major) #issueID

refactor: Cambios internos que no afectan al uso

docs: documentación de soporte

test: pruebas

chore : Para cambios en editor o configuración

`pacakge.json`
```json
{
  "scripts": {
    "release": "standard-version"
  }
}
```

```
npm init
npm i --save-dev standard-version
git add *
git commit -m 'chore: add standard version to commits'
npm run release
```

> Genera un CHANGELOG.md y etiqueta los commits


## Ramas


### Crear y moverse a otra rama

**BORRAR RAMA ENLACES Y REPETIR PROCESO**

```bash
git add *
git commit -m 'feat: previo a crear rama'
git branch # lista de ramas
git branch enlaces # crea la rama, pero NO se cambia
git commit -am 'feat: previo a mover a rama' # -am hace add y commit
git checkout enlaces # cambio de rama
```

### Realizar cambios

```bash
# Crear fichero de enlaces.md
git add *
git commit -m 'feat: enlaces de interés'
```

### Integrar los cambios

> Hay un corriente promovida por BLM para cambiar master por main

## Integración remota

### Crear repositorio remoto

### Enviar cambios

### Obtener cambios

## Gestión de conflictos