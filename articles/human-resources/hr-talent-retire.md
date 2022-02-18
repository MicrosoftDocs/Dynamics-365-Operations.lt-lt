---
title: Išėjimas į pensiją Dynamics 365 Talent - Pritraukti ir integruotos programos
description: Šioje temoje aprašomas išėjimas į pensiją Dynamics 365 Talent - Pritraukti ir integruotos programos.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: df33f35f66e356c3c2a99f0d81ebba1d0f34b5d9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069409"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract ir „Onboard Apps“ išėjimas į pensiją


2019 m. gruodžio mėn. paskelbėme, kad 2022 m. vasario 1 d Dynamics 365 Talent - Pritraukti ir integruotas programas, suteikiant klientams dvejus metus planuoti.

Norėdami gauti daugiau informacijos apie šių programų pašalinimą, žr.
 - [Išeina į pensiją Dynamics 365 Talent - Pritraukti ir Dynamics 365 Talent: Onboard Programėlės](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Sukurti sėkmingesnę darbo jėgą su Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Mes ir toliau palaikysime Dynamics 365 Human Resources, kuri padės mūsų klientams gauti darbo jėgos įžvalgų, reikalingų norint sukurti duomenimis pagrįstą darbuotojų patirtį įvairiose srityse, pvz.:

- Atlyginimo dalis
- Nauda
- Atostogos ir neatvykimai
- Atitiktis
- Payroll
- Atsiliepimas apie našumą
- Mokymas ir sertifikavimas
- Savitarnos programos

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent programų išėjimo į pensiją DUK

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Kokia yra abiejų vartotojų patirtis Dynamics 365 Talent – „Attract“ ir „Onboard“ programas nuo 2022 m. vasario 1 d.?

Vartotojai negalės naudotis programomis ir bus nukreipti į išėjimo į pensiją puslapį.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Ar klientai gali toliau eksportuoti abiejų duomenis Dynamics 365 Talent – Pritraukti ir Onboard programas po 2022 m. vasario 1 d.?
  
Ne, pasitraukimas buvo paskelbtas 2019 m. gruodžio mėn., o reikiami eksporto pajėgumai buvo suteikti iki 2022 m. vasario 1 d. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Ar kliento duomenys, susiję su abiem Dynamics 365 Talent - Pritraukti ir integruotas programas Dataverse bus ištrinti po 2022 m. vasario 1 d.?

Ne,Dataverse subjektai liks kliento nuosavybėje Microsoft Dataverse aplinką net ir išėjus į pensiją, nebent būtų ištrintas arba pašalintas „Human Capital Management Talent“ sprendimas.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Žinau Talent aplinkos pavadinimą. Kaip galiu peržiūrėti „Attract“ ir „Onboard“ duomenis Dataverse?

1.  Prisijungti Power Apps :https://make.powerapps.com
2.  Pasirinkite aplinką, kurioje norėtumėte matyti „Attract“ ir „Onboard“ duomenis.
3.  Eiti į **Dataverse > Lentelės**. 
4.  Įveskite „msdyn_“.**Paieška**. Jei matote lentelių sąrašą, prasidedantį "msdyn_" + lentelių pavadinimais (pavyzdys: msdyn_candidate), vadinasi, radote aplinką su "Attract" ir "Onboard" duomenimis.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Talent aplinkos pavadinimo nežinau. Kaip rasti aplinką, kurioje yra duomenų Dynamics 365 Talent: Attract ir Dynamics 365 Talent: Onboard programos?

1)  Prisijungti Power Platform administravimo centras:https://admin.powerplatform.microsoft.com/
2)  Pasirinkite **Aplinkos**.
3)  Pasirinkite tam tikrą aplinką, kurią norite įvertinti.
4)  Pasirinkite **Ištekliai > „Dynamics 365“ programos**.
5)  Jei matai **HCM talentas** įdiegtas sprendimas, šioje aplinkoje turėtų būti saugomi „Attract“ ir „Onboard“ duomenys. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> The **HCM talentas** tirpalas taip pat naudojamas Dynamics 365 Human Resources.
