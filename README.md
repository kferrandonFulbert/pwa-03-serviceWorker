# pwa-03 PWA grace au service worker

 Maintenant que votre application de bière est opérationnelle, nous allons ajouter le service worker pour que notre
  site devienne une PWA.

## attendu 

https://kferrandonfulbert.github.io/pwa-03-serviceWorker/

## Service Worker
Le Service Worker (worker.js) fournit une mise en cache des ressources statiques pour améliorer la rapidité de chargement et permettre une utilisation hors ligne. Voici comment intégrer le Service Worker à votre projet :

- Créez le fichier Service Worker (service-worker.js):
- Copiez et collez le contenu du Service Worker fourni dans votre fichier service-worker.js.
- Ajoutez les ressources à mettre en cache:

Dans la section resourcesToCache du Service Worker, ajoutez toutes les ressources que vous souhaitez mettre en cache. Assurez-vous d'inclure le chemin correct pour chaque ressource.

## Enregistrez le Service Worker:

Dans le fichier HTML principal de votre application (probablement index.html), ajoutez le code suivant dans la balise <script>:

``` javascript 
<script>
  if ('serviceWorker' in navigator) {
    navigator.serviceWorker.register('/worker.js')
      .then(registration => {
        console.log('Service Worker enregistré avec succès.', registration);
      })
      .catch(error => {
        console.log("Erreur lors de l'enregistrement du Service Worker.", error);
      });
  }
</script>
```
Assurez-vous que le chemin vers le fichier Service Worker est correct.

- Testez l'application:

Ouvrez votre application dans le navigateur, et vérifiez la console du navigateur pour vous assurer que le Service Worker s'est enregistré avec succès.

