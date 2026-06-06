Koostada ERD mudel, mis rahuldab all pool kirjeldatud tingimusi. Skeem tuleb 
joonistada ainut ANDMELOOGILISEL tasemel st. olemitele tuleb kirjeldada ka 
vajalikul määral atribuute. „Vajalik määr“ tähendab seda, et andmemudelis on KÕIK 
vajalikud atribuudid, mi kirjeldatud ülesande toimimiseks vaja on. Ei piisa sellest, kui te 
ainult ID-d (st Primaty ja Foreign Keyd ära kirjeldate). Tuleb meeles pidada, et ei ole 
olemas ühtegi olemit, kus oleksid ainult ID-d.

Meil on kauba vedamiseks robottehnoloogiat kasutav firma. Me ei vea oma kaupu vaid meie 
klientidele kuuluvaid kaupu. Me ei tea mida veetakse. Meie jaoks on need lihtsalt 
„konteineritäied“ – me saadame kliendi juurde sellise suurusega roboti, mida ta tellis, ta paneb 
sinna sisse midagi ja me viime selle kauba saaja juurde ning tema võtab selle „midagi“ sealt 
konteinerist välja. On neid asju seal üks või mitu pole meie jaoks oluline – need peavad tellitud 
konteineri sisse mahtuma nii ära, et kaan/sahtel läheb kinni. 

Meil on oma töötajad, kes haldavad andmeid – Muudavad teatmikke, täiendavad hinnakirju, 
lahendavad klientide probleeme jne. 

Meie klientideks on kaupade saatjad – kaupade saajad ei pruugi meie kliendid olla. Meie 
klientideks saab ainult registreerides ennast kauba saatjaks. Loomulikult võib ka kauba saatja 
olla kauba saatjaks. Sellisel juhul on kauba saaja meie klient. 

Kliendiks võib olla nii firma kui eraisik. 

Igal firmakliendil on üks või mitu administraator kasutajat, kes haldavad selle kliendi 
kasutajate õigusi. Klientidel on õigus vormistada antud kliendi saadetisi, annulleerida neid, 
jälgida saadetiste liikumist, lahendada oma klientide probleeme jms. 

Tegelikult on meie klientideks loomulikult ka kauba saajad, kellest me suurt midagi ei tea. 
Teame ainult seda, mida kauba saatja meile kauba saatmise hetkel ütleb. See võib olla üsna 
„kõva“ teave (nimi, telefoni nr, aadress) aga võib olla ka üsna „pehme“ teave (Märt, ootab 
Rävala pst ja Lauteri nurgal, 5623320). Siiski ei ole meie asi otsustada (sest paljudel juhtudel 
ei suuda me isegi otsust vastu võtta, kas andmed on „kõvad“ või „pehmed“). Seega on kõik 
isikud, kes pole registreerinud meie kliendiks, meie jaoks nö „pehmed“ kliendid, kelle kohta 
me teame telefoninumbrit, mis tal sellel hetkel oli, mingit nime, mingit aadressi või mitut 
aadressi. Kui tuleb mitmeid tellimusi, samalt telefoninumbril, siis seome sama numbriga kõik 
muutunud andmed. Kliendi nimeks jääb viimati esitatud nimi ja kui aadresse tuleb mitu, siis 
need kõik jäetakse meelde. Siit saab teha järelduse, et „pehme“ klient on telefoninumber. 

Meil on palju roboteid (sellised neoonpunased ja öösel helendavad antennidega „panged“) 
Neoonpunased selle pärast, et nad oleks paremini silma paistvad. Roboteid on meil mitme 
suurusega. Suuruse määrab roboti hoiutuumi suurus: S, M, L, XL, ja XXL. Aga samal robotil 
võib olla ka mitu hoiuruumi (konteinerit) st kui samas suunas jääb mitu tellimust, siis saab 
panna robotisse korraga mitu kaupa erinevatesse hoiuruumidesse, mis avanevad õige kliendi 
juures. Hoiuruum avaneb koodiga, mis saadetakse talle SMSga. 

