---
title: Nuomos koregavimas
description: Straipsnyje paaiškinama, kaip koreguoti nuomą. Koreguoti gali reikėti, jei pakeičiamos nuomos sąlygos, nuoma pratęsiama arba pasikeičia kitos aplinkybės.
author: moaamer
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 48d1a261a43d6e3a68dfc0aae6f06c0d7d6b82db
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898333"
---
# <a name="adjust-leases"></a>Nuomos koregavimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Straipsnyje paaiškinama, kaip koreguoti nuomą. Koreguoti gali reikėti, jei pakeičiamos nuomos sąlygos, nuoma pratęsiama arba pasikeičia kitos aplinkybės. Turto nuoma atitinka rekomendacijas, kurios pateiktos 842 apskaitos standartų kodifikavimo temos (ASC 842) ir 16 tarptautinių finansinių ataskaitų standarto (16 TFAS) dalyse apie nuomos keitimą. ASC 842-20-15-1 nuomos keitimą apibrėžia kaip bet kokį sutarties sąlygų pakeitimą, kuris lemia nuomos apimties ar nagrinėjimo pasikeitimą. IFRS 16 39 pastraipoje nurodyta, kad nuomininkas turi perkainoti nuomos įsipareigojimą taip, kad jame atspindėtų nuomos mokesčių pasikeitimai.

Organizacijoms, kurios laikosi ASC 842 arba IFRS 16, nuoma perskaičiuojama, kad atsispindėtų dabartinės būsimų minimalių nuomos mokesčių (PVFMLP) vertės pasikeitimas. Jei PVFMLP didėja, sukuriamas žurnalo įrašas bus skola naudojimo teise valdomo turto paskyroje ir kreditas nuomos įsipareigojimų paskyrai dėl skirtumo tarp naujo PVFMLP ir ankstesnio PVFMLP. Jei PVFMLP mažėja, sukuriamas žurnalo įrašas bus skola naudojimo nuomos įsipareigojimo paskyrai ir kreditas naudojimo teise valdomas turto paskyrai dėl skirtumo.

Jei koreguojant naudojimo teise valdomas turtas sumažėja žemiau 0 (nulio), likutis bus kredituotas į pelną nuomos keitimo registravimo sąskaitoje, kuri nurodyta puslapyje **Nuomos registravimo sąskaitos**. Sistema atsižvelgia į šias operacijas ir kitus koregavimo įrašus, pvz., klasifikacijos pakeitimus, pradines tiesiogines išlaidas, nuomos paskatas, išankstinius mokėjimus ir išskaidymo kaštus, atsirandančius dėl nuomos pakeitimų.

Norėdami gauti konkrečių rekomendacijų dėl nuomos koregavimo operacijų, peržiūrėkite IFRS 16 ir ASC 842.

## <a name="lease-adjustment-wizard"></a>Nuomos koregavimo vedlys

Norėdami koreguoti nuomą, užbaikite tolesnius žingsnius. Pakeisti duomenys atnaujins nuomos grafikus po to, kai publikuosite iš **Nuomos koregavimo** vedlio. Galite išsaugoti savo darbą ir uždaryti vedlį bet kuriuo metu ir tuomet vėliau sugrįžti ir tęsti darbą.

Norėdami atverti **Nuomos koregavimo** vedlį iš nuomos santraukos, atlikite šiuos žingsnius.

1. Eikite į **Turto nuoma \> Nuomos \> Nuomos suvestinė**. 
2. Pasirinkite koreguojamą nuomą ir tuomet rinkitės **Koregavimo vedlys**.
3. Sekite skatinančius langus vedlyje, kad įvestumėte reikiamus keitimus.

Norėdami atverti **Nuomos koregavimo** vedlį iš **Nuomos koregavimo** puslapyje koregavimui, kuris jau vyksta, atlikite šiuos žingsnius.

