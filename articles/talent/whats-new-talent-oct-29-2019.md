---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. spalio 29 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529689"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. spalio 29 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2586 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Šalių, kurios neturi vaidmenų, naikinimas turi būti numatytasis (371233)

Kai ruošiate naują aplinką „Talent“, parametras **Naikinti šalis, jei nėra vaidmenų** turi būti įjungtas pagal numatytuosius parametrus. Kai naikinate darbuotoją, su darbuotoju susijusi šalis yra pašalinama, nebent įjungtas šis parametras. Šis keitimas apriboja pasikartojančius įrašus visuotinėje adresų knygelėje, kai reikia importuoti, keisti arba iš naujo importuoti darbuotojus.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Turi būti leidžiama naikinti juodraščius ir atšauktas atostogų užklausas „Common Data Service“ (376999)

Atlikę šį keitimą, galite naikinti užklausas, kurių būsena „Common Data Service“ yra **Juodraštis** arba **Atšaukta** .

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Papildomos sąrašo reikšmės pasirinktiniuose laukuose nėra atspindimos „Common Data Service“ spustelėjus Taikyti pasirinktinių laukų formoje (379599)

Kai įtraukiate naujas sąrašo reikšmes į esamą pasirinktinį lauką, kuris jau sinchronizuotas su „Common Data Service“, jos bus pasiekiamos „Common Data Serivce“, kai keitimus pritaikysite formoje **Pasirinktiniai laukai**

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Taikykite kontrolinius sąrašus tarp juridinių subjektų, kai yra daugiau nei vienas įdarbinimas (371270)

Šiose savaitės leidime galite taikyti kontrolinį sąrašą darbuotojams su daugiau nei vienu įdarbinimu eidami į **Darbuotojo forma > Kontroliniai sąrašai**.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Išmokų atviros registracijos peržiūros funkcija pašalinta

Kartu su mūsų pranešimu, paskelbtu tinklaraščio įraše [Strateginis investavimas į „Core HR“ veiklos efektyvumą](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence), „Microsoft“ pašalino išmokų atviros registracijos funkciją iš viešosios peržiūros. Ateityje bus išleistos naujos funkcijos. Gamybos išmokų atviros registracijos funkcijos naudojimas nepalaikomas.

## <a name="coming-soon"></a>Jau greitai

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Žr. [Veiklos efektyvumo vertinimų spausdinimas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) dirbant su „Dynamics 365“: 2019 leidimo 2 bangos planu.

### <a name="feature-management-workspace"></a>Funkcijos valdymo darbo sritis

Funkcijos įtraukiamos ir atnaujinamos kiekviename leidime. Funkcijų valdymo patirtis suteikia darbo sritį, kurioje galite peržiūrėti kiekviename leidime pristatytų funkcijų sąrašą. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją.

Norėdami daugiau sužinoti apie pakeitimus, pristatytus su funkcijų valdymu, žr. [Funkcijų valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
