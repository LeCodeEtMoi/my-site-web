+++
title = ""
description = "Systeme de pagination"
weight = 0
+++

Tuto très rapide , nous allons voir comment faire utilise un systeme de pagination avec Bulma .

Tout d'abos nous alons créé un site web avec bulma , ou nous allons lui mettre 10 articles , ici on la fleme donc on a automatiser les articles ! 

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@0.9.2/css/bulma.min.css">
  <title>Votre Page Web</title>
</head>
<body>

<section class="section">
  <div class="container">
    <h1 class="title">Bienvenue sur Votre Page Web</h1>

    <!-- Articles -->
    <div class="columns is-multiline" id="articles-container">
      <!-- Le contenu des articles sera généré ici par JavaScript -->
    </div>

    <!-- Pagination -->
    <nav class="pagination is-centered" role="navigation" aria-label="pagination">
      <a class="pagination-previous">Précédent</a>
      <a class="pagination-next">Suivant</a>
      <ul class="pagination-list">
        <!-- Utilisation d'une boucle pour générer 10 boutons de pagination -->
        <?php for ($i = 1; $i <= 10; $i++) { ?>
          <li><a class="pagination-link" aria-label="Goto page <?php echo $i; ?>" aria-current="page"><?php echo $i; ?></a></li>
        <?php } ?>
      </ul>
    </nav>
  </div>
</section>

<script>
  // Code JavaScript pour générer automatiquement 10 articles
  document.addEventListener('DOMContentLoaded', function () {
    var articlesContainer = document.getElementById('articles-container');

    for (var i = 1; i <= 10; i++) {
      var articleDiv = document.createElement('div');
      articleDiv.className = 'column is-6';

      articleDiv.innerHTML = `
        <div class="box">
          <h2 class="title is-4">Titre de l'article ${i}</h2>
          <p>Contenu succinct de l'article ${i}.</p>
        </div>
      `;

      articlesContainer.appendChild(articleDiv);
    }
  });
</script>

</body>
</html>
```
