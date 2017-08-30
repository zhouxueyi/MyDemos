# MyDemos

关于CSS居中：

居中可以以下几种情况：
1.单行文本居中
2.定宽高内容居中
3.不定宽高居中

其中，单行文本居中分元素text-align：center；line-height与height相等即可
定宽高内容可采用position:absolute; top:50%; left:50; margin-top:-50%高；margin-left:-50%宽; 直接解决

以下内容主要针对不定宽高内容块居中：

方法1：
position + transform解决方案
//增加空outer层
.outer{
    position: relative;
    top: 50%;
    left: 50%;
}
.inner{
    position: relative;
    transform: translate(-50%, -50%);
}

方法2：vh、vw、transform解决方案
.inner{
    position:absolute;
    top: 50vh;
    left: 50vw;
    transform: translate(-50%, -50%);
}

方法3：flex解决方案
.inner{
    display:flex;
    align-items:center;
    justify-content:center;
}
