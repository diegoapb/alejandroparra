---
title: Introduction Django Project
date: "2015-05-28T22:40:32.169Z"
description: This is a little project, based on instagram and devolped in django.
---
# Cimientos

## IMPORTANTE

## Resumen Cimientos

[Django Avanzado - Slides P1.pdf](Cimientos%204865b7486a354b89b1379cedbb49ff74/Django_Avanzado_-_Slides_P1.pdf)

.

Comandos iniciales

- Descargar Codigo

> `git clone https://github.com/pablotrinidad/cride-platzi.git`

- exec

> `cd cride`
`docker-compose -f local.yml build`

## 1 Introduccion

**Palabras Clave:**

- Historias de usuario
- Funcionalidades
- Temas iniciales

**Resumen:** 

**Documentacion:**

**Notas:**

- 5.00 Explicacion del proyecto final
- 5.48 ¿Como funciona? Historias Epicas de la aplicacion
- 6.40 Modelo de usuarios
- 7.37 Modelo de "Circulos" grupos de rides
- 8.20 Modelo de "Rides" o viajes compartidos.
- 9.00 Funcionalidades de Usuarios5
- 9.17 Funcionalidades de Circulos
- 9.40 Funcionalidades de Rides
- 9.57 Funcionalidades extras
    - Administracion de admins
    - Despliege en aws
- 11.14 Contenido

---

---

## [2 Arquitectura de una aplicación](https://platzi.com/clases/1461-django-avanzado/17209-arquitectura-de-una-aplicacion/)

**Palabras Clave:**

El **Backend** consiste en:

- Servidor
- Aplicación
- Base de Datos

- APIs
    - SOPA
    - REST
    - GraphQL x Facebook

**Resumen:** El objetivo de este curso es convertirte en un Backend profesional que usa Django como su herramienta profesional.

Un Backend developer es un diseñador, su trabajo consiste un 90% en leer, diseñar, analizar y planear. Un 10% en programar. Nuestro trabajo más importante es el diseño del sistema y las decisiones tomadas son más costosas y más difíciles de cambiar.

Web Services es la manera en que se implementan las arquitecturas orientadas a servicios, se crean bloques que son accesibles a través de la web, son independientes del lenguaje de programación.

**Documentacion:**

Lecturas Recomendadas:

