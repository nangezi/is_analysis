<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setStudentCourse  [返回](../README.md)
用例： [老师选课](../用例/老师选课.md)

- 功能：
    老师选择要修的课程。
    
- 权限：
    老师：选课之前必须先登录，选择学期，才会出现本学期将要选的课程。    
    
- API请求地址： 
    接口基本地址/v1/api/setTeacherCourse/<student_id>/<term>/<course_name>

- 请求方式 ：
    POST

- 请求实例：

        {
            "teacher_id":"14110",
            "term":"2017-2018 第2学期",
            "course_name":"信息系统与数据",            
        }
        
- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |teacher_id|老师的工号。对应表TEACHERS.TEACHER_ID的值|
  |term|学期。对应表COURSE.TERM|
  |course_name|课程的名字。| 
  
- 返回实例：

        {         
            "status": true,
            "info": null
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|


