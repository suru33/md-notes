# Python

### pip install from git
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

### Update all python packages
```sh
pip3 list --format=freeze | grep -v '^\-e' | cut -d = -f 1 | xargs -n1 pip3 install
```
