
# “查看对应课程成绩”用例 [返回](../../README.md)
## 1. 用例规约

|用例名称|查看对应课程成绩|
|-------|:-------------|
|功能|学生查看该课程的实验的各成绩以及最终成绩|   
|参与者|学生|
|前置条件|学生需要登录|
|后置条件| |
|主事件流| |
|备选事件流| |

## 2. 业务流程（顺序图） [源码](../hd/searchCourseGrades.wsd)
![searchCourseGrades](../../image/hd/searchCourseGrades.png) 

## 3. 界面设计
- 界面参照: [searchCourseGradesUI](../../image/ui/searchCourseGrades.png)
- API接口调用
    - 接口设计：[searchCourseGrades](../../api/searchCourseGrades.md) 

## 4. 算法描述

- 实验成绩计算  
  - 后台返回各实验成绩以及各评分项的分数
  - 利用各评分项分数相加得到实验的总分
  - 对各实验总分求平均值得到该课程的平均分
    
## 5. 参照表

- [STUDENTS](../data.md/#STUDENTS)
- [TESTS](../data.md/#TESTS)
- [GRADES](../data.md/#GRADES)