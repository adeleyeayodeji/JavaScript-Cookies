# JavaScript-Cookies
Simple JavaScript Cookies

```
function setCookie(cname, cvalue, exdays, path) {
		  var d = new Date();
		  d.setTime(d.getTime() + (exdays * 24 * 60 * 60 * 1000));
		  var expires = "expires="+d.toUTCString();
		  document.cookie = cname + "=" + cvalue + ";" + expires + ";path="+path;
		  console.log("Cookies set", cname);
		}

		function getCookie(cname) {
		  var name = cname + "=";
		  var ca = document.cookie.split(';');
		    var c = ca[0];
		    if (c.indexOf(name) == 0) {
		       console.log(c.substring(name.length, c.length));
		       return c.substring(name.length, c.length);
		    }
		  return "";
		}

		function delete_cookie( name, path ) {
		  if( getCookie( name ) ) {
		    document.cookie = name + "=" +
		      (";path="+path)+";expires=Thu, 01 Jan 1970 00:00:01 GMT";
		  }
		}
    
```
