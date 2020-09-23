<div align="center">

## WebCam Image Refresh  with Java script


</div>

### Description

This code was written to display an image an constantly refresh it without reloading the entire page.

This works great with webcam software that constantly uploads a picture to your server.

All you have to do is put this java script into your page with the name of the image & WebCam IP address (in the Srvr_IP variable ),

and it will constantly refresh the image ( you can change it's timeout ) without forcing an entire page reload.

This example includes a test page and the source code java script file .

Enjoy ...
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Reza  Zahidi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/reza-zahidi.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |
**Category**       |[\.JS files](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/js-files__2-77.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/reza-zahidi-webcam-image-refresh-with-java-script__2-2159/archive/master.zip)

### API Declarations

```
<html><body>
<script LANGUAGE="JavaScript" src="my_tv2web.js">
</script>
</body></html>
```


### Source Code

```
<!-- ======== my_tv2web.js ===========
//========= ©Reza Zahidi, Rasht-Iran, www.Zahidi.Net ======
browserType = navigator.appName;
newImage = new Image();
Srvr_IP= "http://127.0.0.1/Image.jpg?";
var dly;
if (browserType == "Netscape") document.write('<IMG SRC="'+ Srvr_IP +'" >')
 else	document.write('<IMG SRC="' + Srvr_IP +'" name=ZahidiTV2Web Alt="Zahidi Camera(TV) to Web Server is off. Please Try later." border=1 >');
uniq= 1;
newImage.src= Srvr_IP + uniq;
SnapShot_Loop(4000);
function SnapShot_Loop(delay)
{
 dly= delay
 if( document.all) loadNewImage();
 setTimeout("SnapShot_Loop(dly)",delay);
}
function loadNewImage()
{
  Stamp = new Date();
  uniq= Stamp.getTime();
  document.images.ZahidiTV2Web.src= newImage.src;
  newImage.src= Srvr_IP + uniq;
  window.status = "Displaying live video ...";
}
//============================== -->
```

