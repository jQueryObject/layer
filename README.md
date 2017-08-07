# layer jquery弹出层插件layer

效果如下：
![](img/img.gif)

all code:
```
<!Doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="keywords" content="JS代码,其他代码,JS广告代码,JS特效代码" />
    <meta name="description" content="此代码内容为layer jQuery弹出层插件。" />
    <title>layer jQuery弹出层插件</title>
    <style>
        html{background-color:#E3E3E3; font-size:14px; color:#000; font-family:'微软雅黑'}
        a,a:hover{ text-decoration:none;}
        pre{font-family:'微软雅黑'}
        .box{padding:20px; background-color:#fff; margin:50px 100px; border-radius:5px;}
        .box a{padding-right:15px;}
        #about_hide{display:none}
        .layer_text{background-color:#fff; padding:20px;}
        .layer_text p{margin-bottom: 10px; text-indent: 2em; line-height: 23px;}
        .button{display:inline-block; *display:inline; *zoom:1; line-height:30px; padding:0 20px; background-color:#56B4DC; color:#fff; font-size:14px; border-radius:3px; cursor:pointer; font-weight:normal;}
        .photos-demo img{width:200px;}
    </style>
</head>
<body>
<div style="text-align:center;margin:50px 0">
    <p></p>
    <p>
    <p>layer jQuery弹出层插件，兼容主流浏览器！</p>
    <p>layer是一款近年来备受青睐的web弹层组件，它具备全方位的解决方案，致力于服务各水平段的开发人员，您的页面会轻松地拥有丰富友好的操作体验。</p>
    <p>使用方法：</p>
    <p>1、使用时，请把文件夹layer整个放置在您站点的任何一个目录，只需引入layer.js即可，除jQuery外，其它文件无需再引入。</p>
    <p>2、如果您的js引入是通过合并处理或者您不想采用layer自动获取的绝对路径，您可以通过layer.config()来配置（详见官网API页）</p>
    <p>3、jquery需1.8+</p>
    </p>
    <p style="margin:20px 0"></p>
</div>
<!-- 代码 开始 -->
<div class="box">
    <h2 style="padding-bottom:20px;">扩展模块：图片查看器（相册层）</h2>
    <div id="photosDemo" class="photos-demo">
        <!-- layer-src表示大图  layer-pid表示图片id  src表示缩略图-->
        <img layer-src="img/1.jpg" layer-pid="" src="img/1.jpg" alt="第一张">
        <img layer-src="img/2.jpg" layer-pid="" src="img/2.jpg" alt="第二张">
        <img layer-src="img/3.jpg" layer-pid="" src="img/3.jpg" alt="第三张">
        <img layer-src="img/4.jpg" layer-pid="" src="img/4.jpg" alt="第四张">
        <img layer-src="img/5.jpg" layer-pid="" src="img/5.jpg" alt="第五张">
    </div>
</div>
</body>
</html>
<script src="layer/jquery-1.8.3.min.js"></script>
<script src="layer/layer.js"></script>
<script>
    !function(){
//页面一打开就执行，放入ready是为了layer所需配件（css、扩展模块）加载完毕
        layer.ready(function(){
            //官网欢迎页
            layer.open({
                type: 2,
                //skin: 'layui-layer-lan',
                title: 'layer弹层组件',
                fix: false,
                shadeClose: true,
                maxmin: true,
                area: ['1000px', '500px'],
                content: 'http://www.baidu.com/',
                end: function(){
                    layer.tips('试试相册模块？', '#photosDemo', {tips: 1})
                }
            });

            //layer.msg('欢迎使用layer');

            //使用相册
            layer.photos({
                photos: '#photosDemo'
            });
        });

//关于
        $('#about').on('click', function(){
            layer.alert(layer.v + ' - A5源码出品 sentsin.com');
        });

    }();
</script>
<!-- 代码 结束 -->
```

