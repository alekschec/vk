Рубежный контроль 2. Git.

git init
touch project.py
git add .
git commit -m "initial"
echo "print('Hello World2!')" >> project.py
git add .
git commit -m "added hello_world2"
echo "print('Hello World3!')" >> project.py
git add .
git commit -m "added hellow_world3"
mkdir screenshots
git add .
git commit -m "added ./screenshots"


git checkout -b fast-forward-merge
touch data.txt
git add .
git commit -m "added data.txt"
echo "second line" >> data.txt
git add .
git commit -m "added second line to data"
echo "print('Hello from fast-forward-merge')" >> project.py
git add .
git commit -m "add hello-word from branch"
git branch -m feature1
git commit -m "changed branch name"
git checkout master
git merge feature1
git add screenshots/2.png
git commit -m "added 2nd screenshot"

git checkout -b feature2
touch feature2.py
echo "print('This is feature2')" > feature2.py
git add feature2.py
git commit -m "added feature2.py"
echo "print('End of feature2')" > feature2.py
git add feature2.py
git commit -m "finished feature2"
git checkout master
git merge --no-ff feature2 -m "Merge commit without conflicts"
git add screenshots/3.png
git commit -m "added 3rd screenshot"

git checkout -b feature3
echo "print('feature3')" > project.py
git add project.py
git commit -m "changed project.py in feature3 branch"
git checkout master
echo "print('master branch')" > project.py
git add project.py
git commit -m "changed project.py in master branch"
git merge feature3
*Получили Merge Conflict*
*Отредактируем project.py так, как нужно*
git add project.py
git commit -m "Resolved merge conflict with feature3"
git add screenshots/4.png
git commit -m "added 4th screenshot"
