---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. liepos 23 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Human Resources“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd71ab5c48be1bec5ce2272bbff37ab10a4aed67
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614415"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. liepos 23 d.)

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3416 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Finansinių dimensijų pašalinimas padėtyje neveikiat kaip tikėtasi (445476)

Dimensijų pašalinimas iš padėties dabar pašalina tas pačias padėtis ir iš „Common Data Service“.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Padėtys nehierarchinėje tvarkoje rodo neaktyvias padėtis (397257)

Neaktyvios padėtys (turi galiojimo laiko pabaigą), daugiau nerodo padėties hierarchijos kaip **Padėtys nehierarchijoje**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Patvirtinimas atsitinkantis tarp „LeaveEnrollmentEntity“ ir „HcmWorkerEntity“ duomenų valdymo darbotvarkės (DMF) importavime sulėtina duomenų atsiuntimus (442324)

Pakeitimai šiame leidime pagerina **„LeaveEnrollmentEntity“** veikimą.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Nepavyskta personalizuoti organizacijos administravime (447490)

Su šiuo pakeitimu, galite dabar personalizuoti nuorodas **Organizacijos administravime**.

## <a name="in-preview"></a>Peržiūros režimu

## <a name="mandatory-fields"></a>Privalomi laukai 

Dabar galite padaryti laukus privalomais naudodami Žmogiškųjų išteklių personalizavimo galimybes. Šiai funkcijai reikia **Įrašyti rodiniai**.

## <a name="human-resources-application-in-teams"></a>„Human Resources“ programa programoje „Teams“

Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“. Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą. Daugiau informacijos žr. [„Human Resources“ programa programoje „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Duomenų valdymo sistemos (DMF) objektai, skirti išmokų valdymui
 
Išmokų valdymo objektai ir išleidimas. DMF objektai leidžia paprastai importuoti ir eksportuoti duomenis, kad lengviau konfigūruotumėte išmokų valdymą. Išmokų valdymo šablonas taps prieinamu duomenų perkėlimui. Šablonas nuosekliai eksportuoja ir importuoja duomenis išsaugodamas duomenų priklausomumą.

## <a name="buy-and-sell-leave"></a>Atostogų pirkimas ir pardavimas 

Kai kurios organizacijos suteikia išmoką, kuri leidžia darbuotojams pirkti ar parduoti savo atostogas. Šis procesas dažnai valdomas neautomatiniu būdu. Ši funkcija automatizuoja žmogiškųjų išteklių departamento valdymo strategijas ir užklausas. Ji supaprastina atostogų valdymo procesą ir padeda pašalinti klaidas. Daugiau informacijos ieškokite:

- [Atostogų pirkimo ir pardavimo strategijų valdymas](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atostogų pirkimas ir pardavimas](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Atostogų kaupimas vienai įmonei arba vienam planui

Klientai gali apdoroti vienoje įmonėje sukauptas atostogas, vienkartines atostogas ir neatvykimų planą. Ši galimybė suteikia aiškumo padidėjimo procesui klientams su skirtingais atostogų metais ar atostogų kaupimo politikomis. Norėdami sužinoti daugiau, skaitykite [Sukauptos atostogos įmonėje ar atostogų planas](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

## <a name="add-attachments-to-time-off-requests"></a>Įtraukite priedus į laiko prašymus

Galimybė pridėti priedus prie patvirtintų atostogų prašymų yra itin svarbi dabartinėje COVID-19 situacijoje. Dabar darbuotojai gali pridėti šiuos priedus. Jie taip pat turi daugiau įžvalgų apie atostogų prašymų naujinimų kūrimą. Norėdami sužinoti daugiau, skaitykite [Priedo prie esamo prašymo pridėjimas](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Priežasties kodo pridėjimas į kaupimo sustabdymus 

Į kaupimo sustabdymus įtraukti priežasties kodai.

## <a name="carry-forward-rules"></a>Perkėlimo taisyklės 

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Atostogų kaupimo sustabdymas konkretiems atostogų tipams

Galite sukurti taisyklę sustabdyti darbuotojų, įvedusių neapmokamų atostogų prašymus, atostogų kaupimą. Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma. Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF objektas pasiekiamas kaupimo sustabdymams 

DMF objektas dabar pasiekiamas kaupimo sustabdymams.

## <a name="coming-soon"></a>Jau greitai

## <a name="checklist-entities-included-in-common-data-service"></a>Kontrolinio sąrašo objektai, nurodyti „Common Data Service”

Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Common Data Service“.

## <a name="platform-changes"></a>Platformų pakeitimai

Platformos atnaujinimas 10.0.12 (36)

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)
