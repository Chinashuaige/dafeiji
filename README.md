1.<!DOCTYPE HTML>  
2.<html lang="zh-CN">  
3.<head>  
4.    <meta charset="UTF-8">  
5.    <title>手机APP下载页面：根据终端辨别下载地址</title>  
6.    <script type="text/javascript">  
7.        // 获取终端的相关信息  
8.        var Terminal = {  
9.            // 辨别移动终端类型  
10.            platform : function(){  
11.                var u = navigator.userAgent, app = navigator.appVersion;  
12.                return {  
13.                    // android终端或者uc浏览器  
14.                    android: u.indexOf('Android') > -1 || u.indexOf('Linux') > -1,  
15.                    // 是否为iPhone或者QQHD浏览器  
16.                    iPhone: u.indexOf('iPhone') > -1 ,  
17.                    // 是否iPad  
18.                    iPad: u.indexOf('iPad') > -1  
19.                };  
20.            }(),  
21.            // 辨别移动终端的语言：zh-cn、en-us、ko-kr、ja-jp...  
22.            language : (navigator.browserLanguage || navigator.language).toLowerCase()  
23.        }  
24.   
25.        // 根据不同的终端，跳转到不同的地址  
26.        var theUrl = 'https://itunes.apple.com/cn/app/id1148626685?mt=8';  
27.        if(Terminal.platform.android){  
28.            theUrl = 'http://klby.3838wan.com/?package_id=555502';  
29.        }else if(Terminal.platform.iPhone){  
30.            theUrl = 'https://itunes.apple.com/cn/app/id1148626685?mt=8';  
45.            }  
46.        }  
47.   
48.        location.href = theUrl;  
49.    </script>  
50.</head>  
51.<body>  
52.    <!--  
53.   
54.    -->  
55.</body>  
56.</html>  
