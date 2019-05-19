## PHP astuces et bizarreries ##

Cette semaine j'ai appris deux choses nouvelles en PHP, je vais les partager ici (même si ce n'est pas quelque chose de nouveau pour PHP, seulement nouveau pour moi). Aussi, de même que tout ce que je prévois d'écrire dans ce blog, c'est une manière de m'en rappeler dans le futur et de pouvoir y faire référence plus tard. 

## Astuce: Utilisation de `empty` en conjonction avec `isset` ##

Je suis tombé sur ce [post StackOverflow](https://stackoverflow.com/q/4559925/3729797), et la question est:

> Est-ce redondant d'écrire `isset($var) AND !empty($var)`?

Contrairement à ma première intuition sur le sujet, la réponse à cette question est: [OUI](https://stackoverflow.com/a/4559976/3729797)! 

Comme écrit dans la réponse en lien ci-dessus, la [documentation](http://php.net/empty) dit:
                     

> Determine si une variable est considérée vide. **Une variable est considérée vide si elle n'existe pas** ou si sa valeur est égale à FALSE. `empty()` ne génère pas de warning si la variable n'existe pas.

Un peu plus loin, la documentation continue ainsi:

> `empty()` est essentiellement un équivalent concis de `!isset($var) || $var == false`.

J'utilisais assez souvent les deux fonctions de cette manière, et même si ça n'a pas une importance capitale, je pense que c'est plus propre d'utiliser seulement `empty` dans cette situation. Une autre considération est la performance du code, on peut observer les opcodes générés par les deux versions sur le site [3v4l.org](https://3v4l.org). 


[Ici les opcodes](https://3v4l.org/EccAc/vld#output) pour
    
    if(isset($var) AND !empty($var))
        echo $var;


Et [ici les opcodes](https://3v4l.org/oCGDk/vld#output) pour

    if(!empty($var))
        echo $var;

Le premier bout de code génère 8 opcodes alors que le second seulement 5. La plupart du temps ça n'a aucun impact mais j'imagine qu'il vaut mieux être conscient de la différence tout de même.

## Bizarrerie ##

La bizarrerie dont je veux parler succinctement, je l'ai trouvée sur Reddit, et elle fait partie des comportements étranges de PHP.
Essaye de deviner le résultat de ce code:


    <?php
    
    $a = 1;
    $c = $a + $a++;
    var_dump($c);
    
    $a = 1;
    $c = $a + $a + $a++;
    var_dump($c);


Si tu as deviné:

    int(3)
    int(3)

Tu as raison! Mais tu as probablement triché ou tu étais déjà au courant de ce résultat étrange!

Une très bonne explication(en anglais) sur le pourquoi de ce comportement se trouve [ici](https://gist.github.com/nikic/6699370). En très très bref, ça vient d'une optimisation qui est apparue dans PHP5.1, et qui se comporte étrangement dans ce cas précis.

C'est un résultat curieux, et ça peut être très compliqué de le débuguer! Va voir le lien pour l'explication, c'est très bien écrit. Et pour découvrir plus de curiosité sur PHP, tu peux voir [ce subreddit](https://www.reddit.com/r/lolphp/), certains posts sont vraiment intéressants.

----------

C'est tout pour aujourd'hui. Étant relativement novice en PHP (j'ai commencé à utiliser PHP au début de septembre 2017, il y a 4 mois), je découvre souvent des astuces (et aussi des bizarreries) et je partagerais mes découvertes intéressantes au fur et à mesure que je les découvrirais.