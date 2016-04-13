- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
	git reset --hard HEAD~1 (utilizo el --hard para perder los cambios que tenia en mi working copy )

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
	git reset HEAD@{1} (utilizo este comando porque se vengo de ese reset, de manera que si quiero deshacer el reset que acabo de hacer justo en la instrucción anterior puedo usar HEAD@{1}. Si el reset no fuera el inmediatamente anterior tendría que haber buscado el ID en el git log y haber hecho un reset a ese ID)

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
	No causa conflicto porque styled ya tiene todo lo que tiene la rama master, esta al día. Habiamos modificado el fichero pero al hacer un reset hard nos pusimos en el mismo commit de rama master y aunque luego deshicimos el reset seguimos teniendo en nuestro repositorio los mismos cambios que tenia master, por eso estamos al dia.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
	Sí causo conflicto porque htmlify nació de master y avanzó con un commit al margen de styled de manera que el fichero git-nuestro.md tenia contenido diferente y al hacer el merge salta el conflicto.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
	No se ha creado ningún conflicto porque estaban en la misma línea de commits de manera que master puede avanzar y hacer un fast fordward hacia styled.

- ¿Qué comando o comandos utilizaste en el paso 25?
	git log --graph --decorate

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
	Sí podría haber sido un merge no fast fordward porque estaban en la misma línea de commit hacia debajo de manera que se podría haber llevado el puntero master hasta title sin haber hecho un commit nuevo.

- ¿Qué comando o comandos utilizaste en el paso 27?
	git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?
	git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?
	git branch -D title
	git push origin --delete title

- ¿Qué comando o comandos utilizaste en el paso 30?
	git reflog
	git reset --hard HEAD@{1}

- ¿Qué comando o comandos usaste en el paso 32?
	git reflog 
	git reset --hard 0eb87c9

- ¿Qué comando o comandos usaste en el punto 33?
	git reflog
	git reset --hard HEAD@{1}
