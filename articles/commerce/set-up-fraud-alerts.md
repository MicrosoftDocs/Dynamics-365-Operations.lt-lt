---
title: Įspėjimų dėl apgaulės nustatymas skambučių centre ir jų naudojimas
description: Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją. Galite apibrėžti konkrečius kodus, kuriuos naudojant galima automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus.
author: josaw1
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e692d43b8c2648a424ff3b4fdc9d0cf16d0e03702d6a237f71caaf49646c5ec3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763673"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Įspėjimų dėl apgaulės nustatymas skambučių centre ir jų naudojimas

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti kriterijus ir taisykles, leidžiančias sulaikyti galimai apgaulingus pardavimo užsakymus ir juos peržiūrėti. Apgaulės patikros funkcija naudojama siekiant nustatyti pardavimo užsakymo informacijos pagrįstumą. Jei remiantis organizacijos nustatytais apgaulės kriterijais ir taisyklėmis, pardavimo užsakyme esanti informacija pradeda kelti abejonių, užsakymas gali būti sulaikytas siekiant jį atidžiau peržiūrėti. Tokiu atveju užsakymo negalima išleisti į sandėlį toliau apdoroti, kol nebus atšauktas sulaikymas.

> [!NOTE]
> Šią funkciją galima naudoti tik apdorojant pardavimo užsakymus, gautus per „Commerce“ skambučių centro kanalą.

## <a name="turning-on-the-fraud-check-feature"></a>Apgaulės patikros funkcijos įjungimas

Norėdami naudoti apgaulės patikros funkciją, nustatykite kanalo parinktį **Įgalinti užsakymo baigimą** kaip **Taip**, kai skambučių centro kanalas yra [apibrėžtas](/dynamics365/unified-operations/retail/set-up-order-processing-options). Įjungus užsakymo baigimo funkciją, skambučių centro vartotojai kiekvieno sukurto pardavimo užsakymo puslapyje turi pasirinkti **Baigti**. Pasirinkus baigimo veiksmą atidaromas puslapis **Pardavimo užsakymo suvestinė**. Kai vartotojai įveda reikiamus mokėjimo duomenis puslapyje **Pardavimo užsakymo suvestinė**, reikia pasirinkti **Pateikti**, kad užsakymas būtų baigtas. Pateikus užsakymą, suaktyvinama apgaulės patikros funkcija ir automatiškai patikrinamos bet kokios sistemoje esančios aktyvios taisyklės.

Skambučių centro vartotojai taip pat gali rankiniu būdu sulaikyti pardavimo užsakymus ir patikrinti juos dėl galimos apgaulės prieš pasirinkdami **Pateikti**. Norėdami rankiniu būdu sulaikyti pardavimo užsakymą, puslapyje **Pardavimo užsakymo suvestinė** pasirinkite **Sulaikyti** \> **Sulaikymas dėl apgaulės rankiniu būdu**. Tada būsite paraginti įvesti komentarą, nurodantį užsakymo sulaikymo priežastį. Šis komentaras bus rodomas [užsakymų sulaikymo](/dynamics365/unified-operations/retail/work-with-order-holds) darbo srityje, kad sulaikytus užsakymus peržiūrinčiam vartotojui būtų paprasčiau nuspręsti, ar užsakymo sulaikymą reikia atšaukti.

Sukonfigūravus kanale parinktį **Įgalinti užsakymo baigimą**, skambučių centro parametrų dalyje taip pat reikia sukonfigūruoti apgaulės patikros funkciją. Eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo nustatymas** \> **Skambučių centro sąranka** \> **Skambučių centro parametrai**. Puslapio **Skambučių centro parametrai** skirtuke **Sulaikymai** nustatykite parinkties **Apgaulės patikra** parametrą **Taip**.

Skirtuke **Sulaikymai** taip pat reikia apibrėžti [sulaikymo kodus](/dynamics365/unified-operations/retail/work-with-order-holds), kurie taikomi rankiniu būdu ar automatiškai sulaikytam užsakymui, kurį reikia peržiūrėti dėl galimos apgaulės. Nustatykite sulaikymo kodus laukuose **Sulaikymo dėl apgaulės rankiniu būdu kodas** ir **Sulaikymo dėl apgaulės kodas**. Galite sukurti du unikalius sulaikymo kodus, kad sulaikymo darbo srityje dirbantys vartotojai galėtų lengvai filtruoti ir atskirti automatinius sulaikymus ir rankiniu būdu atliktus sulaikymus.

