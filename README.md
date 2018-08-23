# German Translation of Yup Messages

This repository contains a single JavaScript file which exports German versions for [Yup](https://github.com/jquense/yup) validation messages. (Only mixed.notType hasn't been translated as it would need a helper method that is not publicly exported by Yup.)

Another approach to localization of Yup messages would be to change the default messages to translation property keys and do the translation in the "UI part" of your app. See this [Yup issue discussion](https://github.com/jquense/yup/issues/71) for details.

## Usage

Copy the file and use it however you like or "npm install" it directly from this Github repository.

Make sure to set your localized messages before any other calls to Yup, see [yup#using-a-custom-locale-dictionary](https://github.com/jquense/yup#using-a-custom-locale-dictionary) for details.

```javascript
import * as yup from 'yup';
import yupLocaleDe from 'yup-locale-de';

yup.setLocale(yupLocaleDe);

// Now use Yup schemas AFTER you defined your custom dictionary
const schema = yup.object().shape({
  name: yup.string(),
  age: yup.number().min(18),
});
```
