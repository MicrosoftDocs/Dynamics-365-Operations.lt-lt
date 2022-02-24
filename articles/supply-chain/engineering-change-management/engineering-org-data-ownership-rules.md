---
title: Inžinerijos bendrovės ir duomenų turėjimo taisyklės
description: Šioje temoje paaiškina, kaip galite naudoti vieną ar keletą inžinerijos bendrovių siekiant užtikrinti, kad pagrindiniai duomenys produktams yra sukuriami ir palaikomi centriniu būdu. Inžinerijos bendrovė reiškia įmonę, kuri turi inžinerijos produktus ir su jų inžinerija susijusius duomenis.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: ab5ca3bee65bb0ee8ce7f44ba97c00347fe38366
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963668"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Inžinerijos bendrovės ir duomenų turėjimo taisyklės

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Inžinerijos bendrovės ir veikiančios bendrovės

Siekiant užtikrinti pagrindiniai duomenys produktams yra sukuriami ir palaikomi centriniu būdu galite naudoti vieną ar daugiau *inžinerijos bendrovių*. Inžinerijos bendrovė reiškia įmonę, kuri turi inžinerijos produktus ir su jų inžinerija susijusius duomenis. Ji visuomet susijusi su (pagrįsta) esančiu *juridinu asmeniu*, kuris yra ir bendrovė. Per šią jungtį, sistema įsteigia centrinį įvesties tašką visiems su inžinerija susijusiems duomenims inžinerijos produktams inžinerijos bendrovėje. Šiame centriame įvesties taške produktai yra sukuriami ir su inžinerija susiję duomenys laikomi. Iš jų, visi inžinerijos produktai ir su jais susiję duomenys yra išleidžiami į *veikiančias bendroves*, kurios yra kiti juridiniai asmenys. (Dėl daugiau informacijos apie išleidimo valdymą, žr. [Išleidimo produkto struktūros](release-product-structure.md).) Šios veikiančios bendrovės naudos inžinerijos duomenis taip, kaip jie buvo nustatyti inžinerijos bendrovės. Bet kurie logistinia duomenys yra laikomi lokiai inžinerijos bendrovės ir operacijos bendrovės.

Norėdami sukurti inžinerijos bendrovę, eikite į **Inžinerijos keitim valdymas \> Nustatymys \> Inžinerijso organizacijos**. Rinkitės **Naujas**, įveskite inžinerijos bendrovės pavadinimą ir pasirinkite esančią bendrovę (juridinį asmenį), kuriuo ji grįsta.

Jei integruojate išorės produkto gyvavimo ciklo valdymo (PLM) sistemas, turite sukurti verslo vienetą (įmonės tipą), kuris taps išorės bendrove.

## <a name="engineering-product-categories-and-engineering-companies"></a>Inžinerijos produkto kategorijos ir inžinerijos bendrovės

*Inžinerijos produkto kategorijos* padeda užtikrinti, kad inžinerjos produktai yra sukurti pagal jūsų bendrovės verslo taisykles ir elgiasi kaip reikia. Dėl daugiau informacijos apie inžinerijos produktų kategorijas, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).

Visos inžinerijos produkto kategorijos priklauso konkrečiai inžinerijos bendrovei ir gali sukurti tik produktus priklausančius tai bendrovei. Taip pat, teisė palaikyti inžinerijos produktą taip pat priklauso bendrovei, kuri susieta su produkto inžinerijos produkto kategorija.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Duomenis turi inžinerijos bendrovė

Kadangi Inžinerijos bendrovė reiškia įmonę, kuri turi inžinerijos duomenis, ji valdo šiuos procesus:

