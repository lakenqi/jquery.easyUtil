# jquery.easyUtil
 * Introduce
 * 1. $.log(message.title)
 * 2. $.superAlert/superConfirm(options)   need layer.js
 * 3. $(selector).color()/background()/border()
 * 4. $.superConcat(option)
        var option = {					
					strData: ['需拼接字符串,为数组形式, 必填项目'], 
					isArray: '默认为‘true’,设置为‘false’可得到字符串类型拼接结果', 
					models: {
						betweenStr1: '每个字符串的引用起始符号，选填', 
						prefix: '前缀,选填',
						suffix: '后缀,选填', 
						betweenStr2: '每个字符串的引用终止符号，如果与‘betweenStr1’相同可不填，选填', 	
					},
					startStr: '拼接结果值的起始符号，选填,当‘isArray’设为‘false’时生效', 
					endStr: '拼接结果值的终止符号，选填 ,当‘isArray’设为‘false’时生效', 
					splitStr: '分隔符号，当‘isArray’设为‘false’时生效，选填，默认为‘,’', 
				};
 
 * 5. $.changeUrlArg(url, arg, val)
 * */
