# <h1>jquery.easyUtil</h1></br>
 * <h3>Introduce</h3>
 * <h3>为便于使用jquery.easyUtil插件现在分为完全版（位于easyUtil_core文件夹下的.all.js）和分项版（位于split文件夹下的各种名字版）</h3>
 * <h3>可根据需要引用不同的，其中完全版涵盖除drag方法外（另见split文件下）的其他所有方法，文件体积较大。而分项版体积小，但是需配合引用.core.js后缀的核心js(位于easyUtil_core文件夹下)使用。</h3>
 * <h3>方法如果没有独立的js，则均在后缀core.js核心js中</h3>
 * <h3>drag方法的参数，参见split文件夹下内容，其余所有方法使用参数及描述如下：</h3>
 * 1.<strong>$.log(message.title)</strong></br>
 * 2.<strong>$.superAlert/superConfirm(options)   needs layer.js</strong></br>
 				&emsp;<strong>var option</strong> = {</br>
						&emsp;&emsp;&emsp;<strong>msg : </strong>“请定义提示信息内容-参数‘msg’！”，  //必填</br>
						&emsp;&emsp;&emsp;<strong>title :</strong> “提示信息”，</br>
						&emsp;&emsp;&emsp;<strong>iconNum :</strong> 默认3, （1 成功，2 失败，3 问号，4 锁定，5 难过表情，6 高兴表情，7 感叹号）</br>
						&emsp;&emsp;&emsp;<strong>btn1 : </strong>'确定'， alert可修改此项 选填</br>
						&emsp;&emsp;&emsp;<strong>btn2 :</strong> '取消'，</br>
						&emsp;&emsp;&emsp;<strong>closeBtn :</strong> 1 ,关闭按钮的样式，参照layer的样式，默认为1</br> 
						&emsp;&emsp;&emsp;<strong>fnSuccess :</strong> function (){},</br>
						&emsp;&emsp;&emsp;<strong>fnCancle :</strong> function (){},</br>
						&emsp;&emsp;&emsp;<strong>isLog: </strong>“是否输出内部自带日志,默认为false”，</br>
				&emsp;};</br>
 * 3.<strong>$(selector).color()/background()/border()/getClass()/changeClass(oldName,newName)</strong></br>
 			<strong>一组整合Jquery的方法，可直接获得或修改颜色color(),background(),border();</strong></br>
 			<strong>可直接获得元素的class名称：getClass(),可以完成元素class的转换changeClass(old,new);</strong></br>
 * 4.<strong>$.superConcat(option)</strong></br>
        &emsp;<strong>var option</strong> = {					</br>
					&emsp;&emsp;&emsp;<strong>strData:</strong> ['需拼接字符串,为数组形式, 必填项目'], </br>
					&emsp;&emsp;&emsp;<strong>isArray:</strong> '默认为‘true’，设置为‘false’可得到字符串类型拼接结果', </br>
					&emsp;&emsp;&emsp;<strong>models:</strong> {</br>
						&emsp;&emsp;&emsp;&emsp;&emsp;<strong>betweenStr1:</strong> '每个字符串的引用起始符号，选填', </br>
						&emsp;&emsp;&emsp;&emsp;&emsp;<strong>prefix: </strong>'前缀,选填',</br>
						&emsp;&emsp;&emsp;&emsp;&emsp;<strong>suffix:</strong> '后缀,选填', </br>
						&emsp;&emsp;&emsp;&emsp;&emsp;<strong>betweenStr2: </strong>'每个字符串的引用终止符号，选填', </br>	
					&emsp;&emsp;&emsp;},</br>
					&emsp;&emsp;&emsp;<strong>startStr:</strong> '拼接结果值的起始符号，选填,当‘isArray’设为‘false’时生效', </br>
					&emsp;&emsp;&emsp;<strong>endStr:</strong> '拼接结果值的终止符号，选填 ,当‘isArray’设为‘false’时生效', </br>
					&emsp;&emsp;&emsp;<strong>splitStr:</strong> '分隔符号，当‘isArray’设为‘false’时生效，选填，默认为‘,’', </br>
					&emsp;&emsp;&emsp;<strong>isLog:</strong> '是否输出内部自带日志，默认为false'</br>
				&emsp;};</br> 
 * 5.<strong> $.changeUrlArg(url, arg, val)</strong></br>
 * 6.<strong>$.(selector).swicthBlockElm(option,togather) --块级元素切换，第二参数设置是否同时转换，默认false,可加入动画，需要引入 animate.css, 也可以引入其他css动画样式，或者自定义css动画;</strong></br>
 				&emsp;<strong>var exemple</strong> = {</br>
					&emsp;&emsp;&emsp;<strong>switchElmNames:</strong> '[元素id或class,使用块级元素,数组类型, 样式为"#idName或.className"],必填',</br>
					&emsp;&emsp;&emsp;<strong>isEvent:</strong> '是否启用鼠标事件,默认为"false",第二参数为true时，无效',</br>
					&emsp;&emsp;&emsp;<strong>eventType: </strong>'鼠标事件类型,默认"click",选填，第二参数为true时，无效',</br>
					&emsp;&emsp;&emsp;<strong>currentShowElm: </strong>'当前首先显示的元素序号,顺序以"switchElmNames"为主,从1开始,默认为1,即数组中第一个元素,选填,第二参数为true时，无效',</br>
					&emsp;&emsp;&emsp;<strong>animation:</strong> '[],数组形式，如果动画相同，则写一个，否则需一一对应，动画样式,采用animate.css中的动画,默认为"animated flipInY",如使用该css,类名输入要完整,即“animated xxx”,保证动画正确调用;该项也可自定义,选填 ',</br>
					&emsp;&emsp;&emsp;<strong>callbackFn: </strong>'切换完成后的回调函数,function() {}, 选填',</br>
					&emsp;&emsp;&emsp;<strong>callbackFnElm :</strong> '仅在事件模式下生效,激活函数的元素,可根据"switchElmNames"中顺序定义,从1开始;默认为0,即每次事件发生都激活,选填,第二参数为true时，无效' ,</br>
					&emsp;&emsp;&emsp;<strong>delayTime :</strong>'回调函数执行的时间,单位毫秒,默认为1000',</br>
					&emsp;&emsp;&emsp;<strong>isLog: </strong>'是否输出内部自带日志,默认为false',</br>
				&emsp;};</br>
 * 7.<strong> $.getRootPath()</strong></br>
 * 8.<strong> $.getUrlParam()</strong></br>
 * 9.<strong> $(selector).windowHeight(options) 设置屏幕高度，参数可不写，如有特殊处理参考如下：</strong></br>
 			&emsp;<strong>var exemple</strong> = {</br>
 					&emsp;&emsp;&emsp;<strong>specailElms :</strong> [],'选填，数组形式，如果有需要特殊调整高度的元素，写入此参数，注意仅限于动态取屏幕高度的元素，否则会减小到0'</br>
 					&emsp;&emsp;&emsp;<strong>changeNums :</strong> [],'选填，数组形式，上述参数中需调整的高度，如果调整高度相同，写一个即可，否则需要与上述参数一一对应'</br>
 					&emsp;&emsp;&emsp;<strong>isLog: </strong>false '是否输出内部日志，默认false'</br>
 			&emsp;}</br>
 * 10.<strong> $.superTimer(options) 统一设置js定时器管理，可自动激活和清除，也可通过事件驱动进行，详见参数设置'</strong></br>
			&emsp;<strong>var exemple</strong> = {</br>
					&emsp;&emsp;&emsp;<strong>isInterval: </strong>'选填，是否循环定时，默认false',</br>
					&emsp;&emsp;&emsp;<strong>times:</strong> '选填，[1000] 每个定时器的执行时间，单位毫秒，数组形式，默认一个时间：1000ms,如有多个触发时间，需要与定时器函数一一对应',</br>
					&emsp;&emsp;&emsp;<strong>timerFns:</strong> '必填，[function() {}] 定时器执行函数内容，数组形式，将完整函数写入数组，每一个functiong(){}代表一个定时器，如有多个，则按先后顺序写入',</br>
					&emsp;&emsp;&emsp;<strong>isEvent:</strong> '选填，是否事件驱动定时器，默认false',</br>
					&emsp;&emsp;&emsp;<strong>eventType:</strong> "选填，['click']，事件驱动类型，数组，默认click,建议使用一个事件，如有多个事件，则必须要与触发元素，定时器函数一一对应（顺序，个数必须完全一致）",</br>
					&emsp;&emsp;&emsp;<strong>eventElms:</strong> '选填，[]，事件触发元素#xx或.xx,数组，如开启事件驱动，该项必填，要求与事件驱动类型一致，如有多个，需要一一对应',</br>
					&emsp;&emsp;&emsp;<strong>isClear: </strong>'选填，是否清除定时器，默认false',</br>
					&emsp;&emsp;&emsp;<strong>clear:</strong> {</br>
					&emsp;&emsp;&emsp;&emsp;	&emsp;<strong>cELms: </strong>'选填，[]，清除定时器子项，事件触发元素，数组，该项如不填，默认采用定时清除，如有多个，则要求同上',</br>
						&emsp;&emsp;&emsp;&emsp;&emsp;<strong>cEventType: </strong>"选填，['click']，清除定时器事件驱动类型，数组，默认click,建议使用一个事件，如有多个事件，则必须要与触发元素，定时器函数一一对应（顺序，个数必须完全一致）",</br>
						&emsp;&emsp;&emsp;&emsp;&emsp;<strong>cTimes: </strong>'选填，[1000]，清除定时器的时间，如设置了事件触发元素，则此项无效，默认1000ms,如有多个时间，要求同上',</br>
					&emsp;&emsp;&emsp;},</br>
					&emsp;&emsp;&emsp;<strong>isLog:</strong> '是否输出内部自带日志,默认为false',</br>
				&emsp;};</br>
 * 11.<strong> $.optionCardSwitch(options) --设置选项卡切换div功能，可设置事件激活类型，设置动画，详见参数设置</strong></br>
			 &emsp; <strong>var example</strong> = {</br>
							&emsp;&emsp;&emsp;<strong>triggerElm :</strong> '触发转换的元素.class或标签名,建议使用无序列表Ul li 必填',</br>
								&emsp;&emsp;&emsp;<strong>switchElm :</strong> '转换div的主容器.Class,#id,或标签,建议使用DIV,必填',</br>
								&emsp;&emsp;&emsp;<strong>switchInner : </strong>'被转换的div.class或标签，建议使用div，默认值为div,如与默认值一致，选填',</br>
								&emsp;&emsp;&emsp;<strong>selectedClass :</strong> '当前激活的选项卡样式类型，选填',</br>
								&emsp;&emsp;&emsp;<strong>eventType:</strong> 'click，触发切换的鼠标事件类型，默认click,不可使用伪类，选填',</br>
								&emsp;&emsp;&emsp;<strong>animation : </strong>'切换时的动画class类，默认无，选填',</br>
								&emsp;&emsp;&emsp;<strong>switchTime : </strong>'100,切换的速度，默认100毫秒，选填',</br>
								&emsp;&emsp;&emsp;<strong>hoverClass :</strong> '鼠标移动到选项卡的样式，选填',</br>
								&emsp;&emsp;&emsp;<strong>isLog :</strong> 'false,是否输内部日志，默认false',</br>
							&emsp;};</br>
 * 12.<strong>$.autoFoldMenu(options) -- 设置菜单自动折叠和显示功能</strong></br>
 				<strong>var example</strong> = {</br>
 						&emsp;&emsp;<strong>eventElm : </strong>'触发动作的元素,#id,.class,标签,必填',</br>
						&emsp;&emsp;<strong>menuElm :</strong> '做为菜单隐藏和显示的元素,#id,.class,标签,必填',</br>
						&emsp;&emsp;strong>parentElm :</strong> '菜单项和触发元素的共同直接父级元素,#id,.class,标签,必填',</br>
						&emsp;&emsp;<strong>showClass : </strong>'菜单显示时动作按钮的CSS类,选填 如有则两项必填',</br>
						&emsp;&emsp;<strong>hiddenClass : </strong>'菜单隐藏时动作按钮的CSS类,选填 如有则两项必填',</br>
						&emsp;&emsp;<strong>eventType : </strong>'click,触发事件类型,默认click,选填',</br>
						&emsp;&emsp;<strong>speed : </strong>'600,折叠速度,毫秒,默认600,选填',</br>
						&emsp;&emsp;<strong>isMouseout : </strong>'false,是否在鼠标离开时自动隐藏所有菜单,默认false, 选填',</br>
						&emsp;&emsp;<strong>isLog :　</strong>'false,是否显示内部日志,默认false, 选填',</br>
				&emsp;};</br>
*  
*/
