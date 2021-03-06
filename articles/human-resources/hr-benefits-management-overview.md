---
title: Išmokų valdymo apžvalga
description: Išmokų valdymo funkcijos programoje „Dynamics 365 Human Resources“ apžvalga. Siūlykite savo darbuotojams išplėstines išmokų parinktis naudodami paprastas naudoti internetines funkcijas.
author: andreabichsel
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1b6ace2ce83c668e83ec1b433f8062148a6dfaf4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059069"
---
# <a name="benefits-management-overview"></a>Išmokų valdymo apžvalga

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Norėdami išlikti konkurencingi, turite pasiūlyti gausų išmokų rinkinį, kad pritrauktumėte ir išlaikytumėte savo geriausius darbuotojus. Be įprastų privalumų, pvz., sveikatos ir dantų priežiūros draudimo, taip pat galite siūlyti išplėstines paslaugas, pvz., įvaikinimo pagalbą, poilsio programas ir išmokas drabužiams. Išmokų valdymas programoje „Microsoft Dynamics 365 Human Resources“ – dinamiškas sprendimas, palaikantis daugybę išmokų parinkčių. „Human Resources“ taip pat apima lengvai naudojamas darbuotojų funkcijas, kuriomis demonstruojami jūsų pasiūlymai.

- Išplėstiniai išmokų planai leidžia kurti ir valdyti unikalius išmokų planus ir palaikymo sudėtinių išmokų tarifų lenteles ir įdėtąsias pakopas. Galite lengvai sukurti išmokų programas, paketus ir automatinės registracijos taisykles, kad palengvintumėte darbuotojo patirtį.

- Lanksčiųjų kreditų programomis galite proporcingai paskirstyti, kad būtų palaikomi išėjimas į pensiją ir kiti gyvenimo įvykiai.

- Dėl platesnių tinkamumo taisyklių galite būti užtikrinti, kad reikiamos išmokos pasieks reikiamus darbuotojus.

- Internetine išmokų registracija suteikiama puiki jūsų darbuotojų patirtis.

- Tinkamo gyvenimo įvykio apdorojimas palaiko būsimus gyvenimo įvykius.

Jei norite gauti prieigą prie demonstracinių duomenų, turite iš naujo įdiegti savo smėlio dėžės aplinką.

>[!NOTE]
>Dabar galite pritaikyti išmokų valdymo formas. Dabar galite pridėti pasirinktinius laukus, susijusius su padengimo **tarifais, į** išmokų planų parinkties formą. Norėdami gauti daugiau informacijos apie darbą su pasirinktinais laukais, žr. [Pasirinktini laukai](hr-developer-custom-fields.md).
>![Išmokų valdymo pasirinktiniai laukai](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Išmokų valdymo įjungimas

Šioje temoje aprašoma, kaip įjungti personalo valdymo funkcijas. Jame taip pat nurodoma, kurios esamos personalo valdymo funkcijos išmokų valdyme pakeičiamos arba kurios yra išjungiamos, kai įjungiate išmokų valdymą.

> [!IMPORTANT]
> Po to, kai **gamybos** aplinkoje įgalinate išmokų valdymą, jo išjungti negalima. Rekomenduojame įjungti ir testuoti išmokų valdymą **smėlio dėžės** aplinkoje prieš įjungiant jį **gamybos** aplinkoje. Yra reikšmingų skirtumų tarp pasenusių išmokų funkcijų ir naujų išmokų valdymo funkcijų – joms reikalingi papildomi nustatymai ir tikrinimai prieš įtraukiant į gamybos procesą.

- [Funkcijų valdymas](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Darbuotojų informacijos konfigūravimas

Kad užregistruotumėte darbuotojus išmokoms gauti, turite pateikti reikiamą informaciją. Turite užregistruoti darbuotoją į **pastoviosios atlyginimo dalies planą** jų darbo pradžios dieną ir pasirinkti **išmokų mokėjimo dažnumą** dalies **Įdarbinimo informacija** formoje **Darbininkas**.

Jei turite darbuotoją, kuris gauna papildomą užmokestį kaip komisinį mokestį, galite įtraukite **Metinio užmokesčio algos** sumą iš darbuotojo įrašo. Žmogiškieji ištekliai naudos **Metinės algos išmokos** sumą nustatydami padengiamas sumas, o ne fiksuotą metinio atlyginimo sumą. **Metinės algos išmokos** turi būti galiojančios nuo darbuotojo pradžios dienos arba nuo išmokos laikotarpio, priklausomai nuo to, kuri data yra vėlesnė. Jei fiksuota alga ir metinės algos užmokesčio suma darbuotojui įrašoma, metinės algos užmokestis bus naudoojamas nustatant padengiamas sumas.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]