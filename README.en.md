<div align="center">
   <p align="center">
      <img src="./mkdocs/docs/resources/images/logo.png" height="150" alt="logo"/>
   </p>
      <h1 align="center" style="margin: 30px 0 30px; font-weight: bold;">Fastapi-Vue3-Admin v1.0.0</h1>
      <h4 align="center">A fast development framework for Web + Mini Programs + H5 applications based on the separation of front-end and back-end in Fastapi-Vue-Admin.</h4>
   <p align="center">
      <a href="https://gitee.com/tao__tao/fastapi_vue3_admin.git">
         <img src="https://gitee.com/tao__tao/fastapi_vue3_admin/badge/star.svg?theme=dark">
      </a>
      <a href="https://github.com/1014TaoTao/fastapi_vue3_admin.git">
         <img src="https://img.shields.io/github/stars/1014TaoTao/fastapi_vue3_admin?style=social">
      </a>
      <a href="https://gitee.com/tao__tao/fastapi_vue3_admin/blob/master/LICENSE">
         <img src="https://img.shields.io/badge/License-MIT-orange">
      </a>
      <img src="https://img.shields.io/badge/Python-≥3.10-blue">
      <img src="https://img.shields.io/badge/NodeJS-≥20.0-blue">
      <img src="https://img.shields.io/badge/MySQL-≥8.0-blue">
      <img src="https://img.shields.io/badge/Redis-≥7.0-blue">
   </p>
</div>

English | [Chinese](./README.md)

## 📚 Project Introduction

**Fastapi-Vue3-Admin** is a fully open-source modern rapid development platform designed to help developers efficiently build high-quality backend systems. The project integrates the high-performance backend framework FastAPI and the powerful ORM library SQLAlchemy, along with the frontend technology stack Vue3, Vite6, Ant Design Vue, and the mobile development framework UniApp and its component library uView-plus, providing developers with an out-of-the-box solution. The project directory structure is as follows:

```sh
fastapi_vue_admin
├─ backend        # Backend project
├─ frontend       # Frontend project
├─ devops         # Deployment project
├─ mkdocs         # Documentation project
├─ uni-app        # Uni-app project
├─ README.en.md   # English documentation
└─ README.md      # Chinese documentation
```

- **Backend**:
  - **FastAPI**:A modern, high-performance asynchronous framework.
  - **Swagger**:Automatically generates interactive API documentation.
  - **Pydantic**:Enforces type constraints.
  - **SQLAlchemy 2.0**:A powerful ORM library.
  - **APScheduler**:A powerful job scheduling library.

- **Frontend**:
  - **Vue3**:A modern frontend framework.
  - **Ant Design Vue**:An enterprise-level UI component library.
  - **TypeScript**:Static type checking.
  - **Vite**:A fast build tool.

- **App**:
  - **Vue3**: A progressive JavaScript framework for building user interfaces.
  - **Vite**: A fast frontend build tool that supports hot reloading.
  - **Pinia**: A state management library for Vue3 that provides a rich set of components.
  - **UniApp**: A cross-platform application development framework that supports multi-terminal development.
  - **uView-plus**: A Vue3-based UI component library that provides a rich set of components.

- **Authentication**:OAuth2 using hashed passwords and JWT Bearer tokens.
- **Authorization Architecture**:Designed based on RBAC, supporting dynamic permission menus, button-level permission control, and data-level permission control.
- **Ready-to-use**:Suitable as a starting template for new projects, also useful for learning and reference.

If you find the project helpful, please give it a star!

## 🍻 Project Features

- Modular and loosely coupled
- Rich modules, ready-to-use
- Simple and easy to integrate
- Comprehensive documentation, easy to maintain
- Top-down, systematic design
- Unified framework, unified components, reducing selection costs
- Development standards, design patterns, code layering models
- Powerful and convenient development toolchain
- Complete local internationalization support
- Designed for team and enterprise use

## 📌 Built-in Modules

- **Dashboard**: Dashboard display, entry point for common features.

