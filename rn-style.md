# ReactNative et le style

Contrairement à tout ce que vous avez pu faire jusqu'à présent, vous n'allez pas utiliser un fichier css, sass, ou scss mais bien un autre ... objet JavaScript.

```javascript
const styles = {
    textStyle:{
      fontSize:20,
    }
}
```

## À retenir 

* Pour calculer la résolution du périphérique : `let { height, width } = Dimensions.get(“window”);`
* L'orientation peut changer



https://fredcavazza.net/2017/01/26/pourquoi-les-applications-natives-ne-doivent-plus-etre-votre-priorite/

https://fredcavazza.net/2017/09/04/les-interfaces-naturelles-sont-lavenir-du-web-en-partie/


## Making the header reusable
* Dans notre cas, c'est la fonction App qui rendra le header, ça serait donc mieux si elle pouvait décider du contenu à afficher en fonction du contexte
* Pour se faire, on utilise les props, je ne vais pas trop expliquer ce que c'est aujourd'hui. Props = property. Que dit la doc : Most components can be customized when they are created, with different parameters. These creation parameters are called props.
* Passer un(e) props à l'enfant (Header)
* S'assurer que le parent (App) passe bien la props à l'enfant (Header)

## List component boilerplate
* Faire une requête Ajax vers l'API herukoapp
* AlbumList fetch les datas de l'API
* Afficher un Album Detail pour chaque élément du tableau d'objet
* Capital pour tout les noms de fichiers des composants