**Delete all executable files in Mac command line**
```vim
find . -maxdepth 1 -perm -111 -delete
```

**pip install from git**
```bash
# hash
pip install git+git://github.com/aladagemre/django-notification.git@2927346f4c513a217ac8ad076e494dd1adbf70e1

# branch
pip install git+git://github.com/aladagemre/django-notification.git@cool-feature-branch

# branch source bundle
pip install https://github.com/aladagemre/django-notification/archive/cool-feature-branch.tar.gz

# tag
pip install git+git://github.com/aladagemre/django-notification.git@v2.1.0

# tag source bundle
pip install https://github.com/aladagemre/django-notification/archive/v2.1.0.tar.gz
```
