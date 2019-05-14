+ **Application Initialization** : 
  + **Applicationhost.config** can be found in your Windows directory. It'll be the C:\Windows\System32\**inetsrv**\config.
    + **Application pool** : `startMode="AlwaysRunning"`. 
    + **Sites** : `preloadEnabled=true`.  
  By setting this attribute, we're telling IIS to send a fake request to the application when it starts up. When combined with the AlwaysRunning mode we set earlier, we'll know that every time IIS is started it will send a fake request to the application and then keep it always running.
