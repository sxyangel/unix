##Shell Manpage 帮助

Unix命令都有许多可选的和强制性的选项，而忘记这些命令的完整语法是很常见的事情。


因为没有人能记住每个 Unix 命令及其所有选项,所以在 Unix 的最早版本中，用户就可以获得在线帮助。


Unix 版本的帮助文件被称为 Manpage。如果你知道所有命令的名称,但你不知道如何使用它,这时 Manpage 可以在每一步中帮助你。

###语法:

Unix系统工作时，以下是获取 Unix 命令细节的简单指令


    $man command

###举例：

你现在想象任何一个命令并且你需要得到与这个命令对应的帮助。假设你想知道 pwd 命令的用法,那么你只需要使用以下命令:

    $man pwd

上面的命令将打开一个帮助，它会给你提供关于 pwd 命令的完整的信息。自己试试根据你的命令提示符来获得更多的细节。


使用以下命令，你可以获得更详细的关于 man 命令的细节:

    $man man

###Man Page 选项:

Man Page通常被划分为不同的部分，而且由于不同 Man page 作者的偏好不同，划分情况也不一样。下面是一些常见的部分:

<table>
   <tr>
  <td><strong>部分<td><strong>描述</td>
</tr>
<tr>
<td>名称<td>命令的名字
<tr>
<td>描述<td>一般描述命令和他的作用</td>
<tr>
<td>摘要<td>一般命令所使用的参数</td>
<tr>
<td>选项<td>描述命令的所有参数和选项</td>
<tr>
<td>另请参阅<td>列出其他的在 Manpage 中与该命令直接相关的命令或功能相似的命令</td>
<tr>
<td>漏洞<td>描述存在于命令或输出中的问题或错误</td>
<tr>
<td>例子<td>常见的用法示例,让读者了解如何使用命令。</td>
<tr>
<td>作者<td>Manpage 或其他命令的作者。</td>
<tr>
</table>
所以最后,我想说，当你需要使用 Unix 命令或它的系统文件信息时， Man page 是一个至关重要的资源。

###有用的Shell命令:

下面的链接中给出了最重要和频繁使用 Unix Shell命令列表。


如果你不知道如何使用命令，可以使用 Man page 获得命令的完整细节。


这里是 [Unix Shell -有用的命令列表](http://www.tutorialspoint.com/unix/unix-useful-commands.htm)
