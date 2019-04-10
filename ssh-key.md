#### Generating a new SSH key and adding it to the ssh-agent

---

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

eval "$(ssh-agent -s)"

```

**For Mac**

```bash
~/.ssh/config

Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_rsa


ssh-add -K ~/.ssh/id_rsa
```



**For Windows/Linux**

```bash
ssh-add ~/.ssh/id_rsa
```

