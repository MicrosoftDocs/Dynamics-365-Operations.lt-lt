---
title: Inžinerijos bendrovės ir duomenų turėjimo taisyklės
description: Šioje temoje paaiškina, kaip galite naudoti vieną ar keletą inžinerijos bendrovių siekiant užtikrinti, kad pagrindiniai duomenys produktams yra sukuriami ir palaikomi centriniu būdu. Inžinerijos bendrovė reiškia įmonę, kuri turi inžinerijos produktus ir su jų inžinerija susijusius duomenis.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: a434bf3727432f4964b7b0ed60905449378245de
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830008"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Inžinerijos bendrovės ir duomenų turėjimo taisyklės

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Inžinerijos bendrovės ir veikiančios bendrovės

Siekiant užtikrinti pagrindiniai duomenys produktams yra sukuriami ir palaikomi centriniu būdu galite naudoti vieną ar daugiau *inžinerijos bendrovių*. Inžinerijos bendrovė reiškia įmonę, kuri turi inžinerijos produktus ir su jų inžinerija susijusius duomenis. Ji visuomet susijusi su (pagrįsta) esančiu *juridiniu subjektu*, kuris yra ir bendrovė. Per šią jungtį, sistema įsteigia centrinį įvesties tašką visiems su inžinerija susijusiems duomenims inžinerijos produktams inžinerijos bendrovėje. Šiame centriniame įvesties taške produktai yra sukuriami ir su inžinerija susiję duomenys laikomi. Iš jų, visi inžinerijos produktai ir su jais susiję duomenys yra išleidžiami į *veikiančias bendroves*, kurios yra kiti juridiniai subjektai. (Dėl daugiau informacijos apie išleidimo valdymą, žr. [Išleidimo produkto struktūros](release-product-structure.md).) Šios veikiančios bendrovės naudos inžinerijos duomenis taip, kaip jie buvo nustatyti inžinerijos bendrovės. Bet kurie logistikos duomenys yra laikomi kiekvienoje inžinerijos bendrovėje ir operacijos bendrovėje.

Norėdami sukurti inžinerijos bendrovę, eikite į **Inžinerijos keitimų valdymas \> Nustatymai \> Inžinerijos organizacijos**. Rinkitės **Naujas**, įveskite inžinerijos bendrovės pavadinimą ir pasirinkite esančią bendrovę (juridinį subjektą), kuriuo ji grįsta.

Jei integruojate išorės produkto gyvavimo ciklo valdymo (PLM) sistemas, turite sukurti verslo vienetą (įmonės tipą), kuris taps išorės bendrove.

## <a name="engineering-product-categories-and-engineering-companies"></a>Inžinerijos produkto kategorijos ir inžinerijos bendrovės

*Inžinerijos produkto kategorijos* padeda užtikrinti, kad inžinerijos produktai yra sukurti pagal jūsų bendrovės veiklos taisykles ir elgiasi kaip reikia. Dėl daugiau informacijos apie inžinerijos produktų kategorijas, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).

Visos inžinerijos produkto kategorijos priklauso konkrečiai inžinerijos bendrovei ir gali sukurti tik produktus priklausančius tai bendrovei. Taip pat, teisė palaikyti inžinerijos produktą taip pat priklauso bendrovei, kuri susieta su produkto inžinerijos produkto kategorija.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Duomenis turi inžinerijos bendrovė

Kadangi Inžinerijos bendrovė reiškia įmonę, kuri turi inžinerijos duomenis, ji valdo šiuos procesus:

