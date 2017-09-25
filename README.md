# React-Internationalization

Internationalization - often referred to as 'i18n' - is more than just translating text site-wide. Localised currency formats can break coding, plurals can change sentence structure, and long words in languages like Russian can cause issues with layouts.

Yahoo has created a library called 'React-Intl', which uses the i18n API through its own set of components. By providing locale data at the root of the application, these components will render appropriate text based on the language of the browser.

I created a basic online store that sells tours and events to London. I localised information about the tours using the tools 'React-Intl' provides.

![1](https://user-images.githubusercontent.com/28790452/30825467-b855ddc2-a1f8-11e7-8a8d-1dedaee6ba0b.gif)

There are a lot of things that can change across different languages. It is possible for apps to deal with the bigger things like date formatting manually, but more delicate aspects like plurals and relative time values can prove tricky.

React-Intl can support all these adjustments automatically, but as they can be quite large they need to be selectively imported when needed. This library provides React components and an API to format dates, numbers, and strings, including pluralization and handling translations.

## Import supported locales

Import the locale data for the languages - English, French, and Spanish.
```
import { IntlProvider, addLocaleData } from "react-intl";
import en from "react-intl/locale-data/en";
import fr from "react-intl/locale-data/fr";
import es from "react-intl/locale-data/es";
addLocaleData([...en, ...fr, ...es]);
```

## Fetch translation messages

The way React-Intl translates phrases is through the use of a 'message' variable, which contains a set of key-value pairs matching unique identifiers to translated blocks of text.

```
function getTranslations(languageCode) {
  const code = languageCode.toLowerCase();
  const language = getLanguage(code);
  switch(language) {
    case 'en':
      return en;
    case 'fr':
      return fr;
    case 'es':
      return es;
    default:
      // Default to English
      return en;
  }
}

const messages = getTranslations(language);
```
## Formatters 

React-Int provides a selection of special components that can be used to place formatted text on the screen. 

One of these is *FormattedNumber*, which formats numeric values, including currency.

Like numbers, dates also have their own component - *FormattedDate* - that deals with the complex formatting involved with differing locales.

*FormattedMessage* provides translated strings.

```
import { FormattedMessage, FormattedNumber, FormattedDate } from "react-intl";
```

### Project Installation

There are two methods to download the repository.

#### Method I: Familiar with Git?
Clone this repository, install dependencies, then run the project with the following:

```
> git clone git@github.com:artprofi91/React-Internationalization.git
> cd React-Internationalization
> npm install   or   yarn install
> npm start   or   yarn start
```

#### Not Familiar with Git?
Click [here](https://github.com/artprofi91/React-Internationalization) then download the .zip file. Extract the contents of the zip file, then open your terminal, change to the project directory and:

```
> npm install   or   yarn install
> npm start   or   yarn start
```

#### Project will run on:
Open the browser go to localhost:3000

I built this app with help of ([Web Designer Magazine Tutorial](https://www.myfavouritemagazines.co.uk/design/web-designer-magazine-subscription/)).

