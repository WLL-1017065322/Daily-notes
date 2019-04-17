​        afterEnter(el){

​          // 这句话， 第一个功能，是控制小球的显示与隐藏

​          // 第二个功能： 直接跳过后半场动画，让 flag 标识符 直接变为 false

​          // 当第二次再点击 按钮的时候， flag  false  ->    true

​          this.flag = !this.flag

​          // el.style.opacity = 0.5

​          // Vue 把一个完整的动画，使用钩子函数，拆分为了两部分：

​          // 我们使用 flag 标识符，来表示动画的切换；

​          // 刚以开始，flag = false  ->   true   ->   false

​        }