- **Inžinerijos produktų sukūrimą:** Visos inžinerijos bendrovės gali sukurti tik naujus inžinerijos produktus, pagrįstus turima inžinerijos produkto kategorija. Kai kuriais atvejais, veikiančios bendrovė išlaiko jų turimus lokalius duomenis, kurie susiję su tais produktais.
- **Inžinerijos versijų sukūrimas:** Bendrovei sukūrus naują inžinerijos produktą, sistema automatiška isukuria pradinė inžinerijos versiją. Tik turinti inžinerijos bendrovė galės sukurti naujas to produkto versijas.
- **Inžinerijos atribūtų sukūrimas ir palaikymas:** Bendrovei sukūrus naują inžinerijos produktą, sistema automatiška įtraukia inžinerijos atributus į ją. Tik turinti inžinerijos bendrovė galės sukurti ir palaikyti šių atributų vertes. Dėl daugiau informacijos apie inžinerijos atributus kategorijas, žr. [Inžinerijos atributai ir inžinerijos atributų paieška](engineering-attributes-and-search.md).
- **Važtaraščių sukūrimas ir palaikymas (BOMs), kurie yra susieti su inžinerijos versijomis:** Inžinerijos bendrovės turėjimas gali tiesiogia sujungti BOM su inžinerijos produkto versija. Kai šie BOM yra išleisti į kitus juridinius asmenis, tų inžinerijos duomenų keitimai BOM yra apriboti tokiais būdais:

    - Veikianti bendrovė negali pašalinti išleistų BOM eilučių.
    - Inžinerijos laukeliai BOM eilutėse skirti tik skaitymui veikiančiai bendrovei. Visi kiti laukeliai yra logistiškai implementuojami ir gali būti redaguojami veikiančios įmonės.
    - Veikianti bendrovė negali įtraukti BOM eilutes į tą patį BOM. Tokiu būdu, ji gali įtraukti vietinius priedus, tokius kaip pakavimo medžiagos ar sutepimo skysčiai.
    - Veikianti bendrovė gali įtraukti visai naują, vietinį BOM. Tokio pokyčio gali reikėti tada, kai pavyzdžiui, nėra jokio BOM pateikto šių leidimų metu. Veikianti bendrovė turi ir palaiko šiuos BOM. Dėl išsamensės informacijos apie leidimo valdymą, žr. [Leidimo produkto struktūros](release-product-structure.md).
    - Visi vietiniai BOM ir BOM eilutės yra saugomos, kai inžinerijos bendrovės naujina savo BOM.

- **Maršrutų sukūrimas ir palaikymas, kurie yra susieti su inžinerijos versijomis:** Inžinerijos bendrovės turėjimas gali tiesiogia sujungti maršrutu su kiekviena inžinerijos versija. Kai šie maršrutai yra išleisti į kitus juridinius asmenis, tų inžinerijos duomenų keitimai maršrutai yra apriboti tokiais būdais:

    - Kiti jurdiniai asmenys negali pašalinti inžinerijos duomenų maršrutuose.
    - Kiti juridiniai asmenys gali įtraukti veiksmus į maršrutą. Tokiu būdu, jie gali įtraukti vietinius maršruto žingsnius.
    - Veikiančios bendrovės gali įtraukti visai naują, vietinį maršrutą. Tokio pokyčio gali reikėti tada, jei pavyzdžiui, neįtraukėte maršrutų leidimo metu. Veikianti bendrovė turi ir palaiko savo vietinį maršrutą. Dėl išsamensės informacijos apie leidimo valdymą, žr. [Leidimo produkto struktūros](release-product-structure.md).
    - Visi keitimai yra padaromi lokaliai ir saugomi, kai nuajiniai inžinerijos bendrovei išleidžiami dar kartą į maršrutus.

- **Inžinerijos dokumentų sukūrimas ir palaikymas:** Inžinerijos bendrovė gali pridėti inžinerijos dokumentus į kiekvieną inžinerijos versiją.

    - Kai šie dokumentai išleisti į kitus juridinius asmenis, dokumentai yra apsaugoti nuo panaikinimo jų veikiančios bendrovės.
    - Kiti juridinia asmenys gali įtraukti visai naujus, vietinius dokumentus. Veikianti bendrovė turi ir palaiko šiuos vietinius dokumentus.
