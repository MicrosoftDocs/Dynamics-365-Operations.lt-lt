---
title: Grąžinimų valdymo modulio apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Supply Chain Management” grąžinimo valdymo modulio apžvalga.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 75311e137df522c476b938f660b8305004396137
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985512"
---
# <a name="rebate-management-module-overview"></a>Grąžinimų valdymo modulio apžvalga

[!include [banner](../includes/banner.md)]

Galite naudoti **Grąžinimų valdymo** modulį kurti kontraktams, sandoriams ar sutartims tarp jūsų verslo ir jo klientų arba tiekėjų, kad būtų galima apskaičiuoti grąžinimus, atskaitymus ir autorinius honorarus. Grąžinimo valdymas seka ir prižiūri grąžinimo ir atskaitymo operacijas centrinėje vietoje, kurioje vartotojai gali jas efektyviai kurti, peržiūrėti ir apdoroti.

Grąžinimų valdymas palaiko *grąžinimų* kūrimą, priežiūrą ir apdorojimą. Grąžinimas yra pirkimo kainos dalies grąžinimas pirkėjui arba pardavėjui. Grąžinimai paprastai yra grindžiami konkretaus kiekio arba vertės prekių pirkimu tam tikru laikotarpiu. Skirtingai nei nuolaidos, grąžinimai atliekami po to, kai pirkimo sumai pilnai išrašoma sąskaita faktūra.

Grąžinimų valdymas taip pat palaiko *atskaitymus*. Atskaitymas yra kompensacija, atlyginimas arba mokestis, mokamas už licenciją arba mokestį, siekiant naudoti intelektinę nuosavybę, pavyzdžiui, prekės ženklą, autoriaus teisės arba patentą, taip pat už teisę naudoti gamtos išteklius žvejybos, medžioklės ar kasybos tikslais. Atskaitymai paprastai apskaičiuojami kaip procentas nuo įplaukų arba pelno nuo realizuoto panaudojimo. Kuo daugiau naudojama intelektinė nuosavybė arba gamtos ištekliai, tuo didesnis atskaitymas.

Taip pat, grąžinimo valdymas palaiko kliento *autorinius honorarus*. Autoriniai honorarai yra mokėjimai, kuriuos viena šalis atlieka licencijos savininkui arba franšizei už teisę naudotis turtu.

Grąžinimų valdymas leidžia jums apibrėžti nuostatų, grąžinimų ir nurašymų registravimo šablonus. Be to, galima nurodyti konkretaus kliento arba tiekėjo registravimus. Tokiu būdu, pasiūlymai, kurie netaikomi visiems klientų ar tiekėjų scenarijams, gali būti sekami naudojant registravimus.

Grąžinimo operacijos generuojamos automatiškai, remiantis paketinėms užduotims pasirinktu ir suplanuotu skaičiavimo metodu. Taip pat, galite nustatyti darbo eigas sutartims valdyti, peržiūrėti ir tvirtinti.

## <a name="basis-calculation"></a>Pagrindas skaičiavimui

Kliento grąžinimai, kliento autoriniai honorarai ir tiekėjo grąžinimai gali naudoti skirtingą pagrindą, atsižvelgiant į jūsų verslo reikalavimus:

- Kliento grąžinimai gali būti pagrįsti pardavimo užsakymais, pristatymo pastabomis arba sąskaitomis faktūromis.
- Kliento autoriniai honorarai gali būti pagrįsti pardavimo užsakymais, pristatymo pastabomis arba apmokėtomis sąskaitomis faktūromis.
- Tiekėjo grąžinimai gali būti pagrįsti pirkimo arba pardavimo užsakymais. Jie gali būti apskaičiuojami pagal produktus, kurie yra perkami iš grąžinimo tiekėjo ir parduodami klientams pagal pardavimo sąskaitas faktūras.

## <a name="flexible-calculations"></a>Lankstūs skaičiavimai

Grąžinimo skaičiavimo laikotarpius galima naudoti tiek klientų, tiek tiekėjų sandorių atvejais. Skaičiavimo laikotarpis nurodo sandorio ilgį, skaičiavimo dažnį ir laikotarpį. Grąžinimai gali būti sukaupti remiantis pardavimo užsakymo kiekiais arba patvirtintų produktų sumomis grąžinimo laikotarpiu.

Kiekvienam sutarties skaičiavimui galima nustatyti bet kurį iš šių laikotarpių:

- Sąskaita faktūra
- Diena
- Savaitė
- Mėnuo
- Ketvirtis
- Metai
- Pritaikytas laikotarpis
- Bet kuris kartotinis iš anksčiau išvardintų laikotarpių

