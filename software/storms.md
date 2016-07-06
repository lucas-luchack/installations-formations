# WebStorm / PHPStorm, alors ?

Tu es sûr-e ? Pas Sublime Text ?  Bon, OK…

# Paramétrer ton EDI

Ces réglages sont indiqués pour les versions 2016.1.

Travail préparatoire :

1. L’EDI étant fermé, va dans [ton dossier de paramètres](https://www.jetbrains.com/help/phpstorm/2016.1/directories-used-by-phpstorm-to-store-settings-caches-plugins-and-logs.html).
2. Crée si besoin un sous-dossier `codestyles`
3. Colles-y un fichier `Standard.xml` avec le contenu que voici :

```xml
<code_scheme name="Standard">
  <JSCodeStyleSettings>
    <option name="USE_SEMICOLON_AFTER_STATEMENT" value="false" />
    <option name="USE_DOUBLE_QUOTES" value="false" />
    <option name="SPACES_WITHIN_OBJECT_LITERAL_BRACES" value="true" />
    <option name="SPACES_WITHIN_IMPORTS" value="true" />
  </JSCodeStyleSettings>
  <XML>
    <option name="XML_LEGACY_SETTINGS_IMPORTED" value="true" />
  </XML>
  <codeStyleSettings language="JavaScript">
    <option name="KEEP_BLANK_LINES_IN_CODE" value="1" />
    <option name="SPACE_WITHIN_BRACKETS" value="true" />
    <option name="SPACE_BEFORE_METHOD_PARENTHESES" value="true" />
    <option name="KEEP_SIMPLE_BLOCKS_IN_ONE_LINE" value="true" />
    <option name="KEEP_SIMPLE_METHODS_IN_ONE_LINE" value="true" />
    <indentOptions>
      <option name="INDENT_SIZE" value="2" />
      <option name="CONTINUATION_INDENT_SIZE" value="2" />
      <option name="TAB_SIZE" value="2" />
    </indentOptions>
  </codeStyleSettings>
</code_scheme>
```

Donc, dans les Préférences…

## Indentation et gestion du *whitespace*

Dans *Editor > General* 

* Partie *Virtual Space* :
  * Cocher *Allow placement of caret after end of file*
* Partie *Other* :
  * Pour *Strip trailing spaces on Save*, choisir *All*
  * Cocher *Ensure line feed at file end on Save*

Dans *Editor > Code Style > JavaScript* :

* Pour *Scheme*, choisir *Standard*

## ES2015+

Dans *Languages & Frameworks > JavaScript* :

* Pour *JavaScript language version*, choisir *ECMAScript 6* voire carrément *JSX Harmony* (préférable pour nos formations)
* Cocher *Prefer Strict mode*

## StandardJS

La définition du style de code plus haut a géré l’essentiel.  Reste à virer quelques vérifs statiques intégrées à l’EDI, et à activer ESLint seul.

Dans *Editor > Inspections > JavaScript > Code style issues* :

* Décocher *Unterminated statement*

Dans *Languages & Frameworks > JavaScript > Code Quality Tools* :

* Décocher tout sauf ESLint (qu'on coche, du coup)
* S’assurer que *Search for .eslintrc* est sélectionné
* Attention à bien vérifier qu'on utilise la version d’ESLint du projet contenant Standard (pas forcément l’ESLint global pour le Node courant)

À la racine du projet concerné, ajouter le `.eslintrc` suivant (ou modifier l’existant comme suit) :

```json
{
  "extends": ["standard"],
  "parser": "babel-eslint"
}
```

## Complétion

Les EDIs JetBrains ont leur propre gestion de complétion, et TernJS n’y est donc pas disponible.  La complétion native n’est pas mal mais tout de même moint avancée / fûtée que Tern…
