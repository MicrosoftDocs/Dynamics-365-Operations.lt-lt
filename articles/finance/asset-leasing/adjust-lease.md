---
title: Nuomos koregavimas
description: Šioje temoje paaiškinama, kaip koreguoti nuomą. Koreguoti gali reikėti, jei pakeičiamos nuomos sąlygos, nuoma pratęsiama arba pasikeičia kitos aplinkybės.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446205"
---
# <a name="adjust-leases"></a>Nuomos koregavimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip koreguoti nuomą. Koreguoti gali reikėti, jei pakeičiamos nuomos sąlygos, nuoma pratęsiama arba pasikeičia kitos aplinkybės. Turto nuoma atitinka rekomendacijas, kurios pateiktos 842 apskaitos standartų kodifikavimo temos (ASC 842) ir 16 tarptautinių finansinių ataskaitų standarto (16 TFAS) dalyse apie nuomos keitimą. ASC 842-20-15-1 nuomos keitimą apibrėžia kaip bet kokį sutarties sąlygų pakeitimą, kuris lemia nuomos apimties ar nagrinėjimo pasikeitimą. IFRS 16 39 pastraipoje nurodyta, kad nuomininkas turi perkainoti nuomos įsipareigojimą taip, kad jame atspindėtų nuomos mokesčių pasikeitimai.

Organizacijoms, kurios laikosi ASC 842 arba IFRS 16, nuoma perskaičiuojama, kad atsispindėtų dabartinės būsimų minimalių nuomos mokesčių (PVFMLP) vertės pasikeitimas. Jei PVFMLP padidėja, sukurtas žurnalo įrašas bus naudojimo teise valdomo turto debetas ir nuomos įsipareigojimo kreditas kaip skirtumas tarp naujos PVFMLP ir ankstesnės PVFMLP. Jei PVFMLP sumažėja, žurnalo įrašas bus nuomos įsipareigojimo debetas ir naudojimo teise valdomo turto kreditas kaip atitinkamas skirtumas.

Jei koreguojant naudojimo teise valdomas turtas sumažėja žemiau 0 (nulio), likutis bus kredituotas į pelną nuomos keitimo registravimo sąskaitoje, kuri nurodyta puslapyje **Nuomos registravimo sąskaitos**. Sistema atsižvelgia į šias operacijas ir kitus koregavimo įrašus, pvz., klasifikacijos pakeitimus, pradines tiesiogines išlaidas, nuomos paskatas, išankstinius mokėjimus ir išskaidymo kaštus, atsirandančius dėl nuomos pakeitimų.

Norėdami gauti konkrečių rekomendacijų dėl nuomos koregavimo operacijų, peržiūrėkite IFRS 16 ir ASC 842.

Norėdami koreguoti nuomą, atlikite toliau nurodytus veiksmus. Modifikuoti duomenys atnaujins nuomos grafikus po to, kai bus vykdomas procesas Kurti grafiką.

1. Eikite į **Turto nuoma \> Nuomos \> Nuomos suvestinė**.
2. Puslapyje **Nuomos suvestinė** pasirinkite norimą koreguoti nuomą, tada – **Koreguoti nuomą**.
3. Puslapyje **Nuomos koregavimas** įveskite naują koreguotos nuomos informaciją.

    Atkreipkite dėmesį, kad puslapis **Nuomos koregavimas** yra panašus į puslapį **Nuomos įtraukimas**. Be to, taip, kaip pradžios data, kurią nurodote įtraukdami nuomą, nustato, kada prasideda nauja nuoma, puslapio **Nuomos koregavimas** laukas **Keitimo data** nustato pakeistos nuomos pradžios datą. Ši data negali būti vėlesnė nei darbo grafiko eilutėse nurodyta pradžios data.

    > [!NOTE]
    > Koreguojant nuomą taikomi **naudojimo teise valdomo turto aspektų** laukai. Jeigu nėra pradinių tiesioginių išlaidų, nuomos paskatų, išankstinių apmokėjimų ar išskaidymo kaštų, susijusių su pakeista nuoma, šiuos laukus reikia palikti tuščius. Pradinės sumos atnaujintai nuomai nebus taikomos. Visos papildomos išlaidos, patirtos keičiant nuomą, turėtų būti įvestos į puslapį **Nuomos koregavimas**.
    > 
    > Pavyzdžiui, nuomotojas suteikia 1 000 USD paskatą, kad būtų pritarta nuomos pratęsimui. Šiuo atveju, kai koreguojate nuomą atsižvelgdami į pratęsimą, lauke **Nuomos paskatos** įvedate **1000**. Jei nėra paskatų, susijusių su nuomos koregavimu, turite panaikinti visas reikšmes, kurios anksčiau buvo įvestos šiame lauke. Ta pati logika taikoma kitiems naudojimo teise valdomo turto aspektams.

    Pakoreguotos nuomos mokėjimo grafiko eilutės turėtų būti sukurtos galimų situacijų pagrindu. Mokėjimo grafiko eilutės, sukurtos galimų situacijų pagrindu, negali prasidėti prieš įsigaliojant nuomos pakeitimams.

    Toliau pateikti veiksmai beveik sutampa su veiksmais, kuriais iš pradžių pripažįstama nuoma.

