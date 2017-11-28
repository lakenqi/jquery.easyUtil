# jquery.easyUtil</br>
 * Introduce</br>
 * 1. $.log(message.title)</br>
 * 2. $.superAlert/superConfirm(options)   need layer.js</br>
 * 3. $(selector).color()/background()/border()</br>
 * 4. $.superConcat(option)</br>
        var option = {					</br>
					strData: ['需拼接字符串,为数组形式, 必填项目'], </br>
					isArray: '默认为‘true’,设置为‘false’可得到字符串类型拼接结果', </br>
					models: {</br>
						betweenStr1: '每个字符串的引用起始符号，选填', </br>
						prefix: '前缀,选填',</br>
						suffix: '后缀,选填', </br>
						betweenStr2: '每个字符串的引用终止符号，如果与‘betweenStr1’相同可不填，选填', </br>	
					},</br>
					startStr: '拼接结果值的起始符号，选填,当‘isArray’设为‘false’时生效', </br>
					endStr: '拼接结果值的终止符号，选填 ,当‘isArray’设为‘false’时生效', </br>
					splitStr: '分隔符号，当‘isArray’设为‘false’时生效，选填，默认为‘,’', </br>
				};</br>
 </br>
 * 5. $.changeUrlArg(url, arg, val)</br>
 * */</br>
