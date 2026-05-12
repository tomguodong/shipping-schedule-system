# 海运整柜船期查询系统 (Shipping Schedule System)

一个功能完善的海运整柜船期查询管理系统，支持多数据源刷新、批量价格编辑、SQLite数据库存储等功能。

## 功能特性

- 📋 **船期查询** - 支持按船公司、起运港、目的港、航线等多维度筛选
- ➕ **添加船期** - 手动添加新的船期记录
- 🔄 **刷新船期** - 从多个数据源（GitHub、COSCO、Maersk等）自动获取最新船期
- 💰 **批量修改价格** - 支持批量编辑 20GP/40GP/40HQ 价格
- 🗄️ **数据库存储** - 使用 SQLite 数据库存储，支持数据持久化
- 🤖 **AI 助手** - 内置智能问答助手

## 技术栈

- **后端**: Python + Flask
- **前端**: HTML + CSS + JavaScript (原生)
- **数据库**: SQLite
- **API**: RESTful API

## 快速开始

### 安装依赖

```bash
pip install flask flask_cors
```

### 启动服务器

```bash
python server.py
```

服务器将在 http://127.0.0.1:5000 启动

### 默认管理员账号

- 用户名: `admin`
- 密码: `admin123`

## 数据源支持

系统支持以下数据源刷新船期：

| 数据源 | 状态 | 说明 |
|--------|------|------|
| GitHub 开源数据 | ✅ 可用 | 开源爬虫数据，免费无限制 |
| COSCO 中远海运 | ⚠️ 需配置 | 官方开放API，需申请Key |
| Maersk 马士基 | ⚠️ 需配置 | DCSA标准API，需OAuth认证 |
| MSC 地中海航运 | ⚠️ 需配置 | DCSA标准API，需注册 |
| SeaRates | ⚠️ 需配置 | 第三方平台，付费API |
| VesselFinder | ⚠️ 需配置 | AIS船舶追踪，免费额度 |

## 项目结构

```
shipping-schedule/
├── index.html      # 主页面（前端）
├── admin.html      # 管理后台
├── server.py       # Flask后端服务
├── README.md       # 项目说明
└── .gitignore      # Git忽略文件
```

## 浏览器访问

打开浏览器访问: http://127.0.0.1:5000

## 版本历史

- v4.4 - 添加多数据源刷新功能
- v4.3 - 添加SQLite数据库支持
- v4.2 - 修复全宽布局
- v4.1 - 添加批量价格编辑
- v4.0 - 初始版本

## License

MIT License