1.  Eikite į **Nuoma \> Nuoma \> Nuomos koregavimai**.
2.  Pasirinkite nuomą, kurios koregavimo būsena yra **Vykdoma** ir tada rinkitės **Koregavimo vedlys**.
3.  Laukeliuose **Keitimo pradžios data** ir **Publikavimo data** įveskite atitinkamas datas.
4.  Pasirinkite **Toliau**.

    Nuoma dabar yra įtraukiama į **Nuomos koregavimo** puslapį, kuriame galite įvesti naują informaciją apie ją.

    Po to, kai nuoma buvo koreguota, naudojimo teisės aprašų laukeliai bus jai taikomi. Jei nėra jokių pradinių tiesioginių kaštų, nuomos iniciatyvų, išankstinių mokėjimų ar išmontavimo kaštų susietų su pakeista nuoma, palikite šiuos laukelius tuščius. Pradinės sumos atnaujintai nuomai nebus taikomos. 

    Pavyzdžiui, nuomotojas suteikia 1 000 USD paskatą, kad būtų pritarta nuomos pratęsimui. Tokiu atveju, kai keičiate nuomą paskyros pratęsimui, įveskite **1,000** laukelyje **Nuomos iniciatyvos kėlimas dėl koregavimo**.

    Mokėjimo grafiko eilutės dabar rodo visus mokėjimus už mėnesį ir vėlesnius mėnesius laukelyje **Keitimo pradžios data**. Kadangi keitimai yra būsini, mokėjimo grafiko eilutės negali prasidėdi prieš šį keitimą. Norėdami peržiūrėti grafiko eilutes iš ankstesnio keitimo datos, eikite į **Nuomos versijos istorijos** puslapį.

8.  Pasirinkite **Toliau**.

    Tolesniame puslapyje rodoma pagrindinė išsami informacija apie tikėtiną nuomos koregavimą, tokį kaip esamos nuomos įsipareigojimų vertės prieš keitimą ir naujas tikėtinas nuomos įsipareigojimas po keitimo. Puslapyje taip pat rodomas išankstinis žurnalo įrašo tikėtinam nuomos keitimui rodinys.

9.  Rinkitės **Teikti darbo eigai** norėdami pateikti nuomos keitimą darbo eigos sistemai, jei nuomos keitimo darbo eiga yra įjungta ir keitimas dar nėra patvirtintas. Dėl daugiau informacijos apie tai, kaip naudoti nuomos keitimo darbo eigą, žr. [Naudoti nuomos keitimų darbo eigas](use-create-lease-wrkflw.md).

    > [!NOTE]
    > Dabar, sistema perskaičiuoja keitimo kintamuosius, kad patvirtintų, jog jokios transakcijos nebuvo publikuotos už nuomą iki keitimo peržiūros ir anksčiau apskaičiuoto keitimo žurnalo įrašo. Jei bet kurios vertės keičiasi, koregavimo apžvalgos tinklelis yra atnaujintas ir galite peržiūrėti informaciją prieš pakartotinį nuomos keitimų pateikimą į darbo eigos sistemą.

10. Jei darbo eiga nėra šjungta arba nuomos keitimas buvo patvirtintas, rinkitės **Užbaigti** tam, kad sutvarkytumėte keitimus ir publikuotumėte keitimo žurnalo įrašą.

    > [!NOTE] 
    > Dabar, sistema perskaičiuoja keitimo kintamuosius, kad patvirtintų, jog jokios transakcijos nebuvo publikuotos už nuomą iki keitimo peržiūros ir anksčiau apskaičiuoto keitimo žurnalo įrašo. Jei bet kurios vertės keičiasi, koregavimo apžvalgos tinklelis yra atnaujintas ir galite peržiūrėti keitimus prieš pasirinkdami **Baigti**. Jei darbo eiga yra įjungta ir nuomos koregavimas buvo patvirtintas, visi koregavimo apžvalgos keitimai patvirtins būseną atgal į **Nepateikta**. Tokiu atveju, turėtumėte pateikti nuomos koregavimą į darbo eigos sistemą dar kartą.

    Puslapyje **Nuomos koregavimai**, koregavimo būsena dabar nustatyta į **Užbaigta**.

    Puslapyje **Nuomos koregavimai**, vis dar galite peržiūrėti **Koregavimo apžvalgą** ir **Koregavimo įrašo išankstinės peržiūros** „FastTabs“. Nuomos išsami informacija ir datos informacija yra rodoma nuomos versijos istorijoje.

    Nauja nuomos versija ir naujas grafikų rinkinys dabar yra sukuriami naudojant pakeistą informaciją. 

