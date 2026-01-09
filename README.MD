# 🌌 Django Space Gallery

![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

## 📝 Sobre o Projeto

Aplicação web de galeria de imagens espaciais desenvolvida com Django, criada durante o curso da plataforma Alura. O projeto demonstra conceitos fundamentais do framework Django incluindo MVT (Model-View-Template), sistema de templates, gerenciamento de arquivos estáticos.

## ✨ Funcionalidades

- 🖼️ **Galeria de Imagens**: Visualização de imagens do espaço
- 🔍 **Sistema de Busca**: Filtro e pesquisa de imagens
- 👤 **Área Administrativa**: Painel admin do Django para gerenciamento
- 📱 **Design Responsivo**: Interface adaptável para diferentes dispositivos
- 🎨 **Templates Dinâmicos**: Sistema de templates com herança

## 🚀 Tecnologias Utilizadas

- **Python 3.x**: Linguagem de programação
- **Django 4.x**: Framework web
- **HTML5 & CSS3**: Frontend
- **JavaScript**: Interatividade
- **SQLite**: Banco de dados (desenvolvimento)

## 📁 Estrutura do Projeto

```
django_space/
├── setup/                  # Configurações do projeto Django
├── galeria/               # App principal
│   ├── templates/         # Templates HTML
│   ├── static/           # Arquivos estáticos (CSS, JS, imagens)
│   ├── models.py         # Modelos de dados
│   ├── views.py          # Views
│   └── urls.py           # Rotas
├── assets/                # Assets do projeto
├── static/               # Arquivos estáticos globais
├── manage.py
├── requirements.txt
└── README.md
```

## ⚙️ Como Executar

### Pré-requisitos
- Python 3.8+
- pip

### Instalação

1. Clone o repositório:
```bash
git clone https://github.com/fqgiord/django_space.git
cd django_space
```

2. Crie e ative um ambiente virtual:
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

4. Execute as migrações:
```bash
python manage.py migrate
```

5. Crie um superusuário (opcional):
```bash
python manage.py createsuperuser
```

6. Execute o servidor:
```bash
python manage.py runserver
```

Acesse em: `http://127.0.0.1:8000/`

## 🔐 Admin

Acesse o painel administrativo em: `http://127.0.0.1:8000/admin/`

## 📚 Aprendizados

Este projeto foi desenvolvido como parte do curso de Django da Alura e cobre:
- Arquitetura MVT do Django
- Sistema de templates e herança
- ORM do Django para manipulação de banco de dados
- Configuração de arquivos estáticos e media
- Django Admin customizado
- Boas práticas de desenvolvimento web

## 👨‍💻 Autor

**Fernando Giordano**
- GitHub: [@fqgiord](https://github.com/fqgiord)
- LinkedIn: [fernando-g-tech](https://www.linkedin.com/in/fernando-g-tech/)

## 📄 Licença

Este projeto está sob a licença MIT.

---

⭐ Desenvolvido com Django durante o curso da Alura
