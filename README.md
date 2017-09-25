# React-Internationalisation

Internationalisation - often referred to as 'i18n' - is more than just translating text site-wide. Localised currency formats can break coding, plurals can change sentence structure, and long words in languages like Russian can cause issues with layouts.

Yahoo has created a library called 'React-Intl', which uses the i18n API through its own set of components. By providing locale data at the root of the application, these components will render appropriate text based on the language of the browser.

I created a basic online store that sells tours and events to London. I localised information about the tours using the tools 'React-Intl' provides.

There are a lot of things that can change across different languages. It is possible for apps to deal with the bigger things like date formatting manually, but more delicate aspects like plurals and relative time values can prove tricky.

React-Intl can support all these adjustments automatically, but as they can be quite large they need to be selectively imported when needed.

Import the locale data for the languages - English, French, and Spanish.
```
import { IntlProvider, addLocaleData } from "react-intl";
import en from "react-intl/locale-data/en";
import fr from "react-intl/locale-data/fr";
import es from "react-intl/locale-data/es";
addLocaleData([...en, ...fr, ...es]);
```

I built this app with help of ([Web Designer Magazine Tutorial](https://www.myfavouritemagazines.co.uk/design/web-designer-magazine-subscription/)).

