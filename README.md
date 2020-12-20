This repo was done as part of tutorial of creating the custom user model
https://learndjango.com/tutorials/django-custom-user-model





Note that we did not run migrate to configure our database. 
It's important to wait until after we've created our new custom user model before doing so.

AbstractUser vs AbstractBaseUser
There are two modern ways to create a custom user model in Django: AbstractUser and AbstractBaseUser. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much, much more work. Seriously, don't mess with it unless you really know what you're doing. And if you did, you wouldn't be reading this tutorial, would you?

So we'll use AbstractUser which actually subclasses AbstractBaseUser but provides more default configuration.

Custom User Model
Creating our initial custom user model requires four steps:

    update config/settings.py
    create a new CustomUser model
    create new UserCreation and UserChangeForm
    update the admin

