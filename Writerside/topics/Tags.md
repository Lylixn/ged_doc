# Tags

- **Fermez** toujours les tags qui n'ont pas de **children**

**[eslint: react/self-closing-comp](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/self-closing-comp.md)**

```HTML
// bad
<Foo variant="stuff"></Foo>

// good
<Foo variant="stuff" />
```

- Si votre composant a des propriétés sur **plusieurs lignes**, fermez sa balise sur une nouvelle ligne

**[eslint: react/jsx-closing-bracket-location](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-closing-bracket-location.md)**

```HTML
// bad
<Foo
  bar="bar"
  baz="baz" />

// good
<Foo
  bar="bar"
  baz="baz"
/>
```