# Ramas en git

Una rama es un puntero a un commit. Cada vez que se crea una rama, se crea un nuevo puntero a un commit. Las ramas son útiles para trabajar en diferentes características o correcciones de errores sin afectar la rama principal (master o main).

## Crear una rama local

Si tu repositorio solo existe localmente, puedes crear una rama local con el siguiente comando:

```bash
git branch nombre_rama
```

## Crear una rama remota

Si tu repositorio ya apunta a un repositorio remoto, puedes crear una rama remota con el siguiente comando:

```bash
git push origin nombre_rama
```

`origin` es el nombre del repositorio remoto y `nombre_rama` es el nombre de la rama que deseas crear. Si no has configurado un repositorio remoto, puedes hacerlo con el siguiente comando:

```bash
git remote add origin url_del_repositorio
```

Si no sabes si tienes un repositorio remoto configurado, puedes verificarlo con el siguiente comando:

```bash
git remote -v
```

## Workflow

```bash
git init
git add .
git commit -m "Initial commit"

# crear el repo de github

git remote add origin <url>
git push

# crear una rama local y cambiar a ella

git branch nombre_rama
git checkout nombre_rama

# subir rama a github

git add .
git commit -m "Cambios en la rama"
git push origin nombre_rama

# cambiar a la rama master y fusionar los cambios

git checkout master
git merge nombre_rama
git push origin master
```

Al hacer push puedes encontrar el siguiente error:

```bash
datadiego@/tmp/test git push
fatal: The current branch feature_wapa has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feature_wapa

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.
```

Puedes usar la flag `--set-upstream` o `-u` para crear la rama remota y hacer push a ella al mismo tiempo:


