---
title: "Įspėjimų dėl apgaulės nustatymas"
description: "Šioje temoje paaiškinama, kaip nustatyti taisykles, kad klientų aptarnavimo atstovai užsakymų apdorojimo metu būtų įspėjami apie galimai apgaulingą informaciją. Galite apibrėžti konkrečius kodus, kurie būtų naudojami norint automatiškai arba rankiniu būdu sulaikyti įtartinus užsakymus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Įspėjimų dėl apgaulės nustatymas

[!include[banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti kriterijus ir taisykles, skirtas sulaikant galimai apgaulingo pardavimo užsakymus tolesnei peržiūrai. Apgaulės peržiūros funkcija naudojama siekiant nustatyti pardavimo užsakymo informacijos pagrįstumą. Jei, remiantis organizacijos apgaulės kriterijais ir taisyklėmis, pardavimo užsakyme esanti informacija pradeda kelti abejonių, užsakymas gali būti sulaikytas, kad jo tolimesnę peržiūrą galėtų atliktų administratorius.

> [!NOTE]
> Šią funkciją galima naudoti tik apdorojant Mažmeninės prekybos skambučių centro kanalo pardavimo užsakymą. 

Nustačius skambučių centro kanalą, parinktį **Įgalinti užsakymo baigimą** reikia nustatyti į **Taip**. Įgalinus užsakymo baigimą, vartotojai gali peržiūrėti užsakymo reziumė ir spustelėti **Pateikti**, kad užsakymas būtų baigtas. Vartotojams taip pat bus pateiktos parinktys, skirtos rankiniu būdu sulaikyti pardavimo užsakymą, kad būtų galima atlikti peržiūrą dėl apgaulės. Pardavimo užsakymai, kuriuos į skambučių centrą klaviatūra įveda vartotojas, apdorojami pateikimo proceso metu taikant patikros dėl apgaulės taisykles ir kriterijus.

Sulaikius užsakymą siekiant atlikti peržiūrą dėl apgaulės, atlikdama patikrą sistema remsis toliau nurodytais dviejų tipų apgaulės kriterijais.

-   **Statinėmis taisyklėmis**, naudojančiomis konkrečią reikšmę, pvz., telefono numerį, kuris buvo įtrauktas į juodąjį sąrašą, arba el. pašto adresą, kuris buvo pažymėtas kaip naudotas atliekant ankstesnes apgaulingas operacijas. Puslapyje **Statiniai apgaulės duomenys** apgaulės informaciją galima pridėti neautomatiniu būdu arba importavus duomenis ir kartu su apgaulinga informacija pateikus rezultatus. Jei įjungta apgaulės tikrinimo funkcija, kiekvienas pardavimo užsakymas bus lyginamas su statistiniais duomenimis. Jei duomenys aptinkami kliento atsiskaitymo arba pristatymo adrese arba pardavimo eilutės pristatymo adrese, visų unikalių atitikčių rezultatai bus sudėti.  
-   **Dinaminėmis taisyklėmis**, sudarytomis iš kintamųjų ir šiems kintamiesiems apibrėžtų sąlygų. Naudojant dinamines taisykles galima patikrinti kitus kriterijus, neapibrėžtus statinėse taisyklėse. Naudojant sudėtingesnius išrašus su IR/ARBA galima numatyti kelias sąlygas ir nustatyti, ar atitiktis taisyklės kriterijams yra teigiama ir ar pardavimo užsakymas yra teiktinas. Pavyzdžiui, jei vartotojas nori sulaikyti visų klientų, susietų su konkrečia klientų grupe ir užsisakiusių konkretų produktą, užsakymus, kad galėtų atlikti patikrą dėl apgaulės, sąlygos, skirtos patikrinti klientą ir produktus, bus apibrėžtos puslapyje **Taisyklės** ir nurodyta sąlyga IR. Užsakymas, siekiant patikrinti jį dėl apgaulės, bus sulaikytas tik tada, jei abi šios sąlygos bus teisingos ir jei taisyklei priskirta rezultato vertė bendrą apgaulės rezultatą padidins tiek, jog jis viršys skambučių centro parametruose apibrėžtą mažiausią apgaulės rezultatą.

Skambučių centro vartotojas užsakymą į sulaikytų užsakymų, kuriuos reikia patikrinti dėl apgaulės, eilę taip pat gali įtraukti rankiniu būdu. Jei užsakymą įvedantis klientas mano, kad užsakymą teikiantis klientas gali būti įtartinas ir nori, kad prieš apdorojant užsakymą jo pagrįstumą peržiūrėtų kas nors kitas, užsakymą įvedantis vartotojas puslapio **Pardavimo užsakymo suvestinė** (pasirodo iškvietus užsakymo funkciją **Baigti**) išskleidžiamajame meniu **Sulaikymai** gali pasirinkti parinktį **Sulaikymas dėl apgaulės rankiniu būdu** . Vartotojas bus paragintas įvesti pastabą ir išsamiau paaiškinti, kodėl jam atrodo, kad užsakymas gali būti apgaulingas, tokiu būdu pateikiant tikrintojui daugiau konteksto.

Visi užsakymai, sulaikyti rankiniu būdu norint patikrinti dėl apgavystės arba sistemai apskaičiavus apgavystės rezultatus, bus rodomi puslapyje **Užsakymo sulaikymas**, kuriame užsakymą bus galima peržiūrėti, tada atšaukti arba pateikti, kad jis būtų apdorotas.

> [!NOTE]
> Naudojant keletą taisyklių arba pernelyg sudėtingas taisykles ir pateikus pardavimo užsakymus, sistema veiks prastai. Įspėjimo dėl apgaulės funkcija nėra optimizuota apdoroti didelius statinius apgaulingus duomenis ir daug aktyvių taisyklių. Svarbu prisiminti, kad kiekviena taisyklė vertinama kaskart, kai teikdami pardavimo užsakymo įvedimą naudojate skambučių centro pateikimo funkciją. Taisyklės vertinamos pagal pardavimo užsakymo antraštę ir visas užsakymo eilutes. Kuo daugiau taisyklių taikote ir kuo sudėtingesni jų išrašai, tuo ilgiau truks apdorojimo procesas. Jei savo užsakyme turite daug eilutės elementų, aktyvių taisyklių ir statistinių duomenų įvesčių, šis sisteminis procesas, kurio metu peržiūrimi ir patikrinami visi duomenys bei apskaičiuojamas apgaulės rezultatas, gali stipriai paveikti našumą.  Organizacijos, naudojančios šią funkciją, prieš keisdamos taisykles ar statinių apgaulingų duomenų kriterijus gamybos aplinkoje turi visada patikrinti ir patvirtinti, kad užsakymo pateikimo apdorojimo laikas yra priimtinas.

