---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. birželio mėn. 25 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Human Resources“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa02cf10b2b4fe08440d3641472e83dfe58169c9
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614391"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. birželio mėn. 23 d.)

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Human Resources“ funkcijos. Pakeitimai taikomi 8.1.3347 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Kai baigiasi atleisto darbuotojo registracijos galiojimo laikas, atostogų tipas, likutis ir suma yra pašalinami iš Atostogų registracijos formos (444867)

**Atostogų tipas**, **Likutis** ir **Suma** laukai dabar yra palaikomi vietoje išvalytų atliekant šį žymėjimą.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Neteisingas prognozuojamas likutis, kai nauja funkcija (vienos įmonės ar vieno plano atostogos) yra įjungta (456553)

Teisingas prognozuojamas likutis dabar rodo, kai vienos įmonės ar vieno plano atostogų funkcija yra įjungta.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Objektai, kuriuose yra ryšiai, dėl kurių kartojasi naršymo ypatybės (456486)

Šis leidimas ištaiso kelių objektų naršymo ypatybių (ryšys) klaidą. Aptikti pasikartojantys ryšiai. Šie scenarijai buvo ištaisyti.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Visos įmonės komentarai našumo apžvalgoje (455536)

Visos įmonės komentarai dabar matomi našumo apžvalgose su šia pataisa. Šis pakeitimas pataiso recenzento komentarų, kurie buvo įvesti skirtingoms įmonėms tai pačiam našumo peržiūrai, rodinį.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Nesutapimas rodant kompensavimo valdymo duomenis (432562)

Nuoseklus kompensacijų duomenų rodinys dabar palaikomas Vadovo savitarnoje. Atsižvelgiant į tai, kaip naršote darbuotojo **Kompensavimo išsami informacija**, kompensacijų duomenys dabar nuolat parodomi vadovams.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Fiksuotų kompensacijų plano įsigaliojimo data numatyta šiandienos data (411994)

Kompensacijų pradžios data dabar pagrįsta pagal darbuotojui priskirtų pareigų pradžios datą.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Atostogų ir nebuvimo forma „Įjungti pusiaudienio aprašą” yra išjungta, kai forma atsidaro (452607)

Su šiuo pakeitimu **Įjungti pusiaudienio aprašą** bus įjungta, kol naujosios atostogų operacijos egzistuoja. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Išjunkite paskelbimą į HcmDiskusijųObjektas per „Excel”; BendrasVertinimoRezultatas lauko klaida (453899)

Dabar galite atnaujinti **BendrasVertinimoRezultatas** lauką naudodami **HCMDiskusijųObjektas** „Excel ”darbaknygės kūrimo įrankyje.

## <a name="in-preview"></a>Peržiūros režimu

## <a name="database-logging"></a>Duomenų bazės registravimas

Duomenų bazės registravimo funkcija leidžia nustatyti, kurios lentelės ir laukai turi būti stebimi. Taip pat galite nustatyti įvykius, kurie turi aktyvinti keitimų sekimą. Naudojate duomenų bazės registravimo galimybes, kad laikui bėgant pamatytumėte šiuos pakeitimus. Daugiau informacijos ieškokite [Duomenų bazės registravimo konfigūravimas ir tvarkymas](hr-admin-database-logging.md).

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

Klientai gali apdoroti vienoje įmonėje sukauptas atostogas, vienkartines atostogas ir neatvykimų planą. Šis gebėjimas suteikia klientams su skirtingais išėjimo į pensiją metais ar atostogomis aiškumo apie kaupimo strategijas. Norėdami sužinoti daugiau, skaitykite [Sukauptos atostogos įmonėje ar atostogų planas](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).

## <a name="add-attachments-to-time-off-requests"></a>Priedų pridėjimas prašymams atidėti

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

## <a name="configure-the-name-of-employee-self-service"></a>Darbuotojų savitarnos pavadinimo konfigūravimas

Naujoji parinktis bus prieinama **Žmogiškųjų išteklių parametrai**, kad būtų atnaujintas Darbuotojo savitarnos darbo srities pavadinimas į Savitarną.

## <a name="checklist-entities-included-in-common-data-service"></a>Kontrolinio sąrašo objektai, nurodyti „Common Data Service”

Kontrolinių sąrašų objektai, skirti supažindinimo, atleidimo, perkėlimo ir verslo procesams, greitai taps prieinami „Common Data Service”.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)