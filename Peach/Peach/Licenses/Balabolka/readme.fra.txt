Balabolka (application console), version 1.78
Copyright (c) 2013-2021 Ilya Morozov
All Rights Reserved

WWW : http://balabolka.site/fr/bconsole.htm
E-mail : crossa@list.ru

Licence : Freeware
Syst�me d'exploitation : Microsoft Windows XP/Vista/7/8/10
Microsoft Speech API: v4.0/5.0 and above
Microsoft Speech Platform: v11.0



*** Ligne de commande ***

balcon [options ...]


*** Param�tres de ligne de commande ***

-l
   Affiche la liste des voix disponibles.

-g
   Affiche la liste des p�riph�riques de sortie audio disponibles.

-f <nom_de_fichier>
   Sp�cifie le nom du fichier texte d'entr�e. La ligne de commande peut contenir quelques options [-f].

-fl <nom_de_fichier>
   Sets the name of the text file with the list of input files (one file name per line). La ligne de commande peut contenir quelques options [-fl].

-w <nom_de_fichier>
   Sp�cifie le nom du fichier de sortie au format WAV. Si l'option est sp�cifi�e, un fichier audio sera cr��. Dans le cas contraire, le texte sera lu � haute voix.

-n <nom_de_voix>
   Sp�cifie le nom de la voix (la partie du nom est suffisant). 
   Si le param�tre n'est pas sp�cifi�, la voix d�finie par le param�tre [-id] ou la voix par d�faut de Windows sera utilis�e.

