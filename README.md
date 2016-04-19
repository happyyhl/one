# one
xixi
/*前端资源*/
https://cnodejs.org/topic/56ef3edd532839c33a99d00e    
/*知乎 html5 demo*/
http://www.zhihu.com/question/24398907
/*阿里*/
http://www.alloyteam.com/
/*移动端*/
http://www.alloyteam.com/2016/03/mobile-web-adaptation-tool-rem/
/*谷歌缓存查看*/
chome://net.internals/#dns


var a = cuso.content;
editorA.ready(function() {
	editorA.setContent(a);
 });
 
 
 /*问题*/
 userCenterMenu: function (menu) {
	var menuHtml = $.ajax({
		type:"GET",
		url:"/views/userCenter/per_center.html",
		data:{},
		async:false,
		datetype:"html"
	}).responseText;
	var html = $(menuHtml);
	html.find(".col-main").append($("body").children());//*****
	
	$("body").empty().html($(html));
	$("body").find(".user-ck dd a").removeClass("active");
    	$("body").find(".user-ck dd a."+menu).addClass("active");
	$("body").prepend(common.global.header('.type1','',true)).append(common.global.footer()).show();
}
=== 》》》》//多次触发
$(function () {
	console.log($("body .col-main").length);
	if($("body .col-main").length <= 0){
	}
    
});
