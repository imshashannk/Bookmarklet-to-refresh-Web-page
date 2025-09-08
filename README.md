# Auto Page Refresher (Bookmarklet)

This is a simple JavaScript snippet that reloads the current webpage inside an iframe every **30 seconds**.  
Useful for monitoring dashboards, live data pages, or any website that needs periodic refreshing.  

---

## How It Works
- Injects an `<iframe>` that loads the current page.  
- Uses `setInterval` to refresh the iframe every 30 seconds.  
- Runs locally in the browser — no data is stored or sent anywhere.  

---

## Usage
1. Copy the code below:
   ```javascript
   javascript:document.getElementsByTagName("body")[0].innerHTML = "<iframe id=\"testFrame\" src=\""+window.location.toString()+"\" style=\"position: absolute; top:0; left:0; right:0; bottom:0; width:100%; height:100%;\"></iframe>";reloadTimer = setInterval(function(){ document.getElementById("testFrame").src=document.getElementById("testFrame").src },30*1000)
