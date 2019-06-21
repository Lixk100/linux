# vim操作
**实验知识点**
- vim中的六种基本模式
- vim的基本操作  
## vim模式（来自维基百科）
vim有六种基本模式和五种派生模式，下面是六种基本模式。  
<html>
    <table style="margin-left: auto; margin-right: auto;">
        <tr>
            <td>
                <!--左侧内容-->
                普通模式 
            </td>
            <td>
                <!--右侧内容-->
                插入模式
            </td>  
            <td>
                <!--左侧内容-->
                可视模式 
            </td>
            <td>
                <!--右侧内容-->
                选择模式
            </td>  
             <td>
                <!--左侧内容-->
                命令行模式 
            </td>
            <td>
                <!--右侧内容-->
                Ex模式
            </td>
        </tr>
    </table>  
</html>
这六种里面我们常用到的也就是普通模式、插入模式和命令行模式  

### 普通模式
vim启动即进入到普通模式，处于插入模式或命令行模式时只需要按ESC键即可进入普通模式。  
普通模式中只需要按i(插入)或a(附加)即可进入插入模式。  
在普通模式中，按：即可进入命令行模式。命令行模式中，输入wq回车后保存并退出vim。
### 进入vim
打开xfce终端，输入   
> $ vim test1.txt

![图](https://github.com/liytgy/linux/blob/master/vim/test1.png)  
直接输入vim也可以打开文件，但不会打开任何文件  
> $ vim  

![图](https://github.com/liytgy/linux/blob/master/vim/vim.png)    
这时进入命令行模式，输入 *e 文件路径* 同样可以打开相应文件    
![图](https://github.com/liytgy/linux/blob/master/vim/e%20test.png)   
当不小心输入vim进入vim后直接i插入信息，最后保存时会发现报错现象    
![图](https://github.com/liytgy/linux/blob/master/vim/e32.png)  
此时，可以重新进入命令行模式，输入*w 文件名*来另存为文件    
![图](https://github.com/liytgy/linux/blob/master/vim/w.png)    
成功界面  
![图](https://github.com/liytgy/linux/blob/master/vim/ok.png)  
### 退出vim  
**命令行界面退出vim**  
- 输入*wq*保存并退出  
- 输入*q!* 强制退出不保存
- 输入*x*保存并退出  
**普通模式下退出vim**  
输入*shift+zz*即可保存并退出了
### 删除文本  
**在普通模式下删除文本**  
|  命令   |            说明            |
| :-----: | :------------------------: |
|    x    |     删除游标所在的字符     |
|    X    |   删除游标所在前一个字符   |
| Delete  |            同x             |
|   dd    |          删除整行          |
|   dw    | 删除一个单词（不适用中文） |
| d$`或`D |         删除至行尾         |
|   d^    |         删除至行首         |
|   dG    |      删除到文档结尾处      |
|   d1G   |        删至文档首部        |
