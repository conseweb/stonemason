# stonemason
石匠：刻字人


## milestone 1.0

目的：为了鉴定文件系统没有被非法篡改，随时可以快速验证，使用merkle树的特性来保存一个根hash。

* 对整个目录下的所有文件进行遍历，获取所有文件的大小和计算文件的sha1哈希值，记录在一个文件里面
* 建议结果文件格式：每一行一个文件，用逗号隔开，前面是文件名称，后面是哈希值，文件大小
* 需要可以指定忽略哪些目录、文件，需要支持通配符
* 代码实现简洁，运行性能高得分高
* 要求通过测试代码自我证明代码能够可靠运行并正确实现上述功能
* 将整个目录生成相应的merkle树，并将该树的根打印出来，并存储到sqlite数据库里面（包括时间戳、目录路径）