# Git / GitHub
## Exercice N°3
- ### Créez un nouveau repo GitHub appelé git-learning-3.
  #### gh repo create git-learning-3 --public
- ### Sur la branche main, ajoutez un nouveau fichier notes.txt avec pour contenu "Ligne écrite depuis la branche main".
  #### git clone < lien >
  #### cd git-learning-3
  #### echo "Ligne écrite depuis la branche main" > notes.txt
- ### Faites un commit et pushez.
  #### git add notes.txt
  #### git commit -m "premier ligne du fichier notes"
  #### git push -u origin main
- ### Créez une branche conflict-test
  #### git checkout -b conflict-test
- ### Editez note.txt depuis la branche conflict-test et insérez y la phrase "Ligne écrite depuis la branche conflict-test".
  #### echo "Ligne écrite depuis la branche conflict-test" >> notes.txt
- ### Faites un commit et pushez.
  #### git add .
  #### git commit -m "deuxième ligne du notes"
  #### git push -u origin conflict-test
- ### Revenez à la branche main et remodifiez notes.txt différemment avec la phrase "Ligne écrite depuis la branche main pour la seconde fois".
  #### git checkout main
  #### echo "Ligne écrite depuis la branche main pour la seconde fois" >> notes.txt
- ### Faites un commit et pushez.
  #### git add .
  #### git commit -m "le deuxième ligne du fichier dans main"
  #### git push
- ### Essayez de merger la branche conflict-test dans main.
  #### git merge conflict-test (en étant dans main)
  ##### Après la resolution manuel
  #### git add .
  #### git commit -m "fusion de deux branches"
  #### git push
  <br><br>
  ![exercice3](exercice3.png)