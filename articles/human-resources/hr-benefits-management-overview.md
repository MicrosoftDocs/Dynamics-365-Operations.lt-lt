---
title: Išmokų valdymo apžvalga
description: Išmokų valdymo peržiūros funkcijos programoje „Dynamics 365 Human Resources“ apžvalga. Siūlykite savo darbuotojams išplėstines išmokų parinktis naudodami paprastas naudoti internetines funkcijas.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029468"
---
# <a name="benefits-management-overview"></a>Išmokų valdymo apžvalga

[!include [banner](includes/preview-feature.md)]

Norėdami išlikti konkurencingi, turite pasiūlyti gausų išmokų rinkinį, kad pritrauktumėte ir išlaikytumėte savo geriausius darbuotojus. Be įprastų privalumų, pvz., sveikatos ir dantų priežiūros draudimo, taip pat galite siūlyti išplėstines paslaugas, pvz., įvaikinimo pagalbą, poilsio programas ir išmokas drabužiams. Išmokų valdymo peržiūros funkcija programoje „Microsoft Dynamics 365 Human Resources“ – dinamiškas sprendimas, palaikantis daugybę išmokų parinkčių. „Human Resources“ taip pat apima lengvai naudojamas darbuotojų funkcijas, kuriomis demonstruojami jūsų pasiūlymai.

- Išplėstiniai išmokų planai leidžia kurti ir valdyti unikalius išmokų planus ir palaikymo sudėtinių išmokų tarifų lenteles ir įdėtąsias pakopas. Galite lengvai sukurti išmokų programas, paketus ir automatinės registracijos taisykles, kad palengvintumėte darbuotojo patirtį.

- Lanksčiųjų kreditų programomis galite proporcingai paskirstyti, kad būtų palaikomi išėjimas į pensiją ir kiti gyvenimo įvykiai.

- Dėl platesnių tinkamumo taisyklių galite būti užtikrinti, kad reikiamos išmokos pasieks reikiamus darbuotojus.

- Internetine išmokų registracija suteikiama puiki jūsų darbuotojų patirtis.

- Tinkamo gyvenimo įvykio apdorojimas integruojamas su darbuotojo savitarnos paslauga, taip pat palaiko būsimus gyvenimo įvykius.

Jei norite gauti prieigą prie demonstracinių duomenų, turite iš naujo įdiegti savo smėlio dėžės aplinką.

Galite pateikti tiesioginį grįžtamąjį ryšį arba pranešti apie problemas šiuo adresu: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Išmokų valdymo žinomos problemos

### <a name="eligibility-processing"></a>Tinkamumo apdorojimas

Paleidus tinkamumą gauti išmokas, kuriam naudojami penktadalis atlyginimo,procentinė atlyginimo dalis ir standartinė draudimo suma, turite nustatyti datą **Išmokų išsami informacija** kaip **Darbuotojo darbo pradžios data**, esančią **Įdarbinimo retrospektyva**. Taip pat turite nurodyti **Išdirbtos valandos**, **Mokėjimo dažnis** ir **Metinių išmokų atlyginimo suma**. Jei darbuotojui priskirta pastovioji atlyginimo dalis, įveskite **Išdirbtos valandos** ir **Mokėjimo dažnis**. Apskaičiuojamas metinio atlyginimo sumos dydis. Jei darbuotojas gauna fiksuotą atlyginimą, jums nereikia įvesti **Išdirbtos valandos**. Rekomenduojame, kad kurdami naujus darbininkus, pirmiausia įvestumėte pastoviąją atlyginimo dalį. Norėdami atnaujinti išmokų išsamios informacijos įrašą, eikite į **Darbininkas > Darbininko retrospektyva > Įdarbinimo išsami informaciją**. Darbininko pradžios datai koreguokite datą.

### <a name="employee-self-service"></a>Darbuotojų savitarna

Darbuotojo suma neapskaičiuojama atnaujinant gyvybės draudimo sumą. Pavyzdžiui, kai darbuotojui siūlomas gyvybės draudimo planas, jis gali pasirinkti iki 50 000 $ draudimo sumos, kai mokama 0,36 $ už draudimo sumos 1 000 $.  Kai darbuotojas atnaujina draudimo sumą, su darbuotoju susijusios išlaidos išlieka lygios nuliui.

Pasirinkdamas išmokų planą, kuriam leidžiama pasirinkti tik vieną to plano tipą, vartotojas gaus klaidos pranešimą, jei mėgins atsisakyti plano jau jį pasirinkęs. Pavyzdžiui, vartotojas pasirenka gydymo planą ir perkelia jį į krepšelį. Tada vartotojas pasirenka **Atsisakyti** kitam gydymo planui. Vartotojas gaus klaidos pranešimą.

## <a name="enable-benefits-management"></a>Išmokų valdymo įjungimas

Išmokų valdymas yra peržiūros funkcija ir ji pasiekiama tik **smėlio dėžės** aplinkose. Šiuose straipsniuose aprašoma, kaip įjungti „Human Resources“ peržiūros funkcijas. Juose taip pat nurodoma, kurios esamos „Human Resources“ funkcijos išmokų valdyme pakeičiamos arba kurios yra išjungiamos, kai įjungiate išmokų valdymą.

- [Funkcijų valdymas](hr-admin-manage-features.md)
- [Peržiūros funkcija: išmokų valdymas](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Išmokų valdymo konfigūravimas

Kad galėtumėte kurti savo darbuotojų išmokų planus, reikia konfigūruoti planų parinktis.

- [Išmokų valdymo parametrų nustatymas](hr-benefits-setup-parameters.md)
- [Tinkamumo taisyklių ir parinkčių konfigūravimas](hr-benefits-setup-eligibility-rules.md)
- [Asmeninių kontaktų tinkamumo parinkčių konfigūravimas](hr-benefits-setup-contact-eligibility-options.md)
- [Draudimo parinkčių kūrimas](hr-benefits-setup-coverage-options.md)
- [Mokėjimo dažnio nustatymas](hr-benefits-setup-payment-frequencies.md)
- [Gyvenimo įvykių tipų konfigūravimas](hr-benefits-setup-life-event-types.md)
- [Planų tipų kūrimas](hr-benefits-setup-plan-types.md)
- [Nustatyti priežasčių kodus](hr-benefits-setup-reason-codes.md)
- [Pakopų kodų nustatymas](hr-benefits-setup-tier-codes.md)
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

- [Išmokų planų sąranka](hr-benefits-plans-setup.md)
- [Darbininko išmokų planų kūrimas](hr-benefits-plans-worker.md)
- [Lanksčiųjų kreditų programų nustatymas](hr-benefits-plans-flex-credit-programs.md)
- [Būsimų gyvenimo įvykių konfigūravimas](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Išmokos planų apdorojimas

Turite apdoroti kai kuriuos keitimus, kad jie būtų aktyvūs.

- [Tinkamumo registracijai apdorojimas](hr-benefits-process-enrollment-eligibility.md)
- [Gyvenimo įvykių apdorojimas](hr-benefits-process-life-events.md)
- [Gyvenimo įvykio keitimų apdorojimas](hr-benefits-process-life-event-changes.md)
- [Gyvenimo įvykio tinkamumo apdorojimas](hr-benefits-process-life-event-eligibility.md)
- [Tarifo pakeitimų apdorojimas](hr-benefits-process-rate-changes.md)

