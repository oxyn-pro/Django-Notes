# Django-Notes
#### My Notes on how to use Django effectively and make it work for you.

## Using a custom user model when starting a project


If you’re starting a new project, it’s highly recommended to set up a custom user model, even if the default User model is sufficient for you. This model behaves identically to the default user model, but you’ll be able to customize it in the future if the need arises.

If there is going to be created a new Custom User Model, creating a Custome User Manager is recommended, because in customer user model there can be some fields that need to be modified, that will change default user manager as well. It means that creating a new Customer User Manager is also important.

In order to create a Custom User Manager we first need to inherit required dependencies from BaseUserManager: 

```
from django.contrib.auth.models import BaseUserManager

class CustomUserManager(BaseUserManager):
    pass
```

In order to create a Custom User we first need to inherit it from AbstractBaseUser:

```
from django.contrib.auth.models import AbstractUser

class CustomUser(AbstractUser):
    pass
```

About AbstractBaseUser: https://docs.djangoproject.com/en/3.2/topics/auth/customizing/#django.contrib.auth.models.AbstractBaseUser
About BaseUserManager: https://docs.djangoproject.com/en/3.2/topics/auth/customizing/#django.contrib.auth.models.BaseUserManager
About PermissionsMixin: https://docs.djangoproject.com/en/3.2/topics/auth/customizing/#django.contrib.auth.models.PermissionsMixin


