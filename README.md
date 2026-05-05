# Orbia

![Django](https://img.shields.io/badge/Django-5.2-092E20?logo=django&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?logo=bootstrap&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-4-FF6384?logo=chartdotjs&logoColor=white)
![Leaflet](https://img.shields.io/badge/Leaflet-1.9-199900?logo=leaflet&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-blue)
![Status](https://img.shields.io/badge/status-portfolio-purple)

> Plataforma corporativa para gestÃ£o de empresas, projetos, pesquisas e relatÃ³rios â€” em um Ãºnico fluxo.

---

## ðŸ“– DescriÃ§Ã£o

**Orbia** Ã© uma plataforma web full-stack desenvolvida em Django 5 que centraliza a operaÃ§Ã£o de uma organizaÃ§Ã£o em um Ãºnico painel: cadastro e geolocalizaÃ§Ã£o de empresas, gestÃ£o de projetos por status, pesquisas estruturadas com histÃ³rico, dashboards com mÃ©tricas em tempo real, mapas interativos e exportaÃ§Ã£o para CSV/PDF.

A interface adota uma estÃ©tica **dark moderna** com efeitos de glassmorphism, gradientes e tipografia Inter, oferecendo uma experiÃªncia polida tanto em desktop quanto em dispositivos mÃ³veis.

---

## ðŸªª Contexto e Autoria

Este projeto Ã© uma versÃ£o prÃ³pria, refatorada e adaptada para portfÃ³lio, baseada em um sistema acadÃªmico desenvolvido em equipe durante o curso. No projeto original, atuei como principal responsÃ¡vel por toda a camada de frontend, incluindo identidade visual, templates Django, landing page, dashboard, formulÃ¡rios, telas de autenticaÃ§Ã£o, pÃ¡ginas pÃºblicas e experiÃªncia do usuÃ¡rio. AlÃ©m disso, contribuÃ­ diretamente em funcionalidades de backend, como autenticaÃ§Ã£o, recuperaÃ§Ã£o de senha, upload de mÃ­dia, rotas, seeders, estatÃ­sticas dinÃ¢micas, filtros avanÃ§ados, integraÃ§Ã£o com Chart.js, geolocalizaÃ§Ã£o com geopy, mapas interativos com Leaflet.js e controle de acesso.

- **Autor (portfÃ³lio):** Matheus Beiruth â€” [@BeiruthDEV](https://github.com/BeiruthDEV)
- **RepositÃ³rio:** https://github.com/BeiruthDEV/orbia
- **Projeto original (em equipe):** https://github.com/JoaoLopes07/projeto-integrador-curso

---

## âœ¨ Funcionalidades

- ðŸ” **AutenticaÃ§Ã£o completa** â€” login, registro, recuperaÃ§Ã£o de senha por e-mail, logout, alteraÃ§Ã£o de senha
- ðŸŒ **Login social** â€” Google e GitHub via `django-allauth`
- ðŸ‘¥ **Controle de acesso por papÃ©is** â€” Diretoria, Associado, Afiliado (cada papel com permissÃµes e dashboards prÃ³prios)
- ðŸ¢ **GestÃ£o de empresas** â€” cadastro com CNPJ, razÃ£o social, Ã¡rea de atuaÃ§Ã£o, contato, redes sociais e endereÃ§o completo
- ðŸ—ºï¸ **GeolocalizaÃ§Ã£o automÃ¡tica** â€” geocoding via `geopy` + Nominatim ao salvar a empresa
- ðŸ“ **Mapa interativo** â€” `Leaflet.js` com pinos por empresa, popups com link para o site
- ðŸ“Š **Dashboards** â€” mÃ©tricas consolidadas, grÃ¡ficos `Chart.js` (top cidades, status de projetos, distribuiÃ§Ã£o por estado)
- ðŸ“‹ **GestÃ£o de projetos** â€” CRUD vinculado Ã  empresa, status (Planejamento / Em Desenvolvimento / Finalizado)
- ðŸ“ **Pesquisas anuais** â€” formulÃ¡rio pÃºblico, histÃ³rico, controle de submissÃ£o Ãºnica, relatÃ³rios pÃºblicos
- ðŸ”Ž **Filtros avanÃ§ados** â€” busca por estado, cidade (carregamento dinÃ¢mico), status no diretÃ³rio pÃºblico
- ðŸ“¤ **ExportaÃ§Ã£o** â€” CSV e PDF (via `xhtml2pdf`) para empresas e projetos
- ðŸ“· **Upload de avatar de usuÃ¡rio** â€” armazenado em `/media`
- ðŸ“± **UI responsiva** â€” Bootstrap 5 + estÃ©tica dark com glassmorphism
- ðŸ›¡ï¸ **Hardening bÃ¡sico** â€” `whitenoise` para estÃ¡ticos em produÃ§Ã£o, `CompressedManifestStaticFilesStorage`, secrets via env

---

## ðŸ§° Tech Stack

| Camada            | Ferramenta                                                  |
|-------------------|-------------------------------------------------------------|
| Backend           | Python 3.11+, Django 5.2                                    |
| Auth              | `django-allauth` (Google + GitHub), `djangorestframework_simplejwt` |
| Forms             | `django-crispy-forms` + `crispy-bootstrap5`                 |
| Banco (dev)       | SQLite                                                      |
| Banco (prod)      | PostgreSQL via `dj-database-url` + `psycopg`                |
| EstÃ¡ticos         | `whitenoise`                                                |
| PDF               | `xhtml2pdf`                                                 |
| Imagens           | `Pillow`                                                    |
| Geocoding         | `geopy` (Nominatim/OpenStreetMap)                           |
| Frontend          | Bootstrap 5.3, Font Awesome 6, Inter (Google Fonts)         |
| Mapas             | `Leaflet.js` 1.9                                            |
| GrÃ¡ficos          | `Chart.js` 4                                                |
| Servidor (prod)   | `gunicorn`                                                  |
| Config            | `python-dotenv`                                             |

---

## ðŸ“ Estrutura de Pastas

```
orbia/
â”œâ”€â”€ accounts/                   # Custom user, auth views, perfis, signals
â”œâ”€â”€ companies/                  # Empresas + Representantes (geocoding no save)
â”œâ”€â”€ projects/                   # CRUD de projetos vinculados Ã  empresa
â”œâ”€â”€ surveys/                    # Pesquisas, histÃ³rico, relatÃ³rios pÃºblicos
â”œâ”€â”€ public/                     # Landing, mapa, diretÃ³rio, estatÃ­sticas
â”œâ”€â”€ core/                       # Permissions, utils, comandos (setup_roles, setup_social_login)
â”œâ”€â”€ meuprojeto/                 # Settings, urls, wsgi, asgi do projeto Django
â”œâ”€â”€ templates/                  # Templates HTML centralizados
â”‚   â”œâ”€â”€ accounts/               # login, register, home, profile, change_password
â”‚   â”œâ”€â”€ companies/              # company_list, company_form, company_public_register
â”‚   â”œâ”€â”€ projects/               # project_list, project_detail, project_form
â”‚   â”œâ”€â”€ surveys/                # survey_form, history, success, report
â”‚   â”œâ”€â”€ public/                 # landing, mapa, diretÃ³rio, estatÃ­sticas
â”‚   â”œâ”€â”€ registration/           # password reset (4 telas)
â”‚   â”œâ”€â”€ representante/          # CRUD de representantes
â”‚   â”œâ”€â”€ dashboard/diretoria/    # painel administrativo
â”‚   â””â”€â”€ base.html               # layout raiz
â”œâ”€â”€ static/                     # CSS + assets (style.css, orbia-icon.png)
â”œâ”€â”€ media/                      # uploads de usuÃ¡rios (avatar etc.)
â”œâ”€â”€ manage.py

```

---

## ðŸš€ Como rodar localmente

### 1. Clonar o repositÃ³rio

```bash
git clone https://github.com/BeiruthDEV/orbia.git
cd orbia
```

### 2. Criar e ativar ambiente virtual

**Windows (PowerShell)**
```powershell
python -m venv venv
venv\Scripts\Activate.ps1
```

**Linux / macOS**
```bash
python -m venv venv
source venv/bin/activate
```

### 3. Instalar dependÃªncias

```bash
pip install -r requirements.txt
```

### 4. Configurar variÃ¡veis de ambiente

```bash
cp .env.example .env       # Linux/macOS
copy .env.example .env     # Windows
```

Edite o `.env` e gere uma `SECRET_KEY` real:
```bash
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
```

### 5. Aplicar migraÃ§Ãµes e criar superusuÃ¡rio

```bash
python manage.py migrate
python manage.py createsuperuser
```

### 6. (Opcional) Configurar papÃ©is e providers sociais

```bash
python manage.py setup_roles
python manage.py setup_social_login
```

### 7. Subir o servidor

```bash
python manage.py runserver
```

Acesse: <http://127.0.0.1:8000/>

---

## ðŸ” VariÃ¡veis de Ambiente

Veja `.env.example` para a lista completa documentada. Resumo:

| VariÃ¡vel                   | ObrigatÃ³ria | DescriÃ§Ã£o                                           |
|----------------------------|-------------|-----------------------------------------------------|
| `SECRET_KEY`               | âœ…           | Chave criptogrÃ¡fica do Django                       |
| `DEBUG`                    | âœ…           | `True` em dev, `False` em produÃ§Ã£o                  |
| `ALLOWED_HOSTS`            | âœ…           | Hosts separados por vÃ­rgula                         |
| `DATABASE_URL`             | prod        | URL completa do Postgres (vazio = SQLite local)     |
| `SITE_ID`                  | â€”           | ID do site para `django.contrib.sites` (default: 1) |
| `EMAIL_HOST` / `EMAIL_PORT`| prod        | SMTP de envio de e-mails                            |
| `EMAIL_HOST_USER` / `_PASSWORD` | prod   | Credenciais SMTP                                    |
| `DEFAULT_FROM_EMAIL`       | prod        | EndereÃ§o remetente padrÃ£o                           |
| `EMAIL_TIMEOUT`            | â€”           | Timeout SMTP em segundos (default: 10)              |
| `RENDER_EXTERNAL_HOSTNAME` | auto        | Injetado pela Render â€” nÃ£o setar manualmente        |

> âš ï¸ Em desenvolvimento, **nÃ£o defina `DATABASE_URL`**. O `settings.py` levanta `RuntimeError` se `DEBUG=True` e `DATABASE_URL` estiver presente, para evitar tocar produÃ§Ã£o sem querer.

---

## ðŸ› ï¸ Comandos Ãºteis

```bash
# MigraÃ§Ãµes
python manage.py makemigrations
python manage.py migrate

# SuperusuÃ¡rio
python manage.py createsuperuser

# Setup inicial (papÃ©is + login social)
python manage.py setup_roles
python manage.py setup_social_login

# Coletar estÃ¡ticos para produÃ§Ã£o
python manage.py collectstatic --noinput

# Testes
python manage.py test
```

---

## ðŸ“¸ Screenshots

> _Substitua os placeholders abaixo pelos prints reais ao publicar o repositÃ³rio._

| Tela                | Preview                                                                 |
|---------------------|-------------------------------------------------------------------------|
| Landing page        | ![Landing](https://placehold.co/800x420/0a0a0a/a742f5?text=Landing+Page) |
| Dashboard           | ![Dashboard](https://placehold.co/800x420/0a0a0a/FF6B6B?text=Dashboard) |
| Login               | ![Login](https://placehold.co/800x420/0a0a0a/a742f5?text=Login)         |
| DiretÃ³rio pÃºblico   | ![Directory](https://placehold.co/800x420/0a0a0a/2dce89?text=Directory) |
| Mapa interativo     | ![Map](https://placehold.co/800x420/0a0a0a/4361ee?text=Mapa)            |
| EstatÃ­sticas        | ![Stats](https://placehold.co/800x420/0a0a0a/fb6340?text=Charts)        |

---

## ðŸ—ºï¸ PrÃ³ximas Melhorias

- [ ] SuÃ­te de testes mais ampla (cobrir views/permissions de cada app)
- [ ] API REST pÃºblica com `djangorestframework` (jÃ¡ instalado) + JWT
- [ ] InternacionalizaÃ§Ã£o â€” atualmente fixado em `pt-br`, expor `en`
- [ ] CI/CD: GitHub Actions com lint (`ruff`) + testes em PR
- [ ] ContainerizaÃ§Ã£o â€” `Dockerfile` + `docker-compose.yml` para Postgres local
- [ ] Logging estruturado (substituir `print()` por `logging` em `companies/models.save`)
- [ ] Cache de geocoding para evitar chamadas repetidas ao Nominatim
- [ ] Acessibilidade (WAI-ARIA) â€” auditar formulÃ¡rios e contraste
- [ ] PWA â€” `manifest.json` + service worker para uso offline bÃ¡sico

---

## ðŸ“„ LicenÃ§a

MIT â€” uso livre para fins de portfÃ³lio e estudo.
