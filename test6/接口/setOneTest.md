﻿﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：setOneTest  [返回](../README.md)
用例： [增加实验](../用例/增加实验.md)

- 功能：
    增加一个新的实验
    
- 权限：
    老师：可以增加实验信息
    
- API请求地址： 
    接口基本地址/v1/api/setOneTest

- 请求方式 ：
    POST
 
- 请求实例：
  
        { 
            "course_name": "信息系统与设计", 
            "test_id":1 ,
            "title":"实验一：业务流程建模" ,
            "test_content":"明确业务流程，使用UML语言绘图，用markdown语法编写文档" ,
            "test_standard":"业务流程正确（25）#$$#文档内容正确（25）#$$#流程图美观（25）#$$#代码正确（25）" ,
            "last_time":"2018-3-17 24:00:00" ,
        }

- 请求参数说明:       
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |course_name|课程名字|
  |test_id|实验编号|
  |title|实验标题|
  |test_content|实验内容|
  |test_standard|本实验评分项的标准，每个评分项用分隔符#$$#分隔开|
  |last_time|实验截止日期|
     
 
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


