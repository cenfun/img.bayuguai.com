# Welcome to Bayuguai 
- homepage: [https://img.bayuguai.com/](https://img.bayuguai.com/)
- github: [https://github.com/cenfun/img.bayuguai.com](https://github.com/cenfun/img.bayuguai.com)
## Endpoint
```
https://img.bayuguai.com/:platform/:type/:ns?/:name
```
## npm downloads (svg)
```
https://img.bayuguai.com/npm/downloads/:ns?/:name?height=&color=&bg=&title=
```


|Name|20 height (default)|30 height|
|---|----|-----|
|puppeteer-chromium-resolver|![](https://img.bayuguai.com/npm/downloads/puppeteer-chromium-resolver)|![](https://img.bayuguai.com/npm/downloads/puppeteer-chromium-resolver?height=30)|
|vue|![](https://img.bayuguai.com/npm/downloads/vue)|![](https://img.bayuguai.com/npm/downloads/vue?height=30)|
|open-icons|![](https://img.bayuguai.com/npm/downloads/open-icons?title=downloads:{total})|![](https://img.bayuguai.com/npm/downloads/open-icons?height=30)|
|lithops-ui|![](https://img.bayuguai.com/npm/downloads/lithops-ui)|![](https://img.bayuguai.com/npm/downloads/lithops-ui?height=30)|
|@koa/router|![](https://img.bayuguai.com/npm/downloads/@koa/router)|![](https://img.bayuguai.com/npm/downloads/@koa/router?height=30)|

## github contributions (svg)
```
https://img.bayuguai.com/github/contributions/:name?width=&color=&axis=&bg=&title=
```
![](https://img.bayuguai.com/github/contributions/cenfun)
![](https://img.bayuguai.com/github/contributions/ruanyf)
![](https://img.bayuguai.com/github/contributions/yyx990803?width=380&title={name}%20contributions:%20{total})
![](https://img.bayuguai.com/github/contributions/tj?width=700)
![](https://img.bayuguai.com/github/contributions/ro)
## github languages (svg)
```
https://img.bayuguai.com/github/languages/:name?width=&limit=&colors=&bg=&title=
```
![](https://img.bayuguai.com/github/languages/cenfun)
![](https://img.bayuguai.com/github/languages/ruanyf)
![](https://img.bayuguai.com/github/languages/yyx990803?width=380&title={name}%20used%20languages:%20{total})
![](https://img.bayuguai.com/github/languages/tj?width=700)
![](https://img.bayuguai.com/github/languages/ro)


### clear github image cache
- [About anonymized URLs](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-anonymized-urls)
- first you need generate urls from github page
```js
Array.from(document.querySelectorAll("[data-canonical-src]")).filter(img=>img.getAttribute('data-canonical-src').startsWith("https://img.bayuguai.com")).map(img=>img.src)
```
- copy urls and call with PURGE method (axios example)
```js
const axios = require('axios');
const start = async () => {
    const list = [
        //paste your urls
    ];
    for (const item of list) {
        const res = await axios({
            url: item,
            method: 'PURGE'
        });
        console.log(res.data);
    }
};

start();
```