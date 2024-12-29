# Rainyun_AutoSignIn
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FIcyBlue17%2FRainyun_AutoSignIn.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FIcyBlue17%2FRainyun_AutoSignIn?ref=badge_shield) [![每日签到（tg通知）](https://github.com/IcyBlue17/rainyun_autosignin/actions/workflows/signin-with-tg.yaml/badge.svg)](https://github.com/IcyBlue17/rainyun_autosignin/actions/workflows/signin-with-tg.yaml)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FIcyBlue17%2FRainyun_AutoSignIn.svg?type=shield&issueType=security)](https://app.fossa.com/projects/git%2Bgithub.com%2FIcyBlue17%2FRainyun_AutoSignIn?ref=badge_shield&issueType=security)

自动签到脚本for雨云 ，提供shell文件/Github Action两种方式，提供带Telegram通知/不带Telegram通知的两个版本。  

并且增加了一个一键完成积分任务的功能。后期会完善成一个使用Github调用雨云api实现很多功能的项目。  


## 运行Shell文件自动签到（不推荐，好久没更新了）

```shell
curl -s https://raw.githubusercontent.com/IcyBlue17/Rainyun_AutoSignIn/main/AutoSignin.sh | sh
```
## 使用Github Action自动签到（推荐）  
1. Fork此仓库
2. 在你自己fork的仓库的Settings - Secrets and variables - Actions - Repository secrets中创建一个名为RAINYUN_API_KEY的Repository secret，值为你获取的雨云apikey。
3. 为这个仓库启用Github Actions。然后运行一次测试。如果返回"未达成条件"，或者"任务成功"为正确配置。此后这个workflow将定时执行。如果返回需要登录，请检查你的api密钥是否填写在了正确的位置，你是否正确填写apikey。 
4. （可选）在Repository secret中新建两个Secret，分别名为TELEGRAM_CHAT_ID和TELEGRAM_BOT_TOKEN。填入你的tgchatid和对应通知机器人的token，保存。运行action时选取带tg通知版本的运行就可以收到通知了。
至于为什么我要分开两个文件 后面会合并的（当我抽风了).
注意⚠️ 你需要先給你創建的bot隨便發點消息機器人才能對你進行消息推送。



## 使用Github Action一键完成积分任务  

同上，运行action时选取"一键完成任务"的action并手动触发一次即可    

## 关于为什么我要写这个项目（个人观点）  
1.雨云的APIKEY可以直接获取到实名信息，不是太放心使用非自部署的服务  
2.Github Action足够稳定而且零成本。  





