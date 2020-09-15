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
git commit -m "feat: primeros pasos"
git status
```