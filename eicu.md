# 检查检验



|                    |                            |
| ------------------ | -------------------------- |
| eicu_check_report  | 检查报告，一个患者多个报告 |
| eicu_checkout_info | 检查信息表，一对多检查条目 |
| eicu_checkout_item | 检查信息表条目表           |
|                    |                            |







| 检查报告             | eicu_check_report                  |
| -------------------- | ---------------------------------- |
| primary_id           | 主键ID                             |
| hosp_area            | 院区                               |
| exam_no              | 检验申请单号                       |
| patient_id           | 患者编号                           |
| visit_id             | 住院编号                           |
| critical_id          | 重症编号（患者编号和住院号的拼接） |
| report_title         | 检查报告标题                       |
| report_type          | 类型                               |
| position             | 部位                               |
| check_type           | 检查方式                           |
| description          | 影像描述                           |
| result               | 检查结果                           |
| exec_time            | 检查时间                           |
| report_datetime      | 报告时间                           |
| pictrue_url          | 报告影像查询地址                   |
| report_operator_name | 报告人姓名                         |
| report_operator_code | 报告人编号                         |
| check_doctor         | 审核医生                           |
| created_id           | 创建人                             |
| created_time         | 创建时间                           |
| updated_id           | 修改人                             |
| updated_time         | 修改时间                           |
| is_deleted           | 状态0:未删除 1：已删除             |





| 检查信息               | eicu_checkout_info                 |
| ---------------------- | ---------------------------------- |
| primary_id             | 主键ID                             |
| hosp_area              | 院区                               |
| patient_id             | 患者编号                           |
| visit_id               | 住院编号                           |
| critical_id            | 重症编号（患者编号和住院号的拼接） |
| title                  | 标题                               |
| test_id                | 单号                               |
| sample                 | 标本                               |
| exec_time              | 执行时间                           |
| report_time            | 报告日期                           |
| test_aims              | 检验目的                           |
| sampling_name          | 采样人                             |
| sampling_time          | 采样时间                           |
| receive_time           | 接收时间                           |
| send_inspection_doctor | 送检医师                           |
| inspection_doctor      | 检验医师                           |
| check_doctor           | 审核医师                           |
| created_id             | 创建人                             |
| created_time           | 创建时间                           |
| updated_id             | 修改人                             |
| updated_time           | 修改时间                           |
| is_deleted             | 状态                               |



| 检查条目        | eicu_checkout_item      |
| --------------- | ----------------------- |
| primary_id      | 主键ID                  |
| hosp_area       | 院区                    |
| item_code       | 检验项目编号            |
| item_name       | 项目名称                |
| test_id         | 单号                    |
| sub_id          | 检验子编号              |
| test_val        | 检验结果                |
| test_time       | 检验时间                |
| unit            | 单位                    |
| sign            | 标志 高H 低L 正常N      |
| max             | 最大参考值              |
| min             | 最小参考值              |
| sort            | 排序                    |
| reference_value | 结果范围                |
| focus           | 关注项：0:未关注 1:关注 |
| focus_sort      | 关注项排序              |
| created_id      | 创建人                  |
| created_time    | 创建时间                |
| updated_id      | 修改人                  |
| updated_time    | 修改时间                |
| is_deleted      | 状态                    |



关注：得分：已关注条目数+1，修改条目关注状态

取消关注：修改条目状态，重新排序设置sort





# 设备



？ 

时间-5分钟



查询程序配置信息

|                   |            |
| ----------------- | ---------- |
| sys_config        | 配置信息   |
| eicu_dict_info    | 字典信息   |
| pat_bed_equipment | 床位设备表 |
|                   |            |





```
患者类型0：正常 1：抢救  不是0分0秒的是抢救
```





# 护士



保存护嘱



更新/修改nursing_rec









| nursing_rec     | 护理记录表                               |
| --------------- | ---------------------------------------- |
| primary_id      | 系统编号                                 |
| critical_id     | 重症编号                                 |
| item_id         | 项目ID                                   |
| item_value      | 项目值                                   |
| item_type       | 项目类别：0-入量，1-出量，2-观察，3-护理 |
| exec_type       | 录入方式：0-手工采集，1-自动采集         |
| rec_date        | 记录日期                                 |
| rec_point       | 记录时间点                               |
| nurse_type_code | 护理分类                                 |
| signature       | 双签名用户                               |
| creator         | 创建人                                   |
| create_time     |                                          |
| updator         | 修改人                                   |
| update_time     |                                          |
| is_deleted      | 逻辑删除标识符                           |





