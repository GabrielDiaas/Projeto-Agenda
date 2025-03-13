Iniciar o projeto Django

'''

python -m venv venv
.\venv\Scripts\Activate
pip install django
django-admin statproject project .
python manage.py startapp contact


'''

Configurar o git

'''

git config --global user.name 'Meu nome'
git config --global user.email 'meu e-mail'
git config --global init.defaultBranch main
git init
git add .
git commit -m 'Mensagem'
git remote add origin 'URL_DO_GIT'

'''

Migrando a base de dados do Django

'''

python manage.py makemigrations
python manage.py migrate

'''

Criando e modificando a senha de um super usuário Django

'''
python manage.py createsuperuser
python manage.py changepassword USERNAME

'''
