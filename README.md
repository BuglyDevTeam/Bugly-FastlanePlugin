# Fastlane 插件

## 一. Beta 插件
**[下载插件][1],解压后将ruby文件放到工程的`/fastlane/actions`目录下**
### 1.1 上传插件使用
1. 在 **`/fastlane/Fastfile`** 中添加如下任务，根据 [API说明][2] 配置对应参数：
```fastlane
 	lane :upload do
		upload_app_to_bugly(
      		file_path:"filepath",
      		app_key:"appkey",
      		app_id:"appid",
      		pid:"pid",
      		title:"title",
      		desc:"description",
      		secret:"secret",
      		users:"users",
      		password:"password",
      		download_limit:download_limit
    	)
  	end
  ```

2. 配置好任务后，打开终端,进入工程目录，输入命令
  > fastlane upload

  	上传成功后会在终端提示 **`upload success`** ,否则会提示 **`upload failed,result is {error msg}`**

### 1.2 更新插件使用
1. 在 **`/fastlane/Fastfile`** 中添加如下任务,根据 [API说明][2] 配置对应参数：
  ```fastlane
    lane :update do
    	update_app_to_bugly(
      	file_path:"pathfile",
      	app_key:"appkey",
      	exp_id:"expid",
      	title:"title",
      	desc:"escription",
      	secret:"secret",
      	password:"password",
      	download_limit:download_limit
    	)
  	end
  ```

2. 配置好任务后，打开终端,进入工程目录，输入命令
  > fastlane update

  	更新成功后会在终端提示 **`update success`** ,否则会提示 **`update failed,result is {error msg}`**




[1]:http://softfile.3g.qq.com/myapp/buglysdk/fastlane_plugin.zip
[2]:../apis/beta.md
