---
title: ER konfigūracijų kūrimas norint importuoti duomenis iš išorinių CSV failų
description: Naudokite šią procedūrą elektroninių ataskaitų (ER) konfigūracijoms kurti, kad iš išorinio CSV formato failo būtų galima importuoti duomenis į „Dynamics 365 for Finance and Operations“.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d3ea3d797de154979eae112658cf05d1914feeb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544937"
---
# <a name="design-er-configurations-to-import-data-from-external-csv-files"></a>ER konfigūracijų kūrimas norint importuoti duomenis iš išorinių CSV failų

[!include [task guide banner](../../includes/task-guide-banner.md)]

Naudokite šią procedūrą elektroninių ataskaitų (ER) konfigūracijoms kurti, kad iš išorinio CSV formato failo būtų galima importuoti duomenis į „Dynamics 365 for Finance and Operations“. Šioje procedūroje kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Norėdami atlikti šiuos veiksmus, pirmiausia turite užbaigti procedūros „ER: konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“ veiksmus. 

Ši procedūra sukurta vartotojams, kuriems priskirtas vaidmuo Sistemos administratorius arba Elektroninių ataskaitų teikimo programuotojas. Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį. 

Taip pat turite atsisiųsti ir įrašyti į savo kompiuterį šiuos failus: (https://go.microsoft.com/fwlink/?linkid=862266): 1099model.xml, 1099formatcsv.xml, 1099entriescsv.csv.

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Galite konfigūruoti procesą, skirtą importuoti išorinius failus XML, TXT arba CSV formatu į „Dynamics 365 for Finance and Operations“ programos leidimą. Pirmiausia turite sukurti abstraktų duomenų modelį, kuris verslo požiūriu atspindėtų importuotus duomenis – tam tikslui sukuriama ER duomenų modelio konfigūracija. Tada nurodykite importuoto failo struktūrą, kuri susieja sukurtą duomenų modelį, nes yra būdas nukreipti duomenis iš failo į abstraktų duomenų modelį – tam tikslui sukuriama ER formato konfigūracija. Tada ER duomenų modelio konfigūracija turi būti išplėsta įtraukiant naujo modelio susiejimą, kuriame aprašoma, kokiu būdu duomenys iš importuoto failo ir iš abstraktaus duomenų modelio išlaikyti duomenys naudojami norint atnaujinti programos lenteles arba duomenų objektus.  
    * Toliau nurodytuose veiksmuose vaizduojama, kaip išoriškai sekamos tiekėjų operacijos importuojamos iš išorinio CSV failo, kad vėliau jas būtų galima panaudoti atliekant tiekėjo 1099-ųjų formų sudengimą.   
    * Patikrinkite, ar pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra galimas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, pirmiausia turite atlikti procedūros „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu” veiksmus.  
2. Spustelėkite Ataskaitų konfigūracijos.
3. Taikykite filtrą „1099 mokėjimų modelis“. Jei jau atlikote procedūra „ER Reikiamų konfigūracijų kūrimas elektroninėse ataskaitose, norint importuoti duomenis iš išorinio failo“ ir konfigūracijų medyje galima pasirinkti konfigūraciją „1099 mokėjimų modelis“, praleiskite visus kitos antrinės užduoties veiksmus.   

## <a name="add-a-new-er-model-configuration"></a>Įtraukti naują ER modelio konfigūraciją
1. Užuot kūrę naują modelį, skirtą duomenų importavimui palaikyti, įkelkite anksčiau atsisiųstą failą 1099model.xml. Šiame faile yra tiekėjų operacijų pasirinktinių duomenų modelis. Šis duomenų modelis jau susietas su reikiamais duomenų komponentais.  
2. Spustelėkite Keitimas.
3. Spustelėkite Įkelti iš XML failo.
4. Spustelėkite Naršyti ir suraskite anksčiau atsisiųstą failą 1099model.xml.  
5. Spustelėkite GERAI.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Įtraukti naują ER formato konfigūraciją, kuri palaiko duomenų importavimą
1. Medyje pasirinkite „1099 mokėjimų modelis”.
2. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
3. Lauke „Naujas“ įveskite „Formatas pagal duomenų modelį 1099 mokėjimų modelis“.
4. Lauke Palaikomas duomenų importavimas pasirinkite Taip.
5. Norėdami uždaryti šį puslapį, paspauskite klavišą ESC.
    * Užuot kūrę naują ER formatą, skirtą duomenų importavimui palaikyti, įkelkite anksčiau atsisiųstą failą 1099formatcsv.xml. Šiame faile pateikiamas reikiamas gaunamo CSV failo struktūrą ir šios struktūros susiejimą su tiekėjų operacijų duomenų modeliu nulemiantis ER formatas.   
6. Spustelėkite Keitimas.
7. Spustelėkite Įkelti iš XML failo.
    * Spustelėkite Naršyti ir suraskite anksčiau atsisiųstą failą 1099formatcsv.xml.  
8. Spustelėkite GERAI.
9. Medyje išplėskite „1099 mokėjimų modelis”.
10. Medyje pasirinkite „1099 mokėjimų modelis\Skirtas tiekėjų operacijoms importuoti (CSV)“.

## <a name="review-format-settings"></a>Peržiūrėti formato parametrus
1. Spustelėkite Konstruktorius.
2. Spustelėkite Išplėsti / sutraukti.
3. Įjunkite „Rodyti išsamią informaciją”.
    * Sukurtas formatas atitinka numatytą išorinio CSV formatu pateikiamo failo struktūrą.  
4. Medyje pasirinkite „Gaunama: failas\Šaknis: seka“.
    * Naudojant šakninio elemento tipą SEQUENCE (seka) lauke „Specialieji simboliai“ pažymėta parinktis „Nauja eilutė – „Windows“ (CR LF)“. Pagal šį parametrą kiekviena analizavimo failo eilutė turi būti laikoma atskiru įrašu.   
5. Medyje pasirinkite „Gaunama: failas\Šaknis: seka\Eilutė: seka 1..* “.
    * Naudojant SEKA tipo elementą Šaknis\Eilutė, lauke „Įvairovė“ pažymėta parinktis „Vienas daug“. Pagal šį parametrą analizavimo faile sutaps mažiausiai viena eilutė.   
6. Medyje pasirinkite „Gaunama: failas\Šaknis: seka\Eilutė: seka 1..* \Tipai: atvejis“.
    * Atkreipkite dėmesį į tai, kad tipo ATVEJIS elementas Šaknis\Eilutė\Tipai įtrauktas kaip įdėtasis sekos Šaknis\Eilutė elementas. Kadangi šis CASE (atvejo) elementas apima 3 įdėtuosius sekos elementus, naudojant šį parametrą manoma, kad analizavimo faile yra tikimasi surasti 3 skirtingus eilučių tipus.   
7. Medyje pasirinkite „Gaunama: failas\Šaknis: seka\Eilutė: seka 1..* \Tipai: atvejis\Antraštė: seka 1..1 “.
    * Tipo SEKA elementas Šaknis\Eilutė\Tipai\Antraštė apima įdėtąjį elementą EILUTĖ, kurio reikšmė nurodyta kaip fiksuota eilutės reikšmė. Ši seka analizuoja analizavimo failo antraštės eilutę.   
8. Medyje pasirinkite „Gaunama: failas\Šaknis: seka\Eilutė: seka 1..* \Tipai: atvejis\Įrašas: seka 1..1 (,)“.
    * Sukonfigūruota, kad tipo SEKA elementas Šaknis\Eilutė\Tipai\Įrašas analizuotų operacijos eilutes. Atkreipkite dėmesį, kad simbolio parinktis „Pasirinktinis skyriklis“ sukonfigūruota kaip kablelis. Tai reiškia, kad analizavimo faile kablelis naudojamas kaip tokio tipo eilučių laukų skyriklis.   
    * Atkreipkite dėmesį į tai, kad, naudojant elementą Šaknis\Eilutė\Tipai\Įrašas ir norint analizuoti operacijos eilutes kaip atskirus laukus, buvo įtraukta keletas skirtingų duomenų tipų įdėtųjų elementų. Atkreipkite dėmesį į tai, kad pasirinkta parinkties „Pasiūlymų programa“ konfigūracija „Nėra“. Tai reiškia, kad analizės faile visi šio tipo laukai laikomi neturinčiais pridedamų simbolių.   
9. Medyje pasirinkite „Gaunama: failas\Šaknis: seka\Eilutė: seka 1..* \Tipai: atvejis\Įrašas: seka 1..1 (,)\OperacijosData: DataLaikas“.
    * Pavyzdžiui, sukonfigūruota, kad tipo DATALAIKAS elementas Šaknis\Eilutė\Tipai\Įrašas\OperacijosData iš analizavimo failo gautų operacijos datos ir laiko reikšmę formatu „M/d/mmmm“.   
10. Medyje pasirinkite „Gaunama: failas\Šaknis: seka\Eilutė: seka 1..* \Tipai: atvejis\Įrašas: seka 1..1 (,)\ŠaliesKodas: eilutė 0..1 “.
    * Atkreipkite dėmesį, kad sukonfigūruota, jog tipo EILUTĖ elementas Šaknis\Eilutė\Tipai\Įrašas\ŠaliesKodas lauke „Įvairovė“ turėtų parinktį „Nulis vienas“. Naudojant šį parametrą analizavimo eilutės lauko „CountryCode“ (šalies kodas) reikšmė laikoma pasirinktine.   
11. Medyje pasirinkite „Gaunama: failas\Šaknis: seka\Eilutė: seka 1..* \Tipai: atvejis\Įrašas: seka 1..1 (,)\Pastaba: seka 1..1 (,)“.
    * Atkreipkite dėmesį, kad sukonfigūruota, jog tipo SEKA elementas Šaknis\Eilutė\Tipai\Įrašas\Pastaba lauke „Pasiūlymų programa“ turėtų parinktį „Visi“, o lauke „Pasiūlymo žymė“ – dvigubų kabučių simbolį. Tai reiškia, kad analizavimo faile (aprašomame naudojant įdėtuosius elementus: tipo STRING (eilutė) tekstą) visi šio tipo eilučių laukai laikomi parašyti naudojant dvigubų kabučių simbolius.  
12. Medyje pasirinkite „Gaunama: failas\Šaknis: seka\Eilutė: seka 1..* \Tipai: atvejis\Neišanalizuota: seka 1..1 “.
    * Sukonfigūruota, kad tipo SEKA elementas Šaknis\Eilutė\Tipai\Neišanalizuota analizuotų viršuje pradiniame elemente ATVEJIS aprašytos struktūros neatitinkančios struktūros eilutes.   

## <a name="review-the-setting-of-the-format-mapping-to-the-data-model"></a>Peržiūrėti formato susiejimo su duomenų modeliu parametrą
1. Spustelėkite Susieti formatą su modeliu.
    * Modelio susiejime „Susiejimas su CSV formato modeliu“ aprašomas duomenų srautas, gautas perkeliant duomenis iš gaunamo CSV failo į duomenų modelį.   
2. Spustelėkite Konstruktorius.
3. Medyje išplėskite „format“.
    * Atkreipkite dėmesį, kad sukurtas formatas čia pateikiamas kaip duomenų šaltinio komponentas.  
4. Medyje išplėskite „formatas\Gaunama: failas(gaunama)“.
5. Medyje išplėskite „formatas\Gaunama: failas(gaunama)\Šaknis: seka(šaknis)“.
6. Medyje išplėskite „formatas\Gaunama: failas(gaunama)\Šaknis: seka(šaknis)\Eilutė: seka 1..* (eilutė)“.
7. Medyje išplėskite „formatas\Gaunama: failas(gaunama)\Šaknis: seka(šaknis)\Eilutė: seka 1..* (eilutė)\Tipai: atvejis(tipai)“.
8. Medyje išplėskite „formatas\Gaunama: failas(gaunama)\Šaknis: seka(šaknis)\Eilutė: seka 1..* (eilutė)\Tipai: atvejis(tipai)\Įrašas: seka 1..1 (,)(įrašas)“.
9. Medyje išplėskite „formatas\Gaunama: failas(gaunama)\Šaknis: seka(šaknis)\Eilutė: seka 1..* (eilutė)\Tipai: atvejis(tipai)\Įrašas: seka 1..1 (,)(įrašas)\Duomenys“.
10. Medyje išplėskite „formatas\Gaunama: failas(gaunama)\Šaknis: seka(šaknis)\Eilutė: seka 1..* (eilutė)\Tipai: atvejis(tipai)\Įrašas: seka 1..1 (,)(įrašas)\Duomenys\ŠaliesKodas: eilutė 0..1 (ŠaliesKodas)“.
11. Medyje išplėskite „formatas\Gaunama: failas(gaunama)\Šaknis: seka(šaknis)\Eilutė: seka 1..* (eilutė)\Tipai: atvejis(tipai)\Įrašas: seka 1..1 (,)(įrašas)\Duomenys\OperacijosData: DataLaikas (OperacijosData)“.
    * Atkreipkite dėmesį į tai, kad iš anksto numatytame „formato“ duomenų šaltinio komponente reikiami ir pasirenkami formato elementai, pavyzdžiui, „TransactionDate“ (operacijos data) ir „CountryCode“ (šalies kodas) atrodo skirtingai.   
12. Medyje išplėskite „Transactions = '$both'“.
    * Atminkite, kad formato, kuris nurodo importuoto failo struktūrą, elementai susieti su duomenų modelio elementais. Pagal šiuos susiejimus importuoto CSV failo turinys apdorojimo metu bus saugomas esamame duomenų modelyje. Atkreipkite dėmesį į elemento „CountryRegion“ (šalis ir regionas) susiejimą. Kai gaunamame faile naudojamas bet kuris operacijos elementas, kuriame nenurodyta šalies kodo reikšmė, į duomenų modelį įvedamas numatytasis šalies kodas „JAV”.   
13. Įjunkite „Rodyti išsamią informaciją”.
14. Spustelėkite skirtuką Tikrinimai.
15. Spustelėkite Ieškoti.
16. Lauke Rasti įveskite „tiekėjas”.
17. Spustelėkite Rasti kitą.
    * Šio formato susiejimas gali būti vartotojo nustatyta logika verslo požiūriu patikrinti importuotų duomenų tikslumą. Pvz., pagal parametrus, bet kai bet kuri importuojamo failo eilutės struktūra neatitinka nei antraštės eilutės struktūros, nei operacijos eilutės struktūros, sistemos pranešime rodomas įspėjamasis pranešimas ir vartotojai informuojami apie šį atvejį, nurodant failo operacijos eilės numerį.   
18. Uždarykite puslapį.

## <a name="run-the-format-mapping"></a>Paleisti formato susiejimą
Bandymams atlikti formato susiejimą vykdykite naudodami anksčiau atsisiųstą failą 1099entriescsv.csv. Sugeneruotoje išvestyje bus pateikiami iš pasirinkto CSV failo importuoti duomenys, kurie realiojo importo metu bus automatiškai įvesti į pasirinktinių duomenų modelį.   
1. Spustelėkite Vykdyti.
    * Spustelėkite Naršyti ir suraskite anksčiau atsisiųstą failą 1099entriescsv.csv.  
2. Spustelėkite GERAI.
    * Atkreipkite dėmesį į apie nepriimtas eilutes įspėjančius pranešimus. 4 eilutėje yra pajamų vertė, kuri pateikta nepriimtinu formatu, o 7 eilutėje nėra dvigubose kabutėse pateikiamos pastabos apie operaciją.   
    * Peržiūrėkite išvestį XML formatu, kuriuo rodomi iš pasirinkto failo importuoti ir į duomenų modelį perkelti duomenys. Atkreipkite dėmesį, kad apdorojamos visos 7 importuojamo CSV failo eilutės. Praleista 1 eilutė, kurioje nurodomi laukų pavadinimai, 4 operacijos išanalizuotos tinkamai, o 2 operacijos pripažintos netinkamomis.   
3. Uždarykite puslapį.
4. Uždarykite puslapį.

