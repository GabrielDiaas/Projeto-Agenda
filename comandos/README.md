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

Trabalhando com o model do Django

# Iniciando o shell o Django
python manage.py shell

# Importe o módulo
from contact.models import Contact

# Criar um contato (Lazy)
contact = Contact(**fields)
contact.save()

# Criar um contato (Não Lazy)
contact = Contact.objects.create(**fields)

# Selecionar um contato com id
# Retorna o contato
contact = Contact.objects.get(pk=10) # pode ser utilizado o ID ao invés de PK caso não tenha sido alterado a nomenclatura

# Editar um contato
# Retorna o contato
contact.field_name1 = 'Novo Valor 1'
contact.field_name2 = 'Novo Valor 2'
contact.save()

# Apaga um contato
# Depende da base de dados, geralmente retorna o número
# de valores manipulados na base de dados
contact.delete()

# Seleciona todos os contato ordenando por id DESC
# Retorna QuerySet[]
contacts = Contact.objects.all().order_by('-id)

# Seleciona contatos usando filtros
# Retorna QuerySet[]
contacts = Contact.objects.filter(**filters).order_by('-id')

