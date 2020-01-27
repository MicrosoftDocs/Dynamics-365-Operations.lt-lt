---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. spalio 8 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 06758ff5eb1c00ae299b1b8849fcabb0cd9593e8
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896640"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. spalio 8 d.)

Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2542 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Iš viešosios peržiūros pašalinta išmokų atvira registracija

Kartu su mūsų pranešimu, paskelbtu tinklaraščio įraše [Strateginis investavimas į „Core HR“ veiklos efektyvumą](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/), „Microsoft“ pašalino išmokų atviros registracijos funkciją iš viešosios peržiūros 2019 m. spalio 18 d. Vietoj jos ateityje bus išleistos naujos funkcijos. Išmokų atviros registracijos funkcijos, kuri šiuo metu yra viešojoje peržiūroje, nebus galima naudoti gamybos aplinkoje. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Remiantis naujomis nuostatomis, esant numatytiesiems parametrams „Common Data Service“ integravimas dabar išjungtas (343675)
 
Sukonfigūravus naujas aplinkas, „Common Data Service“ integravimas dabar yra išjungtas. Daugiau informacijos žr. [„Common Data Service“ integravimo konfigūravimas](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Supaprastintas darbuotojo įrašo sukūrimas ir naršymas

Darbuotojo įrašo ir naršymo funkcijas dabar galima naudoti visose aplinkose. Norėdami įjungti šią funkciją, eikite į **Sistemos administravimas \> Saitai \> Sąranka \> Sistemos parametrai \> Peržiūros funkcijos** ir pasirinkite **Patobulintoji darbuotojo forma ir naršymas**. Funkcija įjungta visiems vartotojams. Šią parinktį galite bet kuriuo metu išjungti.

Daugiau informacijos žr. [Supaprastintas darbuotojo įrašo sukūrimas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) dirbant su „Dynamics 365“: 2019 leidimo 2 bangos planu.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>„Attract“ ir „Oboard“ kuria neaktyvius darbuotojus „Core HR“ (380517)

Šios savaitės leidimas ištaiso problemą, kai „Attract“ ir „Onboard“ kuria neaktyvius darbuotojus „Core HR“.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Darbo eiga nutrūksta, kai vadovas yra prisijungęs prie kitos įmonės atleidžiant darbuotoją (346852)

Darbo eiga nenutrūks atsižvelgiant į juridinį subjektą, prie kurio prisijungęs vadovas.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>HcmOnboardingWorkerChecklistTaskEntity trūksta informacijos (349591)

Šiame leidime yra papildomos informacijos apie **HcmOnboardingWorkerChecklistTaskEntity**. Štai keletas pavyzdžių:

- **Grupės pavadinimas**, kai priskirtas tipas yra **grupė**
- **Darbuotojo vardas**, kai priskirtas tipas yra **darbuotojas**
- **Vadovo vardas**, kai priskirtas tipas yra **vadovas**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>„Common Data Service“ administravimo puslapyje objektai nėra išvardyti abėcėlės tvarka (377414)

Dabar puslapyje **CDS administravimas** objektai yra įvardyti abėcėlės tvarka.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Keičiant įdarbinimo tipą ir būsimą datą, neleidžiama priskirti pareigų (339958)

Šis pakeitimas leidžia paskirti pareigas, kai pasikeičia darbuotojų tipai (pvz., iš darbuotojo į rangovą).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Atnaujinant „Common Data Service“ banko išėjimo operacijos objektą, sukuriamas naujas „Talent“ įrašas (352938)

Atnaujinant „Common Data Service“banko išėjimo operaciją, dabar išėjimo operacija yra atnaujinama.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Atsiliepimo elementų priedų antraštėje rodomas atsiliepimo aprašymas (343765)

Atsiliepimo aprašymas neberodomas priedo antraštėje.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Kompensacijos darbo eigos komentarų lauke rodomas neteisingas turinys (339297)

Atlikus šį pakeitimą, rodomas lauko **%HcmActionState.HcmWorkerActionComment.Comments%** turinys.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity ir WorkCalendarDayEntity nėra pasiekiami per „OData“ (376329)

Šiame leidime **WorkCalendarEntity** ir **WorkCalendarDayEntity** yra pasiekiami per „Open Data Protocol“ („OData“).

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity veikia lėtai, kai naudojamas „OData“ (375221)

Atlikus pakeitimus, pagerintas **HCMWorkerEntity** efektyvumas, kai naudojamas „Microsoft Excel“ darbaknygės dizaino įrankis.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Pašalinus našumo žurnalą ir sukūrus naują, vadovo našumo žurnalo įraše rodoma klaida (336061)

Šiame leidime ištaisyta problema, kuri atsiranda po to, kai vienas našumo žurnalas pašalinamas ir iš karto po to sukuriamas naujas. Ši pataisa keičia vadovo savitarnos paslaugos veikimą.

## <a name="coming-soon"></a>Jau greitai

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Žr. [Veiklos efektyvumo vertinimų spausdinimas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) dirbant su „Dynamics 365“: 2019 leidimo 2 bangos planu.
