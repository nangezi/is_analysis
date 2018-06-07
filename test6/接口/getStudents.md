﻿﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getStudents  [返回](../README.md)
用例： [学生列表](../用例/学生列表.md),[老师查看成绩](../用例/老师查看成绩.md)

- 权限：
    老师必须登录后选择学期课程后才会显示该课程所有学生的学生列表。

- 功能：
    返回该门课程所有学生的列表。

- API请求地址：
   接口基本地址/v1/api/getStudents/<student_id>/<term>/<course_name>

- 请求方式 ：
    GET

- 请求参数说明:

    |参数名称|说明|
    |:---------:|:--------------------------------------------------------|      
    |term|学期|
    |course_name|课程名字|

- 返回实例：

        {
            "status": true,
            "info": null,
            "total": 121,
            "data": [
                {"WEB_SUM": "Y",
                "RESULT_SUM": "83.75,90,80,80,85,N",
                "GITHUB_USERNAME": "Chinajuedui",
                "STUDENT_ID": "201510315203",
                "CLASS": "软件(本)15-1",
                "NAME": "陈松华",
                },
                {
                ...其他学生
                }
            ]
        }

- 返回参数说明：

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |total|返回学生人数|
  |data|所有学生的数组|
  |WEB_SUM|该课程网址是否正确|
  |RESULT_SUM|成绩的汇总|
  |GITHUB_USERNAME|GITHUB 用户名|
  |STUDENT_ID|学号|
  |CLASS|班级|
  |NAME|真实姓名|
 