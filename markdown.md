[![N|Solid](https://img1.freepng.fr/20180526/viq/kisspng-linux-tux-computer-icons-5b09f4802d7dc4.3209953815273790721863.jpg)](https://nodesource.com/products/nsolid)
# UNIX 

### Gérer les droits :

| commandes | description |
| ------ | ------ |
| sudo | accorder à certains utilisateurs les droits administrateur |
| chown | changer le propriétaire d'un fichier ou d'un dossier |
| chmod | gérer les droits d'accès d'un fichier ou d'un répertoire |





| Degré de propriété | Action | Type d'accès) |
| ------ | ------ |  ------ |
| u (utilisateur) | + (ajoute le droit) |r (lecture) |
| g (groupe) | - (enlève le droit) | w (écriture) |
| o (autres) | = (définit le droit) | x (exécution |
| a (tout le monde) |  |  |


Exemple :

sas ~ $ chmod og+r fichier.txt


[![N|Solid](https://www.solutions-numeriques.com/wp-content/uploads/2019/04/github.png)](https://nodesource.com/products/nsolid)
# GIT

### Faire relire mon code à mon équipe avec une pull request :

Etapes :
    1- Faire un git add . (mettre à jour l'index)
    2- Faire un git commit (commenter les changement)
    3- Faire un git push (mettre à jour les changement sur la branche)
    4- faire une pull request via github
    
### Commits atomiques : 

L'une des bonnes pratiques consiste à décomposer en une multitudes de petits commits les modifications à enregistrer. Cela permet de référencer les étapes de codage et de pouvoir revenir avant certains changement en cas de problème.

### pull request à taille humaine :

Afin d'optimiser le temps de travail, et d'eviter les difficultés de relectures et validation de code du à une pull request importante, engendrant de nombreux problèmes tels que de nombreux conflits, erreurs etc... Il est important d'automatiser au maximum (linters...), et de fractionner dans la mesure du possible son code.


[![N|Solid](https://i.pinimg.com/originals/d5/bc/80/d5bc803f0ab768736cb0df5c06109c9a.png)](https://nodesource.com/products/nsolid)

# INTEGRATION

### Structurer une page HTML :
[![N|Solid](https://lh3.googleusercontent.com/proxy/4LW4R7PKKzxRLYmvpUb-PUKHrp98D1z7kHnUc2mTk_NdP2dopp9FwSsFWF1hKs_zsmJCWoqgsuJh-aoAIx32rdtvyFs1WdxUf5V85cKKszsp9r_14p0)](https://nodesource.com/products/nsolid)
[![N|Solid](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRBWyeQ1iQ_mzhFtrydA191Z3aDuedHEJ1q_A4ypwGyW8PJ4D0B&usqp=CAU)](https://nodesource.com/products/nsolid)

### Bonnes pratiques SEO :

Afin d'obtenir un bon référencement auprès des moteurs de recherches, il est important de respecter certaines pratiques comme : 
    - Utiliser les balises META <title> (titre sur la fenêtre de navigation), <description> (descriptions affichées sur les moteurs de recherches) etc..., qui donnent envie aux internautes de cliquer.
    - URLs compréhensibles.
    - respecter les règles d'accessibilité.
    - Ajouter des images (les plus légères possible) + texte alternatif dans le ALT.
    - contenu textuel pertinant (mots clés).
    -etc...
 
[![N|Solid](https://www.techgig.com/files/photo_1426162032_small_temp.png)](https://nodesource.com/products/nsolid)

# JAVASCRIPT

## ES6+ :

### Les fonctions fléchées :

Les fonctions fléchées offrent une syntaxe raccourcie des fonctions en utilisant la syntaxe =>.

Exemple:
```sh
// es5
var myFn = function(x) {
  return x + 1;
};

// es6
const myFn = x => {
  return x + 1;
};

```

### Le destructuring :

Le destructuring consiste à assigner des variables provenant d'un objet ou tableau en reposant sur leur structure.


Exemple :
```sh
// Partons d'un objet `myObject`
var myObject = {
  foo: 1,
  bar: 2,
};

Avec ES5, vous deviez par exemple faire

var foo = myObject.foo;
var bar = myObject.bar;

foo; // 1
bar; // 2

Avec ES6, vous pouvez désormais l'écrire sous la forme

const { foo, bar } = myObject;
foo; // 1
bar; // 2

On peut bien entendu destructurer la valeur retournée par une
fonction, pour peu qu'il s'agisse d'un objet ou d'un tableau

const getMyObject = function() {
  return {
    foo: 1,
    bar: 2,
  };
};
const { foo, bar } = getMyObject();
foo; // 1
bar; // 2
```

### Spread operator :

Opérateur de décomposition, il permet de développer un objet itérable (comme un Array) lorsqu'on a besoin de plusieurs arguments.

const myArray = [1991, 8, 1]
new Date(...myArray) // object Date - équivaut à: new Date(1991, 8, 1)

```sh
const myString = "foo bar"
// les objets String étant itérables
[...myString] // ["f", "o", "o", " ", "b", "a", "r"]
```

### ASYNC/AWAIT

Les fonctions async / await permettent d'écrire du code asynchrone non bloquant

#### ASYNC

Une fonction définie avec le mot clé async renvoie systématiquement une promesse : si une erreur est levée pendant l’exécution de la fonction, la promesse est rejetée, et si une valeur est retournée, la promesse est résolue avec cette valeur. Si une promesse est retournée, elle est inchangée.

```sh
async function fonctionAsynchroneOk() {
 // équivaut à :
 // return Promise.resolve('résultat');
 return 'résultat';
}
fonctionAsynchroneOk().then(console.log) // log "résultat"

async function fonctionAsynchroneKo() {
 // équivaut à :
 // return Promise.reject(new Error('erreur'));
 throw new Error('erreur');
}
fonctionAsynchroneKo().catch(err => console.log(err.message)) // log "erreur"
```

#### AWAIT :

await

La partie la plus intéressante est l’utilisation du mot clé await, qui ne peut être utilisé que dans une fonction async. Il permet d’attendre la résolution d’une promesse et retourner sa valeur.

```sh
async function getNombreAsynchrone1() {/* traitement asynchrone (e.g. appel d’une API HTTP) */}
async function getNombreAsynchrone2() {/* traitement asynchrone (e.g. appel d’une API HTTP) */}

async function getAdditionAsynchrone() {
 const nombre1 = await getNombreAsynchrone1();
 const nombre2 = await getNombreAsynchrone2();
 return nombre1 + nombre2;
}
```

### Try/catch :

Pour gérer les erreurs en JavaScript, vous utilisez l'instruction try...catch :

```sh 
try { // code may cause error } catch (error){ // code to handle error }
try { nonExistingFunction(); } catch (error){ console .log(error.name + ":" + error.message); }
```

Dans cette instruction, vous placez le code qui peut provoquer des erreurs dans le bloc try et le code qui gère l'erreur dans le bloc catch .

Si une erreur se produit, JavaScript met fin à l'exécution du code et passe au bloc catch .

Dans le bloc catch , vous pouvez accéder à un objet d' error qui contient au moins le name de l'erreur et le message qui explique l'erreur en détail. 

L'instruction finally est facultative de  try...catch . Le code que vous placez dans le bloc finally s'exécute toujours, que l'erreur se produise ou non.


### JSON :

L’objet JavaScript global JSON possède deux méthodes pour interpréter du JSON et convertir des valeurs en JSON. : les méthodes parse() et stringify().

#### La méthode parse(): 
analyse une chaîne de caractères JSON et construit la valeur JavaScript ou l’objet décrit par cette chaîne. On peut lui passer une option en deuxième argument qui va prendre la forme d’une fonction permettant transformer la valeur analysée avant de la transformer.

#### La méthode stringify():
 convertit une valeur JavaScript en chaîne JSON. On peut lui passer une fonction qui modifie le processus de transformation ou un tableau de chaînes de caractères et de nombres qui sont utilisés comme liste blanche pour sélectionner/filtrer les propriétés de l’objet à inclure dans la chaîne JSON en deuxième argument facultatif.


### Fetch :

L’API Fetch fournit une définition pour trois interfaces Request, Response et Headers. Les interfaces Request et Response représentent respectivement une requête et la réponse à une requête. L’interface Headers représente les en-têtes de requête et de réponse tandis que le body fournit un ensemble de méthodes nous permettant de gérer le corps de la requête et de la réponse.

Pour récupérer le corps de la réponse, nous allons pouvoir utiliser les méthodes de l’interface Response en fonction du format qui nous intéresse :

    La méthode text() retourne la réponse sous forme de chaine de caractères ;
    La méthode json() retourne la réponse en tant qu’objet JSON ;
    La méthode formData() retourne la réponse en tant qu’objet FormData ;
    La méthode arrayBuffer() retourne la réponse en tant qu’objet ArrayBuffer ;
    La méthode blob() retourne la réponse en tant qu’objet Blob ;

Exemple:
```sh 
fetch("https://www.une-url.com")
.then(response => response.json())
.then(response => alert(JSON.stringify(response)))
.catch(error => alert("Erreur : " + error));
```

[![N|Solid](https://logos-download.com/wp-content/uploads/2016/09/React_logo_small.png)](https://nodesource.com/products/nsolid)
# REACT

### Utiliser le débogueur :


###  Afficher une liste de composants :

Pour afficher des listes il y a 2 moyens:
- Assigner à une variable un tableau contenant les elements à afficher
- Utiliser map dans l'expression jsx retournée

```sh
const nombres = [1, 2, 3];

// Méthode 1 :

const elements = nombres.map(n => <li>{n}</li>);
function Composant() {
  return (
  <div>
    <ul>{elements}</ul>
    
// Méthode 2 :

    <ul>
      {nombres.map(n =>
        <li> {n * 2}</li>
      )}
    </ul>
  </div>);
}
```

### LES KEYS ###

Les keys servent à identifier quel élement est ajouté, modifié ou supprimé au sein d'un liste ou d'un tableau.
C'est un identifiant unique. 

Exemple:
```sh
    <ul>
      {nombres.map(n =>
        <li key={n.id}> {n * 2}</li>
      )}
    </ul>
```
### Les props:

Les props sont des propriétés qui permettent de passer des données d'un composant parent à un composant enfant afin de le rendre dynamique.


### Le state:

Le state va être pour un composant donné un objet accessible uniquement depuis ce composant, où l’on va pouvoir stocker les données que nous voudrons utiliser à travers notre composant. La data stockée dans le state sera accessible via l’invocation "this.state". Le state devra uniquement être modifié via la méthode this.setState à laquelle on passera un objet avec l’attribut à modifier et la nouvelle valeur à appliquer. Lorsqu’un attribut du state est modifié, un re-rendering va être déclenché dans notre composant, qui sera mis à jour avec la nouvelle valeur du state.


### Cycle de vie:

#### componentDidMount:
executé après que le composant ait ́ete inséré dans le DOM, render a ́eté appelé 

#### componentWillUpdate:
exécuté avant que le composant ne soit mis à jour dans le DOM, render n’a pas encore ́eté rappelé 

#### componentDidUpdate:
exécuté après que le composant ait ́eté mis à jour dans le DOM, render a déja ́eté rappelé 

#### componentWillUnMount:
exécuté juste avant que le composant ne soit retiré du DOM


### Les formulaires:

Les composants de formulaire contrôlés sont définis avec une propriété value . La valeur des entrées contrôlées est gérée par React, les entrées utilisateur n'auront aucune influence directe sur l'entrée rendue. Au lieu de cela, une modification de la propriété de value doit refléter ce changement. 

L'exemple ci - dessous montre comment la value propriété définit la valeur actuelle de l'entrée et le onChange gestionnaire d'événements met à jour l'état du composant avec l'entrée de l'utilisateur.

Les entrées de formulaire doivent être définies comme des composants contrôlés dans la mesure du possible. Cela garantit que l'état du composant et la valeur d'entrée sont synchronisés à tout moment, même si la valeur est modifiée par un déclencheur autre qu'une entrée utilisateur.



```sh
class Form extends React.Component {
  constructor(props) {
    super(props);
    
    this.onChange = this.onChange.bind(this);
    
    this.state = {
      name: ''
    };
  }
  
  onChange(e) {
    this.setState({
      name: e.target.value
    });
  }
  
  render() {
    return (
      <div>
        <label for='name-input'>Name: </label>
        <input
          id='name-input'
          onChange={this.onChange}
          value={this.state.name} />
      </div>
    )
  }
}
```

### Le routing:

Cela rend l'interface de l'application synchrone avec l' URL du navigateur. Le React Router vous permet de router clairement le flux de données dans votre application. Cela équivaut à une affirmation. Si vous avez cette URL, elle sera équivalente à cette Route et l'interface sera comme suit.

[![N|Solid](https://o7planning.org/fr/12139/cache/images/i/26653903.png)](https://nodesource.com/products/nsolid)

```sh
import React from "react";
import { BrowserRouter, Route, Link } from "react-router-dom";
 
import './App.css';
 
class App extends React.Component {
 
  render()  {
    return  (
      <BrowserRouter>
        <div>
          <ul>
            <li>
              <Link to="/">Home</Link>
            </li>
            <li>
              <Link to="/about">About</Link>
            </li>
            <li>
              <Link to="/topics">Topics</Link>
            </li>
          </ul>
          <hr />
          <div className="main-route-place">
            <Route exact path="/" component={Home} />
            <Route path="/about" component={About} />
            <Route path="/topics" component={Topics} />
          </div>
        </div>
      </BrowserRouter>
    );
  }
}
```


### Les Hooks:

#### useState:

const [state, setState] = useState(initialState);

Renvoie une valeur d’état local et une fonction pour la mettre à jour.


#### setState:

La fonction setState permet de mettre à jour l’état local. Elle accepte une nouvelle valeur d’état local et planifie un nouveau rendu du composant.

setState(newState);


#### useEffect:

useEffect(didUpdate);

Accepte une fonction qui contient du code impératif, pouvant éventuellement produire des effets.


### Consommer une API:

La consommation d'API REST dans une application React peut se faire de différentes manières, les méthodes les plus connues sont Axios (un client HTTP basé sur les promesses) et Fetch API (une API Web intégrée au navigateur).

Les API sont constituées d'un ensemble de données que nous pouvons exploiter et intégrer dans nos application, souvent au format JSON avec des points de terminaison spécifiés.

Une API REST est une API qui suit ce qui est structuré conformément à la structure REST pour les API. REST signifie «Representational State Transfer». Il se compose de différentes règles que les développeurs suivent lors de la création d'API.

#### Fetch:

Fetch() est une méthode JavaScript intégrée pour obtenir des ressources à partir d'un serveur ou d'un point de terminaison API. Il est similaire à XMLHttpRequest, mais l' API fetch fournit un ensemble de fonctionnalités plus puissant et plus flexible.

Fetch() prend toujours un argument obligatoire, qui est le chemin ou l'URL de la ressource que vous souhaitez récupérer. Il renvoie une promesse qui pointe vers la réponse de la demande, que la demande soit réussie ou non.

```sh
fetch('https://api.github.com/users/hacktivist123/repos')
  .then(response => response.json())
  .then(data => console.log(data));

```

#### Axios:

Axios est un client HTTP basé sur des promesses facile à utiliser pour le navigateur et node.js. Comme Axios est basé sur des promesses, nous pouvons profiter de l'async et attendre un code plus lisible et asynchrone.

```sh
// GET 
axios({
  method: 'get',
  url: 'https://api.github.com/users/hacktivist123',
});

// Post
axios({
  method: 'post',
  url: '/login',
  data: {
    firstName: 'shedrack',
    lastName: 'akintayo'
  }
});
```