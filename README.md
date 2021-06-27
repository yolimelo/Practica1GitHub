# Práctica 1 de Git y GitHub

- ¿Qué comando utilizaste en el paso 11?  
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git reset --hard HEAD~1
	cls
	HEAD is now at 01cbace Primer commit, moviendo git-nuestro.md al Repositorio
	
	¿Por qué? Porque al usar el modificador --hard se mueve el puntero HEAD y además deja el Working copy 
	como estaba.
	
- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git reflog
	01cbace (HEAD -> styled, master) HEAD@{0}: reset: moving to HEAD~1
	a56bd9c HEAD@{1}: commit: Modificado archivo git-nuestro.md en la rama styled
	01cbace (HEAD -> styled, master) HEAD@{2}: checkout: moving from master to styled
	01cbace (HEAD -> styled, master) HEAD@{3}: commit (initial): Primer commit, moviendo git-nuestro.md al Repositorio
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git reset --hard a56bd9c
	HEAD is now at a56bd9c Modificado archivo git-nuestro.md en la rama styled	
	
	¿Por qué? Porque con git reset --hard a56bd9c movemos el puntero MASTER al commit donde modificamos el archivo 
	git-nuestro.md 	en la rama styled y además restauramos lo que había en el working copy.
 
- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
	Me aseguro de estar en la rama styled:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git branch
	  master
	* styled
	
	Mergeo:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git merge master
	Already up to date.
	
- El merge del paso 19, ¿Causó algún conflicto? Sí.

	*Git* nuestro que estás en los repos 
	Comprimidos sean tus *commits* 
	Venga a nosotros tu *log* 
	En el local como en el *remote* 
	Danos hoy nuestro *pull* de cada día 
	Perdona nuestros *conflictos* 
	Como también perdonamos los de otros geeks 
	No nos dejes caer en *detached HEAD* 
	y líbranos de *SVN* 
	`git commit --amend`
	=======
	<p><em>Git</em> nuestro que estas en los repos<br /> 
	Comprimidos sean tus <em>commits</em><br /> 
	Venga a nosotros tu <em>log</em><br /> 
	En el local como en el <em>remote</em><br /> 
	Danos hoy nuestro <em>pull</em> de cada día<br /> 
	Perdona nuestros <em>conflictos</em><br /> 
	Como también perdonamos los de otros geeks<br /> 
	No nos dejes caer en <em>detached HEAD</em><br /> 
	y líbranos de <em>SVN</em><br /> 
	<code>git commit --amend</code></p>
	>>>>>>> htmlify
	
	¿Por qué? 
	Porque el contenido del archivo git-nuestro.m de la rama styled y el contenido de la rama htmlify son diferentes.
	
	Ahora añado git-nuestro.md, quedándome con el contenido de la rama "styled", al staging area y luego haré un commit.
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git add git-nuestro.md
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git commit -m "Commit que concluye el merge de la rama styled con la rama htmlify"
	[styled 75194e9] Commit que concluye el merge de la rama styled con la rama htmlify
 
- El merge del paso 21, ¿Causó algún conflicto? No. 
	¿Por qué? Porque ambas ramas tienen el archivo git-nuestro.md con el mismo contenido.
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git merge styled
	Updating 01cbace..75194e9
	Fast-forward
	 git-nuestro.md | 19 +++++++++----------
	 1 file changed, 9 insertions(+), 10 deletions(-)

- ¿Qué comando o comandos utilizaste en el paso 25?

	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git log --graph
*   commit 75194e933333618ed5f1c9d7e2756b65e0d82098 (HEAD -> master, styled)
|\  Merge: a56bd9c 2e9ca7a
| | Author: Yolanda Mesa <yolimelo@gmail.com>
| | Date:   Sun Jun 27 19:23:58 2021 +0200
| |
| |     Commit que concluye el merge de la rama styled con la rama htmlify
| |
| * commit 2e9ca7adc928c6ab203082db1a376f6b8d302520 (htmlify)
| | Author: Yolanda Mesa <yolimelo@gmail.com>
| | Date:   Sun Jun 27 19:06:40 2021 +0200
| |
| |     Modificado archico git-nuestro.md en la rama htmlify
| |
* | commit a56bd9c841b683ad2de0e3ed4214f8751a422403
|/  Author: Yolanda Mesa <yolimelo@gmail.com>
|   Date:   Sun Jun 27 18:39:05 2021 +0200
|
|       Modificado archivo git-nuestro.md en la rama styled
|
* commit 01cbace129caecab677dffcf60123e7621c12357
  Author: Yolanda Mesa <yolimelo@gmail.com>
  Date:   Sun Jun 27 18:29:46 2021 +0200

      Primer commit, moviendo git-nuestro.md al Repositorio
 
- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 
	No podría ser Fast forward porque se ha añadido un commit adicional.


- ¿Qué comando o comandos utilizaste en el paso 27?

	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git reset HEAD~1
	Unstaged changes after reset:
	M       git-nuestro.md
 
- ¿Qué comando o comandos utilizaste en el paso 28?
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git restore git-nuestro.md
- ¿Qué comando o comandos utilizaste en el paso 29? 
	Compruebo en qué rama estoy:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git branch
	  htmlify
	* master
	  styled
	  title
	Ahora borro la rama title:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git branch -D title
	Deleted branch title (was b9026e2).
	
