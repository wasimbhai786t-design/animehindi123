<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>AnimeHindi123 — Anime Discovery</title>
<meta name="description" content="AnimeHindi123 — Discover trending, popular and latest anime.">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  font-family:Arial,Helvetica,sans-serif;
  background:#070711;
  color:#fff;
  min-height:100vh;
}

/* NAVBAR */
.navbar{
  position:sticky;
  top:0;
  z-index:1000;
  background:rgba(7,7,17,.88);
  backdrop-filter:blur(15px);
  border-bottom:1px solid rgba(255,255,255,.08);
}

.nav-inner{
  max-width:1200px;
  margin:auto;
  height:70px;
  padding:0 20px;
  display:flex;
  align-items:center;
  justify-content:space-between;
}

.logo{
  font-size:25px;
  font-weight:900;
  color:#fff;
}

.logo span{
  color:#a855f7;
}

.nav-links{
  display:flex;
  gap:28px;
}

.nav-links a{
  color:#c9c9d8;
  text-decoration:none;
  font-size:14px;
  font-weight:600;
  transition:.3s;
}

.nav-links a:hover{
  color:#c084fc;
}

/* HERO */
.hero{
  min-height:520px;
  display:flex;
  align-items:center;
  position:relative;
  overflow:hidden;
  background:
    radial-gradient(circle at 80% 30%,rgba(168,85,247,.25),transparent 35%),
    radial-gradient(circle at 20% 70%,rgba(79,70,229,.18),transparent 35%);
}

.hero-inner{
  width:100%;
  max-width:1200px;
  margin:auto;
  padding:70px 20px;
}

.hero-badge{
  display:inline-block;
  padding:8px 14px;
  border:1px solid rgba(192,132,252,.4);
  background:rgba(168,85,247,.1);
  border-radius:30px;
  color:#d8b4fe;
  font-size:12px;
  margin-bottom:20px;
}

.hero h1{
  max-width:750px;
  font-size:clamp(42px,7vw,78px);
  line-height:1;
  margin-bottom:22px;
}

.hero h1 span{
  color:#a855f7;
}

.hero p{
  max-width:600px;
  color:#a9a9ba;
  font-size:17px;
  line-height:1.7;
  margin-bottom:30px;
}

.hero-buttons{
  display:flex;
  gap:12px;
  flex-wrap:wrap;
}

.btn{
  border:0;
  padding:13px 20px;
  border-radius:12px;
  text-decoration:none;
  font-weight:700;
  cursor:pointer;
}

.btn-primary{
  background:#9333ea;
  color:white;
}

.btn-primary:hover{
  background:#a855f7;
}

.btn-secondary{
  background:rgba(255,255,255,.07);
  color:white;
  border:1px solid rgba(255,255,255,.1);
}

/* MAIN */
.container{
  max-width:1200px;
  margin:auto;
  padding:70px 20px;
}

.section-head{
  display:flex;
  align-items:end;
  justify-content:space-between;
  gap:20px;
  margin-bottom:25px;
}

.section-head h2{
  font-size:30px;
}

.section-head p{
  color:#858596;
  font-size:14px;
}

/* SEARCH */
.search-box{
  display:flex;
  gap:12px;
  margin-bottom:35px;
}

.search-box input,
.search-box select{
  width:100%;
  padding:15px 16px;
  background:#11111d;
  border:1px solid #29293a;
  border-radius:12px;
  color:#fff;
  outline:none;
}

.search-box input:focus,
.search-box select:focus{
  border-color:#9333ea;
}

/* CARDS */
.grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:20px;
}

.card{
  background:#10101b;
  border:1px solid rgba(255,255,255,.07);
  border-radius:17px;
  overflow:hidden;
  transition:.35s;
}

.card:hover{
  transform:translateY(-8px);
  border-color:rgba(168,85,247,.55);
  box-shadow:0 18px 45px rgba(0,0,0,.45);
}

.poster{
  height:285px;
  position:relative;
  overflow:hidden;
  background:#191928;
}

