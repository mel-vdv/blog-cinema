## Welcome to GitHub
<!DOCTYPE html>
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<link rel="stylesheet" type="text/css" href="blogcine.css">
	<title>blogcine</title>
</head>

<body>
	<div id="bloc_page">
	<header>
		<div id="titre_blog_cine">
			<img src="logo_cine.jpg" alt="logo_cine"/>
			<h1> BLOG CINE  </h1>
		</br></br>
			<h2> chroniques d'une geek...</h2>
		</div>

		<nav>
			<ul>
				<li> <a href="...">FILMS  </a></li>
				<li> <a href="tableau.html">SERIES  </a></li>
			</ul>
			<img src="salle.jpg" alt="salle" id="salle"/>
		</nav>
	</header>



	<section>
		<article>
			<h1><img src="logo_netflix.png" alt="logo_netflix"> My Love</h1>
				<p>
<?php
try{
	$bdd = new PDO("mysql:host=localhost;dbname=commentaires;charset=utf8","root","");
}
catch(Exception $e)
{
	die("Erreur:".$e-> getMessage());
}
$req=$bdd-> query("SELECT*FROM liste_articles ORDER BY date_creation DESC LIMIT 0,5");

while ($donnees=$req -> fetch()) 
{
	echo $donnees["titre"]";
	echo $donnees["contenu"];
}
$req->closeCursor();

?>
</p>

		</article>
		<aside id="connexion">
			<h1> CONNECTE-TOI: </h1>
				<form method="post" action="form.php">
					<label for="pseudo"class="soulign">Pseudo: </label>
					<input type="text" name="pseudo"id="pseudo"/></br></br></br>
					<label for="pass"class="soulign">Mot de Passe: </label>
					<input type="password" name="pass"id="pass"> </br></br></br>
				</form>
			<p><a href= "form.html" title="inscription">CLIQUE ICI SI TU ES NOUVEAU</a></p>

		</aside>
		<aside id="auteure">
			<h1> A PROPOS DE L'AUTEURE:</h1>
			<p id="photo_de_mel"><img src="fotocv.jpg" alt="photo de mel"></p>
				
			<p>
				<img src="pharma_logo.png" class="flottant" alt="logo pharma">
				Vieille pharmacienne à la dérive, je pagaye tant bien que mal vers la berge, celle où les développeurs web bronzent sur des transat. </p>
			<p> Passionnée de films et de séries, j'ai décidé de jouer le rôle de celle qui ne crée rien et ne fait que critiquer le travail des autres. Soyons ensemble le mauvais Eric zemmour de la cinématosphère!</p>	
			<p> Parlons coups de coeur, parlons rires, et parlons larmes. Bienvenue sur mon blog.</p>	
			<p><a href="https://www.facebook.com/melly.vdv" title="mon profil facebook"></a><img src="logo_fb.jpg" alt="logo_fb"></a><a href="https://www.linkedin.com/in/m%C3%A9lanie-vandervaeren-1a054019b/"title="mon profil linkedin"><img src="logo_linkedin.png"alt="logo_linkedin"></a><a href="https://github.com/mel-vdv" title="mon profil github"><img src="logo_github.png" alt="github"></a><a href="mailto:melvdv@yahoo.fr" title="me contacter"><img src="contact.png"alt="contact"></a></p>
		</aside>
		<aside id="deco"> </aside>
	</section>
	<footer>
		<div id="mon_top_trois"> </div>
			<ol>MON TOP 3 :
				<li>The handmaid's tale</li>
				<li>Ozark</li>
				<li>Mommy</li>
			</ol>
		<div id="plateformes"></div>
			<ul>
				<li><a href="http://www.allocine.fr/"title="allocine"><img src="logo_allocine.png"></a></li>
				<li><a href="https://www.imdb.com/"title="IMDB"><img src="logo_imdb.png"></a></li>
				<li><a href="https://www.ocs.fr/"title="ocs"><img src="ocs_logo.jfif"></a></li>
			</ul>
	</footer>
</div>
</body>
</html>
