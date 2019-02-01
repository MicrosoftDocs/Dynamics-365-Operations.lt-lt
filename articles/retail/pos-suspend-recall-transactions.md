---
title: "Elektroninio kasos aparato (EKA) operacijos sustabdymas ir pratęsimas"
description: "Šioje temoje paaiškinama, kaip vartotojai gali sustabdyti vykdomas operacijas, o paskui jas tęsti vėliau arba kitame kasos aparate naudodami „Microsoft Dynamics 365 for Retail“."
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: ffb04609318c7de4b9ef729a8e03a7f9395806b8
ms.contentlocale: lt-lt
ms.lasthandoff: 01/04/2019

---

# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a>Elektroninio kasos aparato (EKA) operacijų sustabdymas ir pratęsimas

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Elektroninio kasos aparato (EKA) vartotojai gali sustabdyti vykdomas operacijas, o paskui jas tęsti vėliau arba kitame kasos aparate. Operacijos dažnai sustabdomos tam, kad būtų galima greitai atlaisvinti kasos aparatą kitai užduočiai, neprarandant dabartinės operacijos vykdymo eigos. Pavyzdžiui, parduotuvės atstovas pradeda apdoroti kliento operaciją mobiliajame įrenginyje, bet turi ją užbaigti kasos aparate, kuriame yra kasos stalčius. Šiuo atveju parduotuvės atstovas gali sustabdyti operaciją mobiliajame įrenginyje, o paskui atšaukti ir ją tęsti kasos aparate.

## <a name="configure-suspend-and-resume-functionality"></a>Sustabdymo ir pratęsimo funkcijų konfigūravimas

### <a name="pos-operations"></a>POS operacijos

Dvi [EKA operacijos](pos-operations.md) leidžia EKA palaikyti sustabdymo ir pratęsimo scenarijus. Šias operacijas galite priskirti [mygtukynams](pos-screen-layouts.md) operacijų arba darbo pradžios puslapiuose.

- 503: sustabdyti operaciją
- 504: atšaukti operaciją

### <a name="receipt-template"></a>Kvito šablonas

EKA galima konfigūruoti važtaraščiui generuoti, kai operacija sustabdyta. Paskui šį kvitą galima naudoti norint greitai identifikuoti ir vėliau atšaukti operaciją.

Norėdami įgalinti EKA spausdinti kvitą, turite įtraukti kvito formatą **Sustabdyta operacija** į parduotuvės kvitų šabloną. Kvito formatą galite sudaryti taip, kad jis apimtų arba neįtrauktų konkrečių duomenų apie operaciją. Pavyzdžiui, formatas gali apimti brūkšninį kodą nuskaitymui palaikyti.

### <a name="receipt-numbering"></a>Kvitų numeravimas

Kaip ir kitiems EKA operacijų tipams, generuojantiems spausdintą kvitą, galite nurodyti sustabdytų operacijų numerių seką parduotuvės funkcijų šablono dalyje **Kvitų numeravimas**.

### <a name="void-when-closing-shift"></a>Anuliuoti uždarant pamainą

Galite naudoti parinktį **Anuliuoti uždarant pamainą**, jei reikia, kad prieš uždarydami savo pamainą vartotojai užbaigtų arba anuliuotų visas sustabdytas operacijas. Per operaciją **Uždaryti pamainą** EKA paragins vartotojus peržiūrėti arba anuliuoti visas neįvykdytas sustabdytas operacijas.

## <a name="suspend-and-resume-a-transaction"></a>Sustabdyti ir tęsti operaciją

### <a name="suspend-a-transaction"></a>Sustabdyti operaciją

Vartotojai, turintys pakankamai teisių ir naudojantys ekrano maketą, kuris apima operaciją **Sustabdyti operaciją**, gali sustabdyti operaciją taip, kad ją būtų galima atšaukti vėliau arba kitame kasos aparate.

Operacijas galima sustabdyti tik tada, jei jose **nėra** šių eilučių tipų:

- Aktyvios mokėjimo eilutės
- Dovanų kortelių eilutės (išduoti dovanų kortelę arba pridėti prie dovanų kortelės balanso)

Sustabdyta operacija neturi poveikio pardavimo informacijai arba informacijai apie atsargų likučius parduotuvėje.

### <a name="resume-a-suspended-transaction"></a>Tęsti sustabdytą operaciją

Sustabdytas operacijas gali atšaukti ir toje pačioje parduotuvėje pratęsti bet kuris vartotojas, turintis pakankamai teisių ir taip pat naudojantis maketą, kuris apima operaciją **Atšaukti operaciją**.

Norėdami greitai ir lengvai atšaukti sustabdytą operaciją, nuskaitykite ant spausdinto kvito esantį brūkšninį kodą peržiūrėdami operacijos **Atšaukti operaciją** operacijų sąrašą.

### <a name="considerations-for-offline-mode"></a>Autonominio režimo aplinkybės

- Bet kokios sustabdytos operacijos, kol EKA veikia internetiniu režimu, negalima tęsti autonominiu režimu, nes duomenys su autonomine duomenų baze nesinchronizuojami.
- Jei sustabdote operaciją, kol EKA veikia autonominiu režimu, galite ją atšaukti autonominiu režimu, jei EKA nebuvo perjungtas į internetinį režimą bet kuriuo metu nuo tada, kai sustabdėte operaciją. EKA perjungus į internetinį režimą, duomenys apie sustabdytas operacijas perkeliami į internetinę duomenų bazę ir pašalinami iš autonominės duomenų bazės. Todėl operacijas galima tęsti tik internetiniu režimu. Jei perjungsite EKA į autonominį režimą, negalėsite tęsti šių sustabdytų operacijų, nes jos jau buvo pašalintos iš autonominės duomenų bazės.

### <a name="void-a-suspended-transaction"></a>Anuliuoti sustabdytą operaciją

Galite anuliuoti sustabdytas operacijas atšaukdami operaciją, o paskui atlikdami operaciją **Anuliuoti operaciją**, arba pasirinkdami operaciją sąraše **Atšaukti operaciją** ir programos juostoje pasirinkdami **Anuliuoti**. Taip pat galima sukonfigūruoti parduotuvę, kad vartotojai būtų raginami anuliuoti sustabdytas operacijas, kai jie baigia savo pamainą.