| nursing_item_value_list |                           |
| ----------------------- | ------------------------- |
| column_name             | column_comment            |
| primaryId               | 系统编号                  |
| item_id                 | 监护字典id                |
| monitor_data_name       | 监测内容                  |
| item_value              | 值                        |
| input_code              | 输入码                    |
| status                  | 状态：0-可用，1-不可用    |
| created_id              | 创建人                    |
| created_time            |                           |
| updated_id              | 更新操作人                |
| updated_time            |                           |
| is_deleted              | 是否删除0：未删除 1：删除 |







| nursing_item    | 护理项                                   |
| --------------- | ---------------------------------------- |
| primary_id      | 系统编号                                 |
| item_id         | 项目ID                                   |
| item_name       | 项目名称                                 |
| item_unit       | 项目单位                                 |
| item_value_type | 项目值类型：数字、字符等等               |
| item_type       | 项目类别：0-入量，1-出量，2-观察，3-护理 |
| data_store      | 数据存储                                 |
| exac_type       | 录入方式：0-手工采集，1-自动采集         |
| sort            | 排序号                                   |
| nurse_type_code | 护理分类                                 |
| created_id      | 创建人                                   |
| created_time    |                                          |
| updated_id      | 修改人                                   |
| updated_time    |                                          |
| is_deleted      | 是否删除0：未删除 1：删除                |





| eicu_dict_info | 字典树                      |
| -------------- | --------------------------- |
| primary_id     | 主键编号                    |
| hosp_code      | 医院编号                    |
| hosp_area      | 院区编号                    |
| dict_code      | 字典编号                    |
| dict_name      | 字典名称                    |
| dict_value     | 字典值                      |
| shortcut_code  | 字典快捷码                  |
| dict_sort      | 字典排序                    |
| dict_status    | 字典状态                    |
| parent_id      | 父级字典                    |
| is_deleted     | 是否删除0：是未删除 1：删除 |
| created_id     | 创建人                      |
| created_time   | 创建时间                    |
| updated_id     | 修改人                      |
| updated_time   | 修改时间                    |



code，name，value=itemId



护理类型1:n护理项1:n护理值



护理字典

护理类型下的护理项

护理项写条目值列表





## 保存护嘱



知识库内容判断(对检查项值的范围进行判断)





| eicu_knowledge       |                                                 |
| -------------------- | ----------------------------------------------- |
| id                   | 主键                                            |
| hosp_area            | 院区                                            |
| rule_type            | 规则说明：1：检验规则，2：体征规则，3：药物规则 |
| project_name         | 项目名称                                        |
| ranges               | 范围                                            |
| conditions           | 条件                                            |
| unit                 | 单位                                            |
| suggestions_measures | 建议措施                                        |
| alert_level          | 提醒级别 0：关注时提醒，1：随时提醒             |
| operation            | 操作                                            |
| created_id           | 创建人                                          |
| created_time         | 创建时间                                        |
| updated_id           | 修改人                                          |
| updated_time         | 修改时间                                        |
| is_deleted           | 逻辑删除标识符                                  |











字典Value对应护理itemId





| vital_signs_config | 体征项配置                                                   |
| ------------------ | ------------------------------------------------------------ |
| primary_id         | 主键                                                         |
| param_code         | 参数code                                                     |
| param_name         | 参数名称                                                     |
| param_unit         | 单位                                                         |
| dept_code          |                                                              |
| hosp_area          |                                                              |
| hosp_code          |                                                              |
| param_type         | 参数类型：0、生命体征 2、体温单出量 3、体温单折线5、监测项目6、护嘱出量 |
| param_comment      | 参数说明                                                     |
| state              | 状态 1-禁用 0-启用                                           |
| icon_name          | 图标名字                                                     |





param_code与item_id





**病情观察列表**

code=HZBQGOJORE03713