Üks saadetis on üks kaubaruum, kus võib olla mitu pakki, mis kõik lähevad samale kliendile. 
Hind on määratud kaubaruumi suurusele. Mingil kliendil võivad olla just temale kehtestatud 
hinnad. Meie saame teha oma hinnakirjas soodustusi, mis ei laiene kliendi lepingulistele 
hindadele, sest need on nii või teisti üldisest hinnakirjast madalamad. 

Meie robotid on juhtmevabalt laetavad. Meil on linna peal mitmeid laadimispunkte. See 
tähendab, et kui roboti aku hakkab tühjaks saama otsib ta lähima laadimisjaama ja läheb 
laadima. Robot saab minna laadima siis, kui temas pole kaupa. Seega peab robot kogu aeg 
arvestama, kas tal on veel järgmise paki peale võtmiseks ja ära viimiseks piisavalt energiat. 
Kui ei ole, siis peab ta otsima üles lähima laadimisjaama. Seega, et teha selliseid arvestusi, 
peavad kõik meie logistikapunktid olema varustatud GPS koordinaatidega (X ja Y – mõlemad 
DECIMAL(10,7)).Sellisteks logistikapunktideks on: Kliendi tegevuskoht (mitte klient, sest 
kliendil võib olla tegevuskohti mitu), laadimisjaam ja tarne sihtkoht (st kuhu kaup viiakse). 
Peab olema teada ka keskuse GPS-aadress st koht kuhu robot sõidab käsu „koju“ saamisel. 

Meie kasutajad registreerivad süsteemis kõik robotid ja vajadusel eemaldavad need sealt. Igal 
robotil on unikaalne kood (serial number). Sama laadimisjaamadega (ka neil on unikalased 
koodid). Lisaks sellel on osa roboteid ajuti hoolduses,. Ka see tuleb märkida (millal ja kuhu 
nad remonti läksid ja millal nad sealt uuesti kasutusse saabusid)

Kauba saatmise protsess ise järgmine. Kõigepealt registreerib firma või isik ennast kliendiks. 
Selleks sõlmib ta kliendilepingu ja kui lepitakse kokku erihindades, siis seotakse lepinguga ka 
need hinnad (konteinerite suuruste kaupa). Kliendile tehakse üks administraatorkasutaja. Kõik 
teised selle kliendi kasutajad teeb see kasutaja. Kliendi vastavate õigustega kasutajad seovad 
kliendiga tegevuskohad. Ja võibki kaupade saatmise protsess alata: 

1. Klient tellib roboti oma mingisse tegevuskohta öeldes, millise suurusega konteinerit 
ta vajab ja seda, kellele (tel nr, nimi), kuhu (aadress ja GPS-punkt) ja mis ajaks kaup 
on vaja kohale toimetada. See viimane võib ka tühjaks jääda. See tähendab: nii pea 
kui võimalik. 

2. Pakirobotite süsteem vastab, kas sellistele tingimustele vastav robot leidub ja teatab 
aja, millal robot saabuda võiks. Kui päris sellist ei leidu, siis pakutakse kliendile 
erinevaid variante kohale jõudmise aegadest ja konteinerite suurustest, kust klient 
saab valida talle sobiva või loobuda üldse. 

3. Valitud roboti jaoks tehakse tellimus, kus seotakse robot, tellija (klient), 
tegevuskoht kust robot peab kauba võtma ja koht kuhu kaup tuleb viia. Tellimusega 
seotakse PIN-kood ja saadetakse see kasutajale SMS-ga või E-mailiga. 

4. Robot asub teele 

5. Robot võib tee peal uusi kaupu peale võtta kui tal on mõni konteiner tühi ja selleks 
on vormistatud tellimus. 

6. Kui robot jõuab kohale, PIN-kood sisestatakse ja kaan suletakse siis märgitakse 
tellimus täidetuks. 

Nagu öeldud käivad robotid aegajalt ennast laadimisjaamades laadimas. Peab olema teada, 
millisel ajal millises laadimisjaamas mingi robot oli või on. 

Robotite liikumist jälgitakse 5 minutise sammuga st. et keskse andmebaasi salvestatakse roboti 
GPS asukoht, aku laetuse tase (kahe kohaga pärast punkti) ja vea kood (kui selline on aga ka 
selle seisundil, kui viga pole on kood).