.poster img{
  width:100%;
  height:100%;
  object-fit:cover;
  display:block;
  transition:.5s;
}

.card:hover .poster img{
  transform:scale(1.07);
}

.poster::after{
  content:"";
  position:absolute;
  inset:0;
  background:linear-gradient(transparent 45%,rgba(0,0,0,.9));
}

.poster-title{
  position:absolute;
  left:15px;
  bottom:15px;
  z-index:2;
  font-size:19px;
  font-weight:800;
}

.rating{
  position:absolute;
  top:12px;
  right:12px;
  z-index:3;
  background:rgba(0,0,0,.7);
  padding:7px 9px;
  border-radius:8px;
  font-size:12px;
}

.card-body{
  padding:15px;
}

.card-meta{
  display:flex;
  gap:7px;
  flex-wrap:wrap;
  margin-bottom:12px;
}

.tag{
  padding:5px 8px;
  border-radius:6px;
  background:#1d1d2c;
  color:#bdbdce;
  font-size:11px;
}

.card-body p{
  color:#89899a;
  font-size:13px;
  line-height:1.5;
  margin-bottom:14px;
}

.details-btn{
  width:100%;
  padding:10px;
  border:0;
  border-radius:9px;
  background:#181827;
  color:#ddd;
  cursor:pointer;
}

.details-btn:hover{
  background:#9333ea;
  color:#fff;
}

/* FEATURE */
.feature{
  margin-top:70px;
  border:1px solid rgba(168,85,247,.2);
  border-radius:22px;
  padding:35px;
  background:
    linear-gradient(135deg,rgba(88,28,135,.18),rgba(30,27,75,.15));
}

.feature h2{
  font-size:30px;
  margin-bottom:12px;
}

.feature p{
  color:#9999aa;
  line-height:1.7;
}

/* ABOUT */
.about{
  max-width:800px;
}

.about p{
  color:#9999aa;
  line-height:1.8;
  margin-top:15px;
}

/* MODAL */
.modal{
  display:none;
  position:fixed;
  inset:0;
  z-index:2000;
  background:rgba(0,0,0,.8);
  backdrop-filter:blur(8px);
  align-items:center;
  justify-content:center;
  padding:20px;
}

.modal-box{
  width:100%;
  max-width:650px;
  max-height:90vh;
  overflow:auto;
  background:#11111d;
  border:1px solid #303044;
  border-radius:20px;
  padding:25px;
}

.close{
  float:right;
  background:#222232;
  color:#fff;
  border:0;
  width:35px;
  height:35px;
  border-radius:50%;
  cursor:pointer;
}

.modal h2{
  margin:10px 0;
  font-size:28px;
}

.modal p{
  color:#9999aa;
  line-height:1.6;
}

.episodes{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:8px;
  margin-top:20px;
}

.episode{
  padding:10px;
  border:1px solid #29293a;
  background:#191927;
  color:#ddd;
  border-radius:8px;
  cursor:pointer;
}

.episode:hover{
  background:#9333ea;
}

/* FOOTER */
footer{
  border-top:1px solid rgba(255,255,255,.07);
  padding:35px 20px;
  text-align:center;
  color:#666678;
  font-size:13px;
}

/* MOBILE */
@media(max-width:900px){
  .grid{
    grid-template-columns:repeat(2,1fr);
  }

  .nav-links{
    display:none;
  }
}

@media(max-width:600px){
  .hero{
    min-height:500px;
  }

  .hero h1{
    font-size:48px;
  }

  .search-box{
    flex-direction:column;
  }

  .grid{
    grid-template-columns:repeat(2,1fr);
    gap:12px;
  }

  .poster{
    height:240px;
  }

  .card-body{
    padding:11px;
  }

  .section-head{
    display:block;
  }

  .section-head p{
    margin-top:7px;
  }

  .episodes{
    grid-template-columns:repeat(3,1fr);
  }
}

