---
title: Išmokų valdymo apžvalga
description: Išmokų valdymo funkcijos programoje „Dynamics 365 Human Resources“ apžvalga. Siūlykite savo darbuotojams išplėstines išmokų parinktis naudodami paprastas naudoti internetines funkcijas.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4157cb1f83d686d435f3d04e47c578df455376c9
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429271"
---
# <a name="benefits-management-overview"></a>Išmokų valdymo apžvalga

Norėdami išlikti konkurencingi, turite pasiūlyti gausų išmokų rinkinį, kad pritrauktumėte ir išlaikytumėte savo geriausius darbuotojus. Be įprastų privalumų, pvz., sveikatos ir dantų priežiūros draudimo, taip pat galite siūlyti išplėstines paslaugas, pvz., įvaikinimo pagalbą, poilsio programas ir išmokas drabužiams. Išmokų valdymas programoje „Microsoft Dynamics 365 Human Resources“ – dinamiškas sprendimas, palaikantis daugybę išmokų parinkčių. „Human Resources“ taip pat apima lengvai naudojamas darbuotojų funkcijas, kuriomis demonstruojami jūsų pasiūlymai.

- Išplėstiniai išmokų planai leidžia kurti ir valdyti unikalius išmokų planus ir palaikymo sudėtinių išmokų tarifų lenteles ir įdėtąsias pakopas. Galite lengvai sukurti išmokų programas, paketus ir automatinės registracijos taisykles, kad palengvintumėte darbuotojo patirtį.

- Lanksčiųjų kreditų programomis galite proporcingai paskirstyti, kad būtų palaikomi išėjimas į pensiją ir kiti gyvenimo įvykiai.

- Dėl platesnių tinkamumo taisyklių galite būti užtikrinti, kad reikiamos išmokos pasieks reikiamus darbuotojus.

- Internetine išmokų registracija suteikiama puiki jūsų darbuotojų patirtis.

- Tinkamo gyvenimo įvykio apdorojimas palaiko būsimus gyvenimo įvykius.

Jei norite gauti prieigą prie demonstracinių duomenų, turite iš naujo įdiegti savo smėlio dėžės aplinką.

## <a name="benefits-management-known-issues"></a>Išmokų valdymo žinomos problemos

### <a name="flex-credit-programs"></a>Lanksčiųjų kreditų programos

Bendra kreditų vertė, nustatyta lanksčiųjų kreditų programai, nėra rodoma formoje **Darbininkų išmokų planai**. Be to, jei lanksčiųjų kreditų programoje esančią proporcingumo taisyklę nustatysite į **Nėra**, formoje **Darbininkų išmokų planai** pasirenkant ir patvirtinant planus gali kilti klaida.

## <a name="enable-benefits-management"></a>Išmokų valdymo įjungimas

Šiame straipsnyje aprašoma, kaip įjungti „Human Resources“ funkcijas. Jame taip pat nurodoma, kurios esamos „Human Resources“ funkcijos išmokų valdyme pakeičiamos arba kurios yra išjungiamos, kai įjungiate išmokų valdymą.

> [!IMPORTANT]
> Po to, kai **gamybos** aplinkoje įgalinate išmokų valdymą, jo išjungti negalima. Rekomenduojame įjungti ir testuoti išmokų valdymą **smėlio dėžės** aplinkoje prieš įjungiant jį **gamybos** aplinkoje. Yra reikšmingų skirtumų tarp pasenusių išmokų funkcijų ir naujų išmokų valdymo funkcijų – joms reikalingi papildomi nustatymai ir tikrinimai prieš įtraukiant į gamybos procesą.

- [Funkcijų valdymas](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Darbuotojų informacijos konfigūravimas

Kad užregistruotumėte darbuotojus išmokoms gauti, turite pateikti reikiamą informaciją. Turite užregistruoti darbuotoją į **pastoviosios atlyginimo dalies planą** jų darbo pradžios dieną ir pasirinkti **išmokų mokėjimo dažnumą** dalies **Įdarbinimo informacija** formoje **Darbininkas**.

Kai kuriate išmokų planą, naudojantį tarifus, pagrįstus lytimi arba amžiumi, turite įvesti darbuotojo gimimo datą ir lytį, kad būtų apskaičiuota išmokų savikaina.

## <a name="configure-benefits-management"></a>Išmokų valdymo konfigūravimas

Kad galėtumėte kurti savo darbuotojų išmokų planus, reikia konfigūruoti planų parinktis.

- [Išmokų valdymo parametrų nustatymas](hr-benefits-setup-parameters.md)
- [Tinkamumo taisyklių ir parinkčių konfigūravimas](hr-benefits-setup-eligibility-rules.md)
- [Asmeninio kontakto tinkamumo parinkčių konfigūravimas](hr-benefits-setup-contact-eligibility-options.md)
- [Padengimo parinkčių kūrimas](hr-benefits-setup-coverage-options.md)
- [Mokėjimo dažnumo nustatymas](hr-benefits-setup-payment-frequencies.md)
- [Gyvenimo įvykių tipų konfigūravimas](hr-benefits-setup-life-event-types.md)
- [Planų tipų kūrimas](hr-benefits-setup-plan-types.md)
- [Priežasčių kodų nustatymas](hr-benefits-setup-reason-codes.md)
- [Pakopos kodų nustatymas](hr-benefits-setup-tier-codes.md)
- [Tarifų konfigūravimas](hr-benefits-setup-rates.md)
- [Atskaitymų konfigūravimas](hr-benefits-setup-deductions.md)
- [Laukimo dienų konfigūravimas](hr-benefits-setup-waiting-days.md)
- [Laukimo laikotarpių konfigūravimas](hr-benefits-setup-waiting-periods.md)
- [Apvalinimo taisyklių nustatymas](hr-benefits-setup-rounding-rules.md)
- [Įdarbinimo kategorijų kūrimas](hr-benefits-setup-employment-categories.md)
- [Įdarbinimo tipų nustatymas](hr-benefits-setup-employment-types.md)
- [Darbuotojų savitarnos paslaugos konfugūravimas](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Išmokų planų kūrimas

Šiuose straipsniuose nurodoma, kaip sukurti išmokų planus, įskaitant grupių ir lanksčiųjų kreditų programas.

- [Išmokų planų nustatymas](hr-benefits-plans-setup.md)
- [Lanksčių kredito programų nustatymas](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Išmokų planų apdorojimas

Turite apdoroti kai kuriuos keitimus, kad jie būtų aktyvūs.

- [Tinkamumo registracijai apdorojimas](hr-benefits-process-enrollment-eligibility.md)
- [Gyvenimo įvykių apdorojimas](hr-benefits-process-life-events.md)
- [Gyvenimo įvykio keitimų apdorojimas](hr-benefits-process-life-event-changes.md)
- [Gyvenimo įvykio tinkamumo apdorojimas](hr-benefits-process-life-event-eligibility.md)
- [Tarifo pakeitimų apdorojimas](hr-benefits-process-rate-changes.md)

