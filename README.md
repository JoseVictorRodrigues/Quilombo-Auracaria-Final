# Quilombo - Site Institucional

Este é o projeto do site institucional do Quilombo Auracária, desenvolvido com Django.

## Descrição

O site apresenta informações sobre o quilombo, incluindo seções de home, sobre, galeria de fotos, eventos, posts e contato. Possui um painel administrativo para gerenciamento de conteúdo.

## Funcionalidades

- **Página Inicial**: Apresentação do quilombo
- **Sobre**: Informações históricas e culturais
- **Galeria**: Fotos do quilombo
- **Eventos**: Agenda de eventos
- **Posts**: Notícias e atualizações
- **Contato**: Formulário de contato
- **Painel Administrativo**: Gerenciamento de conteúdo (usuários autenticados)

## Tecnologias Utilizadas

- **Backend**: Django 4.x
- **Banco de Dados**: SQLite (desenvolvimento) / PostgreSQL (produção)
- **Frontend**: HTML, CSS, JavaScript
- **Outros**: Google Calendar API (para sincronização de eventos)

## Instalação

### Pré-requisitos

- Python 3.8+
- Git
- Virtualenv (recomendado)

### Passos

1. Clone o repositório:
   ```bash
   git clone https://github.com/JoseVictorRodrigues/Quilombo-Auracaria-Final.git
   cd Quilombo-Auracaria-Final
   ```

2. Crie e ative um ambiente virtual:
   ```bash
   python -m venv .venv
   # No Windows:
   .venv\Scripts\activate
   # No Linux/Mac:
   source .venv/bin/activate
   ```

3. Instale as dependências:
   ```bash
   pip install -r quilombo_site/requirements.txt
   ```

4. Execute as migrações do banco de dados:
   ```bash
   cd quilombo_site
   python manage.py migrate
   ```

5. Crie um superusuário (opcional, para acessar o admin):
   ```bash
   python manage.py createsuperuser
   ```

6. Execute o servidor de desenvolvimento:
   ```bash
   python manage.py runserver
   ```

7. Acesse o site em: http://127.0.0.1:8000/

## Estrutura do Projeto

```
quilombo_site/
├── apps/
│   ├── core/          # App principal (home, sobre, galeria, contato)
│   ├── eventos/       # Gerenciamento de eventos
│   ├── posts/         # Sistema de posts/notícias
│   └── usuarios/      # Autenticação e painel do usuário
├── docs/              # Documentação
├── logs/              # Arquivos de log
├── media/             # Arquivos de mídia (fotos, etc.)
├── static/            # Arquivos estáticos (CSS, JS, imagens)
├── templates/         # Templates HTML
├── manage.py          # Script de gerenciamento Django
└── settings.py        # Configurações do projeto
```

## Configuração

### Configurações do Site

As configurações gerais do site podem ser alteradas no painel administrativo em `/admin/core/configuracaosite/`.

### Sincronização de Eventos

Para sincronizar eventos com o Google Calendar, configure as credenciais no arquivo `settings.py` e execute:

```bash
python manage.py sync_calendar
```

## Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

## Contato

Para dúvidas ou sugestões, entre em contato através do formulário no site ou envie um email para [seu-email@exemplo.com].

## Documentação Técnica

Para mais detalhes técnicos, consulte os arquivos em `docs/`:
- `DOCUMENTACAO_TECNICA.md`
- `GUIA_DO_SITE.md`