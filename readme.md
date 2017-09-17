dragSearch pc端原生js下拉带搜索插件

版本:2.0
兼容性:兼容IE7及以上和其他浏览器

提示：时间紧促，难免可能出现问题，若发现问题可以联系QQ:1484840832，谢谢！

使用方法:
示例：
new DragSearch({
	id:'select1',
	config:{
	   tip:'请选择',
       placeholder:'请输入内容搜索',
       maxHeight:300
	},
	data:[
        {
           value:100,
           text:'列表1',
           selected:true
        },
        {
           value:101,
           text:'列表2'
        },
        {
           value:102,
           text:'列表3'
        },
        {
           value:103,
           text:'列表4'
        }
	],
	success:function(res,e){
        console.log(res,e);
    }
});

解释：
1) id:传入input或者select元素的id,将会自动创建内容替换该input输入框或者select下拉框，input或者select中加入name属性，可以创建包含同name的type=hidden的隐藏域，以便用于表单提交

2) config:配置。tip为提示框默认显示的文字，placeholder为创建的输入框的提示文字，maxHeight为创建的下拉框的最大高度，可以传入数字如300或者字符串'300px'。不设置配置将会使用默认配置

3) data: 数据。  数据格式必须严格如上所示包含value和text的项，value传列表id，text传列表内容，如果想初始化选中某项，则可以在该项中设置selected:true，如果设置了多项selected为true，则只会有第一个设置的成功。如果传入空数组，则显示暂无数据。

4) success:成功回调。 点击选择某项时将会调用，参数：第一个参数为选择该项的value和text的对象，第二个参数为点击时的事件对象。如果初始化选中了某项，则初始化也会执行回调，只不过第二个参数为null
