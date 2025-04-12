
## 📸 截图
| 主页上传界面 | 文件管理面板 | Telegram 交互 |
|--------------|--------------|---------------|
| ![Upload Page](https://via.placeholder.com/300x200.png?text=Upload+Page) | ![Admin Panel](https://via.placeholder.com/300x200.png?text=Admin+Panel) | ![Telegram Bot](https://via.placeholder.com/300x200.png?text=Telegram+Bot) |

## ✨ 核心特性

- **Telegram 集成**：通过 Telegram 机器人直接上传图片和文件，实时获取直链。
- **双存储选项**：
  - **Telegram 存储**：利用 Telegram 的文件存储功能，简单高效。
  - **Cloudflare R2**：支持大文件存储，享受 Cloudflare 的低延迟和高可靠性。
- **文件管理**：通过网页界面管理上传的文件，支持分类、删除和后缀修改。
- **安全认证**：可选的用户名/密码认证，保护你的文件隐私。
- **二维码分享**：上传后自动生成二维码，方便快速分享。
- **多格式支持**：支持图片、视频、音频和文档等多种文件类型。
- **缓存优化**：内置文件和菜单缓存，提升响应速度。
以下是项目中需要在 Cloudflare 环境中绑定的变量及其说明：

| **变量名**                  | **类型**   | **描述**                                                                 | **默认值/示例**            |
|-----------------------------|------------|--------------------------------------------------------------------------|----------------------------|
| `DATABASE`                 | D1 绑定    | Cloudflare D1 数据库绑定名称，用于存储文件元数据、用户设置和分类信息。   | `cloudsnap-db`             |
| `DOMAIN`                   | 环境变量   | Cloudflare Workers 部署域名，用于生成文件直链和设置 Telegram Webhook。    | `yourdomain.workers.dev`   |
| `TG_BOT_TOKEN`             | 环境变量   | Telegram 机器人 Token，用于与 Telegram API 通信以处理文件上传和交互。    | `123456:ABC-DEF1234ghIkl` |
| `TG_CHAT_ID`               | 环境变量   | 允许使用机器人的 Telegram 用户或群组 ID（逗号分隔），限制访问权限。      | `123456789,-987654321`     |
| `TG_STORAGE_CHAT_ID`       | 环境变量   | 用于存储文件的 Telegram 群组或频道 ID，Telegram 存储模式必需。           | `-100123456789`            |
| `ENABLE_AUTH`              | 环境变量   | 是否启用网页管理界面的用户名/密码认证（`true` 或 `false`）。             | `true`                     |
| `USERNAME`                 | 环境变量   | 管理面板的登录用户名，配合 `ENABLE_AUTH` 使用。                          | `admin`                    |
| `PASSWORD`                 | 环境变量   | 管理面板的登录密码，配合 `ENABLE_AUTH` 使用。                            | `your_secure_password`     |
| `MAX_SIZE_MB`              | 环境变量   | 单个文件的最大大小限制（单位 MB），防止上传过大文件。                    | `20`                       |
| `BUCKET`                   | R2 绑定    | Cloudflare R2 存储桶绑定名称，用于 R2 存储模式（若启用）。               | `cloudsnap-bucket`         |
| `COOKIE`                   | 环境变量   | 网页认证 Cookie 的有效期（单位天），控制登录会话时长。                   | `7`                        |


# star 谢谢您的star
![Star 增长趋势](https://raw.githubusercontent.com/iawooo/StarCharts/refs/heads/main/images/cftc_star_chart.png)
