---
title: Peržiūra
description: Programos Dynamics 365 Human Resources darbo sritis Atostogos ir neatvykimai suteikia lanksčią sistemą, skirtą naujiems atostogų planams ir užklausų tvarkymo darbo eigoms kurti, taip pat intuityvų savitarnos puslapį, skirtą darbuotojų atostogų užklausoms teikti.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428972"
---
# <a name="overview"></a>Peržiūra

„Dynamics 365 Human Resources“ padeda jums suteikti puikias atostogų išmokas savo darbuotojams. Darbo sritis **Atostogos ir neatvykimai** suteikia lanksčią sistemą, skirtą naujiems atostogų planams bei užklausų tvarkymo darbo eigoms kurti, taip pat intuityvų savitarnos puslapį, skirtą darbuotojų atostogų užklausoms teikti. Analizė padeda organizacijai matuoti ir stebėti atostogų balansus ir atostogų planų naudojimą.

## <a name="set-up-leave-and-absence"></a>Atostogų ir neatvykimų nustatymas

Norėdami kurti atostogų planus savo darbuotojams, turite atlikti keletą sąrankos veiksmų:

- [Atostogų ir neatvykimų parametrų konfigūravimas](hr-leave-and-absence-parameters.md)
- [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md)
- [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Sukurti ir valdyti atostogų planus

Prieš kurdami savo darbuotojų atostogų planus, turite sukurti atostogų ir neatvykimo tipus. Sukūrę atostogų planą, galite užregistruoti darbuotojus šiam planui gauti. Taip pat galite vykdyti kaupimo procesą, kurti įspėjimus ir peržiūrėti savo planų analizę.

- [Atostogų ir neatvykimų tipai konfigūravimas](hr-leave-and-absence-types.md)
- [Atostogų ir neatvykimų plano kūrimas](hr-leave-and-absence-plans.md)
- [Darbininkų priskyrimas atostogų planui](hr-leave-and-absence-enroll.md)
- [Atostogų ir neatvykimų kaupimo planai](hr-leave-and-absence-accrue.md)
- [Peržiūrėti atostogų ir neatvykimų analizę](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Atostogų užklausos ir užklausų valdymas

Jūsų darbuotojai gali pateikti atostogų užklausas, o jūs galite jas tvarkyti darbo srityje **Darbuotojo savitarna**.

- [Prašyti išleisti iš darbo](hr-employee-self-service-request-time-off.md)
- [Atostogų ir leidimo neatvykti prašymų valdymas](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Žinomos atostogų ir neatvykimų problemos

### <a name="rounding-precision"></a>Apvalinimo tikslumas

Negalite nustatyti **apvalinimo tikslumo**, kai nustatote **apvalinimo tipą**. **Apvalinimo tikslumą** galite nustatyti tik naudodami objektą **Atostogų ir neatvykimo tipai**. 

1. Dalyje **Atostogų ir neatvykimų tipai** pasirinkite **Atidaryti naudojant „Excel“**, kad atidarytumėte objektą **Atostogų ir neatvykimų tipai**.

2. Atidarę ir įjungę failą, pasirinkite **Dizainas**.

3. Lentelėje **Atostogų ir neatvykimo tipai** pasirinkite pieštuko parinktį, kad galėtumėte redaguoti.

4. Pasirinkite **Apvalinimo tikslumas** ir **Apvalinimo tipas**, tada pasirinkite **Įtraukti**, kad įtrauktumėte į laukų sąrašą.

5. Pasirinkite **Naujinti**, tada – **Atlikta**.

6. Įveskite arba pasirinkite kiekvieno atostogų tipo **apvalinimo tipą**, jei nėra jau nustatyta. 

7. Įveskite atitinkamų tipų **apvalinimo tikslumą**.

8. Pasirinkite **Publikuoti**, kad keitimai būtų taikomi „Human Resources”.

## <a name="leave-and-absence-preview-features"></a>Atostogų ir neatvykimų peržiūros funkcijos

Naujas atostogų ir neatvykimų funkcijas galite išbandyti aplinkoje **Smėlio dėžė**. Daugiau informacijos apie peržiūros funkcijas, žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md). 

[!include [banner](includes/preview-feature.md)]

Peržiūros funkcijos apima:

- **Įmonės arba plano atostogų kaupimas**– galite vykdyti kaupimo procesą visoms įmonėms arba vienai įmonei. Taip pat galite vykdyti konkrečios įmonės konkrečių atostogų plano kaupimo procesą. 

- **Atostogų pirkimas** – galite įgalinti ir kurti atostogų pirkimo strategijas, skirtas darbuotojams, kad jie pateiktų pirkimo reikalavimus. Darbuotojai gali pateikti pirkimo užklausas ir automatiškai atnaujintus likučius, kad galėtų atsižvelgti į užklausą.  

- **Įtraukti priedų į patvirtintas atostogų užklausas** – galite įtraukti priedą į jau patvirtintą atostogų prašymą. 

