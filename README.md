# jisuanqi
This is a 计算器
#案例演示[演示效果](http://wangyuting-v.github.io/jisuanqi/)
#用法
##step1 html格式
~~~
<div class="computer">
	 	<div class="showbox">
	 		<input type="text" id="show"/>
	 	</div>
	 	<div class="butns">
	 		<input type="button" value="c" id="move"/>
	 		<input type="button" value="←" id="back"/>
	 		<input type="button" value="/" id="min"/>
	 		<input type="button" value="*" id="max"/>
	 		<input type="button" value="7" id="n7"/>
	 		<input type="button" value="8" id="n8"/>
	 		<input type="button" value="9" id="n9"/>
	 		<input type="button" value="+" id="add"/>
	 		<input type="button" value="4" id="n4"/>
	 		<input type="button" value="5" id="n5"/>
	 		<input type="button" value="6" id="n6"/>
	 		<input type="button" value="-" id="reduce"/>
	 		<input type="button" value="1" id="n1"/>
	 		<input type="button" value="2" id="n2"/>
	 		<input type="button" value="3" id="n3"/>
	 		<input type="button" value="=" id="equal"/>
	 		<input type="button" value="." id="dot"/>
	 		<input type="button" value="0" id="zero"/>
	 	</div>
	 </div>
~~~
##Step2 CSS格式
~~~
*{margin: 0;padding: 0;box-sizing:border-box;}
			.showbox{height: 30vh;display: flex;width: 100vw;}
			#show{flex: 1;background-color: gainsboro;border: none;font-size: 7vw;padding: 7vw;}
			.butns{width:100vw;display: flex;flex-wrap: wrap;}
			.butns input{height:25vw;width: 25vw;flex: 0 0 25vw;font-size: 7vw;}
			#equal{height: 50vw;background-color: orange;color: #fff;border: none;}
			#equal:hover{background-color: orangered;}
			#zero{margin-top: -25vw;flex:0 0 50vw;}
			#dot{margin-top: -25vw;}
~~~

##Step3 JS格式
~~~
var show=document.getElementById("show")
	 	var n1=document.getElementById("n1")
	 	var n2=document.getElementById("n2")
	 	var n3=document.getElementById("n3")
	 	var n4=document.getElementById("n4")
	 	var n5=document.getElementById("n5")
	 	var n6=document.getElementById("n6")
	 	var n7=document.getElementById("n7")
	 	var n8=document.getElementById("n8")
	 	var n9=document.getElementById("n9")
	 	var zero=document.getElementById("zero")
	 	var dot=document.getElementById("dot")
	 	var move=document.getElementById("move")
	 	var back=document.getElementById("back")
	 	var max=document.getElementById("max")
	 	var min=document.getElementById("min")
	 	var add=document.getElementById("add")
	 	var reduce=document.getElementById("reduce")
	 	var equal=document.getElementById("equal")
	 	n1.onclick=changeIt;
	 	n2.onclick=changeIt;
	 	n3.onclick=changeIt;
	 	n4.onclick=changeIt;
	 	n5.onclick=changeIt;
	 	n6.onclick=changeIt;
	 	n7.onclick=changeIt;
	 	n8.onclick=changeIt;
	 	n9.onclick=changeIt;
	 	zero.onclick=changeIt;
	 	add.onclick=change;
	 	reduce.onclick=change;
	 	max.onclick=change;
	 	min.onclick=change;
	 	dot.onclick=change;
	 function changeIt(){
	  	show.value=show.value+this.value;
	  }
	 
	 function change(){
	 	var len=show.value.length;
	 	if(isNaN(show.value.substring(len-1,len))|show.value==""){show.value=show.value;}
	 	else{show.value=show.value+this.value;}
	 }
	 equal.onclick=function(){
	 	show.value=eval(show.value);
	 }
	 move.onclick=function(){
	 	show.value="";
	 }
	 back.onclick=function(){
	 	var len=show.value.length;
	 	show.value=show.value.substring(0,len-1)
	 }
~~~
