## 哪里不会点哪里，so easy    

### ctrl + shift + i 打开dev tool  

**点击`选择`箭头**  

![image](https://github.com/user-attachments/assets/8f61b01d-f507-45e5-b96e-eaf63410b580)  

**然后在cherry上点击想要修改的地方**   

在样式中查看属性  

![image](https://github.com/user-attachments/assets/42aeed4f-6528-4438-8b6f-3db714461f3e)  

**在css中修改即可**  

## 示例  

### 修改头像背景  

我的头像是黑白，在深色模式下啥也看不见   

![image](https://github.com/user-attachments/assets/ba4c0262-e66f-4fd0-ac1d-7f242940293c)  

- 使用dev tool查看样式
  
  ![image](https://github.com/user-attachments/assets/57fd5609-cdf9-4c5a-b15c-e2f1a4f1dbc3)
  
  右边红框里`.ant-avatar >img`是控制头像的css，
  
  怎么来的？在右边的元素里
  
  ![image](https://github.com/user-attachments/assets/c9ab5d34-cab1-4c59-a230-344972b0215c)
  
  `.`代表class，因此是`.ant-avatar`，img是子元素？直接使用空格就可以，`.ant-avatar >img`就是`.ant-avatar img`
  
  重要！！整个元素里可能有很多`.ant-avatar img`，为了避免出现意外，或者其他乱七八糟的，我们再往上加一级（也可以搜索一下，这里不说了）
  
  ![image](https://github.com/user-attachments/assets/2d5a8bbc-adfc-411e-95c6-26c47322e6ae)

  再加上`id="app-sidebar"`，id用#表示，即`#app-sidebar .ant-avatar img`
  
  
- 修改css
  
  在CSS中添加下面的内容
  
  ```CSS
   #app-sidebar .ant-avatar img {  
     background:  #F5F4ED; /* 使用浅色模式的背景色 */  
   }  
    
  ```

#### 搞定

![image](https://github.com/user-attachments/assets/12da4d04-3f93-42e7-ba7f-985ff7ea85d5)  


### 删除开始新对话

![image](https://github.com/user-attachments/assets/e6925daf-54f0-4a3a-a195-1a5ce751d460)

原理同上，选择开始新对话，直接修改  

![image](https://github.com/user-attachments/assets/85a6317d-482c-4424-b02c-40efb3293afa)

```CSS
.kwIEiN {  
  display: none;  
}  
```

  
