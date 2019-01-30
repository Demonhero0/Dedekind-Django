### 项目说明

这是一个开发中的用于中珠数院公益时管理的Django Web App，代号：Project Dedekind


### 项目进展

- 已完成基本开发，正在进行改进

### 本地部署

1. 安装virtualenv (pip install virtualenv)
2. clone仓库，用virtualenv创建虚拟环境venv，并激活venv

```bash
cd Dedekind-Django
git checkout bs4 #切换到bs4分支，该分支为已发布的公益时平台的版本
virtualenv venv -p python3
source venv/bin/activate
```

3. 安装依赖

```bash
pip install -Ur requirements/local.txt
```

4. 初始化数据库，并创建超级用户

```bash
python manage.py makemigrations sua   
python manage.py migrate          #迁移数据库
python manage.py createsuperuser  #创建超级用户
```

5. 启动服务器

```bash
python manage.py runserver
```

7. 用浏览器打开[http://localhost:8000/](http://localhost:8000/)
（由于后端代码还不完善，启动服务器后应通过[http://localhost:8000/super/admin](http://localhost/super/admin:8000/)及时添加两个SuaGroup：“个人用户”及“学院”）
