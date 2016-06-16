## 任务笔记 ##

[效果]()

# js代码中绑定事件的三种方法 #

原生函数
`` <input  onclick="alert('谢谢支持')"  type="button"  value="点击我，弹出警告框" /> ``

自定义函数

``<input  onclick="myAlert()"  type="button"  value="点击我，弹出警告框" />``
``  <script type="text/javascript">
  function myAlert(){
      alert("谢谢支持");
  }
  </script
``

在JavaScript代码中绑定

    elementObject.onXXX=function(){
        // 事件处理代码
    }
  
绑定事件监听函数
    
    elementObject.addEventListener(eventName,handle,useCapture);
    elementObject.attachEvent(eventName,handle);
考虑到兼容性    

        function addEvent(obj,type,handle){
            try{  // Chrome、FireFox、Opera、Safari、IE9.0及其以上版本
                obj.addEventListener(type,handle,false);
            }catch(e){
                try{  // IE8.0及其以下版本
                    obj.attachEvent('on' + type,handle);
                }catch(e){  // 早期浏览器
                    obj['on' + type] = handle;
                }
            }
        }
    
接受键盘输入

    $("aqi-input").onkeyup = function(event){
                if(event.keyCode == 13){
                    handler();
                }
            };
            
    一个keycode对应着键盘上的一个按键
            
            
尚未解决的问题：抵御XSS攻击，对 <><>这样的符号进行处理