nursing_rec(主要记录病人什么时候做了什么项目，项目值)，nursing_item(护理项目基本信息)，nursing_item_value_list(护理项目的取值列表)，eicu_dict_info(院区项目字典)

护理记录，护理项与取值通过item_id字段关联

护理字典的value与护理项的item_id关联



item_id



通过code，name，hospArea拿护理字典

先拿出院区所有的字典，构造字典树并排序



字典对应的护理项





？

cat_dict_special



鼻肠管/胃管

cat_dict_special 名字映射

cat_catheter_pat_info 患者导管信息表

cat_catheter_care_record 导管护理记录表

cat_catheter_model_relation 导管和人体模型位置关系表

cat_dict_model  皮肤信息表

cat_dict_catheter 导管信息表





pre_anonym_info死亡人员登记信息





































# 医嘱



* 医嘱子医嘱

* 医嘱执行
* 组医嘱
* 交班





## **数据字典**

| table_name               | comment      |
| ------------------------ | ------------ |
| eicu_order_info          | 医嘱信息表   |
| eicu_order_detail        | 医嘱详情表   |
| eicu_order_exec_record   | 医嘱执行记录 |
| eicu_order_column_config | 医嘱列配置   |



？ 

* 医嘱与子医嘱
* his_order_id,order_id
* 修改最后一个子医嘱编号
* 住医嘱的总剂量与剩余剂量



**新建医嘱**

*医嘱状态：*有执行量的的医嘱状态是执行中

*剩余量：*总量

*医嘱详情：*































## 创建保存医嘱



一般不手动建



saveOrder



### 分组与频次







**创建分组**



分组(通过OrderID)

每一组的类别/途径/频次是一样的

所有数据存入`医嘱详情表`

每组第一个医嘱的子医嘱ID为null，存入`医嘱信息表`

如果有医嘱频率，要在重复`n-1`次，重新生成OrderID，有n个一样的医嘱(组)





？ 

* 添加/修改分组中的医嘱
* 调整频率





```json
{
     "addListData": [
          {
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06T17:18:55",
               "defaultStopTime": "2023-12-07T06:59:59",
               "dosage": "1",
               "dosageUnit": "g",
               "frequency": "Qd",
               "odClass": "0",
               "odCode": null,
               "odName": "a1",
               "odType": "0",
               "orderId": "54135273627193344",
               "orderSubId": null,
               "useWay": "口服"
          },
          {
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06T17:18:55",
               "defaultStopTime": "2023-12-07T06:59:59",
               "dosage": "1",
               "dosageUnit": "g",
               "frequency": "Qd",
               "odClass": "0",
               "odCode": null,
               "odName": "b1",
               "odType": "0",
               "orderId": "54135273627193344",
               "orderSubId": "e4d1134c-3291-4692-b940-6fbd60539f53",
               "useWay": "口服"
          }
     ],
     "deleteListData": [],
     "updateListData": []
}
```





### **更新医嘱**







只更新选中的医嘱



## 删除医嘱





不删除医嘱。删执行计划











































































order/getCreateOrdersList/2023-12-06/53327533511806976_14523652

