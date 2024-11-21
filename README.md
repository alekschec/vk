Рубежный контроль 2. Git.

git init <br/>
touch project.py <br/>
git add .<br/>
git commit -m "initial"<br/>
echo "print('Hello World2!')" >> project.py<br/>
git add .<br/>
git commit -m "added hello_world2"<br/>
echo "print('Hello World3!')" >> project.py<br/>
git add .<br/>
git commit -m "added hellow_world3"<br/>
mkdir screenshots<br/>
git add .<br/>
git commit -m "added ./screenshots"<br/>
<br/>
<br/>
git checkout -b fast-forward-merge<br/>
touch data.txt<br/>
git add .<br/>
git commit -m "added data.txt"<br/>
echo "second line" >> data.txt<br/>
git add .<br/>
git commit -m "added second line to data"<br/>
echo "print('Hello from fast-forward-merge')" >> project.py<br/>
git add .<br/>
git commit -m "add hello-word from branch"<br/>
git branch -m feature1<br/>
git commit -m "changed branch name"<br/>
git checkout master<br/>
git merge feature1<br/>
git add screenshots/2.png<br/>
git commit -m "added 2nd screenshot"<br/>
<br/>
<br/>
git checkout -b feature2<br/>
touch feature2.py<br/>
echo "print('This is feature2')" > feature2.py<br/>
git add feature2.py<br/>
git commit -m "added feature2.py"<br/>
echo "print('End of feature2')" > feature2.py<br/>
git add feature2.py<br/>
git commit -m "finished feature2"<br/>
git checkout master<br/>
git merge --no-ff feature2 -m "Merge commit without conflicts"<br/>
git add screenshots/3.png<br/>
git commit -m "added 3rd screenshot"<br/>
<br/>
<br/>
git checkout -b feature3<br/>
echo "print('feature3')" > project.py<br/>
git add project.py<br/>
git commit -m "changed project.py in feature3 branch"<br/>
git checkout master<br/>
echo "print('master branch')" > project.py<br/>
git add project.py<br/>
git commit -m "changed project.py in master branch"<br/>
git merge feature3<br/>
*Получили Merge Conflict*<br/>
*Отредактируем project.py так, как нужно*<br/>
git add project.py<br/>
git commit -m "Resolved merge conflict with feature3"<br/>
git add screenshots/4.png<br/>
git commit -m "added 4th screenshot"<br/>
<br/>
<br/>
git remote add origin https://github.com/alekschec/vk.git<br/>
git push -u origin master<br/>

