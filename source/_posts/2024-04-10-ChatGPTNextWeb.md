---
title: ChatGPTNextWeb
date: 2024-04-10 22:14:48
tags: chatgpt
---
# ChatGPT

目前利用chatgpt其实可以解决很多现实中的问题，比如说前一段时间帮我表姐写了一个简单的说明书网页显示，自己搞定了前端的页面（preview/login/admin page),配合eggjs的后端渲染能力轻松搞定增删改查，阿里云的部署，ICP备案一条龙服务，虽然是个很小的项目，大项目该走的流程也都走了一遍。
话具体的说来gpt的帮助远比我想象中的好一些，英文的答案也比想象中更加的充分一些，目前国内的访问途径基本就如下几种
- 付费openai（direct/indirect）
- 国产平替

目前github也有一些大模型的统一界面比如什么chatall什么的，今天我看了一眼[chatGPT-NextWeb](https://github.com/ChatGPTNextWeb/ChatGPT-Next-Web)， 目前支持azure/openai/google，其他的一些软件可能支持的全一些。
巧的是我通过公司的邮箱地址成功申请下来了azure的openai服务，填了url和azure-api-key就可以直接访问了，提问了十几次，预算是CNY0.17，在gpt-3.5-turbo的下面也算是国内访问最便捷的方式了，缺点就是目前该项目只支持端侧和网页，不支持移动端，不过好消息是比较稳定目前。
GPT-4其实也可以在申请配额（quota increase）不过相对于几乎0.2元一次的价格（几乎），还是有一点肉疼，不过先尽量发挥3.5的潜力，毕竟有他的帮助，感觉还是很轻松。

另外提一嘴，azure的付费模式和阿里云完全不同，接口走的是先用后付，openai会挂载在subscription的下面，然后使用绑定信用卡就可以了（好像是要求visa/master，我正好有一张就没有在尝试别的，国内办理也很好办理)