# Git / GitHub
## Exercice N°1
- ### Créez un nouveau repo GitHub appelé git-learning-1.
  #### gh repo create git-learning-1 --public
- ### Clonez le localement
  #### git clone < lien >
- ### Créez un fichier README.md with some text (exemple: "Mon premier projet Git")
  #### echo "Mon premier projet Git" > README.md
- ### Ajoutez une autre ligne au README.md (votre nom et le numéro de votre MAc), puis faites un commit, puis un push final
  #### echo "Almoustapha Moulaye Omar né à Agadez." >> README.md
  #### git add README.md
  #### git commit -m "Ajoute de mes informations."
  #### git push -u origin main(nom de la branch)
## Exercice N°2
- ### Depuis un repo clonez du nom: git-learning-2 que vous aurez créez, créez une nouvelle branche du nom de myself.
  #### gh repo create git-learning-2 --public
  #### git clone < lien >
  #### git checkout -b myself
- ### Créez un fichier about.txt avec des infos sur vous (nom, prénom, lieu de naissance...)
  #### echo "Almoustapha Moulaye Omar né à Agadez." > about.txt
- ### Faites un commit puis, puis pushez la branche myself.
  #### git add .
  #### git commit -m "ajout de mes information dans about."
  #### git push -u origin myself
- ### Faites un pull request de git-learning-2/myself -> main.
  #### gh pr create --base main --head myself --title "Ajout de mon profil" --body "Voici mes informations dans about.txt"
- ### Mergez le pull request.
  #### gh pr merge 1 (à travers le numéro du pr)
  #### gh pr merge --head myself (à travers le nom de la branche)
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