```json
{
     "code": 200,
     "data": [
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 14:27:01",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ug",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Bid",
               "hisOrderId": null,
               "isDrugOrder": 0,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "血制品",
               "odCode": null,
               "odName": "x6",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133921764741120",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "332",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ug",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 14:31:37",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ug",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 0,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "血制品",
               "odCode": null,
               "odName": "x7",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133957937598464",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "333",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ug",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 14:33:17",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ug",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 0,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "血制品",
               "odCode": null,
               "odName": "x8",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133971034574848",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "334",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ug",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 14:34:16",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ug",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 0,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "血制品",
               "odCode": null,
               "odName": "x9",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133978804523008",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "335",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ug",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 14:56:38",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 0,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "血制品",
               "odCode": null,
               "odName": "x10",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134154735915008",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "336",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ml",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 15:26:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ug",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 0,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "血制品",
               "odCode": null,
               "odName": "x11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134390418182144",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "337",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ug",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 15:29:19",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x22",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134411715022848",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "338",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 15:42:26",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x33",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134514914430976",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "342",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 15:42:26",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x33",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134518156627968",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "343",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 15:42:26",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x33",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134518161215488",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "344",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 15:42:26",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x33",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134518164623360",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "345",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 15:42:26",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x33",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134518168948736",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "346",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 15:42:26",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x33",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54134518171963392",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "347",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "鼻饲"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:30:34",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Prn",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x44",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54134904381378560",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "354",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": "jackli",
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:30:34",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x44",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54134893435817984",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "349",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:30:34",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x44",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54134904363028480",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "350",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:30:34",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x44",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54134904371023872",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "351",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:30:34",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x44",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54134904374562816",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "352",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:30:34",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x44",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54134904377708544",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "353",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:30:34",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 2,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Prn",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x55",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54134904381378560",
               "orderSubId": "0067f38c-8602-44df-b4f2-95b94f90ee34",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "354",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": "jackli",
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:30:34",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 3,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Prn",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x66",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54134904381378560",
               "orderSubId": "7d745b0d-8591-478d-a7e5-febe06e052c1",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "354",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": "jackli",
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Prn",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "f11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135050990129152",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "356",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": "jackli",
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Prn",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "m11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135050990129152",
               "orderSubId": "0341ef3f-786c-42e6-83f5-17855cae7bc2",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "356",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": "jackli",
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Prn",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "n11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135050990129152",
               "orderSubId": "d6eb0dc0-98a4-4204-ba7e-ca0abf07c79a",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "356",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": "jackli",
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "f11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063017689088",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "357",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "f11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063023063040",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "358",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "f11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063028043776",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "359",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "f11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063033286656",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "360",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "f11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063038267392",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "361",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "m11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063017689088",
               "orderSubId": "5001c7a1-b2c4-4e09-b0f9-2d2145af2831",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "357",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "m11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063023063040",
               "orderSubId": "2449a7de-1b99-4a6c-85ac-4d1ecdf5e4e2",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "358",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "m11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063028043776",
               "orderSubId": "4f8b3ff5-c8a5-45d9-9f09-e360f345ac01",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "359",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "m11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063033286656",
               "orderSubId": "4f5adde6-4b32-46ac-82ba-0a277bc469fb",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "360",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "m11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063038267392",
               "orderSubId": "ef9f0e98-27d8-48c0-8c0c-234023a30952",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "361",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "n11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063017689088",
               "orderSubId": "4fde7614-aa4f-48f8-919a-d6fada66c309",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "357",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "n11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063023063040",
               "orderSubId": "ad0072c3-5fa7-44dc-b6a0-aea9c7c0e244",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "358",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "n11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063028043776",
               "orderSubId": "193f1510-7d68-4bec-b338-75ff0c20ec45",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "359",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "n11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063033286656",
               "orderSubId": "187a5d3c-06e3-4564-849f-958952f08cfd",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "360",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "jackli",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 16:50:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "g",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "n11",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54135063038267392",
               "orderSubId": "d1753004-ad74-4743-b789-90c8a6fc886a",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "361",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "g",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 10:19:56",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Prn",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": "1",
               "isSingleDrug": "0",
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "(G)阿司匹林肠溶片",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "执行中",
               "odType": "临时医嘱",
               "orderId": "54131978601238528",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "321",
               "startTime": "2023-12-06 10:22:01",
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ml",
               "transfuseWay": null,
               "updatedId": "zgx",
               "useWay": "口服"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 10:19:56",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Prn",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": "1",
               "isSingleDrug": "0",
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "1(G)葡萄糖氯化钠注射液(百特)",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "执行中",
               "odType": "临时医嘱",
               "orderId": "54131978601238528",
               "orderSubId": "321ef943-5d24-4520-9cd0-1e19a3f22786",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "321",
               "startTime": "2023-12-06 10:22:01",
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ml",
               "transfuseWay": null,
               "updatedId": "zgx",
               "useWay": "口服"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 10:29:28",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "瓶",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "输液",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54132053638385664",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "322",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "瓶",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "静注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 10:29:28",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 100,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "复方维生素(3)注射液(唯帛)",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54132053638385664",
               "orderSubId": "052cd445-360b-4dae-84fb-66d4e2938587",
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "322",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "瓶",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "静注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 11:07:03",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "袋",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 0,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "血制品",
               "odCode": null,
               "odName": "(J)20%人血白蛋白(基立福)",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "长期医嘱",
               "orderId": "54132349156200448",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "323",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "袋",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "口服"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 11:11:36",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "阿斯qd",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54132384931516416",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "324",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ml",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "皮下"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 11:15:00",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "支",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "asiqd",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54132411751862272",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "325",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "支",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "肌注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 13:42:37",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "xqd",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133572671377408",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "326",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ml",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "静注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 13:43:44",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x1qd",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133581458444288",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "327",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ml",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "静注"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 13:48:05",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x2qd",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133615602831360",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "328",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ml",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "泵入"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 13:49:11",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ml",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x3qd",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133624220160000",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "329",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ml",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "泵入"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 13:51:54",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 2,
               "dosageUnit": "瓶",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x4qd",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133645570084864",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "330",
               "startTime": null,
               "stopTime": null,
               "surplus": 2,
               "totalDose": 2,
               "totalDoseUnit": "瓶",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "泵入"
          },
          {
               "abortTime": null,
               "changeFlag": 0,
               "createdId": "zgx",
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06 13:53:59",
               "defaultStopTime": "2023-12-07 06:59:59",
               "dosage": 1,
               "dosageUnit": "ug",
               "execOrdersDTOList": null,
               "finishDosage": null,
               "frequency": "Qd",
               "hisOrderId": null,
               "isDrugOrder": 1,
               "isHisOrder": 0,
               "isNutrition": null,
               "isSingleDrug": null,
               "medType": null,
               "odClass": "药品",
               "odCode": null,
               "odName": "x5",
               "odSpec": null,
               "odSpeed": null,
               "odSpeedUnit": null,
               "odStatus": "未执行",
               "odType": "临时医嘱",
               "orderId": "54133661975842816",
               "orderSubId": null,
               "pauseTime": null,
               "prepareDosage": null,
               "primaryId": "331",
               "startTime": null,
               "stopTime": null,
               "surplus": 1,
               "totalDose": 1,
               "totalDoseUnit": "ug",
               "transfuseWay": null,
               "updatedId": null,
               "useWay": "泵入"
          }
     ],
     "errCode": "00000",
     "msg": "ok",
     "success": true,
     "userTip": ""
}
```



