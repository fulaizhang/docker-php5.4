# Notes pour l'utilisation du docker

Une base de données vide est initialisée au build du docker. Le nom de la base est `db`, le mot de passe `dbpassword`.


## Exemple de build & run
### Build
docker build -t generic-php54 .

### Run (après chaque build)
docker run --name="php54" -d -p 3354:3306 -p 9054:9000 -p 44354:443 -p 8054:80 -t -i -v /var/www/host:/var/www/html -v $SSH_AUTH_SOCK:/ssh-agent --env SSH_AUTH_SOCK=/ssh-agent generic-php54
