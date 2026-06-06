Koostada ERD mudel, mis rahuldab all pool kirjeldatud tingimusi. Skeem tuleb 
joonistada ANDMELOOGILISEL tasemel st. olemitele tuleb kirjeldada ka vajalikul 
määral atribuute. „Vajalik määr“ tähendab seda, et andmemudelis on KÕIK vajalikud 
atribuudid, mis kirjeldatud ülesande toimimiseks vaja on. Ei piisa sellest, kui te ainult 
ID-d (st Primaty ja Foreign Keyd ära kirjeldate). Tuleb meeles pidada, et ei ole olemas 
ühtegi olemit, kus oleksid ainult ID-d.

Meil on pakendiringlust korraldav organisatsioon „Tants Taaraga AS“, mille hallata on pakendi 
kogumise kastid ja taarapunktides asuvad pakendiautomaadid. Pakendi kogumise kastid on 
kõik meie omad. Pakendiautomaate on nii selliseid, mis on meie omanduses, kui ka selliseid, 
mis on kaupluste (kaupluste omanike) ja kaubanduskettide omanduses. 

Antud töö raames soovime me lahendada pakendiautomaatide haldamise ülesannet. Taara 
kogumise kaste see ei puuduta. 

Taara on pakend. Pakend on taara. 

Taaraautomaadid asuvad poodide juures taarapunktides. Pood peab sinna määrama oma 
töötaja, kes tegeleb seal jälgimisega ja haldustegevusega sh. probleemide korraldamisega. 
Ühel poel võib olla mitu taarapunkti. Igas taarapunktis on üks või mitu automaati. See sama 
poe töötaja võib olla korraldajaks mitmes taarapunktis. 

Süsteem on riigipiiride ülene st kauplus võib olla mistahes riigis ja igas riigis võetakse vastu 
ka teise riigi taarat, kui selles on sõlmitud riikide vaheline kokkulepe. Kokkulepe sõlmitakse 
riikides taara kogumist korraldavate firmade/organisatsioonide vahel. Kokkulepe võib olla nii 
ühepoolne (st üks riik teise taarat võtab vastu aga teine riik teise riigi taarat vastu ei võta) aga 
ka mõlemapoolne (st mõlemad riigid võtavad teise taarat vastu. Iga riik kirjeldab taara 
pandihinnad ise. 

Taarale väljastatakse märgis. Märgisel on hind. Märgise hinna määrab see riik, kus taarat vastu 
võetakse. Kui märgisele pole riigis hinda määratud, siis selle märgisega taarat seal vastu võtta 
ei saa. 

Praegu on kõik pakendi kogumise automaadid kohaldatud klaas-, plekk- ja plastmasstaara 
kogumiseks. Aga mine tea , mis tulevik toob võib olla on vaja koguma hakata ka mingit muud 
sorti taarat. 

Taara jaguneb gruppideks. Iga grupi all on erinevad tooted, mida tuleb vastu võtta. Igale taara 
tüübile on kehtestatud tüki hind, mida makstakse kliendile taara tagastamisel. 

Igal taarapunktil on mahutavus st palju sinna mahub konteinereid kuhu taarat kogutakse. 
Konteineritel on tüübid ja tüübi kohta on kirjeldatud, millist tüüpi taarat selle tübi 
konteineritesse koguda saab aj palju mingit tüüpi taara sinna ligikaudu mahub. Peab saama 
jälgida, millal mahud täis hakkavad saama ja saata auto õigel ajal taarat ära tooma. Seega 
peame me tegema autode ja juhtide töögraafiku – kes millal on tööl ja siis määrama, kes kuhu 
reisi teeb st kes miilist tellimust täitma läheb. 

On võimalik, et kogu tellimus ei mahu ära ühe auto peale st kas see sama juht peab veel ühe 
reisi tegema või siis läheb mõni teine juht 

Kuskil on keskne kogumispunkt, kes võtab konteinereid vastu, Osa konteinerid on 
taarapunktides (kas täis, poolikult täidetud või tühjad, kas ootamas automaadi alla viimist, 
automaadi all olevad või ära viimist ootavad), osa konteinereid on autodel (kas tühjad, mis 
liiguvad taarapunktidesse, või täis, mis liiguvad kogumiskeskusesse) ja osa konteinereid on 
kogumiskeskuses (kas täis, mis just saabusid ja ootavad tühjendamist või tühjad, mis ootavad 
taarapunktidesse viimist). 

Kogumiskeskusi on mitu. Need asuvad erinevates asulates. Samas asulas võib neid olla mitu.