# 可以简单的编译自定义固件，把自己想要的插件集成到固件中。可以自定义固件安装包空间大小。


  ## 使用说明
  
- 单击 [Use this template](https://github.com/noviachen/Image-Builder/generate)按钮以创建新的存储库。
- 默认情况下，使用 immortalwrt-imagebuilder-23.05-SNAPSHOT-x86-64 构建。要更改它，请修改 `. github/workflow/image-builder.yml` 中的 `DOWNLOAD_URL`。也可能适用于编译官方 OpenWrt 版本（未经测试）。
- 根据您的设备修改 image-builder. yml 中的 `PROFILE`。
- 根据需要修改 `uci - custom`（第一个引导脚本）和 `packages.list`（添加或删除包）。
- 将其他 ipk 文件上传到 `packages` 文件夹（如果有）。
- 在操作页面上选择 `ImmortalWrt Image Builder`。
- 单击 `Run workflow` 按钮。
- 构建完成后，单击 `Artifacts` 下的文件链接以下载固件。

💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕💕
# 简单使用方法

  1. 简单使用方法，fork项目。
  
  2. 编辑`uci-custom`文件自定义设置。
  
  3. 编辑`packages.list`文件，添加包例如：`luci-app-openclash`， 删除默认包，在包名前输入“-” 例如：`-luci-app-aria2`。
  
  4. 需要添加第三方插件的，把ipk文件以及依赖ipk 上传到packages文件夹里，编辑`packages.list`文件，依赖文件会自动安装。例如添加 `luci-i18n-minidlna-zh-cn`会自动安装 `luci-app-minidlna`
  
  5. 点击GitHub页面上[Action](https://github.com/wpsdoo/Image-Builder/actions)按钮,点击左侧`ImmortalWrt Image Builder`，点击右侧`Run workflow`， 在弹出的imagebuilder_Url_Path 对话框里输入完整的Image-Builder路径，在点击绿色的`Run workflow`按钮开始自动编译。
	
  6. 等待几分钟后在`Action`页面下载编译好的文件。
 
 immortalwrt下载地址：[Project ImmortalWrt](https://downloads.immortalwrt.org/releases/)
 完整的Image-Builder路径：https://downloads.immortalwrt.org/releases/23.05-SNAPSHOT/targets/x86/64/immortalwrt-imagebuilder-23.05-SNAPSHOT-x86-64.Linux-x86_64.tar.xz

## Thanks

- [GitHub Actions](https://github.com/features/actions)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [Project ImmortalWrt](https://github.com/immortalwrt/immortalwrt)

## Reference

[ImmortalWrt Image Builder 使用说明](https://github.com/1715173329/blog/issues/8)

## License

[MIT](https://github.com/noviachen/Image-Builder/blob/main/LICENSE)
