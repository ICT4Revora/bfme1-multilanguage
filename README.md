bfme1-multilanguage
=========

This repo contains all multilanguage versions of 105 and later patches.

Patch 1.05 of thor introduced global data/lotr.str which overwrites every
/lang/*/lotr.str|csf file. For that reason I had to rewrite his structure.
But because the _languagepatch10x.big files might overwrite it again, and many
users use forshires online edition, we have to cheat and use the english lotr.csf
for every other language for 1.05/1.06 as well. That means

/lang/polish/lotr.csf
/lang/italian/lotr.csf
/lang/english/lotr.csf
/lang/russian/lotr.csf
...

in _patch106.big and _patch105.big is everytime the english lotr.csf.
Use the cncstringeditor for clean conversions.

To get the language versions to work we have to provide the translated lotr.csf in
_patch10xLanguage.big with /lang/english/lotr.csf + /lang/Language/lotr.csf and in
_languagepatch10x.big to satisfy the original language installations which might 
overwrite the _patch10xLanguage.big files due to alphabetical order.