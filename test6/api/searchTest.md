# 接口：searchTest  [返回](../README.md)

- 权限：
    游客：不可查看
    学生、老师：必须先登录，才能查看所上课程的对应的实验

- 功能：
    返回该课程对应的实验的内容。

- API请求地址：
   接口基本地址/api/searchTest
  
- 请求方式 ：
    GET

- 请求参数说明:
   |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |TERM_ID|需要查看的上课学期|
  |COURSE_ID|课程的编号|
  |TESTS_ID|实验的编号|

- 返回实例：

        {
            "status": true,
            "info": null,
            "data": [
                {
                "TEST": [
                    {
                        "TEST_NAME":"实验一"
                        "TEST_ADDRESS":"https://github.com/WangHuagang/is_analysis/tree/master/test1"
                    },
                    {
                        "TEST_NAME":"实验二"
                        "TEST_ADDRESS":"https://github.com/WangHuagang/is_analysis/tree/master/test1"
                    }
                ],
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |COURSE_NAME|课程名称|
  |TERM_ID|上课所在学期|
  |TEST|返回的实验的数组|
  |TEST_NAME|实验的名称|
  |TEST_ADDRESS|实验对应的地址|
