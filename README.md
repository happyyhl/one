
 
	通用但很繁琐的方法： prototype
	alert(Object.prototype.toString.call(a) === ‘[object String]’) -------> true;
	alert(Object.prototype.toString.call(b) === ‘[object Number]’) -------> true;
	alert(Object.prototype.toString.call(c) === ‘[object Array]’) -------> true;
	alert(Object.prototype.toString.call(d) === ‘[object Date]’) -------> true;
	alert(Object.prototype.toString.call(e) === ‘[object Function]’) -------> true;
	alert(Object.prototype.toString.call(f) === ‘[object Function]’) -------> true;

