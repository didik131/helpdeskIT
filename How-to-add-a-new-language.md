If you want to add a translation for OpenSupports, you'll need to [create a Pull Request](https://help.github.com/articles/creating-a-pull-request-from-a-fork/) to this repository from a fork with the necessary code changes.

The changes that need to be made are the following:
1. Create corresponding `.js` translation file in the folder [client/src/data/languages](https://github.com/opensupports/opensupports/tree/master/client/src/data/languages), you can take `en.js` as a template. Please use a two-letter code for each language. The language code should mirror [famfamfam flag icons](http://www.famfamfam.com/lab/icons/flags/).
2. Add the language code and require the newly created file in [language-list.js](https://github.com/opensupports/opensupports/blob/master/client/src/data/language-list.js)
3. Add the language code to the `LANGUAGES` constant in [Language.php](https://github.com/opensupports/opensupports/blob/master/server/models/Language.php#L6)
4. Create a element with the language code in the array returned by `getTexts()` in [MailTexts.php](https://github.com/opensupports/opensupports/blob/master/server/data/MailTexts.php). Insert the corresponding translations for each mail template.

One the changes are made, you can create a PR with those. Once it's merged, you will need to wait to the next OpenSupports release to see the changes.

If you want to test the changes you can build your own version by setting up the development environment and [building a package](https://github.com/opensupports/opensupports/blob/master/README.md#building). It will create a `.zip` file ready for installation with your changes.