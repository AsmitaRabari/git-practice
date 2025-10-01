# git-practice
Learning git and github hand-on in this project.


1. Configure git 

git config --global user.name "yourname"
git config --global user.email "youremailaddress"

2. Initialize git

git init

if you want to init in any specific branch or just want to do with main 

git config --global init.defaultBranch main

3. create new repository on your github account

4. clone the repository locally

git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name

5. make changes and push

echo "Hello everyone" > notes.txt
echo "- step 1: clone" >> notes.txt

6. Branching

git checkout -b feature-hello
echo "print('Hello, GitHub!')" > hello.py

git add hello.py
git commit -m "Add hello.py with hello message"
git push origin feature-hello


7. merge pull request

git checkout main
git pull origin main    

8. Simulate merge conflict

git checkout -b branch-a
echo "Line from A" > conflict.txt
git add conflict.txt
git commit -m "Add line from A"
git push origin branch-a

git checkout main
git checkout -b branch-b
echo "Line from B" > conflict.txt
git add conflict.txt
git commit -m "Add line from B"
git push origin branch-b


9. Resolving conflict

git checkout main
git pull origin main
git checkout branch-b
git merge main        # You'll see a conflict in conflict.txt
// Open the file and manually fix it
git add conflict.txt
git commit -m "Resolve conflict between branch-a and branch-b"
git push origin branch-b


10. pull all changes from github

    git pull origin main   # Fetch + merge remote changes

