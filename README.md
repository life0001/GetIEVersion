# GetIEVersion
判断是否是IE浏览器

function getInternetExplorerVersion()
// Returns the version of Windows Internet Explorer or a -1
// (indicating the use of another browser).
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
function checkVersion()
{
    var msg = "You're not using Windows Internet Explorer.";
    var ver = getInternetExplorerVersion();
    if ( ver> -1 )
    {
        if ( ver> 8.0 ){
            // "IE9以上";
            
        }
            
        else{
            //IE8一下
            
        }
        
    }
}
