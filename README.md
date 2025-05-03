# NeoScout Website Translations

Welcome to the **NeoScout Website Translations** repository! This is the central hub for all localization files for the NeoScout website (https://neoscout.ru). Our mission is to make the NeoScout web experience accessible to hackers and cyber-raccoons worldwide by supporting multiple languages. Whether you're a translator, linguist, or just love breaking language barriers, your contributions here are key to our global community. Ready to join the digital underground? Let’s make NeoScout speak your language!

## Purpose

This repository stores translation files for the NeoScout website. Each project (currently only the website) has its own folder containing:
- A `messages.pot` template with translatable strings extracted from the website’s templates and code.
- Language-specific folders (e.g., `en`, `ru`) with `messages.po` files for translations.

By contributing translations, you help localize the NeoScout website, making it accessible to a global audience. Plus, for every fully translated and verified language, you’ll earn a spot in our contributors’ list **and a 3-month subscription** to NeoScout’s premium features!

## Repository Structure
```
neoscout-translations/
├── website/                # Translations for the NeoScout website
│   ├── messages.pot        # Template with translatable strings
│   ├── en/                 # English translations
│   │   └── LC_MESSAGES/
│   │       └── messages.po
│   ├── ru/                 # Russian translations
│   │   └── LC_MESSAGES/
│   │       └── messages.po
├── README.md               # This file
└── babel.cfg               # Configuration for pybabel
```
- **`messages.pot`**: Contains all translatable strings extracted from the website’s Jinja2 templates and Python code.
- **`messages.po`**: Language-specific files where translators add `msgstr` for each `msgid`.
- **Languages**: Currently `en` (English) and `ru` (Russian), but you can add new ones (e.g., `es` for Spanish).
- **`babel.cfg`**: Configuration file for `pybabel` to extract strings.

## How to Contribute Translations

We welcome contributions from anyone who wants to help localize the NeoScout website! Follow these steps to add or update translations:

### 1. Install Tools
Install `pybabel` for managing translations:
```bash
pip install Babel
```
### 2. Clone the Repository
Clone this repo to your machine:
```bash
git clone https://github.com/neoscout-tech/translations.git
cd neoscout-translations
```
### 3. Work on the Translations
The folder contains all translation files for the NeoScout:
- `messages.pot`: The source file with all translatable strings.
- Language folders (e.g., `en`, `ru`) with `messages.po` files.
### 4. Add a New Language (Optional)
If your language isn’t supported (e.g., no `es` folder for Spanish):
- Create a new language folder:
```bash
mkdir -p website/es/LC_MESSAGES
```
- Initialize a `messages.po` file for the new language:
```bash
pybabel init -i website/messages.pot -d website -l es
```
This creates website/es/LC_MESSAGES/messages.po.
### 5. Update Translations
- Open the `messages.po` file for your language (e.g., `website/ru/LC_MESSAGES/messages.po`) in a text editor.
For each `msgid`, add or update the corresponding `msgstr` with the translated text. Example:
```po
msgid "Welcome to NeoScout"
msgstr "Добро пожаловать в NeoScout"
```
- Save the file.
### 6. Compile Translations
Compile messages.po into messages.mo for use on the website:
```bash
pybabel compile -d website
```
This generates messages.mo in each language’s LC_MESSAGES folder (e.g., website/ru/LC_MESSAGES/messages.mo).
### 7. Submit Your Changes
- Create a branch for your changes:
```bash
git checkout -b add-es-translations
```
- Commit your changes:
```bash
git add website/es/LC_MESSAGES/messages.po
git commit -m "Add Spanish translations for NeoScout website"
```
- Push your branch:
```bash
git push origin add-es-translations
```
- Open a Pull Request (PR) on the [NeoScout Translations repo](https://github.com/neoscout-tech/translate).
In the PR description, mention the language and project (e.g., “Added Spanish translations for website”).
### Rewards
For every fully translated and verified language, you’ll receive:
- A spot in our contributors’ list on the NeoScout website and repository.
- A **3-month subscription** to NeoScout’s premium features, giving you access to exclusive tools and analytics.
Once your PR is merged and verified, we’ll reach out via GitHub or your preferred contact method to activate your subscription.

### Guidelines for Translators
- **Accuracy**: Match the hacker/cyberpunk tone of NeoScout (e.g., keep it bold and edgy).
- **Consistency**: Use consistent terms (e.g., always translate "WiFi" as "WiFi" or "Вай-Фай").
- **Test**: If possible, test translations on the website to catch formatting issues.
- **Fuzzy Translations**: Lines marked # fuzzy need review. Update them and remove the fuzzy tag when done.

### Getting Help
Stuck? We’ve got your back:
- Open an issue in this repo with `[Question]` in the title.
- Ping us on [X](https://x.com/neoscout_tech) or via [NeoScout](https://t.me/the_neoscout_manager).

### Contributing
Want to add translations, fix errors, or suggest improvements? Check our CONTRIBUTING.md for details on how to join the NeoScout crew.

### Acknowledgments
Big thanks to all translators who help make the NeoScout website accessible worldwide. You’re the MVPs of our cyberpunk squad, and your work powers our global mission!

**NeoScout — Scan. Analyze. Take control.**
