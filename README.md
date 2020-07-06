# my-test-repo
# 日常记录用测试型仓库
  [My blog](http://blog.csdn.net/archiewade "点击跳转")<br><br>
# Model-menu-slider
## html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="x-ua-compatible" content="id=edge">
    <!--  link或script中的 integrity 属性：为了防止 CDN 篡改 javascript 用的  -->
    <!-- cloudflare是部署在国外的一个免费CDN服务平台 -->
<!--    <link-->
<!--            rel="stylesheet"-->
<!--            href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.min.css"-->
<!--            integrity="sha256-+N4/V/SbAFiW1MPBCXnfnP9QSN3+Keu+NlB+0ev/YKQ="-->
<!--            crossorigin="anonymous"-->
<!--    />-->
    <link rel="stylesheet" href="menu.css">
    <title>登录界面</title>
</head>
<body>
<!-- 导航栏 -->
<nav id="navbar">
    <div class="logo">
<!--        <img src="https://randomuser.me/api/portraits/men/76.jpg" alt="user">-->
        <img src="huawei_logo.png" alt="user">
    </div>
    <ul>
        <li><a href="#" name="Home">主页</a></li>
        <li><a href="#" name="Portfolio">作品集</a></li>
        <li><a href="#" name="Blog">博客</a></li>
        <li><a href="#" name="Contaction">联系我</a></li>
    </ul>
</nav>
<!-- 内容头部 -->
<header>
    <button id="toggle" class="toggle">
        <i class="fa fa-bar fa-2x"></i>
    </button>
    <h1>登录界面</h1>
    <p>学而不思则罔，思而不学则殆</p>

    <button class="cta-btn" id="open">登录</button>
</header>

<div class="container">
    <h2>本页面简介</h2>
    <p>
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa
        aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa.
    </p>
    <p>
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbb
        bbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb
        bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb.
    </p>

    <h2>和我交流</h2>
    <p>ccccccccccccccccccccccccccccccc
    ccccccccccccccccccccccccccccccccccccc
    cccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccc
    cccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccccc
    </p>

    <h2>Benefits</h2>
    <ul>
        <li>Lifetime Access</li>
        <li>30 Day Money Back</li>
        <li>Tailored Customer Support</li>
    </ul>

    <p></p>
</div>

<!-- Model -->
<div class="model-container" id="model">
    <div class="model">
        <button class="close-btn" id="close">
            <i class="fa fa-times"></i>
        </button>
        <div class="model-header">
            <h3>登入</h3>
        </div>
        <div class="model-content">
            <p>通过注册可以获得更多帮助和信息
            <form class="model-form">
                <div>
                    <label for="name">Name</label>
                    <input type="text" id="name" class="form-input" placeholder="请输入...">
                </div>
                <div>
                    <label for="email">Email</label>
                    <input type="email" id="email" class="form-input" placeholder="请输入...">
                </div>
                <div>
                    <label for="pwd">Password</label>
                    <input type="password" id="pwd" class="form-input" placeholder="请输入...">
                </div>
                <div>
                    <label for="pwd2">Password2</label>
                    <input type="password" id="pwd2" class="form-input" placeholder="请输入...">
                </div>
                <input type="submit" value="Submit" class="submit-btn">
            </form>
            </p>
        </div>
    </div>
</div>
<script src="menu.js"></script>
</body>
</html>
```

## css
``` (css)
@import url('https://fonts.googleapis.com/css?family=Lato&display=swap');

:root {
    --model-duration: 1s;
    --primary-color: #30336b;
    --secondary-color: #be2edd;
}

* {
    box-sizing: border-box;
}

body {
    font-family: 'Lato', sans-serif;
    margin: 0;
    transition: transform 0.3s ease;
}

body.show-nav {
    transform: translateX(200px);
}

nav {
    background-color: var( --primary-color);
    border-right: 2px solid rgba(200, 200, 200, 0.1);
    color: #f0f0f0;
    position: fixed;
    top: 0;
    left: 0;
    width: 200px;
    height: 100%;
    z-index: 100;
    transform: translateX(-100%);
}

nav .logo {
    padding: 30px 0;
    text-align: center;
}

nav .logo img {
    height: 75px;
    width: 75px;
    border-radius: 50%;
}

nav ul {
    padding: 0;
    list-style-type: none;
    margin: 0;
}

nav ul li {
    border-bottom: 2px solid rgba(200, 200, 200, 0.1);
    padding: 20px;
}

nav ul li:first-of-type {
    border-top: 2px solid rgba(200, 200, 200, 0.1);
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

nav ul li a:hover {
    text-decoration: underline;
}

header {
    background-color: var(--primary-color);
    color: #fff;
    font-size: 130%;
    position: relative;
    padding: 40px 15px;
    text-align: center;
}

header h1 {
    margin: 0;
}

header p {
    margin: 30px 0;
}

button,
input[type='submit'] {
    background-color: var(--secondary-color);
    border: 0;
    border-radius: 5px;
    color: #fff;
    cursor: pointer;
    padding: 8px 12px;
}

button:focus {
    outline: none;
}

.toggle {
    background-color: rgba(0, 0, 0, 0.3);
    position: absolute;
    top: 20px;
    left: 20px;
}

.cta-btn {
    padding: 12px 30px;
    font-size: 20px;
}

.container {
    padding: 15px;
    margin: 0 auto;
    max-width: 100%;
    width: 800px;
}

.model-container {
    background-color: rgba(0, 0, 0, 0.6);
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
}

.model-container.show-model {
    display: block;
}

.model {
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    position: absolute;
    overflow: hidden;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    max-width: 100%;
    width: 400px;
    animation-name: modelopen;
    animation-duration: var(--model-duration);
}

.model-header {
    background: var(--primary-color);
    color: #fff;
    padding: 15px;
}

.model-header h3 {
    margin: 0;
    border-bottom: 1px solid #333;
}

.model-content {
    padding: 20px;
}

.model-form div {
    margin: 15px 0;
}

.model-form label {
    display: block;
    margin-bottom: 5px;
}

.model-form .form-input {
    padding: 8px;
    width: 100%;
}

.close-btn {
    background: transparent;
    font-size: 25px;
    position: absolute;
    top: 0;
    right: 0;
}

@keyframes modelopen {
    from {
        opacity: 0;
    }

    to {
        opacity: 1;
    }
}
```

## js
```
const toggle = document.getElementById('toggle');
const close = document.getElementById('close');
const open = document.getElementById('open');
const model = document.getElementById('model');
const navbar = document.getElementById('navbar');

function closeNavbar(e) {
    if (document.body.classList.contains('show-nav') &&
        e.target !== toggle && !toggle.contains(e.target) &&
        e.target !== navbar && !navbar.contains(e.target)) {
        document.body.classList.toggle('show-nav');
        document.body.removeEventListener('click', closeNavbar);
    } else if (!document.body.classList.contains('show-nav')) {
        document.body.removeEventListener('click', closeNavbar);
    }
}

// 切换导航栏
toggle.addEventListener('click', () => {
    document.body.classList.toggle('show-nav');
    document.body.addEventListener('click', closeNavbar);
});

// 展示登录模型块
open.addEventListener('click', () => model.classList.add('show-model'));

// 隐藏登录模型块
close.addEventListener('click', () => model.classList.remove('show-model'));

// 通过块外点击实现隐藏登录模型块
window.addEventListener('click', e =>
    e.target == model ? model.classList.remove('show-model') : false
)
;
```

# 排行确认
##HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="x-ua-compatible" content="ie=egde">
    <title>十大富豪</title>
    <link rel="stylesheet" href="list.css">
    <script src="https://kit.fontawesome.com/3da1a747b2.js" crossorigin="anonymous"></script>
</head>
<body>
<h1>10 Richest People</h1>
<p>将人员拖放到相应的位置</p>
<ul class="draggable-list" id="draggable-list"></ul>
<button class="check-btn" id="check">
    Check Order
    <i class="fas fa-paper-plane"></i>
</button>

<script src="list.js"></script>
</body>
</html>
```
#CSS
```
@import url('http://fonts.googleapis.com/css?family=Lato&display=swap');

:root {
    --border-color: #e2e5e4;
    --background-color: #c3c7ca;
    --text-color: #35444f
}

* {
    box-sizing: border-box;
}

body {
    background-color: #f0f0f0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    height: 100vh;
    margin: 0;
    font-family: 'Lato', sans-serif;
}

.draggable-list {
    border: 1px solid var(--border-color);
    color: var(--text-color);
    padding: 0;
    list-style-type: none;
}

.draggable-list li {
    background-color: #fff;
    display: flex;
    flex: 1;
}

.draggable-list li:not(:last-of-type) {
    border-bottom: 1px solid var(--border-color);
}

.draggable-list .number {
    background-color: var(--background-color);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 28px;
    height: 60px;
    width: 60px;
}

.draggable-list li.over .draggable {
    background-color: #eaeaea;
}

.draggable-list .person-name {
    margin: 0 20px 0 0;
}

.draggable-list li.right .person-name {
    color: #3ae374;
}

.draggable-list li.wrong .person-name {
    color: #ff3838;
}

.draggable {
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 15px;
    flex: 1;
}

.check-btn {
    background-color: var(--background-color);
    border: none;
    color: var(--text-color);
    font-size: 16px;
    padding: 10px 20px;
    cursor: pointer;
}

.check-btn:active {
    transform: scale(0.98);
}

.check-btn:focus {
    outline: none;
}
```
#JS
```
const draggable_list = document.getElementById('draggable-list');
const check = document.getElementById('check');

const richestPeople = [
    'Jeff Bezos',
    'Bill Gates',
    'Warren Buffett',
    'Bernard Arnault',
    'Carlos Slim Helu',
    'Amancio Ortega',
    'Larry Ellison',
    'Mark Zuckerberg',
    'Michael Bloomberg',
    'Larry Page'
];

// 存储人员项
const listItems = [];

let dragStartIndex;

createList();

// Insert list items into DOM
function createList() {
    [...richestPeople]
        .map(a => ({ value: a, sort: Math.random() }))
        .sort((a, b) => a.sort - b.sort)
        .map(a => a.value)
        .forEach((person, index) => {
            const listItem = document.createElement('li');

            listItem.setAttribute('data-index', index);

            listItem.innerHTML = `
        <span class="number">${index + 1}</span>
        <div class="draggable" draggable="true">
          <p class="person-name">${person}</p>
          <i class="fas fa-grip-lines"></i>
        </div>
      `;

            listItems.push(listItem);

            draggable_list.appendChild(listItem);
        });

    addEventListeners();
}

function dragStart() {
    // console.log('Event: ', 'dragstart');
    dragStartIndex = +this.closest('li').getAttribute('data-index');
}

function dragEnter() {
    // console.log('Event: ', 'dragenter');
    this.classList.add('over');
}

function dragLeave() {
    // console.log('Event: ', 'dragleave');
    this.classList.remove('over');
}

function dragOver(e) {
    // console.log('Event: ', 'dragover');
    e.preventDefault();
}

function dragDrop() {
    // console.log('Event: ', 'drop');
    const dragEndIndex = +this.getAttribute('data-index');
    swapItems(dragStartIndex, dragEndIndex);

    this.classList.remove('over');
}

// Swap list items that are drag and drop
function swapItems(fromIndex, toIndex) {
    const itemOne = listItems[fromIndex].querySelector('.draggable');
    const itemTwo = listItems[toIndex].querySelector('.draggable');

    listItems[fromIndex].appendChild(itemTwo);
    listItems[toIndex].appendChild(itemOne);
}

// Check the order of list items
function checkOrder() {
    listItems.forEach((listItem, index) => {
        const personName = listItem.querySelector('.draggable').innerText.trim();

        if (personName !== richestPeople[index]) {
            listItem.classList.add('wrong');
        } else {
            listItem.classList.remove('wrong');
            listItem.classList.add('right');
        }
    });
}

function addEventListeners() {
    const draggables = document.querySelectorAll('.draggable');
    const dragListItems = document.querySelectorAll('.draggable-list li');

    draggables.forEach(draggable => {
        draggable.addEventListener('dragstart', dragStart);
    });

    dragListItems.forEach(item => {
        item.addEventListener('dragover', dragOver);
        item.addEventListener('drop', dragDrop);
        item.addEventListener('dragenter', dragEnter);
        item.addEventListener('dragleave', dragLeave);
    });
}

check.addEventListener('click', checkOrder);

```
# 歌词搜索
## HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="x-ua-compatible" content="ie=edge">
    <link rel="stylesheet" href="lyrics.css">
    <title>歌词搜索</title>
</head>
<body>
    <header>
        <h1>歌词搜索</h1>
        <input type="text" id="search" placeholder="请输入短文或歌名">
        <button>Search</button>
    </header>

    <div id="result" class="container">
        <p>结果展示如下</p>
    </div>

    <div id="more" class="container centered"></div>
</body>
</html>
```
## CSS
```
* {
    box-sizing: border-box;
}

body {
    background-color: #fff;
    font-family: Arial, Helvetica, sans-serif;
    margin: 0;
}

button {
    cursor: pointer;
}

button:active {
    transform: scale(0.95); /* 缩放函数，param1-水平缩放值，param2-垂直缩放值 */
}

/*对于很多元素来说，如果没有设置样式，轮廓是不可见的。
因为样式（style）的默认值是 none。
但 input 元素是例外，其样式默认值由浏览器决定。*/
input:focus,
button:focus {
    outline: none; /* 文本框和按钮获得焦点时，去除轮廓 */
}

header {
    /* background-image 属性用于为一个元素设置一个或者多个背景图像 ，第一个图像“最接近用户” */
    background-image: url('https://images.unsplash.com/photo-1510915361894-db8b60106cb1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80');
    /* 图像不会被重复. 那个没有被重复的背景图像的位置是由background-position属性来决定. */
    background-repeat: no-repeat;
    /* 将原图像缩放，直到能完全覆盖背景区域 */
    background-size: cover;
    background-position: center center;
    color: #fff;
    display: flex;
    /* flex容器的主轴和块轴相同。主轴起点与主轴终点和书写模式的前后点相同 */
    flex-direction: column;
    /* 元素在侧轴居中。如果元素在侧轴上的高度高于其容器，那么在两个方向上溢出距离相同。 */
    align-items: center;
    /* 伸缩元素向每行中点排列。每行第一个元素到行首的距离将与每行最后一个元素到行尾的距离相同。 */
    justify-content: center;
    padding: 100px 0;
    position: relative;
}

header::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    background-color: rgba(0, 0, 0, 0.4);
}

header * {
    z-index: 1;
}

header h1 {
    margin: 0 0 30px;
}

form {
    position: relative;
    width: 500px;
    max-width: 100%;
}

form input {
    border: 0;
    border-radius: 50px;
    font-size: 16px;
    padding: 15px 30px;
    width: 100%;
}

form button {
    position: absolute;
    top: 2px;
    right: 2px;
    background-color: #e056fd;
    border: 0;
    border-radius: 50px;
    color: #fff;
    font-size: 16px;
    padding: 13px 30px;
}

.btn {
    background-color: #8d56fd;
    border: 0;
    border-radius: 10px;
    color: #fff;
    padding: 4px 10px;
}

ul.songs {
    list-style-type: none;
    padding: 0;
}

ul.songs li {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin: 10px 0;
}

.container {
    margin: 30px auto;
    max-width: 100%;
    width: 500px;
}

.container h2 {
    font-weight: 300;
}

.container p {
    text-align: center;
}

.centered {
    display: flex;
    justify-content: center;
}

.centered button {
    transform: scale(1.3);
    margin: 15px;
}

```
## JS
```
const form = document.getElementById('form');
const search = document.getElementById('search');
const result = document.getElementById('result');
const more = document.getElementById('more');

const apiURL = 'https://api.lyrics.ovh';

// Search by song or artist
async function searchSongs(term) {
    const res = await fetch(`${apiURL}/suggest/${term}`);
    const data = await res.json();

    showData(data);
}

// Show song and artist in DOM
function showData(data) {
    result.innerHTML = `
    <ul class="songs">
      ${data.data
        .map(
            song => `<li>
      <span><strong>${song.artist.name}</strong> - ${song.title}</span>
      <button class="btn" data-artist="${song.artist.name}" data-songtitle="${song.title}">Get Lyrics</button>
    </li>`
        )
        .join('')}
    </ul>
  `;

    if (data.prev || data.next) {
        more.innerHTML = `
      ${
            data.prev
                ? `<button class="btn" onclick="getMoreSongs('${data.prev}')">Prev</button>`
                : ''
        }
      ${
            data.next
                ? `<button class="btn" onclick="getMoreSongs('${data.next}')">Next</button>`
                : ''
        }
    `;
    } else {
        more.innerHTML = '';
    }
}

// Get prev and next songs
async function getMoreSongs(url) {
    const res = await fetch(`https://cors-anywhere.herokuapp.com/${url}`);
    const data = await res.json();

    showData(data);
}

// Get lyrics for song
async function getLyrics(artist, songTitle) {
    const res = await fetch(`${apiURL}/v1/${artist}/${songTitle}`);
    const data = await res.json();

    if (data.error) {
        result.innerHTML = data.error;
    } else {
        const lyrics = data.lyrics.replace(/(\r\n|\r|\n)/g, '<br>');

        result.innerHTML = `
            <h2><strong>${artist}</strong> - ${songTitle}</h2>
            <span>${lyrics}</span>
        `;
    }

    more.innerHTML = '';
}

// Event listeners
form.addEventListener('submit', e => {
    e.preventDefault();

    const searchTerm = search.value.trim();

    if (!searchTerm) {
        alert('Please type in a search term');
    } else {
        searchSongs(searchTerm);
    }
});

// Get lyrics button click
result.addEventListener('click', e => {
    const clickedEl = e.target;

    if (clickedEl.tagName === 'BUTTON') {
        const artist = clickedEl.getAttribute('data-artist');
        const songTitle = clickedEl.getAttribute('data-songtitle');

        getLyrics(artist, songTitle);
    }
});

```
