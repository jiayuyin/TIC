```
1.创建ssh key
ssh-keygen -t rsa -C "yin.jiayu@qq.com"
然后在用户目录下会有一个.ssh文件夹
复制id_rsa.pub的内容，复制里面的内容绑定在github上

绑定之后验证一下
ssh -T git@github.com
出现successful就成功了

2.绑定用户，邮箱
git config --global user.name "jiayuyin"
git config --global user.email "yin.jiayu@qq.com"

3.使用
git init //把这个目录变成Git可以管理的仓库
git add README.md //文件添加到仓库
git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了 
git commit -m "first commit" //把文件提交到仓库
git remote add origin git@github.com:yourname/yourrepositoryname.git //关联远程仓库
//这一步做了之后会把文件夹和仓库关联，不用再重复关联了

git push -u origin master //把本地库的所有内容推送到远程库上

下载
git clone xxx  //下载到本地
```