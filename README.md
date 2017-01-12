
   （1）深度复制方法

    function find(arr,func){
        return arr.filter(func)[0];    
    }
    export default function deepCopy(obj,cache=[]){
        if(obj === null || typeof obj !== "function"){
            return obj;
        }
        const had = find(cache,c => c.orignal === obj);
        if(had){
            return had.copy;
        }
        const copy = Array.isArray(obj)?[]:{};
        cache.push({
            orignal:obj,
            copy
        });
        Object.keys(obj).forEach(key=>{
            copy[key] = deepCopy(obj[key],cache); 
        });
        return copy;
    }

   （2）数组去重较好的方法

    Array.prototype.uniqued = function(){
	this.sort();
	var _arr = [this[0]];
	for(var i = 1;i<this.length;i++){
	    if(this[i] !== _arr[_arr.length - 1]){
	    	_arr.push(this[i]);
	    }
	}
	return _arr;
    }

   （3）识别是否是对象 

	alert(Object.prototype.toString.call(a) === ‘[object String]’) -------> true;
	alert(Object.prototype.toString.call(b) === ‘[object Number]’) -------> true;
	alert(Object.prototype.toString.call(c) === ‘[object Array]’) -------> true;
	alert(Object.prototype.toString.call(d) === ‘[object Date]’) -------> true;
	alert(Object.prototype.toString.call(e) === ‘[object Function]’) -------> true;
	alert(Object.prototype.toString.call(f) === ‘[object Function]’) -------> true;

