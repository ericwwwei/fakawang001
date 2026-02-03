# fakawang001
2026全新个人发卡网 可以上传自己收款码.不需要支付接口

# 免费下载链接：https://zibovip.top/3933.html

<img width="968" height="850" alt="image" src="https://github.com/user-attachments/assets/76cc7754-d07d-47d4-8d1e-045bed0268c4" />
<img width="865" height="713" alt="image" src="https://github.com/user-attachments/assets/82fa52d0-f31c-48a4-a84e-25b5708c341d" />
<img width="718" height="634" alt="image" src="https://github.com/user-attachments/assets/7b46ff10-b702-4e23-a187-96443d6abcfd" />
# 邀请码购买系统搭建教程

## 项目概述
这是一个基于React+TypeScript+Tailwind CSS的邀请码购买系统，包含前台购买页面和后台管理功能，支持商品管理、订单处理、卡密发放和邮件通知等功能。

## 环境准备

### 1. 安装Node.js
项目需要Node.js环境，建议安装LTS版本。

– 访问 [Node.js官网](https://nodejs.org/) 下载并安装
– 验证安装：`node -v` 和 `npm -v` 命令应显示版本号

### 2. 安装pnpm（推荐）
项目使用pnpm作为包管理器，可以通过以下方式安装：

“`bash
npm install -g pnpm
“`

验证安装：`pnpm -v`

## 项目搭建步骤

### 1. 克隆项目代码

“`bash
git clone [项目仓库地址]
cd [项目目录]
“`

### 2. 安装依赖

“`bash
pnpm install
“`

### 3. 启动开发服务器

“`bash
pnpm dev
“`

开发服务器将在 `http://localhost:3000` 启动

### 4. 项目结构说明

“`
├── src/                # 源代码目录
│   ├── components/     # 公共组件
│   ├── contexts/       # React上下文
│   ├── hooks/          # 自定义Hooks
│   │   ├── useConfig.ts # 配置管理和业务逻辑
│   │   └── useTheme.ts  # 主题切换功能
│   ├── lib/            # 工具函数
│   ├── pages/          # 页面组件
│   │   ├── AdminPage.tsx            # 后台管理页面
│   │   ├── Home.tsx                 # 首页
│   │   └── InvitationCodePurchasePage.tsx # 邀请码购买页面
│   ├── App.tsx         # 应用入口组件
│   └── main.tsx        # 程序入口文件
├── index.html          # HTML模板
└── package.json        # 项目配置和依赖
“`

## 核心功能说明

### 前台功能
– 商品展示和选择
– 购买数量调整
– 联系方式填写
– 支付二维码展示
– 卡密查询功能

### 后台功能
– 商品管理（添加、编辑、删除商品和卡密）
– 订单管理（查看、审核、拒绝订单）
– 网站内容配置（文本、价格、收款码等）
– 邮箱服务器配置（用于自动发送卡密）
– 管理员密码修改

## 数据存储说明
项目使用浏览器的LocalStorage进行数据存储，包括：
– 商品信息和卡密
– 订单数据
– 网站配置
– 管理员密码

> 注意：LocalStorage仅在当前浏览器有效，且有存储容量限制。生产环境建议使用后端数据库。

## 构建和部署

### 1. 构建生产版本

“`bash
pnpm build
“`

构建后的文件将生成在 `dist/` 目录中

### 2. 部署方式

#### 静态网站部署
由于项目是纯前端应用，可以部署到任何支持静态网站的托管服务：
– Vercel
– Netlify
– GitHub Pages
– 阿里云OSS
– 腾讯云COS等

#### 自定义服务器部署
也可以部署到自己的服务器上，使用Nginx等Web服务器提供静态文件服务：

“`nginx
server {
    listen 80;
    server_name your-domain.com;
   
    root /path/to/your/project/dist;
    index index.html;
   
    location / {
        try_files $uri $uri/ /index.html;
    }
}
“`

## 默认登录信息
– 后台登录地址：`/admin`
– 默认密码：`admin123`（登录后可修改）

## 开发注意事项

1. 项目使用Tailwind CSS进行样式管理，请遵循相关规范
2. 组件化开发，尽量将功能拆分为可复用的组件
3. 所有数据操作都通过`useConfig` hook进行，保持数据一致性
4. 如需添加新功能，建议先了解现有代码结构和逻辑

## 常见问题解决

### 1. 页面样式错乱
– 检查Tailwind CSS类名是否正确
– 清除浏览器缓存后重试

### 2. 数据不保存
– 确认LocalStorage是否被禁用
– 检查浏览器隐私设置

### 3. 邮件发送失败
– 检查邮箱服务器配置是否正确
– 确认SMTP端口和认证信息
– 注意：某些邮箱需要开启”第三方应用授权”并使用授权码而非密码

## 技术栈
– React 18+
– TypeScript
– Tailwind CSS
– Vite
– React Router
– Sonner (Toast提示)
– Recharts (图表库)

