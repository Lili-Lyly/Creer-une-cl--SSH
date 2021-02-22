# Creer-une-cl--SSH

Créer une clé SSH
Cela peut être un peu intimidant, mais si vous suivez attentivement les étapes, vous devriez être en mesure de le faire fonctionner. (Si vous êtes bloqué, GitHub fournit également des instructions sur la configuration de SSH.)

Ouvrez le terminal.
N'importe où dans le Terminal, collez ce qui suit ssh-keygen -t rsa -b 4096 -C "PUT YOUR EMAIL HERE"et remplacez "METTEZ VOTRE EMAIL ICI" par l'e-mail que vous avez utilisé pour vous inscrire à GitHub.
Une fois que vous êtes invité à Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]appuyer sur Entrée.
Vous serez alors invité à entrer une phrase de passe. Appuyez simplement sur Entrée ici
Vous serez alors invité à saisir à nouveau une phrase de passe. Appuyez simplement sur Entrée ici aussi
Collez le texte suivant dans le terminal: eval "$(ssh-agent -s)". Si vous ne voyez pas de pidnombre, recommencez à partir de la première étape.
Collez le texte suivant dans le terminal: ssh-add ~/.ssh/id_rsa. si vous voyez un message d'erreur, recommencez à partir de la première étape.
Collez ce qui suit dans le terminal pbcopy < ~/.ssh/id_rsa.pub.
Rendez-vous sur votre compte GitHub (assurez-vous de vous connecter).
Dans le coin supérieur droit de n'importe quelle page, cliquez sur votre photo de profil, puis sur Paramètres.
Dans la barre latérale des paramètres utilisateur, cliquez sur Clés SSH et GPG.
Cliquez sur Nouvelle clé SSH ou Ajouter une clé SSH.
Dans le champ "Titre", ajoutez une étiquette descriptive pour la nouvelle clé. Par exemple, si vous utilisez un Mac personnel, vous pouvez appeler cette touche "Personal MacBook Air".
Collez votre clé dans le champ "Clé". (vous pouvez simplement cliquer avec le bouton droit de la souris et cliquer sur coller ou utiliser un raccourci clavier. La commande précédente a pbcopyfait la copie pour vous).
Cliquez sur Ajouter une clé SSH.
Si vous y êtes invité, confirmez votre mot de passe GitHub.
N'importe où dans le terminal, tapez ssh -T git@github.comet si vous voyez "Authentifié avec succès" (ignorez le reste du message), vous êtes prêt à partir! Si vous ne voyez pas cela, recommencez depuis le début.
Cela peut sembler pénible, mais heureusement, vous ne devez le faire qu'une seule fois. Une fois la connexion établie, vous pourrez pousser et tirer sans avoir à vous authentifier à chaque fois.
