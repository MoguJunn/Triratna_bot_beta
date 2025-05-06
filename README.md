# Triratna_bot_beta

一个基于 [NoneBot2](https://nonebot.dev/) 的 QQ 机器人，集成了多种实用插件，支持 OneBot V11 协议。

## 环境要求

- Python 3.9（必要！ 版本过高插件可能不兼容）
- pip
- 推荐使用虚拟环境

## 安装与启动

1. **克隆仓库**
   ```sh
   git clone 当前仓库
   cd Triratna_bot_beta
   ```

2. **创建虚拟环境并激活**
   ```sh
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # Linux/Mac
   source venv/bin/activate
   ```

3. **安装依赖**
   ```sh
   pip install -r requirements.txt
   ```

4. **生成项目（如首次运行）**
   ```sh
   nb create
   ```

5. **安装插件**
   ```sh
   nb plugin install
   ```

6. **配置环境变量**

   编辑 [.env](.env) 文件，参考如下示例：

   ```
   MAIMAIDXPATH=D:\Learning\QQbot\static
   MAIMAIDXTOKEN=your_token
   SUPERUSERS=["你的QQ号"]
   COMMAND_START=["/", ""]
   COMMAND_SEP=[".", " "]
   NICKNAME=["净饭"]
   IS_OVERSEA=False
   RESOLVER_PROXY = "http://127.0.0.1:7897"
   LOCALSTORE_USE_CWD=True
   reminder_expire_time=15
   ```

7. **运行机器人**
   ```sh
   nb run
   ```

## 已集成插件

- nonebot_plugin_maimaidx
- nonebot_plugin_status
- nonebot_plugin_arkgacha
- nonebot_plugin_alconna
- nonebot_plugin_pjsk_helper
- nonebot_plugin_p5generator
- nonebot_plugin_batitle
- nonebot_plugin_make_choice

插件配置可在 [pyproject.toml](pyproject.toml) 的 `[tool.nonebot]` 部分查看和修改。

## 目录结构说明

- `cache/`：缓存数据
- `data/`：插件数据与资源
- `.env`：环境变量配置
- `pyproject.toml`：项目配置
- `README.md`：项目说明

## 文档与支持

- [NoneBot2 官方文档](https://nonebot.dev/)
- 插件文档请参考各插件仓库

## 常见问题

- **依赖安装失败**：请确认 Python 版本与 pip 已正确安装。
- **插件不可用**：请检查 `.env` 和 `pyproject.toml` 配置是否正确。
- **连接失败**：请确认 OneBot 适配器和 QQ 机器人端已正确运行。

如有其他问题欢迎提 Issue 或联系维护者。
