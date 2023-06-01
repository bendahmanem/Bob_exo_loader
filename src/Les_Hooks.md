# Les Hooks

## Quelques regles a respecter pour les hooks en React:

- Les hooks ne peuvent etre appeles qu'au niveau le plus haut d'un composant. Les hooks ne peuvent pas etre appeles au sein de boucle ou au sein d'event handler.
- un hook ne peut pas etre appele conditionnellement
- Les hooks ne peuvent etre appeles qu'a l'interieur de composant fonction et pas dans un composant classe

## Le Hook useContext

Le hook useEffect permet de gerer les effets de bords en React (sideEffects)
Comme vous le savez, votre application React est une fonction qui affiche du contenu a un endroit tres precis du DOM (un element HTML dont l'id est root...)

La syntaxe du hook useEffect est la suivante :

```ts
function unComponent() {
  useEffect(() => {
    console.log('passage par le hook useEffect');
  }, []);

  return <>Hello World!</>;
}
```

Le premier parametre est une fonction.

Le second est un tableau de dependances, si ce dernier est vide, la fonction passee en premier parametre du hook useEffect est execute a chaque rendu du composant a l'ecran.

Si un element (une dependance) est present dans ce tableau, on passera dans le hook useEffect a chaque mise a jour de cet element.
