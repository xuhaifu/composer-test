### 对composer的应用

name是当前库的名称

```
"name": "test/test",
```

git项目的引入，如下。url可以是远程git库，也可以是本地git项目路径，下面require添加对应name

```
"repositories": [
    {
        "type": "git",
        "url": "https://github.com/bjeavons/zxcvbn-php.git"
    },
    {
        "type":"git",
        "url":"/data/default/composer-test/composer-test"
    }
],
```

require是远程库name，以及对应版本号，默认*

```
"require": {
    "php": ">=7.0.0",
    "predis/predis":"*",
    "bjeavons/zxcvbn-php":"*",
    "matyhtf/swoole_framework": "dev-master"
},
```

autoload可以通过files导入本地类库,或者是PSR4格式的本地命名空间类

```
"autoload": {
    "files":["lib/ClassTest.php"],
    "psr-4": {
        "Xhf\\Test\\": "src/Xhf/Test"
    }
}
```