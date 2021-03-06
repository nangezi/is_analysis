﻿﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getTeacherCourse  [返回](../README.md)
用例： [老师选课](../用例/老师选课.md),[]

- 功能：
    老师选课
    
- 权限：    
    老师：登陆后选择学期后，才能选课
    
- API请求地址： 
    接口基本地址/v1/api/getTeacherCourse/<teacher_id>/<term>

- 请求方式 ：
    GET

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |teacher_id|老师的工号|
  |term|学期|
    
- 返回实例：

          {         
               "status": true,
               "info": null,    
               "term": "2017-2018 第2学期",       
               "data": [
                    {
                    "course_num":120,
                    "course_time": "星期一5,6节课和星期二1,2节课", 
                    "course_wtime": "第二周到十四周", 
                    "course_name": "信息系统与设计",
                    }, 
                    {
                    ...其他课程
                    }
                    ] 
                }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|
  |course_name|课程名称|
  |term|学期|
  |course_num|课程限定人数|
  |course_time|上课时间|
  |course_wtime|上课周数|

