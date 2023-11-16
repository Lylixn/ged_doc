# Formatage

- Chaque fonction doit faire au **maximum 25 lignes** sans compter les accolades du bloc de la fonction.
- Chaque ligne ne peut faire **plus de 80 colonnes**, commentaires compris. Attention : une tabulation ne compte pas pour une colonne mais bien pour les n espaces qu’elle représente.
- Une **seule** instruction par ligne
- Une ligne vide ne doit pas contenir **d’espace ni tabulation**
- Une ligne ne devrait jamais se terminer par des **espaces** ou des **tabulations**
- Chaque virgule ou point-virgule doit être suivi d’un **espace** si nous ne sommes pas en **fin de ligne**
- Chaque opérateur (binaire ou ternaire) et opérandes doivent être séparés par **un espace** et seulement un.

## Dans un appel de composant

- Suivez ces styles d'alignement pour la syntaxe **JSX**

**[eslint: react/jsx-closing-bracket-location](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-closing-bracket-location.md)
[eslint:  react/jsx-closing-tag-location](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-closing-tag-location.md)**

```HTML
// bad
<Foo superLongParam="bar"
     anotherSuperLongParam="baz" />

// good
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
/>

// if props fit in one line then keep it on the same line
<Foo bar="bar" />

// children get indented normally
<Foo
  superLongParam="bar"
  anotherSuperLongParam="baz"
>
  <Quux />
</Foo>
```

## Dans un return

- Suivez ces styles d'alignement pour la **syntaxe JSX**

**[eslint: react/jsx-closing-bracket-location](https://github.com/jsx-eslint/eslint-plugin-react/blob/master/docs/rules/jsx-closing-bracket-location.md)**

```Javascript
// bad
return <MyComponent className="long body" foo="bar">
         <MyChild />
       </MyComponent>;

// good
return (
  <MyComponent className="long body" foo="bar">
    <MyChild />
  </MyComponent>
);

// good, when single line
return <MyComponent className="long body" foo="bar" />;
```

## Espaces

- Ne laissez **pas d'espace** avant la parenthèse d'ouverture

**[eslint: react/jsx-tag-spacing](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-tag-spacing.md)
[eslint: no-multi-spaces](https://eslint.org/docs/rules/no-multi-spaces)**

```Javascript
// bad
<Foo/>

// very bad
<Foo                 />

// bad
<Foo
 />

// good
<Foo />
```

- Ne pas remplir les **accolades** JSX avec des **espaces**

**[eslint: react/jsx-curly-spacing](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-curly-spacing.md)**

```Javascript
// bad
<Foo bar={ baz } />

// good
<Foo bar={baz} />
```