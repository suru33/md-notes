**Delete all executable files in Mac command line**
```vim
find . -maxdepth 1 -perm -111 -delete
```

**pip install from git**
```vim
pip install git+git://github.com/aladagemre/django-notification.git@2927346f4c513a217ac8ad076e494dd1adbf70e1

pip install git+git://github.com/aladagemre/django-notification.git@cool-feature-branch

pip install https://github.com/aladagemre/django-notification/archive/cool-feature-branch.tar.gz

pip install git+git://github.com/aladagemre/django-notification.git@v2.1.0

pip install https://github.com/aladagemre/django-notification/archive/v2.1.0.tar.gz
```
