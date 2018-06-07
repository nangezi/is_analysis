﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：deleteTest  [返回](../README.md)
用例： [删除实验](../用例/删除实验.md)

- 功能：
    删除一个实验信息
    
- 权限：
    老师：可以删除实验信息
    
- API请求地址： 
    接口基本地址/v1/api/deleteTest

- 请求方式 ：
    POST
 
- 请求实例：
  
        { 
            "course_name": "信息系统与设计", 
            "test_id":1,
             
        }

- 请求参数说明:       
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |course_name|课程名字|
  |test_id|实验编号|

     
 
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


