###Welcome to use MarkDown
一、三种继承类别：
1.拷贝继承：通用型，有new 无new的时候都可以
2.类式继承：new 构造函数型
3.原型链继承：无new的情况

二、组件开发：
1.定义：多组对象，像兄弟之间的关系，代码复用的一种形式
2.问题：
		1）参数不写报错
	    2）参数个数不同，顺序错乱
3.解决方案
  		1）当参数超过3个时，传参数方式使用json对象传递，也叫自定义参数opt
  		2）默认参数报错的情况，可以初始化一个settings对象，也叫配置参数
  			eg：var settings={
  				toUp:function(){},
  				id:NULL
  			}
		这样，根据属性继承方式：extend(settings,opt)，当opt参数没有自身方法属性调用的话，
		会默认调用配置参数，这样就不会报错。
		function extend(obj1,obj2){
			for(var attr in obj2){
				obj1[attr]=obj2[attr];
			}
		}
		 
三、组件开发进阶--自定义事件
1）UI组件
2）功能组件
3）自定义事件：主要是跟函数有关，让函数具备事件的某些特性。
eg:
	window.addEventListener('show',function(){
		alert(1)
	},false)
	show();
		
	
	自定义事件实例：
	自定义函数和事件建立关系。
	function FireEvent(obj,events){
		
	}
		