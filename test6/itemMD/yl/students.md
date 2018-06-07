
# “学生列表”用例 [返回](../../README.md)
## 1. 用例规约

|用例名称|学生列表|
|-------|:-------------|
|功能|以表形式的显示出所有学生的信息|
|参与者|游客，学生，老师|
|前置条件|学生，老师需要先登录|
|后置条件| |
|主事件流| |
|备选事件流| |

## 2. 业务流程（顺序图） [源码](../hd/students.wsd)
![sequence1](../../image/hd/students.png) 

## 3. 界面设计
- 界面参照: 
    - 老师查看所有学生信息[getStudentsUI](../../image/ui/getStudents.png)
    - 学生查看所有学生信息[getStudentsUI](../../image/ui/getStudents2.png)
- API接口调用
    - 接口设计：[getStudents](../../api/getStudents.md) 

## 4. 算法描述

- WEB_SUM解析为列表  
  - WEB_SUM是接口getStudents的返回值中的一部分，形如："WEB_SUM": "Y,Y,Y,Y,Y,N"。需要在前端进行解析。  
  - 作用是判断GitHub网址是否正确，用逗号分开，Y代表正确，N代表不正确。  
  - 第1位代表总的GitHUB地址是否正确，第2位表示第1次实验的地址，第3位表示第2位实验地址，依此类推。
  - 比如：“Y,Y,Y,Y,Y,N”表示第5次实验地址不正确，其他地址正确。  
  - 算法是使用使用字符串分离方法将其分开。

    
## 5. 参照表

- [STUDENTS](../data.md/#STUDENTS)
- [GRADES](../data.md/#GRADES)
- [TESTS](../data.md/#TESTS)