13. Norėdami peržiūrėti naujus grafikus, eikite į nuomą ir tada rinkitės **Knygos**.
14. Norėdami peržiūrėti naujai sukurtą mokėjimų grafiką, rinkitės **Mokėjimų grafikas**.
15. Norėdami peržiūrėti naują nuomos įsipareigojimų amortizavimo grafiką, kuris sukuriamas su nauja informacija, užverkite **Mokėjimo grafiko** puslapį ir atverkite **Įsipareigojimų amortizacimo grafiko** puslapį.
16. Norėdami peržiūrėti naujai sugeneruotą turto nusidėvėjimo grafiką, puslapyje **Knygų informacija** atidarykite puslapį **Turto nusidėvėjimo grafikas**.
17. Norėdami peržiūrėti koregavimo žurnalo įrašą, rinkitės **Žurnalai \> Turto nuomos žurnalas**.

## <a name="cancel-a-lease-adjustment"></a>Atšaukti nuomos koregavimą

Norėdami panaikinti vykstantį nuomos redagavimą, atlikite šiuos žingsnius.

1.  Eikite į **Nuoma \> Nuoma \> Nuomos koregavimai**.
2.  Pasirinkite vykstantį nuomos koregavimą norėdami jį atšaukti.
3.  Rinkitės **Atšaukti koregavimą**. 
4.  Pasirinkite **Gerai**.

    > [!NOTE] 
    > Jei rinksitės **Atšaukti** vedlyje **Nuomos koregavimas** grąžinsite naujausią keitimą, kurį užbaigėte vedlyje, tačiau nepašalinsite vykstančio keitimo.

## <a name="use-the-lease-adjustment-workflow"></a>Naudokite nuomos koregavimo darbo eigą

Šiame skyriuje paaiškinta, kaip naudoti nuomos koregavimo darbo eigą. Nuomos koregavimo darbo eiga jums padeda valdyti nuomos koregavimus nuoseklia tvarka suteikiant patvirtinimo žingsnių rinkinį ir priskiriant juos konkretiems vartotojams, kurie patvirtina nuomos keitimą prieš galutinį jo etapą. Po nuomos koregavimo patvirtinimo darbo eigoje, galite naudoti **Nuomos koregavimo** vedlį, jei norite užbaigti nuomos koregavimą.

1.  Norėdami pateikti nuomos koregavimą patvirtinimui, eikite į **Nuoma \> Nuoamos \> Nuomos koregavimas**.
2.  Rinkitės nuomos ID jos koregavimui ir tuomet pasirinkite **Koregavimo vedlys**.
3.  Paskutiniame vedlio puslapyje rinkitės **Teikti patvirtinimui**.
4.  Įveskite komentarą apie koregavimą ir tada rinkitės **Gerai**.

    Darbo eigos būsena pakeista į **Laukiantis patvirtinimas** ir visi laukeliai vedlyje yra užrakinti redagavimui.

