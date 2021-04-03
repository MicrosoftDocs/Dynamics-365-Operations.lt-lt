---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. gegužės 28 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources funkcijos 2020 m. gegužės 28 d.
author: andreabichsel
manager: tfehr
ms.date: 05/28/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8e8d7f87f30286eefa1b3b53925702f4735132e6
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465275"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ (2020 m. gegužės 28 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos. Pakeitimai taikomi 8.1.3287 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>Objektas „LeaveRequest“ neveikia, kai įgalinate kelis tipus pagal atostogų planui (447498)

Šiuo pakeitimu **„LeaveEnrollmentV2Entity“** nuo šiol galima taisyti klaidą, kuri įvyksta, kai įgalinami keli atostogų plano tipai.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Paketinio konflikto sumažinimo priemonė (peržiūra) (446619)

Kai įgalinate šią funkciją, galite tikėtis, kad sumažės blokavimų paketinės sistemos lentelėse, kai pasirenkate ir užbaigiate užduotis.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>„UpdateConflict“ įrašant darbuotoją neleidžia redaguoti įrašo dalyje Žmonės (427915)

Šis pakeitimas ištaiso klaidą, pateikiamą, kai įtraukiamas naujas darbuotojas, naujinama adreso informacija ir keičiamos kalbos nuostatos. Šiame unikaliame scenarijuje pateikiama klaida, rodanti, kad įrašo nepavyko atnaujinti. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Nepavyksta įtraukti priedo prie patvirtintos atostogų užklausos pakartotiniam pateikimui (425407)

Šis pakeitimas nuo šiol leidžia priedus patvirtintiems atostogų prašymams.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Vartotojas gali įvesti darbuotojo kompensaciją kitoje juridinio subjekto formoje (409529)

Šiuo pakeitimu išjungiamos kompensavimo parinktys, siekiant išvengti netyčinio netinkamo juridinio subjekto kompensacijų įrašų įvedimo.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Klaida, kai perkeliant darbuotoją, darbuotojo pareigų priskyrimo data yra ankstesnė nei pareigų trukmė (429402)

Klaidos pranešimai perkeliant darbuotoją šiame scenarijuje buvo atnaujintas, kad aiškiau aprašytų problemą ir reikalingus pakeitimus.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Priedų galimybės darbuotojo savitarnos išmokų registracijoje
 
Nuo šiol galite įtraukti priedus išmokų registracijos proceso metu kiekvienam planui, kuriam darbuotojas registruojasi. Tada galite peržiūrėti priedus, esančius formoje **Darbuotojo užregistruotos išmokos**.

## <a name="in-preview"></a>Peržiūros režimu

## <a name="human-resources-application-in-teams"></a>„Human Resources“ programa programoje „Teams“

Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“. Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą. Daugiau informacijos žr. [„Human Resources“ programa programoje „Teams“](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="leave-suspension"></a>Atostogų sustabdymas

Programoje „Human Resources” galite sustabdyti darbuotojo atostogas ir neatvykimą. Atostogų sustabdymas sustabdo pasirinktų atostogų tipų atostogų kaupimus. Jei sustabdymas įvyksta po to, kai kaupimas buvo apdorotas, atostogų sustabdymas sukuria proporcingai paskirstytą darbuotojo atostogų balanso koregavimą. Daugiau informacijos žr. [Atostogų sulaikymas](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Vartotojo patirties naujinimas nurodyti, jog kaupimas sustabdytas (429550)

Dabar vartotojo patirtis nurodo, kad plano kaupimas buvo sustabdytas.

## <a name="coming-soon"></a>Jau greitai

## <a name="database-logging-in-preview-in-june"></a>Duomenų bazės registravimas (peržiūra nuo birželio mėn.)

Duomenų bazės registravimo funkcija leidžia nustatyti, kurios lentelės ir laukai turi būti stebimi. Taip pat galite nustatyti įvykius, kurie turi aktyvinti keitimų sekimą. Ilgalaikiams pokyčiams stebėti suteikiamos užklausos galimybės.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Atostogų pirkimas ir pardavimas (peržiūra nuo birželio 1 d.)

Kai kurios organizacijos suteikia išmoką, kuri leidžia darbuotojams pirkti ar parduoti savo atostogas. Šis procesas dažnai valdomas neautomatiniu būdu. Ši funkcija suteikia automatizuotą būdą tvarkyti žmogiškųjų išteklių skyriaus strategijas ir reikalavimus, taip pat padeda pašalinti klaidas, tuo pačiu supaprastinant atostogų tvarkymo procesą. Daugiau informacijos ieškokite:

- [Atostogų pirkimo ir pardavimo strategijų valdymas](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atostogų pirkimas ir pardavimas](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Duomenų valdymo sistemos (DMF) objektai, skirti išmokų valdymui
 
Išmokų valdymo objektai ir išleidimas. DMF objektai leidžia importuoti ir eksportuoti duomenis, kad būtų lengviau konfigūruoti išmokų valdymą. Išmokų valdymo šablonu taip pat bus galima perkelti duomenis. Šablonas nuosekliai eksportuoja ir importuoja duomenis, išsaugodamas duomenų ryšius.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Priežasties kodo įtraukimas į kaupimo sustabdymus (birželio 1 d.)

Į kaupimo sustabdymus įtraukti priežasties kodai.

## <a name="carry-forward-rules-june-1"></a>Taisyklių perkėlimas (birželio 1 d.)

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Nurodytų atostogų tipų atostogų kaupimo sustabdymas (birželio 1 d.)

Šiame leidime personalas gali sukurti taisyklę, skirtą sustabdyti darbuotojų, įvedusių atostogų užklausas neapmokamoms atostogoms, atostogų kaupimus. Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma. Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF objektas pasiekiamas kaupimo sustabdymams (birželio 1 d.)

DMF objektas dabar pasiekiamas kaupimo sustabdymams.

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]