Kad apgaulės patikros funkcija veiktų efektyviai, taip pat reikia nustatyti lauką **Minimalus rezultatas**. Kiekvienas sistemoje nustatytas apgaulės kriterijus ir taisyklė turi priskirtą rezultato vertę. Kai pardavimo užsakymas tikrinamas dėl apgaulės, radus vieną arba kelis atitinkančius kriterijus, rezultatai sudedami ir gaunamas bendras užsakymo apgaulės rezultatas. Jei bendras užsakymo apgaulės rezultatas viršija lauke **Minimalus rezultatas** nurodytą vertę, užsakymas automatiškai sulaikomas. Pasirinktinai naudodami kitus su rezultatu susijusius skirtuko **Sulaikymai** laukus, galite apibrėžti el. pašto rezultatą, telefono rezultatą, pašto indekso rezultatą ir išplėsto pašto indekso rezultatą. Jei nenurodysite jokių statinių apgaulės duomenų kriterijų, kai juos apibrėžiate puslapyje **Statiniai apgaulės duomenys**, rezultatų verčių, sistema juos vertins naudodama numatytąsias rezultatų vertes, kurias nurodėte puslapio **Skambučių centro parametrai** skirtuke **Sulaikymai**.

Galiausiai naudodami lauką **Apgaulės komentaro tipas** nurodykite dokumento tipą, kurį reikia naudoti, kai vartotojai įveda komentarus, kai rankiniu būdu dėl galimos apgaulės sulaiko užsakymą, kurį reikia peržiūrėti. Dažniausiai nustatomas šio lauko parametras yra **Pastaba**.

## <a name="defining-fraud-criteria-and-rules"></a>Apgaulės kriterijų ir taisyklių apibrėžimas

Sistema naudoja dviejų tipų apgaulės kriterijus, pagal kuriuos nustatoma, ar užsakymą reikia sulaikyti dėl galimos apgaulės ir peržiūrėti:

- **Statiniai apgaulės duomenys** naudoja konkrečią vertę, pvz., telefono numerį, kuris buvo įtrauktas į užblokuotų numerių sąrašą, ar el. pašto adresą, kuris yra pažymėtas, nes buvo anksčiau naudotas atliekant apgaulingas operacijas. Norėdami nustatyti statinius apgaulės duomenis, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo nustatymas** \> **Skambučių centro sąranka** \> **Apgaulė** \> **Statiniai apgaulės duomenys**. Puslapyje **Statiniai apgaulės duomenys** galite įtraukti apgaulės kriterijus rankiniu būdu ar importuodami duomenis. Prie apgaulingos informacijos pridedamos rezultatų vertės. Jei įjungta apgaulės patikros funkcija, kiekvienas įvestas pardavimo užsakymas bus lyginamas su statiniais duomenimis. Jei duomenys randami kliento sąskaitų siuntimo adrese arba pristatymo adrese, susietame su užsakymo antrašte, arba jei duomenys randami pristatymo adresuose, susietuose su bet kuria to pardavimo užsakymo eilute, visų unikalių atitikmenų rezultatų vertės sudedamos ir bendras rezultatas palyginamas su lauke **Minimalus rezultatas** nurodyta verte, siekiant nustatyti, ar užsakymą reikia sulaikyti.

- **Apgaulės taisykles** sudaro vartotojo apibrėžti kintamieji ir apibrėžtos tų kintamųjų sąlygos. Norėdami kurti taisykles, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo nustatymas** \> **Skambučių centro sąranka** \> **Apgaulė** \> **Taisyklės**. Naudodama apgaulės taisykles įmonė gali sukonfigūruoti sudėtingesnį taisyklių rinkinį, kuriame naudojami sakiniai **IR** arba **ARBA**, kad būtų galima įvertinti keletą sąlygų. Pavyzdžiui, vartotojas nori sulaikyti ir peržiūrėti dėl galimos apgaulės visus klientų, kurie priklauso konkrečiai klientų grupei ir kurie užsisakė konkretų produktą, užsakymus. Tokiu atveju sąlygos, taikomos tikrinant klientą ir produktus, apibrėžiamos puslapyje **Taisyklės** ir naudojama sąlyga IR. Užsakymas sulaikomas tik tada, jei tenkinamos abi sąlygos ir jei bendras užsakymo apgaulės rezultatas, sudarytas iš šiai taisyklei priskirtos rezultato vertės ir kitų taisyklių, kurias atitinka užsakymas, rezultatų verčių, viršija vertę **Minimalus rezultatas**, kuri apibrėžta puslapyje **Skambučių centro parametrai**.

