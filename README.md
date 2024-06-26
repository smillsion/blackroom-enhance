# blackroom
chatgpt-on-wechat plugins

**本项目fork自：[blackroom](https://github.com/dividduang/blackroom)，自己增加的拓展，如果不需要白名单模式，不需要切换到本插件。**

## 更新
* 2024-4-16： 
  * 增加动态切换type模式，查看帮助:***bot $blackroom help***，注意：切换type会清空黑名单和白名单
  ```
    # 获取当前type:
    bot $blackroom type get
    # 修改type:
    bot $blackroom type balck or bot $blackroom type white
  ```
  <img  src="./docs/images/screen6.png">
  <img  src="./docs/images/screen7.png">
* 2024-4-15： 
  * 增加白名单模式,type修改为white即可切换白名单模式
  * 修改配置文件读取方式，先从全局配置文件读取，如果读取不到插件配置，再从当前插件目录获取配置<br/>docker可以在映射出来的config.json增加以下配置内容，参考：[官方文档](https://github.com/zhayujie/chatgpt-on-wechat?tab=readme-ov-file#3-%E6%8F%92%E4%BB%B6%E4%BD%BF%E7%94%A8)
  ```
   "blackroom":{
        "type": "black",
        "incantation" : ["封印","该用户已经封印","封印成功"],
        "amnesty" : ["解封","封印中，好好反省","解封成功","该用户没有被封印"],
        "patronus" : ["赐予能力","该用户已获得过能力","赐予能力成功"],
        "ban" : ["收回能力","你未获得能力","收回能力成功","该用户没有获得能力"]
    }
  ```
  
## config.json格式：
``` json
{
  "type": "black",
  "incantation" : ["封印","该用户已经封印","封印成功"],   
  "amnesty" : ["解封","封印中，好好反省","解封成功","该用户没有被封印"],   
  "patronus" : ["赐予能力","该用户已获得过能力","赐予能力成功"],
  "ban" : ["收回能力","你未获得能力","收回能力成功","该用户没有获得能力"],
  "admin_nickname" : []
}
```

