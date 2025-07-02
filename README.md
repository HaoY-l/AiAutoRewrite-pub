# AiAutoRewrite 智能内容创作平台
  [![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)  
  [![GitHub Stars](https://img.shields.io/github/stars/lxy/ai-auto-rewrite?style=social)](https://github.com/lxy/ai-auto-rewrite/stargazers)  
  [![Last Commit](https://img.shields.io/github/last-commit/lxy/ai-auto-rewrite)](https://github.com/lxy/ai-auto-rewrite/commits)

---

## 🌟 平台简介  
**告别繁琐，开启智能创作新时代！**
是否还在为撰写内容而绞尽脑汁？是否还在为微信公众号的排版而抓耳挠腮？是否还在为繁琐的发布流程而心烦意乱？别担心，有了 **AiAutoRewrite 系统**，这些烦恼都将一扫而空！
只需提供一句话、一个主题、一段内容，甚至是链接（后续开发），AiAutoRewrite 系统就能为你生成精美排版的微信公众号文章。无论是插入图片、设置封面，还是其他复杂的排版需求，都能轻松搞定，让你一键发布到微信，省心又省力。   
**AiAutoRewrite 系统：智能创作的得力助手**
AiAutoRewrite 系统是一个强大的智能内容创作平台，它汇聚了多 AI 平台的协同创作能力，能够实现内容的高效生成、智能格式转换以及多渠道发布。无论是内容创作新手，还是忙碌的运营人员，都能通过这个系统获得稳定、可靠的内容创作体验，让创作变得轻松又高效。      
**PS：该系统主要实现微信公众号的对接，包括微信公众号草稿、素材、正文等管理。后续会添加各主流内容创作平台。**



## 演示视频🥸
[![演示视频](https://www.bilibili.com/video/BV1gCgQz3Edr/?vd_source=cff7fcd848c6edafc7ece1f24cea2db5)

## 🚀 功能亮点
### 核心价值
- **多 AI 协同创作**：智能路由 DeepSeek/豆包/Kimi 模型，根据不同需求选择最优 AI 引擎，提升内容质量和创作效率。（开发ing）
- **全渠道发布**：支持微信公众号即时内容同步，实现内容的快速传播和广泛覆盖。
- **智能格式转换**：提供 Markdown/HTML/TEXT 双向精准转换功能，满足不同场景下的内容格式需求。


## 🛠️ 技术栈 | Tech Stack
**后端核心**  
![Flask](https://img.shields.io/badge/Flask-2.3.2-44CC11?logo=flask)  
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-2.0-29BEB0?logo=sqlalchemy)  
![APScheduler](https://img.shields.io/badge/APScheduler-3.10-01A9F7)

**AI集成**  
![DeepSeek](https://img.shields.io/badge/DeepSeek-API-7D3C98)  
![Moonshot](https://img.shields.io/badge/Moonshot-Kimi-FF6F61)
![豆包](https://img.shields.io/badge/豆包-API-FFD700)

**前端生态**  
![Vite](https://img.shields.io/badge/Vite-4.4-646CFF?logo=vite)

## 🚀 快速开始 | Quick Start(脚本一键部署)
```bash
#!/bin/bash

set -e  # 一旦出错就退出

echo "=============================="
echo "🚀 开始自动部署流程..."
echo "=============================="


# === 2. 构建前端 ===
echo "=============================="
echo "🔨 开始构建前端..."
echo "=============================="

cd frontend
npm install
npm run build
cd ..

# === 3. 拷贝前端静态资源到后端 ===
echo "=============================="
echo "📂 拷贝前端静态资源到后端 static..."
echo "=============================="

rm -rf backend/static/*
cp -r frontend/dist/* backend/static/

# === 4. 启动/重启后端 Flask 服务 ===
echo "=============================="
echo "🔄 重启后端 Flask 服务..."
echo "=============================="

# 检查 Flask 服务是否已运行 (假设运行在5000端口)
PID=$(lsof -ti tcp:5001)
if [ -n "$PID" ]; then
  echo "杀掉进程 $PID"
  kill -9 $PID
else
  echo "端口 5001 没有占用"
fi

# 启动 Flask 服务 (根据你需要选一个)
cd backend
rm -rf venv
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple
# 用 gunicorn：
nohup gunicorn app:app --bind 0.0.0.0:5001 --workers 4 > backend.log 2>&1 &

cd ..
echo "✅ 部署完成！后端服务已启动，端口: 5001"
echo "=============================="
```

## ⚡ 核心API示例
```python
API文档补充ing
```

## 🔧 变量配置
`.env` 配置模板：
```ini
ai_model=AI模型名称如：doubao-1.5-lite-32k-250115
api_key=AI接口密钥如：a6962abXXXXXXdd8f8da5
channel_type=AI渠道类型如：doubao
rewrite_article_prompt='请将以下文章进行改写，要求内容不变，字数不变，语句通顺，符合中文语法规范。'
wx_appid=微信小程序appid如：wxcXXXXXXXfe4
wx_secret=微信小程序secret如：3e16xxxxxxxxx7dfd5
```


## 📞 联系我们
**技术支持**：tomorrow_me-       