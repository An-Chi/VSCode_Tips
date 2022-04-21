---
tags: VSCode Tips
title: 筆記 - 20 個 VSCode 開發小技巧(六角學院-卡斯伯)
---

### 已安裝過的 VSCode 
觀看影片之前，卡斯伯老師有在社團提醒 如果有裝了一堆擴充套件卻不知道有什麼用的症狀，建議先移除 VSCode ( [Clean uninstall VSCode](https://code.visualstudio.com/docs/setup/uninstall#_clean-uninstall) ) 


#### 筆記內容
主要參考自 六角學院卡斯伯老師的教學
20 個 VSCode 開發小技巧，讓你 Coding 三倍速！
- 部落格：[](https://www.casper.tw/)[https://www.casper.tw/](https://www.casper.tw/)
- 文件連結：[](https://hex.school/w5FJv)[https://hex.school/w5FJv](https://hex.school/w5FJv)
- video：[](https://youtu.be/LOjUnXk_TNU)[https://youtu.be/LOjUnXk_TNU](https://youtu.be/LOjUnXk_TNU)

---


### VSCode 筆記待補
- [ ] 個人使用的介面是英文版的，紀錄VSCode內建會是英文，中文之後再補充
- [ ] 操作附圖說明


### 使用 VSCode 的好習慣
1. 裝任何工具(Extensions)之前，先確保自己知道此工具是要做什麼的，否則一旦不常使用或是用不到的工具裝太多，只會佔電腦空間(記憶體、硬碟空間)

2. 安裝工具之後，試用後不符合自己需求，那就直接移除掉。


#### 再簡單的專案都要用伺服器的方式開啟
不要直接將專案的網頁檔案直接拖曳到瀏覽器，有可能(上線時)會出錯
使用 **Live Server** 的 **GO Live**


---

### Recording Keys
>**`Ctrl + K , Ctrl + S` -> Keyboard Shortcuts**
>**File -> Preferences -> Keyboard Shortcuts**



#### 待整理表格

|Windows|MacOS| description |
|---------|-----|--------------- |
|`Ctrl` + `N` |  `Cmd` + `N` | New File|
|`Ctrl` + `K` -> `M` | `Cmd` + `K` -> `M` |select a language|
|`!`  `tab`|`!`  `tab`| create a basic HTML DOCTYPE structure|
|`Ctrl` + Mouse Click|`Cmd` + Mouse Click|Follow link|
|`Ctrl` + `tab` ||Switch file|
|`Ctrl` + `p` | `cmd` + `p` |select file|
|`Ctrl` + `Shift` + `P` | `cmd` + `shift` + `p`||
| `Ctrl` + `\` | `cmd` + `\` | split Vertically|
||cmd + K...M||
||cmd + L||
||cmd + /||
|Ctrl+K -> W||Close Current Panel|

可以另外安裝 [Atom Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.atom-keybindings)，其快捷鍵和原始設定不太一樣。

---

#### `Ctrl + P`  `cmd + p` select file
1. 在輸入框中輸入  `file_name` + `@` + `element/function/variable name` 可以跳到該名稱所在位置(symbols)
2.  在輸入框中輸入  `@` + `element/function/variable name` 可以跳到**目前檔案**該名稱所在位置(symbols)

---

#### `Ctrl+Shift+P`  `cmd + shift + p`  
>show command platte

---

#### `alt` + `arrow key` 可以移動目前所在的那行程式碼
>MacOS: `option` + `arrow key`

---

#### `Windows + Arrow key` 
>Windows Shortcut
可以移動 VSCode 整個介面(或其他軟體、瀏覽器) 在電腦畫面上的位置、最小化、最大化

---

#### `Ctrl` + `RightArrow` / `LeftArrow`  可以跳下一個單字

---

#### USE Emmet
>[Cheat Sheet | Emmet](https://docs.emmet.io/cheat-sheet/)

```html
    <!--nav>div>ui>li*5-->
	<nav>
        <div>
            <ui>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
                <li></li>
            </ui>
        </div>
    </nav>
```

---

####  在 JS 片段使用 emmet
`Ctrl` + `,`  **開啟設定  settings 工具  -> settings.json -> 貼上下方的  json 片段**, 這樣就可以在JS檔案中使用 Emmet，有益於VueJS, ReactJS開發
>在JS檔案中，輸入 `p` + **tab key** 會變成  `<p></p>`

```jsx
"emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "vue-html": "html",
    "plaintext": "jade"
},
"emmet.triggerExpansionOnTab": true,
```


---

####  tab, space：轉換法
##### 1. 2spaces -> 主流
>先轉定位點 **convert indentation to Tabs -> Indent Using Space: 2 -> convert indentation to Spaces**

**可以設定預設值，就不用每次開新檔案就要再設定一次**

##### 2. 4spaces
##### 3. tab
##### 4. Extension: Prettier - Code formatter
1. 開發專案中，每個人格式不一致，可使用 Prettier - Code formatter 設定存檔轉換成同一個規範格式，這樣在使用Git 版控時就不會時常發生衝突。
2. 有安裝  **Extension: [Prettier - Code formatter]( https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)**，`Ctrl` + `Shift` + `P` 輸入 `format`-> **Format Document... 文件格式化方式**
3. MacOS : `alt + shift + f` 會格式化在 prettier 中設定的格式
4. settings.json -> 加入 `"prettier.singleQuote": true`，就可以將比如 `console.log("xxx")` 轉成 `console.log('xxx')`
5. 在檔案中添加.[prettierrc.yaml 的設定檔案](https://prettier.io/docs/en/options.html)(可以設定每個人的格式化)


---

#### 專案同文字多選
1. 選取文字後，再按 `Ctrl + D` 會把選取的相同文字，逐一選取反白後，再一次一起修改
2. 選取文字後，再按 `F2` 就可以修改文字，會連同相同的文字一併修改


---

#### 程式碼片段移動
`alt` + `UpArrow` / `DownArrow` key 搬移目前該行程式碼
>MacOS: `option` + `UpArrow` / `DownArrow` key.
會跟著縮排移動

---

#### 拼字檢查
1. Extension: [Code Spelling Checker for VSCode](https://github.com/streetsidesoftware/vscode-spell-checker)


---

####  縮排辨識
1. Extension: [indent-rainbow](https://github.com/oderwat/vscode-indent-rainbow)

---

#### 為括號上色
- Extension: Braket Pair Colorizer 2 (Deprecated) - VSCode 已內建，因此這個應用程式棄用了
- 使用 **[VSocde 內建 (August 2021 (version 1.60))](https://code.visualstudio.com/updates/v1_60#_high-performance-bracket-pair-colorization)**
	- 輸入 `Ctrl + ,` 開啟設定  **File -> Preferences ->settings.json -> 加上 High performance bracket pair colorization提到的 json**

```jsx
	"editor.bracketPairColorization.enabled": true
```



- 自訂括號顏色(待補圖)
	1. settings.json 搜尋 Bracket 
	2. 找到 Editor > `Bracket Pair Colorization: Enabled`
	3. 點選 `Workbench: Color Customizations`
	4. 跳到 Color Customizations 點選 `Edit in settings.json` 
	5. 輸入 Bracket 在選單中找到 `"editorBracketHighlight.foreground1"` ~ `        "editorBracketHighlight.foreground6` 可設定六層顏色。


	
##### 為括號上色參考資料
>+ [Visual Studio Code August 2021 | High performance bracket pair colorization](https://code.visualstudio.com/updates/v1_60#_high-performance-bracket-pair-colorization)
>+ [How We Made Bracket Pair Colorization 10,000x Faster In Visual Studio Code](https://code.visualstudio.com/blogs/2021/09/29/bracket-pair-colorization)
>+ [VSCode: Bracket Pair Colorization Now Native | Justin James](https://digitaldrummerj.me/vscode-bracket-pair-colorization/)
>+ [VS Code 開啟效能提升 1 萬倍的「內建」bracket pair colorization - Code and Me](https://blog.kyomind.tw/bracket-pair-colorization/)
	
---


### Code Snippet
>兩種方式
1. 另外安裝 Extension:  [VS Code Snippet Generator](https://marketplace.visualstudio.com/items?itemName=dkultasev.vs-code-snippet-generator)
2. 使用 VsCode 內建方式，Click **Manage icon (= Gear icon at the bottom left ) -> User snippet -> javascript.json**

在`javascript.json`檔案中加入參考 Example 所做的以下 `Query Selector` 的自訂JSON片段
```jsx
// javascript.json

{
    // Place your snippets for javascript here. Each snippet is defined under a snippet name and has a prefix, body and

    // description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. Possible variables are:

    // $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. Placeholders with the

    // same ids are connected.

    // Example:
    // "Print to console": {
    //  "prefix": "log",
    //  "body": [
    //      "console.log('$1');",
    //      "$2"
    //  ],
    //  "description": "Log output to console"
    // }
	// ${1} 使用dqs + tab 會產生以下這段程式碼，${1} 會是第一個輸入文字的地方，輸入完後，再按 tab鍵，就會跳到 ${2} 再輸入變數    
	// description
	"Query Selector": {
        "prefix": "dqs",
        "body": [
            "const ${2} = document.querySelector(${1});", 
        ],

    }
}

// const productBtn1 = document.querySelector("#product1");

```


---

#### 選取片段
1. `Ctrl + Shift` + Mouse Click
2. `Ctrl + K  Ctrl + S` 開啟 Keyboard Shortcuts 或 **File -> Preferences -> Keyboard Shortcuts**
1. search `expand selection` When `editorTextFocus`
	>Shortcut: `Shift + Alt + RightArrow`

---

#### 複製片段
1. `Shift + Alt + UpArrow`   會把已複製的選取片段下方，貼上同樣片段
2. `Shift + Alt + DownArrow`  會把已複製的選取片段上方，貼上同樣片段

---

#### 片段程式碼抽取成函式
1. 選取要重構的程式碼片段，鍵盤按 `Ctrl + .` -> Extract to in global scope ->語義化命名新的 function name -> Enter (參數再局部修改)
2. 或 滑鼠按右鍵，選重構 refactor -> Extract to in global scope ->語義化命名新的function name -> Enter (參數再局部修改)


**index.html**
```html

<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <button id="product1">noodle + 1</button>
    <button id="product2">spaghetti + 1</button>
    <button id="product3">Kimchi + 1</button>


    <button id="removeProduct">移除最後一個品項</button>
    <script src="./all.js">

    </script>

</body>

</html>

```




**all.js**
```javascript
const products = [
    {
        name: "noodle",
        price: 100,
    },

    {
        name: "spaghetti",
        price: 120,
    },

    {
        name: "Kimchi",
        price: 115,
    },
];

  

let shoppingCart = [];
let total = 0;

  
  

const productBtn1 = document.querySelector("#product1");
const productBtn2 = document.querySelector("#product2");
const productBtn3 = document.querySelector("#product3");
const removeProductBtn = document.querySelector("#removeProduct");

  

productBtn1.addEventListener("click", () => {
    shoppingCart.push(products[0]);
    total = shoppingCart.reduce((pre, curr) => {
        return pre + curr.price;
    }, 0);
    console.log(shoppingCart, total);
});

  
  

productBtn2.addEventListener("click", () => {
    shoppingCart.push(products[1]);
    total = shoppingCart.reduce((pre, curr) => {
        return pre + curr.price;
    }, 0);
    console.log(shoppingCart, total);
});

  

productBtn3.addEventListener("click", () => {
    shoppingCart.push(products[2]);
    sumTotal();
});

  
  

removeProductBtn.addEventListener("click", () => {
    shoppingCart.pop();
    total = shoppingCart.reduce((pre, curr) => {
        return pre + curr.price;
    }, 0);
    console.log(shoppingCart, total);
});


```


#### **重構改成**

**index.html**
```html

<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

    <button id="product1">noodle + 1</button>
    <button id="product2">spaghetti + 1</button>
    <button id="product3">Kimchi + 1</button>
 

    <button id="removeProduct">移除最後一個品項</button>

	<!--要加上 type="module"-->	
    <script src="./all.js" type="module"></script>

</body>

</html>



```



**methods.js**
```javascript


const products = [
    {
        name: "noodle",
        price: 100,
    },

    {
        name: "spaghetti",
        price: 120,
    },

    {
        name: "Kimchi",
        price: 115,
    },
];

  

let shoppingCart = [];
let total = 0;

  
  

export function addToCart(num) {
    shoppingCart.push(products[num]);
}

  
  

export function removeFromCart() {
    shoppingCart.pop();
}

  

export function sumTotal() {
    total = shoppingCart.reduce((pre, curr) => {
        return pre + curr.price;
    }, 0);
    console.log(shoppingCart, total);
}

```




**all.js**
```javascript

import { removeFromCart, addToCart, sumTotal } from "./methods.js";
const productBtn1 = document.querySelector("#product1");
const productBtn2 = document.querySelector("#product2");
const productBtn3 = document.querySelector("#product3");
const removeProductBtn = document.querySelector("#removeProduct");

  

productBtn1.addEventListener("click", () => {
    addToCart(0);
    sumTotal(); 
});


productBtn2.addEventListener("click", () => {
    addToCart(1);
    sumTotal();
});  

productBtn3.addEventListener("click", () => {
    addToCart(2);
    sumTotal();
});
 

removeProductBtn.addEventListener("click", () => {
    removeFromCart();
    sumTotal();
});


```


---


#### 註解最佳化技巧
>**跳出提示**

**JS 文件格式註解**  -> 輸入`/` + `**` 就會自動生成
```javascript
 
// 無參數
/**
 *
 * 
 */


//有參數
/**
 *
 * @param {*} num  //此行是在 function addToCart(num) 上方生成
 */


```



```javascript

const products = [
    {
        name: "noodle",
        price: 100,
    },
    {
        name: "spaghetti",
        price: 120,
    },
    {
        name: "Kimchi",
        price: 115,
    },
];

  

let shoppingCart = [];
let total = 0;

  
  

/**
 * function add to cart~~~
 * @param {Number} num Parameter num is Product ID
 */

export function addToCart(num) {
    shoppingCart.push(products[num]);
}

  

/**
 * remove from Cart
 */

export function removeFromCart() {
    shoppingCart.pop();
}

  

export function sumTotal() {
    total = shoppingCart.reduce((pre, curr) => {
        return pre + curr.price;
    }, 0);
    console.log(shoppingCart, total);
}
```




---


#### 多層巢狀 HTML 元件重新命名

```html
    <div>
        <div>
            <div></div>
        </div>
        <div>
            <div></div>
        </div>
    </div>
    <div>
        <div>
            <div></div>
        </div>
        <div>
            <div></div>
        </div>
    </div>
```

**選取要改名的element，按 F2 改名稱，**
```html

    <div>
        <div>
            <div></div>
        </div>
        <div>
            <div></div>
        </div>
    </div>
    <div>
        <section>
            <div></div>
        </section>
        <div>
            <div></div>
        </div>
    </div>

```





### References
- [20 個 VSCode 開發小技巧，讓你 Coding 三倍速！](https://www.youtube.com/watch?v=LOjUnXk_TNU) 
- [共筆文件 | 20 個 VSCode 開發小技巧，讓你 Coding 三倍速！] https://bejewled-air-4cb.notion.site/20-VSCode-Coding-6e35278e50a0488faa027461940240f0



