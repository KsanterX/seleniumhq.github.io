---
title: "编写第一个Selenium脚本"
linkTitle: "第一个脚本"
weight: 8
description: >
    逐步构建一个Selenium脚本的说明
---

当你完成 [Selenium安装]({{< ref "install_library.md" >}}) and
[驱动安装]({{< ref "install_drivers.md" >}}) 后, 便可以开始书写Selenium脚本了.

## 八个基本组成部分

Selenium所做的一切, 
就是发送给浏览器命令,
用以执行某些操作或为信息发送请求.
您将使用Selenium执行的大部分操作,
都是以下基本命令的组合:

### 1. 使用驱动实例开启会话

有关启动会话的更多详细信息, 
请阅读我们关于[打开和关闭浏览器]({{< ref "open_browser.md" >}})的文档

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java#L17" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py#L6" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs#L15" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb#L5" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js#L6" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt#L17" >}}
    {{< /tab >}}
{{< /tabpane >}}

### 2. 在浏览器上执行操作

在本例中, 我们
[导航]({{< ref "/documentation/webdriver/browser/navigation.md" >}}) 
到一个网页. 

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java#L19" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py#L8" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs#L17" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb#L7" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js#L8" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt#L19" >}}
    {{< /tab >}}
{{< /tabpane >}}

### 3. 请求 [浏览器信息]({{< ref "/documentation/webdriver/browser" >}})

您可以请求一系列关于[浏览器的信息]({{< ref "/documentation/webdriver/browser" >}}) , 
包括窗口句柄、浏览器尺寸/位置、cookie、警报等.

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java#L21" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py#L10" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs#L19" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb#L9" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js#L10" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt#L21" >}}
    {{< /tab >}}
{{< /tabpane >}}

### 4. 建立等待策略

将代码与浏览器的当前状态同步
是Selenium面临的最大挑战之一, 
做好它是一个高级主题. 

基本上, 您希望在尝试定位元素之前, 
确保该元素位于页面上, 
并且在尝试与该元素交互之前, 
该元素处于可交互状态.

隐式等待很少是最好的解决方案, 
但在这里最容易演示, 
所以我们将使用它作为占位符. 

阅读更多关于[等待策略]({{< ref "/documentation/webdriver/waits.md" >}})
的信息. 

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java#L24" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py#L13" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs#L22" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb#L12" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js#L12" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt#L24" >}}
    {{< /tab >}}
{{< /tabpane >}}

### 5. 发送命令 [查找元素]({{< ref "/documentation/webdriver/elements" >}})
大多数Selenium会话中的主要命令都与元素相关, 
如果不先[找到元素]({{< ref "/documentation/webdriver/elements" >}}), 
就无法与之交互.

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java#L26-L27" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py#L15-L16" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs#L24-L25" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb#L14-L15" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js#L14-L15" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt#L26-L27" >}}
    {{< /tab >}}
{{< /tabpane >}}

### 6. 操作元素
对于一个元素, 
只有少数几个[操作]({{< ref "/documentation/webdriver/elements/interactions.md" >}})可以执行, 
但您将经常使用它们. 

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java#L29-L30" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py#L18-L19" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs#L27-L28" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb#L17-L18" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js#L17-L18" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt#L29-L30" >}}
    {{< /tab >}}
{{< /tabpane >}}

### 7. 获取元素信息
元素存储了很多[被请求的信息]({{< ref "/documentation/webdriver/elements/information" >}}). 
请注意, 我们需要重新定位搜索框, 
因为自从我们第一次找到它以来, 
DOM已经发生了变化. 

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java#L33" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py#L22" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs#L31" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb#L21" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js#L20" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt#L33" >}}
    {{< /tab >}}
{{< /tabpane >}}

### 8. 结束会话 

这将结束驱动程序进程, 
默认情况下, 该进程也会关闭浏览器. 
无法向此驱动程序实例发送更多命令. 

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java#L36" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py#L25" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs#L34" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb#L24" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js#L23" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt#L36" >}}
    {{< /tab >}}
{{< /tabpane >}}

## 组合所有事情

让我们将这8个部分组合成一个完整的脚本, 
包括需要使用的库:

按照选项卡底部的链接查看代码示例, 
因为它将使用测试运行程序而不是独立文件执行.

{{< tabpane disableCodeBlock=true >}}
    {{< tab header="Java" >}}
        {{< gh-codeblock path="examples/java/src/test/java/dev/selenium/getting_started/FirstScriptTest.java" >}}
    {{< /tab >}}
    {{< tab header="Python" >}}
        {{< gh-codeblock path="examples/python/tests/getting_started/test_first_script.py" >}}
    {{< /tab >}}
    {{< tab header="CSharp" >}}
        {{< gh-codeblock path="examples/dotnet/SeleniumDocs/GettingStarted/FirstScriptTest.cs" >}}
    {{< /tab >}}
    {{< tab header="Ruby" >}}
        {{< gh-codeblock path="examples/ruby/spec/getting_started/first_script_spec.rb" >}}
    {{< /tab >}}
    {{< tab header="JavaScript" >}}
        {{< gh-codeblock path="examples/javascript/getting_started/firstScript.js" >}}
    {{< /tab >}}
    {{< tab header="Kotlin" >}}
        {{< gh-codeblock path="examples/kotlin/src/test/kotlin/dev/selenium/getting_started/FirstScriptTest.kt" >}}
    {{< /tab >}}
{{< /tabpane >}}

## 接下来的步骤

利用你所学的知识, 
构建你的Selenium代码. 

当您发现需要更多功能时, 
请阅读我们的[WebDriver文档]({{< ref "/documentation/webdriver/" >}})的其余部分. 
