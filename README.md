# Ce dépôt regroupe divers usages de l'outil pcal

Divers usages de l'outils pcal regroupés sous formes de commandes

## Le mois courant

Avec :

 * les semaines qui commencent au lundi 
 * les textes en français

    pcal -a fr -F 1 -S $(date -u +"%m %Y") 1 -o calendar.ps


## Le mois courant avec mercredi marqués

Avec :

 * les semaines qui commencent au lundi 
 * les textes en français
 * les mercredi en écriture contour/vide

    pcal -a fr -F 1 -S $(date -u +"%m %Y") 1 -O wed -o calendar.ps

## Le mois courant (avec les mois avant/après en petit)

Avec :

 * les semaines qui commencent au lundi 
 * les textes en français
 * les mois avant/après en petit en bas à droite

    pcal -a fr -F 1 $(date -u +"%m %Y") 1 -o calendar.ps

## **Les 7 mois à venir**

Avec :

 * les weekends en écriture contour/vide
 * les semaines qui commencent au lundi 
 * les jours fériés marqués à partir d'un fichier dates.txt
 * les cycles lunaires
 * les textes en français
 * le titre en français avec un signe diacritique

    pcal -a fr -F 1 -m -S -E -s 0.3:0.3:0.6 -n /18 -O sat-sun -f dates.txt $(date -u +"%m %Y") 7 -o calendar.ps -C "$(echo 'Les 7 mois à venir'|iconv -f UTF-8 -t ISO-8859-15)"


## Remerciement

Un gros merci à cette page de blog :
http://blog.rtwilson.com/automatic-pdf-calendar-generation-with-pcal/
qui m'a fait découvrir pragmatiquement cet outil

## liens 

La page man :
http://pcal.sourceforge.net/pcal-help.html

Le site :
http://pcal.sourceforge.net/

La page open data des jours fériés français :
https://www.data.gouv.fr/fr/datasets/jours-feries-en-france/

Pour les autres pays hésitez pas à me faire une PR ;)
