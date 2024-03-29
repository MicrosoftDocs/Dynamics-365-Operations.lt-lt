---
title: Atidėjimai
description: Šiame straipsnyje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.
author: t-benebo
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e7e0150e40193f2f799677ad19cae2ea589afc0
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740636"
---
# <a name="delays"></a>Atidėjimai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie atidėtas bendrojo planavimo datas. Atidėta data yra realus terminas, kurį gauna operacija, jei bendrojo planavimo metu apskaičiuota anksčiausia įvykdymo data yra vėlesnė nei pareikalauta data.

Bendrasis planavimas pagal vykdymo laiką, turimas medžiagas, turimus pajėgumus ir įvairius planavimo parametrus gali apskaičiuoti anksčiausią operacijos įvykdymo datą. 

Jei bendrojo planavimo apskaičiuota užsakymo data yra ankstesnė negu dabartinė data, užsakymas negali būti įvykdytas laiku. Todėl užsakymas atidedamas. Tokiu atveju bendrasis planavimas suplanuoja užsakymą į ateitį nuo dabartinės datos ir įtraukia vykdymo laikus. Šie vykdymo laikai prasideda nuo žemesnio lygio komponento elementų. Tada užsakymui suteikiama atidėjimo data. Atidėjimo data yra realus terminas, sugeneruotas remiantis esamais duomenimis. Bendrasis planavimas taip pat apskaičiuoja atidėjimo dienų skaičių. 

Kai kuriais atvejais jūs galite pasirinkti neapskaičiuoti atidėjimų, pvz., kai vartotojai žino, kad jie gali pagreitinti vykdymo laikus, pasirinkdami alternatyvius pristatymo būdus. 

Galite konfigūruoti, kaip skaičiuojami padengimo grupės atidėjimai. Vėliau prie prekės galite pridėti padengimo grupę. 

Puslapyje **Bendrojo planavimo parametrai** galite nustatyti atidėjimų skaičiavimo pradžios laiką. Jei užsakymas įvykdomas po šio laiko, prie užsakymo atidėjimo datos pridedamas vienos dienos atidėjimas. 

> [!NOTE]
> Ankstesnėse versijose apskaičiuoti atidėjimai buvo vadinami *ateities pranešimais*, atidėjimo data buvo vadinama *ateities data*, o atidėta *operacija buvo vadinama į ateitį nustatyta operacija*.

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a>Riboti vėlavimai gamybos sąrankoje, turinčioje kelis KS lygius
Kai dirbate su vėlavimais gamybos sąrankoje, turinčioje kelis KS lygius, svarbu atkreipti dėmesį, kad tik prekės, esančios tiesiai virš prekės (KS struktūroje), kurios sukelia vėlavimą, bus atnaujintos vėlavimu kaip bendrojo planavimo vykdymo dalis. Kitoms KS struktūros prekėms nebus taikomas vėlavimas iki pirmo bendrojo planavimo vykdymo, kai patvirtinamas aukščiausio lygio suplanuotas užsakymas. 

Norint apeiti šį žinomą apribojimą, prieš kitą bendrojo planavimo vykdymą KS struktūros viršuje esantys gamybos užsakymai su vėlavimais gali būti patvirtinami. Taip bus saugomas atidėto patvirtinto suplanuoto gamybos užsakymo vėlavimas ir atitinkamai atnaujinti visi esami komponentai.
Veiksmo pranešimus taip pat galima naudoti norint nustatyti suplanuotus užsakymus, kuriuos galima perkelti į vėlesnę datą dėl kitų KS struktūros vėlavimų.

## <a name="desired-date"></a>Norima data

Puslapio **Suplanuotas užsakymas** skirtuke **Atidėjimai** nurodyta suplanuoto užsakymo **Norima data**. Norima suplanuoto užsakymo data yra pagrindinė atidėjimų data – apskaičiuota data, lygi **pageidaujamai datai**, apskaičiuotai pagal **grynąjį poreikį**. Jei suplanuotas užsakymas yra KS eilutė, gamybos eilutė arba „kanban“ eilutė, norima data nustatoma pagal **pageidaujamą datą** ir norima data nebus rodoma puslapyje **Suplanuotas užsakymas**.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Padengimo parametrai](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]