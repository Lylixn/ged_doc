# Règles de base

## Définition :

- Ne définir qu'**un seul** composant par fichier **[eslint : react/no-multi-comp](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/no-multi-comp.md#ignorestateless)**

```Javascript
// Ne pas faire
var Hello = createReactClass({
  render: function() {
    return <div>Hello {this.props.name}</div>;
  }
});

var HelloJohn = createReactClass({
  render: function() {
    return <Hello name="John" />;
  }
});


// Faire
var Hello = require('./components/Hello');

var HelloJohn = createReactClass({
  render: function() {
    return <Hello name="John" />;
  }
});
```

## Class / Fonction / Arrow Function / React.createClass

- Si vous avez un internal state et/ou des références, préférez **class extends React.Component** à React.createClass :

**[eslint: react/prefer-es6-class](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/prefer-es6-class.md) [eslint: react/prefer-stateless-function](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/prefer-stateless-function.md)**
```Javascript
// bad
const Listing = React.createClass({
  // ...
  render() {
    return <div>{this.state.hello}</div>;
  }
});

// good
class Listing extends React.Component {
  // ...
  render() {
    return <div>{this.state.hello}</div>;
  }
}
```

- Si vous n'avez pas d'état ou de références, préférez les **fonctions normales** (pas les arrow fonctions) aux classes :

```Javascript
// bad
class Listing extends React.Component {
  render() {
    return <div>{this.props.hello}</div>;
  }
}

// bad (relying on function name inference is discouraged)
const Listing = ({ hello }) => (
  <div>{hello}</div>
);

// good
function Listing({ hello }) {
  return <div>{hello}</div>;
}
```
