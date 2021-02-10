# Settings notes

Extend all environment-specific settings in the settings_local.py file, which is ignored by VCS. Note secrets not in VCS. This may lose some environment settings. We need to let developers know an example in VCS to explain settings. settings_local.example (in VCS)

```py
# typical settings.py
ALLOWED_HOSTS = ['example.com']
DEBUG = False
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'production_db',
        'USER': 'user',
        'PASSWORD': 'password',
        'HOST': 'db.example.com',
        'PORT': '5432',
        'OPTIONS': {
            'sslmode': 'require'
        }
    }
}

#... all the rest of the settings file

from .settings_local import *

##############settings_local.py

ALLOWED_HOSTS = ['localhost']
DEBUG = True
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'local_db',
        'HOST': '127.0.0.1',
        'PORT': '5432',
    }
}

```