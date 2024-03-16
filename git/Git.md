- Resources
	- https://git-scm.com/book/en/v2
	- **So You Think You Know Git - FOSDEM 2024**
		- https://www.youtube.com/watch?v=aolI_Rz0ZqY

```bash

git config --global user.name "Vlad"
git config --global user.email "name@domain"

```

# Install git-gui & gitk
```bash
sudo apt-get update
sudo apt-get install git-gui gitk
```


# After New Repository created

## **Quick setup** — if you’ve done this kind of thing before
https://github.com/savagekilomike/dev-env-setup.git

## …or create a new repository on the command line
```bash
echo "# dev-env-setup" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/savagekilomike/dev-env-setup.git
git push -u origin main
```

## …or push an existing repository from the command line
```bash
git remote add origin https://github.com/savagekilomike/dev-env-setup.git
git branch -M main
git push -u origin main
```