order/addOrders/53327533511806976_14523652/012

```json
{"isMainOrder":1}

{
     "code": 200,
     "data": {
          "criticalId": "53327533511806976_14523652",
          "defaultStartTime": "2023-12-06 17:18:55",
          "defaultStopTime": "2023-12-07 06:59:59",
          "dosage": null,
          "dosageUnit": null,
          "execDosage": null,
          "frequency": null,
          "isHisOrder": 0,
          "isMainOrder": "1",
          "odClass": null,
          "odCode": null,
          "odName": null,
          "odType": null,
          "orderId": "54135273627193344",
          "orderSubId": null,
          "patientId": "012",
          "subList": null,
          "totalDose": null,
          "totalDoseUnit": null,
          "useWay": null
     },
     "errCode": "00000",
     "msg": "ok",
     "success": true,
     "userTip": ""
}
```



order/addOrders/53327533511806976_14523652/01

```json
{"isMainOrder":0,"orderId":"54135273627193344"}

{
     "code": 200,
     "data": {
          "criticalId": "53327533511806976_14523652",
          "defaultStartTime": "2023-12-06 17:19:19",
          "defaultStopTime": "2023-12-07 06:59:59",
          "dosage": null,
          "dosageUnit": null,
          "execDosage": null,
          "frequency": null,
          "isHisOrder": 0,
          "isMainOrder": "0",
          "odClass": null,
          "odCode": null,
          "odName": null,
          "odType": null,
          "orderId": "54135273627193344",
          "orderSubId": "e4d1134c-3291-4692-b940-6fbd60539f53",
          "patientId": "012",
          "subList": null,
          "totalDose": null,
          "totalDoseUnit": null,
          "useWay": null
     },
     "errCode": "00000",
     "msg": "ok",
     "success": true,
     "userTip": ""
}
```



order/saveOrder

