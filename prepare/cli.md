# Se préparer à la ligne de commande

La ligne de commande, c’est cette fenêtre ou on tape des commandes textuelles au lieu de cliquer partout.  C’est en quelque sorte **l’interface universelle**pour une application, celle disponible sur toutes les plates-formes, sans même avoir besoin d’une interface graphique.  Elle était d’ailleurs là bien avant.

Et ce n’est pas parce qu’elle n’est pas graphique, ou parce qu’elle existe depuis les années 60, qu’elle est moins puissante. **Bien au contraire.**

## La CLI, pourquoi ?

On parle en anglais de *Command Line Interface*, d’où l’abréviation usuelle : **CLI**.  Une CLI n’est pas limitée par l’espace disponible à l’écran pour proposer toutes les options imaginables : elle n’a pas besoin d’aligner rangée après rangée de cases à cocher, boutons radios, champs textuels, onglets et boutons.  Elle a juste besoin de connaître chaque option, et les utilisateurs n’ont plus qu’à taper celles qui les intéressent.

C’est pourquoi **des logiciels comme Git, par exemple, ne sont pleinement exploitables qu’en ligne de commande.**  L’ensemble des sous-commandes de Git totalisent plusieurs milliers d’options.  Les proposer toutes de façon intelligible et exploitable dans une interface graphique (une **GUI**, pour *Graphical User Interface*, qui se prononce « Gou-ï ») est tout simplement impossible.

Bien sûr, une CLI est intimidante les premières fois.  Mais n’aie crainte, on va te donner les bases.

## Windows vs. le reste du monde

L’univers Windows tire sa principale ligne de commande, le programme *Invite de Commande*, également connu sous son petit nom de `cmd.exe`, de ses origines dans MS-DOS.  C’est donc la syntaxe de l’époque DOS qu'on y retrouver, ainsi que la gestion du système de fichiers de cette époque.

À l’inverse, les écosystèmes Linux, Unix et OSX prennent tous leurs gestions de ligne de commande et leur systèmes de fichiers dans l’historique Unix et la série de standards POSIX.  Sur la majorité des points, c’est nettement plus avancé et puissant.  Toutefois, à l’utilisation, il reste quelques points communs.

| Facette |Windows (7+) |Linux / Unix / OSX |
|:-|:-:|:-:|
| Séparateur de dossiers | Anti-slash (*backslash*, `\`) | *Slash* (`/`) |
| Fichiers exécutables | Binaires du système (généralement `.exe`) et fichiers « batch » (`.bat` ou `.cmd`) | Tout fichier ayant le droit d’exécution (`chmod +x`) |
| Fichiers cachés | Attribut spécifique | Nom démarrant par un point (ex. `.bashrc`) |
| Racine du compte | `C:\Users\ton-compte` | `/home/ton-compte` ou `/Users/ton-compte`, mais toujours synonyme de `~` (tilde) |
| Redirections | `>` et `<` | `>` et `<`, `>>`, `<<`, `<<<`… |
| Séquence de commandes | `&&` | `&&`, <code>&vert;&vert;</code>, `;` et bien d’autres… |
| Pipelines | <code>&vert;</code> | <code>&vert;</code> |
| Commandes parallèles | `&` | `&` |
| Variables | `%NOM%` | `$NOM` |
| Surcharge d’environnement | `set NOM=valeur` en amont | `export NOM=valeur` en amont ou `NOM=valeur` en préfixe de commande à la volée |

## Ouvrir une nouvelle CLI

* **Jusqu’à Windows 7 :** dans le menu *Démarrer*, cliquez sur *Exécuter…*, tapez `cmd` et validez.
* **Sur Windows 8 ou ultérieur :** ouvrez le menu Windows, et tapez directement `cmd` : vous devriez rapidement avoir une série de résultats dont *Invite de commandes* ou *Command prompt*.  Cliquez dessus.
* **Sur OSX :** cliquez sur l’icône de recherche Spotlight (la loupe en haut à droite), tapez `Terminal` : OSX devrait sélectionner l’application, vous n’avez plus qu’à cliquer dessus ou utiliser les flèches du clavier pour la sélectionner et presser *Return* (↩︎).  Alternativement, vous pouvez ouvrir une fenêtre *Finder*, sélectionner le dossier *Applications* puis, à l’intérieur, le dossier *Utilitaires* et double-cliquer sur *Terminal*.
* **Sur Linux :** je n’ai probablement pas besoin de vous l’expliquer :grin:…  Mais vous trouverez forcément l’icône de votre terminal dans le lanceur applicatif général.

### Git Bash Et « Node Command Prompt »

Lorsque vous installez Git sur Windows, il installe *Git Bash*, une CLI similaire à celle de Linux et OSX, avec un *shell* Bash, qui utilise donc les mêmes commandes, séparateurs de répertoires, etc.  Si vous avez envie de fonctionner comme sur OSX / Linux alors que vous êtes sur Windows, c’est une alternative possible.  Cherchez-le dans votre menu Démarrer ou en tapant `Bash`dans le menu Windows (8 et ultérieur).

Node.js sur Windows installe également un raccourci *Node Command Prompt*, mais il s’agit simplement de l’invite de commande normale, avec Node.js garanti dans le `PATH`, ce qui ne présente aucun intérêt si vous avez suivi nos recommandations d’installation Node.  En tous les cas, les syntaxes qui y sont proposées sont les mêmes que celles de l’invite de commandes classique.

## Complétion

Il n’est généralement pas nécessaire de taper à la main, intégralement, les noms de commandes, programmes, chemins et fichiers dans une CLI.  La **complétion** est généralement disponible : en pressant la touche *Tabulation* (à gauche du A, au-dessus des majuscules verrouillées) après avoir saisi les premiers caractères, on obtient généralement le reste, ou en tout cas une liste de propositions.

FIXME/RESUME:ILLUS

## Déplacement entre les répertoires

FIXME

## Arrêt de programme en cours

FIXME

## Surcharge de l’environnement

FIXME
