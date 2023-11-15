# Nommage

- Utilisez PascalCase pour les noms de composants React. Par exemple, `ReservationCard`.

```Javascript
// bad
import reservationCard from './ReservationCard';

// good
import ReservationCard from './ReservationCard';
```

- Utilisez le **nom du fichier comme nom du composant**. Par exemple, ReservationCard.jsx doit avoir pour nom de référence ReservationCard.
- Toutefois, pour les **composants racine d'un répertoire**, utilisez **index.jsx** comme nom de fichier et le **nom du répertoire comme nom de composant** :

```Javascript
// bad
import Footer from './Footer/Footer';

// bad
import Footer from './Footer/index';

// good
import Footer from './Footer';
```

- Utilisez PascalCase pour les noms de références de composants.

[eslint: react/jsx-pascal-case](https://github.com/yannickcr/eslint-plugin-react/blob/master/docs/rules/jsx-pascal-case.md)

```Javascript
// bad
const ReservationItem = <ReservationCard />;

// good
const reservationItem = <ReservationCard />;
```