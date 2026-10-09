# Web 前端课程设计：学生成绩管理系统

本项目是 Web 前端课程设计的最终成果，完成了一个前后端分离的学生成绩管理系统。系统支持管理员、教师、学生三类用户登录，并提供成绩管理、组合查询、分页、统计分析、智能预警和一键启动演示功能。

## 项目亮点

- 账号登录后自动识别管理员、教师或学生身份。
- 教师只能查看和修改自己所教课程的成绩，学生只能查看个人成绩。
- 支持成绩新增、修改、删除、排序、组合筛选和分页。
- 支持成绩等级统计、课程均分、班级排名、课程表现和风险学生预警。
- 同时支持 MySQL 正式数据库模式与 SQLite 便携演示模式。
- 提供 Windows 一键启动脚本，便于答辩时在新电脑演示。

## 技术栈

| 模块 | 技术 |
| --- | --- |
| 前端 | HTML、CSS、JavaScript |
| 后端 | Python、Flask、Flask-Cors |
| 数据库 | MySQL、SQLite |
| 数据交互 | RESTful API、JSON |
| 部署 | PowerShell、BAT |

## 快速演示

推荐在 Windows 电脑上安装 Python 3 后，直接双击项目根目录的：

```text
一键启动演示.bat
```

脚本会自动完成以下操作：

```text
创建 Python 虚拟环境
安装后端依赖
生成 SQLite 演示数据库
启动 Flask 后端
启动前端本地服务并打开登录页
```

登录测试账号：

| 身份 | 账号 | 密码 |
| --- | --- | --- |
| 管理员 | admin | 123456 |
| 教师 | teacher | 123456 |
| 学生 | 20240001 | 123456 |

## MySQL 模式

如需使用 MySQL，请先创建并导入数据库，再启动系统：

```powershell
powershell -ExecutionPolicy Bypass -File .\scripts\init_demo.ps1
powershell -ExecutionPolicy Bypass -File .\scripts\start_demo.ps1
```

数据库脚本位于 `database/`：

- `schema.sql`：创建数据库及核心表。
- `seed.sql`：基础测试数据。
- `bulk_seed.sql`：批量测试数据，包含 1 名管理员、12 名老师、120 名学生、48 条开课记录和 960 条成绩记录。

## 项目结构

```text
.
├── frontend/       前端页面、样式和交互代码
├── backend/        Flask 后端接口与数据库工具
├── database/       MySQL 建表与测试数据脚本
├── scripts/        启动、初始化和 SQLite 演示脚本
├── docs/           需求、分工、测试、使用和打包说明
├── outputs/        最终课程设计报告与答辩 PPT
├── 一键启动演示.bat
└── README.md
```

## 最终材料

- `outputs/学生成绩管理系统-项目汇报.pptx`：答辩汇报 PPT（已清理作者和生成工具元数据）。
- `outputs/B2051009_Web前端课程设计_学生成绩管理系统_完善版.docx`：课程设计报告。
- `docs/09-第12周接口测试记录.md`：接口与权限测试记录。
- `docs/02-小组分工.md`：四人小组分工说明。

## 相关文档

- [系统使用说明](docs/08-系统使用说明.md)
- [新电脑快速演示说明](docs/10-新电脑快速演示说明.md)
- [数据库模式切换说明](docs/12-数据库模式切换说明.md)
- [GitHub 上传说明](docs/14-GitHub上传说明.md)
