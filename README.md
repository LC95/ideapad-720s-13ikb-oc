OpenCore引导版 | [Clover引导版](https://github.com/FuckDoctors/ideapad-720s-13IKB)


## OpenCore

配置上跟Clover版差别比较大，主要是下面几点：

- 不使用自定义DSDT，尽量使用SSDT
- 尽可能少的使用更名补丁，OC不推荐的那几个不使用

其他差别稍后补充。

电脑配置，BIOS设置，更多详情信息请参考[OpenCore引导版](https://github.com/FuckDoctors/ideapad-720s-13ikb-oc)。

感谢：

 - [OpenCore](https://github.com/acidanthera/OpenCorePkg)
 - [OC-little](https://github.com/daliansky/OC-little)

## rEFInd

OC引导Windows不成功，干脆使用rEFInd做引导，ACPI无副作用，还可以引导Windows，Clover，OpenCore，为黑苹果做双重引导，降低翻车几率。

为了避免NVMe内容对OC，Clover或系统有影响，rEFInd没使用NVMe。

OC文件夹可以单独引导，最好修改`ShowPicker`为`true`，我用rEFInd引导所以，不使用`ShowPicker`，直接进系统。

自己可以按需配置引导项，修改`themes¥simple¥theme.conf`即可。

忽略了默认扫描的Windows启动项，自己添加了Windows启动项，方便自定义图标。

EFI目录结果：

![EFI](./snapshots/EFI.png)

rEFInd启动效果图（大晚上，而且拍照技术不行。。）：

![rEFInd](./snapshots/rEFInd.jpg)
