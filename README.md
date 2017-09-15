# php spam word filter based on Double-Array Trie tree

## Dependence

- php >=5.4 && php < 7

## Useage

**Compile and Install**

```shell
git clone https://github.com/iliubang/php-double-array-trie-tree.git
cd php-double-array-trie-tree
phpize
./configure
make && sudo make install
```

```php
<?php

$words = array('管理员','admin','哈哈','我擦');
linger\TrieTree::build($words, "./bbb.dic");

$filter = new linger\TrieTree('./bbb.dic');
$content = 'this is testadmin这是一段测试文字，哈哈的飞洒管理员的司法地方哈哈，火红的萨来开发大健康我擦';
$res = $filter->searchOne($content);
var_dump($res);
$res = $filter->searchAll($content);
print_r($res);
```

## Thanks

Inspired by [wulijun/php-ext-trie-filter](https://github.com/wulijun/php-ext-trie-filter.git)

Depends on [libdatrie-0.2.4](https://linux.thai.net/~thep/datrie/datrie.html)

