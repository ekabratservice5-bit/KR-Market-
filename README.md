# KR-Market-
L'objectif est de faciliter les acheteurs et vendeurs 

<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>KR MARKET - Votre marché en ligne</title>
<style>
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:#f5f6fa;color:#172033}
header{background:#101827;color:white;padding:18px;text-align:center}
header h1{margin:0;color:#f5ad25}
nav{background:white;padding:14px;text-align:center}
nav a{margin:10px;color:#172033;text-decoration:none;font-weight:bold}
.hero{background:#172033;color:white;text-align:center;padding:55px 20px}
.hero h2{font-size:32px}
.hero button,.product button{background:#f5ad25;border:0;padding:12px 20px;border-radius:6px;font-weight:bold;cursor:pointer}
.search{text-align:center;padding:25px}
.search input{width:85%;max-width:500px;padding:14px;border:1px solid #ccc;border-radius:7px}
main{max-width:1100px;margin:auto;padding:20px}
.categories,.products{display:grid;grid-template-columns:repeat(auto-fit,minmax(150px,1fr));gap:15px}
.category,.product{background:white;padding:20px;border-radius:10px;text-align:center;box-shadow:0 2px 8px #00000010}
.category{font-weight:bold}
.product .emoji{font-size:48px}
.product button{width:100%;margin-top:12px}
footer{background:#101827;color:white;text-align:center;padding:25px;margin-top:40px}
</style>
</head>
<body>

<header>
<h1>KR MARKET</h1>
<p>Votre marché en ligne</p>
</header>

<nav>
<a href="#accueil">Accueil</a>
<a href="#categories">Catégories</a>
<a href="#produits">Produits</a>
<a href="#contact">Contact</a>
</nav>

<section class="hero" id="accueil">
<h2>Achetez et vendez facilement !</h2>
<p>Découvrez des produits et rapprochez-vous des vendeurs.</p>
<button onclick="document.getElementById('produits').scrollIntoView()">Découvrir les produits</button>
</section>

<section class="search">
<input id="recherche" type="search" placeholder="Rechercher un produit..." oninput="filtrer()">
</section>

<main>
<h2 id="categories">Nos catégories</h2>
<div class="categories">
<div class="category">📱 Électronique</div>
<div class="category">👕 Mode</div>
<div class="category">🏠 Maison</div>
<div class="category">🥭 Alimentation</div>
<div class="category">🧰 Bricolage</div>
<div class="category">🧴 Beauté</div>
</div>

<h2 id="produits">Produits à découvrir</h2>
<div class="products" id="liste">
<div class="product"><div class="emoji">📱</div><h3>Téléphones</h3><p>Prix à confirmer</p><button onclick="ajouter()">Ajouter au panier</button></div>
<div class="product"><div class="emoji">👕</div><h3>Vêtements</h3><p>Prix à confirmer</p><button onclick="ajouter()">Ajouter au panier</button></div>
<div class="product"><div class="emoji">🪑</div><h3>Meubles</h3><p>Prix à confirmer</p><button onclick="ajouter()">Ajouter au panier</button></div>
<div class="product"><div class="emoji">🥭</div><h3>Produits alimentaires</h3><p>Prix à confirmer</p><button onclick="ajouter()">Ajouter au panier</button></div>
</div>
</main>

<footer id="contact">
<h3>KR MARKET</h3>
<p>Une marketplace pour tous.</p>
<p>Burkina Faso</p>
<p>© 2026 KR MARKET</p>
</footer>

<script>
let panier=0;
function ajouter(){
panier++;
alert("Article ajouté au panier de démonstration. Articles : "+panier);
}
function filtrer(){
let recherche=document.getElementById("recherche").value.toLowerCase();
document.querySelectorAll(".product").forEach(p=>{
p.style.display=p.innerText.toLowerCase().includes(recherche)?"block":"none";
});
}
</script>

</body>
</html>


