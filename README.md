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

 
	通用但很繁琐的方法： prototype
	alert(Object.prototype.toString.call(a) === ‘[object String]’) -------> true;
	alert(Object.prototype.toString.call(b) === ‘[object Number]’) -------> true;
	alert(Object.prototype.toString.call(c) === ‘[object Array]’) -------> true;
	alert(Object.prototype.toString.call(d) === ‘[object Date]’) -------> true;
	alert(Object.prototype.toString.call(e) === ‘[object Function]’) -------> true;
	alert(Object.prototype.toString.call(f) === ‘[object Function]’) -------> true;


	document.write 的 替代方案：
	_var sNew = document.createElement("script");
	sNew.async = true;
	sNew.src = "https://example.com/script.min.js";
	var s0 = document.getElementsByTagName('script')[0];
	s0.parentNode.insertBefore(sNew, s0);
