<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AnimeHindi123 — Hindi Dubbed Anime</title>
<meta name="description" content="AnimeHindi123 — Discover trending anime, popular series and latest releases.">

<style>
*{margin:0;padding:0;box-sizing:border-box}

:root{
 --bg:#07070d;
 --card:#11111b;
 --card2:#181827;
 --text:#fff;
 --muted:#aaaabd;
 --purple:#8b5cf6;
 --purple2:#6d28d9;
 --border:rgba(255,255,255,.08)
}

html{scroll-behavior:smooth}

body{
 font-family:Arial,Helvetica,sans-serif;
 background:
 radial-gradient(circle at 15% 10%,rgba(139,92,246,.14),transparent 28%),
 radial-gradient(circle at 85% 25%,rgba(109,40,217,.12),transparent 25%),
 var(--bg);
 color:var(--text);
 min-height:100vh
}

/* NAVBAR */
.navbar{
 position:sticky;
 top:0;
 z-index:1000;
 min-height:72px;
 display:flex;
 align-items:center;
 justify-content:space-between;
 padding:14px 6%;
 background:rgba(7,7,13,.88);
 backdrop-filter:blur(18px);
 border-bottom:1px solid var(--border);
 gap:20px
}

.logo{
 color:#fff;
 text-decoration:none;
 font-size:24px;
 font-weight:900
}

.logo span{color:var(--purple)}

.nav-links{
 display:flex;
 gap:25px;
 align-items:center
}

.nav-links a{
 color:#d8d8e5;
 text-decoration:none;
 font-size:14px;
 font-weight:700;
 transition:.25s
}

.nav-links a:hover{color:var(--purple)}

.search-box{
 display:flex;
 align-items:center;
 gap:7px
}

.search-box input{
 width:180px;
 padding:10px 14px;
 border-radius:25px;
 border:1px solid var(--border);
 outline:none;
 background:#12121d;
 color:#fff
}

.search-box button{
 width:38px;
 height:38px;
 border:0;
 border-radius:50%;
 background:var(--purple);
 color:#fff;
 cursor:pointer;
 font-size:17px
}

/* HERO */
.hero{
 min-height:520px;
 padding:90px 7%;
 display:flex;
 align-items:center;
 position:relative;
 overflow:hidden
}

.hero:before{
 content:"";
 position:absolute;
 width:500px;
 height:500px;
 border-radius:50%;
 background:rgba(139,92,246,.17);
 filter:blur(110px);
 right:-150px;
 top:20px
}

.hero-content{
 max-width:720px;
 position:relative;
 z-index:2
}

.badge{
 display:inline-block;
 padding:8px 14px;
 border-radius:20px;
 background:rgba(139,92,246,.13);
 border:1px solid rgba(139,92,246,.35);
 color:#c4a7ff;
 font-size:12px;
 font-weight:800;
 margin-bottom:20px
}

.hero h1{
 font-size:clamp(45px,7vw,78px);
 line-height:.98;
 letter-spacing:-3px;
 margin-bottom:20px
}

.hero h1 span{color:var(--purple)}

.hero p{
 max-width:600px;
 color:var(--muted);
 line-height:1.7;
 font-size:16px
}

.hero-buttons{
 display:flex;
 gap:12px;
 margin-top:30px;
 flex-wrap:wrap
}

.btn{
 display:inline-block;
 padding:13px 20px;
 border-radius:10px;
 text-decoration:none;
 border:1px solid var(--border);
 color:#fff;
 font-weight:800;
 font-size:14px;
 transition:.25s
}

.btn:hover{transform:translateY(-3px)}

.btn-primary{
 background:var(--purple);
 border-color:var(--purple)
}

.btn-primary:hover{background:var(--purple2)}

/* MAIN */
main{
 width:86%;
 max-width:1250px;
 margin:auto
}

.section{padding:45px 0}

.section-head{
 display:flex;
 justify-content:space-between;
 align-items:center;
 margin-bottom:22px
}

.section-head h2{font-size:26px}

.section-head span{
 color:#9999aa;
 font-size:13px
}

/* CARDS */
.grid{
 display:grid;
 grid-template-columns:repeat(5,1fr);
 gap:18px
}

.card{
 background:linear-gradient(145deg,var(--card),var(--card2));
 border:1px solid var(--border);
 border-radius:15px;
 overflow:hidden;
 cursor:pointer;
 transition:.3s ease
}

.card:hover{
 transform:translateY(-7px);
 border-color:rgba(139,92,246,.55);
 box-shadow:0 18px 45px rgba(0,0,0,.4)
}

