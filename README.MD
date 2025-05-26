Inicio projeto: 23/05/25
# Aplicação em Django - projeto Alura

## Instalar pacotes (terminal)
- bootstrap: curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
- python: python3 get-pip.py
- ambiente virtual: pip install virtualenv
  
## Preparar ambiente (terminal)
- carregar arquivos (html/css) fornecidos
- iniciar ambiente virtual: source venv/bin/activate
- instalar Django: pip istall django
- visualizar dependencias necessarias: pip freeze
- boa pratica: 
  - criar um arquivo .txt e manter atualizado com os requerimentos: pip freeze > requirements.txt
- visualizar comandos django: django-admin help
- iniciar um projeto em django: django-admin startproject setup .
  - boa pratica: nomear arquivo como "config" ou "setup" para manter o codigo relacionado a      todas as configuração do projeto como um todo. e o ponto "." cria um arquivo separado.

## Informações:
- arquivo manage.py: responsavel por realizar a maioria dos comandos do Django assim como subir o servidor

## iniciar
- subir servidor: python manage.py runserver
- alterar timezone e language em /setup/settings.py: "internacionalization"

## versionar: 
Possibilitar envio do projeto para github sem expor dados sensiveis
- instalar pacote: pip install python-dotenv
- atualizar requerimentos: pip freeze > requirements.txt
- criar arquivo para armazenar secret key: ".env"
  - adcionar secret key (sem aspas)
- em "settings.py: 
  - adicionar "os" no import
  - remover a chave da variavel "Secret_key" e incluir: 
  SECRET_KEY = str(os.getenv('SECRET_KEY'))
  - adcionar: from dotenv import load_dotenv
  - adicionar: load_dotenv()
- 
# Testar
- python manage.py runserver

## versionar 2:
- criar arquivo gitignore na raiz do projeto
- na pagina: https://www.toptal.com/developers/gitignore
- incluir "django" na caixa de pesquisa e copiar todo item gerado
- colar o item gerado no arquivo .gitignore

## github
-  adicionar projetos no repositorio local:
  - git add .
  - git commit -m "projeto django"
  
- repositorio remoto:
- criar novo repositorio
  - copiar do repositorio: git remote add origin https://github.com/fqgiord/django_space.git 
  - git push origin master
  - ** PRONTO! Arquivos enviados para repositorio no github
  
## No projeto:
- criar pasta:  python manage.py startapp galeria
- setup/settings: adicionar em "INSTALLED_APPS": 'galeria'
- rodar programa: python manage.py runserver

# Dia 2: 24/05/25
## Modificar pagina
- /galeria/views.py adicionar: 
  from django.http import HttpResponse

def index(request):
    return HttpResponse('<h1>Pagina em Django,</h1>')

- /setup/urls.py adicionar em "urlpatterns":
  from galeria.views import index 
   path('', index),

- ## Atentar as boas praticas separando responsabilidades
- criado em /galeria: urls.py, que faz link com views.py 
- adicionado em /setup/urls.py: path('', include(galeria.urls')) para ler o conteudo das paginas que forem criadas em cada diretorio

# Vincular pagina html a Aplicação
- criado pasta: templates
- adicionado em /setup/settings.py: referencia para pasta templates:
  'DIRS': [os.path.join(BASE_DIR, 'templates')],
- adicionado codigo html

# confirmar passos a partir daqui:
- criar pasta static dentro da raiz do projeto
- colar pastas styles e assets para dentro do diretorio "static"
- rodar comando: python manage.py collectstatic
- embedar codigo html com python em /templates/index.html:  <link rel="stylesheet" href="{% static '/styles/style.css' %}">  
- rodar aplicação: python manage.py runserver