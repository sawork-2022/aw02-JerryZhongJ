# Poshell

这个应用程序分为三层：交互层、服务层、数据层。

## 交互层
交互层实现了命令行的输入输出。它的任务为解析输入，转换为服务层的接口和参数。对服务层的返回内容，交互层进行解释，并打印到屏幕上。

交互层可以说是文本与程序之间的桥梁。

## 服务层
交互层是业务逻辑无关的，交互层只是在做翻译任务。所有的业务逻辑都在服务层之下。因此服务层定义了这了应用程序能够实现什么功能。

服务层有一个模型，包含Cart，Item，Product等表示。这些是服务层的组成部分，是用来实现业务逻辑的。

## 数据层
业务是围绕着数据进行的，业务逻辑也是关于数据的逻辑。为了将逻辑与数据分离，数据的管理工作单独形成一个层，负责读取和写入数据。

这个层次可以实现与多个数据库或者多种存储方式的交互，从而实现业务逻辑与数据的存储分离，让服务层只关注业务逻辑。