- **System Management**
  - **Menu Management**:Configures system menus, operation permissions, and button permission identifiers.
  - **Department Management**:Configures the organizational structure of the system, supports data permissions in tree structures.
  - **Position Management**:Manages user positions.
  - **Role Management**:Manages role menus and permission allocation, sets menu permissions for roles.
  - **User Management**:Maintains and manages system users, including regular information maintenance and account settings.
  - **Log Management**:Uniformly maintains commonly used and relatively fixed data in the system.
  - **Config Management**:Maintains system configuration information, such as system parameters and system settings.
  - **Notice Management**:Manages system notifications, such as system messages and system announcements.
  - **Dict Management**:Manages system dictionaries, such as system parameters and system settings.
  - **Job Management**:Manages system jobs, such as system messages and system announcements.

- **Monitoring Management**
  - **Online Users**:Views currently online users in the system.
  - **Server Monitoring**:Views the system's runtime status, including memory, CPU, disk, etc.
  - **Cache Monitoring**:Views system cache information, such as cache hit rate and cache keys.

- **Common Management**
  - **API Management**:Maintains system APIs, such as API addresses and request methods.
  - **Documentation Management**:Maintains system API documentation, supports online API calls.

- **App**
  - **home**：Application home page.
  - **work**：Application work page.
  - **me**：Application me page.

## 🍪  Account Information

| Account Type   | Username   | Password  |
| :--------- | :----- | :----- |
| **Admin Account** | admin  | 123456 |
| **Demo Account**   | demo   | 123456 |

## 👷 Installation and Usage

### Version Information

| Type | Technology Stack | Version  |
|----------|------------|------------|
| Backend     | Python     | 3.10       |
| Backend     | FastAPI    | 0.109      |
| Frontend     | Node.js    | >= 20.0（Recommended latest version）|
| Frontend     | npm        | 16.14      |
| Frontend     | Vue3       | 3.3        |
| Database   | MySQL      | 8.0 Recommended latest version|
| Database   | PostgreSQL | 14（Recommended latest version）|
| Database   | MongoDB    | 8.0（Recommended latest version）|
| Middleware   | Redis      | 7.0 Recommended latest version|
| App       | uni-app    | 3.0.0 |
| App       | uview-plus | ^3.3.74 |

### Get the Code

```sh
git clone https://gitee.com/tao__tao/fastapi_vue3_admin.git
```

### Backend

1. Install dependencies

   ```shell
   cd backend
   pip3 install -r requirements.txt

   When running pip install, I encountered the following error: UnicodeDecodeError: 'gbk' codec can't decode byte 0xad in position.
   Solution Link：https://www.cnblogs.com/RexTooru/p/17303318.html
   ```

2. Modify project database configuration
   The `DB_DRIVER` database driver type and the corresponding database configuration information are located in the `app/config/.env.dev (.env.test, .env.prod)` files.

3. Create a database named `fastapi_vue_admin`

4. Initialize database data

   ```shell
   # Run in the root directory of the backend project (backend)
   # This command will automatically generate tables and data in the database
   # If the database has already been initialized, this command can be skipped
   python3 main.py init
   ```

5. Start the backend

   ```shell
   # Run in the root directory of the backend project (backend)
   python3 main.py run

   # After modifying the models, you need to: regenerate migration files and then apply migrations
   # Generate migration
   # python main.py revision "initial migration" --env=dev (default is dev if not specified)
   # Apply migration
   # python main.py upgrade --env=dev (default is dev if not specified)
   ```

### Frontend

1. Install dependencies

   ```shell
   cd frontend
   npm install
   ```

2. Run the frontend

   ```shell
   npm run dev
   ```

3. Build the frontend

   ```shell
   npm run build
   ```

### App

1. Install dependencies

   ```shell
   cd frontend
   npm install
   ```

2. Run the frontend

   ```shell
   npm run dev:h5
   ```

3. Build the frontend

   ```shell
   npm run build
   ```

### Access the Project

- Frontend URL: <http://127.0.0.1:5180>
- Username: `admin` Password: `123456`
- API URL: <http://127.0.0.1:8000/api/v1/docs>

### Docker Deployment

