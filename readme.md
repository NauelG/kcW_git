# Práctica del curso de Git de KeepCoding

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

`git reset --hard HEAD~1`
Movemos el puntero head y la rama actual al comit anterior modificando el working copy.

- ¿Qué comando utilizaste en el paso 12? ¿Por qué?

`git reflog` para averiguar la referéncia del commit del paso anterior, al cual no tenemos acceso.
`git reset --hard [ref del commit` para moverme a ese commit y modificar el working copy.

- El merge del paso 12, ¿Causó algún conflicto? ¿Por qué?

No, en ese caso la rama styled ya tenia acceso a todos los commits de la rama master por lo tanto
no se llega a realizar el merge.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Si, en ese caso se da conflicto. El archivo git-nuestro.md fue modificado en la rama htmlify y en la
rama styled en las mismas lineas. Al hacer el merge hay que resolver conflictos.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No, en la rama master no se habia modificado el archivo git-nuestro.md por lo tanto se podía hacer
el merge.

- ¿Qué comando o comandos utilizaste en el paso 25?

`git log --graph --pretty=oneline`

- El merge del paso 26, ¿Pordía ser fast-forward? ¿Por qué?

Si, la rama master sólo tenía que avanzar un commit para situarse a la altura de title.
No perdía acceso a sus commits anteriores.

- Que comando o comandos utilizaste en el paso 27?

`git reset HEAD~1` Moviendo la rama a su posicion anterior sin modificar el working-copy.

- Que comando o comandos utilizaste en el paso 28?

`git checkout -- git-nuestro.md` para descartar los cambios detectados por git.
Se devuelve el working-copy a la posición del commit actual en el archivo referenciado.

- Que comando o comandos utilizaste en el paso 29?

`git branch -D title` Al deshacer el merge, la rama title quedaba un commit por delante de la rama
master, con un `git branch -d title` no se habría eliminado.

- Que comando o comandos utilizaste en el paso 30?

Localizamos el commit del merge con `git reflog`
Hacemos `git reset --hard [ref-del-commit]` para mover la rama a ese commit modificando el working-copy

- Que comando o comandos utilizaste en el paso 32?

Localizamos el id del primer commit con `git log`
`git checkout [ref-del-commit]` para mover el punter head a ese commit.

- Que comando o comandos utilizaste en el paso 33?

Hacemos un `git reflog` para ver la posicion anterior de head.
`git checkout [ref-del-commit]` para movernos a el.
`git checkout master` para dejar el punter head en master y no en detached HEAD.



