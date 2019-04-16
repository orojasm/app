git config --global user.name "David G."
git config --global user.email dave74@gmail.com
git config --global core.editor nano

mkdir app
cd app

touch README.md
touch .gitignore
git init
git add --all
git commit -m "first commit"
git remote add origin https://github.com/orojasm/app.git
git push -u origin master

git pull origin master
# Consulta de commits
git log
git log --oneline
# Copia del repositorio
git clone https://github.com/user/repo.git

# HTTPS + credential-osxkeychain
# Almacena user/pass en texto plano
git config --global credential.helper osxkeychain

# URL's Git sobre Secure Shell (SSH)
# Generando Claves SSH
ssh-keygen -t rsa -b 4096 -C "dave74@gmail.com"
# Añadir clave SSH a ssh-agent
ssh-add ~/.ssh/id_rsa
# Copiar clave SSH al portapapeles
pbcopy < ~/.ssh/id_rsa.pub

# Nueva Rama
git branch feature/sliderhome
# Git merge conflict
git merge iss53
Auto-merging index.html
CONFLICT (content): Merge conflict in index.html
Automatic merge failed; fix conflicts and then commit the result.
# Fixing Merge conflict,  Código sin conflicto
<<<<<<< HEAD
I love cats!
=======
Dogs are better
>>>>>>> Master (o SHA del commit)

# Pull Request
# Aportar una mejora al software existente.  Contribuir en un proyecto Open Source


