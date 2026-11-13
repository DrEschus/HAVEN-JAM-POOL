**Godot script**



**BEZ ODRAZEK, LINE JE KONEC ŘÁDKU, CASE SENSITIVE,**



DOCUMENTATION IN-EDITOR



func \_ready():    #začátek hry



func \_ready():









print("xy") -- print do konzole



pass   #exit loop, one order higher



**MODIFYING NODES CODEBASED**

**refference -- $xy.vlastnost (zobrazit si, CASE SENSITIVE) -> jméno nodky**



**VISIBILITY (INSPECTOR) -- $xy.modulate -> Color.VÝBĚR BARVY**





**INPUT**

**ZAČIT V INPUT MAPĚ (PROJECT, PROJECT MANAGER)**

&#x09;	**key, select bind**





**func \_input(event):**

&#x09;**if event.is\_action\_pressed("VYTVOŘENÝ INPUT"):       #kontroluje press inputu**

&#x09;	**ZBYTEK KÓDU**



&#x09;**if event.is\_action\_released("VYTVOŘENÝ INPUT"):      #kontroluje release inputu**

&#x09;	**ZBYTEK KODU**



**https://www.youtube.com/redirect?event=video\_description\&redir\_token=QUlxb01IWTdtTWp0bU1Oay1BcFpfeXhsZk5DeHxBQnJ0NjlubFNJc1NnZlJLVXVRZ3dlNnh1MVJrMlc2VXdhY0dhS09GZGFLbkVicmNsUkdXQ2JPM2ZVMmZlTVdBcVFEb21IV2FlMHdkcTNpV2kweXlGY3hESEpibzQ0UjEtTHRO\&q=https%3A%2F%2Fdocs.godotengine.org%2Fen%2Fstable%2Ftutorials%2Finputs%2Finput\_examples.html\&v=e1zJS31tr88 input**







**VARIABLES**



**!! mame dynamic declaration by default, typy random pendluji**



**typy --->   string, int, float, bool, Vector2, Vector3**





**CONVERSION SE JMENUJE CASTING typ()    # např**



**var JMENO = hodnota      # assign value dynamic**

**var JMENO: typ = hodnota # assign value static**

**var JMENO := hodnota	 # assign value static recognition**

**JMENO = hodnota          # reassign value			@export před var --> editor v inspectoru**



**počty ------- = #set**

&#x09;      **= x + y # součet**

&#x09;      **+= x # přičíst**

&#x09;      **-= x # odečíst**

&#x09;      **\*= x # vynásobit**

&#x09;      **/= x # vydělit**

**GODOT MA SCOPE A GLOBAL!!!**



**KONSTANTY**

**const JMENO = hodnota #nemohou se menit nijak**







**ARRAYE**

var JMENO = \[hodnota, hodnota] # dynamic content

var JMENO: Array\[Typ] = \[]	# static content

INDEXOVANY OD 0



items\[0] -- # vrati objekt na pozici

items\[1] = 69 == #reassign



items.remove\_at(1) #odstrani item na pozici

items.append()	    # prida na konec 



**DICTIONARY**

var JMENO = {key:value, key:value}



print(hraci\[key])	# vrati spojeny value

players\[key] = 58       # pokud existuje, prepise NEBO VYTVORI NOVY



MUZE BYT UVNITR DALSI ARRAY NEBO DICTIONARY



var hraci = {

&#x09;Jirmen: {HP: 20, Penize: 5}

&#x09;Ondra: {HP: 80, Penize: 10}

&#x09;Adam: {HP: 40, Penize: 2}









**ENUMY**

specialni variable která uklada tagy nebo oznaceni pro jednodussi acess

v podstate glorified listy s konstantama uvnitř





enum Povaha = {HODNY, ZLY, NEUTRALNI}

var hracova\_povaha = Povaha.HODNY



if hracova\_povaha == Povaha.ZLY:

&#x09;do shi





vic safe checking, **jednodussi @export**











**IF statementy, podmínky**



**if PODMINKA:  	#muze byt built in bool funkce**

&#x09;**indent bloc**

**elif:		#nepovinny**

&#x09;**indent**

**else:		#nepovinny**

&#x09;**indent**



**porovnani  -------    == #rovna se**

&#x09;		**>  # vetsi 	>= vetsi bo rovno**

&#x09;		**<  # mensi 	<= mensi bo rovno**

&#x09;		**!= # nerovna se**



**kombinace --------    and # a**

&#x09;		**or # bo**



**FUNKCE**

**nekdy prebuilt -- \_ready(): nebo \_input():**

**podtržítko znamena auto call od enginu**



**func JMENO():	#syntax**

&#x09;**indent**



**FUNKCE MUZE MIT INPUTY A RETURNY**



**func JMENO(cis1: typ, cis2: typ) -> typ:**

&#x09;**return cis1\*cis2   #vraceni hodnoty, konec funkce**



&#x09;



var soucet = add(1,2) #pouziti jako declare





RANDOM CISLA --- randf() #mezi 1  a 0

&#x09;	randi\_range(x, y)  #vraci int in range





&#x09;

**LOOPY**

**for item in items:				# na array (list)**

&#x09;**print(item) 		# playing around**

&#x09;**if item.length() > x	# fce na delku OBSAHU**

&#x09;	**do shi**

**for pro arraye:::**

**for jmeno in hraci:**

&#x09;**print(str(hraci\[jmeno]))**

&#x09;









**for i in 10:		# generic, začína 0, opakuje se dle cisla na konci**

&#x09;print(i)	



while HP > 50:		# while loopa, dle podmínky pokracuje az do false

&#x09;do shi		# bacha



break --> prestat s loopou uplne

continue --> prestat s aktuálním opakovanim, primo na DALSI	



MATCH

v podstate switch a case z c#

match HP:

&#x09;100:			#nejde checkovat range

&#x09;	do shi

&#x09;













**.**

