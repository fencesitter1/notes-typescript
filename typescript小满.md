# 接口和对象类型

## 函数接口
```ts
interface Fn{
	(name:string):number[]
}

const fn:Fn=function(name:string){
	return [1]
}
```
