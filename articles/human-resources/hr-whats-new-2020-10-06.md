---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. spalio 6 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. spalio 6 d.
author: jcart1106
manager: tfehr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 330b037e2ba50ed090fd41b0990d6cf37d9d8b01
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463555"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. spalio 6 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos. Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2020 m. 2-os leidimo bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.3636 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinama toliau pateikta funkcija.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Papildomos įžvalgos apie atostogų kalendorius | [Papildomų įžvalgų apie atostogų kalendorių rodinius teikimas](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Komandos ir įmonės kalendorių peržiūra](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

>[!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Gali būti šios temos naujinimų siekiant įtraukti klaidų ištaisymus, įtrauktus į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema | Aprašas |
| --- | --- | --- |
| 448806 | **Numatytasis identifikavimo tipas** eksportuojamas kaip **RecID** HCM parametruose | Šis „Human Resources” parametrų objekto pakeitimas įtraukia papildomą stulpelį, kuriame rodomas **Numatytasis identifikavimo tipas**. |
| 492923 | Užduočių įrašai neįrašomi „Lifecycle Services” (LCS) | Užduočių įrašus dabar galima įrašyti LCS. |
| 429950 | Pastoviosios atlyginimo dalies galiojimas neteisingai pasibaigia keičiant pareigas | Keičiant darbuotojo pareigas puslapyje **Darbuotojo perkėlimas**, kompensacijos pabaigos data nustatyta į viena diena ankstesnę datą nei pareigų pabaigos data. Kompensacijos pabaigos data dabar tokia pati, kaip pareigų pabaigos data. |
| 467214 | **Fiksuoto atlyginimo analizė** rodoma tik tada, jei **Užmokesčio tarifo konvertavimo pavadinimas** nustatytas į **Metinis** | Kompensacijos analizėje nerodomi fiksuoto užmokesčio tarifai, kurių pavadinimai nėra **Metinis**. Šiame naujinime kompensacijos analizė dabar naudoja visus užmokesčio tarifo konvertavimus. Vykdant ataskaitas pagal **valandas** arba **atlyginimą**, bet koks užmokesčio tarifo konvertavimas, naudojantis kitą laikotarpį nei valandinį, įtraukiamas į filtrą **Atlyginimas**. Į filtrą **Valandinis** įtraukiami tik tie užmokesčio tarifai, kurių laikotarpis yra **Valandinis**. |
| 482464 | Peržiūrint **atsiliepimus**, rodinys **Išsami informacija** nepasikeičia į tinklelio rodinį pritaikius filtrą | Pritaikius filtrą, atsiliepimų tinklelis rodomas kaip numatyta. |
| 483184 | „Human Resources” negeneruoja atostogų kaupimų, kai įraše **Atostogų registracija** pasirenkate lauko **Patikslinta darbo pradžios data** parinktį **Pakopų pagrindas** |Laukas **Patikslinta darbo pradžios data** užpildomas ir naudojamas generuojant atostogų kaupimus.  |
| 509731 | Darbuotojo, kuris bus atleistas, prašymas išleisti iš darbo sukelia problemų, jei prašoma išleisti iš darbo po atleidimo datos | Darbuotojai, kurių atleidimo data ateityje, gali pateikti prašymus išleisti iš darbo, jei prašymai pateikiami anksčiau nei atleidimo data. |
| 510716 | Kompensacijos analizės dalyje **Vyrų vidutinis valandinis atlygis** rodomi ir darbuotojai vyrai, ir moterys | Kompensacijos analizės srities **Kompensacijos demografinė analizė** dalyje **Vyrų vidutinis valandinis atlygis** buvo rodomas ir moterų vidutinis atlyginimas. Dabar joje rodomi tik vyrai. |
| 511348 | Išmokų savitarnos paslauga turėtų rodyti tik išmokų planus, galiojančius nuo šiandienos iki išmokų laikotarpio pabaigos | Puslapyje **Išmokų registravimas** darbuotojams buvo rodomi nebegaliojantys išmokų planai. Ši pataisa pašalina šiuos planus. |
| 512706 | Nustatykite toliau pateiktus laukus į tik skaitomus.<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Po veiksmo atlikimo dimensijos informacijos mygtukai **Įtraukti** ir **Šalinti** buvo netinkamai įjungti. Šis puslapio **Pareigų veiksmų informacija** naujinimas paverčia laukus neredaguojamais atlikus veiksmą. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| „Human Resources“ programa, esanti „Microsoft Teams” | [Darbuotojo atostogos ir neatvykimai „Microsoft Teams”](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [„Human Resources“ programa „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Atostogų prašymų valdymas „Teams“](hr-teams-leave-app.md) |
| Patobulintos darbo eigos užklausos ir patvirtinimai | [Organizacijos ir personalo valdymo darbo eigos patobulinimai](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigūracijos parinktis, skirta sąrašui Man priskirti darbo elementai perkelti](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtualūs objektai, esantys „Dataverse”, skirtoje „Human Resources“ | [„Dynamics 365 Human Resources” pagrindinių duomenų išplėtimas „Dataverse”](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [„Dataverse“ virtualių objektų konfigūravimas](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Jau greitai

Toliau pateiktos naujos funkcijos bus įtrauktos į būsimus leidimus.

- **Kontrolinių sąrašų objektai, įtraukti į „Dataverse”**: kontrolinių sąrašų objektai, skirti supažindinimo, atleidimo, perkėlimo ir verslo procesams, greitai taps prieinami „Dataverse”.

- **Išmokų valdymo priežasčių kodai**: išmokų valdymo priežasčių kodai netrukus bus sujungti su esamais „Human Resources” priežasčių kodais. Jei išmokų valdyme sukūrėte priežasčių kodų, kurie sudaryti iš daugiau nei 15 simbolių, turite pakeisti priežasties kodo pavadinimą išmokų valdymo formoje **Priežasčių kodai**, kad jį sudarytų 15 ar mažiau simbolių. Atnaujinus pavadinimą, priežasties kodas atsiras esamoje priežasties kodo formoje personalo valdyme. Šis pakeitimas bus prieinamas ateityje ir neturės įtakos jau esamoms funkcijoms.

- **Pasirinktiniai vadovų savitarnos saitai**: norėdami palaikyti vadovus, mes plečiame vadovų savitarnos galimybes. Įtraukėme galimybę įtraukti pasirinktinius saitus skirtuke **Mano komanda**. Ši funkcija panaši į pasirinktinių darbuotojų savitarnos saitų funkciją, esančią skirtuke **Mano informacija**. Dėl išsamesnės informacijos, žr. [Tinkintos nuorodos vadovo savitarnos paslaugose](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2019 m. 2-os leidimo bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Papildomi ištekliai

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2020 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]