```json
{
     "addListData": [
          {
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06T17:18:55",
               "defaultStopTime": "2023-12-07T06:59:59",
               "dosage": "1",
               "dosageUnit": "g",
               "frequency": "Qd",
               "odClass": "0",
               "odCode": null,
               "odName": "a1",
               "odType": "0",
               "orderId": "54135273627193344",
               "orderSubId": null,
               "useWay": "口服"
          },
          {
               "criticalId": "53327533511806976_14523652",
               "defaultStartTime": "2023-12-06T17:18:55",
               "defaultStopTime": "2023-12-07T06:59:59",
               "dosage": "1",
               "dosageUnit": "g",
               "frequency": "Qd",
               "odClass": "0",
               "odCode": null,
               "odName": "b1",
               "odType": "0",
               "orderId": "54135273627193344",
               "orderSubId": "e4d1134c-3291-4692-b940-6fbd60539f53",
               "useWay": "口服"
          }
     ],
     "deleteListData": [],
     "updateListData": []
}
```



**order/getExecList**



























































## 修改医嘱





























































## 执行医嘱





![image-20231208113855805](E:\Users\LAN-IT-0212\AppData\Roaming\Typora\typora-user-images\image-20231208113855805.png)

执行医嘱是执行一组内的所有医嘱



首次执行的执行总量



修改主医嘱，新增执行记录



### **开始执行**



执行指的是整个医嘱组



前置条件：待入量为总量，没有其他执行记录

？

营养液

单次用药 

速率



```
isSingleDrug: "1"
isNutrition: "0"
```



1. 更新主医嘱状态，开始时间，剩余量，是否是营养液/单词用药，(泵入类型的：速率，速率单位，输液路数). 
2. 新增执行记录



### 执行



前置条件：待入量判断

修改主医嘱的状态与剩余量等

新增执行记录





### **暂停医嘱**



前置条件：执行中的

更新主医嘱状态

生成执行记录：执行量为0.0，剩余量与最新一次执行记录相同



### **恢复执行**





前置条件：状态为已暂停

修改状态为执行中

添加执行记录







### **中断医嘱**



前置条件：执行中的

更新主医嘱状态，添加完成时间

生成执行记录：执行量为0.0，剩余量与最新一次执行记录相同































































### 完成医嘱





更新医嘱状态

执行剂量=剩余剂量

新增执行记录



### 取消完成



就是删除执行记录，更新主医嘱状态，重新开始执行



### 删除医嘱

物理删除



### 还原医嘱

修改删除状态



















































**执行类型**



开始

执行

完成





医嘱状态



**主医嘱与子医嘱**

主医嘱有完成量



总剂量，剩余量，完成量

新建医嘱时detail里没加总剂量，剩余量，要跟着主医嘱走



医嘱默认开始时间









































































## 医嘱执行列表







**时间点**

* 当天的早八到晚八
* 未执行的医嘱，时间点集中加上默认开始时间



**过滤条件**

1. 默认开始时间在今天的时间点内的可以展示
2. 默认开始时间小于今天8点并且不是完成/中断
3. 当日中断/完成的





主医嘱

设置完成量

如果没有执行且状态为已暂停，设置暂停时间



所有医嘱根据useWay排序



























## 列配置





单表CRUD



## 交接班









获取医嘱交班信息



change_flagshi否交接班







# 评估评分



```
得到评估表

```



## 数据字典



|                      |                                     |
| -------------------- | ----------------------------------- |
| eicu_eval_sheet      | 评估单名称,类型，排序等基本信息信息 |
| eicu_eval_sheet_data | 评估得分记录                        |
|                      |                                     |



？

* 保护性约束巡视记录表









apache评分，生命体征

1.12汇报PPT





![image-20231212113911930](E:\Users\LAN-IT-0212\AppData\Roaming\Typora\typora-user-images\image-20231212113911930.png)



* 平均动脉压：Mean Arterial Pressure
* PaO2：动脉血氧分压
* A-aDO2：动脉血氧分压（PaO2）与静脉血氧分压（PvO2）之间的氧分压差





## Apache II



年龄

```
dandelion-eicu-patient/pat_info/globalPatientsBasicInformation
```























































