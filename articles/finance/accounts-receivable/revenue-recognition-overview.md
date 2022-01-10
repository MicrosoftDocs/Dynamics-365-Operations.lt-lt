---
title: Įplaukų pripažinimo funkcijos apžvalga (yra vaizdo įrašas)
description: Šioje temoje pateikiama informacija apie įplaukų pripažinimo funkciją. Šia funkcija teikiama lanksti sistema, leidžianti nustatyti įmonei būdingas taisykles, skirtas kelių elementų užsakymų tiek įplaukų vertei, tiek įplaukų grafikui pripažinti.
author: kweekley
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.custom: intro-internal
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: c027b3edb12c34c2373c58a5aa7e39cfbff39045
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937587"
---
# <a name="revenue-recognition-overview"></a>Įplaukų pripažinimo apžvalga

[!include [banner](../includes/banner.md)]

Pramonės šakų įmonės, prekiaujančios keliais elementais, pvz., produktais, paslaugomis, abonementais ir t. t., privalo galėti išskaidyti kelių elementų užsakymus, kad įplaukos galėtų būti pripažintos pagal konkrečios įmonės ir konkrečios pramonės šakos rekomendacijų rinkinį.

> [!NOTE]
> Įplaukų pripažinimo funkcija negali būti įjungta naudojant funkcijų valdymą. Dabar norėdami ją įjungti, turite naudoti konfigūracijos raktus.

> Įplaukų atpažinimas, įskaitant grupavimo funkcijas, nepalaikomas „Commerce“ kanaluose (el. prekyba, EKA, skambučių centras). Prekės, sukonfigūruotos atpažinti įplaukas, neturėtų būti įtraukiamos į „Commerce“ kanaluose sukurtus užsakymus ar operacijas.

Paprastai įplaukų pripažinimo procesas gali būti naudojamas šioms užduotims atlikti:

* Įplaukoms paskirstyti, siekiant padėti užtikrinti, kad tinkama įplaukų vertė būtų pripažinta remiantis kelių elementų užsakymų komponentų verte.
* Įplaukoms atidėti pagal įplaukų grafiką, nurodantį sutartinius laikotarpius ir procentus, skirtus įplaukoms per tam tikrą laikotarpį pripažinti.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

[Įplaukų pripažinimo funkcijos naudojimo „Dynamics 365 Finance“](https://youtu.be/v3amIsiqvoo) vaizdo įrašas (pateiktas pirmiau) yra įtrauktas į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kurį galima rasti „YouTube“.

Įplaukų pripažinimo funkcija teikiama lanksti sistema, leidžianti nustatyti įmonei būdingas taisykles, skirtas tiek įplaukų vertei, tiek įplaukų grafikui pripažinti.

Patvirtinti produktai naudojami įplaukų pripažinimui pardavimo užsakymų dokumentuose palaikyti. Išleisti produktai apima sąranką, kurios reikia įplaukų vertei ir įplaukų grafikui apibrėžti. Pardavimo užsakymas gali būti sukurtas iš laiko ir medžiagų projekto.

Įmonės gali naudoti įplaukų grafiko funkcijas nenaudodamos įplaukų vertės funkcijos. Todėl pardavimo užsakymo eilutėse nurodyta kaina bus naudojama arba kaip įplaukos, arba kaip atidėtos įplaukos. Jei pardavimo užsakymo eilutėje nurodytas įplaukų grafikas, pardavimo užsakymo eilutėje nurodyta kaina bus atidėta. Jei pardavimo užsakymo eilutėje įplaukų grafikas nenurodytas, pardavimo eilutėje nurodyta kaina įplaukų sąskaitoje bus užregistruota išrašius sąskaitą faktūrą.

Įplaukų vertė apskaičiuojama patvirtinus pardavimo užsakymą arba užregistravus sąskaitą faktūrą. Norėdami peržiūrėti įplaukų vertę prieš tai, kai sąskaita faktūra yra užregistruojama, turite patvirtinti pardavimo užsakymą.

Patvirtinus pardavimo užsakymą, taip pat sukuriamas numatomas įplaukų grafikas, jei bet kurioje pardavimo užsakymo eilutėje nurodytas įplaukų grafikas. Išrašius pardavimo užsakymo sąskaitą faktūrą, numatomas įplaukų grafikas panaikinamas ir numatomas įplaukų grafikas keičiamas faktiniu įplaukų pripažinimo grafiku.

Išlaikoma kiekvienos pardavimo užsakymo eilutės išsami įplaukų pripažinimo grafiko informacija. Todėl pajamų pripažinimo vadybininkas gali peržiūrėti išsamią informaciją ir išleisti eilutes į įplaukas, kai yra įvykdytas sutartinis įsipareigojimas. Kiekvieno laikotarpio pabaigoje pajamų pripažinimo vadybininkas gali sukurti įplaukų žurnalą ir išleisti bet kokias grafiko eilutes, kurias reikia įvykdyti vadybininko nustatytą datą arba prieš ją. Šis įplaukų žurnalas nėra užregistruojamas iš karto. Todėl pajamų pripažinimo vadybininkas gali patikrinti, ar tinkamos sumos išleidžiamos iš atidėtų įplaukų į faktines įplaukas.

Jeigu dėl sutarties pakeitimų nauja pardavimo užsakymo eilutė įtraukiama arba į esamą pardavimo užsakymą, arba į naują pardavimo užsakymą, gali būti vykdomas perskirstymo procesas siekiant ištaisyti visų pardavimo užsakymų eilučių įplaukų vertę.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]