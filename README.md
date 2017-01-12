
    深度复制方法：
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
    识别是否是对象
    通用但很繁琐的方法： prototype
	alert(Object.prototype.toString.call(a) === ‘[object String]’) -------> true;
	alert(Object.prototype.toString.call(b) === ‘[object Number]’) -------> true;
	alert(Object.prototype.toString.call(c) === ‘[object Array]’) -------> true;
	alert(Object.prototype.toString.call(d) === ‘[object Date]’) -------> true;
	alert(Object.prototype.toString.call(e) === ‘[object Function]’) -------> true;
	alert(Object.prototype.toString.call(f) === ‘[object Function]’) -------> true;

