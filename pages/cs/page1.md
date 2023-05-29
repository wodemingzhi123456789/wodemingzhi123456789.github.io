#博客架构1.0说明


##Index.html



     <!DOCTYPE html> 
     <html> 
     <head>
        
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title> Le Jardin Èternel</title>
        <link rel="stylesheet" type="text/css" href="css/theme.css">

        </head>
     <body>
    
     <!--First section-->
    <div class="hphts">
        <img src="img/headphoto.jpg" >
       

    </div>
    

    
      <nav>
     <div class="topnav">
        <a class="active" href="https://www.yunfuling.xyz" target="_self">主页</a>
        <a href="html/falv.html" target="_blank"> 法律</a>
        <a href="html/cs.html" target="_blank"> 计科</a>
        <a href="html/waiyu.html" target="_blank"> 外语</a>
        <a href="html/reading.html" target="_blank"> 阅读</a>
        <a href="html/writing.html" target="_blank">写作 </a>
        <a href="html/kexue.html" target="_blank"> 科学</a>
        <a href="html/art.html" target="_blank"> 艺术</a>
        <a href="html/learning.html" target="_blank">学习 </a>
        <a href="html/shenghuo.html" target="_blank"> 生活</a>
       

      </div>
    </nav>
      
      
    <main>

      <article class="article">

        <h1>
          2023-5-17更新
        </h1>
        <ul>
          <li> 外语页面:
            <ul>
              <li><a href="html/waiyu.html#article2" target="_blank">The Definition of the Word 'Capitalism'
          </a></li>
          </ul>
          </li>

        </ul>
       


      </article>
   
        
        
    </main>




        <footer class="footer">
           
           <a href="#">点击跳转至顶部 
          </a>
          
            
          </footer>
          
        </body>
  
       </html> 
---
     <meta name="viewport" content="width=device-width, initial-scale=1.0">

比例自动适应设备屏幕

---

        <link rel="stylesheet" type="text/css" href="css/theme.css">
外部链接css ，因为在同级目录文件夹的下面，直接css/xxx.css,如果在上级目录的下面 就需要../css/xxx.css

---

    <div class="hphts">
        <img src="img/headphoto.jpg" >
       </div>
 div是一个区，用class定义类后可以通过css改变这里面的样式，id是单独的唯一的一个，可以链接也可以改变样式。class后是.xxx {}. 如果要选择class里面的小的 就 .xxx xxx {}.Id后是#Xxx。

 


    .topnav {
        overflow: hidden;
        background-color: #e1bdbd;
      }

     .article h1 {
    color: #471fa5;
    font-size:40px;
    text-align:center;
    }


---

制作的导航  index.html 的同级目录，其他html应该是../xxx. Target 就是点击后怎么样，blank新窗口。

     <nav>
     <div class="topnav">
        <a class="active" href="https://www.yunfuling.xyz" target="_self">主页</a>
        <a href="html/falv.html" target="_blank"> 法律</a>
        <a href="html/cs.html" target="_blank"> 计科</a>
        <a href="html/waiyu.html" target="_blank"> 外语</a>
        <a href="html/reading.html" target="_blank"> 阅读</a>
        <a href="html/writing.html" target="_blank">写作 </a>
        <a href="html/kexue.html" target="_blank"> 科学</a>
        <a href="html/art.html" target="_blank"> 艺术</a>
        <a href="html/learning.html" target="_blank">学习 </a>
        <a href="html/shenghuo.html" target="_blank"> 生活</a>
       

      </div>
    </nav>

---
多个列表不按顺序，链接到其他页面的id，格式是另外一个.HTML#xxx(id名称)


        <ul>
          <li> 外语页面:
            <ul>
              <li><a href="html/waiyu.html#articles" target="_blank">The Definition of the Word 'Capitalism'
          </a></li>
          </ul>
          </li>

        </ul>
    
---

定义了顶部，链接到顶部
<footer class="footer">
           
           <a href="#">点击跳转至顶部 
          </a>
          
            
          </footer>

---


##other.html


       

最上面格式都一样,main之下开始写文章，给每个文章的h1定义id=articlex,这样就可以在最上面列一个表链接到每一篇文章的H1.每篇文章时的底部插入点击。

     <main>
      <ul id="articles">
        <li>English
          <ul>
            <li>
              <a href="#article2" >The Definition of the Word 'Capitalism'</a>
            </li>
            <li><a href="#article1">Alain Badiou: A Pseudo-Maoist Obscurantist </a></li>
          </ul>
       
       
      </ul>
      
      
      <article class="article">
        <h1 id="article2">
          The Definition of the Word 'Capitalism'
        </h1>

        <pre >
     </pre>
        <a href="#"  position: relative;
        font-size: 13px;
        bottom: 0; 
        width: 100%;>点击跳转至顶部 
        </a>

    
  
  pre元素表示预定义格式文本。在该元素中的文本通常按照原文件中的编排，以等宽字体的形式展现出来，文本中的空白符（比如空格和换行符）都会显示出来。
  

  ##html页面插入markdown


>      <!doctype html>
         <html>
        <head>
    <meta charset="utf-8"/>
    <title>cs-page1</title>
    </head>

    <body>
    <div id="content"></div>

     <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
      <script src="https://cdn.staticfile.org/jquery/1.10.2/jquery.min.js"></script>
     <script>
    $(function(){
        $.ajax({
            type:"get",
            url:"page1.md",
            dataType:"html",
            success:function(res){
               show(res)
            }
        })

        function show(data) {
            document.getElementById('content').innerHTML = marked.parse(data);
        }
    })
     </script>
      </body>
      </html>


markdown文件会转化未HTML然后在div id content  div  之间显示，js里面的 url表示 是解析的markdown的路径。

---

.md文件
        
        # 一级标题
        ## 二级标题
        ##### 五级标题
        ***             表示分割线