> [!NOTE]
> Kelių taisyklių arba pernelyg sudėtingų taisyklių naudojimas paveiks sistemos našumą, pateikiant pardavimo užsakymus. Apgaulės patikros funkcija nėra optimizuota apdoroti didelį statinių apgaulės duomenų kiekį ir daug aktyvių taisyklių. Atminkite, kad kiekviena taisyklė įvertinama tada, kai skambučių centro vartotojas įvesdamas pardavimo užsakymą pasirenka **Pateikti**. Taisyklės vertinamos pagal pardavimo užsakymo antraštę ir visas užsakymo eilutes. Kuo daugiau taisyklių taikote ir kuo sudėtingesni taisyklių sakiniai, tuo ilgiau truks apdorojimas. Jei užsakyme yra daug eilučių elementų, daug aktyvių taisyklių ir statinių duomenų įvesčių, šis automatinis procesas, kurio metu peržiūrimi ir patikrinami visi duomenys bei apskaičiuojamas apgaulės rezultatas, gali stipriai paveikti našumą. Organizacijos, naudojančios šią funkciją, prieš keisdamos taisykles ar statinių apgaulės duomenų kriterijus gamybos aplinkoje, turi visada patikrinti ir patvirtinti, kad užsakymo pateikimo apdorojimo laikas yra priimtinas.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Užsakymų, kurie yra sulaikyti ir kuriuos reikia peržiūrėti dėl apgaulės, identifikavimas

Kai skambučių centro vartotojai pateikia pardavimo užsakymą, jei užsakymas atitinka apgaulės kriterijus arba taisykles ir jei bendras rezultatas viršiją minimalų rezultatą, vartotojai gauna įspėjimo pranešimą, informuojantį, kad užsakymas yra sulaikytas. Vartotojai gali uždaryti šį pranešimą, nes jis pateikiamas tik informaciniais tikslais. Vartotojai gali pasirinktinai apie tai informuoti klientą. Įmonė turėtų nustatyti protokolą, kuriuo tokioje situacijoje turėtų vadovautis vartotojai.

Užsakymas įrašomas, bet jis pažymimas žyme **Neapdoroti**. Ši žymė padeda užtikrinti, kad užsakymas nebūtų išleistas į sandėlį. Vartotojai bet kada gali peržiūrėti bet kurio pardavimo užsakymo žymės **Neapdoroti** nustatymą puslapyje **Išsami būsena**. Šį puslapį galima atidaryti puslapiuose **Visi pardavimo užsakymai** ir **Klientų aptarnavimas**. Sistema taip pat pakeičia užsakymo lauko **Išsami būsena** parametrą į **Sulaikymas dėl apgaulės**.

Norėdami peržiūrėti ir tvarkyti užsakymus, kurie sulaikyti ir kuriuos reikia peržiūrėti dėl apgaulės, eikite į **Mažmeninė prekyba ir prekyba** \> **Klientai** \> **Užsakymo sulaikymas**. Puslapyje **Užsakymo sulaikymas** esančiame sąraše pasirinkite įrašą ir spustelėkite **Užsakymo sulaikymas**, kad pamatytumėte išsamesnį rodinį, kuriame pateikiama informacija apie sulaikymo priežastį. „FastTab“ **Apgaulės informacija** galite peržiūrėti sistemoje nustatytus apgaulės kriterijus, pagal kuriuos rasta atitikmenų užsakyme, ir pritaikytas rezultatų vertes. Jei užsakymas buvo sulaikytas rankiniu būdu, galite peržiūrėti užsakymą sulaikiusio vartotojo įvestus komentarus „FastTab“ **Pastabos** skyriuje **Apgaulės pastabos**.

Daugiau informacijos apie tai, kaip dirbti su sulaikytais užsakymais, žr. [Užsakymo sulaikymas](/dynamics365/unified-operations/retail/work-with-order-holds).


[!INCLUDE[footer-include](../includes/footer-banner.md)]