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

Komponentidena on käsitletud andmestiku kui terviku ülevaatlikku kirjeldust,  andmestiku sisu  detailset kirjeldust ning sõnastike osa kirjeldust ehk mõistelist kirjeldust, mis aitab hallata sõnavara. 

Olemitena  on  käsitletud  andmekirjelduse  standardi  eraldi hallatavaid  ja  kirjeldatavaid objekte, mis koos moodustavad mudeli.  

Standard  on  koostatud  ühilduvana  DCAT-AP  3.0.0-ga.  See  võimaldab  organisatsioonidel andmekataloogis kirjeldada andmestikud ning nende levitused, rühmitada andmestikud sarjadesse. Standardis on samuti andmekataloogis kirjeldatud andmestike andmeteenuste osa. 

Standard  käsitleb andmestiku  struktuuri  detailset sisemist  kirjeldust. See on  kitsendatud tabeli kirjeldusega, mis on kas nimekirja või risttabeli kujul.


# 2. Admekataloogi ja selle olemite kirjelduselemendid

(WIP)