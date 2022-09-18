---
title: "How to connect to github"
draft: false
---

When using git, it is a hassle to retype the password every time we commit. Of course, you can always save the password locally on the disk, like this:

```
git config credential.helper store
```

The problem with this method is that the password is stored in plain text locally, which can be a security concern if your device gets stolen.  
A more secure method would be to set a time-out for the password cache. For example, something like this would expire the password after 1 hour:

```
git config --global credential.helper 'cache --timeout=3600'
```

If you don't want to use passwords altogether, you can also connect to Github through SSH. A more detailed guide can be found on Github's documentation.  
Nevertheless, the most secure way is obviously to retype the password every time you commit, but if you are looking for other ways, perhaps consider one of these methods listed above.