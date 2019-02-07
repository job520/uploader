> uploader
>> 自用的上传文件的包  
>> 官方文档：[点击进入](http://doc.job520.net/web/#/3?page_id=39)

### 1. 引入：
1. 下载：  
`
composer require job520/uploader
`
2. 引入：  
`
require_once "vendor/autoload.php";
`
### 2. 用法：
1. 示例代码：
```php
<?php
// 1. 引入包
require_once 'vendor/autoload.php';
// 2. 使用命名空间
use job520\uploader;
// 3. 获取文件
$file = $_POST['file'];
// 4. 实例化上传类
$imageupload = new uploader($file);
// 5. 使用缩略图
$imageupload -> thumb = array(
    'is_thumb' => 1,
    'width' => 150,
    'height' => 150
);
// 6. 保存到file文件夹
$ret = $imageupload->save('files');
// 7. 打印输出
var_dump($ret);
```
2. 输出：
![](http://doc.job520.net/server/../Public/Uploads/2019-02-02/5c54950673295.png)
`
string(42) "files/6a40c31c0851968e22c5bcb2763ac2e8.jpg"
`
