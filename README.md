# jquery.easyUtil</br>
 * Introduce</br>
 * 1. $.log(message.title)</br>
 * 2. $.superAlert/superConfirm(options)   need layer.js</br>
 				var option = {</br>
						msg : '请定义提示信息内容-参数‘msg’！',  //必填</br>
						title : '提示信息',</br>
						iconNum : 3, （1 成功,2 失败,3 问号,4 锁定,5 难过表情,6 高兴表情,7 感叹号,）</br>
						btn1 : '确定', alert可修改此项 选填</br>
						btn2 : '取消',</br>
						fnSuccess : function (){},</br>
						fnCancle : function (){},</br>
						isLog: '是否输出内部自带日志,默认为true',</br>
				};</br>
 * 3. $(selector).color()/background()/border()</br>
 * 4. $.superConcat(option)</br>
        var option = {					</br>
					strData: ['需拼接字符串,为数组形式, 必填项目'], </br>
					isArray: '默认为‘true’,设置为‘false’可得到字符串类型拼接结果', </br>
					models: {</br>
						betweenStr1: '每个字符串的引用起始符号，选填', </br>
						prefix: '前缀,选填',</br>
						suffix: '后缀,选填', </br>
						betweenStr2: '每个字符串的引用终止符号，选填', </br>	
					},</br>
					startStr: '拼接结果值的起始符号，选填,当‘isArray’设为‘false’时生效', </br>
					endStr: '拼接结果值的终止符号，选填 ,当‘isArray’设为‘false’时生效', </br>
					splitStr: '分隔符号，当‘isArray’设为‘false’时生效，选填，默认为‘,’', </br>
					isLog: '是否输出内部自带日志,默认为true',</br>
				};</br> 
 * 5. $.changeUrlArg(url, arg, val)</br>
 * 6. $.(selector).swicthBlockELm(options), needs animate.css, you can use “animate.css” or DIY animation css');</br>
 				var exemple = {</br>
					switchElmNames: '[元素id或class,使用块级元素,数组类型, 样式为"#idName或.className"],必填',</br>
					isEvent: '是否启用鼠标事件,默认为"true",选填',</br>
					eventType: '鼠标事件类型,默认"click",选填',</br>
					currentShowElm: '当前首先显示的元素序号,顺序以"switchElmNames"为主,从1开始,默认为1,即数组中第一个元素,选填',</br>
					animation: '动画样式,采用animate.css中的动画,默认为"animated flipInY",如使用该css,类名输入要完整,即“animated xxx”,保证动画正确调用;该项也可自定义,如不需要动画，填入false即可，选填 ',</br>
					callbackFn: '切换完成后的回调函数,function() {}, 选填',</br>
					callbackFnElm : '仅在事件模式下生效,激活函数的元素,可根据"switchElmNames"中顺序定义,从1开始;默认为0,即每次事件发生都激活,选填' ,</br>
					isLog: '是否输出内部自带日志,默认为true',</br>
				};</br>
 * 
 */
