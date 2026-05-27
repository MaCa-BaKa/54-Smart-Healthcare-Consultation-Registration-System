# 54-智慧医疗问诊-挂号系统

[文档地址](http://wechat.zjrcsy.cn/)

# 54-智慧医疗问诊-挂号系统


[文档地址](http://wechat.zjrcsy.cn/)


**技术栈：** Spring Boot + Vue

**访问说明：** 本项目采用前后端分离部署；前端通过 Vite 开发服务访问，后端提供 `/api` 业务接口与本地 `/upload` 文件访问能力。默认后端端口为 `8080`，前端端口为 `5173`，数据库脚本位于 `sql/yyghgl.sql`，具体配置以 `src/main/resources/application.yml` 与 `frontend/vite.config.js` 为准。


## 补充说明

- 后端技术要点：Spring Boot 3、MyBatis-Plus、JWT 登录鉴权、MySQL、本地文件上传、统一响应封装、操作日志切面、统计分析接口、智谱 AI 问诊接口等。
- 前端技术要点：Vue 3、Vite、Element Plus、Pinia、Vue Router、Axios、ECharts、Sass 等。


## 患者端

1. **患者登录与注册：** 患者独立入口登录，支持新用户注册；登录后使用 JWT 保存会话信息。
2. **首页：** 展示轮播图、欢迎横幅、挂号统计、热门科室、系统公告、医疗资讯与快捷入口。
3. **AI 智能问诊：** 患者可输入症状描述，系统返回症状分析、风险等级、推荐科室、推荐医生与健康建议。
4. **科室浏览：** 展示医院科室分类、科室说明、常见疾病与对应医生数量，便于患者按科室查找医生。
5. **医生列表与详情：** 支持按科室查看医生，展示医生职称、擅长方向、挂号费、评分与排班信息。
6. **在线挂号：** 患者可选择医生、排班日期与时段提交挂号，并通过余额完成挂号支付。
7. **我的挂号：** 查看个人挂号记录、状态、就诊时间、医生信息与费用信息。
8. **电子病例：** 查看医生开具的病例记录，包括主诉、诊断、处理意见与医嘱。
9. **处方记录：** 查看处方列表与处方详情，支持药品明细、用法用量、费用与支付状态查看。
10. **检查记录：** 查看检查项目、检查费用、报告上传状态与报告图片。
11. **医患沟通与消息中心：** 支持患者与医生在线沟通，查看系统通知、就诊提醒与业务消息。
12. **医疗资讯：** 浏览健康科普文章，支持查看分类、作者、阅读量与文章详情。
13. **个人中心：** 维护头像、姓名、性别、年龄、手机号、过敏史、既往病史、账户余额等资料。


## 医生端

1. **工作台首页：** 展示今日挂号、待接诊、已完成、总挂号、病例数、处方数，以及近 7 天接诊趋势图。
2. **挂号管理：** 医生查看分配给自己的患者挂号列表，处理待就诊、已完成、取消与爽约等状态。
3. **病例管理：** 医生可为就诊患者新增病例，维护主诉、诊断、现病史、治疗方案与医嘱。
4. **处方记录：** 医生可开具处方，选择药品、填写用法用量，并自动计算处方金额。
5. **检查记录：** 医生可为患者创建检查单，维护检查项目、费用、说明，并上传检查报告。
6. **患者管理：** 医生查看重点患者与相关就诊信息，便于持续随访与健康管理。
7. **排班管理：** 医生维护自己的出诊日期、上午/下午时段、可预约数量与排班状态。
8. **就诊评价：** 查看患者对医生的评分与评价内容。
9. **医患沟通：** 医生与患者进行在线会话，支持未读消息提示与图文消息记录。
10. **消息中心与个人中心：** 查看系统消息，维护医生个人资料与头像等信息。


## 管理员端

1. **数据统计：** 展示患者数、医生数、科室数、挂号数、病例数、AI 问诊数、药品数等核心指标，并提供用户增长、科室挂号量、挂号状态分布图表。
2. **用户管理：** 管理管理员、医生、患者账号，支持检索、分页、启用/禁用与重置密码。
3. **科室管理：** 维护科室名称、类型、图标、介绍、常见疾病、排序与启用状态。
4. **医生管理：** 管理医生账号、所属科室、职称、擅长方向、简介、挂号费与评分等信息。
5. **挂号管理：** 查看全院挂号记录，支持按患者、医生、日期、状态等条件管理业务数据。
6. **病例管理：** 查看所有病例记录，便于院内统一监管与追踪。
7. **药品管理：** 维护药品名称、分类、规格、单价、库存、适应症、禁忌与状态。
8. **评价管理：** 管理患者评价内容，支持查看评分与隐藏违规评价。
9. **首页轮播图：** 维护患者端首页轮播图标题、图片、跳转链接、排序与上下架状态。
10. **公告管理：** 发布医院公告与系统通知，支持置顶、启用与禁用。
11. **医疗资讯文章：** 发布健康科普文章，维护分类、封面图、作者与正文内容。
12. **AI 对话管理：** 查看患者 AI 问诊记录、症状输入、系统分析结果与推荐科室医生。
13. **操作日志：** 记录后台关键操作，包括操作人、方法、参数、IP、耗时与结果状态。
14. **系统配置：** 维护系统名称、医院名称、联系电话、地址、挂号规则等基础配置。


## 患者端界面示意

![患者登录](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/01_patient_login.png)

![患者首页](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/02_patient_home.png)

![AI智能问诊](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/03_patient_ai_chat.png)

![科室浏览](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/04_patient_departments.png)

![医生列表](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/05_patient_doctors.png)

![我的挂号](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/06_patient_appointments.png)

![我的病例](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/07_patient_medical_records.png)

![我的处方](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/08_patient_prescriptions.png)

![检查记录](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/09_patient_inspections.png)

![医疗资讯](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/10_patient_articles.png)


## 医生端界面示意

![医生工作台](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/11_doctor_dashboard.png)

![医生挂号管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/12_doctor_appointments.png)

![医生病例管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/13_doctor_medical_records.png)

![医生处方记录](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/14_doctor_prescriptions.png)

![医生检查记录](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/15_doctor_inspections.png)

![患者管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/16_doctor_patients.png)

![排班管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/17_doctor_schedules.png)


## 管理员端界面示意

![管理员数据统计](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/18_admin_dashboard.png)

![用户管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/19_admin_users.png)

![科室管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/20_admin_departments.png)

![医生管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/21_admin_doctors.png)

![挂号管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/22_admin_appointments.png)

![药品管理](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/23_admin_medicines.png)

![医疗资讯文章](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/24_admin_articles.png)

![系统配置](https://yunzhuceshi.oss-cn-beijing.aliyuncs.com/typoraImg/25_admin_config.png)

