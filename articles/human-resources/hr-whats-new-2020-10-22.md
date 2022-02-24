---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources“ 2020 m. spalio 22 d.
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Human Resources“ funkcijos.
author: jcart1106
manager: tfehr
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 513fc3b35f0b6a7f5d9703d2b5eb4109289a189a
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529987"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources“ 2020 m. spalio 22 d.

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos. Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2020 m. 2-os leidimo bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.3680 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Platformos naujinimas 10.0.14 (38) | -- | [Platformos naujinimai, skirti 10.0.14 „Finance and Operations” programų versijai (2020 m. lapkričio mėn.)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| Organizacijos ir personalo valdymo darbo eigos patobulinimai | [Organizacijos ir personalo valdymo darbo eigos patobulinimai](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigūracijos parinktis, skirta sąrašui Man priskirti darbo elementai perkelti](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris| Problema  | Aprašas|
| --- | --- | --- |
| 437922 | Importuojant FMLA valandas naudojant DMF objektą pateikiama tik skaitoma klaida. | Naudojant objektą FMLA valandos nepavyko importuoti valandų, susietų su FMLA atveju. Įtraukėme logiką, siekdami užtikrinti, kad importuotos valandos neviršytų likusių atvejo valandų. |
| 512019 | Netinkama **paskutinio perkeliamo balanso** suma. | Puslapyje **Ne darbo laikas** pakeitus lauką **Nuo datos** į pirmą ataskaitinio laikotarpio dieną rodoma netinkama tipo **Metinės atostogos** **paskutinio perkeliamo balanso** suma. Dabar rodoma tinkama suma. |
| 458639 | Objektas **Darbuotojo kontaktai** nepalaiko keitimų sekimo režimo. | Atnaujinome objektą **Darbuotojo kontaktai**, kad jį galėtumėte naudoti savo duomenų bazės naudojimo (BYOD) scenarijuose.|
| 505347 | Mokymo vadovai galėjo pateikti darbuotojo atostogų užklausą, kai buvo įjungta supaprastinta darbuotojo funkcija. | Visi vaidmenys, išskyrus personalo asistentą ir personalo vadovą, negali pateikti darbuotojų prašymų išleisti iš darbo. |
| 513490 | Išmokų valdymo registravimas: įtraukite planų be padengimo parinkčių registravimą. | Įjungėme **planų be padengimo parinkčių** rezultatų registravimą. Dabar jie rodomi lentelėje **Proceso rezultatai** ir tinkamai rikiuojami, kad būtų rodomi viršuje. |
| 517021 | Negalima pasirinkti kelių planų, kurių **plano tipo** kodas yra tas pats, jei nustatyta viena **plano tipo** registracija vienam tipui. | Pakeitėme planų pasirinkimo apribojimus, kai leidžiama tik viena registracija. Šie apribojimai dabar pateikiami **plano tipo kodo** lygiu, o ne **plano tipo** lygiu. Šis pakeitimas leidžia HSA ir FSA planus, kurių tipai yra vienodi, tačiau galite jiems suteikti atskirą **plano tipo kodą**. Tokiu būdu galite pasirinkti abu to paties registracijos laikotarpio planus. |
| 444791 | Negalima peržiūrėti kompensacijos darbuotojų savitarnos paslaugoje, kai kompensacijos plane įjungta **Apriboti prieigą**. | Darbuotojo savitarnos paslaugos kortelėje **Kompensacija** dabartinės kompensacijos suma ir padidėjimo procentas rodomas kaip „0”, jei darbuotojas buvo užregistruotas plane, kuriame įjungta parinktis **Apriboti prieigą**, ir priskirtas konkretiems vaidmenims. Mes išsprendėme šią problemą, kad darbuotojas ir vadovas visada galėtų peržiūrėti jų ir jų tiesioginių pavaldinių kompensacijų informaciją. |
| 457542 | Atnaujinus kurso informaciją po to, kai kursas uždarytas, ta pati informacija neatnaujinama kursą atlikusiam darbuotojui. | Darbuotojo informacija dabar atnaujinama tinkamai, kai keičiate kurso informaciją po to, kai kursas uždarytas ir atidarytas iš naujo. |
| 515342 | Negalima įterpti duomenų naudojant **CDSLeaveRequestDetailEntity**. Įmonė nerandama arba jos nėra. | Dabar galite naudoti **CDSLeaveRequestDetailEntity**, norėdami įterpti duomenis. |
| 514743 | Klaida **El. pašto parametro** formoje naudojant „Microsoft Exchange“. | Pranešimas „Nepavyko įkelti failų arba rinkinio...” rodomas puslapyje **El. pašto parametrai**, kai el. pašto teikėjas nustatytas į **„Exchange”**. Ši pataisa taip pat leidžia įkelti ir įrašyti puslapį **El. pašto parametrai** kaip tikėtasi. |


## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| „Human Resources“ programa, esanti „Microsoft Teams” | [Darbuotojo atostogos ir neatvykimai „Microsoft Teams”](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [„Human Resources“ programa „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md) |
| Patobulintos darbo eigos užklausos ir patvirtinimai | [Organizacijos ir personalo valdymo darbo eigos patobulinimai](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigūracijos parinktis, skirta sąrašui Man priskirti darbo elementai perkelti](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtualūs objektai, esantys „Common Data Service”, skirtoje „Human Resources“ | [„Dynamics 365 Human Resources” pagrindinių duomenų išplėtimas „Common Data Service”](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [„Common Data Service“ virtualių objektų konfigūravimas](hr-admin-integration-common-data-service-virtual-entities.md) |
| Integravimas su „LinkedIn Talent Hub“ | [Integravimas su „LinkedIn Talent Hub“](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integravimas su „LinkedIn Talent Hub“](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Pasirinktiniai saitai vadovų savitarnoje | [Pasirinktiniai saitai vadovų savitarnoje](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Pasirinktiniai saitai vadovų savitarnoje](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>Jau greitai

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2020 m. 2-os leidimo bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2020 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)
