  
<html>   
<head>  
	<title>简易图片处理</title> 
    <style type="text/css"> 
		#header
		{
	
			height:50px;
			font-size:25px;
			text-align:center;
			font-family:"宋体";
			background:#00CC66;
		}  
        #main
		{
			width:80%;
			height:100%;
			float:left;
			border:groove;
			margin-left:50px;
			margin-top:50px;
			background-color:#8080C0
		}
		#menu
		{
		margin-top:150px;
			float:left;
		}
		#mycanvas
		{
		margin-top:100px;
		margin-left:50px;
		margin-right:50px;
		}
		#photo
		{
			display:none;
		}                    
		ul   
        {   
          margin: 0;                      
           padding: 0;   
            width: 150px;   
            list-style: none;   
            background-color: Orange;   
            border: 1px solid red;   
        }   
        .lili:hover   
        {   
            padding: 5px;   
           	background-color: #FC756F;   
            border-left-color: #51A9F3;   
            border-right-color: #51A9F3;   
            border-left-width: medium;   
            border-right-width: medium;   
            font-weight: bolder;   
            color: White;   
        }   
        .lili   
        {   
            padding-top: 5px;   
            height: 25px;   
            border-top: solid 2px Orange;   
            border-bottom: solid 2px Orange;   
            color: black;   
            background-color: White;   
        }   
        span   
        {   
            font-weight: bolder;   
            color: black;    
        }   
        span:hover   
        {   
            color: White;   
            font-size: large;   
        }   
       .lititle a   
       {   
            font-size: larger;   
            font-weight: 900;   
            color: White;   
        }   
     
        .lititle:hover   
        {   
            cursor: pointer;   
        }  
		.lili a
		{
			cursor:pointer; 
		}	
        .ggtitle   
        {   
            border-top: 1px solid red;         
		}
		  
    </style>   
    <script type="text/javascript" src="jquery-2.2.3.min.js"></script>   
    <script type="text/javascript">   
       
        $(function () {   
            $(".tztitle").click(function () {   
                $(".tz").fadeToggle(500);   
            });   
    
            $(".ggtitle").click(function () {   
                $(".gg").fadeToggle(500);   
            });   
        });   
        function onloadimg()   
{                                         
		var input=document.getElementById('photo');  
		input.click(); 
   	 	var c=document.getElementById("mycanvas");   
   		 var cxt=c.getContext("2d");   
   		 var img=new Image()
		 var hum=document.getElementById('photo');  
		 var src=URL.createObjectURL(hum);
		 img.src=src;
    	 cxt.drawImage(img,0,0);   
}   

    </script>   
</head>   
<body bgcolor="#EFEFEF">  
	<div id="header">
	<h1>简易图片处理</h1>
	</div> 
    <div id="menu"">   
        <ul class="ulul">   
            <li class="lititle tztitle"><a id="aaa">基础操作</a></li>   
            <li class="lili tz"><a style="padding-left: 20px;" onClick="onloadimg()"><span>打开</span></a></li> 
            <li class="lili tz"><a style="padding-left: 20px;" href=""><span>保存</span></a></li>   
            <li class="lili tz"><a style="padding-left: 20px;" href=""><span>缩放</span></a></li>   
            <li class="lili tz"><a style="padding-left: 20px;" href=""><span>裁剪</span></a></li>   
            <li class="lili tz"><a style="padding-left: 20px;" href=""><span>撤销</span></a></li>   
            <li class="lili tz"><a style="padding-left: 20px;" href=""><span>拼接多张图片</span></a></li>   
            <li class="lititle ggtitle"><a>复杂操作</a></li>   
            <li class="lili gg"><a style="padding-left: 20px;" href=""><span>橡皮擦</span></a></li>   
            <li class="lili gg"><a style="padding-left: 20px;" href=""><span>输入文字</span></a></li>   
            <li class="lili gg"><a style="padding-left: 20px;" href=""><span>加边框</span></a></li>   
            <li class="lili gg"><a style="padding-left: 20px;" href=""><span>调节拼接关系</span></a></li>   
        </ul>   
    </div> 
	<div id="main">
		<canvas id="mycanvas">您的浏览器暂不支持canvas，请更换Firefox，Chrome</canvas>
	</div>  
	<input id="photo" type="file"></input>    
</body>   
</html>  
