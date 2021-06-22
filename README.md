# IONIC5 Svelte Sidemenu Template

ionic https://ionicframework.com/

Svelte https://svelte.dev/

This template should help get you quick started developing a sidemenu IONIC5 app using Svelte.

这个模板应该将会帮助你快速搭建IONIC5开发环境，使用Svelte来开发一个SideMenu应用




**What packages were used in the template and why?**
**用到了哪些包，为什么要用这些包？**

svelte-spa-router is used for routing instead of using default routing components like ion-route ,this package use URL.hash (like 'http://localhost/#/inbox') to routing which will not cause a page refreshing and it is pretty simple to use.

使用svelte-spa-router代替了IONIC5默认的路有组件，它使用Hash方式进行路由（如'http://localhost/#/inbox' ），不会造成页面刷新，并且它用起来非常简单



**How to use ionic locally without using CDN in Svelte?**
**如何在本机使用IONIC而不是使用CDN连接**


replace the CDN link content in index.html with  following:
```html

    <script type="module" src="/js/ionic/ionic.esm.js"></script>
    <script nomodule src="/js/ionic/ionic.js"></script>
    <link rel="stylesheet" href="/css/ionic.bundle.css"/>

    <script type="module" src="/js/ionicons/ionicons.esm.js"></script>
    <script nomodule src="/js/ionicons/ionicons.js"></script>


```
THEN<br>
1,copy ionic and ionicons  js folder to /public/js/ionic , /public/js/ionicons <br>
2,copy ionic.bundle.css to /public/css/