- ¿Qué comando o comandos utilizaste en el paso 30? 
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git reset --hard
	HEAD is now at 75194e9 Commit que concluye el merge de la rama styled con la rama htmlify
	
- ¿Qué comando o comandos usaste en el paso 32?
	Primero miro el id que tiene y su puntero HEAD:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git reflog
	75194e9 (HEAD -> master) HEAD@{0}: checkout: moving from master to master
	75194e9 (HEAD -> master) HEAD@{1}: reset: moving to HEAD
	75194e9 (HEAD -> master) HEAD@{2}: reset: moving to HEAD~1
	f0a7aac HEAD@{3}: merge title: Merge made by the 'recursive' strategy.
	75194e9 (HEAD -> master) HEAD@{4}: checkout: moving from title to master
	b9026e2 HEAD@{5}: commit: Modificado archivo git-nuestro.md poni<C3><A9>ndole un titulo y estando en la rama title
	75194e9 (HEAD -> master) HEAD@{6}: checkout: moving from master to title
	75194e9 (HEAD -> master) HEAD@{7}: merge styled: Fast-forward
	01cbace HEAD@{8}: checkout: moving from styled to master
	75194e9 (HEAD -> master) HEAD@{9}: commit (merge): Commit que concluye el merge de la rama styled con la rama htmlify
	a56bd9c HEAD@{10}: checkout: moving from htmlify to styled
	2e9ca7a HEAD@{11}: commit: Modificado archico git-nuestro.md en la rama htmlify
	01cbace HEAD@{12}: checkout: moving from master to htmlify
	01cbace HEAD@{13}: checkout: moving from styled to master
	a56bd9c HEAD@{14}: reset: moving to a56bd9c
	01cbace HEAD@{15}: reset: moving to HEAD~1
	a56bd9c HEAD@{16}: commit: Modificado archivo git-nuestro.md en la rama styled
	01cbace HEAD@{17}: checkout: moving from master to styled
	01cbace HEAD@{18}: commit (initial): Primer commit, moviendo git-nuestro.md al Repositorio
	
	Y ahora vuelvo al primer commit:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git checkout 01cbace
	Note: switching to '01cbace'.

	You are in 'detached HEAD' state. You can look around, make experimental
	changes and commit them, and you can discard any commits you make in this
	state without impacting any branches by switching back to a branch.

	If you want to create a new branch to retain commits you create, you may
	do so (now or later) by using -c with the switch command. Example:

	  git switch -c <new-branch-name>

	Or undo this operation with:

	  git switch -

	Turn off this advice by setting config variable advice.detachedHead to false

	HEAD is now at 01cbace Primer commit, moviendo git-nuestro.md al Repositorio
	
	Puedo comprobarlo:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git log
	commit 01cbace129caecab677dffcf60123e7621c12357 (HEAD)
	Author: Yolanda Mesa <yolimelo@gmail.com>
	Date:   Sun Jun 27 18:29:46 2021 +0200

		Primer commit, moviendo git-nuestro.md al Repositorio
	
- ¿Qué comando o comandos usaste en el punto 33? 
	Comprobamos:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git reflog
	01cbace (HEAD) HEAD@{0}: checkout: moving from master to 01cbace
	75194e9 (master) HEAD@{1}: checkout: moving from master to master
	75194e9 (master) HEAD@{2}: reset: moving to HEAD
	75194e9 (master) HEAD@{3}: reset: moving to HEAD~1
	f0a7aac HEAD@{4}: merge title: Merge made by the 'recursive' strategy.
	75194e9 (master) HEAD@{5}: checkout: moving from title to master
	b9026e2 HEAD@{6}: commit: Modificado archivo git-nuestro.md poni<C3><A9>ndole un titulo y estando en la rama title
	75194e9 (master) HEAD@{7}: checkout: moving from master to title
	75194e9 (master) HEAD@{8}: merge styled: Fast-forward
	01cbace (HEAD) HEAD@{9}: checkout: moving from styled to master
	75194e9 (master) HEAD@{10}: commit (merge): Commit que concluye el merge de la rama styled con la rama htmlify
	a56bd9c HEAD@{11}: checkout: moving from htmlify to styled
	2e9ca7a HEAD@{12}: commit: Modificado archico git-nuestro.md en la rama htmlify
	01cbace (HEAD) HEAD@{13}: checkout: moving from master to htmlify
	01cbace (HEAD) HEAD@{14}: checkout: moving from styled to master
	a56bd9c HEAD@{15}: reset: moving to a56bd9c
	01cbace (HEAD) HEAD@{16}: reset: moving to HEAD~1
	a56bd9c HEAD@{17}: commit: Modificado archivo git-nuestro.md en la rama styled
	01cbace (HEAD) HEAD@{18}: checkout: moving from master to styled
	01cbace (HEAD) HEAD@{19}: commit (initial): Primer commit, moviendo git-nuestro.md al Repositorio

	Nos posicionamos en ese momento:
	
	C:\Users\yolim\Desktop\Git y GitHub\Practica1GitGitHub\Practica1GitHub>git checkout b9026e2
	Previous HEAD position was 01cbace Primer commit, moviendo git-nuestro.md al Repositorio
	HEAD is now at b9026e2 Modificado archivo git-nuestro.md poniéndole un titulo y estando en la rama title