5.  Norėdami patvirtinti nuomos koregavimą patvirtinimui, eikite į **Nuoma \> Nuoamos \> Nuomos koregavimas**.
6.  Rinkitės nuomos koregavimo ID ir peržiūrėkite **Koregavimo apžvalgą** ir **Koregavimo įrašo išankstinės peržiūros** „FastTabs“.
7.  Rinkitės **Darbo eiga \> Patvirtinta**.

    Puslapyje **Nuomos koregavimai**, darbo eigos būsena dabar nustatyta į **Patvirtinta**. Dabar nuomos koregavimas yra parengtas publikavimui per koregavimo žurnalo įrašą.

8.  Norėdami nuomos koregavimo vykdymą ir publikuoti redagavimo įrašą, eikite į **Nuoma \> Nuomos \> Nuomos koregavimai**.
9.  Rinkitės nuomos ID jos koregavimui ir tuomet pasirinkite **Koregavimo vedlys**.
10. Rinkitės **Toliau** tol, kol pasieksite paskutinį vedlio puslapį ir tada rinkitės **Užbaigti**.

Sistema iš naujo apskaičiuoja nuomos esamas vertes siekiant užtikrinti, kad patvirtinti redagavimo kintamieji yra dabartiniai. Jei esama kokių nors pakeitimų, patvirtinimo būsena yra grąžinama į **Šabloną** ir turėtumėte iš naujo pateikti nuomos redagavimą į darbo eigos sistemą.

## <a name="view-lease-versions"></a>Nuomos versijų peržiūra

Jei nuoma buvo pakoreguota, galite peržiūrėti skirtingas jos versijas. Taip pat galite peržiūrėti istorinius grafikus ir praeities nuomos informaciją.

1. Puslapyje **Nuomos suvestinė** pasirinkite nuomą, tada veiksmų srityje pasirinkite **Nuomos versijų retrospektyva**.

    Jei pasirinkta nuoma buvo pakoreguota, puslapis **Nuomos versijos istorija** rodo skirtingas versijas. Pradinė nuoma yra pažymėta **1**, o vėlesnės versijos – didėjančia skaičių tvarka.

    Galite peržiūrėti pasirinktos nuomos versijos finansines dimensijas, sutarties informaciją, vietą ir mokėjimo grafiko eilutes.

2. Norėdami peržiūrėti istorinius grafikus, atidarykite pakeistą nuomą puslapyje **Nuomos suvestinė**, pasirinkite norimą knygą, tada veiksmų srityje pasirinkite **Knygos versijų retrospektyva**.
3. Puslapyje **Knygos versija** rinkitės versiją ir nustatyti rodinio grafiką.

## <a name="adjust-a-lease-book"></a>Nuomos knygos koregavimas

Norėdami koreguoti tik nuomos knygą, atlikite šiuos veiksmus.

1. Eiti į turto **nuomos** \> **nuomos suvestinę.** \> **·**
2. Pasirinkite ir atidarykite nuomą.
3. Nuomos informacijos **puslapyje** pasirinkite **Knygos**.
4. Informacijos apie **knygas** puslapyje, veiksmų srityje, grupėje Tvarkyti **pasirinkite** Koreguoti **knygą**. 
5. Pašalinti mokėjimo grafiko eilutes.
6. Lauke Nuomos **modifikavimo** data įveskite modifikavimo datą. Tada apsvarstyti galimybę pašalinti visas papildomas turto ir (arba) įsipareigojimų aplinkybes (pradines tiesiogines išlaidas, skatinamąją nuomą, išankstinio apmokėjimo nuomą, išmontavimo išlaidas ir likutinės vertės garantiją), jei jų yra. 
7. Norėdami išvengti nuomos koregavimo suplanuotų skaičiavimų, pridėkite naujų mokėjimo grafiko eilučių, kurios atitinka modifikavimo datą. 

> [!NOTE] 
> Nuomos koregavimui koreguoti rekomenduojame **naudoti** nuomos koregavimo vedlį. Vedlys sumažina neautomatinių veiksmų skaičių, pateikia balansų peržiūrą po koregavimo ir leidžia keisti sumas prieš registruojant.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
