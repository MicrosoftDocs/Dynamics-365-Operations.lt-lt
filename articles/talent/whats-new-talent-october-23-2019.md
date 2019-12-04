---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. spalio 23 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 66419d9093cff68aa6109b22ab57bcb46ac6c718
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772901"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. spalio 23 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai
Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai
Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2569 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>„Finance and Operations“ programų platformos 30 naujinimas

Daugiau informacijos žr. [žr. Kas nauja arba pakeista „Finance and Operations“ programų platformos 30 naujinime (2019 m. lapkritis)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Šalinama išmokų atviros registracijos peržiūros funkcija

Kartu su mūsų pranešimu, paskelbtu tinklaraščio įraše [Strateginis investavimas į „Core HR“ veiklos efektyvumą](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence), „Microsoft“ pašalino išmokų atviros registracijos funkciją iš viešosios peržiūros 2019 m. spalio 18 d. Vietoj jos ateityje bus išleistos naujos funkcijos. Išmokų atviros registracijos funkcijos, kuri šiuo metu yra viešojoje peržiūroje, nebus galima naudoti gamybos aplinkoje.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Klaida antrą kartą pasirenkant šalį / regioną darbuotojo formoje (350294)

Šios savaitės leidime buvo išspręsta problema pasirenkant šalį / regioną formoje **Darbuotojas**.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Kaip numatytosios finansinių dimensijų vertės naudojamos jungtinio rodinio lauko reikšmės, kai neleidžiama įrašyti rankiniu būdu (340097)

Esant šiam pakeitimui, nustatant finansines dimensijas ir naudojant parinktį, kuri neleidžia įvesti rankiniu būdu, sistema tinkamai nustatys dimensijos vertę lauke **Jungtinis rodinys**.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Nauji ryšių tipai turi būti pridėti prie ryšio peržvalgos asmeninių kontaktų formoje (347691)

Šiame leidime yra naujų galimybių pridėti naujus ryšių tipus lentelėje **Ryšių tipai** ir atsižvelgti į šiuos keitimus asmeninių kontaktų ryšio peržvalgoje.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Papildomos sąrašo reikšmės, esančios pasirinktiniuose laukuose, neatsispindi „Common Data Service“ (379599)

Šios savaitės leidime, įtraukus naują sąrašo reikšmę į esamą pasirinktinį lauką, kuris jau sinchronizuotas su „Common Data Service“, naujos išrinkimo sąrašo reikšmės dabar bus rodomos objektui pritaikius keitimus.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>Įdarbinimo sąlygų puslapyje pasirinkus „Atidaryti naudojant „Excel“, rodomos visų darbuotojų įdarbinimo sąlygos (348073)

Dirbant su šiuo leidimu, programoje „Excel“ atsidarys tik pasirinkto darbuotojo įdarbinimo sąlygos. Visa įmonės apsauga taip pat įvertinta.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>„Common Data Service“ trūksta sąsajos tarp darbo kalendoriaus poilsio dienų objekto ir darbo kalendoriaus objekto (324178)

Šiame leidime šis ryšys buvo įtrauktas. Atlikus pakeitimą, darbuotojo darbo dienos galės būti rodomos „PowerApps“. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Klaida darbuotojų savitarnos darbo eigas naudojant su konfigūruojamomis hierarchijomis (370132)

Šiame leidime pateikiami geresni pranešimai, kaip konfigūruoti darbo eigas naudojant konfigūruojamas hierarchijas. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Sistema leidžia kurti naujas pareigas, kuriose galima priskyrimo data yra ankstesnė už aktyvinimo datą (340103)

Esant šiam pakeitimui, kai data **Galima priskirti** yra ankstesnė už datą **Aktyvinimas**, bus rodomas įspėjimas.

## <a name="coming-soon"></a>Jau greitai

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Žr. [Veiklos efektyvumo vertinimų spausdinimas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) dirbant su „Dynamics 365“: 2019 leidimo 2 bangos planu.

### <a name="feature-management-workspace"></a>Funkcijos valdymo darbo sritis

Funkcijos įtraukiamos ir atnaujinamos kiekviename leidime. Funkcijų valdymo patirtis suteikia darbo sritį, kurioje galite peržiūrėti kiekviename leidime pristatytų funkcijų sąrašą. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją.

Norėdami daugiau sužinoti apie pakeitimus, pristatytus su funkcijų valdymu, žr. [Funkcijų valdymo apžvalga](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
