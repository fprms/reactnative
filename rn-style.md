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
