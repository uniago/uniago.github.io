---
title: MacOS快速输入日期
date: 2023-11-05 19:50:58 +0800
categories: ['Tool', 'Skills']
tag: ['快捷键', '小技巧', 'MacOS']
typora-root-url: ../
---



1、打开Automator(自动操作)

![image-20231105195908909](/assets/img/image-20231105195908909.png)

2、新建文稿后选择快速操作

![image-20231105203429558](/assets/img/image-20231105203429558.png)

3、选择"实用工具" => "运行shell脚本" ,然后将其拖到右侧

![image-20231105203540658](/assets/img/image-20231105203540658.png)

4、选择"没有输入"并勾选"用输出内容替换所选文本"

![image-20231105204525500](/assets/img/image-20231105204525500.png)

5、在编辑器中输入脚本,可以尝试运行下,点击结果看效果

```shell
date +"%Y-%m-%d %H:%M:%S %z"
```

6、保存后打开"设置" => "键盘" => "键盘快捷键"

![image-20231105204712217](/assets/img/image-20231105204712217.png)

7、选择"服务" => "文本",最后双击右边的快捷键进行设置即可

![image-20231105204925494](/assets/img/image-20231105204925494.png)

Tips:注意不能和其他快捷键冲突,否则是会被覆盖的~