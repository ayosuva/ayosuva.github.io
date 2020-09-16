---
layout: post
title:  "Useful git commands"
author: Yosuva
categories: [Git]
featured: true
image: https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.pngegg.com%2Fen%2Fpng-chcmm&psig=AOvVaw2ZJ7raSmvuX0VnPUcnO21t&ust=1600381823690000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCNi5noPd7usCFQAAAAAdAAAAABAI
---
This page contains few useful git commands

1. Create repository in github
2. Go to you local project folder
3. Add README.md file using ```echo "Hello" >> README.md```
4. Add ```.gitignore``` file manually and add the below content if your project is eclipse maven project
```java
 #Eclipse
.classpath
.project
.settings/

#Intellij
.idea/
*.iml
*.iws

#Mac
.DS_Store

#Maven
log/
target/
```
5. Add remote repository using ```git remote add origin https://github.com/ayosuva/test.git```
6. create branch using ```git branch -M master```
6. Add ```.gitignore``` file alone using ```git add .gitignore``` and then commit using ```git commit -m ".gitignore commit"```
7. push the commits using ```git push -u origin master``` 
   use ```git pull origin master --allow-unrelated-histories``` if you have initialized repo in github and also committed locally
8. Now add the all others files using ```git add .``` - This will add only the required file and it will ignore the file/folders that we have mentioned in the .gitignore file
9. commit using ```git commit -m ".gitignore commit"```
10. push the commits using ```git push -u origin master``` 

