---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2020 m. sausio 21 d.)
description: Šiame straipsnyje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c0c303ec5d009fce0c975eb797f018b5e27a41eb
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982412"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2020 m. sausio 21 d.)

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“. Į „Attract” įtraukėme funkciją, papildančią neseniai skelbtą mūsų pranešimą [Sėkmingesnės darbo jėgos kūrimas naudojantis „Dynamics 365 Human Resources”](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Aplinkos duomenų atsisiuntimas

Administratoriai gali atsiųsti savo aplinkos duomenis. Duomenys su visomis užduotimis ir kandidatais eksportuojami standartiniu JSON formatu, o konfigūracija eksportuojama į „zip” faile. Norėdami gauti daugiau informacijos, žr. [Duomenų eksportavimas iš „Attract” ir „Onboard”](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Prieigos prie aplinkų apribojimas vartotojams, kurie nėra administratoriai

Administratoriai dabar gali riboti vartotojų, kurie nėra administratoriai, prieigą prie aplinkos. Šio veiksmo anuliuoti negalima. Daugiau informacijos žr. [Prieigos prie „Attract” apribojimas](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

### <a name="exporting-onboarding-guides"></a>Supažindinimo vadovų eksportavimas

Dabar vartotojai gali eksportuoti visus savo supažindinimo vadovus ir supažindinimo šablonus „Word” dokumento formatu. Norėdami gauti daugiau informacijos, žr. [Duomenų eksportavimas iš „Attract” ir „Onboard”](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2726 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Naujausias metinės kompensacijos laukas „Verify” įdarbinimo formoje nėra nuoseklus (392092)

Šiame leidime atliktas keitimas, po kurio formoje **Tinkamumas dirbti** bus nuosekliai rodoma naujausia valiuta, nustatyta pagal įmonių išrinkiklį.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Laukas „Žinomas kaip”, įtrauktas į atsiliepimo gavėjo peržvalgą (407789)

Teikiant atsiliepimus apie našumą, darbininkų peržvalga nepateikdavo pakankamai informacijos, kad būtų galima nustatyti, ar atsiliepimus gauna tas asmuo, kuriam jie skirti. Pridėjome stulpelį **Žinomas kaip**, kad būtų galima identifikuoti unikalų darbuotojo vardą.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>HcmWorkerPayrollInfo įrašas kuriamas nesusiejant jo su darbininku (394526)

Šiame leidime atliktas keitimas, po kurio HCMWorkerPayrollInfo įraišai nebus rašomi nepateikus rekomendacijos apie darbuotoją.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Galimybė redaguoti padalinį naršant pareigų hierarchijos skiltį (341001)

Nustačius saugos parametrus taip, kad būtų draudžiama redaguoti padalinius, redagavimo funkcija pereinant į formą **Padaliniai** išjungiama visais atvejais.

## <a name="coming-soon"></a>Jau greitai

Nauju „Common Data Service” sprendimu greitai galėsite naudotis atlikdami šiuos keitimus:

| Aprašymas | Keitimas |
| --- | --- |
| Objekto **Užduotis / pareigos** keitimai | <ul><li>Pridėta **Kompensacijos sritis**</li><li>Pridėta **Finansinės dimensijos**</li></ul> |
| Objekto **Darbininkas** keitimai | <ul><li>Pridėta **Pavadinimų seka**</li><li>Pridėta **Dirba iš namų**</li><li>Pridėta **Kalba**</li><li>Pridėta **Paaukštinimo data**</li><li>Pridėta **Jubiliejaus data**</li><li>Pridėta **Pradinio įdarbinimo data**</li></ul> |
| Objekto **Įdarbinimas** keitimai | <ul><li>Pridėta **Finansinės dimensijos**</li><li>Pridėta **Atleidimo priežastis**</li><li>**Perėjimo data** pervardyta į **Atleidimo data**</li><li>Pridėta **Bandomojo laikotarpio data**</li></ul> |
| Objekto **Darbininko adresas** keitimai | <ul><li>Pridėta **Gatvė**</li><li>**1 adreso eilutė**, **2 adreso eilutė**ir **3 adreso eilutė** pažymėtos kaip nebenaudojamos</li></ul> |
| Nauji kintamosios atlyginimo dalies sąrankos objektai | <ul><li>**Kompensacijų kitimo plano tipas**</li><li>**Kompensacijų kitimo planas**</li><li>**Kintamosios atlyginimo dalies paskirstymo taisyklės**</li><li>**Kompensacijų kitimo plano lygis**</li></ul> |
| Naujas objektas **Darbininko įdarbinimo kalendorius** | <ul><li>Pridėta **Darbo kalendoriaus objektas**</li></ul> |
