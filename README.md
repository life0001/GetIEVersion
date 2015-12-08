# GetIsBrowser
判断是什么浏览器

<pre>
$(function() {
    var fox = 0, chro = 0, timer, now = 0;
    //判断是否IE8以下
    (function checkVersion() {
        var ver = getInternetExplorerVersion();
        if (ver > -1) {
            if (ver > 9.0) {
                // "IE10以上";
                //$('#u1').show();
                //$('.arrow').show();
            }
            else {//ie8以下
                $('.buttons-wrapper').hide();
                $('#u1').show();
                $('.arrow').show()
            }
        }
    })();
    function myBrowser() {
        var userAgent = navigator.userAgent; //取得浏览器的userAgent字符串
        var isOpera = userAgent.indexOf("Opera") > -1; //判断是否Opera
        var isMaxthon = userAgent.indexOf("Maxthon") > -1; //判断是否傲游3.0
        var isIE = userAgent.indexOf("compatible") > -1 && userAgent.indexOf("MSIE") > -1 && !isOpera; //判断是否IE
        var isFF = userAgent.indexOf("Firefox") > -1; //判断是否Firefox
        var isSafari = userAgent.indexOf("Safari") > -1 && userAgent.indexOf("Chrome") < 1; //判断是否Safari
        var isChrome = userAgent.indexOf("Chrome") > -1; //判断是否Chrome
        if (isFF) {
            return "FF";
        }
        if (isOpera) {
            return "Opera";
        }
        if (isMaxthon) {
            return "Maxthon";
        }
        if (isSafari) {
            return "Safari";
        }
        if (isChrome) {
            return "Chrome";
        }
    } //myBrowser() end
    //判断是否safari
    if (myBrowser() == "Safari") {
        
    }
    //判断是否Firefox
    if (myBrowser() == "FF") {
        
    }
});
function getInternetExplorerVersion()
{
    var rv = -1; // Return value assumes failure.
    if (navigator.appName == 'Microsoft Internet Explorer')
    {
        var ua = navigator.userAgent;
        var re  = new RegExp("MSIE ([0-9]{1,}[\.0-9]{0,})");
        if (re.exec(ua) != null){
            rv = parseFloat( RegExp.$1 );
        }
    }
    return rv;
}



</pre>