.poster{
 height:270px;
 position:relative;
 overflow:hidden;
 display:flex;
 align-items:center;
 justify-content:center;
 background:linear-gradient(145deg,#21144a,#090912)
}

.poster:after{
 content:"ANIME";
 font-size:30px;
 font-weight:900;
 color:rgba(255,255,255,.12);
 letter-spacing:4px
}

.poster.one{background:linear-gradient(145deg,#40145e,#12091c)}
.poster.two{background:linear-gradient(145deg,#102e5c,#080d1b)}
.poster.three{background:linear-gradient(145deg,#5a2114,#170907)}
.poster.four{background:linear-gradient(145deg,#14523d,#07140f)}
.poster.five{background:linear-gradient(145deg,#38205c,#0d0917)}

.tag{
 position:absolute;
 left:10px;
 top:10px;
 padding:5px 8px;
 border-radius:6px;
 background:var(--purple);
 font-size:10px;
 font-weight:900
}

.card-info{padding:13px}

.card-info h3{
 font-size:15px;
 margin-bottom:6px;
 white-space:nowrap;
 overflow:hidden;
 text-overflow:ellipsis
}

.meta{
 color:#9898aa;
 font-size:12px
}

/* GENRES */
.genres{
 display:flex;
 flex-wrap:wrap;
 gap:10px
}

.genre{
 padding:11px 16px;
 border-radius:25px;
 background:#11111b;
 border:1px solid var(--border);
 color:#c9c9d6;
 font-size:13px;
 cursor:pointer;
 transition:.25s
}

.genre:hover{
 background:var(--purple);
 color:#fff;
 border-color:var(--purple);
 transform:translateY(-2px)
}

/* FOOTER */
footer{
 margin-top:50px;
 border-top:1px solid var(--border);
 padding:35px 7%;
 text-align:center;
 color:#888899;
 font-size:13px
}

footer strong{color:#fff}

/* MODAL */
.modal{
 position:fixed;
 inset:0;
 z-index:2000;
 background:rgba(0,0,0,.78);
 backdrop-filter:blur(8px);
 display:none;
 align-items:center;
 justify-content:center;
 padding:20px
}

.modal.active{display:flex}

.modal-box{
 width:100%;
 max-width:600px;
 background:#11111b;
 border:1px solid var(--border);
 border-radius:20px;
 padding:30px;
 position:relative;
 animation:pop .25s ease
}

@keyframes pop{
 from{transform:scale(.94);opacity:0}
 to{transform:scale(1);opacity:1}
}

.close{
 position:absolute;
 right:18px;
 top:13px;
 background:none;
 border:0;
 color:#fff;
 font-size:27px;
 cursor:pointer
}

.modal-box h2{
 font-size:29px;
 margin-bottom:10px
}

.modal-box p{
 color:#aaaabd;
 line-height:1.7;
 font-size:14px
}

/* SEARCH */
.no-results{
 display:none;
 text-align:center;
 padding:50px 10px;
 color:#9999aa
}

/* RESPONSIVE */
@media(max-width:1000px){
 .grid{grid-template-columns:repeat(3,1fr)}
 .poster{height:240px}
}

@media(max-width:700px){
 .navbar{
  min-height:68px;
  padding:13px 5%;
  flex-wrap:wrap
 }

 .nav-links{
  order:3;
  width:100%;
  justify-content:center;
  gap:17px;
  overflow:auto
 }

 .search-box input{width:130px}

 .hero{
  min-height:450px;
  padding:65px 7%
 }

 .hero h1{letter-spacing:-2px}

 main{width:90%}

 .grid{
  grid-template-columns:repeat(2,1fr);
  gap:13px
 }

 .poster{height:220px}

 .section{padding:32px 0}
}

@media(max-width:420px){
 .logo{font-size:20px}
 .search-box input{width:105px}
 .hero h1{font-size:42px}
 .poster{height:190px}
 .card-info h3{font-size:13px}
}
</style>
</head>

<body>

<header class="navbar">

<a href="#home" class="logo">
Anime<span>Hindi123</span>
</a>

<nav class="nav-links">
<a href="#home">Home</a>
<a href="#anime">Anime</a>
<a href="#genres">Genres</a>
<a href="#popular">Popular</a>
</nav>

<div class="search-box">
<input id="searchInput" type="search" placeholder="Search anime...">
<button onclick="searchAnime()">⌕</button>
</div>

</header>

<section class="hero" id="home">

<div class="hero-content">

<span class="badge">🇮🇳 HINDI DUBBED ANIME</span>

<h1>
Anime.<br>
<span>Your Way.</span>
</h1>

<p>
Discover trending anime, popular series and your next favourite
adventure — all in one clean and modern anime hub.
</p>

<div class="hero-buttons">
<a href="#anime" class="btn btn-primary">Explore Anime →</a>
<a href="#popular" class="btn">Popular Now</a>
</div>

</div>
</section>

<main>

<section class="section" id="anime">

<div class="section-head">
<h2>🔥 Trending Anime</h2>
<span>Popular right now</span>
</div>

<div class="grid anime-grid">

<article class="card" data-title="Demon Slayer">
<div class="poster one">
<span class="tag">HD</span>
</div>
<div class="card-info">
<h3>Demon Slayer</h3>
<div class="meta">Action • Fantasy • Hindi</div>
</div>
</article>

<article class="card" data-title="Attack on Titan">
<div class="poster two">
<span class="tag">HD</span>
</div>
<div class="card-info">
<h3>Attack on Titan</h3>
<div class="meta">Action • Drama • Hindi</div>
</div>
</article>

<article class="card" data-title="Jujutsu Kaisen">
<div class="poster three">
<span class="tag">NEW</span>
</div>
<div class="card-info">
<h3>Jujutsu Kaisen</h3>
<div class="meta">Action • Supernatural</div>
</div>
</article>

<article class="card" data-title="One Piece">
<div class="poster four">
<span class="tag">HD</span>
</div>
<div class="card-info">
<h3>One Piece</h3>
<div class="meta">Adventure • Fantasy</div>
</div>
</article>

<article class="card" data-title="Solo Leveling">
<div class="poster five">
<span class="tag">NEW</span>
</div>
<div class="card-info">
<h3>Solo Leveling</h3>
<div class="meta">Action • Fantasy</div>
</div>
</article>

</div>

<div class="no-results" id="noResults">
No anime found. Try another search.
</div>

</section>

<section class="section" id="popular">

<div class="section-head">
<h2>⭐ Popular Picks</h2>
<span>Fan favourites</span>
</div>

<div class="grid">

<article class="card" data-title="Naruto">
<div class="poster two"></div>
<div class="card-info">
<h3>Naruto</h3>
<div class="meta">Action • Adventure</div>
</div>
</article>

<article class="card" data-title="Dragon Ball">
<div class="poster three"></div>
<div class="card-info">
<h3>Dragon Ball</h3>
<div class="meta">Action • Shonen</div>
</div>
</article>

<article class="card" data-title="Vinland Saga">
<div class="poster five"></div>
<div class="card-info">
<h3>Vinland Saga</h3>
<div class="meta">Drama • Historical</div>
</div>
</article>

<article class="card" data-title="Pokemon">
<div class="poster four"></div>
<div class="card-info">
<h3>Pokémon</h3>
<div class="meta">Adventure • Family</div>
</div>
</article>

<article class="card" data-title="My Hero Academia">
<div class="poster one"></div>
<div class="card-info">
<h3>My Hero Academia</h3>
<div class="meta">Action • Superhero</div>
</div>
</article>

</div>
</section>

<section class="section" id="genres">

<div class="section-head">
<h2>🎭 Browse Genres</h2>
<span>Find your mood</span>
</div>

<div class="genres">

<div class="genre">Action</div>
<div class="genre">Adventure</div>
<div class="genre">Romance</div>
<div class="genre">Comedy</div>
<div class="genre">Fantasy</div>
<div class="genre">Drama</div>
<div class="genre">Psychological</div>
<div class="genre">School</div>
<div class="genre">Shonen</div>
<div class="genre">Slice of Life</div>

</div>
</section>

</main>

<footer>

<p>
<strong>AnimeHindi123</strong> — Your Anime Discovery Hub
</p>

<p style="margin-top:8px">
© 2026 AnimeHindi123. Built with passion for anime fans.
</p>

</footer>

<div class="modal" id="modal">

<div class="modal-box">

<button class="close" onclick="closeModal()">×</button>

<h2 id="modalTitle">Anime</h2>

<p>
Welcome to AnimeHindi123. This is an anime information page.
Add your own legal links, descriptions and official streaming
destinations here.
</p>

<div style="margin-top:20px">
<a href="#anime" class="btn btn-primary" onclick="closeModal()">
← Back to Anime
</a>
</div>

</div>
</div>

<script>

const input=document.getElementById("searchInput");
const cards=document.querySelectorAll(".card");
const noResults=document.getElementById("noResults");

const modal=document.getElementById("modal");
const modalTitle=document.getElementById("modalTitle");

function searchAnime(){

 const value=input.value.toLowerCase().trim();

 let found=0;

 cards.forEach(card=>{

  const title=card.dataset.title.toLowerCase();

  if(!value || title.includes(value)){
   card.style.display="";
   found++;
  }else{
   card.style.display="none";
  }

 });

 noResults.style.display=found ? "none" : "block";

 document.getElementById("anime").scrollIntoView({
  behavior:"smooth"
 });

}

input.addEventListener("input",()=>{

 if(input.value.trim()===""){

  cards.forEach(card=>{
   card.style.display="";
  });

  noResults.style.display="none";
 }

});

cards.forEach(card=>{

 card.addEventListener("click",()=>{

  modalTitle.textContent=card.dataset.title;

  modal.classList.add("active");

 });

});

function closeModal(){
 modal.classList.remove("active");
}

modal.addEventListener("click",(e)=>{

 if(e.target===modal){
  closeModal();
 }

});

</script>

</body>
</html>
