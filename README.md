# WaxPatch_X64
在waxPath(https://github.com/mmin18/WaxPatch) 的基础上，创建一个demo，并试着修改了64bit的问题；

参考https://github.com/felipejfc/wax_x86-64 进一步修复，支持回调使用

arm64设备crash问题已修复

arm64设备 delegate crash问题已修复



======================使wax框架真正兼容64位系统==========================

苹果强制要求所有新提交的应用必须兼容64位，但原来使用lua的框架wax是不支持64位的。为此，在github上一番搜索，发现两个兼容64位的wax的分支。如下：

https://github.com/felipejfc/wax_x86-64    此分支中的例子程序丰富。

https://github.com/maxfong/WaxPatch_X64   对上述64位进行了优化，建议使用此框架

Tips：使用wax框架中json解析的同学看过来，如果没用到的，可以不看。

https://github.com/maxfong/WaxPatch_X64地址中的..../extensions/json 文件在被调用时总是无法正确解析。解决方案是，下载一个32位的wax框架（https://github.com/probablycorey/wax/），然后使用其中的json文件夹替换64框架中的json文件夹，即可。

至此，wax框架可以支持64位了。



======================苹果没有强制兼容64位之前的策略==========================

设置如下参数：

Standard architectures(armv7,armv7s)    

$(ARCHS_STANDARD_32_BIT)

设置方法如下：

http://blog.csdn.net/remote_roamer/article/details/22100253

 

http://blog.csdn.net/jimjarry/article/details/8000668

 

http://www.360doc.com/content/13/1102/09/2036337_326014723.shtml

 

参考：

Xcode的Architectures、Valid Architectures和Build Active Architecture Only属性(原创) - hikoming
