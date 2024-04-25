# 学生信息管理系统

## 概述

本套系统是我大一程序设计进阶课的结课作业，实现了登录、文件读写，以及对数据的查询、排序等操作。

1、单人完成巨量代码的编写（本以为几百行能解决的系统，前前后后写了两千多行，虽然很多是注释...）

2、本套系统基于Windows系统，执行C11标准。

3、项目使用Clion集成环境开发。

4、项目模块化，将不同功能写在不同的源文件中，通过头文件集中管理和调用。

5、用户输入检测，只允许用户输入规则内的数据，不合法的数据一律提示重新输入。

**相关文件的解释：**

| 文件                                      | 解释                                         |
| ----------------------------------------- | -------------------------------------------- |
| for_main.h                                | 包含主函数所需的所有头文件                   |
| user.h                                    | 定义登录用户的相关信息结构体                 |
| stu_info.h                                | 定义用于存储学生信息的结构体                 |
| for_function_module.h                     | 包含每个模块函数所需的头文件以及主函数的声明 |
| main.c                                    | 主函数                                       |
| main_menu.h & main_menu.c                 | 主菜单模块                                   |
| secondary_menu.h & secondary_menu.c       | 二级菜单模块                                 |
| login_module.h & login_module.c           | 登录模块                                     |
| registered_module.h & registered_module.c | 用户注册模块                                 |
| add_module.h & add_module.c               | 学生信息添加模块                             |
| query_module.h & query_module.c           | 学生信息查询模块                             |
| modify_module.h & modify.c                | 学生信息修改模块                             |
| delete_module.h & delete_module.c         | 学生信息删除模块                             |
| statistic_module.h & statistic_module.c   | 成绩统计模块                                 |



## 系统结构

- 主菜单
- 二级菜单
- 登录模块
- 注册模块
- 学生信息添加模块
- 学生信息查询模块
- 学生信息修改模块
- 学生信息删除模块
- 成绩统计

## 功能详解

### 一、主菜单

本系统设置有权限，只有注册账号后输入正确的账号密码才能进入。

主菜单设置有输入内容的控制功能，即检测输入内容是否合法：

![image-20240422092216668](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092216668.png)

### 二、登录模块

![image-20240422092223123](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092223123.png)

输入正确的账号密码即可进入系统。

### 三、二级菜单

![image-20240422092230325](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092230325.png)

二级菜单中提供5个功能，输入代码即可跳转至对应功能。

二级菜单设置有输入内容的控制功能，即检测输入内容是否合法：

![image-20240422092239674](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092239674.png)

### 四、学生信息添加模块

![image-20240422092246421](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092246421.png)

在此模块中，需依次输入学生的学号、姓名、性别、年龄、语文成绩、数学成绩、英语成绩。

输入结束后，学生信息被保存在stu_info目录下的stu_info.txt文件中：

![image-20240422092253662](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092253662.png)

输入结束后，提示是否继续添加，选择”是“则当前界面清除，进入下一轮的输入，否则返回二级菜单。

本模块同样设置有输入内容检测功能，非法输入无效。

### 五、学生信息查询模块

![image-20240422092300298](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092300298.png)

本系统支持按学号、姓名和性别查询学生信息，输入要查询的学生的学号、姓名或性别均可查询。

![](https://yvling-blog-image-1257337367.cos.ap-shanghai.myqcloud.com/%E5%8D%9A%E5%AE%A2/%E5%AD%A6%E7%94%9F%E4%BF%A1%E6%81%AF%E7%AE%A1%E7%90%86%E7%B3%BB%E7%BB%9F/2022-04-23/%E5%AD%A6%E7%94%9F%E4%BF%A1%E6%81%AF%E6%9F%A5%E8%AF%A21.png)

![image-20240422092306537](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092306537.png)

若系统中没有要查询的学生信息，则提示：

![image-20240422092312685](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092312685.png)

### 六、学生信息修改模块

![image-20240422092319467](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092319467.png)

本系统支持按学号、姓名查询学生信息并修改。

![image-20240422092325948](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092325948.png)

依次输入修改后的学生学号、姓名、性别、年龄及各科成绩即可。

### 七、学生信息删除模块

![image-20240422092332975](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092332975.png)

本系统支持按学号、姓名和性别删除学生信息，输入学生的学号、姓名或性别均可删除相关信息。

![image-20240422092339130](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092339130.png)

### 八、成绩统计模块

本系统支持对单科成绩的查询，包括升序、降序查询和分数段查询，同时显示该科目的平均分。

![image-20240422092344683](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092344683.png)

按语文成绩升序查询：

![image-20240422092350703](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092350703.png)

按数学成绩降序查询：

![image-20240422092356587](https://yvling-typora-image-1257337367.cos.ap-nanjing.myqcloud.com/typora/image-20240422092356587.png)


