# Gepetto-ChatGPT

[JusticeRage/Gepetto](https://github.com/JusticeRage/Gepetto/) 的修改版本

## 特性

- 使用 text-davinci-002-render 模型

  与原项目不同的是 这个脚本使用ChatGPT的"text-davinci-002-render" 模型来进行代码分析
- 减少API费用

  ChatGPT暂时处在beta阶段 不收取费用 原项目使用的davinci-003模型每次API请求会按照Token数量收费 但是ChatGPT在用户高峰期并不稳定
- 增加对对长对话的支持 以分析更长的函数

  ChatGPT的Token数量限制更宽 可以分析更长的函数 返回更多的分析结果

- 分析结果增加中文支持

- 使用selenium来进行认证，代码来自[LanLan69/easyChatGPT](https://github.com/LanLan69/easyChatGPT)

- 由于Windows7不支持python3.9，无法使用`pypasser`，所以加了一个`solve_recaptcha`选项以手动点击验证码

- 增加了一个登录快捷键，防止每次打开ida都会登录chatgpt

- 增加了一个发送代码的快捷键

## 安装

`pip install pypasser`

修改`Gepetto-ChatGPT.py`开头的config，配置账号密码，如果无法安装`pypasser`，可以设置`solve_recaptcha`为`False`来手动过验证

把`Gepetto-ChatGPT.py`和`chatgpt/chatgpt.py`丢进ida plugins文件夹即可

![](demo.png)

## 使用

- Ctrl+Alt+L 打开chrome登录chatgpt

- Ctrl+Alt+S 发送当前反编译的C代码

- Ctrl+Alt+G 要求ChatGPT对代码进行分析解释

- Ctrl+Alt+R 重命名变量