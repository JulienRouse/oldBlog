## CodeReview Quest summary ##

### Préambule ###
Cet article est la suite d'un article que j'avais écrit début janvier. C'est probablement plus facile de lire l'article d'aujourd'hui en ayant lu celui auquel il se réfère (ou de le relire pour se le remettre en mémoire). Tu peux lire cet article [ici](http://www.julienrouse.com/template/articles/fr/2018-01-06_StackExchange_codereview_quest.html) en français (ou [ici](http://www.julienrouse.com/template/articles/en/2018-01-06_StackExchange_codereview_quest.html) en anglais).

### Résultats ###

J'ai écrit **5** revues de code du 6 janvier au 6 février: (toutes les revues sont en anglais)

- [Implémentation d'une pile en Python](https://codereview.stackexchange.com/a/184444/87312) 
- [Implémentation du Jeu de la Vie de Conway en Java](https://codereview.stackexchange.com/a/184519/87312)
- [Un programme qui calcule des points d'expérience pour des personnages de jeux de rôles en Java](https://codereview.stackexchange.com/a/185096/87312)
- [Un algorithme qui enlève certaines occurrences des éléments d'un tableau](https://codereview.stackexchange.com/a/185247/87312)
- [Utilitaire de validation pour des schémas JSON](https://codereview.stackexchange.com/a/185423/87312)

Au moment où j'écris, trois de ces postes ont eu 0 vote positif, un a eu 3 votes positifs et le dernier a eu 5 votes positifs. Sur StackExchange, une réponse est considérée un "top post"(littéralement "super article/réponse") à partir de 5 votes positifs. C'est-à-dire qu'une de mes réponses peut être considéré comme très bonne, une est correcte mais sans plus et les trois autres autres sont considérées sans importance(ces trois réponses ont été vues par un peu moins de 50personnes mais aucunes n'a voté en leur faveur).

### Interprétation de ces revues ###

Pour la revue en Python, cela faisait un bon moment que je n'avais pas codé en Python de manière significative, donc je me suis concentré dans la revue sur le style. J'ai également pu écrire sur les similitudes et différences entre le `self` de Python et le `this` de Java. Je devrais très certainement coder plus en Python avant de refaire des revues, à part des codes de débutant. Faire cette revue m'a forcé à revoir les **PEP** (*Python Enhancement Proposals*, ou Propositions d'améliorations pour Python) surs comment rendre son code conforme au style standard de Python. En particulier [**PEP8**](https://www.python.org/dev/peps/pep-0008/) qui est le guide officiel sur les questions de style, indentation, etc., et [**PEP257**](https://www.python.org/dev/peps/pep-0257/) qui lui est le guide concernant la documentation. Ces documents sont principalement des conventions, pas des règles absolues, mais dans l'écosystème Pythons ces conventions sont très respectées et c'est un bon point de les connaitre. Il existe des linter(des programmes qui corrigent les non-respects de ces conventions) pour aider à transformer son code dans le respect du standard. (Par exemple [PyLint](https://www.pylint.org/) qui est un linter mais pas seulement. Il s'intègre dans plusieurs IDE, génère des diagrammes UML, détection d'erreur commune, etc.). 

Cette revue m'a permis de me remémorer des bonnes pratiques, et également le fait que je suis un peu "rouillé" en Python. Je devrais m'y remettre sérieusement avant de pouvoir aider d'autres codeurs chevronnés.

Pour les revues sur le Java, il y a eu du bon et du moins bon. J'ai corrigé des erreurs de nommage, de répétition de code, ai pu discuter de l'utilisation des `Exception`, l'utilisation judicieuse de la documentation et des commentaires. Mais à chaque fois que j'ai répondu, d'autres réponses avaient des remarques très pertinentes sur la manière de résoudre le problème, la présence trop envahissante de commentaires (oui c'est possible :p) et aussi des réponses en désaccord avec ce que j'écrivais. Ce que j'en retire, c'est que des fois la manière de coder certaines fonctionnalités ou de résoudre un problème peut avoir plusieurs solutions très différentes. Aussi, il faut que je prenne du recul par rapport au code que je regarde et pense plus au problème pour ne pas louper des solutions plus élégantes/performantes/simples plutôt que d'essayer d'améliorer une solution non optimale.

Lire du code Java, et essayer de le comprendre et de l'améliorer a été dur, il faut que je continue pour améliorer mes compétences en revue de code.

### Conclusion ###

Une bonne expérience que de lire du code qui n'est pas le mien, je devrais définitivement le refaire pour continuer de m'améliorer. À noter aussi que c'est une activité chronophage mais enrichissante!

Si tu as lu jusqu'ici bravo, et je t'encourage vivement à tenter l'expérience de la revue de code sur [codereview](https://codereview.stackexchange.com/)! 