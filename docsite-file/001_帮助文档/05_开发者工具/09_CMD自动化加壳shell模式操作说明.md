
###  **CMD自动化加壳shell模式操作说明**
1.	登录系统以后，在左侧导航栏的“开发者工具”中单击“task模板文件设置”，即可进入“task模板文件设置”的页面，如下图右侧上方所示；
<div style="text-align:center">
<img data-src="shell1.png" width="700px"></img>
</div>
2.	在“选择taskName”输入框中输入需要封装的task的名称(如“TestSamtools”);
3.	选中“调试模式”即可进入通过编写shell命令的方式进行task封装的模式。如上图右侧下方所示；
4.	在“task模板文件设置”页面的左侧，“script结构”标签中，勾选中需要添加shell命令的阶段（Prepare、Run、Summary），点击“新增文件”，即可出现一个对话框，如下图所示：
<div style="text-align:center">
<img data-src="shell2.png" width="700px"></img>
</div>
分别填写，shell文件的名称、运行该命令所在的container的资源（包括，CPU数，以及内存，内存以MB为单位）以及带解析的命令，如下图所示：
 <div style="text-align:center">
<img data-src="shell3.png" width="700px"></img>
</div>

5.	点击“完成”以后，会有“保存完成”的提示，表示已经成功保存，如下图所示：
 <div style="text-align:center">
<img data-src="shell4.png" width="700px"></img>
</div>
6.	然后点击弹出框右侧上方的关闭按钮，关掉对话框，即可。
