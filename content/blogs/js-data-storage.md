---
title: "Javascript Data Storage"
draft: true
---

Sometimes you need to store a large amount of data in the browser, such as when the privacy policy doesn't allow the data to be uploaded to the server, or simply that your app requires a lot of temporary storage.
The old-school solution would be to use cookies, but it is painful to set up. The current simple solution would be to use localStorage. you can simply:

```
localStorage.setItem('name','Chris');
```

This works great if you have a handful of data to handle, but you might want a better library for more data, such as IndexedDB