<h1 align="center"> xml </h1>

<p align="center"> xml 创建、解析 </p>

来自超哥 [EasyWechat](https://github.com/overtrue/wechat)

## Installing

```shell
$ composer require hedeqiang/xml -vvv
```

## Usage

### 解析XML，返回数组
```php
require __DIR__ .'/vendor/autoload.php';

use Hedeqiang\Xml\Xml;

$xml = "<xml>
        <foo>name</foo>
        <bar>age</bar>
        <name><![CDATA[text here]]></name>
    </xml>";
print_r(xml::parse($xml)) ;
```
### 创建XML
```php
$data = [
    'id' => 'bk101',
    'author' => 'Gambardella, Matthew',
    'title' => 'XML Developer\'s Guide',
    'genre' => 'Computer',
    'price' => '44.95',
    'items' => ['foo', 'bar'],
    'publish_date' => '2000-10-01',
    'description' => 'An in-depth look at creating applications with XML.',
];
print_r(xml::build($data));
```

## 鸣谢
该内容来自超哥 [EasyWechat](https://github.com/overtrue/wechat) ,因业务需要解析xml数据，网上找到一个关于解析的，无奈该扩展xml 数据源不能从接口获取，So 把超哥的代码搬过来了.原封不动，就连测试用例也搬过来了......


[Rodenastyle/stream-parser](https://github.com/Rodenastyle/stream-parser)  ，另外刚才说的扩展就是这个，如果你是读取一个xml文件的话，可以使用这个扩展


## License

MIT