-id <nombre_int�gral>
   Sp�cifier le code de langue pour la voix (Locale ID). Locale ID est le code de langue attribu� par Microsoft
   (par exemple "1033" ou "0x0409" pour Anglais - �tats-Unis", "1036" ou "0x040C" pour "Fran�ais - France").
   Le logiciel choisit dans la liste de voix la premi�re voix avec l'ID sp�cifi�.
   Si le param�tre n'est pas sp�cifi�, la voix d�finie par le param�tre [-n] ou la voix par d�faut de Windows sera utilis�e.
   La liste de pays avec leurs Locale ID : https://msdn.microsoft.com/en-us/library/cc233982.aspx

-m
   Affiche les param�tres de la voix.

-b <nombre_int�gral>
   Sp�cifie le p�riph�rique audio par son index. L'index de l'appareil audio utilis� par d�faut est 0.

-r <texte>
   Sp�cifie le p�riph�rique audio par son nom.

-c
   Utilise le texte du presse-papiers.

-t <ligne_de_texte>
   Utilise le texte de la ligne de commande. La ligne de commande peut contenir quelques options [-t].

-i
   Utilise le texte de flux d'entr�e standard (STDIN).

-o
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : enregistre les donn�es audio dans le flux de sortie standard (STDOUT) ; si l'option est sp�cifi�e, l'option [-w] est ignor�e.

-s <nombre_int�gral>
   SAPI 4 : sp�cifie le d�bit de la parole compris entre 0 et 100 (pas de valeur par d�faut).
   SAPI 5 et Microsoft Speech Platform : sp�cifie le d�bit de la parole compris entre -10 et 10 (la valeur par d�faut est 0).

-p <nombre_int�gral>
   SAPI 4 : sp�cifie le timbre de la voix compris entre 0 et 100 (pas de valeur par d�faut).
   SAPI 5 et Microsoft Speech Platform : sp�cifie le timbre de la voix compris entre -10 et 10 (la valeur par d�faut est 0).

-v <nombre_int�gral>
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : sp�cifie le volume compris entre 0 et 100 (la valeur par d�faut est 100).

-e <nombre_int�gral>
   Sp�cifie la longueur des pauses entre les phrases (en millisecondes). La valeur par d�faut est 0.

-a <nombre_int�gral>
   Sp�cifie la longueur des pauses entre les paragraphes (en millisecondes). La valeur par d�faut est 0.

-d <nom_de_fichier>
   Utilise un dictionnaire pour la correction de la prononciation (fichier *.BXD, *.DIC ou *.REX). La ligne de commande peut contenir quelques options [-d].

-k
   D�sactive les autres copies de l'application console dans la m�moire de l'ordinateur.

-ka
   D�sactiver la copie de l'application console en cours d'ex�cution.

-pr
   Make pause or resume reading aloud by the active copy of the application. The action is the same as for the context menu item "Pause"/"Resume".

-q
   Met l'application dans une file d'attente. L'application console va attendre que les autres copies du programme terminent leur op�ration.

-lrc
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : cr�e un fichier LRC, si l'option [-w] ou [-o] est sp�cifi�e.

-srt
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : cr�e un fichier SRT, si l'option [-w] ou [-o] est sp�cifi�e.

-vs <nom_de_fichier>
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : sets the name of output text file with visemes, if the option [-w] is specified.
   A viseme is the mouth shape that corresponds to a particular speech sound. SAPI supports the list of 21 visemes.
   This list is based on the original Disney visemes. The application will create the audio file and then read it aloud to get visemes and their timecodes.
   The list of visemes supported by SAPI 5: https://msdn.microsoft.com/en-us/library/ms720881(v=vs.85).aspx

-sub
   Le texte constitue des sous-titres et doit �tre converti en fichier audio, compte tenu des pauses sp�cifi�es. Le param�tre peut �tre utile lorsque les options [-i] ou [-c] sont sp�cifi�es en ligne de commande.

-tray
   Afficher l'ic�ne du logiciel dans la zone de notification du syst�me d'exploitation.
   Cela permet � l'utilisateur de suivre l'ex�cution d'une op�ration et de l'arr�ter � l'aide de l'�l�ment ��Arr�t�� dans le menu contextuel.

-ln <nombre_int�gral>
   S�lectionner une ligne du fichier texte � l'aide de son num�ro. La num�rotation des lignes commence par "1".
   Pour s�lectionner plusieurs lignes, sp�cifiez les num�ros de la ligne de d�part et de celle d'ach�vement dans le texte (par exemple, "26�34").
   La ligne de commande peut contenir quelques options [-ln].

-fr <nombre_int�gral>
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : sets the output audio sampling frequency in kHz (8, 11, 12, 16, 22, 24, 32, 44, 48).
   If the option is not specified, the default value of the selected voice will be used.

-bt <nombre_int�gral>
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : sets the output audio bit depth (8 ou 16).
   If the option is not specified, the default value of the selected voice will be used.

-ch <nombre_int�gral>
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : sets the output audio channel mode (1 ou 2).
   If the option is not specified, the default value of the selected voice will be used.

-? ou -h
   Affiche la liste des options de ligne de commande.

--encoding <encodage> ou -enc <encodage>
   L'encodage du texte de flux d'entr�e standard ("ansi", "utf8" ou "unicode"). La valeur par d�faut est "ansi".

--silence-begin <nombre_int�gral> ou -sb <nombre_int�gral>
   Sp�cifier la longueur de la pause en d�but du fichier audio (en millisecondes). La valeur par d�faut est 0.

--silence-end <nombre_int�gral> ou -se <nombre_int�gral>
   Sp�cifier la longueur de la pause en fin du fichier audio (en millisecondes). La valeur par d�faut est 0.

--lrc-length <nombre_int�gral>
   Sp�cifie la longueur maximale des lignes de texte pour le fichier LRC (en caract�res).

--lrc-fname <nom_de_fichier>
   Sp�cifie le nom du fichier LRC. L'option peut �tre utile lorsque l'option [-o] est sp�cifi�e en ligne de commande.

--lrc-enc <encodage>
   Sp�cifie l'encodage pour le fichier LRC ("ansi", "utf8" ou "unicode"). La valeur par d�faut est "ansi".

--lrc-offset <nombre_int�gral>
   Sp�cifie le d�calage temporel pour le fichier LRC (en millisecondes).

--lrc-artist <texte>
   Sp�cifie une balise ID pour le fichier LRC : artiste.

--lrc-album <texte>
   Sp�cifie une balise ID pour le fichier LRC : album.

--lrc-title <texte>
   Sp�cifie une balise ID pour le fichier LRC : titre.

--lrc-author <texte>
   Sp�cifie une balise ID pour le fichier LRC : auteur.

--lrc-creator <texte>
   Sp�cifie une balise ID pour le fichier LRC : cr�ateur du fichier LRC.

--lrc-sent
   Inserts blank lines after sentences in the LRC file.

--lrc-para
   Inserts blank lines after paragraphs in the LRC file.

--srt-length <nombre_int�gral>
   Sp�cifie la longueur maximale des lignes de texte pour le fichier SRT (en caract�res).

--srt-fname <nom_de_fichier>
   Sp�cifie le nom du fichier SRT. L'option peut �tre utile lorsque l'option [-o] est sp�cifi�e en ligne de commande.

--srt-enc <encodage>
   Sp�cifie l'encodage pour le fichier SRT ("ansi", "utf8" ou "unicode"). La valeur par d�faut est "ansi".

--raw
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : sortie des donn�es audio comme fichiers PCM brut ; les donn�es audio sont sans l'en-t�te WAV.
   L'option est utilis�e avec l'option [-o].

--ignore-length ou -il
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : omet la longueur des donn�es audio dans l'en-t�te WAV.
   L'option est utilis�e avec l'option [-o].

--sub-format <texte>
   Le format des sous-titres ("srt", "lrc", "ssa", "ass", "smi" ou "vtt"). Si le param�tre n'est pas sp�cifi�, le format est d�termin� d'apr�s l'extension du fichier des sous-titres.

--sub-fit ou -sf
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : augmenter automatiquement le d�bit de la parole pour s'adapter aux intervalles sp�cifi�s dans les sous-titres.

--sub-max <nombre_int�gral> ou -sm <nombre_int�gral>
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : sp�cifier le d�bit maximal de la parole dans une gamme de -10 � 10 (pour convertir des sous-titres en fichier audio).

--delete-file ou -df
   Supprimer le fichier texte apr�s la lecture � haute voix ou enregistrer le fichier audio.

--ignore-square-brackets ou -isb
   Ignore text in [square brackets].

--ignore-curly-brackets ou -icb
   Ignore text in {curly brackets}.

--ignore-angle-brackets ou -iab
   Ignore text in <angle brackets>.

--ignore-round-brackets ou -irb
   Ignore text in (round brackets).

--ignore-url ou -iu
   Ignore URLs.

--ignore-comments ou -ic
   Ignore comments in text. Single-line comments start with // and continue until the end of the line. Multiline comments start with /* and end with */.

--voice1-name <nom_de_voix>
   SAPI 4 : l�option n�est pas utilis�e.
   SAPI 5 et Microsoft Speech Platform : sets the additional voice name to read foreign words in text (the part of the name will be enough).
   The option is used together with the option [--voice1-langid]. Other voices can be set by options [--voice2-name], [--voice3-name], etc.

--voice1-langid <id_de_langue>
   Sets the language ID for foreign words in text. The option is used together with the option [--voice1-name]. The command line may contain more than one option [--voice1-langid]. Also an option may contain a comma-separated list of IDs.
   The list of supported language IDs is based on ISO 639-1 codes: am, ar, az, ba, bg, be, ca, cs, cu, cv, da, de, el, en, es, et, eu, fi, fil, fr, ja, he, hi, hr, hu, hy, it, gn, gu, ka, kk-Cyr, kk-Lat, kn, ko, ky, lo, lt, lv, mk, no, pl, pt, ro, ru, sk, sl, sr-Cyr, sr-Lat, sv, tg, th, tr, tt, uk, zh.

--voice1-rate <nombre_int�gral>
   Sets the rate for the additional voice in a range of -10 to 10 (the default is 0).

--voice1-pitch <nombre_int�gral>
   Sets the pitch for the additional voice in a range of -10 to 10 (the default is 0).

--voice1-volume <nombre_int�gral>
   Sets the volume for the additional voice in a range of 0 to 100 (the default is 100).

--voice1-roman
   Use the default voice to read Roman numerals in text. If text with non-Latin characters contains Roman numerals, the application will not change a voice to read them.

--voice1-digit
   Use the default voice to read numbers in text.

--voice1-length <nombre_int�gral>
   Set the minimal length of foreign text parts that will be read by the additional voice (in characters).


*** Exemples ***

balcon -l

balcon -n "Microsoft Anna" -m

balcon -f "d:\Text\book.txt" -w "d:\Sound\book.wav" -n "Emma"

balcon -n "Callie" -c -d "d:\rex\rules.rex" -d "d:\dic\rules.dic"

balcon -n "Mathieu" -t "Le texte sera lu lentement." -s -5 -v 70

balcon -k

balcon -f "d:\Text\book.txt" -w "d:\Sound\book.wav" -lrc --lrc-length 80 --lrc-title "The Lord of the Rings"

balcon -f "d:\Text\film.srt" -w "d:\Sound\film.wav" -n "Laura" --sub-fit --sub-max 2

balcon -f "d:\Text\book.txt" -n Kimberly --voice1-name Tatyana --voice1-langid ru


Un exemple de l'utilisation de l'application avec l'utilitaire LAME.EXE :

balcon -f d:\book.txt -n Julie -o --raw | lame -r -s 22.05 -m m -h - d:\book.mp3


Un exemple de l'utilisation de l'application avec l'utilitaire OGGENC2.EXE :

balcon -f d:\book.txt -n Julie -o -il | oggenc2 --ignorelength - -o d:\book.ogg


Un exemple de l'utilisation de l'application avec l'utilitaire WMAENCODE.EXE :

balcon -f d:\book.txt -n Julie -o -il | wmaencode - d:\book.wma --ignorelength


*** Fichier de configuration ***

Les options de ligne de commande peuvent �tre enregistr�es en tant que fichier de configuration � balcon.cfg � dans le m�me dossier que l'application console.

Exemple de fichier de configuration :
===============
-f d:\Text\book.txt
-w d:\Sound\book.wav
-n Microsoft Anna
-s 2
-p -1
-v 95
-e 300
-d d:\Dict\rules.bxd
-lrc
--lrc-length 75
--lrc-enc utf8
--lrc-offset 300
===============

Le programme peut combiner les options du fichier de configuration et celles de la ligne de commande.


*** Clips audio ***

Le logiciel permet d'ins�rer des liens vers des fichiers audio externes au format WAV (clips audio) dans le texte. La balise de clip audio ressemblera � ceci :

{{Audio=C:\Sounds\ring.wav}}

Si un lien vers un clip audio survient lors de la lecture d�un texte � haute voix, le logiciel se met en pause, lit le clip audio et ensuite reprend la parole.
Lors de la conversion de la parole en fichier audio, le clip audio externe sera int�gr� dans le fichier audio cr�� par le logiciel.


*** "Voice" Tag ***

S�il faut modifier une voix ou ses attributs, une balise sp�ciale peut �tre utilis�e pour SAPI 5 et Microsoft Speech Platform (les voix SAPI 4 ignoreront cette balise).

Format de la balise�:

{{Voice=Nom;Vitesse;Hauteur;Volume}}

- Nom � nom de la voix (un mot ou m�me une partie d�un mot suffit)�;
- Vitesse � vitesse de lecture (la valeur doit �tre entre -10 et 10) ;
- Hauteur � hauteur du son (la valeur doit �tre entre -10 et 10) ;
- Volume � volume du son (la valeur doit �tre entre 0 et 100).

La balise s�applique � tout le texte suivant. Les valeurs des attributs sont s�par�es au sein d�une m�me balise par des points-virgules. Par exemple�:

Le programme lira ce texte par la voix par d�faut. {{Voice=Audrey;0;0;100}} La voix Audrey lira le reste du texte.

Le contenu de la balise ne d�pend pas du registre des lettres. Les valeurs de certains attributs peuvent �tre omis�:

{{voice=mathieu;;;50}}

{{Voice=Thomas;-1}}

{{Voice=Suzanne}}

Pour retourner � la voix par d�faut choisie dans le programme, utilisez la balise ci-dessous�:

{{Voice=}}

Attention�! Il est impossible de basculer entre les voix SAPI 5 et les voix de Microsoft Speech Platform � l�aide des balises.


*** "Pause" Tag ***

Lorsque le programme convertit un texte en fichier audio, on peut utiliser une balise pour ins�rer une pause. La dur�e de la pause doit �tre sp�cifi�e en millisecondes.

Le silence durera deux secondes. {{Pause=2000}} Ensuite, la lecture reprendra.


*** Licence ***

Droits d'utilisation non commerciale de l�application :
- personnes physiques � sans restriction,
- personnes morales � avec les restrictions stipul�es dans l'Accord de Licence du logiciel Balabolka.

L�utilisation commerciale du logiciel demande l'autorisation du d�tenteur du copyright.

###