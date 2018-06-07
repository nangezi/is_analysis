﻿<!-- markdownlint-disable MD033-->
<!-- 禁止MD033类型的警告 https://www.npmjs.com/package/markdownlint -->

# 接口：getTests  [返回](../README.md)
用例： [查看实验](../用例/查看实验.md),[修改实验](../用例/修改实验.md)

- 功能：
    返回一个课程所有实验信息。
    
- 权限：
    学生/老师：必须选择学期，课程后才能显示该门课程的实验信息
    学生：只能查看实验信息
    老师：可以查看修改删除实验信息
    
- API请求地址： 
    接口基本地址/v1/api/getOneStudentResults/<term>/<course_name>

- 请求方式 ：
    GET

- 请求参数说明:        

  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|
  |term|学期|
  |course_name|课程名称。|      
    
- 返回实例：

        {         
            "status": true,
            "info": null,    
            "total": 6,      
            "data": [
                { 
                "test_id":1 ,
                "title":"实验一：业务流程建模" ,
                "test_content":"明确业务流程，使用UML语言绘图，用markdown语法编写文档" ,
                "test_standard":"业务流程正确（25）#$$#文档内容正确（25）#$$#流程图美观（25）#$$#代码正确（25）" ,
                "last_time":"2018-3-17 24:00:00" ,
                }, 
                {
                ...其他实验
                }
            ] 
        }
 
- 返回参数说明：    
 
  |参数名称|说明|
  |:---------:|:--------------------------------------------------------|      
  |status|bool类型，true表示正确的返回，false表示有错误|
  |info|返回结果说明信息|  
  |total|实验总数|
  |test_id|实验编号|
  |title|实验标题|
  |test_content|实验内容|
  |test_standard|本实验评分项的标准，每个评分项用分隔符#$$#分隔开|
  |last_time|实验截止日期|


