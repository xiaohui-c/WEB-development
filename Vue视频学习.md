# Vue视频学习

### 第一天

##### 第一节课：

1. MVC模式(原生)   MVVM模式(Vue);

   ```html
   <!DOCTYPE HTML>
   <html>
       <head>
           <link rel="Vue.js"/>
       </head>
       <body>
           <div id="app"><!--这一部分内容是VIEW区域，即V-->
               <p>{{value}}</p>
           </div>
           <script>
               let app=new Vue({//id选择器app和链接Vue.js文件框架的就是VM
                   el:"#app",
                   data:{//这一部分内容是Model，即M
                       value:"Hello world!"
   					}
               })
           </script>
       </body>
   </html>
</!doctype>
   ```
   
   
   
   
   
   
   
2. 主要的作用特征就是为我们解决了频繁获取DOM对象，Vue建构了一个虚拟DOM对象，从而达到一次性，快速的去操作DOM对象；

##### 第二节课：

1：我们可以把Vue的方法看作是在html标签里面嵌入了JS代码段，只不过这一个代码段是一个标记；而在Vue里边就来对上述标记进行添加内容状态，或者是方法；
2：在我们使用Vue的时候，其实部署在html的源代码就是原来的标记,比如{{value}}，只是Vue把它所指向的内容渲染在了页面上而已；
3：在使用标记v-if/v-else-if/v-else，语句之前不能有其他无关语句，否则会报错；
4：使用v-if的时候，它所指向的代码如果是false，就会直接移除，v-show只是把显示内容设置为dispaly:none，这样做的好处就是避免了反复调用空间，浪费资源；



### 第二天

1：我们在使用Vue事件的时候，使用方法：在html的标签中@click="方法名字"，定义好了之后我们接着就要在script里边写入methods:{方法名字：()=>{点击之后要做的事情}}；

2：Vue中使用循环的方法：在html的标签中v-for="item（每一个元素）,index（每一个元素对应的下标） in 要遍历的对象名字（数组，对象等）"