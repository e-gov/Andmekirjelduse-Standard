# Andmekirjelduse juhis lisa 1. Andmekirjelduse standard

Veebruar 2026

Versioon 3.0.1


## Dokumendi ajalugu

| ver | muutuse sisu | autor | kuupäev |
|-----|--------------|--------|----------|
| 1.0 | Juhise aluseks on 2019–2020. a koostatud juhis „Eesti andmehalduse metoodikaprojekt. Andmekirjelduse juhis“. Selle üheks osaks on Lisa 2 Andmekirjelduse standard. | Raivo Ruusalepp, Kuldar Aas, Siim Aben, Veiko Berendsen | aug 2020 |
| 1.1 | Versiooni 1.0 Lisa 2 Andmekirjelduse standard on tõstetud eraldi dokumendiks. | Veiko Berendsen | märts 2021 |
| 1.7 | Sisse on viidud versioon 1.0 tagasiside ja RIHAKEse arendusel tekkinud vajadused, täpsustatud DCAT võrdlus.<br><br>MKM, STAT, RIA tagasisides edastamine. | Kuldar Aas | aprill 2022 |
| 1.8 | Sisse viidud v1.7 tagasiside kommentaarid ja parandused.<br>Üle vaadatud MKM, RIA, SA. Keeletoimetatud.<br><br>Edastamine andmete võrgustiku tagasisideks. | Kuldar Aas, Veiko Berendsen, Eero Vegmann, Reana Parve | mai 2022 |
| 2.0 | Lõppversioon | Kuldar Aas, Veiko Berendsen | mai 2022 |
| 2.1 | Kirjelduselementide nimekirja täiendamine Euroopa andmehalduse määruse ([andmehaldust käsitlev õigusakt](https://eur-lex.europa.eu/legal-content/ET/TXT/?uri=CELEX:52020PC0767) – DGA) ja [väärtuslike andmestike nimekirja rakendusmääruse](https://eur-lex.europa.eu/legal-content/ET/TXT/?uri=CELEX:32023R0138) (HVD) nõuetest tuleneva katmiseks.<br><br>Täiendamine lähtuvalt asutuste tagasisidest. | Kuldar Aas, Annika Uibopuu, Eero Vegmann | nov 2023 |
| 2.2 | Märkuste sisseviimine. Üle vaadatud MKM, RIA, SA. | Veiko Berendsen, Annika Uibopuu, Kuldar Aas | jaan 2024 |
| 2.3 | Otsesed osutused RIHAKEsele välja jäetud, sest vajab eraldi RIHAKEse rakendusjuhist. Keeletoimetatud. | Veiko Berendsen, Kuldar Aas | jaan 2024 |
| 3.0 | Lõppversioon, avalikustamine. | Veiko Berendsen, Annika Uibopuu, Kuldar Aas | juuli 2024 |


Kommentaarid standardi kohta on oodatud: 

Statistikaamet (andmehaldus@stat.ee), 

Majandus- ja Kommunikatsiooniministeerium (andmed@mkm.ee).


## Sisukord

(WIP)


## Lühendid

- DCAT – andmekataloogi sõnastik (*Data Catalog Vocabulary*), mis on W3C standard. 
- DCAT-AP – andmekataloogi sõnastiku rakendusprofiil (*Data Catalog Vocabulary Application Profile*) Euroopa Liidu riikide vahel andmestike ja andmeteenuste kirjelduste vahetamiseks.
- DGA – Euroopa Parlamendi ja nõukogu määrus (EL) 2022/868, 30. mai 2022, Euroopa  andmehalduse kohta ning millega muudetakse määrust (EL) 2018/1724 (andmehalduse määrus, *Data Governance Act*).
- HVD – väärtuslikud andmestikud (*high value datasets*) nagu need on määratletud Euroopa Liidu väärtuslike andmestike nimekirja rakendusmääruses ja mis käsitleb andmestikke valdkondi; neid nimetatakse ka kõrgväärtuslikud andmestikud.
- RIHA – riigi infosüsteemi haldussüsteemi käitlev rakendus.
- RIHAKE – asutustele loodud rakendus andmekirjeluste koostamiseks ja edastamiseks RIHAsse.
- ODD – Euroopa Parlamendi ja nõukogu direktiiv (EL) 2019/1024, 20. juuni 2019, avaandmete ja avaliku sektori valduses oleva teabe taaskasutamise kohta. 


## Muudatuste ajalugu

Võrreldes versiooniga 2.0 on sisse toodud järgmised muudatused:
- Sissejuhatava peatüki muutmine. Lisatud on kirjeldusstandardisse kuuluvate komponentide ja olemite ülevaade ja seosed. 
- Ühildatud järgmiste alusstandardite versioonidega: DCAT 3.0 ja DCAT-AP 3.0.0 
- Lisatud objektide kirjeldused: andmekataloog, andmeteenus. 
- Muudetud  kirjelduse  tabeli  struktuuri.  Veerg  DCAT-AP  viide  koondab  endas  nii  viite kirjelduselemendi  terminile  (Dublin  Core  või  muu),  DCAT-ile  (W3C  standardis)  ja  selles kirjeldatud  semantilisele  väärtuste  vahemikule  (range,  lühendatult  standardis  vahemik) ning samale DCAT-AP osas. 
- Tehtud on sisulised kirjelduselementide muutused vastavalt muutunud alusstandarditele ja kasutuspraktikale. Selles on silmas peetud riigi kesksete andmekirjeldusi kasutatavate süsteemide eesmärke ja vajadusi.  
- Kirjelduselemendid on olemi piires järjestatud alfabeetiliselt. 


# 1. Sissejuhatus

## 1.1 Eessõna

Käesolev andmekirjelduse juhise lisa 1 esitab andmekirjelduse standardi. Standard on loetelu kohustuslikest ja soovituslikest kirjelduselementidest, nende tähendusest näidetega ning tehnilistest ja semantilistest seostest. Standardi rakendamine organisatsioonis tagab andmekirjelduste kokkulepitud semantikaga masintöödeldavuse. Standard võimaldab liidestuste tegemist andmekirjelduste ja ka andmete vahetamiseks nii organisatsioonide vahel kui ka riigi keskselt hallatavate andmete valdkonna infosüsteemidega.[^1]

Andmekirjelduse standardi väljatöötamisel on võimalikult palju kasutatud rahvusvahelist praktikat ja taotletud sellega semantilist ühildumist. Peamiseks rahvusvaheliseks aluseks on andmekataloogi sõnastiku versioon 3.0[^2] ja selle rakendusprofiil DCAT-AP. Lähtutud on rakendusprofiili versioonist DCAT-AP 3.0.0.[^3]

Andmekataloogi sõnastiku DCAT paljud kirjelduselemendid on seotud kirjeldusstandardiga Dublin Core.[^4] Dublin Core on ka Eestis üle võetud rahvusvaheline standard üldiseks inforessursside kirjeldamiseks.[^5] Samuti toetavad nii Dublin Core kui DCAT lingitud andmete kasutuselevõttu. Rahvusvahelise praktika kasutamine võimaldab kirjeldusi vahetada rahvusvaheliselt ning vähendab standardi pikaajalise haldamise kulusid.

Sõnastike kirjelduselementide osas on arvestatud Eesti standardiks üle võetud rahvusvahelise standardiga ISO 25964 „Tesaurused ja nende koostalitusvõime teiste sõnastikega.“[^6] Seda eelkõige kasutatava terminoloogia osas.

[^1]: Avaliku sektori andmekogude osas on selleks infosüsteemiks [riigi infosüsteemi haldussüsteem](https://www.riha.ee/Avaleht) (RIHA). Avaandmete osas on selleks infosüsteemiks [Eesti avaandmete teabevärav](https://andmed.eesti.ee/)(andmed.eesti.ee). 
[^2]: [Data Catalog Vocabulary (DCAT) - Version 3](https://www.w3.org/TR/vocab-dcat-3/) (W3C Proposed Recommendation 13 June 2024)
[^3]: [DCAT Application Profile for data portals in Europe](https://interoperable-europe.ec.europa.eu/collection/semic-support-centre/solution/dcat-application-profile-data-portals-europe/release/300)(DCAT-AP 3.0.0)
[^4]: [Dublin Core Metadata Innovation (DCMI)](https://www.dublincore.org/)
[^5]: EVS-ISO 15836-1:2019 Informatsioon ja dokumentatsioon. Dublin Core’i metaandmeelemendid. Osa 1: Põhielemendid (kehtiv alates 15.05.2019) ja EVS-ISO 15836-2:2023 Osa 2: DCMI atribuudid ja klassid (kehtiv alates 02.05.2023).
[^6]: EVS-ISO 25964-1:2023 Informatsioon ja dokumentatsioon. Tesaurused ja nende koostalitusvõime teiste sõnastikega. Osa 1: Infootsingu tesaurused ja EVS-ISO 25964-2:2023 Informatsioon ja dokumentatsioon. Tesaurused ja nende koostalitusvõime teiste sõnastikega. Osa 2: Koostalitusvõime teiste sõnastikega (kehtiv alates 02.05.2023).


## 1.2 Käsitlusala

Standard käsitleb organisatsiooni andmestike kirjeldamise osasid: komponente ja olemeid.  

**Komponentidena** on käsitletud andmestiku kui terviku ülevaatlikku kirjeldust,  andmestiku sisu  detailset kirjeldust ning sõnastike osa kirjeldust ehk mõistelist kirjeldust, mis aitab hallata sõnavara. 

**Olemitena**  on  käsitletud  andmekirjelduse  standardi  eraldi hallatavaid  ja  kirjeldatavaid objekte, mis koos moodustavad mudeli.  

Standard  on  koostatud  ühilduvana  DCAT-AP  3.0.0-ga.  See  võimaldab  organisatsioonidel andmekataloogis kirjeldada andmestikud ning nende levitused, rühmitada andmestikud sarjadesse. Standardis on samuti andmekataloogis kirjeldatud andmestike andmeteenuste osa. 

Standard  käsitleb andmestiku  struktuuri  detailset sisemist  kirjeldust. See on  kitsendatud tabeli kirjeldusega, mis on kas nimekirja või risttabeli kujul.


## 1.3 Kirjeldusstandardisse kuuluvate olemite ülevaade ja seosed

### 1.3.1 Komponendid ja olemid

Kirjeldusstandardisse kuuluvad komponendid ja olemid on omavahel seotud. Olemite vahelised seosed on esitatud joonisel 1 ning moodustavad andmekirjelduse.[^7] Sellel on kujutatud, kuidas andmestikud ja nende sarjad on hierarhiliselt osad andmekataloogist. On näidatud, kuidas andmestik on kirjeldatav levitusena, mis on kasutatav andmeteenusena, mida saab edastada organisatsioonist välja ja mida saab pärida.[^8]

Andmestikud ja levitused on andmestruktuurid (üldiselt failid ja/või tabelid). Tabel või muu hästi struktureeritud andmete hulk koosneb andmeelementidest. Andmeelemendid on kirjeldatavad sõnastikes kui terminid ja mõisted. Andmeelemendid on ka grupeeritavad ning see andmeelementide grupp on ka eraldi hallatav. Nii andmetabel kui ka andmeelementide grupp on käsitletav andmeobjektina. Selline andmeobjekt luuakse kas arusaadavuse ehk andmete mõistmise parandamiseks või halduslikult seotud objektina nagu põhiandmete (master data) objekt või kui toimingu või teenuse kontekstis kokku kuuluv kirje (record).


![Joonis 1](images/joonis1.png)

*Joonis 1: Tervikliku andmekirjelduse koostamisel komponentide vahel toimivad seosed.*


Järgnevalt on esitatud kirjeldusstandardisse kuuluvate olemite lühikirjeldused ning kui need on seotud standardiga DCAT 3.0, siis olemi määratlused eesti ja inglise keeles. DCAT standard nimetab neid olemeid klassideks.

[^7]: Andmekirjelduse määratlus ja selle sisu kirjeldus on esitatud andmekirjelduse juhises.
[^8]: Andmeteenust on standardis käsitletud DCAT 3.0.0 määratletud tähenduses. Andmeteenus on operatsioonide kogum, mille abil antakse juurdepääs ühele või enamale andmestikule või andmetöötlusfunktsioonile. (A collection of operations that provides access to one or more datasets or data processing functions.)


### 1.3.2 Andmekataloog

Andmekataloog (Catalog) on nimekiri kataloogitud objektidest, mis andmehalduses on andmestikud ja mille kohta on kataloogis metaandmekirje. Andmekataloog võib ka toimida repositooriumina, millisel juhul on selles lisaks metaandmetele halduse all ka andmestikud ise.

Andmestikud võivad olla rühmitatud sarjadesse. Tavaliselt on organisatsioonil üks andmekataloog. Andmekataloog on vahend, mille abil saab muu hulgas hallata andmestike pealt osutatavaid andmeteenuseid.

**DCAT määratlus**
- Inforessursside hallatud metaandmete kogum.
- A curated collection of metadata about resources.


### 1.3.3 Andmestike sari

Andmestike sarja (Dataset Series) moodustavad mingi kindla rühmitamiskriteeriumi alusel kokku kuuluvad andmestikud. Andmestike esitamine andmekataloogis sarjades võimaldab ühelt poolt terve kataloogi jagada osadeks ja teiselt poolt rühmitada andmestikud. Tavalised rühmitamiskriteeriumid on: temaatiline, kronoloogiline, seotus teenuse või protsessiga. Harvemini on kriteeriumiteks aktiivne ja arhiivi osa ning faili vorming. Sarjade moodustamine ei ole kohustuslik, kuid kui sarjad on kasutusel, on need kohustuslik kirjeldada st koostada sarja metaandmekirje.

Sarja mõiste on kasutusel arhiivi- ja dokumendihalduses. Arhiivieeskirjas on punkt, mis ütleb, et sarja saab moodustada andmete kogumitest, mida saab identifitseerida ja koos hallata.[^9] Sarjade moodustamise põhimõtted andmekataloogis ja liigitusskeemis on andmestike sarjadena haldamist soodustavana kokkulangevad. Soovitav on organisatsioonis tekkivad andmestikud liigitada sarjadesse.

**DCAT määratlus**
- Eraldi avaldatav andmestike kogum, millel on mingid ühised tunnused, mille alusel need on rühmitatud.
- A collection of datasets that are published separately, but share some characteristics that group them.

[^9]: Arhiivieeskiri. (RT I, 19.06.2020, 4) § 7 Liigitusskeemi tasandid, lõige 4, punkt 1. Arhiivieeskirja seletuskirjast võib järeldada, et andmete kogumi all on silmas peetud sama, mida riikliku statistika seadus määratleb kui andmestikku. Seletuskirjas on: „Sarja moodustamise ühe tunnusena on lisatud „andmete kogum, mida saab identifitseerida ja koos hallata“. See annab selgema võimaluse andmekogudes oleva teabe liigitamiseks, soodustades sealhulgas ka säilitustähtaegade määramist mistahes andmetele, mida on mõistlik kogumina hallata. Kokkuvõtlikult märkides tähendab see sätte mõttes mistahes andmete kogumit, mida on mõistlik koos hallata (sama säilitustähtaeg, samad eraldamistoimingud hävitamiseks, samad juurdepääsutingimused ja muud võimalikud haldamistoimingud).“

### 1.3.4 Andmestik

Andmestik (Dataset) on terviklikult identifitseeritav ja hallatav andmete kogum.[^10] Andmestiku tüüpe on mitmesuguseid ning kataloogis on need kokku viidavad Dublin Core inforessursi tüüpidega.[^11] Dublin Core inforessursi tüüpide märksõnastikus on andmestik (dataset) üks märksõna. Praktikas on andmekataloogis enamasti andmestiku tüüpi inforessursid. See tähendab, et andmestik võib olla terve õiguslikult kehtestatud andmekogu või ka infosüsteem. Samas on võimalik nii andmekogusid kui infosüsteeme hallata sisuliselt või tehniliselt määratletud ja eristatavate osade kaupa, mida võib nimetada alamandmestikeks. Kui andmekogu kui andmestikku määravad kriteeriumid on peamiselt selle eraldi õiguslik olemasolu, siis paljud infosüsteemid, andmebaasid või nende osad on organisatsiooniliselt või tehniliselt hallatavad andmestikena ning samuti on avaandmete portaalides ja mujal andmestikeks teksti, pildi jms tüüpi andmestikud. 

**DCAT määratlus**
- Ühe isiku [või organisatsiooni] avaldatud või hallatud andmete kogum, mis on tehtud kättesaadavaks või alla laetavaks ühel või enamal esituskujul.
- A collection of data, published or curated by a single agent, and available for access or download in one or more representations.

[^10]: Põhjalikum andmestiku selgitus koos määratlustega on andmekirjelduse juhises.
[^11]: [DCMI Metadata Terms](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/). Osa 7. DCMI Type Vocabulary


### 1.3.5 Alamandmestik

Alamandmestik on objektitüübina sarnane andmestikuga. Vajadus alamandmetiku eristamiseks tuleneb sellest, et andmekogudes (infosüsteemides, andmebaasides) on loogiliselt või tehniliselt eristuvad osad, mida on otstarbekas hallata eraldi. Need võivad olla hulk tabeleid või terve skeem relatsioonilises andmebaasis.

DCATis alamandmestiku klassi ei ole. Käesolevasse standardisse on see lisatud andmekogude (andmebaaside) loogilise või füüsilise haldamise lihtsustamise jaoks ehk konkreetselt selleks, kuidas on otstarbekas luua seos andmekataloogi ja andmebaasi osa vahel ja seda hallata. Osalt tuleneb vajadus ka sellest, et õiguslikult reguleeritud andmekogu, see tähendab andmete struktuur, mille kohta on andmekogu põhimäärus, võib mõnel juhul sisaldada tegelikult üsna eraldi ’töötavaid’ osasid. Just selliseid osasid ongi praktikas otstarbekas hallata kui alamandmestikke.


### 1.3.6 Levitus

Levitus (Distribution) on andmestiku salvestamiseks või edastamiseks tehtav andmete tehniline esitus, konkreetseks kasutusjuhuks mõeldud andmestiku terviklik või osaline väljavõte või kasutusmeetod. Levitus võib olla näiteks fail, tabel või teenus. Sageli ongi tegemist eri vormingutes ettevalmistatud failidega.

Levituse kirjeldamisel lähtutakse standardi DCAT 3.0 versioonist. Levituse kirjeldus võimaldab edasi anda täpsemat teavet andmestiku vormingu ja taaskasutamise tingimuste kohta. Levitus on DCATis rangelt eraldi olemina, millele saab kirjeldada pealkirja (title) nagu see on andmestikul. Eesti andmekirjelduse standardis käsitletakse levitust seotuna andmestikuga. Andmestikus on selleks kirjelduselement, mis viitab levitusele. Andmehalduse määruse ja väärtuslike andmetike rakendusmääruse skoobis olevate andmestike kirjeldamisel on kohustuslik vähemalt ühe levituse kirjeldamine.

**DCAT määratlus**
- Andmestiku kindlakujuline esitus. Andmestik võib olla kättesaadav mitmel erineval serialiseeritud kujul, nagu loomulikus keeles, meedia tüübis või vormingus, organiseerituna skeemi, ajalises ulatuses või ruumilises resolutsioonis, detailsuses või profiilis (mida saab täpsustada).[^12]

- A specific representation of a dataset. A dataset might be available in multiple serializations that may differ in various ways, including natural language, media-type or format, schematic organization, temporal and spatial resolution, level of detail or profiles (which might specify any or all of the above).

[^12]: Serialiseerimise all tuleb selles kontekstis mõista eelkõige andmestruktuuride või -objektide teisendamist kitsas tehnilises tähenduses mingisse vormingusse, et need andmed oleks salvestatavad failina või edastatavad erinevates võrkudes.


### 1.3.7 Andmetabel

Tabel on info esitamine ridade ja veergudena.[^13] Selle objektitüübi eraldi välja toomine mudelis ning seeläbi ka sellele eraldi kirjelduse tegemine on vajalik relatsiooniliste andmebaaside kirjeldamise kontekstis, mis koosnevad tabelitest. Andmetabel on selles mudelis esmajoones andmebaasi tabel, mis on andmekirjelduse detailse kirjelduse komponendi juures üks grupeeriv olem. Tabel seob veerud, mis on kirjeldatava relatsioonilise andmebaasi andmeelemendid.

Objektitüüpi andmed tabeli kujul ei tohi segi ajada tabeliga, mida käsitletakse kui eraldi andmestikku või levitust. Andmekirjelduste koostamisel on vaja arvestada tabeli kahetise tähendusega, milleks on tabel kui eraldi hallatav andmestik ja tabel relatsioonilises andmebaasis.

[^13]: Põhjalikum andmetabeli selgitus on andmekirjelduse juhises.


### 1.3.8 Andmeelement

Andmeelemendi kirjelduse moodustavad selle detailsed kirjelduselemendid. Andmeelemendi kirjeldus võimaldab aru saada elemendi tähendusest ja seostest teiste andmeelementidega.

Standardis toodud andmeelemendi kirjeldus on eelkõige mõeldud selleks, et relatsioonilise andmebaasi tabelite veerge oleks võimalik kirjeldada andmeelementidena ning moodustada kirjeldatud andmeelemendist andmesõnastiku kirje, nii et kirjeldatud andmeelementidest moodustub andmesõnastik. Andmeelementidest komplektide moodustamiseks on standardis eraldi olem andmeelementide grupp.

Standardis on kirjelduselemendid esitatud andmekataloogi vaatest eesmärgiga andmeelemendid identifitseerida, neid omavahel seostada ning siduda andmesõnastikuga. Organisatsioonis juba kasutusel olev andmeelementide kirjeldus võib seega olla osaks loodavast andmekataloogist. Andmekataloogis võib kirjeldus sisaldada põhjalikumat teavet andmeelemendi tehnilise realisatsiooni, seotuse kohta ärireeglitega ja andmekvaliteedinõuete kohta (korduvus, kohustuslikkus, vaikeväärtused, täitmise reeglid jt).


### 1.3.9 Andmeelementide grupp

Andmeelementide grupi moodustavad sisuliselt seotud andmeelemendid. Tavaliselt on normaalkujule viidud relatsioonilises andmebaasis sisuliselt grupeeruvad elemendid eraldi tabelites. Vajadus andmeelemente grupeerida tuleneb vajadusest mõista sisuliselt kokku kuuluvaid, kuid tehniliselt laiali olevate andmeelementide tähendust. Ei ole aga ka välistatud juhud, kus tabeli moodustavadki grupeeruvad andmeeleemendid. Näiteks on koha-aadress eraldi tabelis.

Tehniliselt on relatsioonilises andmebaasis loogilist kirjet moodustavad tunnused tavaliselt eri veergudes. Samas kirje võib olla ühe või mitme objekti ja toimunud sündmuse kohta. Näiteks lapse sünnil on ema ja laps oma tunnustega ning mitmesugused sünniga seotud tunnused. Need moodustavad loomulikke ja koos kasutatavaid või ainult koos sisulist tähendust omavaid gruppe.

Lisaks eksisteerib olukordi, kus ei ole lubatud avalikustada detailseid andmekirjeldusi andmeelementide tasemel, kuid on lubatud seda teha grupeeritud tasemel. Samuti on sageli otstarbekas siduda ärimõisteid andmeelementide grupiga. Näiteks sama sünni näite korral on üks isik ’rollis’ ema ja teine ’rollis’ laps. Kindlas kontekstis võib andmeelement ja andmesõnastiku termin näiteks olla: ’ema kaal enne rasedust’, mis on üks andmeelement grupis ’rasedusjärgne jälgimine’.


### 1.3.10 Andmeteenus

Standard käsitleb andmeteenust DCAT 3.0 versiooni kontekstis. Andmeteenusel puudub ühene seos avaliku sektori asutuste muude teenuse käsitlustega. Tegemist on andmekataloogi pealt, mis ei ole teenuste kataloog, osutatava teenusega, kasutades andmestikke. Samas võivad andmekataloogis loetletud teenused olla seotud muude teenustega. Muude teenuste all on silmas peetud digi- ja muid avalikke teenuseid nagu otsene või tugiteenus (TKTA teenused[^14]), samuti planeerimis- ja finantsvaate teenuseid (TERE teenused[^15]) kui ka tehnilised teenused (X-tee teenused[^16]).

Andmeteenuste kirjeldus on kuvatav kataloogis teenuste nimekirjana ning teenus on seotud andmestiku ja selle levitustega.

**DCAT määratlus**
- Operatsioonide kogum, mis võimaldab juurdepääsu ühele või enamale andmestikule või andmetöötlusfunktsioonile
- A collection of operations that provides access to one or more datasets or data processing functions.

[^14]: Avalike digiteenuste disainimise tööriistakast. [Avalike teenuste kataloog](https://digiriik.eesti.ee/juhend/avalike-teenuste-kataloog)
[^15]: Tegevuspõhise eelarvestamise käsiraamat. [4.3.5. Teenused](https://www.fin.ee/riigi-rahandus-ja-maksud/riigieelarve-ja-eelarvestrateegia/tegevuspohise-eelarvestamise-kasiraamat/teenused)
[^16]: [X-tee alamsüsteemide kataloog teenuste ja WSDL kirjeldustega](https://x-tee.ee/catalogue/EE)


### 1.3.11 Andmesõnastik ja ärisõnastik

Standardi teiseks komponendiks on sõnastikud, mida on kahte tüüpi: andmesõnastik ja ärisõnastik.[^17] Sõnastikud on oluline semantilise veebi komponent. Sõnastike olulisus seisneb peamiselt selles, et need muudavad nii tehnilistele kui mittetehnilistele töötajatele andmed arusaadavaks ja kasutatavaks. Teisisõnu aitavad need andmeid linkida ja taaskasutada.

Andmesõnastik on ühelt poolt terminite nimekiri ning teiselt poolt esitab terminitena andmeelementide nimetused (pealkirjad).

Ärisõnastik, mis esitab valdkonnas või organisatsioonis kasutatavad mõisted ning nende tähistamiseks kasutatavad sõnad ehk terminid ja võimaldab mõistelist arusaamist kasutatavast sõnavarast. Ärisõnastik on organisatsiooni või organisatsioonide üleselt kokku lepitud sõnavara, mida ohjatakse.

Sõnavara ohjamine (vocabulary control)[^18] tähendab seda, et mõisted, eriti põhimõisted, peaksid olema terminoloogiliselt kokku lepitud ja sisuliselt määratletud. Sageli on vajalik, et ärisõnastik oleks mitmekeelne. Ärisõnastikke võib asutusel olla üks või mitu. Ärisõnastik võib pärida termineid ja mõistete määratlusi valdkonna sõnastikest, terministandarditest või üldistest märksõnastikest, kui viimased on olemas.

[^17]: Põhjalikum sõnastike selgitus on andmekirjelduse juhises.
[^18]: Ohjatav ehk kontrollitud sõnavara (vocabulary control) moodustab märksõnastiku (controlled vocabulary). EVS-ISO 25964-1:2023 määratleb (2.12), et märksõnastik ehk kontrollitud märksõnastik on mõisteid tähistavate terminite, märksõnade või koodide ettekirjutatud loetelu.


### 1.3.12 Andmesõnastiku ja ärisõnastiku termin

Sõnastikud koosnevad terminitest. Terminid on mõistete sõnalised esitused. Harvem võivad terminid olla ka lühendid, sõned või muud märgid.

Andmesõnastiku termin on sõna või fraas, mis võib olla kindla määratlusega ja kindlast terminiallikast või ka mingi üldkeele sõna, millel definitsioon puudub. Kui definitsioon puudub või on tegu sõna või fraasiga, mida pole mõistlik määratleda, võib sel olla sõnaseletus.

Andmeelement võib olla tähistatud tähendust omava ja arusaadava sõnaga, aga võib olla ka akronüüm, lühend või muu sõne, mis on masinloetav, kuid pole lisaselgitusteta mõistetav. Andmeelemendi tähis on sageli andmemudelis ning võib seetõttu olla inglise keelne. Lisaks tähisele on andmeelemendil kirjeldus, mille aluseks on andmemudel ja mis sageli on andmebaasis andmeelemendi kommentaarina. Praktiline on teha andmeelementidele nimetused (pealkirjad) ning esitata need andmesõnastiku terminitena. Andmesõnastiku terminile lisatakse vajadusel määratlus või selgitus. Andmeelemendi kirjeldus võib sisaldada sõnu, millest andmesõnastiku termin moodustub. Andmesõnastiku terminid on soovitatav luua konteksti avavalt, mis tähendab, et need on pigem liitterminid või terved terminifraasid. Andmesõnastiku terminites kajastuvad mõisted, mille kohta need terminid käivad.

Ärisõnastiku terminid esitavad mingi valdkonna, andmekogu, laiema protsessi (teenuse) ja harvem andmestike sarja või andmestiku oskussõnavara. Oskussõnavara esitamine andmestiku kirjelduses on tavalisem siis, kui tegemist on uuringut, analüüsi või statistikat esitava andmestikuga, kus tunnused (andmeelemendid) esitavad kindlate definitsioonidega näitajaid, arvandmeid, muutujaid.

Ärisõnastik on mõistete ja terminite kogum, mida kasutatakse asutuses igapäevaselt rääkides või mis on kasutusel õigusaktides või tehnoloogias. Ärisõnastik peaks olema organisatsiooni tegevuste ja andmete kohta piisavalt täielik. Samas peaks see olema mõisteid piisavalt üldistav (laiemad ja grupeerivad mõisted) ja detailiseeriv (kitsamad ja seotud mõisted) ning lisaks veel ohjama sõnavara.


## 1.4 Andmekirjelduse standardi kasutusjuhud

### 1.4.1 Integreeriv lähenemine andmekirjeldusele

Tervikliku või ka osalise andmekirjelduse koostamine, ajakohasena hoidmine, et see oleks kasutatav usaldusväärse allikana andmete leidmiseks, arusaamiseks ja kasutamiseks, on töömahukas. Selle tõttu on eriti oluline integreeriv lähenemine. See tähendab, et standardile vastavad kirjeldused tehtaks õigel ajal ja õiges kohas. Selliselt on ühekordne kirjeldamine taaskasutatav. Andmekirjelduse tuuma ja selgroo moodustab andmekataloog ja sellesse kataloogitud andmestikud. Neile luuakse ülevaatlik kirjeldus ning kui andmestikke kirjeldatakse sisuliselt, siis detailne kirjeldus. Semantilise komponendina on kirjelduse osaks sõnastikud. Sõnastikel võib olla terminiallikaid väljaspool organisatsiooni, kust on võimalik pärida valdkonna sõnavara.


![Joonis 2](images/joonis2.png)

*Joonis 2: Standardi käsitlusalas olevad andmekirjelduse komponendid ja olemid*


Integreeritud lähenemine võimaldab andmeid leida ja kasutada nii organisatsiooni sees kui kuvada või edastada andmekirjeldust, mõnikord koos andmetega, organisatsioonist välja.


### 1.4.2 Andmekirjeldus organisatsioonis kasutamiseks

Standardi peamiseks kasutusjuhuks on organisatsioonis andmekirjelduse koostamine enda tarbeks, et oleks parem ja selgem arusaam, mis andmed organisatsioonil on.

Organisatsiooni sees omakorda võib eristada mitmeid kasutusjuhtusid:
- Osa organisatsiooni teabe (info) tervikülevaatest, mis on andmekataloog, kus sarjadesse rühmitatud andmestikud on osa organisatsiooni teabe ja dokumentide liigitusskeemist.
- Omaette vaade andmete leidmiseks ja kasutamiseks, milleks on andmekirjeldus esitatud andmekataloogi kujul. Selle alla võib lugeda ka andmete ettevalmistamise nende avaandmetena avaldamiseks.
- Kasutamine organisatsiooni sees osana protsessist (ETL) või teenusest, kus andmetöötluse sisu on pigem üksikandmete (ühe kirje) edastamine teenusejuhtumi käigus.
- Kasutamine organisatsioonis aruande, statistika või muu infot koondava andmetöötluse tarbeks. Sellise töötluse osaks võib olla andmete edastamine andmelattu või muusse andmestruktuuri.


### 1.4.3 Andmekirjeldus kirjelduste avaldamiseks ja edastamiseks

Teise olulise rühma andmekirjelduse standardi kasutusjuhtudest moodustavad kirjelduste kasutamised edastamiseks organisatsioonist välja või kättesaadavaks tegemised organisatsiooni  portaalides. Andmekirjeldusi võib edastada  ainult kui metaandmeid ja sel juhul on andmestikule viide kui juurdepääsukohale. Samuti on võimalik, et metaandmed edastatakse koos andmestikuga.

Erilisel kohal on avaandmetena avaldamine. DCAT standardi kasutamine kirjelduste koostamise alusena on paljus tõukunud avaandmete eesmärgist ja kohustusest. See on aga seotud teiste kasutusjuhtudega, kui andmeid või andmekirjeldusi avaldatakse.

Andmekirjelduste edastamiseks organisatsioonist välja või organisatsiooni portaalis võib eristada mitmeid kasutusjuhtusid:
- Paljud organisatsioonid on loonud oma avaandmete portaalid, milles avaldavad andmestikke kas aruannete või statistikana või pakuvad juurdepääsu oma avaandmetele teenuste kaudu. Sellistes portaalides tehtud avaldamised peaks kasutama selles andmekirjelduse standardis esitatud kirjeldusstruktuure ja -elemente.

- Kuna andmestiku tasandi kirjeldus on loodud DCAT-AP-ga ühilduvana, siis võimaldab see vahetada – kasutades näiteks OAI-PMH andmevahetusprotokolli[^19] – andmeid Euroopa avaandmete portaaliga.[^20]

[^19]: [Open Archives Initiative Protocol for Metadata Harvesting](https://www.openarchives.org/pmh/)
[^20]: [European data](https://data.europa.eu/en)


# 2. Andmekataloogi ja selle olemite kirjelduselemendid

Kirjeldused põhinevad suures osas standardi DCAT-AP 3.0.0 versioonil. Lisatud on kirjelduselemendid, mis arvestavad riigi kesksete andmehaldust toetavate rakenduste nõuetega, milleks on RIHA, Eesti avaandmete teabevärav ja RIHAKE. Ära on jäetud andmekataloogi kirje (Catalog record) olem, mis ei ole Eestis kasutusel. Elemendid on järjestatud olemites alfabeetiliselt v.a juhul, kui olemil on alamelemente.

## 2.1 Andmekataloogi kirjeldus

| # | elemendi nimetus | määratlus ja kasutamine | kohustuslik / korduv | näide | DCAT-AP viide |
|----|--------------|--------------|--------------|--------------|----------------|
| 1 | kirjeldus | Kataloogi sisuline lühikirjeldus. Peaks iseloomustama andmestike, mida kataloog sisaldab. | 1..1 | Ruumiandmete lehelt leiad Maa-ameti ruumiandmete kirjeldused. | viide: [dcterms:description](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description)<br>- DCAT: [description](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_description)<br>- DCAT-AP: [description](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Catalogue.description)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Literal](https://www.w3.org/2000/01/rdf-schema#Literal)<br>- DCAT-AP: [Literal](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Literal) |
| 2 | omanik | Organisatsiooni nimetus, kes kataloogi peab. | 1..1 | Statistikaamet<br>Maksu-ja Tolliamet | viide: [dcterms:publisher](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#publisher)<br>- DCAT: [publisher](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_publisher)<br>- DCAT-AP: [publisher](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Catalogue.publisher)<br>vahemik:<br>DCAT-AP: [Agent](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Agent) |
| 3 | pealkiri | Kataloogi nimetus või tähis. | 1..1 | (Statistikaamet) Statistika andmebaas<br>(Maksu- ja Tolliamet) Statistika ja avaandmed | viide: [dcterms:title](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title)<br>- DCAT: [title](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_title)<br>- DCAT-AP: [title](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Catalogue.title)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Literal](https://www.w3.org/2000/01/rdf-schema#Literal)<br>- DCAT-AP: [Literal](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Literal) |
| 4 | veebisait | Viide veebisaidile, millel kataloog on juurdepääsetav. | 0..1 | https://andmed.stat.ee/ | viide: <br>- DCAT: [homepage](https://www.w3.org/TR/vocab-dcat-3/#Property:catalog_homepage)<br>- DCAT-AP: [homepage](https://xmlns.com/foaf/spec/)<br>vahemik:<br>DCAT-AP: [Document](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Document) |

## 2.2 Andmestiku kirjeldus

| # | elemendi nimetus | määratlus ja kasutamine | kohustuslik / korduv | näide | DCAT-AP viide |
|----|--------------|--------------|--------------|--------------|----------------|
| 1 | andmestiku identifikaator | Andmestikule omistatud unikaalne ja püsiv identifikaator.Identifikaatori võib omistada alliksüsteem või sihtsüsteem, näiteks Eesti andmete teabevärav. | 1..1 | 8289ed9-8472-44c4-958b-91cef59eaada<br>Selgitus: on GUID kujul ning seda võib kasutada URI osana | DCAT-AP: [Document](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Document) |
| 2 | andmete piirdaatumid | Ajavahemik, mille kohta on andmed olemas ja/või avaldatud.Kuupäev esitatakse ISO 8601-1 vormingus (AAAA-KK-PP/AAAA-KK-PP).<br>Märkus 1: andmete piirdaatumeid ei tohi segi ajada andmekogumise või -sisestamise piirdaatumitega, samuti andmestiku kasutusele võtmise kuupäevaga.<br>Märkus 2: algusdaatumiks arvatakse kirje tegemise (dokumenteerimise) fakti või aega, mitte seotud aeg minevikust (näiteks hoone ehitamine aastal 1882).Lõppdaatumi märkimine on võimalik ja tarvilik ainult lõpetatud andmestike kirjeldamisel. | 0..1 | 1993-11-05/2007-06-30<br>Selgitus: Andmestik katab sisus perioodi 1993-11-05/2007-06-30, mis on kohane ka piirdaatumitena märkimiseks, kuigi andmete avalikustamine toimus alles aastal 2003. | viide: [dcterms:temporal](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#temporal)<br>- DCAT: [temporal coverage](https://www.w3.org/TR/vocab-dcat-3/#Property:dataset_temporal)<br>- DCAT-AP: [temporal coverage](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.temporalcoverage)<br>vahemik: <br>- DCAT:(RDF) [dcterms:PeriodOfTime](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#PeriodOfTime)<br>- DCAT-AP: [Period of time](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Periodoftime) |
| 3 | andmete uuendamise regulaarsus | Andmestiku andmete uuendamise regulaarsus. Kirjelduselemendi väärtused võetakse ELi sageduste sõnastikust (EU Frequency Vocabulary).[^21] Täita juhul, kui andmete kogumine või loomine ei toimu pidevalt, vaid perioodiliselt. | 0..1 | Kord aastas | viide: [dcterms:accrualPeriodicity](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#accrualPeriodicity)<br>- DCAT: [frequency](https://www.w3.org/TR/vocab-dcat-3/#Property:dataset_frequency)<br>- DCAT-AP: [frequency](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.frequency)<br>vahemik: <br>- DCAT:(RDF) [dcterms:Frequency](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#Frequency)<br>- DCAT-AP: [Frequency](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Frequency) |
| 4 | andmestiku seos teise andmestikuga | Teave kirjeldatava andmestikuga hierarhiliselt või ajaliselt seotud teiste andmestike kohta. | 0..n | b49f330-e207-430e-87dd-ca8d5859438b; isPartOf<br>Selgitus: kirjeldatav andmestik “Riigikogu valimiste andmed” on osa (isPartOf) andmestikust “Valimiste andmed” (identifikaatoriga: 8b49f330-e207-430e-87dd-ca8d5859438b)  | - |
| 4.1 | seotud andmestiku identifikaator | Andmestikuga seotud teise andmestiku identifikaator. | 1..1 | 8b49f330-e207-430e-87dd-ca8d5859438b | - |
| 4.2 | seose tüüp | Andmestike vahelise seose tüüp Dublin Core seoste klassifikaatori alusel. Täpsemalt on Eesti andmekirjelduse standardis kasutusel neli seose tüüpi:<br>- isPartOf (kirjeldatav andmestik on osa teisest andmestikust)<br>- hasPart (kirjeldatav andmestik sisaldab teist andmestikku)<br>- replaces (eelkäija; kirjeldatav andmestik asendab teist andmestikku)<br>- isReplacedBy (järeltulija; kirjeldatavat andmestikku asendab teine andmestik) | 1..1 | Selgitus: isPartOf ja hasPart on kasutusel andmestiku ja alamandmestiku juures.<br>Selgitus: replaces ja isReplacedBy on kasutusel juhul kui tegemist on n-ö versioneeritavate andmestikega. | viide: [dcterms:isPartOf](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#isPartOf)<br>viide: [dcterms:hasPart](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#hasPart)<br>- DCAT: [has part](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_has_part)<br>viide: [dcterms:replaces](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#replaces)<br>- DCAT: [replaces](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_replaces)<br>viide: [dcterms:isReplacedBy](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#isReplacedBy) |
| 5 | andmesõnastiku nimi | Sõnastiku pealkiri.<br>Soovitatav on andmesõnastiku pealkirjas kasutada sõnastikule vastava andmestiku ja selle domeeni nimetusi.<br>Märkus: RIHAKEses on kasutusel “Nimetus“. | 1..1 | Loomeliitude andmekogu (LLA) andmesõnastik | - |
| 6 | andmete päritolu |  Teise andmestiku pealkiri, mida on  kasutatud kirjeldatava andmestiku loomiseks ja/või täiendamiseks.<br>Märkus: Mitte segi ajada andmestiku seostega isPartOf ja hasPart, mille abil seotakse omavahel andmestiku ülem- ja alamkomponendid.  | 0..n | TaimekasvatusSelgitus: Kirjeldatavas andmestikus „Taimekaitsevahendite kasutamine“ on taaskasutatud põllukultuuride kasvupinna andmeid andmestikust „Taimekasvatus“.Andmekogude puhul: Maakataster (MIS)Selgitus: Ehitise aluse maaüksuse katastritunnused ehitisregistris on pärit maakatastrist. | - |
| 6.1 | päritolu andmestiku pealkiri | Andmekogu korral on andmestiku pealkirjaks selle pidamist reguleerivas õigusaktis toodud ametlik nimetus.Muu andmestiku puhul selle praktikas kasutatav täielik nimetus. Üksikutest tabelitest koosneva andmestike defineerimisel tuleb pealkirjastamisel lähtuda tabelite pealkirjastamise reeglitest. | 1..1 | Taimekasvatus<br>Andmekogude puhul: Maakataster (MIS) | viide:<br>- DCAT-AP: [provenance](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#provenance)<br>vahemik:<br>- DCAT-AP: [Provenance Statement](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#ProvenanceStatement) |
| 6.2 | päritolu andmestiku URI | Vastavalt kokkuleppele konstrueeritud viide URI-vormingus. | 0..1 | b49f330-e207-430e-87dd-ca8d5859427b<br>Selgitus: ühele andmestikule vastav URI | - |
| 7 | geograafiline kaetus | Andmetega kaetud piirkond või asukoht.<br>Märkus: geograafilise kaetuse märkimisel tuleb kasutada piirkonna tekstilist nimetust (näiteks: “Harju maakond”) ja/või bounding box vormingus koordinaatide esitust.<br>Märkus: kui geograafiline kaetus on märkimata, arvestatakse selle väärtuseks vaikimisi „kogu Eesti“. | 0..n | - | - |
| 7.1 | asukoha nimetus | Piirkonna või asukoha sõnaline nimetus.<br>Eesti asukohtade märkimisel on soovituslik kasutada Eesti haldus- ja asustusjaotuse klassifikaatoris (EHAK) ja kohanimeregistris (KNR) toodud väärtusi.[^22] <br>Välismaiste asukohtade märkimisel on soovituslik kasutada GeoNames kohanimede loetelu.[^23] <br>Märkus: Eesti andmestike puhul on üldjuhul kohane märkida piirkond riigi, maakonna või kohaliku omavalitsuse tasemel. | 0..1 | kogu Eesti;<br>Harju maakond, Kiili vald | viide: [dcterms:spatial](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#spatial)<br>- DCAT: [spatial/geographic coverage](https://www.w3.org/TR/vocab-dcat-3/#Property:dataset_spatial)<br>- DCAT-AP: [geographical coverage](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.geographicalcoverage)<br>vahemik: <br>- DCAT:(RDF) [dcterms:Location](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#Location)<br>- DCAT-AP: [Location](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Location) |
| 7.2 | asukoha koordinaadid | Piirkonna või asukoha määratlus koordinaatsüsteemis.<br>Asukoha koordinaadid tuleb märkida *bounding box* kujul, ehk kahe pikkuskraadi ja kahe laiuskraadi alusel moodustuva väikseima ristkülikuna, mille piiridesse andmed jäävad.<br>Koordinaadid tuleb esitada rahvusvahelises geodeetiliste koordinaatide süsteemis WGS 84 kümnendkraadides vähemalt kahe kümnendkoha täpsusega.<br>Märkus: Integreeritava aadressiotsingu (In-ADS) kasutamisel geograafilise kaetuse märkimiseks esitatakse asukoha koordinaadid automaatselt, asukoha nimetuse valimisel. | 0..1 | x": "6456676.27"<br>"y": "641451.91"<br>"b": "58.22807"<br>"l": "26.40804" | - |
| 8 | avalikustamise kuupäev | Ametliku avalikustamise kuupäev.<br>Kuupäev esitatakse ISO 8601-1 vormingus (AAAA-KK-PP).<br>Märkus: on kasutusel avaandmete puhul | 0..1 | 2022-05-25 | viide: [dcterms:issued](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#issued)<br>- DCAT: [release date](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_release_date)<br>- DCAT-AP: [release date](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.releasedate)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Literal](https://www.w3.org/2000/01/rdf-schema#Literal)<br>- DCAT-AP: [Temporal Literal](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#TemporalLiteral) |
| 9 | HVD kategooria | Väärtusliku andmestiku (HVD – *high value dataset*) kategooria vastavalt rakendusmäärusele.[^24]<br>2023 lõpus on määratletud kuus väärtuslike andmestike kategooriat: 1) georuumilised andmed; 2) maa seire ja keskkond; 3) meteoroloogiateave; 4) statistika; 5) äriühingud ja äriühingu omandisuhted ning 6) liikuvus.<br>Kirjelduselemendi kasutamine on kohustuslik väärtuslike andmestike kirjeldamisel. | 0..n | [high-value-dataset-category.rdf]()<br>- georuumilised andmed;<br>- maa seire ja keskkond;<br>- meteoroloogiateave;<br>- statistika;<br>- äriühingud ja äriühingu omandisuhted;<br>- liikuvus. | - |
| 10 | juurdepääsutase | Andmestiku juurdepääsutaseme kirjeldus.[^25]<br>Juurdepääsutaseme kirjeldamisel tuleb rakendada Euroopa Liidu Ametlike Teadaannete Talituse poolt loodud kontrollitud sõnastiku väärtuseid:<br>- konfidentsiaalne (*confidential*)<br>- mitteavalik (*non-public*)<br>- avalik (*public*)<br>- piiratud (*restricted*)<br>- tundlik (*sensitive*)<br>Märkus: Juurdepääsutaseme märkimine on kohustuslik andmehalduse määruse skoopi kuuluvate andmestike puhul.<br>[^26]Märkus: Eestis on üldjuhul juurdepääsutaseme märkimisel vaja kasutada väärtusi “avalik” või “piiratud”. | 0..1 | avalik<br>piiratud | viide: [dcterms:accessRights](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#accessRights)<br>- DCAT: [access rights](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_access_rights)<br>- DCAT-AP: [access rights](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.accessrights)<br>vahemik: <br>- DCAT:(RDF) [rdfs:RightsStatement](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#RightsStatement)<br>- DCAT-AP: [Rights Statement](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Rightsstatement) |
| 11 | kasutusele võtmise kuupäev | Andmestiku elektroonilise pidamise algusaeg. Kattub enamasti esimese vastava andmestiku kogumiseks, haldamiseks ja avaldamiseks loodud infosüsteemi kasutusele võtmise kuupäevaga.<br>Kuupäev esitatakse ISO 8601-1 vormingus (AAAA-KK-PP).[^27]<br>Märkus: mitte segi ajada elemendiga „andmete piirdaatumid“.<br>Märkus: on kohustuslik andmekogude jaoks, milles see on andmekogu kasutusele võtmise kuupäev | 0..1 | 2010-01-01<br>Selgitus: Andmete infosüsteemi sisestamise, seega kasutusele võtmise kuupäeva jaoks sobiv aasta on 2010; samas paberkujul olid andmed olemas 1992. aastast. | - |
| 12 | keel | Andmestikus kasutatud keel(ed). Kui kirjeldus pole täidetud, eeldatakse vaikimisi eesti keele kasutamist.<br>Andmevahetuses kasutatakse ISO 639-2 standardi alusel defineeritud kolmetähelisi keele koode.[^28] | 0..n | est, ukr | viide: [dcterms:language](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#language)<br>- DCAT: [language](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_language)<br>- DCAT-AP: [language](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.language)<br>vahemik: <br>- DCAT:(RDF) [rdfs:LinguisticSystem](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#LinguisticSystem)<br>- DCAT-AP: [Linguistic system](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Linguisticsystem) |
| 13 | kirjeldus | Andmete sisuline lühikirjeldus ja andmetega seotud üldiste eesmärkide kirjeldus.<br>Andmekogu kirjeldus on selle asutamise õigusaktis toodud andmete kogumise eesmärk ja andmestiku sisu kirjeldus.<br>Märkus: mitte segi ajada elemendiga „koostamiseesmärk“, mille abil kajastatakse (organisatsiooni) funktsioone ja tegevusi, mille käigus andmed tekivad. | 1..1 | Ehitisregister on andmekogu, mille eesmärk on hoida, anda ja avalikustada teavet kavandatavate, ehitatavate ja olemasolevate ehitiste ning nendega seotud menetluste kohta.<br>Selgitus: andmekogu eesmärk põhimäärusest. | viide: [dcterms:description](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#description)<br>- DCAT: [description](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_description)<br>- DCAT-AP: [description](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.description)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Literal](https://www.w3.org/2000/01/rdf-schema#Literal)<br>- DCAT-AP: [Literal](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Literal) |
| 14 | kirjelduse muutmiskuupäev | Andmestiku kirjelduse viimase muutmise kuupäev.<br>Kuupäev esitatakse ISO 8601-1 vormingus (AAAA-KK-PP). | 0..1 | 2020-05-25 | viide: [dcterms:modified](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#modified)<br>- DCAT: [update/modification date](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_update_date)<br>- DCAT-AP: [modification date](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.modificationdate)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Literal](https://www.w3.org/2000/01/rdf-schema#Literal)<br>- DCAT-AP: [Temporal Literal](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#TemporalLiteral) |
| 15 | kohalduvad õigusaktid | Viide andmestikule kohalduvale Euroopa Liidu õigusaktile, mis reguleerib andmestiku ja/või andmestiku kirjelduse avaldamist ja avaldamisele kohalduvaid nõudeid.<br>Kohalduva õigusakti märkimine on kohustuslik kõrgväärtuslike andmestike rakendusmääruse (HVD), avaandmete direktiivi (ODD) ja Euroopa andmehalduse määruse (DGA) kohaldamisalasse kuuluvate andmestike puhul. Samas on kirjelduselementi lubatud kasutada ka muude õigusaktide (näiteks INSPIRE) kohaldumisel. | 0..n | http://data.europa.eu/eli/reg_impl/2023/138/oj<br>Selgitus: kasutada väärtuslike andmestike rakendusmääruse kohaldumisel.<br>http://data.europa.eu/eli/reg/2020/868/oj<br>Selgitus: Euroopa andmehalduse määruse kohaldumisel. | viide:<br>- DCAT-AP: [applicable legislation](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.applicablelegislation)<br>vahemik:<br>- DCAT-AP: [Legal Resource](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#LegalResource) |
| 16 | kontaktpunkt | Andmestiku kontakt: organisatsioon või üksikisik ning alamelementidena kontaktandmed.[^29]<br>Märkus: kasutatakse vCard ontoloogiat, millest omakorda on kasutusel kolm alamelementi (nimi, e-posti aadress, telefoninumber).[^30] | 0..n | Kultuuriministeerium, min@kul.ee, (372) 628 2222<br>Selgitus: organisatsiooni kontaktandmed.<br>Jüri Tamm, jyri.tamm@mmit.ee, (372) 678 9012<br>Selgitus: üksikisiku kontaktandmed. | viide: [dcat:contactPoint](https://www.w3.org/ns/dcat#contactPoint)<br>- DCAT: [contact point](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_contact_point)<br>- DCAT-AP: [contact point](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.contactpoint)<br>vahemik: <br>- DCAT:(RDF) [vcard:Kind](https://www.w3.org/TR/vcard-rdf/#d4e1819)<br>- DCAT-AP: [Kind](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Kind) |
| 16.1 | kontakti nimi | Kontakti täisnimi. Igas kontakti kirjes peab sisalduma täpselt üks nimi. | 1..1 | Kultuuriministeerium<br>Selgitus: organisatsiooni nimi.<br>Jüri Tamm<br>Selgitus: kontaktisiku nimi. | - |
| 16.2 | kontakti e-posti aadress | Kontakti e-posti aadress. Igas kontakti kirjes peab sisalduma vähemalt üks kahest, kas e-posti aadress või telefoninumber. | 0..1 | min@kul.ee<br>Selgitus: organisatsiooni e-posti aadress.<br>jyri.tamm@mmit.ee<br>Selgitus: kontaktisiku e-posti aadress. | - |
| 16.3 | kontakti telefoninumber | Kontakti telefoninumber. Igas kontaktikirjes peab sisalduma vähemalt üks kahest, kas e-posti aadress või telefoninumber.<br>Telefoninumber peab olema esitatud ITU-T E.123 soovituses ette nähtud notatsioonis. | 0..1 | (372) 678 9012 | - |
| 17 | levituse identifikaator | Viide andmestiku baasil loodud levitusele.<br>Märkus: Andmehalduse määruse ja väärtuslike andmestike rakendusmääruse skoobis olevate andmestike kirjeldamisel on kohustuslik vähemalt ühe levituse kirjeldamine. | 0..n | 336a3add-efc9-40dc-8830-091205fe20a5 | - |
| 18 | lühinimetus | Andmestikule viitamisel kasutatav lühinimetus, mis on sageli akronüüm.<br>Kui andmestik (andmekogu) on juba RIHAs kirjeldatud, kasutatakse RIHA lühinimetust. Andmekogude korral on lühinimetuse kasutamine kohustuslik. | 0..1 | haudi<br>Selgitus: Järva valla kalmistregistri lühinimetus.<br>LLA<br>Selgitus: Loomeliitude andmekogu lühinimetus. | - |
| 19 | muu identifikaator |  Teisene viit andmestikule, näiteks DOI, valdkonnapõhine andmestiku identifikaator vms.<br>Märkus: HVD andmestiku kirjeldusprofiili puhul soovituslik kirjelduselement. | 0..n | doi: 10.1308/11340470510582432 | viide:<br>- DCAT-AP: [other identifier](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.otheridentifier)<br>vahemik:<br>- DCAT-AP: [Identifier](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Identifier) |
| 19.1 | muu identifikaatori tüüp | Identifikaatori tüüp. | 0..1 | doi | - |
| 19.2 | muu identifikaatori väärtus | Teisene viit andmestikule. | 1..1 | 10.1308/11340470510582432  | - |
| 20 | märksõna | Kontrollitud märksõnastikust võetud üks või mitu andmestiku sisu iseloomustavat märksõna. Märksõna on märksõnastamise käigus dokumendile (siin andmestikule) määratud termin. Märksõnastik on mõisteid tähistavate terminite, märksõnade või koodide ettekirjutatud loetelu.<br>Andmestiku märksõnastamisel kasutatakse üldist või valdkondlikku märksõnastikku. Nendeks võivad olla Eesti märksõnastik ([EMS](https://ems.elnet.ee/index.php)), [EuroVoc](https://op.europa.eu/et/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/eurovoc) või muu. | 0..n | - | - |
| 20.1 | märksõna termin | Märksõna tekstiline esitus. | 1..1 | ehitus, arhitektuur | viide: [dcat:keyword](https://www.w3.org/ns/dcat#keyword)<br>- DCAT: [keyword/tag](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_keyword)<br>- DCAT-AP: [keyword](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.keyword)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Literal](https://www.w3.org/2000/01/rdf-schema#Literal)<br>- DCAT-AP: [Literal](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Literal) |
| 20.2 | märksõna URI | Märksõna viide URI-vormingus. Kui kasutatavas märksõnastikus on URI-d, siis pannakse URI iga märksõna kohta. | 0..1 | https://ems.elnet.ee/id/EMS008645  | - |
| 21 | omanik | Andmestiku sisu haldav organisatsioon, kes andmestikku levitab. | 1..1 | Kliimaministeerium<br>Selgitus: ehitisregistrit haldav organisatsioon. | viide: [dcterms:publisher](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#publisher)<br>- DCAT: [publisher](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_publisher)<br>- DCAT-AP: [publisher](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.publisher)<br>vahemik:<br>- DCAT-AP: [Agent](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Agent) |
| 22 | pealkiri | Andmekogu korral on andmestiku pealkirjaks selle pidamist reguleerivas õigusaktis toodud ametlik nimetus.<br>Muu andmestiku puhul praktikas kasutatav täielik nimetus. Üksikutest tabelitest koosneva andmestike defineerimisel tuleb pealkirjastamisel lähtuda tabelite pealkirjastamise reeglitest. | 1..1 | Andmekogu: EhitisregisterSelgitus: Ehitisregistri põhimääruses on registri ametlik nimetus ehitisregister.Muu andmestik (kuup): Maakondade vaheline ränne soo järgi.Selgitus: Statistikaameti andmebaasis kuubi pealkiri. | viide: [dcterms:title](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#title)<br>- DCAT: [title](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_title)<br>- DCAT-AP: [title](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Catalogue.title)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Literal](https://www.w3.org/2000/01/rdf-schema#Literal)<br>- DCAT-AP: [Literal](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Literal) |
| 23 | seotud tegevused |  Loetelu organisatsiooni ülesannetest / teenustest, mille käigus andmestik tekib ja täieneb.<br>Andmekogu korral sisestada selle asutamise õigusaktis toodud tegevused. Muude andmestike puhul või kui õigusakt tegevusi ei kajasta, organisatsiooni teabe/dokumentide liigitusskeemis toodud sobivad funktsioonid või sarjade aluseks olevad tegevused.<br>Märkus: mitte segi ajada elemendiga „kirjeldus“, milles esitatakse ülevaade andmestiku sisust (kogutavatest andmetest) ja andmekogumise eesmärkidest. | 0..n | sündmuse registreerimine; ehitise rekonstrueerimisvigade ja lammutamise põhjuste analüüsimine; statistika ja teadusliku uurimistöö tegemine<br>Selgitus: andmetega seotud ülesanded. | viide: [prov:wasGeneratedBy](https://www.w3.org/TR/prov-o/#wasGeneratedBy)<br>- DCAT: [was generated by](https://www.w3.org/TR/vocab-dcat-3/#Property:dataset_was_generated_by)<br>- DCAT-AP: [was generated by](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.wasgeneratedby)<br>vahemik: <br>- DCAT:(RDF) [prov:Activity](https://www.w3.org/TR/prov-o/#Activity)<br>- DCAT-AP: [Activity](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Activity) |
| 24 | tüüp | Kirjeldatava andmestiku tüüp Dublin Core Type Vocabulary[^31] loendi alusel.<br>Märkus: Vaikimisi on kirjelduselemendi väärtuseks "dataset" ehk andmestik. Saab kasutada ka muud väärtust, näiteks "text" või "picture". | 0..1 | Dataset | viide: [dcterms:type](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#type)<br>- DCAT: [type/genre](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_type)<br>- DCAT-AP: [type](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.type)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Class](https://www.w3.org/2000/01/rdf-schema#Class)<br>- DCAT-AP: [Concept](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Concept) |
| 25 | valdkond | Andmestiku valdkond Eesti märksõnastiku ([EMS](https://ems.elnet.ee/index.php)), [EuroVoc](https://op.europa.eu/et/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/eurovoc) või muu alusel.<br>Märkus: avaandmete portaalis on EMSi valdkonnad seotud seal olevate valdkondadega, mis ühilduvad [Euroopa andmete ametliku portaali](https://data.europa.eu/et) valdkondadega (kategooriatega). | 1..n | - | - |
| 25.1 | ainevaldkond | Valdkonna nimetus EMSis, EuroVocis või mujal. | 1..1 | 44 EHITUS. SANITAARTEHNIKA | viide: [dcat:theme](https://www.w3.org/ns/dcat#theme)<br>- DCAT: [theme/category](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_theme)<br>- DCAT-AP: [theme](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.theme)<br>vahemik:<br>- DCAT-AP: [Concept](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Concept) |
| 25.2 | valdkonna URI | Vastavalt kokkuleppele konstrueeritud viide URI-vormingus. Kui kasutatavas märksõnastikus on URI-d, siis pannakse URI iga valdkonna märksõna kohta. | 1..1 | https://ems.elnet.ee/id/EMS023309 | - |
| 26 | vastab standardile | Tehniline vorming või standard, mis kehtestab andmetele põhjalikumad nõuded või struktuuri.<br>Märkus: HVD andmestiku kirjeldusprofiili puhul soovituslik kirjelduselement.  | 0..n | “Euroopa vähiregistrite käsiraamat ja standard”, mis koondab kõik soovitused ja juhised, mis on seni koostanud ENCRI-töörühmad, samuti Rahvusvahelise Vähiregistrite Assotsiatsiooni (IACR) koostatud ja võrgustiku poolt kohandatud soovitused. | viide: [dcterms:conformsTo](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#conformsTo)<br>- DCAT: [conforms to](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_conforms_to)<br>- DCAT-AP: [conforms to](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.conformsto)<br>vahemik: <br>- DCAT:(RDF) [dcterms:Standard](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#Standard)<br>- DCAT-AP: [Standard](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Standard) |
| 27 | veebisait | Viide veebisaidile, millelt saab ligipääsu andmestikule ja/või leiab rohkem teavet andmestiku taaskasutustingimuste ja -võimaluste kohta.<br>Märkus: Mitte segi ajada levituse kirjelduselemendiga „juurdepääsupunkt“. | 0..1 | https://www.ehr.ee/<br>Selgitus: ehitisregistri veebisait. | viide: [dcterms:landingPage](https://www.w3.org/ns/dcat#landingPage)<br>- DCAT: [landing page](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_landing_page)<br>- DCAT-AP: [landing page](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.landingpage)<br>vahemik: <br>- DCAT:(RDF) [foaf:Document](https://xmlns.com/foaf/spec/)<br>- DCAT-AP: [Document](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Document) |
| 28 | õiguslik alus | Andmestiku loomise ja haldamise aluseks oleva õigusakti nimetus ja link allikale.<br>Olemasolul õigusakti nimetus ja link (URL) Riigi Teatajas. Kui õigusakt ei ole Riigi Teatajas avaldatud, lisatakse organisatsiooni kodulehel avaldatud õigusakti link (URL).<br>Märkus: kirjeldusse ei kanta kaudselt andmestiku aluseks olevaid õigusakte,näiteks avaliku teabe seadus, Eesti Vabariigi põhiseadus, vaid ainult otseselt andmestiku aluseks olevaid seaduseid või määruseid.  | 0..n | - | viide: [dcterms:isReferencedBy](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#isReferencedBy)<br>- DCAT: [is referenced by](https://www.w3.org/TR/vocab-dcat-3/#Property:resource_is_referenced_by)<br>- DCAT-AP: [is referenced by](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Dataset.isreferencedby)<br>vahemik:<br>- DCAT-AP: [Resource](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Resource) |
| 28.1 | õigusakti nimetus |  Andmestiku loomise ja haldamise aluseks oleva õigusakti pealkiri. | 1..1 | Ehitisregistri põhimäärus | - |
| 28.2 | õigusakti link | Viide andmestiku aluseks olevale õigusaktile.<br>Märkus: Riigi Teatajas on võimalik esitada viide hetkel kehtivale tervikteksti versioonile: https://www.riigiteataja.ee/akt/115032019011?leiaKehtiv. Eelistada tuleb viitamist konkreetsele tervikteksti versioonile. | 1..1 | https://www.riigiteataja.ee/akt/105072023239 | - |

## 2.3 Andmestiku levituse kirjeldus

| # | elemendi nimetus | määratlus ja kasutamine | kohustuslik / korduv | näide | DCAT-AP viide |
|----|--------------|--------------|--------------|--------------|----------------|
| 1 | ajaline täpsus | Element viitab levituses sisalduvates andmetes minimaalsele eristatavale ajaperioodile. | 0..1 | tund<br>ööpäev<br>aasta | viide: [dcat:temporalResolution](https://www.w3.org/ns/dcat#temporalResolution)<br>- DCAT: [temporal resolution](https://www.w3.org/TR/vocab-dcat-3/#Property:distribution_temporal_resolution)<br>- DCAT-AP: [temporal resolution](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.temporalresolution)<br>vahemik: <br>- DCAT:(RDF) [xsd:duration](https://www.w3.org/TR/xmlschema11-2/#duration)<br>- DCAT-AP: [xsd:duration](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#xsd:duration) |
| 2 | andmete staatus | Element viitab levitatavate andmete kindlale kvaliteediseisundile.<br>Avaandmete teabevärav eristab nelja staatust: valmis, ebasoovitav, arenduses, mahavõetud. | 0..1 |valmis<br>ebasoovitav<br>arenduses<br>mahavõetud | viide:<br>- DCAT-AP: [status](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.status)<br>vahemik: <br>- DCAT-AP: [Concept](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Concept) |
| 3 | avalikustamise kestus | Kuupäev, millal levitus viimast päeva kättesaadav on.Kuupäev esitatakse ISO 8601-1 vormingus (AAAA-KK-PP) | 0..1 | 2025-06-31 | viide:<br>- DCAT-AP: [availability](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.availability)<br>vahemik: <br>- DCAT-AP: [Concept](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Concept) |
| 4 | HVD kategooria | Vt elemendi kasutamist andmestiku tabelis | 0..n | - | - |
| 5 | juurdepääsupunkt | Levituse kasutamist võimaldav või toetav veebileht. Esitab teavet andmestiku juurdepääsukoha kohta.<br>Märkus: mitte segi ajada andmestiku kirjelduselemendiga „veebisait“. Veebisait viitab andmestiku kui terviku kohta lisainfot andvale veebilehele, „juurdepääsupunkt“ asukohale kust on võimalik kirjeldatavat levitust kasutada (avaadmete levituse korral) või selle juurdepääsutingimuste kohta infot saada (piiratud juurdepääsuga levituste korral). | 1..n | https://andmed.stat.ee/et/stat/majandus__infotehnoloogia__infotehnoloogia-leibkonnas/IT621<br>Selgitus: viit statistika andmebaasi tabelile.<br>https://nma.vta.ee/<br>Selgitus: viit navigatsioonimärkide andmekogumile. | viide: [dcat:accessURL](https://www.w3.org/ns/dcat#accessURL)<br>- DCAT: [access URL](https://www.w3.org/TR/vocab-dcat-3/#Property:distribution_access_url)<br>- DCAT-AP: [access URL](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.accessURL)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Resource](https://www.w3.org/2000/01/rdf-schema#Resource)<br>- DCAT-AP: [Resource](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Resource) |
| 6 | juurdepääsutingimused | Levituse juurdepääsutingimusi põhjalikumalt kirjeldava veebilehe aadress või vabatekstiline juurdepääsuõiguste kirjeldus.<br>Märkus: kirjelduselemendi täitmine on kohustuslik andmehalduse määruse skoopi kuuluvate levituste puhul. | 0..1 | https://www.stat.ee/sites/default/files/2020-08/Konfidentsiaalsete%20andmete%20teaduslikel%20eesm%c3%a4rkidel%20edastamise%20kord%202015.pdf<br>Selgitus: Viidatud dokument selgitab põhjalikult statistikaameti põhimõtteid ja tingimusi konfidentsiaalsete andmete taaskasutamisel. | viide: [dcterms:rights](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#rights)<br>- DCAT: [rights](https://www.w3.org/TR/vocab-dcat-3/#Property:distribution_rights)<br>- DCAT-AP: [rights](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.rights)<br>vahemik: <br>- DCAT:(RDF) [dcterms:RightsStatement](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#RightsStatement)<br>- DCAT-AP: [Rights statement](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Rightsstatement) |
| 7 | kasutuslitsents | Kogu andmestikule kohalduv kasutuslitsents, kui see on määratud.<br>Elemendi täitmisel soovitatakse kasutada Creative Commonsi litsentse.[^32] | 0..1 | CC BY-SA 4.0 | viide: [dcterms:license](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#license)<br>- DCAT: [license](https://www.w3.org/TR/vocab-dcat-3/#Property:distribution_license)<br>- DCAT-AP: [license](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.licence)<br>vahemik: <br>- DCAT:(RDF) [dcterms:LicenseDocument](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#LicenseDocument)<br>- DCAT-AP: [License Document](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#LicenceDocument) |
| 8 | kohalduv õigusakt | Viide levitusele kohalduvale õigusaktile, mis reguleerib levituse avaldamist ja avaldamisele kohalduvaid nõudeid.<br>Kohalduva õigusakti märkimine on kohustuslik kõrgväärtuslike andmestike rakendusmääruse (HVD), avaandmete direktiivi (ODD) ja Euroopa andmehalduse määruse (DGA) kohaldamisalasse kuuluvate levituste puhul. Samas on kirjelduselementi lubatud kasutada ka muude õigusaktide (näiteks INSPIRE) kohaldumisel. | 0..n | http://data.europa.eu/eli/reg_impl/2023/138/oj<br>Selgitus: kasutada väärtuslike andmestike rakendusmääruse kohaldumisel.<br>http://data.europa.eu/eli/reg/2020/868/oj<br>Selgitus: Euroopa andmehalduse määruse kohaldumisel:<br>http://data.europa.eu/eli/dir/2019/1024/oj | viide:<br>- DCAT-AP: [applicable legislation](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.applicablelegislation)<br>vahemik:<br>- DCAT-AP: [Legal Resource](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#LegalResource) |
| 9 | levituse identifikaator | Viide andmestiku baasil loodud levitusele.<br>Märkus: Andmehalduse määruse ja väärtuslike andmestike rakendusmääruse skoobis olevate andmestike kirjeldamisel on kohustuslik vähemalt ühe levituse kirjeldamine | 1..1 | 336a3add-efc9-40dc-8830-091205fe20a5 | - |
| 10 | levituse vorming | Levituses sisalduvate andmete failivorming.<br>Vormingu märkimisel tuleb kasutada IANA poolt defineeritud vormingute loendit (nn mime-tüübid).[^33]<br>Märkus: kirjelduselemendi täitmine on kohustuslik andmehalduse määruse skoopi kuuluvate levituste puhul. | 0..1 | application/json<br>text/csv | viide: [dcterms:format](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#format)<br>- DCAT: [format](https://www.w3.org/TR/vocab-dcat-3/#Property:distribution_format)<br>- DCAT-AP: [format](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.format)<br>vahemik: <br>- DCAT:(RDF) [dcterms:MediaTypeOrExtent](https://www.dublincore.org/specifications/dublin-core/dcmi-terms/#MediaTypeOrExtent)<br>- DCAT-AP: [Media Type or Extent](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#MediaTypeorExtent) |
| 11 | levituse suurus | Levituse faili suurus baitides<br>Märkus: kirjelduselemendi täitmine on andmehalduse määruses toodudandmestike puhul kohustuslik, mh tuleb dünaamiliste teenuste kirjeldamisel väärtuseks märkida kogu andmestiku suurus. | 0..1 | 160000<br>Selgitus: levituse suuruseks on 160000 baiti, ehk ligikaudu 160 kB. | viide: [dcat:byteSize](https://www.w3.org/ns/dcat#byteSize)<br>- DCAT: [byte size](https://www.w3.org/TR/vocab-dcat-3/#Property:distribution_size)<br>- DCAT-AP: [byte size](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#Distribution.bytesize)<br>vahemik: <br>- DCAT:(RDF) [rdfs:Literal](https://www.w3.org/2000/01/rdf-schema#Literal)<br>- DCAT-AP: [xsd:nonNegativeInteger](https://semiceu.github.io/DCAT-AP/releases/3.0.0/#xsd:nonNegativeInteger) |

## 2.4 Andmestike sarja kirjeldus

## 2.5 Andmeteenuse kirjeldus

## 2.6 Andmebaasi tabeli kirjeldus

## 2.7 Andmeelemendi kirjeldus

## 2.8 Andmeelementide grupp

[^21]: 
    [EU Vocabularies – Controlled vocabularies – Frequency (versioon 20190619-0)](https://op.europa.eu/en/web/eu-vocabularies/dataset/-/resource?uri=http://publications.europa.eu/resource/dataset/frequency)
[^22]: 
     Kirjelduste loomisel on EHAK ja KNR nimetuste loomine võimalik Maa-ameti [integreeritava aadressiotsingu (In-ADS)](https://geoportaal.maaamet.ee/est/teenused/integreeritav-aadressiotsing-in-ads-p504.html) teenuse kaudu, mis võimaldab sobivalt täita ka asukoha koordinaadid (bbox).
[^23]: 
    [GeoNames](https://www.geonames.org/)
[^24]: Vt ka [avaliku teabe seadus](https://www.riigiteataja.ee/akt/104072017011?leiaKehtiv) § 4<sup>1</sup> Väärtuslikud andmestikud
[^25]: Eestis on piiratud tasemega teabe tähisena kasutusel termin AK (asutusesiseseks kasutamiseks), vt [avaliku teabe seadus](https://www.riigiteataja.ee/akt/104072017011?leiaKehtiv) § 34 Piiratud juurdepääsuga teave ja § 35 Teabe asutusesiseseks tunnistamise alused. Käesolev standard ei sätesta juurdepääsupiiragu määramist õigusakti täpse punkti tasemel.
[^26]: Euroopa Parlamendi ja nõukogu määrus (EL) 2022/868, 30. mai 2022, Euroopa andmehalduse kohta ning millega muudetakse määrust (EL) 2018/1724 ([andmehalduse määrus](https://eur-lex.europa.eu/legal-content/ET/TXT/?uri=CELEX:32022R0868)).
[^27]: [ISO 8601-1:2019 Date and time — Representations for information interchange — Part 1: Basic rules.](https://www.iso.org/standard/70907.html) Kuupäeva sisestamise kuju rakendustes on sellest esitusvormingust erinev ning tavaliselt kujul PP-KK-AAAA.
[^28]: [ISO 639-2:1998 Codes for the representation of names of languages — Part 2: Alpha-3 code](https://www.iso.org/standard/4767.html)
[^29]: Kontaktpunkti alamelementide kohustuslikkus ja korduvus kehtivad ühe kontakti kontekstis. Näiteks võib igas kontakti kirjes olla täpselt üks nimi, samas ei pruugi andmestiku kirjelduses kontakt olla üldse kirjeldatud (kontakti element ei ole kohutuslik) või on kirjeldatud mitu kontakti (kontakti element on korduv).
[^30]: [vCard Ontology - for describing People and Organizations (22 May 2014)](https://www.w3.org/TR/vcard-rdf/)
[^31]: [DCMI Type Vocabulary (2012-06-14)](https://www.dublincore.org/specifications/dublin-core/dcmi-type-vocabulary/)
[^32]: [Creative Commons licenses](https://creativecommons.org/share-your-work/cclicenses/)
[^33]: Internet Assigned Numbers Authority (IANA). [Media types](https://www.iana.org/assignments/media-types/media-types.xhtml).