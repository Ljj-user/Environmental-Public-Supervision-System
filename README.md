# 环保公众监督系统
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

## 项目简介
环保公众监督系统是一个致力于环境保护的综合管理平台，通过多角色协同、数据驱动的方式实现环境数据的采集、监督与管理。系统支持网格员数据录入、公众监督反馈及管理员系统管理，旨在构建全民参与的环保监督体系。


## 技术栈
### 后端技术
| 技术/工具 | 说明 | 版本 |
|------------|------------------------------|-------|
| **Spring Boot** | 核心框架，快速构建后端服务 | 2.x |
| **MyBatis-Plus** | ORM 框架，简化数据库操作 | 3.x |
| **MySQL** | 关系型数据库，存储环境数据 | 5.7/8.0 |
| **Maven** | 依赖管理与项目构建工具 | 3.x |
| **Java** | 开发语言 | JDK 8+ |

### 前端技术
| 技术/工具 | 说明 | 版本 |
|------------|------------------------------|-------|
| **Vue.js** | 渐进式 JavaScript 框架 | 2.x |
| **HTML/CSS/JS** | 基础页面开发 | - |
| **Node.js** | Vue 项目运行环境 | LTS |
| **WebStorm/VSCode** | 开发工具 | - |


## 运行环境要求
### 软件依赖
1. **数据库**  
   - MySQL 5.7 或 8.0（需提前创建数据库并配置字符集为 UTF-8）  
   - 可视化工具：Navicat（推荐）或 MySQL Workbench  

2. **后端环境**  
   - JDK 8+（需配置 `JAVA_HOME` 环境变量）  
   - Maven 3.x（需配置 `MAVEN_HOME` 环境变量并添加到 `PATH`）  

3. **前端环境**  
   - Node.js LTS（需包含 npm，安装后通过 `node -v` 和 `npm -v` 验证）  


## 项目结构
```
环保公众监督系统/
├─ backend/                # 后端项目（Spring Boot + MyBatis-Plus）
│  ├─ src/
│  ├─ pom.xml              # Maven 依赖配置
│  └─ application.properties # 数据库连接等配置
├─ frontend/               # 前端项目（Vue.js）
│  ├─ src/
│  ├─ package.json         # Node 依赖配置
│  └─ vue.config.js        # 项目构建配置
├─ doc/                    # 文档目录（数据库设计、接口文档等）
└─ README.md               # 项目说明
```


## 部署步骤
### 1. 后端服务部署
#### 环境准备
- 安装 JDK 8+ 并配置环境变量  
- 安装 Maven 并配置环境变量（需验证 `mvn -v` 输出）  

#### 运行步骤
1. 克隆项目到本地：  
   ```bash
   git clone https://github.com/your-username/环保公众监督系统.git
   ```

2. 进入后端目录，通过 Maven 安装依赖：  
   ```bash
   cd backend
   mvn clean install
   ```

3. 配置数据库连接：  
   修改 `application.properties` 中的数据库地址、用户名和密码：  
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/环保数据库?useUnicode=true&characterEncoding=utf-8&serverTimezone=Asia/Shanghai
   spring.datasource.username=root
   spring.datasource.password=你的数据库密码
   ```

4. 启动后端服务：  
   ```bash
   mvn spring-boot:run
   ```
   服务启动后默认端口为 `8080`。


### 2. 前端项目部署
#### 环境准备
- 安装 Node.js LTS（需包含 npm）  

#### 运行步骤
1. 进入前端目录：  
   ```bash
   cd frontend
   ```

2. 安装依赖：  
   ```bash
   npm install
   ```

3. 配置前端请求地址（指向后端服务）：  
   修改 `src/api/config.js` 中的接口地址：  
   ```javascript
   export const BASE_URL = 'http://localhost:8080/api' // 后端服务地址
   ```

4. 启动前端开发环境：  
   ```bash
   npm run serve
   ```
   前端应用启动后默认访问地址为 `http://localhost:8081`。


## 功能模块
### 角色与权限
| 角色 | 核心功能 |
|------|------------------------------|
| **网格员** | 环境数据采集与录入（文本、图片、定位等） |
| **公众用户** | 环境问题查看、反馈与监督（数据上报、进度跟踪） |
| **管理员** | 系统管理（用户管理、数据审核、统计分析） |

### 核心功能
1. **数据采集**：网格员通过移动端或PC端录入环境数据（如水质、空气质量、污染源等）。  
2. **公众监督**：用户可查看实时环境数据，上报问题并跟踪处理进度。  
3. **数据管理**：管理员对上报数据进行审核、分类与统计分析，生成可视化报表。  
4. **系统配置**：角色权限管理、字典数据维护、系统参数配置等。


## 贡献指南
欢迎参与项目贡献！如需提交代码或反馈问题，请遵循以下流程：  
1.  Fork 本仓库到个人账号  
2.  创建功能分支：`git checkout -b feature/new-function`  
3.  提交代码并推送到远程分支  
4.  发起 Pull Request，描述功能或修复内容  


## 联系方式
如有问题或建议，可通过以下方式联系：  
- 邮箱：2694569918@qq.com
- Issues：[提交问题](https://github.com/Ljj-user/Environmental-Public-Supervision-System/issues/new)

---

**项目状态**：持续开发中  
**许可证**：MIT License  
**更新时间**：2025年6月3日