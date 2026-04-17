# Xuqi LLM Chat

一个基于 `FastAPI + WebUI` 的本地 AI 伴侣聊天项目，支持多存档、角色卡、世界书、记忆库和可扩展的聊天 UI。

Made by `Frischar`.

## 功能概览

- 欢迎页、聊天页、配置页分离
- 三槽位独立存档
- 角色卡导入、编辑、导出
- 世界书词条触发与管理
- 记忆库管理与对话总结
- 可切换主题、背景图和透明度
- OpenAI 兼容聊天接口
- 流式输出与桌面启动器

## 页面入口

- `/` 欢迎页
- `/chat` 聊天页
- `/config` 配置页
- `/config/card` 角色卡页
- `/config/memory` 记忆库页
- `/config/sprite` 立绘页
- `/config/worldbook` 世界书设置页
- `/config/worldbook/entries` 世界书词条页

## 快速启动

### 方式一：双击脚本

直接运行：

`启动webui.bat`

脚本会自动：
- 检测 Python 是否安装
- 检测 Python 版本是否至少为 3.10
- 首次运行时创建虚拟环境
- 安装依赖
- 启动本地 WebUI

### 方式二：命令行启动

```powershell
cd "E:\AI chat 项目\xuqi_llm聊天"
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
uvicorn app:app --reload --host 127.0.0.1 --port 8000
```

然后访问：

`http://127.0.0.1:8000`

## 目录结构

```text
.
|-- app.py
|-- launcher.py
|-- requirements.txt
|-- README.md
|-- 启动webui.bat
|-- data/
|-- cards/
|-- templates/
`-- static/
```

## 存档机制

默认提供三个存档槽位：
- `slot_1`
- `slot_2`
- `slot_3`

每个槽位独立保存：
- 人设
- 配置
- 聊天记录
- 记忆库
- 世界书
- 当前角色卡
- 对应立绘目录

## 公开仓库说明

这个公开副本已经清理了：
- 个人 API Key / 本地配置
- 聊天记录
- 个人背景图和上传资源
- 浏览器缓存目录
- 测试角色卡与临时文件

保留的内容是可直接二次开发和重新配置的模板态工程。