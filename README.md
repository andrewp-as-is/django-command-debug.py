[![](https://img.shields.io/badge/released-2021.6.12-green.svg?longCache=True)](https://pypi.org/project/django-command-debug/)
[![](https://img.shields.io/badge/license-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)

### Installation
```bash
$ pip install django-command-debug
```

#### `settings.py`
```python
INSTALLED_APPS+=['django_command_debug']
```

#### `migrate`
```bash
$ python manage.py migrate
```

### Examples
```python
from django.core.management.base import BaseCommand
from django_command_debug.management.base import DebugMixin

class Command(DebugMixin,BaseCommand):
    def handle(self, *args, **options):
        self.debug('message')
```

