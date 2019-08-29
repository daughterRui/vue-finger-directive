# vue-finger-directive

vue 自定义手势插件，基于[腾讯AlloyFinger](http://alloyteam.github.io/AlloyFinger/)改造

### Use Setup
```
npm i vue-finger-directive -S

```
在main.js中导入、vue.use()，然后在子组件中就可以直接用v-tap="{methods：func , arg: args}"的方式使用

### Use in SPA
1.点击事件
```
v-tap
```
2.单击事件，和tap的区别是相差250ms
```
v-singleTap
```
3.长按事件，当点击时长超过750ms时候触发
```
v-longTap
```
4.双击事件
```
v-doubleTap

```
5.拖拽移动事件
```
v-pressMove
```
6.多点触控事件开始事件
```
v-multipointStart
```
7.多点触控事件结束事件
```
v-multipointEnd
```
8.滑动事件
```
v-swipe
```
9.旋转事件
```
v-rotate
```
10.缩放事件
```
v-pinch
```
### Example
```
<div
  :style="floatStyle"
  class="floating"
  v-pressMove="{methods: pressMove, args: 'args' }"
  ref="floating"
  v-tap="{methods: tap }"
>
methods: {
  pressMove(e, args){

  },
  tap(){

  }
}
```