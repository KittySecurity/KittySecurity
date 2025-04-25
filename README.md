# KittySecurity

## University Assignment for Computer Systems Security

## Table of Contents
- [General Info](#general-info)
- [Technologies](#technologies)
- [Contributors](#contributors)
- [Repositories Policy](#repositories-policy)
- [Helpful Git Commands](#helpful-git-commands)

## General Info

KittySecurity is a university project developed as part of the *Computer Systems Security* course.  
It is a password manager with a fun cat-themed interface. The application provides secure storage and management of user credentials while showcasing best practices in cybersecurity.

The project is divided into three main components:
- **Frontend**
- **Backend**
- **DevOps**

**_NOTE:_** _This project is for educational purposes only._

## Technologies

The project is built using the following technologies:
- **Java** with **Spring Boot** – backend
- **React.js** – frontend
- **Microsoft Azure** – infrastructure and deployment

## Contributors

#### DevOps Team
- [PeterSaletra](https://github.com/PeterSaletra) - owner of org
- [szymonmar](https://github.com/szymonmar)

#### Backend Team
- [VoxeveR](https://github.com/VoxeveR) - co-owner of org
- [newmon13](https://github.com/newmon13)
- [CottonCandyHeart](https://github.com/CottonCandyHeart)
- [Mautyn](https://github.com/Mautyn)

#### Frontend Team
- [odlugiewicz](https://github.com/odlugiewicz)
- [piotrek1kons](https://github.com/piotrek1kons)
- [EWyroba](https://github.com/EWyroba)

## Repositories Policy

### Branch naming

Use only the following branch names:
-  **feature/** - for adding new feature
-  **bugfix/** - for fixing small bugs
-  **hotfix/** - for fixing urgent or critical bugs

### Commit messages

How you should comment your commits:
- **feat:** - what new feature was added
- **fix:** - what was fix
- **refactor:** - what was refactored
- **docs:** - what was documented
- **test:** - what tests where added


### Helpful Git Commands

Cloning repository

```
# Clone frontend
git clone https://github.com/KittySecurity/kittysecurity-frontend.git
```
```
# Clone backend
git clone https://github.com/KittySecurity/kittysecurity-backend.git
```

Adding changes to local repository

```
git add .
```


Commiting changes

```
git commit -m "messsage"
```

Pushing to remote repository

```
# if branch is already on remote repository
git push
```

```
# if branch is not on remote repository
git push --set-upstream origin branch_name
```

Pulling from remote repository

```
git pull
```

```
# If pulling with unpushed commits
git pull --rebase
```


Adding new branch and swiching to it

```
git checkout -b branch_name
```

Adding new branch without switching

```
git branch branch_name
```

Switching to another branch

```
git checkout branch_name
```

Checking current branch

```
git branch
```

Checking status of changes 

```
git status
```
