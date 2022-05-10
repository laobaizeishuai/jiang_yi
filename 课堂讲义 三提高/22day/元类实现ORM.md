## ORM

### 1. ORM是什么

ORM 是 python编程语言后端web框架 Django的核心思想，“Object Relational Mapping”，即对象-关系映射，简称ORM。

一个句话理解就是：创建一个实例对象，用创建它的类名当做数据表名，用创建它的类属性对应数据表的字段，当对这个实例对象操作时，能够对应MySQL语句

![](/Images/22day/QQ20171108-002937@2x.png)

demo:

```python
class User(父类省略):
    uid = ('uid', "int unsigned")
    name = ('username', "varchar(30)")
    email = ('email', "varchar(30)")
    password = ('password', "varchar(30)")
    ...省略...


u = User(uid=12345, name='Michael', email='test@orm.org', password='my-pwd')
u.save()
# 对应如下sql语句
# insert into User (username,email,password,uid)
# values ('Michael','test@orm.org','my-pwd',12345)
```

#### 说明

1. 所谓的ORM就是让开发者在操作数据库的时候，能够像操作对象时通过`xxxx.属性=yyyy`一样简单，这是开发ORM的初衷
2. 只不过ORM的实现较为复杂，Django中已经实现了 很复杂的操作。这里主要让大家理解ORM框架的意义就可以了。详细的使用在web框架中会详细介绍。





