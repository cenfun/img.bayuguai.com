# Welcome to Bayuguai <a name="top"></a>
- Homepage: [https://img.bayuguai.com/](https://img.bayuguai.com/) 
- Github: [https://github.com/cenfun/img.bayuguai.com](https://github.com/cenfun/img.bayuguai.com)
- [Endpoint](#endpoint)
    - [npm downloads](#npm-downloads)
    - [npm size](#npm-size)
    - [npm dependencies](#npm-dependencies)
    - [github contributions](#github-contributions)
    - [github languages](#github-languages)
- [How to clear github image cache](#how-to-clear-github-image-cache)

## Endpoint
```
https://img.bayuguai.com/:platform/:type/:ns?/:name
```
## npm downloads
```
https://img.bayuguai.com/npm/downloads/:ns?/:name
```
<details>
    <summary>query</summary>
    <ul>
        <li>height=20</li>
        <li>color=#44cc11</li>
        <li>bg=#007ec6</li>
        <li>label={total}/month</li>
        <li>output=svg | json</li>
    </ul>
</details>

|Name|20 height|30 height|
|---|----|-----|
|puppeteer-chromium-resolver|![](https://img.bayuguai.com/npm/downloads/puppeteer-chromium-resolver)|![](https://img.bayuguai.com/npm/downloads/puppeteer-chromium-resolver?height=30)|
|vue|![](https://img.bayuguai.com/npm/downloads/vue)|![](https://img.bayuguai.com/npm/downloads/vue?height=30)|
|open-icons|![](https://img.bayuguai.com/npm/downloads/open-icons?label={total}%20downloads)|![](https://img.bayuguai.com/npm/downloads/open-icons?height=30)|
|lithops-ui|![](https://img.bayuguai.com/npm/downloads/lithops-ui)|![](https://img.bayuguai.com/npm/downloads/lithops-ui?height=30)|
|@koa/router|![](https://img.bayuguai.com/npm/downloads/@koa/router)|![](https://img.bayuguai.com/npm/downloads/@koa/router?height=30&label=)|

[▲Top](#top)
## npm size
```
https://img.bayuguai.com/npm/size/:ns?/:name
```
<details>
    <summary>query</summary>
    <ul>
        <li>bg=#007ec6</li>
        <li>label=</li>
        <li>output=svg | json</li>
    </ul>
</details>

|Name|Size|
|---|---:|
|puppeteer-chromium-resolver|![](https://img.bayuguai.com/npm/size/puppeteer-chromium-resolver)|
|vue|![](https://img.bayuguai.com/npm/size/vue)|
|webpack-stats-report|![](https://img.bayuguai.com/npm/size/webpack-stats-report)|
|console-grid|![](https://img.bayuguai.com/npm/size/console-grid)|
|starfall-cli|![](https://img.bayuguai.com/npm/size/starfall-cli)|
|open-icons|![](https://img.bayuguai.com/npm/size/open-icons?label=size)|
|lithops-ui|![](https://img.bayuguai.com/npm/size/lithops-ui)|
|@koa/router|![](https://img.bayuguai.com/npm/size/@koa/router)|

[▲Top](#top)
## npm dependencies
```
https://img.bayuguai.com/npm/dependencies/:ns?/:name
```
<details>
    <summary>query</summary>
    <ul>
        <li>bg=#007ec6</li>
        <li>label=</li>
        <li>output=svg | json</li>
    </ul>
</details>

|Name|Dependencies|
|---|---:|
|puppeteer-chromium-resolver|![](https://img.bayuguai.com/npm/dependencies/puppeteer-chromium-resolver)|
|vue|![](https://img.bayuguai.com/npm/dependencies/vue)|
|webpack-stats-report|![](https://img.bayuguai.com/npm/dependencies/webpack-stats-report)|
|console-grid|![](https://img.bayuguai.com/npm/dependencies/console-grid)|
|starfall-cli|![](https://img.bayuguai.com/npm/dependencies/starfall-cli)|
|open-icons|![](https://img.bayuguai.com/npm/dependencies/open-icons?label=dependencies)|
|lithops-ui|![](https://img.bayuguai.com/npm/dependencies/lithops-ui)|
|@koa/router|![](https://img.bayuguai.com/npm/dependencies/@koa/router)|

[▲Top](#top)
## github contributions
```
https://img.bayuguai.com/github/contributions/:name
```
<details>
    <summary>query</summary>
    <ul>
        <li>width=600</li>
        <li>color=#44cc11</li>
        <li>axis=#999</li>
        <li>bg=#fff</li>
        <li>label={total} Contributions Past Year - {name}</li>
        <li>output=svg | json</li>
    </ul>
</details>

![](https://img.bayuguai.com/github/contributions/cenfun)
![](https://img.bayuguai.com/github/contributions/ruanyf)
![](https://img.bayuguai.com/github/contributions/yyx990803?width=380&label={name}%20contributions:%20{total})
![](https://img.bayuguai.com/github/contributions/mxschmitt?width=700)
![](https://img.bayuguai.com/github/contributions/ro)

[▲Top](#top)
## github languages
```
https://img.bayuguai.com/github/languages/:name
```
<details>
    <summary>query</summary>
    <ul>
        <li>width=600</li>
        <li>limit=20</li>
        <li>colors=dodgerblue,green,orangered...</li>
        <li>bg=#fff</li>
        <li>label={total} Used Languages - {name}</li>
        <li>output=svg | json</li>
    </ul>
</details>

![](https://img.bayuguai.com/github/languages/cenfun)
![](https://img.bayuguai.com/github/languages/ruanyf)
![](https://img.bayuguai.com/github/languages/yyx990803?width=380&label={name}%20used%20languages:%20{total})
![](https://img.bayuguai.com/github/languages/mxschmitt?width=700)
![](https://img.bayuguai.com/github/languages/ro)

---
[▲Top](#top)
## How to clear github image cache
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
[▲Top](#top)