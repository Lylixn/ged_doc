# Nommage

- Utilisez **camelCase** pour les noms de props

```HTML
// bad
<ReservationCard
  UserName="hello"
  reservAt="world"
/>

// good
<ReservationCard
  userName="hello"
  reservAt="world"
/>
```

- **Omettre** la valeur de la propriété lorsqu'elle est explicitement vraie.

**[eslint: react/jsx-boolean-value](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-boolean-value.md)**

```HTML
// bad
<Foo
    hidden={true}
/>

// good
<Foo
    hidden
/>

// good
<Foo hidden />
```

- Incluez toujours une propriété alt sur les balises **`<img>`**
- Si l'image est présentée, alt peut être une chaîne vide ou le **`<img>`** doit avoir **`role="presentation"`**

```HTML
// bad
<img src="hello.jpg" />

// good
<img src="hello.jpg" alt="Me waving hello" />

// good
<img src="hello.jpg" alt="" />

// good
<img src="hello.jpg" role="presentation" />
```

- Évitez d'utiliser des noms de props qui pourraient être **confondus** avec des mots-clés du Javascript. Par exemple, utilisez **`className` au lieu de `class`, et `htmlFor` au lieu de `for`**

```HTML
// bad
<ReservationCard class="hello" />

// good
<ReservationCard className="hello" />
```

- Évitez d'utiliser les noms des **composants DOM** à des fins différentes

*Pourquoi ? Les gens s'attendent à ce que des props comme style et className signifient une chose spécifique. Varier cette API pour un sous-ensemble de votre application rend le code moins lisible et moins facile à maintenir, et peut provoquer des bogues.*

```HTML
// bad
<MyComponent style="fancy" />

// bad
<MyComponent className="fancy" />

// good
<MyComponent variant="fancy" />
```