@media(max-width:380px){
  .grid{
    grid-template-columns:1fr;
  }
}
</style>
</head>

<body>

<header class="navbar">
  <div class="nav-inner">
    <div class="logo">Anime<span>Hindi123</span></div>

    <nav class="nav-links">
      <a href="#home">Home</a>
      <a href="#popular">Popular</a>
      <a href="#latest">Latest</a>
      <a href="#about">About</a>
    </nav>
  </div>
</header>

<section class="hero" id="home">
  <div class="hero-inner">
    <div class="hero-badge">✦ PREMIUM ANIME DISCOVERY</div>

    <h1>Discover Your Next <span>Anime.</span></h1>

    <p>
      Explore popular, trending and latest anime titles in one beautiful
      anime discovery experience.
    </p>

    <div class="hero-buttons">
      <a class="btn btn-primary" href="#popular">Explore Anime</a>
      <a class="btn btn-secondary" href="#latest">Latest Releases</a>
    </div>
  </div>
</section>

<main class="container">

<section id="popular">

<div class="section-head">
  <div>
    <h2>🔥 Popular Anime</h2>
    <p>Fan-favorite anime worth watching</p>
  </div>
</div>

<div class="search-box">
  <input id="search" type="text" placeholder="Search anime...">

  <select id="genre">
    <option value="all">All Genres</option>
    <option value="action">Action</option>
    <option value="romance">Romance</option>
    <option value="fantasy">Fantasy</option>
    <option value="adventure">Adventure</option>
    <option value="comedy">Comedy</option>
  </select>
</div>

<div class="grid" id="animeGrid">

<!-- ONE PIECE -->
<article class="card" data-title="one piece" data-genre="adventure">
  <div class="poster">
    <img src="one-piece.jpg" alt="One Piece">
    <span class="rating">⭐ 9.0</span>
    <span class="poster-title">One Piece</span>
  </div>
  <div class="card-body">
    <div class="card-meta">
      <span class="tag">Adventure</span>
      <span class="tag">Action</span>
    </div>
    <p>Monkey D. Luffy begins his legendary journey to become Pirate King.</p>
    <button class="details-btn" onclick="openAnime('One Piece')">View Details</button>
  </div>
</article>

<!-- SOLO LEVELING -->
<article class="card" data-title="solo leveling" data-genre="action">
  <div class="poster">
    <img src="solo-leveling.jpg" alt="Solo Leveling">
    <span class="rating">⭐ 8.8</span>
    <span class="poster-title">Solo Leveling</span>
  </div>
  <div class="card-body">
    <div class="card-meta">
      <span class="tag">Action</span>
      <span class="tag">Fantasy</span>
    </div>
    <p>A weak hunter discovers a mysterious system that changes his fate.</p>
    <button class="details-btn" onclick="openAnime('Solo Leveling')">View Details</button>
  </div>
</article>

<!-- ATTACK ON TITAN -->
<article class="card" data-title="attack on titan" data-genre="action">
  <div class="poster">
    <img src="attack-on-titan.jpg" alt="Attack on Titan">
    <span class="rating">⭐ 9.1</span>
    <span class="poster-title">Attack on Titan</span>
  </div>
  <div class="card-body">
    <div class="card-meta">
      <span class="tag">Action</span>
      <span class="tag">Drama</span>
    </div>
    <p>Humanity fights for survival behind enormous walls.</p>
    <button class="details-btn" onclick="openAnime('Attack on Titan')">View Details</button>
  </div>
</article>

<!-- COTE -->
<article class="card" data-title="classroom of the elite" data-genre="action">
  <div class="poster">
    <img src="classroom-of-the-elite.jpg" alt="Classroom of the Elite">
    <span class="rating">⭐ 8.4</span>
    <span class="poster-title">Classroom of the Elite</span>
  </div>
  <div class="card-body">
    <div class="card-meta">
      <span class="tag">Psychological</span>
      <span class="tag">Drama</span>
    </div>
    <p>A brilliant