- **Inžinerijos produktų sukūrimą:** Visos inžinerijos bendrovės gali sukurti tik naujus inžinerijos produktus, pagrįstus turima inžinerijos produkto kategorija. Kai kuriais atvejais, veikiančios bendrovė išlaiko jų turimus lokalius duomenis, kurie susiję su tais produktais.
- **Inžinerijos versijų sukūrimas:** Bendrovei sukūrus naują inžinerijos produktą, sistema automatiška sukuria pradinę inžinerijos versiją. Tik turinti inžinerijos bendrovė galės sukurti naujas to produkto versijas.
- **Inžinerijos atributų kūrimas ir priežiūra:** Bendrovei sukūrus naują inžinerijos produktą, sistema automatiška įtraukia inžinerijos atributus į ją. Tik turinti inžinerijos bendrovė galės sukurti ir palaikyti šių atributų vertes. Dėl daugiau informacijos apie inžinerijos atributus kategorijas, žr. [Inžinerijos atributai ir inžinerijos atributų paieška](engineering-attributes-and-search.md).
- **Komplektavimo specifikacijų (KS), kurie yra susieti su inžinerijos versijomis, kūrimas ir priežiūra:** Inžinerijos bendrovės turėjimas gali tiesiogiai sujungti KS su inžinerijos produkto versija. Kai šie KS yra išleisti į kitus juridinius subjektus, tų inžinerijos duomenų keitimai KS yra apriboti tokiais būdais:

    - Veikianti bendrovė negali pašalinti išleistų KS eilučių.
    - Inžinerijos laukeliai KS eilutėse skirti tik skaitymui veikiančiai bendrovei. Visi kiti laukeliai yra logistiškai įdiegiami ir gali būti redaguojami veikiančios įmonės.
    - Veikianti bendrovė negali įtraukti KS eilutes į tą patį KS. Tokiu būdu, ji gali įtraukti vietinius priedus, tokius kaip pakavimo medžiagos ar sutepimo skysčiai.
    - Veikianti bendrovė gali įtraukti visai naują, vietinį KS. Tokio pokyčio gali reikėti tada, kai pavyzdžiui, nėra jokio KS pateikto šių leidimų metu. Veikianti bendrovė turi ir palaiko šiuos KS. Išsamesnei informacijos apie leidimo valdymą žr. [Leidimo produkto struktūros](release-product-structure.md).
    - Visi vietiniai KS ir KS eilutės yra saugomos, kai inžinerijos bendrovės naujina savo KS.

- **Maršrutų sukūrimas ir palaikymas, kurie yra susieti su inžinerijos versijomis:** Inžinerijos bendrovės turėjimas gali tiesiogiai sujungti maršrutu su kiekviena inžinerijos versija. Kai šie maršrutai yra išleisti į kitus juridinius subjektus, tų inžinerijos duomenų keitimai maršrutai yra apriboti tokiais būdais:

    - Kiti juridiniai subjektai negali pašalinti inžinerijos duomenų maršrutuose.
    - Kiti juridiniai subjektai gali įtraukti veiksmus į maršrutą. Tokiu būdu jie gali įtraukti vietinius maršruto žingsnius.
    - Veikiančios bendrovės gali įtraukti visai naują, vietinį maršrutą. Tokio pokyčio gali reikėti tada, jei pavyzdžiui, neįtraukėte maršrutų leidimo metu. Veikianti bendrovė turi ir palaiko savo vietinį maršrutą. Išsamesnei informacijai apie leidimo valdymą žr. [Leidimo produkto struktūros](release-product-structure.md).
    - Visi keitimai yra padaromi lokaliai ir saugomi, kai naujiniai inžinerijos bendrovei išleidžiami dar kartą į maršrutus.

- **Inžinerijos dokumentų sukūrimas ir palaikymas:** Inžinerijos bendrovė gali pridėti inžinerijos dokumentus į kiekvieną inžinerijos versiją.

    - Kai šie dokumentai išleisti į kitus juridinius subjektus, dokumentai yra apsaugoti nuo panaikinimo jų veikiančios bendrovės.
    - Kiti juridiniai subjektai gali įtraukti visai naujus, vietinius dokumentus. Veikianti bendrovė turi ir palaiko šiuos vietinius dokumentus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]