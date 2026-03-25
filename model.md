# 学生选课成绩系统 - 数据库设计方案

## 1. 学生表 (Student)
- 负责人：组员 1 (学生姓名)
| 字段名 | 数据类型 | 约束 | 说明 |
| :--- | :--- | :--- | :--- |
| **stu_id** | VARCHAR(20) | PRIMARY KEY | 学号（主键） |
| stu_name | VARCHAR(50) | NOT NULL | 学生姓名 |
| gender | CHAR(2) | CHECK (gender IN ('男', '女')) | 性别 |
| birth_date | DATE | - | 出生日期 |
| dept_name | VARCHAR(100) | - | 所属院系 |

## 2. 教师表 (Teacher)
- 负责人：组员 1 (学生姓名)
字段名,数据类型,约束,说明
tea_id,VARCHAR(20),PRIMARY KEY,教师工号（主键）
tea_name,VARCHAR(50),NOT NULL,教师姓名
title,VARCHAR(30),-,职称（如：教授、副教授）
dept_name,VARCHAR(100),-,所属院系

## 3. 课程表 (Course)
- 负责人：组员 2 (你的姓名)
| 字段名 | 数据类型 | 约束 | 说明 |
| :--- | :--- | :--- | :--- |
| **course_id** | VARCHAR(20) | PRIMARY KEY | 课程号 |
| course_name | VARCHAR(100) | NOT NULL | 课程名 |
| credit | INT | - | 学分 |

## 4. 选课成绩表 (Score)
- 负责人：组员 2 (你的姓名)
| 字段名 | 数据类型 | 约束 | 说明 |
| :--- | :--- | :--- | :--- |
| **sid** | VARCHAR(20) | FOREIGN KEY | 学生学号（注意：故意不统一命名） |
| **cid** | VARCHAR(20) | FOREIGN KEY | 课程号 |
| grade | INT | - | 考试成绩 |
