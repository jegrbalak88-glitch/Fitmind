<!DOCTYPE html>

<html lang="ku" dir="rtl">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1">

<meta name="theme-color" content="#101010">

<title>FitMind | ستایلی تایبەت بە تۆ</title>

<style>

*{box-sizing:border-box}

body{margin:0;background:#101010;color:#f7f3ec;font-family:-apple-system,BlinkMacSystemFont,sans-serif}

header{padding:24px 20px;background:#191919;border-bottom:1px solid #333}

.logo{font-size:29px;font-weight:800;color:#d8f36a}

header p{color:#aaa;margin-bottom:0}

nav{display:flex;gap:8px;padding:12px;overflow:auto;background:#191919}

nav button,button{border:0;border-radius:12px;padding:12px 16px;background:#292929;color:white;font-size:15px;cursor:pointer}

nav button.active,.primary{background:#d8f36a;color:#171717;font-weight:bold}

main{padding:18px;max-width:680px;margin:auto}

section{display:none}

section.active{display:block}

h2{font-size:24px}

p{line-height:1.7;color:#c4c4c4}

.card{background:#1d1d1d;border:1px solid #333;border-radius:18px;padding:18px;margin:14px 0}

label{display:block;margin:14px 0 6px;color:#ddd}

input,select{width:100%;padding:13px;border:1px solid #444;border-radius:10px;background:#111;color:white;font-size:16px}

.outfit{font-size:66px;text-align:center;padding:20px;background:#26291e;border-radius:15px}

.item{display:inline-block;background:#292929;padding:9px 12px;margin:4px;border-radius:9px}

a{color:#d8f36a}

small{color:#999}

footer{text-align:center;padding:30px;color:#888}

</style>

</head>

<body>

<header>

<div class="logo">✦ FitMind</div>

<p>ستایلی تایبەت بە تۆ، هەموو ڕۆژێک.</p>

</header>

<nav>

<button class="active" onclick="show('home',this)">سەرەتا</button>

<button onclick="show('profile',this)">پرۆفایل</button>

<button onclick="show('style',this)">ئۆتفیت</button>

<button onclick="show('shop',this)">کڕین</button>

</nav>

<main>

<section id="home" class="active">

<div class="card">

<p>بەخێربێیت بۆ</p>

<h2>جوانترین شێوازی خۆت بدۆزەرەوە ✨</h2>

<p>زانیارییەکانت دابنێ و بۆ ڕۆژەکەت ستایلێک هەڵبژێرە.</p>

<button class="primary" onclick="show('style',document.querySelectorAll('nav button')[2])">دۆزینەوەی ستایل ←</button>

</div>

<div class="card">

<h2>👔 ستایلی ئەمڕۆ</h2>

<div class="outfit">👕 🧥 👖 👟</div>

<p>ساده، مۆدێرن و گونجاو بۆ ڕۆژانە.</p>

<small>ئەمە پێشنیارێکی نموونەییە؛ هێشتا AI و کەشوهەوا پەیوەست نەکراون.</small>

</div>

</section>

<section id="profile">

<h2>پرۆفایلی من</h2>

<div class="card">

<label>ناو (ئارەزوومەندانە)</label>

<input id="name" placeholder="ناوت بنووسە">

<label>ڕەگەز (ئارەزوومەندانە)</label>

<select id="gender"><option>هەڵنەبژێردراوە</option><option>نێر</option><option>مێ</option><option>ستایلی بێ سنوور</option></select>

<label>تەمەن</label>

<input id="age" type="number" placeholder="تەمەن">

<label>بەرزی (cm)</label>

<input id="height" type="number" placeholder="170">

<label>کێش (kg) - ئارەزوومەندانە</label>

<input id="weight" type="number" placeholder="65">

<label>بودجەی کڕین (£)</label>

<input id="budget" type="number" placeholder="100">

<button class="primary" onclick="saveProfile()">پاشەکەوتکردنی زانیاری</button>

<p id="saved"></p>

<small>زانیارییەکان لەم وێبگەڕەدا پاشەکەوت دەبن، نەک لە هەژمارێکی ئۆنلاین.</small>

</div>

</section>

<section id="style">

<h2>ستایلی من</h2>

<div class="card">

<label>بۆ چ بۆنەیەک؟</label>

<select id="occasion"><option>ڕۆژانە</option><option>کار و خوێندن</option><option>مهمانی</option><option>وەرزش</option><option>دەرچوون لەگەڵ هاوڕێیان</option></select>

<label>کەشوهەوا</label>

<select id="weather"><option>سارد</option><option>مامناوەند</option><option>گەرم</option><option>باراناوی</option></select>

<label>ستایلی دڵخواز</label>

<select id="vibe"><option>مۆدێرن</option><option>کلاسیک</option><option>سپۆرت</option><option>مینیمال</option><option>ستریت‌وێر</option></select>

<button class="primary" onclick="recommend()">پێشنیاری ئۆتفیت</button>

</div>

<div class="card" id="result">

<div class="outfit">🧥 👕 👖 👟</div>

<h3>ئۆتفییتی تۆ لێرە دەردەکەوێت</h3>

<p>هەڵبژاردەکانت دیاری بکە و دوگمەی پێشنیار بکە.</p>

</div>

</section>

<section id="shop">

<h2>شوێنی کڕین 🛍️</h2>

<p>بە لینکەکانی خوارەوە دەتوانیت سەردانی فرۆشگا بکەیت.</p>

<div class="card"><h3>Zara</h3><p>جلوبەرگی مۆدێرن</p><a href="https://www.zara.com/" target="_blank" rel="noopener">کردنەوەی Zara ↗</a></div>

<div class="card"><h3>ASOS</h3><p>هەڵبژاردەی جۆراوجۆر</p><a href="https://www.asos.com/" target="_blank" rel="noopener">کردنەوەی ASOS ↗</a></div>

<div class="card"><h3>UNIQLO</h3><p>جلوبەرگی سادە و ڕۆژانە</p><a href="https://www.uniqlo.com/uk/en/" target="_blank" rel="noopener">کردنەوەی UNIQLO ↗</a></div>

<div class="card"><h3>Nike</h3><p>جلوبەرگی وەرزشی</p><a href="https://www.nike.com/gb/" target="_blank" rel="noopener">کردنەوەی Nike ↗</a></div>

<small>ئەمە لینکە گشتییەکانی فرۆشگاکانن؛ کۆگا، نرخ و نوێترین بەرهەمەکان هێشتا بە سیستەمێکی زێرەکی پەیوەست نەکراون.</small>

</section>

</main>

<footer>FitMind © 2026 · ستایلەکەت، شێوازی تۆ</footer>

<script>

function show(id,btn){

document.querySelectorAll('main section').forEach(s=>s.classList.remove('active'));

document.getElementById(id).classList.add('active');

document.querySelectorAll('nav button').forEach(b=>b.classList.remove('active'));

if(btn)btn.classList.add('active');

}

function saveProfile(){

const ids=['name','gender','age','height','weight','budget'];

const data={};

ids.forEach(id=>data[id]=document.getElementById(id).value);

try{localStorage.setItem('fitmind-profile',JSON.stringify(data));

document.getElementById('saved').textContent='✓ زانیارییەکانت لەم ئامێرەدا پاشەکەوت کران.';}

catch(e){document.getElementById('saved').textContent='نەتوانرا زانیارییەکان پاشەکەوت بکرێن.';}

}

function recommend(){

const o=document.getElementById('occasion').value;

const w=document.getElementById('weather').value;

const v=document.getElementById('vibe').value;

let top='👕 تیشێرت',outer='',bottom='👖 جین',shoe='👟 پێڵاوی ڕۆژانە';

if(w==='سارد'||w==='باراناوی')outer='🧥 کۆت یان جاکێت';

if(o==='مهمانی'){top='👔 کراس';bottom='👖 پانتۆڵی جوان';shoe='👞 پێڵاوی کلاسیک';}

if(o==='وەرزش'){top='🏃 جلە وەرزشییەکان';bottom='🩳 شۆرت';shoe='👟 پێڵاوی وەرزشی';}

document.getElementById('result').innerHTML=

'<div class="outfit"> '+top+' '+outer+' '+bottom+' '+shoe+' </div>'+

'<h3>پێشنیاری ئۆتفییت</h3><p>بۆ: '+o+' · کەشوهەوا: '+w+' · ستایل: '+v+'</p>'+

'<p>'+top+'، '+(outer||'جلێکی سووک')+'، '+bottom+' و '+shoe+'.</p>'+

'<small>پێشنیارێکی سادەی ناوخۆییە؛ هێشتا AI، وێنەسازی و زانیاری کەشوهەوا چالاک نین.</small>';

}

try{

const d=JSON.parse(localStorage.getItem('fitmind-profile')||'{}');

Object.keys(d).forEach(k=>{if(document.getElementById(k))document.getElementById(k).value=d[k]});
