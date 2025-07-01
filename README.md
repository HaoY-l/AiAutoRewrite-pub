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
[![演示视频](https://img.youtube.com/vi/your_video_id/maxresdefault.jpg)](https://www.youtube.com/watch?v=your_video_id)

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

## 🚀 快速开始 | Quick Start
```bash
# 克隆仓库
git clone https://github.com/HaoY-l/AiAutoRewrite.git
cd AiAutoRewrite/backend

# 初始化环境
python -m venv venv && source venv/bin/activate
pip install -r requirements.txt
python create_db.py

# 启动服务
flask run --host 0.0.0.0 --port 5001

# 前端部署
cd ../frontend
npm install
npm run dev
```

## ⚡ 核心API示例
```python
API文档补充ing
```

## 🔧 专家配置
`.env` 配置模板：
```ini
[WeChat]
TOKEN = "your_wechat_token"
APPID = "your_appid"

[AI]
DEEPSEEK_KEY = "sk-xxxxxxxx"
MOONSHOT_KEY = "sk-xxxxxxxx"

[Database]
URI = "sqlite:///articles.db"
```


## 📞 联系我们
**技术支持**：tomorrow_me-    
**问题反馈**：[GitHub Issues](https://github.com/HaoY-l/AiAutoRewrite/issues)      
**贡献者**：欢迎提交 PR 或 Issue，参与项目建设！