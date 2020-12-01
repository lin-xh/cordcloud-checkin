
## CordCloud 自动签到脚本 ---  Github Action

签到脚本来自coderbean/cordcloud-checkin，加了个action

### 配置
和 py 同级别新建 `config.json` 文件，文件结构如下
```
.
├── README.md
├── checkin.py
├── config.json
├── requirements.txt
└── venv

```
### 配置示例
```json
{
  "domain": "www.cordcloud.uno",
  "msg_prefix": "【CordCloud签到】" 

}
```
### 配置含义
| 属性         | 含义                                             |
| ------------ | ------------------------------------------------ |
| "domain"     | 签到域名，支持 cordcloud |
| "msg_prefix" | tg通知的前缀                                     |

### Secrets添加

|        Serets       |                     取值                         |
| ------------------- | ------------------------------------------------ |
| CORDCLOUD_USERNAME  | 登陆用户邮箱                                     |
| CORDCLOUD_PASSWORD  | 密码                                             |
| BOT_TOKEN           | telegram的bot token                              |
| CHAT_ID             | chat ID                                     |

### 运行 
每天10点自动签到，如果需要其他时间，修改.github/workflows/checkin.yml中的第5行- cron: '0 2 * * *'


