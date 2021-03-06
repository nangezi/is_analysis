﻿何佳倩的实验报告
========
<table>
<tr>
    <th width=100%, bgcolor=withe >姓名</th>
    <th width=40%, bgcolor=withe>学号</th>
    <th width="50%", bgcolor=withe>班级</th>
  </tr>
  <tr>
      <th width=100%, bgcolor=withe >何佳倩</th>
      <th width=40%, bgcolor=withe>201510414110</th>
      <th width="50%", bgcolor=withe>2015级软件工程1班</th>
    </tr>
</table>

实验1：业务流程建模块
--
流程图1：考试及成绩管理流程
-

#### plantUML的源码如下：
```
>@startuml
  |教务处|
  start
  :安排考试;
  :考试安排表;
  |#AntiqueWhite|教师|
  :出卷;
  fork
     :A、B试卷;
   fork again
     :打印审批表;
  |系主任|
  :审批签字;
  :打印审批表;
  endfork
  |教务处|
  :打印试卷;
  :试卷;
   |#AntiqueWhite|学生|
  :参加考试;
  :答卷;
  |教师|
  :阅卷出成绩;

  fork
     :成绩单;
     |教务处|
     if (有不及格?) then (有)
  	:安排补考;
     endif
    |教师|
 |教务处|
 |教师|
  :补考安排表;
  fork again
     |教师|
     :答卷;
     :装订存档;
 |教师|
 |教务处|
 |教师|
  end fork
  :期末流程结束;
  stop
  @enduml
```

### 成绩管理流程图
![](./flow1.png)

流程图2：客户维修服务流程
--------------
#### plantUML的源码如下：
```
@startuml
|客户|
start
:申请服务;
|#AntiqueWhite|业务经理|
if (是新客户吗?) then (是)
   :登记客户信息;
endif
:上门勘察;
:制定方案;
|客户|
if(满意吗?) then (否)
end
else(是)
   :签订服务合同;
|业务经理|
fork
   :安排工人;
fork again
   :安排材料;
end fork
:填写派工单;
|工人|
:领取材料;
:上门服务;
|客户|
:验收并填写反馈意见;
|业务经理|
:交回派工单;
|#AntiqueWhite|财务人员|
:结算收款;
stop
@enduml
   ```
##### 客户维修服务流程图
![](./flow2.png)
