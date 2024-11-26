# springboot067中小型医院网站

## 简介

本代码仅供学习参考使用

加QQ(**3055269939**)免费获取项目和论文

## 主要内容

### ***\*数据库表设计\****

本基于Spring Boot的中小型医院网站需要后台数据库，本系统采用MYSQL数据库作为数据存储，下面介绍数据库中的各个表的详细信息。

表4-1  jiaofeiqingdan缴费清单信息表

| 字段名称         | 字段意义 | 字段类型  | 字段长度 | 是否主键 | 能否为空 |
| ---------------- | -------- | --------- | -------- | -------- | -------- |
| id               | 编号     | bigint    | 20       | 是       | 否       |
| addtime          | 创建时间 | timestamp |          | 否       | 是       |
| feiyongbianhao   | 费用编号 | varchar   | 200      | 否       | 是       |
| feiyongxiangmu   | 费用项目 | longtext  |          | 否       | 是       |
| feiyongjiage     | 费用价格 | int       | 11       | 否       | 是       |
| feiyongxiangqing | 费用详情 | longtext  |          | 否       | 是       |
| jianmianjine     | 减免金额 | int       | 11       | 否       | 是       |
| jianmianyuanyin  | 减免原因 | longtext  |          | 否       | 是       |
| `shifujine       | 实付金额 | varchar   | 200      | 否       | 是       |
| zhanghao         | 账号     | varchar   | 200      | 否       | 是       |
| xingming         | 姓名     | varchar   | 200      | 否       | 是       |
| sfsh             | 是否审核 | varchar   | 200      | 否       | 是       |
| `shhf`           | 审核回复 | longtext  |          | 否       | 是       |
| `ispay           | 是否支付 | varchar   | 200      | 否       | 是       |

表4-2  yuyueguahao预约挂号信息表

| 字段名称      | 字段意义 | 字段类型  | 字段长度 | 是否主键 | 能否为空 |
| ------------- | -------- | --------- | -------- | -------- | -------- |
| id            | 编号     | bigint    | 20       | 是       | 否       |
| addtime       | 创建时间 | timestamp |          | 否       | 是       |
| keshibianhao  | 科室编号 | varchar   | 200      | 否       | 是       |
| keshileixing  | 科室类型 | varchar   | 200      | 否       | 是       |
| yishixingming | 医师姓名 | varchar   | 200      | 否       | 是       |
| `guahaofei    | 挂号费   | varchar   | 200      | 否       | 是       |
| guahaoshijian | 挂号时间 | datetime  |          | 否       | 是       |
| beizhu`       | 备注     | longtext  |          | 否       | 是       |
| shouji        | 手机     | varchar   | 200      | 否       | 是       |
| zhanghao      | 账号     | varchar   | 200      | 否       | 是       |
| sfsh          | 是否审核 | varchar   | 200      | 否       | 是       |
| `shhf`        | 审核回复 | longtext  |          | 否       | 是       |
| `ispay        | 是否支付 | varchar   | 200      | 否       | 是       |

表4-3  yishi医师信息表

| 字段名称        | 字段意义 | 字段类型  | 字段长度 | 是否主键 | 能否为空 |
| --------------- | -------- | --------- | -------- | -------- | -------- |
| id              | 编号     | bigint    | 20       | 是       | 否       |
| addtime         | 创建时间 | timestamp |          | 否       | 是       |
| yishigonghao    | 医师工号 | varchar   | 200      | 否       | 是       |
| mima            | 密码     | varchar   | 200      | 否       | 是       |
| `yishixingming` | 医师姓名 | varchar   | 200      | 否       | 是       |
| `xingbie        | 性别     | varchar   | 200      | 否       | 是       |
| zhicheng`       | 职称     | varchar   | 200      | 否       | 是       |
| shouji          | 手机     | varchar   | 200      | 否       | 是       |
| `youxiang       | 邮箱     | varchar   | 200      | 否       | 是       |
| shenfenzheng    | 身份证   | varchar   | 200      | 否       | 是       |
| tupian          | 图片     | varchar   | 200      | 否       | 是       |

表4-4  users`管理员信息表 

| 字段名称  | 字段意义 | 字段类型  | 字段长度 | 是否主键 | 能否为空 |
| --------- | -------- | --------- | -------- | -------- | -------- |
| id        | 编号     | bigint    | 20       | 是       | 否       |
| username` | 用户名   | varchar   | 100      | 否       | 是       |
| password  | 密码     | varchar   | 100      | 否       | 是       |
| role`     | 角色     | varchar   | 100      | 否       | 是       |
| addtime   | 新增时间 | timestamp |          | 否       | 是       |

表4-5 yonghu用户信息表 

| 字段名称     | 字段意义 | 字段类型  | 字段长度 | 是否主键 | 能否为空 |
| ------------ | -------- | --------- | -------- | -------- | -------- |
| id           | 编号     | bigint    | 20       | 是       | 否       |
| addtime      | 创建时间 | timestamp |          | 否       | 是       |
| zhanghao     | 账号     | varchar   | 200      | 否       | 是       |
| mima         | 密码     | varchar   | 200      | 否       | 是       |
| xingming     | 姓名     | varchar   | 200      | 否       | 是       |
| xingbie      | 性别     | varchar   | 200      | 否       | 是       |
| shouji`      | 手机     | varchar   | 200      | 否       | 是       |
| youxiang     | 邮箱     | varchar   | 200      | 否       | 是       |
| shenfenzheng | 身份证   | varchar   | 200      | 否       | 是       |

表4-6 menzhenxinxi门诊信息表 

| 字段名称       | 字段意义 | 字段类型  | 字段长度 | 是否主键 | 能否为空 |
| -------------- | -------- | --------- | -------- | -------- | -------- |
| id             | 编号     | bigint    | 20       | 是       | 否       |
| addtime        | 创建时间 | timestamp |          | 否       | 是       |
| keshibianhao   | 科室编号 | varchar   | 200      | 否       | 是       |
| keshileixing   | 科室类型 | varchar   | 200      | 否       | 是       |
| yishixingming  | 医师姓名 | longtext  |          | 否       | 是       |
| zhicheng       | 职称     | varchar   | 200      | 否       | 是       |
| zhuanyetezhang | 专业特长 | longtext  |          | 否       | 是       |
| guahaofei      | 挂号费   | int       | 11       | 否       | 是       |
| xiangqing      | 详情     | longtext  |          | 否       | 是       |
| zhibanbiao     | 值班表   | longtext  |          | 否       | 是       |
| tupian         | 图片     | varchar   | 200      | 否       | 是       |