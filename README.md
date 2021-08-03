# Django-Notes
#### My Notes on how to use Django effectively and make it work for you.

## Using a custom user model when starting a project


If you’re starting a new project, it’s highly recommended to set up a custom user model, even if the default User model is sufficient for you. This model behaves identically to the default user model, but you’ll be able to customize it in the future if the need arises.

In order to create a CustomUser we first need to inherit it from AbstractBaseClass:

```
from django.contrib.auth.models import AbstractUser

class User(AbstractUser):
    pass
```



