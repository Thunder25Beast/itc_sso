# 🔐 SSO: One Login To Rule Them All

A Django-powered Single Sign-On (SSO) service that lets you authenticate once and rule all your applications. Because who has time to remember multiple passwords?

![SSO Flow Diagram](/static/img/sso-flow.png)

## 🚀 Features That Make Life Easier

- **Seamless Authentication**: One account to access them all, one password to find them
- **Session Management**: Keep track of who's who in your digital kingdom
- **API Integration**: RESTful endpoints that play nice with others
- **Security First**: Because we care about your digital well-being
- **User Management**: Control who gets the keys to your kingdom

## 🛠️ Tech Stack

- **Backend**: Django 4.x (Because Python is love ❤️)
- **Database**: PostgreSQL (The elephant that never forgets 🐘)
- **Cache**: Redis (Because speed is what you need ⚡)
- **API**: Django REST Framework (RESTful done right ✨)

## 🏃‍♂️ Quick Start

1. Clone this bad boy:

   ```bash
   git clone https://github.com/devclub-iitd/itc_sso.git
   cd itc_sso
   ```

2. Set up your virtual environment (because isolation is good):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Create your `.env` file (shhh... it's a secret):

   ```bash
   cp .env.example .env
   # Edit .env with your super secret configurations
   ```

5. Run migrations:

   ```bash
   python manage.py migrate
   ```

6. Create a superuser (with great power comes great responsibility):

   ```bash
   python manage.py createsuperuser
   ```

7. Launch the rocket:

   ```bash
   python manage.py runserver
   ```

8. Access the application at `http://127.0.0.1:8000`.

## 🔌 Integration

### Client Side

```python
from sso_client import SSOClient

sso = SSOClient(
    client_id="your_client_id",
    client_secret="your_client_secret"
)

# Magic happens here
user = sso.authenticate(token)
```

### Server Side

```python
@login_required
def your_protected_view(request):
    return HttpResponse("If you see this, you're authenticated! 🎉")
```

## 🔒 Security Features

- JWT-based authentication (because we're fancy)
- Rate limiting (to keep the bad guys at bay)
- Session encryption (your secrets are safe with us)
- CORS protection (because boundaries are important)

## 🌐 API Endpoints

| Endpoint            | Method | Description            |
| ------------------- | ------ | ---------------------- |
| `/api/auth/login/`  | POST   | Get your golden ticket |
| `/api/auth/verify/` | POST   | Make sure you're you   |
| `/api/user/data/`   | GET    | Get the user details   |

## 🤝 Contributing

1. Fork it (because sharing is caring)
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request (let's make this project awesome together!)

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Coffee ☕ - For making this possible
- Stack Overflow 🚀 - Our faithful companion
- Bug reporters 🐛 - For keeping us humble

## 🤔 Need Help?

- 📚 Check out our [Documentation](https://sso.devclub.in/docs)
- 🐞 Found a bug? [Open an issue](https://github.com/devclub-iitd/SingleSignOn/issues)
- 💬 Want to contribute? Join our [Discord](https://discord.gg/devclub)

---

Made with ❤️ by [ITC Web Team](https://web.tech-iitb.org)

_Remember: In a world full of passwords, be the SSO provider!_ 🦸‍♂️

## Folder Structure

```bash
django-sso-app/
│
├── sso_app/                  # Django app for SSO
│   ├── migrations/           # Django migration files
│   ├── templates/            # HTML templates
│   ├── __init__.py           # Python init file
│   ├── admin.py              # Django admin configurations
│   ├── apps.py               # App configuration
│   ├── forms.py              # Forms for registration, login, etc.
│   ├── models.py             # Models for user profiles
│   ├── urls.py               # URL routes
│   ├── views.py              # Views for handling HTTP requests
│
├── static/                   # Static assets (CSS, JS)
├── templates/                # Project-wide templates
│
├── manage.py                 # Django management script
├── .env                      # Environment variables
├── .gitignore                # Files and directories to ignore in Git
├── README.md                 # Project documentation
├── requirements.txt          # Python dependencies
├── db.sqlite3                # SQLite database (can be changed)
└── sso_project/              # Project root directory
    ├── __init__.py
    ├── settings.py           # Django settings
    ├── urls.py               # Root URLs
    └── wsgi.py               # WSGI entry point

```
