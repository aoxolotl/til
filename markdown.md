## Previewing markdown
An easy way to view github flavoured markdown (GFM) without going through the hassle of converting to pdf first is to use a `pip` package called `grip`. `grip` hosts a server with the rendered file on `localhost` like so:
```sh
$ pip install grip
$ grip markdown.md -b 
```
The `-b` opens a tab in the browser.

