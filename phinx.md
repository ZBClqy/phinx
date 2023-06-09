## 数据库迁移

数据库迁移是为了保证多人开发时如果对数据库的更改，可以更好的去多人同步数据库

## phinx

这个库是在php任何框架都可以使用的数据库迁移库

### 下载

```
composer require robmorgan/phinx
```

### 初始化

```
vendor/bin/phinx init
```

这里还需要在我们的框架内建立目录结构，在我们的根目录下建立db文件夹，然后在db文件夹下建立magrations和seeds文件夹

### 生成迁移脚本文件

```
vendor/bin/phinx create 脚本名称
```

### 启动脚本

 php vendor/bin/phinx migrate -e 这里可以指定我们的环境比如development  -t  这里后面是我们的脚步时间戳，可以让我们指定执行固定的脚步20230608015725

### 生成种子脚本文件

```
vendor/bin/phinx seed:create 脚本名称
```

启动脚本

```
vendor/bin/phinx seed:run -s 想执行的脚步名称
```