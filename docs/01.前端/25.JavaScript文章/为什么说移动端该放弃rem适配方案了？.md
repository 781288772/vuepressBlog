1.背景

在做移动端各种尺寸屏幕的适配时，用的最多的就是rem方案。我们都写过这样的代码,来设置根字体大小。这个计算公式中设备宽度，UI设计稿尺寸这两个参数比较好理解，可是为什么要除以100呢，为什么不是10,50或者其它的数值呢。

```
const setRem = () => {
  const deviceWidth = document.documentElement.clientWidth;
  // 获取相对UI稿，屏幕的缩放比例
  const rem = (deviceWidth *100) / 750;
  // 动态设置html的font-size
  document.querySelector('html').style.fontSize =  rem + 'px';
};
```