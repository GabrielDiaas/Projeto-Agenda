Iniciar o projeto Django

'''

python -m venv venv
.\venv\Scripts\Activate
pip install django
django-admin statproject project .

Configurar o git

'''

git config --global user.name 'Gabriel Dias'
git config --global user.email 'gsd_gabriel@hotmail.com'
git config --global init.defaultBranch main
git init
git add .
git commit -m 'Mensagem'
git remote add origin git@github.com:GabrielDiaas/Projeto-Agenda.git

'''