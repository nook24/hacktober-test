Hacktoberfest 2019
========================

Celebrate [Hacktoberfest](https://hacktoberfest.digitalocean.com/) by getting involved in the open source community.
We would like to ask you to help us translate openITCOCKPIT in as many languages as possible.

*As many as you want* - *as long as you want*

## About the project
openITCOCKPIT is a modern web interface to manage a Nagios or Naemon based monitoring environment.

For more information please see the projects home page: https://openitcockpit.io/


## How to contribute

### Step 1: Fork the repository

Fork our repository into your personal GitHub account by pressing on _Fork_ in the top right corner
![Fork openITCOCKPIT repository](https://openitcockpit.io/hacktoberfest/2019/fork.png)

Wait until the fork is done. This will just take a few seconds.
![Waiting for GitHub](https://openitcockpit.io/hacktoberfest/2019/waiting.png)

Clone the repository (replace **YOUR\_ACCOUNT\_NAME**)

![Clone Code](https://openitcockpit.io/hacktoberfest/2019/clone.png)

```
git clone -b ORM https://github.com/YOUR_ACCOUNT_NAME/openITCOCKPIT
cd openITCOCKPIT/
```

Please make sure to clone the **ORM** branch!

---

### Step 2: Go to the `Locale` folder

```
cd app/Locale
```

---

### Step 3: Choose a language you want to translate to

#### Step 3.1: The language folder does not exist yet:

Copy the folder `lang_template` and rename it like your chosen language.

```
cp -r lang_template de_DE
```

If it is done continue with step 3.2

#### Step 3.2: The language folder already exists:
e.g.

```
cd de_DE/LC_MESSAGES
```

---

### Step 4: Translate

Translate the content of `*.po` files (e.g. default.po)

The translation must be done line by line.

The `msgid` contains the original english content and should **not be touched**

The translated message goes to `msgstr`.

#### But before you start, please read our [Important notes](#important-notes) section!

Example:

```
msgid "Week"
msgstr "Woche"
```

### Step 5: Commit, push & create PR

Replace **YOUR\_ACCOUNT\_NAME** with your GitHub account name.

```
git checkout -b ORM_translation_YOUR_ACCOUNT_NAME
git add .
git commit -m "Added translation for de_DE"
git push origin ORM_translation_YOUR_ACCOUNT_NAME
```

To contribute your changes, you need to send a pull request:

![Create Pull Request](https://openitcockpit.io/hacktoberfest/2019/pull_request.png)

Please notice: You need to select **ORM** as `base` while you create your pull request.
![Set base to ORM](https://openitcockpit.io/hacktoberfest/2019/use_ORM_branch.png)

---

## Important notes

#### Don´t translate en_US, that´s our source language :)

- Special words are not to translate
	- openITCOCKPIT, Statusengine, CakePHP, Gearman, GearmanWorker
	- LDAP, OpenLDAP, PHP, SSO, NRPE, NDO, UUID, ARO, ACO, ACL,
	- Nagios, Naemon, NPCE, NDOUtils
	- .....
- Don´t touch placeholders, escape characters, classes, values or html (style) code
	- % prefixed characters are used for replacements. (e.g. `%s` replaces a string or `%1$s`)
	- `\` escapes `"`
	- `CrudAuthorize::authorize()` is an example for an internal class. (Needed for error messages)
	- `$` prefixed words are variables (e.g. `$PATH`, `$USER1$`, `$ARG1$`)
	- use `<b>This is bold</b>` to generate bold characters
	- use `<success>Green text</success>` to generate green characters
- Keep length of strings that are using blank characters to get an uniform length

```
msgid  "User:         %s"
msgstr "Benutzer:     %s"
```

## Need help?
* Join [#openitcockpit](http://webchat.freenode.net/?channels=openitcockpit) on freenode.net for any questions