# Gym-Git-Exercise-Solutions

## Bundle 1:

- ### Exercise1

  - ### Creating a repo

    ```
    code

    git clone https://github.com/KennyKvn001/Gym-Git-Exercise-Solutions.git

    cd Gym-Git-Exercise-Solutions

    echo "#Gym-Git-Exercise-Solutions" > README.md

    git add .

    git commit -m "message"

    git push

    ```

    ### Renaming and Creating

    ```
    codes

    <!-- renaming main to master -->
    git branch master

    <!-- renaming to main -->
    git branch main

    <!-- creating new branch dev -->
    git branch -M dev
    git checkout dev

    <!-- creating new branch test and deleting it -->
    git branch -M test
    git branch -d test or
    git branch -D test  # when your what to force it

    ```

- ### Exercise2

  ```
  code

  # creating a new home.html file and stash it
  git add .
  git stash

  #repeat the same thing for about and team files
  git add .
  git stash

  # restoring the about file
  git stash pop 1    # 1 was the index of about file in stash list

  # restoring the home file
  git stash pop 1    # 1 was the index of home file in stash list after popping the about file

  # saving changes and push them
  git add .
  git push

  # restoring team file and reset current changes
  git stash pop
  git reset --hard HEAD

  ```
