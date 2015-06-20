Multi language url manager
==========================
Multi language url manager

Installation
------------

Add to composer.json

```
"repositories":[
  {
    "type": "git",
    "url": "https://github.com/xfg/yii2-lang.git"
  }
]
```

and run

```
php composer.phar require --prefer-dist xfg/yii2-lang "dev-master"
```


Configuration
-----

Set in Configuration File:

```
'urlManager' => [
  'class' => 'xfg\lang\UrlManager',
  'showScriptName' => false,
  'enablePrettyUrl' => true,
  'enableStrictParsing' => true,
  'displaySourceLanguage' => true,
  'languages' => [
    'en' => 'en-US',
    'ru' => 'ru-RU',
  ]
]
```

Usage
-----

Add in any view:

```
use xfg\lang\LanguageSwitcher;
use xfg\bootstrapLanguages\BootstrapLanguagesAsset;
BootstrapLanguagesAsset::register($this);
echo LanguageSwitcher::widget()
```