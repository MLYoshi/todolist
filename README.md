# Todo List 应用

基于 MERN 栈（MongoDB + Express + React + Node.js）开发的待办事项管理应用。

## 📋 功能特性

- 用户注册与登录（JWT 认证）
- 创建、查看、更新、删除待办事项
- 响应式 UI 设计（Tailwind CSS）
- RESTful API 接口

## 🛠️ 技术栈

### 后端
- **Node.js** - 运行时环境
- **Express** - Web 框架
- **MongoDB** - 数据库
- **Mongoose** - ODM 库
- **JWT** - 身份认证

### 前端
- **React** - UI 库
- **Vite** - 构建工具
- **Redux Toolkit** - 状态管理
- **React Router** - 路由管理
- **Tailwind CSS** - CSS 框架
- **Axios** - HTTP 客户端

## 📁 项目结构

```
todolist/
├── backend/
│   ├── config/         # 数据库配置
│   ├── controllers/    # 控制器逻辑
│   ├── middleware/     # 中间件（认证、错误处理）
│   ├── models/         # 数据模型
│   ├── routes/         # API 路由
│   └── server.js       # 入口文件
├── frontend/
│   ├── src/            # 前端源代码
│   ├── public/         # 静态资源
│   └── index.html      # HTML 模板
├── .env                # 环境变量配置
└── package.json        # 项目依赖
```

## 🚀 快速开始

### 前置要求

- Node.js (v14+)
- MongoDB（本地安装或 MongoDB Atlas）

### 安装步骤

1. **克隆项目**
   ```bash
   git clone <repository-url>
   cd todolist
   ```

2. **安装后端依赖**
   ```bash
   npm install
   ```

3. **安装前端依赖**
   ```bash
   cd frontend
   npm install
   cd ..
   ```

4. **配置环境变量**

   在项目根目录创建 `.env` 文件：
   ```env
   PORT=8080
   MONGO_URI=mongodb://localhost:27017/todolist
   NODE_ENV=development
   JWT_SECRET=your_jwt_secret_key
   ```

   > ⚠️ 请修改 `MONGO_URI` 为你的 MongoDB 连接地址

### 运行项目

#### 开发模式

**启动后端**（终端 1）：
```bash
npm run dev
```

**启动前端**（终端 2）：
```bash
cd frontend
npm run dev
```

#### 生产模式

```bash
# 构建前端
cd frontend
npm run build

# 启动后端（同时服务前端静态文件）
cd ..
npm start
```

## 📡 API 端点

### 用户认证

| 方法 | 端点 | 描述 |
|------|------|------|
| POST | `/api/users` | 注册新用户 |
| POST | `/api/users/login` | 用户登录 |
| GET | `/api/users/me` | 获取当前用户（需认证） |

### 待办事项

| 方法 | 端点 | 描述 |
|------|------|------|
| GET | `/api/goals` | 获取所有待办事项（需认证） |
| POST | `/api/goals` | 创建新待办事项（需认证） |
| PUT | `/api/goals/:id` | 更新待办事项（需认证） |
| DELETE | `/api/goals/:id` | 删除待办事项（需认证） |

## 🌐 访问地址

- **前端开发服务器**: `http://localhost:5173`
- **后端 API**: `http://localhost:8080`

## 📝 环境变量说明

| 变量名 | 说明 | 默认值 |
|--------|------|--------|
| PORT | 后端服务端口 | 8080 |
| MONGO_URI | MongoDB 连接字符串 | 必填 |
| NODE_ENV | 运行环境 | development |
| JWT_SECRET | JWT 密钥 | 必填 |

## 📄 License

MIT