[Web Tools APIs | USPS](https://www.usps.com/business/web-tools-apis/welcome.htm) Servicio postal de estados unidos

[Graph API - Documentation - Facebook for Developers](https://developers.facebook.com/docs/graph-api/) - Hablan de las buenas practicas para crear una graphql api

[GitHub GraphQL API v4 | GitHub Developer Guide](https://developer.github.com/v4/) - 

[GitHub - kamranahmedse/developer-roadmap: Roadmap to becoming a web developer in 2019](https://github.com/kamranahmedse/developer-roadmap)

[2.- Arquitectura de una aplicación - Google Slides](https://docs.google.com/presentation/d/1HlT7niPOISnHjk6ldbmCvZdiOeKqlzLNxfsGY5499_E/edit?usp=sharing)

**Notas:**

- 1.32 Roadmap → Carrera de un FullStack Developer
- 5.00 Arquitectura
    - Monolitica: Fuertemente acoplada a la base de datos y cualquier otro servicio que use, Todo esta **en un solo servidor.**
    - Distribuida: Los servicios estan distribuidos en la red, como la base de datos en otro lugar
    - Hibrida: el backend esta haciendo rendering en el frontend, el cliente se comunica directamente con el Bakend.
    - Orientada a Servicios:
        - Autocontenida
        - Caja negra
        - Representa una actividad de negocio especifica
- Estandares de Arquitectura SOA
    - SOAP → En desuso antiguo
    - RESTfulHTTP → Esta enfocada en el HTTP, Es en la que profundizaremos
    - GraphQL → Esta orientada por facebook, se enfoca en trabajar como un lenguaje de consulta para las APIs
    - Mas Informacion
        - SOAP ([https://www.usps.com/business/web-tools-apis/welcome.htm](https://www.usps.com/business/web-tools-apis/welcome.htm))
        - RESTful HTTP ([https://developers.facebook.com/docs/graph-api/](https://developers.facebook.com/docs/graph-api/))
        - GraphQL ([https://developer.github.com/v4/](https://developer.github.com/v4/))

---

---

## [3 The Twelve-Factor App](https://platzi.com/clases/1461-django-avanzado/17140-the-tlwelve-factor-app/)

**Palabras Clave:**

- SAAS
- Principios basicos
- 

- API
- HTTP
- Metodologia

**Resumen:** Algunos principios de Twelve Factor app
En el proyecto vamos a construir una API en la teoria estas aplicaciones construidas con apis son nombradas SAAS (Software as a Services) y **The Twelve-Factor App** Es una metodologia de desarrolla para aplicaciones SAAS. Esta metodologia ha sido formada por la contribuciones de muchas personas, mayoritariamente desarrolladores de Heroku.

**Documentacion:**

- [The Twelve-Factor App](https://12factor.net/) - Pagina oficial de la metodologia de desarrollo de SAAS

    Este documento sintetiza toda nuestra experiencia y observaciones sobre una amplia variedad de aplicaciones de software como servicio en la naturaleza. Es una triangulación de prácticas ideales para el desarrollo de aplicaciones, prestando especial atención a la dinámica del crecimiento orgánico de una aplicación a lo largo del tiempo, la dinámica de colaboración entre los desarrolladores que trabajan en el código base de la aplicación y evitando el costo de la erosión del software .

**Notas:**

- 0.30 Principios
    - Formas **declarativas** de configuracion: Minimizamos el tiempo que le toma a un desarrollador correr nuestro proyecto
    - Un **contrato claro** con el OS: Ofrecer maxima portabilidad.
    - Listas para **lanzar. El developer tiene que poder lanzar la aplicacion**
    - Minimizar la **diferencia** entre **entornos:** Generar un pipeland de continues deliver, consecuente a esto aumentamos la agilidad.
    - Facil de **escalar:** Evitaremos cambiar la arquitectura.
- 1.54 Los 12 Factores:

    ![Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_12.30.42_p._m..png](Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_12.30.42_p._m..png)

    [I. Código base (Codebase)](https://12factor.net/es/codebase)

    Un código base sobre el que hacer el control de versiones y multiples despliegues. 

    Solo hay un git con el codigo base.

    [II. Dependencias](https://12factor.net/es/dependencies)

    Declarar y aislar explícitamente las dependencias

    como el `package.json` de node.js.

    y **aislamos** usando un virtual env o docker

    [III. Configuraciones](https://12factor.net/es/config)

    Guardar la configuración en el entorno.

    Cada entorno debe llevar su configuracion, llaves usuarios etc

    [IV. Backing services](https://12factor.net/es/backing-services)

    Tratar a los “backing services” como recursos conectables.

    EJEMPLO :Servicios de emails → Debe ser muy facil de cambiar de servicio.

    [V. Construir, desplegar, ejecutar](https://12factor.net/es/build-release-run)

    Separar completamente la etapa de construcción de la etapa de ejecución.

    Build → es la parte donde compilamos nuestro codigo

    Relase→ Es la parte donde incluimos las variables de entorno dentro de nuestro paquete.

    Run → Donde corremos la aplicacion en el entorno que se va a ejecutar. 

    Es muy importante mantener esta etapas totalmente separadas, no escribir codigo de una etapa en otra.

    [VI. Procesos](https://12factor.net/es/processes)

    Ejecutar la aplicación como uno o más procesos sin estado.

    No requerimos el almacenamiento de estados en memoria, de ser asi debemos almacenarlo en el backend

    Procesos **Stateless**

    [VII. Asignación de puertos](https://12factor.net/es/port-binding)

    Publicar servicios mediante asignación de puertos.

    Se le debe asignar un puerto por el que la aplicacion escuchara las peticiones

    [VIII. Concurrencia](https://12factor.net/es/concurrency)

    Escalar mediante el modelo de procesos.

    Podemos escalar un solo proceso en varias cargas usando hilos para distribuir mejor la carga.

    ![Cimientos%204865b7486a354b89b1379cedbb49ff74/process-types.png](Cimientos%204865b7486a354b89b1379cedbb49ff74/process-types.png)

    [IX. Desechabilidad](https://12factor.net/es/disposability)

    Hacer el sistema más robusto intentando conseguir inicios rápidos y finalizaciones seguras.

    Los procesos pueden iniciarse o finalizarse en el momento que sea necesario. Esto permite un escalado rápido y flexible.

    [X. Paridad en desarrollo y producción](https://12factor.net/es/dev-prod-parity)

    Mantener desarrollo, preproducción y producción tan parecidos como sea posible.
    
    

    Reduccion de tiempos en deploys.

    [XI. Historiales](https://12factor.net/es/logs)

    Tratar los historiales como una transmisión de eventos.

    Nos permiten testear el comportamiento de la aplicacion durante su ejecucion.
    
    
    
    [XII. Administración de procesos](https://12factor.net/es/admin-processes)

    Ejecutar las tareas de gestión/administración como procesos que solo se ejecutan una vez

    Procesos como el Backup de base de datos no deben estar en la app, se manejaran como procesos externos.

---

---

## [4 Codebase: Settings modular](https://platzi.com/clases/1461-django-avanzado/17139-codebase-settings-modular/)

Empezamos con el Codigo !! 

**Palabras Clave:**

- Esctructura (esqueleto)
- Esquema de carpetas
- Codigo

- Codigo

Entorno de:

- Production
- Test
- local

**Resumen:** Veremos el esquema de carpetas en donde se enfocan los archivos para la configuracion de los entornos de desarrollo, pruebas y produccion

Analizaremos a detalle cada uno de los archivos con los settings necesarios para llevar a cabo el funcionamiento del servidor.

**Documentacion:**

- Lecturas Recomendadas

    [joke2k/django-environ](https://github.com/joke2k/django-environ)

    [django-extensions/django-extensions](https://github.com/django-extensions/django-extensions)

    [anymail/django-anymail](https://github.com/anymail/django-anymail)

    [](https://github.com/jschneier/django-storages)

    [Get Docker](https://docs.docker.com/install/#supported-platforms)

    [Install Docker Compose](https://docs.docker.com/compose/install/)

    [joke2k/django-environ](https://github.com/joke2k/django-environ)

    [anymail/django-anymail](https://github.com/anymail/django-anymail)

**Notas:**

- 0.30 Porque usar Docker? Requisitos
    - Docker
    - Docker Compose
- 1.10 Servicios docker.

    S50

    Celery : Contiene 3 servicios, Flower es una interfaz virtual que nos permite ver que esta sucediendo con django.

    ![Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_1.56.53_p._m..png](Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_1.56.53_p._m..png)

2.22 Primeros pasos

- Descargar Codigo

> `git clone https://github.com/pablotrinidad/cride-platzi.git`

- exec

> `cd cride`
`docker-compose -f local.yml build`

- 2.50 Explicacion del esquema : **Config**

    ![Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_2.19.15_p._m..png](Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_2.19.15_p._m..png)

    - Arvhicos base de django, `settings` es un folder compuesto por varios archivos
        - `/base.py`

            ```python
            """Base settings to build other settings files upon."""

            import environ # libreria que nos permite hacer resta de pads

            ROOT_DIR = environ.Path(__file__) - 3 # directorio base
            APPS_DIR = ROOT_DIR.path('cride') # directiorio de paths donde se encuentran las apps en este caso cride

            env = environ.Env() 

            # Base
            DEBUG = env.bool('DJANGO_DEBUG', False)# Trae una variable bolleana que se llama DJANGO_DEBUG, o en el caso que no exista pone FALSE

            # Language and timezone
            TIME_ZONE = 'America/Mexico_City'
            LANGUAGE_CODE = 'en-us'
            SITE_ID = 1
            USE_I18N = True
            USE_L10N = True
            USE_TZ = True

            # DATABASES
            DATABASES = { # Con el env traemos esa URL con todo lo que django necesita
                'default': env.db('DATABASE_URL'),
            }
            DATABASES['default']['ATOMIC_REQUESTS'] = True # Configuramos transacciones atomicas en nuestra base de datos

            # URLs donde esta nuestro modulo de urls
            ROOT_URLCONF = 'config.urls'

            # WSGI Donde esta nuestro modulo WSGGI
            WSGI_APPLICATION = 'config.wsgi.application'

            # Apps 
            DJANGO_APPS = [
                'django.contrib.auth',
                'django.contrib.contenttypes',
                'django.contrib.sessions',
                'django.contrib.messages',
                'django.contrib.staticfiles',
                'django.contrib.admin',
            ]

            THIRD_PARTY_APPS = [
            ]
            LOCAL_APPS = [
            ]
            # Las aplicaciones instaaladas se definen como una suma de aplicaciones
            # django 2.1 
            INSTALLED_APPS = DJANGO_APPS + THIRD_PARTY_APPS + LOCAL_APPS

            # Passwords
            PASSWORD_HASHERS = [
            #Primero usamos el argon 2 si no se usan los demas
                'django.contrib.auth.hashers.Argon2PasswordHasher',
                'django.contrib.auth.hashers.PBKDF2PasswordHasher',
                'django.contrib.auth.hashers.PBKDF2SHA1PasswordHasher',
                'django.contrib.auth.hashers.BCryptSHA256PasswordHasher',
                'django.contrib.auth.hashers.BCryptPasswordHasher',
            ]
            AUTH_PASSWORD_VALIDATORS = [
                {
                    'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
                },
                {
                    'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
                },
                {
                    'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
                },
                {
                    'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
                },
            ]

            # Middlewares
            MIDDLEWARE = [
                'django.middleware.security.SecurityMiddleware',
                'django.contrib.sessions.middleware.SessionMiddleware',
                'django.middleware.common.CommonMiddleware',
                'django.middleware.csrf.CsrfViewMiddleware',
                'django.contrib.auth.middleware.AuthenticationMiddleware',
                'django.contrib.messages.middleware.MessageMiddleware',
                'django.middleware.clickjacking.XFrameOptionsMiddleware',
            ]

            # Static files
            **#Aqui no vamos a manejar archivos estaticos ya que es una API**
            STATIC_ROOT = str(ROOT_DIR('staticfiles')) # Los archivos estaticos se pueden encontrar en el folder base en el static
            STATIC_URL = '/static/'
            STATICFILES_DIRS = [
                str(APPS_DIR.path('static')),
            ]
            STATICFILES_FINDERS = [
                'django.contrib.staticfiles.finders.FileSystemFinder',
                'django.contrib.staticfiles.finders.AppDirectoriesFinder',
            ] # Aqui puedes implementar los estaticos si lo deseas para un proyecto futuro

            # Media
            # si se usara la media
            MEDIA_ROOT = str(APPS_DIR('media'))
            MEDIA_URL = '/media/'

            # Templates
            # no vamos a manejar los templates, pero van a estar en el directiorio
            # de apps en le path templates.
            TEMPLATES = [
                {
                    'BACKEND': 'django.template.backends.django.DjangoTemplates',
                    'DIRS': [
                        str(APPS_DIR.path('templates')),
                    ],
                    'OPTIONS': {
                        'debug': DEBUG,
                        'loaders': [
                            'django.template.loaders.filesystem.Loader',
                            'django.template.loaders.app_directories.Loader',
                        ],
                        'context_processors': [
                            'django.template.context_processors.debug',
                            'django.template.context_processors.request',
                            'django.contrib.auth.context_processors.auth',
                            'django.template.context_processors.i18n',
                            'django.template.context_processors.media',
                            'django.template.context_processors.static',
                            'django.template.context_processors.tz',
                            'django.contrib.messages.context_processors.messages',
                        ],
                    },
                },
            ]

            # Security
            SESSION_COOKIE_HTTPONLY = True # La sesion solo se manda por HTTP
            CSRF_COOKIE_HTTPONLY = True # Token CSRF
            SECURE_BROWSER_XSS_FILTER = True # Filtros de inyeccion
            X_FRAME_OPTIONS = 'DENY' # que no se pueda enbeber nuestra pagina

            # Email
            # Configuramos un email backen para enviar correos
            EMAIL_BACKEND = env('DJANGO_EMAIL_BACKEND', default='django.core.mail.backends.smtp.EmailBackend')

            # Admin
            ADMIN_URL = 'admin/' # Esta es la URLs que seteamos al principio
            #Puede cambiar a traves de entronos 
            	# En produccion puede ser Secreta
            ADMINS = [ # Almacena el correo de los administradores
                ("""Pablo Trinidad""", 'pablotrinidad@ciencias.unam.mx'),
            ]
            MANAGERS = ADMINS

            # Celery
            INSTALLED_APPS += ['cride.taskapp.celery.CeleryAppConfig']
            if USE_TZ:
                CELERY_TIMEZONE = TIME_ZONE
            CELERY_BROKER_URL = env('CELERY_BROKER_URL')
            CELERY_RESULT_BACKEND = CELERY_BROKER_URL
            CELERY_ACCEPT_CONTENT = ['json']
            CELERY_TASK_SERIALIZER = 'json'
            CELERY_RESULT_SERIALIZER = 'json'
            CELERYD_TASK_TIME_LIMIT = 5 * 60
            CELERYD_TASK_SOFT_TIME_LIMIT = 60
            ```

        - `/local.py`
        Es una herencia de base

            ```python
            """Development settings."""

            from .base import *  # NOQA
            from .base import env # Es una herencia de BASE.PY

            # Base
            DEBUG = True

            # Security
            # Trae la llave de una variable de entorno y si no usa la default
            # No es correcto versionar pero si estamos en desarrollo no importa.
            SECRET_KEY = env('DJANGO_SECRET_KEY', default='PB3aGvTmCkzaLGRAxDc3aMayKTPTDd5usT8gw4pCmKOk5AlJjh12pTrnNgQyOHCH')
            ALLOWED_HOSTS = [ # Hosts Permitidos
                "localhost",
                "0.0.0.0",
                "127.0.0.1",
            ]

            # Cache 
            # Bakcend de Cahce es el local, 
            CACHES = {
                'default': {
                    'BACKEND': 'django.core.cache.backends.locmem.LocMemCache',
                    'LOCATION': ''
                }
            }

            # Templates
            # Los templates estan en modo DEBUG
            TEMPLATES[0]['OPTIONS']['debug'] = DEBUG  # NOQA

            # Email
            	#Email Bakcned va a ser el mismo
            EMAIL_BACKEND = env('DJANGO_EMAIL_BACKEND', default='django.core.mail.backends.console.EmailBackend')
            EMAIL_HOST = 'localhost'
            EMAIL_PORT = 1025

            # django-extensions
            # Son un conjunto de herramientas que nos permite ecpandir django y sus necesidades
            INSTALLED_APPS += ['django_extensions']  # noqa F405

            # Celery
            CELERY_TASK_ALWAYS_EAGER = True
            CELERY_TASK_EAGER_PROPAGATES = True
            ```

        - `/pdrocuction.py`
        Es una herencia de base

            ```python
            """Production settings."""

            from .base import *  # NOQA
            from .base import env

            # Base
            SECRET_KEY = env('DJANGO_SECRET_KEY')
            # Host permitidos los trae como una lista usando .env
            ALLOWED_HOSTS = env.list('DJANGO_ALLOWED_HOSTS', default=['comparteride.com'])

            # Databases
            DATABASES['default'] = env.db('DATABASE_URL')  # NOQA Trae la URL de la base de datoss
            DATABASES['default']['ATOMIC_REQUESTS'] = True  # NOQA
            DATABASES['default']['CONN_MAX_AGE'] = env.int('CONN_MAX_AGE', default=60)  # NOQA Pone un limite en el limite de conexion

            # Cache
            # El backend de cache va a ser el de Redis ya no el de memoria local
            CACHES = {
                'default': {
                    'BACKEND': 'django_redis.cache.RedisCache',
                    'LOCATION': env('REDIS_URL'),
                    'OPTIONS': {
                        'CLIENT_CLASS': 'django_redis.client.DefaultClient',
                        'IGNORE_EXCEPTIONS': True,
                    }
                }
            }

            # Security
            # Mas settings de Seguridad
            SECURE_PROXY_SSL_HEADER = ('HTTP_X_FORWARDED_PROTO', 'https')
            SECURE_SSL_REDIRECT = env.bool('DJANGO_SECURE_SSL_REDIRECT', default=True)
            SESSION_COOKIE_SECURE = True
            CSRF_COOKIE_SECURE = True
            SECURE_HSTS_SECONDS = 60
            SECURE_HSTS_INCLUDE_SUBDOMAINS = env.bool('DJANGO_SECURE_HSTS_INCLUDE_SUBDOMAINS', default=True)
            SECURE_HSTS_PRELOAD = env.bool('DJANGO_SECURE_HSTS_PRELOAD', default=True)
            SECURE_CONTENT_TYPE_NOSNIFF = env.bool('DJANGO_SECURE_CONTENT_TYPE_NOSNIFF', default=True)

            # Storages
            # Los estaticos que estamos usando deben ser enviados a amazon S3 esta es la configuracion.
            #Lo veremos en produccion
            INSTALLED_APPS += ['storages']  # noqa F405
            AWS_ACCESS_KEY_ID = env('DJANGO_AWS_ACCESS_KEY_ID')
            AWS_SECRET_ACCESS_KEY = env('DJANGO_AWS_SECRET_ACCESS_KEY')
            AWS_STORAGE_BUCKET_NAME = env('DJANGO_AWS_STORAGE_BUCKET_NAME')
            AWS_QUERYSTRING_AUTH = False
            _AWS_EXPIRY = 60 * 60 * 24 * 7
            AWS_S3_OBJECT_PARAMETERS = {
                'CacheControl': f'max-age={_AWS_EXPIRY}, s-maxage={_AWS_EXPIRY}, must-revalidate',
            }

            # Static  files
            # PARA COMPRIMIR EL CACHE EN LOS ESTATICOS
            STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'

            # Media
            # Servimos la media desde amazon S3
            DEFAULT_FILE_STORAGE = 'storages.backends.s3boto3.S3Boto3Storage'
            MEDIA_URL = f'https://{AWS_STORAGE_BUCKET_NAME}.s3.amazonaws.com/'

            # Templates
            TEMPLATES[0]['OPTIONS']['loaders'] = [  # noqa F405
                (
                    'django.template.loaders.cached.Loader',
                    [
                        'django.template.loaders.filesystem.Loader',
                        'django.template.loaders.app_directories.Loader',
                    ]
                ),
            ]

            # Email
            # Usamos un servicio Any Email de Django
            # Esta nos permite conectarnos a cualquier ESP Email Service Provieder como mail assambly para enviar emails
            DEFAULT_FROM_EMAIL = env(
                'DJANGO_DEFAULT_FROM_EMAIL',
                default='Comparte Ride <noreply@comparteride.com>'
            )
            SERVER_EMAIL = env('DJANGO_SERVER_EMAIL', default=DEFAULT_FROM_EMAIL)
            EMAIL_SUBJECT_PREFIX = env('DJANGO_EMAIL_SUBJECT_PREFIX', default='[Comparte Ride]')

            # Admin
            ADMIN_URL = env('DJANGO_ADMIN_URL')

            # Anymail (Mailgun)
            INSTALLED_APPS += ['anymail']  # noqa F405
            EMAIL_BACKEND = 'anymail.backends.mailgun.EmailBackend'
            ANYMAIL = {
                'MAILGUN_API_KEY': env('MAILGUN_API_KEY'),
                'MAILGUN_SENDER_DOMAIN': env('MAILGUN_DOMAIN')
            }

            # Gunicorn
            INSTALLED_APPS += ['gunicorn']  # noqa F405

            # WhiteNoise
            MIDDLEWARE.insert(1, 'whitenoise.middleware.WhiteNoiseMiddleware')  # noqa F405

            # Logging
            # A sample logging configuration. The only tangible logging
            # performed by this configuration is to send an email to
            # the site admins on every HTTP 500 error when DEBUG=False.
            # See https://docs.djangoproject.com/en/dev/topics/logging for
            # more details on how to customize your logging configuration.
            # cConfiguraciones de l login puedes leer mas sobre esto en la documentacion.
            LOGGING = {
                'version': 1,
                'disable_existing_loggers': False,
                'filters': {
                    'require_debug_false': {
                        '()': 'django.utils.log.RequireDebugFalse'
                    }
                },
                'formatters': {
                    'verbose': {
                        'format': '%(levelname)s %(asctime)s %(module)s '
                                  '%(process)d %(thread)d %(message)s'
                    },
                },
                'handlers': {
                    'mail_admins': {
                        'level': 'ERROR',
                        'filters': ['require_debug_false'],
                        'class': 'django.utils.log.AdminEmailHandler'
                    },
                    'console': {
                        'level': 'DEBUG',
                        'class': 'logging.StreamHandler',
                        'formatter': 'verbose',
                    },
                },
                'loggers': {
                    'django.request': {
                        'handlers': ['mail_admins'],
                        'level': 'ERROR',
                        'propagate': True
                    },
                    'django.security.DisallowedHost': {
                        'level': 'ERROR',
                        'handlers': ['console', 'mail_admins'],
                        'propagate': True
                    }
                }
            }
            ```

        - `/test.py`
        Es una herencia de base.py

            ```python
            """Testing settings.
            With these settings, tests run faster.
            """

            from .base import *  # NOQA
            from .base import env

            # Base
            DEBUG = False
            # Configura una llave secreta
            SECRET_KEY = env("DJANGO_SECRET_KEY", default="7lEaACt4wsCj8JbXYgQLf4BmdG5QbuHTMYUGir2Gc1GHqqb2Pv8w9iXwwlIIviI2")
            # el test runer es de django
            TEST_RUNNER = "django.test.runner.DiscoverRunner"

            # Cache
            CACHES = {
                "default": {
                    "BACKEND": "django.core.cache.backends.locmem.LocMemCache",
                    "LOCATION": ""
                }
            }

            # Passwords
            # Vamos a configurar un hasher que es mas facil y rapido de computar
            PASSWORD_HASHERS = ["django.contrib.auth.hashers.MD5PasswordHasher"]

            # Templates
            # Pone todo en DEBUG
            TEMPLATES[0]["OPTIONS"]["debug"] = DEBUG  # NOQA
            TEMPLATES[0]["OPTIONS"]["loaders"] = [  # NOQA
                (
                    "django.template.loaders.cached.Loader",
                    [
                        "django.template.loaders.filesystem.Loader",
                        "django.template.loaders.app_directories.Loader",
                    ],
                )
            ]

            # Email
            #Configuramos el email backnds con el LOCAL
            EMAIL_BACKEND = "django.core.mail.backends.locmem.EmailBackend"
            EMAIL_HOST = "localhost"
            EMAIL_PORT = 1025
            ```

    - Debemos conocer la manera en la qu las variables se cargan al env que utilizamos para setear las variables de cada archivo en settings

---

---

## [5 Codebase: Dependencias y archivos de docker](https://platzi.com/clases/1461-django-avanzado/17142-codebase-dependencias-y-archivos-de-docker/)

**Palabras Clave:**

- 

**Resumen:** 

**Documentacion:**

[GitHub - jschneier/django-storages: https://django-storages.readthedocs.io/](https://github.com/jschneier/django-storages)

[GitHub - anymail/django-anymail: Django email backends and webhooks for Amazon SES, Mailgun, Mailjet, Postmark, SendGrid, SendinBlue, SparkPost and more](https://github.com/anymail/django-anymail)

[GitHub - django-extensions/django-extensions: This is a repository for collecting global custom management extensions for the Django Framework.](https://github.com/django-extensions/django-extensions)

[GitHub - joke2k/django-environ: Django-environ allows you to utilize 12factor inspired environment variables to configure your Django application.](https://github.com/joke2k/django-environ)

[GitHub - getsentry/sentry: Sentry is cross-platform application monitoring, with a focus on error reporting.](https://github.com/getsentry/sentry)

**Notas:**

- 0.29 ¿Que es el requeriments?
    - Es el manifiesto de las aplicaciones instaladas en Django, suele ser un TXT. Pero en nuestro proyecto esta como una serie de archivos
- Esquema de carpetas : **./requirements**

    ![Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_3.32.15_p._m..png](Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_3.32.15_p._m..png)

    - Igual que en nuestros settings utilizamos herencias
    - `/base.txt`

        ```python
        # Base
        pytz==2018.7
        	
        python-slugify==1.2.6
        	#Para imagenes
        Pillow==5.3.0
        psycopg2==2.7.4 --no-binary psycopg2

        # Django
        django==2.0.9

        	#Vamos a insttalar Django REST Framwork

        # Environment
        django-environ==0.4.5

        # Passwords security
        argon2-cffi==18.3.0

        # Static files
        whitenoise==4.1.2

        # Celery
        redis>=2.10.6, < 3
        django-redis==4.10.0
        celery==4.2.1
        flower==0.9.2
        ```

    - `/local.txt`

        ```python
        -r ./base.txt # Para la herencia

        # Debugging
        ipdb==0.11 #Un debbuger como pdb pero mas bonito

        # Tools
        django-extensions==2.1.4 # es la que vimos en el settings

        # Testing
        mypy==0.650
        pytest==4.0.2
        pytest-sugar==0.9.2
        pytest-django==3.4.4
        factory-boy==2.11.1 # Nos permite hacer mocking de datos

        # Code quality
        flake8==3.6.0 # Haremos un codigo limpio
        ```

    - `/production.txt`

        ```python
        # PRECAUTION: avoid production dependencies that aren't in development

        -r ./base.txt

        gunicorn==19.9.0 

        # Static files
        # boto3 es la conexion a amazon
        django-storages[boto3]==1.7.1

        # Email
        # Servicio de Antmail
        django-anymail[mailgun]==5.0
        ```

- 5.00 Esquema de carpetas :  **Docker**

    ![Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_3.42.08_p._m..png](Cimientos%204865b7486a354b89b1379cedbb49ff74/Captura_de_Pantalla_2021-05-14_a_la(s)_3.42.08_p._m..png)

    - `./Compose`: Declara las variables que debemos cargar
    - `/local.yml`

        ```docker
        version: '3'

        volumes:
          local_postgres_data: {}
          local_postgres_data_backups: {}

        services:
          **django: &django**
            build:
              context: .
              dockerfile: ./compose/local/django/Dockerfile #Docker file
            image: cride_local_django 
            depends_on:
              - postgres # Depende de ...
            volumes:
              - .:/app
            env_file:
        		# Este es el codigo que estaremos cambiando para pruebas o local
              - ./.envs/.local/.django    # las variables que carga
              - ./.envs/.local/.postgres  # siempre el codigo esta dependiendo de un entorno 
            ports:
              - "8000:8000" # Lo que esta en el 8000 lo pasa a este servidor
            command: /start

          postgres:
            build:
              context: .
              dockerfile: ./compose/production/postgres/Dockerfile
            image: cride_production_postgres
            volumes:
              - local_postgres_data:/var/lib/postgresql/data
              - local_postgres_data_backups:/backups
            env_file:
              - ./.envs/.local/.postgres

          redis:
            image: redis:3.2

          celeryworker:
            <<: *django
            image: cride_local_celeryworker
            depends_on:
              - redis
              - postgres
              
            ports: []
            command: /start-celeryworker

          celerybeat:
            <<: *django
            image: cride_local_celerybeat
            depends_on:
              - redis
              - postgres
              
            ports: []
            command: /start-celerybeat

          flower:
            <<: *django
            image: cride_local_flower
            ports:
              - "5555:5555"
            command: /start-flower
        ```

        Declara varios servicios:
