## CordCloud 自动签到脚本 ---  Github Action
### 配置
和 py 同级别简历 `config.json` 文件，文件结构如下
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
| "domain"     | 签到域名，理论上支持 帕斯喵， 绝对支持 cordcloud |
| "msg_prefix" | tg通知的前缀                                     |

### Secrets添加

|        Serets       |                     取值                         |
| ------------------- | ------------------------------------------------ |
| CORDCLOUD_USERNAME  | 登陆用户邮箱                                     |
| CORDCLOUD_PASSWORD  | 密码                                             |
| BOT_TOKEN           | telegram的bot token                              |
| CHAT_ID             | chat ID                                     |

### 运行 
执行 py 文件即可

### tips
定时任务配置执行该脚本定时签到
