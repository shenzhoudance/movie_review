
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
![image](https://ws1.sinaimg.cn/large/006tNc79gy1fpedu0pxzoj31kw0qi0yp.jpg)
![image](https://ws4.sinaimg.cn/large/006tNc79gy1fpeduj0z2uj317y0uwtdp.jpg)
![image](https://ws1.sinaimg.cn/large/006tNc79gy1fpedur92znj318w0wc0zb.jpg)

## 第3部分 构建 gem-devise 分支
```
git checkout -b gem-devise
https://rubygems.org/
gem 'devise', '~> 4.4', '>= 4.4.2'
bundle install
```
![image](https://ws1.sinaimg.cn/large/006tNc79gy1fpee3bl2goj31bs0swthp.jpg)
```
rails generate devise:install
```
![image](https://ws2.sinaimg.cn/large/006tNc79gy1fpef061y3rj31kw0l111e.jpg)
![image](https://ws2.sinaimg.cn/large/006tNc79gy1fpef176cafj31700lkjuu.jpg)
![image](https://ws4.sinaimg.cn/large/006tNc79gy1fpef1sfoo5j31kw0fa78h.jpg)
```
rails g devise:views
rails g devise User
rake db:migrate
rails server
http://localhost:3000/users/sign_up
```
![image](https://ws1.sinaimg.cn/large/006tNc79gy1fpeev3hobjj312g0kmabj.jpg)
![image](https://ws3.sinaimg.cn/large/006tNc79gy1fpef8dv6dkj313a0fsjsy.jpg)

## 第3部分 构建 user_id_to_movies 分支
```
git checkout -b user_id_to_movies
rails g migration add_user_id_to_movies user_id:integer
rake db:migrate
```
![image](https://ws1.sinaimg.cn/large/006tNc79gy1fpefj7qk6gj31cq0t8jwo.jpg)

```
rails c
exit
```
![image](https://ws3.sinaimg.cn/large/006tNc79gy1fpefvhq4b8j315o05qdh8.jpg)
```
添加用户关系
current_user.movies.build
belongs_to :user
has_many :movies
```
![image](https://ws4.sinaimg.cn/large/006tNc79ly1fpefzy8y56j31kw0eyq6o.jpg)
![image](https://ws2.sinaimg.cn/large/006tNc79ly1fpefzyd9k8j31gg0lqn1l.jpg)
![image](https://ws4.sinaimg.cn/large/006tKfTcly1fpeg1ao3cwj30z40km0vb.jpg)

```
rails server
http://localhost:3000/movies/new
```
![image](https://ws2.sinaimg.cn/large/006tKfTcly1fpeg2p9qvaj30y80oa400.jpg)
