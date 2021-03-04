---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. gruodžio 10 d.)
description: Šiame straipsnyje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528176"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. gruodžio 10 d.)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2660 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="feature-management-workspace"></a>Funkcijos valdymo darbo sritis

Darbo srityje **Funkcijų valdymas** pateikiamas priemonių, pristatytų kiekviename leidime, sąrašas. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją. Daugiau informacijos apie funkcijų valdymą žr. [Funkcijos valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Visos naujos funkcijos išlieka peržiūroje bent 30 dienų ir paprastai 30–60 dienų. Pagrindinės funkcijos paprastai pasiekiamos kiekvienų metų spalį ir balandį po peržiūros laikotarpio. Kai tik pradedame naujas galimybes darbo srityje **Funkcijų valdymas**, galite jas įjungti. Kai kurios funkcijos gali būti pagal numatytuosius parametrus.
 
Kartais integrali funkcija bus įjungta pagal numatytuosius nustatymus ir jos nebus galima išjungti (pavyzdžiui, darbo sritis **Funkcijų valdymas**).
 
Kai funkcija jau pasiekiama, ją galima įjungti arba išjungti gamybos aplinkose. Darbo sritis **Funkcijų valdymas** nurodo, kada peržiūros funkcija taps privaloma. Paprastai ši data yra spalio 1 d. arba balandžio 1 d., siekiant suderinti su pusmečio leidimų planais. Negalite išjungti privalomų funkcijų. Kol ji taps privaloma, šią funkciją galite įjungti ir išjungti visose aplinkose.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Supaprastinta darbininko forma perkelta į funkcijų valdymo darbo sritį (390583)

Atlikus šį pakeitimą, supaprastintą darbininko formą dabar galima įgalinti darbo srityje **Funkcijų valdymas**. Ši funkcija buvo perkelta iš formos **Sistemos parametrai** srityje **Sistemos administravimas**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Neleisti, kad HcmWorkerPayrollInfo įrašai būtų rašomi nenurodant darbininko vertės (394526)

Šiame leidime **HcmWorkerPayrollInfo** įrašai nebekuriami be darbininkų nuorodų šio scenarijaus atveju. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Pranešimų žurnalas, susietas su veiksmu, nepildomas, kai veiksmo nepavyksta atlikti (374007)

Šiame leidime pateikiamas pakeitimas, po kurio veiksmų pranešimų žurnalas pildomas, kai veiksmo nepavyksta atlikti tam tikrų scenarijų atvejais. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>„Common Data Service“ integravimo paketinės užduoties kūrimas (388030)

Atlikus šį pakeitimą, „Common Data Service“ integravimo paketinės užduotys sukuriamos įgalinus paslaugą.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Papildomos paėmimo sąrašo reikšmės pasirinktiniuose laukuose nėra atspindimos „Common Data Service“ spustelėjus taikyti pasirinktinių laukų formoje (379599)

Atlikus šį pakeitimą, sprendime „Talent“ įvestos naujos paėmimo sąrašo reikšmės dabar sinchronizuojamos su „Common Data Service“, kai pritaikote keitimus.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>„Common Data Service“ naujinimas atvejams, kai banko išėjimo operacijos objektas virsta įterpimu sprendime „Talent“ (352938)

Šiuo pakeitimu išsprendžiama problema, kai atnaujinant banko išėjimo operacijos objektą, sukuriamas naujas „Talent“ įrašas.

## <a name="in-preview"></a>Peržiūros režimu

Peržiūros funkcijos pasiekiamos tik aplinkose **Smėlio dėžė**.

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Žr. [Veiklos efektyvumo vertinimų spausdinimas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) dirbant su „Dynamics 365“: 2019 leidimo 2 bangos planu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]