Essai gem dotenv

IMPORTANT : NE PAS PUSHER SUR GITHUB AVANT D'AVOIR MIT LE .ENV DANS LE .GITIGNORE !!!!!!!!!

ETAPES

# Création du dossier racine

# Création d'un fichier Gemfile et ajouter la gem 'dotenv'

# bundle install pour rendre dispo la gem 'dotenv' à tout le dossier
 	==> création d'un Gemfile.lock

# création d'un fichier .env où on stock ce que l'on ne veut pas pusher sur github
	==> mettre dedans les choses que l'on veut cacher, par ex clés APIs

# création d'un fichier .gitignore
	==> mettre dedans .env 
	==> c'est ce qui va faire que lors du push sur github, .env ne sera pas pushé, donc les clés APIs

# création d'un dossier lib

# création d'un fichier .rb
	==> pour connecter le fichier.rb au .env
	==> require 'dotenv'# Appelle la gem Dotenv

		Dotenv.load('.env') # Ceci appelle le fichier .env (situé dans le même dossier que celui d'où tu exécute app.rb)
		# et grâce à la gem Dotenv, on importe toutes les données enregistrées dans un hash ENV

		# Il est ensuite très facile d'appeler les données du hash ENV, par exemple là je vais afficher le contenu de la clé TWITTER_API_SECRET
		puts ENV['TWITTER_API_SECRET']

		#Autre exemple 
		puts ENV['BEST_WEBSITE_EVER']

# création repo github
# git init
# git remote add....
# git add
# git commit -m""
# git push origin master


