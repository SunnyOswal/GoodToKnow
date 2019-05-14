+ **Application Initialization** : 
  + **Applicationhost.config** can be found in your Windows directory. It'll be the C:\Windows\System32\**inetsrv**\config.
    + **Application pool** : `startMode="AlwaysRunning"`. 
    + **Sites** : `preloadEnabled=true`.  
  By setting this attribute, we're telling IIS to send a fake request to the application when it starts up. When combined with the AlwaysRunning mode we set earlier, we'll know that every time IIS is started it will send a fake request to the application and then keep it always running.

+ **Adjusting HTTP Headers** : 
  + **Cache-Control.** headers control caching behaviors for the browser and proxy servers that are outside your control. When you make a request to a website for the first time, the request is served in all assets, such as images, HTML, and scripts, are server from the website through the internet and into your browser. If no caching is set up, the second time you make the request the same thing happens again. All of the files are transferred and it takes the same amount of time as the first visit to the website. However, if a request is made and you send a cache control header with it, you're telling the browser that these files are good for the next 600 seconds, or 10 minutes. So if the visitor makes another request within that 10 minutes period, the browser already has the file stored in cache. So instead of going out to the server to find them, it will put the assets from its own cache, making the request considerably faster and putting less load on your server. Cache control headers are also used by proxy servers, CDNs and load balancers as well. These tags suggest how long your assets should be stored in their cache. In the next demo, we'll go through adding some cache control headers to our website.  
  
+ **RESPONSE HEADERS** :
  keep-alive. Keep-alive is a header that maintains a persistent connection between the client and server. Without this setting, the browser may open up a connection for every file it needs, meaning all your HTML, JavaScript, CSS, and images.
