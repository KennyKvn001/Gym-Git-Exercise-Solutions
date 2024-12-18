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
  git commit -m "message"
  git push

  # restoring team file and reset current changes
  git stash pop
  git reset --hard HEAD

  ```

## Bundle 2:

- ### Exercise 1:

  ```
  code

  # creating new branch ft/bundle-2
  git checkout -b ft/bundle-2

  # adding changes to service file and push it
  git add .
  git commit -m "message"
  git push

  ```

- ### Exircise 2:

  ```
  code

  # chectout to main and pulling the latest changes
  git checkout main
  git pull origin ft/bundle-2

  # creating new branch ft/service-redesign
  git git checkout -b ft/service-redesign

  # adding new changes to service file and push the changes
  git add .
  git commit -m "message"
  git push

  # going back to main branch and adding changes to service and push them
  git checkout main
  git add .
  git commit -m "message"
  git push

  # Comparing main and ft/service-redesign and merge them
  git diff main
  git merge main

  ```

## Bundle 3:

- ### Exercise 1:

  ```
  code

  # creating new branch team-page
  git checkout -b ft/team-page

  # creating new team html file add some changes and push them
  git add .
  git commit -m "message"
  git push

  # creating new PR on github
  # go back to main branch and create new branch contact page
  git checkout main
  git branch ft/contact-page

  # go back to team-page branch and see last commit using git log and copy its hash
  git log

  # checkout to contact-page and use cherry-pick to get the changes from the last commit of ft/team-page
  git cherry-pick <commit hash>
  git add .
  git push

  # create new PR on github
  # From the ft/contact-page branch create a new branch called ft/faq-page
  git branch ft/faq-page

  # create new file faq.html and push changes
  git add .
  git commit -m "message"
  git push

  # revert changes using git revert and push changes
  git revert <desired commit hash>
  git push


  ```

- ### Exercise 2:

  ```
  code

  # create new branch ft/home-page-redesign
  git checkout -b home-page-redesign

  # go back  to main and make some changes, commit and push changes
  git checkout main
  git add .
  git commit -m "messsage"
  git push

  # go back to ft/home-page-redesign and rebase the branch to main
  git checkout ft/home-page-redesign
  git rebase main
  git add .
  git push

  # then create PR on github


  ```

## Bundle 4:

- ### Exercise 1:

  ```
  code

  # Checkout the main branch
  git checkout main

  # Create a new repository on Github

  # Using git remote, add the repo to your project as a second remote named git-copy
  git remote add git-copy <new-repo-url>

  # Make new changes on the home page
  # Save and commit the changes
  git add .
  git commit -m "message"

  # Push the changes to both remotes: origin and git-copy
  git push origin main && git push git-copy main

  ```

- ### Exercise 2:

  ```
  code

  # Checkout a new branch named ft/footer
  git checkout -b ft/footer

  # Add some changes to the branch and commit them
  git add .
  git commit -m "First footer changes"

  # Add more changes again to the branch and create a second commit
  git add .
  git commit -m "Second footer changes"

  # Push and create a new PR for the branch
  git push origin ft/footer

  # Checkout the main branch again
  git checkout main

  # From there, create a new branch named ft/squashing
  git checkout -b ft/squashing

  # Using git merge squash, squash the changes on the ft/footer branch
  git merge --squash ft/footer

  # Commit the changes with a different commit message
  git commit -m "message"

  # Push the changes and create a PR
  git push origin ft/squashing

  ```
