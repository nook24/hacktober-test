Hacktoberfest 2019
========================

Celebrate [Hacktoberfest](https://hacktoberfest.digitalocean.com/) by getting involved in the open source community by completing some simple tasks in this project.

Our task for you: Translate localization files

*As many as you want* - *as long as you want*

## Steps to create a PR

### Step 1: Clone our repository (ORM branch!)

```
git clone -b ORM https://github.com/it-novum/openITCOCKPIT
```

---

### Step 2: Go to the "Locale" folder

```
cd ./openITCOCKPIT/app/Locale
```

---

### Step 3: Choose a language you want to translate to

#### Step 3.1: The language folder does not exist yet:

Copy the template folder (lang_template) and name it like your chosen language

e.g. cp -r ./lang\_template ./de\_DE

```
cp -r ./lang_template ./{{language}}
```
If it is done continue with step 3.2

#### Step 3.2: The language folder already exists:

e.g. cd ./en\_US/LC\_MESSAGES

```
cd ./{{language}}/LC_MESSAGES
```

---

### Step 4: Translate

Translate the content of *.po files (e.g. default.po)

The translation must be done line by line.

The "msgid" contains the original english content.

In the following "msgstr" the translation is to be entered.

#### But before you start, please read our [Important notes](#important-notes) section!

Example:

```
msgid "Week"
msgstr "Woche"
```

### Step 5: Commit, push & create PR

```
git checkout -b ORM_translation_myUserName
git add .
git commit -m "which language was added or edited"
git push origin ORM_translation_myUserName
```
Go to [https://github.com/it-novum/openITCOCKPIT/branches](https://github.com/it-novum/openITCOCKPIT/branches) and create a new pull request with your branch

---

## Important notes

#### Don´t translate en_US, that´s our source language :)

- Special words are not to translate
	- openITCOCKPIT, Statusengine, CakePHP, GearmanWorker
	- LDAP, OpenLDAP, PHP, SSO, NRPE, NDO, UUID, ARO, ACO, ACL
	- .....
- Replace shortcuts with shortcuts in the other language or leave it
	- e.g. EVC (english) -> EVK (german)
	- .....
- Don´t touch placeholders, escape characters, classes, values or html (style) code
	- % prefixed characters are used for replacements. (e.g. %s replaces a string or %1$s)
	- \ escapes "
	- CrudAuthorize::authorize() is an example for an internal class. (Needed for error messages)
	- $ prefixed words are values (e.g. $path)
	- use \<b>\</b> to generate bold characters
	- use \<success>\</success> to generate green characters
- Keep length of strings that are using blank characters to get an uniform length

```
msgid "User:         %s"
msgstr "Benutzer:     %s"
```

