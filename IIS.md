+ **Application Initialization** : 
  + **Applicationhost.config** can be found in your Windows directory. It'll be the C:\Windows\System32\**inetsrv**\config.
    + **Application pool** : `startMode="AlwaysRunning"`. 
    + **Sites** : `preloadEnabled=true`.  
  By setting this attribute, we're telling IIS to send a fake request to the application when it starts up. When combined with the AlwaysRunning mode we set earlier, we'll know that every time IIS is started it will send a fake request to the application and then keep it always running.

+ **Adjusting HTTP Headers** : 
  + **Cache-Control.** headers control caching behaviors for the browser and proxy servers that are outside your control. If a request is made and you send a cache control header with it, you're telling the browser that these files are good for the next 600 seconds, or 10 minutes. So if the visitor makes another request within that 10 minutes period, the browser already has the file stored in cache. So instead of going out to the server to find them, it will put the assets from its own cache, making the request considerably faster and putting less load on your server.
  
+ **Output Caching** (Can also be set via web.config): 
  + Kernel Mode
  + User Mode
  
+ **RESPONSE HEADERS** :
  Keep-alive is a header that maintains a persistent connection between the client and server. Without this setting, the browser may open up a connection for every file it needs, meaning all your HTML, JavaScript, CSS, and images.