4. Pasirinkite **Kurti grafikus**, kad būtų sugeneruotas pakoreguotas mokėjimo grafikas. Gausite pranešimą, kuriame bus teigiama, kad sukurtas nuomos mokėjimo grafikas.

    > [!IMPORTANT]
    > Prieš pasirinkdami **Sukurti grafikus**, įsitikinkite, kad keitimo data ir mokėjimo grafiko eilutės yra tikslios. Taip pat įsitikinkite, kad visos pradinės tiesioginės išlaidos, nuomos paskatos, išankstiniai mokėjimai ar išskaidymo išlaidos atitinka tik tas išlaidas, kurios susidaro koreguojant.

5. Norėdami peržiūrėti naujai sukurtą mokėjimo grafiką, pasirinkite **Knygos** ir atidarykite puslapį **Mokėjimo grafikas**.
6. Puslapyje **Mokėjimo grafikas** galite redaguoti pakoreguotas mokėjimo sumas prieš patvirtindami mokėjimo grafiką. Norėdami patvirtinti grafiką, pasirinkite **Patvirtinti grafiką**.

    Patvirtinus mokėjimo grafiką, sukuriamas naujas turto nusidėvėjimas ir nauji nuomos įsipareigojimų grafikai.

7. Norėdami peržiūrėti naują nuomos įsipareigojimų amortizacijos grafiką, kuris generuojamas iš naujų įvesčių, uždarykite puslapį **Mokėjimo grafikas** ir atidarykite puslapį **Įsipareigojimų amortizacijos grafikas**.
8. Norėdami peržiūrėti naujai sugeneruotą turto nusidėvėjimo grafiką, puslapyje **Knygų informacija** atidarykite puslapį **Turto nusidėvėjimo grafikas**.
9. Norėdami sugeneruoti koregavimo žurnalo įrašą, pasirinkite **Funkcija \> Nuomos koregavimas**. Gausite pranešimą, kuriame bus teigiama, kad sukurtas koregavimo žurnalo įrašas. 
10. Norėdami peržiūrėti žurnalo įrašą, pasirinkite **Žurnalai \> Turto nuomos žurnalas**.
11. Norėdami užregistruoti žurnalo įrašą, pasirinkite eilutę ir **Registruoti**.

## <a name="view-lease-versions"></a>Nuomos versijų peržiūra

Jei nuoma pakeista, galite peržiūrėti įvairias jos versijas. Taip pat galite peržiūrėti istorinius grafikus ir praeities nuomos informaciją.

1. Puslapyje **Nuomos suvestinė** pasirinkite nuomą, tada veiksmų srityje pasirinkite **Nuomos versijų retrospektyva**.

    Jei pasirinkta nuoma pakoreguota, puslapyje **Nuomos versijų retrospektyva** pateikiamos įvairios jos versijos. Pradinė nuoma yra pažymėta **1**, o vėlesnės versijos – didėjančia skaičių tvarka.

    Galite peržiūrėti pasirinktos nuomos versijos finansines dimensijas, sutarties informaciją, vietą ir mokėjimo grafiko eilutes.

2. Norėdami peržiūrėti istorinius grafikus, atidarykite pakeistą nuomą puslapyje **Nuomos suvestinė**, pasirinkite norimą knygą, tada veiksmų srityje pasirinkite **Knygos versijų retrospektyva**.
3. Puslapyje **Knygos versija** pasirinkite norimą versiją ir norimą grafiką, kuriuos norite peržiūrėti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]