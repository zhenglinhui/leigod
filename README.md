# [LeiGod_Acc auto pause script](https://github.com/zhenglinhui/leigod)
适用于青龙面板的雷神加速器自动暂停脚本

**背景**

由于各种原因忘记暂停加速器,浪费你的时间(~~money~~)，由于官方未出短信等提醒功能，所以自己动手操作。

**如何使用**

1. 青龙面板->依赖管理->添加依赖 类型为nodejs 输入名称`js-md5`

2. 拉取仓库jio本
    ```
    #进入容器
    docker exec -it qinglong /bin/bash
    #拉取仓库脚本
    ql repo https://github.com/zhenglinhui/leigod.git "leigod_"
    ```
3. 在青龙面板中添加环境变量，名称为`LEISHEN_USER`, 值的默认格式为`username=&password=`

4. 配置项说明(青龙面板中添加环境变量)
   - `LEISHEN_USER`：账号密码 示例`username=xxx&password=xxx`
   - `LEISHEN_REPEAT_NOTIFY`：是否开启重复暂停通知，默认为`true`，即不管当前账号是否已经在任务执行前暂停，开启后即每次执行任务都会通知。将其设置为`false`则只有在当前账号未暂停时，首次暂停才会通知


**相关项目**

[青龙面板](https://github.com/whyour/qinglong)：支持python3、javaScript、shell、typescript 的定时任务管理面板

[LeishenAuto](https://github.com/himcs/LeishenAuto)：雷神加速器 自动暂停API
