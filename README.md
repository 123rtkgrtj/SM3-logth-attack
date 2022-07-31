小组成员：王家鹏

账户名称：123rtkgrtj
 
项目简介：实现SM3的长度扩展攻击

项目名称：SM3-logth-attack

完成人：王家鹏

代码说明：
    ![image](https://user-images.githubusercontent.com/110152761/182007875-c9663d5a-80bc-4846-8829-cccc203a540a.png)
    
    长度扩展攻击的原理如图所示
    
    设消息1为m（1）（在我的代码中为’1234‘）
    
    m（1）的哈希值为h（1）
    
    此时，将SM3的iv值替换为h（1）
    
    通过修改后的SM3函数对消息2（记作m（2），在我的代码中为’5678‘）对m（2）进行哈希得到h（2）
    
    使用最初的SM3函数对m（1）||m（2）进行压缩，得到h（1||2）
    
    比较h（1||2）和h（2），发现两者相等
    
    说明我们可以在不知道m（1）但是知道m（1）的哈希值的情况下，任意选定m2，可以得到m（1）和m（2）级联后的哈希值h（1||2）
    
运行截图：
    
    ![image](https://user-images.githubusercontent.com/110152761/182008153-7579f6d3-129f-495b-bc27-76af34cf94f2.png)
    
    可以发现h（1||2）=h（2），攻击成功
    
    
