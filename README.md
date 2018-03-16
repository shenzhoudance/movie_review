
# 才华横溢 movie_review 教学案例 5

## 第1部分 新建专案

### 1.1 新建 movie_review 专案
```
cd workspace
rails new movie_review
cd movie_review
arom .
```
![image](https://ws1.sinaimg.cn/large/006tNc79gy1fped2gk5wvj31kw0tjwki.jpg)

### 1.2 提交 git 仓库
```
git init
git status
git add .
git commit -m "initial commit"
```
### 1.3 查看 专案 效果
```
rails server
http://localhost:3000/
```
![image](https://ws1.sinaimg.cn/large/006tNc79gy1fped0wpmnkj31cm10k1kx.jpg)
### 1.4 提交 远程 仓库
```
git remote add origin https://github.com/shenzhoudance/movie_review.git
git push -u origin master
```
![image](https://ws1.sinaimg.cn/large/006tNc79gy1fped3zehuwj31ka0ycage.jpg)

## 第2部分 构建 scaffold-Movie 分支
```
git checkout -b scaffold-Movie
rails g scaffold Movie title:string description:text movie_length:string director:string rating:string
rake db:migrate
rails server
http://localhost:3000/
```
![image](https://ws3.sinaimg.cn/large/006tNc79gy1fpedoxavwrj311k0ccq3w.jpg)
```
git status
git add .
git commit -m "scaffold-Movie"
git push origin scaffold-Movie
```