Skaičiavimas gali būti taikomas atskiriems klientams ir produktams, klientų ir produktų grupėms arba visiems klientams ir produktams. Grąžinimai, turintis kelias išsamios informacijos eilutes, gali turėti skirtingus tinkamumo datos diapazonus. Nuostatos ir pareikalavimo laikotarpiai gali skirtis. Pavyzdžiui, nuostatos gali būti apdorojamos kiekvieną dieną, o pareikalavimai – kartą per mėnesį.

Grąžinimus galima konfigūruoti pagal daug skirtingų parametrų. Pavyzdžiui, juos galima konfigūruoti kaip procentą, tarifą arba fiksuotą sumą. Yra keturi pagrindiniai skaičiavimo metodai:

- Žingsninis
- Sukauptas
- Sumavimas
- Bendroji vertė

Grąžinimo skaičiavimo rezultatai taip pat gali būti sumažinti kitais grąžinimais, atsižvelgiant į tai, ar grąžinimas nustatytas skaičiuoti pagal grynąją sumą.

Iš tiekėjo pusės pardavimų užsakymais pagrįsti grąžinimai gali apskaičiuoti kainą pagal pirmas ateina, pirmas išeina (FIFO) taisyklę, naujausio pirkimo kainą, vidutinę pirkimo kainą arba pardavimo kainą.

## <a name="rebate-target-transactions"></a>Grąžinimų paskirties operacijos

Išvestis, kurias sugeneruoja grąžinimų sandoris arba sutartis, gali būti finansai arba prekės.

Finansinės išvestis nustatomos pagal mokėjimo tipą, priskirtą sutarčiai iš registravimo šablono. Šias išvestis gali sudaryti kliento atskaitymų žurnalai, laisvos formos ir tiekėjų sąskaitos faktūros. Audito tikslais finansinės grąžinimų paskirties operacijos apima nuorodą į pirminę grąžinimo sutartį.

Prekių išvestys sukuria laisvos prekės pardavimo užsakymą, skirtą kliento grąžinimams, ir pirkimo užsakymą, skirtą tiekėjų grąžinimams. Prekės grąžinimų paskirties operacijose yra parinkčių, nustatančių, kuri grąžinimo nuoroda turi būti įvesta į laisvos prekės pardavimo arba pirkimo užsakymą.

## <a name="accurate-rebate-calculations"></a>Tikslūs grąžinimų skaičiavimai

Pasirinktų susietų sandorių, skaičiavimų dažnumo, skaičiavimo pagrindo ir skaičiavimo metodo derinys lemia grąžinimo skaičiavimų tikslumą. Grąžinimų nuostatos gali būti naudojamos užregistruotų ir pareikalautų verčių kaupimui.

Nuostatos gali būti valdomos kasdien, kas savaitę, kas mėnesį arba pagal pasirinktinį laikotarpį. Tačiau funkcija gali paskirstyti arba sumokėti grąžinimą, taip pat gauti mokėjimą bet kokiu apibrėžtu dažnumu, tokios pat arba ilgesnės trukmės nei nuostatų dažnumu. Nurašymo dažnumas yra toks pat kaip grąžinimo. Vartotojai gali bet kuriuo apmokėjimo metu nesunkiai koreguoti planą ar mokėjimo sumas.

Vartotojams nebereikia tvarkyti sandorių ar nuostatų dvejais veiksmais. Nuostatos ir nurašymai yra registruojami tiesiogiai į didžiąją knygą. Taip pat, kredito pažymas galima kurti automatiškai. Taigi, mokėtinos ir gautinos sumos yra visiškai suintegruotos. Atliekant skaičiavimus galima atsižvelgti į sudengimo nuolaidas, apmokėtas sąskaitas faktūras, prekybos nuolaidas ir esamas kredito pažymas, siekiant užtikrinti, kad sumos ir vertės yra tiksliai apskaičiuojamos.

Apskaičiavus grąžinimus, procesas sukuria operacijas, kurias galima peržiūrėti prieš registravimą. Atskiru procesu registruojamos grąžinimų valdymo operacijos. Tada registruojant į pasiūlytas operacijas galima sukurti žurnalą, kredito pažymą ar debeto operaciją. Norint užtikrinti atitikimą, efektyvumą ir skaidrumą, galima gauti ataskaitų išrašus ir operacijų sąrašus.

## <a name="guaranteed-royalty-payments"></a>Garantiniai autorinių honorarų mokėjimai

Naudojant grąžinimų valdymą, automatinis mokėjimų generavimas leidžia greitai ir lengvai tvarkyti autorinius honorarus, net jei taikomi garantiniai minimumai.

## <a name="maximizing-spend-versus-rebates"></a>Maksimalių išlaidos ir grąžinimai

Tiekėjai ir produktai gali būti sugrupuoti pagal teritoriją, o skirtingi pasiūlymai gali būti pateikti, atsižvelgiant į operacijos šalį arba regioną. Kai vartotojai pasirenka produktus, jie gali apibrėžti įtrauktas prekes ir prekių, kurios bus naudojamos grąžinimo sudengime, skaičių.