- cd fastapi_vue3_amdin/frontend
- npm run build （Ensure the dist directory exists; otherwise, errors will occur during execution）
- cd fastapi_vue3_amdin
- docker compose up -d
- Notes：
- In the frontend .env.production file, change VITE_API_BASE_URL to the public IP address.
- In the backend .env.prod file, set MYSQL_HOST and REDIS_HOST to private IP addresses.
- Common Issues：
- Backend fails to start: Usually because the initialization script was not executed. The script directory is backend/sql/mysql_xxx.sql. Another possibility is that the MySQL or Redis services are not running and need to be started manually.
- Deployment Order：
- 1. Start MySQL and Redis services
- 2. Execute database initialization scripts.
- 3. Start the backend service.
- 4. Start the frontend service.
- Access URL:Public IP address on port 80; login with username admin and password 123456.

## 🔧 Module Showcase

<table>
    <tr>
        <td><img src="./mkdocs/docs/resources/images/login.png"/>Login</td>
        <td><img src="./mkdocs/docs/resources/images/dashboard.png"/>Dashboard</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/menu.png"/>Menu</td>
        <td><img src="./mkdocs/docs/resources/images/dept.png"/>Department</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/position.png"/>Position</td>
        <td><img src="./mkdocs/docs/resources/images/role.png"/>Role</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/user.png"/>User</td>
        <td><img src="./mkdocs/docs/resources/images/log.png"/>Log</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/config.png"/>Config</td>
        <td><img src="./mkdocs/docs/resources/images/online.png"/>Online</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/service.png"/>Server</td>
        <td><img src="./mkdocs/docs/resources/images/cache.png"/>Cache</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/job.png"/>Task</td>
        <td><img src="./mkdocs/docs/resources/images/docs.png"/>API</td>
   </tr>
        <td><img src="./mkdocs/docs/resources/images/redoc.png"/>Documentation</td>
        <td><img src="./mkdocs/docs/resources/images/info.png"/>Personal</td>
   </tr>
   </tr>
        <td><img src="./mkdocs/docs/resources/images/help.png"/>Help</td>
        <td><img src="./mkdocs/docs/resources/images/dict.png"/>Dict</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/app-login.png"/>app-login</td>
        <td><img src="./mkdocs/docs/resources/images/app-home.png"/>app-home</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/app-work.png"/>app-work</td>
        <td><img src="./mkdocs/docs/resources/images/app-me.png"/>app-me</td>
   </tr>
   <tr>
        <td><img src="./mkdocs/docs/resources/images/app-userinfo.png"/>app-userinfo</td>
   </tr>
</table>

## ✨ Special Thanks

Thank you to the following projects for their contributions and support, which have made this project possible:

- [FastAPI Project](https://fastapi.tiangolo.com/)
- [Vue3 Project](https://v3.cn.vuejs.org/)
- [KInit Project](https://gitee.com/ktianc/kinit)
- [Fastapi-Vue3-Admin Project](https://gitee.com/senqi666/fastapi-vue-admin)
- [Vue-FastAPI-Admin Project](https://gitee.com/mizhexiaoxiao/vue-fastapi-admin)
- [RuoYi-Vue3-FastAPI Project](https://gitee.com/insistence2022/RuoYi-Vue3-FastAPI)
- [APScheduler Project](https://github.com/agronholm/apscheduler)
- [Vite Project](https://github.com/vitejs/vite)
- [UniApp Project](https://github.com/dcloudio/uni-app)
- [uView-plus Project](https://uiadmin.net/uview-plus)

## 🎨 WeChat Group

The QR codes below are personal codes that can be used for technical discussions and to discuss various issues encountered during project usage. I sincerely hope everyone can optimize the project together and actively participate in discussions to support each other!！

### Personal QR Codes

<table>
    <tr>
        <td><img src="./mkdocs/docs/resources/images/微信.jpg"/></td>
        <td><img src="./mkdocs/docs/resources/images/微信群.jpg"/></td>
        <td><img src="./mkdocs/docs/resources/images/wechatPay.jpg"/></td>
    </tr>
</table>
