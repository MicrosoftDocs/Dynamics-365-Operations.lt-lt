---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. rugpjūčio 6 d.)
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2020 m. rugpjūčio 06 d.
author: andreabichsel
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dbcf854330b7c5ba6ca812a5aed384584c05ce8d
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062191"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” (2020 m. rugpjūčio 6 d.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šioje temoje aprašomos naujos arba pasikeitusios „Dynamics 365 Human Resources” funkcijos. Pakeitimai taikomi 8.1.3444 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo LCS palaikymo numerius informaciniais tikslais.

## <a name="platform-update-1001236-is-now-available"></a>Platformos atnaujinimas 10.0.12(36) yra dabar prieinamas

Daugiau informacijos žr [„Finance and Operations“ programų 10.0.12 versijos platformos naujiniai (2020 m. rugpjūčio mėn.)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12.md).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Duomenų valdymo sistemos (DMF) objektai, skirti išmokų valdymui
 
Išmokų valdymo objektai ir išleidimas. DMF objektai leidžia paprastai importuoti ir eksportuoti duomenis, kad lengviau konfigūruotumėte išmokų valdymą. Išmokų valdymo šablonas taps prieinamu duomenų perkėlimui. Šablonas nuosekliai eksportuoja ir importuoja duomenis išsaugodamas duomenų priklausomumą. Daugiau informacijos ieškokite:

- [DMF objektas palaikomas](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) „Dynamics 365 2020“ leidimas bangai 1 planui
- [Duomenų valdymo apžvalga](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire sukuria darbo srautą atostogų užklausų įsigijimui ir pardavimui (446557)

Daugiau informacijos ieškokite:

- [Leisti darbuotojams pirkti ir parduoti atostogas](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) „Dynamics 365 2020“ leidimo 2 bangos planui
- [Atostogų pirkimo ir pardavimo strategijų valdymas](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atostogų pirkimas ir pardavimas](./hr-employee-self-service-buy-sell-leave.md)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Darbuotojo pašto adresų V2 objektas turi prieigą prie teisinių objektų su apribota prieiga (459126)

Šiuo pakeitimu, **Darbuotojo pašto adreso V2** objektas bus apribotas pagal teisinio objekto prieigą, kurią suteikė vartotojas.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Darbo srauto elektroninio pašto nuoroda negali atidaryti svarbių peržiūrų (437398)

Jums naudojant rezervuotą vietą siekiant atidaryti vykdymo peržiūrą peržiūrų darbo sraute, elektroniniame pašte sukurta nuoroda dabar atsidaro pasirinktam įrašui.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Nauji objektai atostogų įsigijimui ir pardavimui (473180)

Duomenų valdymo darbotvarkės objektai dabar yra prieinami atostogų įsigijimui ir pardavimui. Dėl daugiau informacijos, žr. [Duomenų valdymo peržiūra](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Peržiūrint įrašo informaciją ir naudojant papildomus filtrus, vartotojas gali gauti prieigą prie kitų darbuotojų įrašų (472490)

Šiuo pakeitimu, darbuotojų savitarnos vartotojai gali tik prieiti prie jų pačių įrašų naudojant darbuotojų savitarnos paslaugas. Įrašo informacijos peržiūra keičiant filtravimo parinktis neberodo papildomų duomenų.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Personalo valdymo analitika apima išėjusių darbuotojų įrašus (382893)

Su šiuo išleidimu, personalo valdymo analitika tik apima dirbančius darbuotojus. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Nepavyksta apdoroti darbuotojo užmokesčio padidėjimo (473125)

Šis keitimas leidžia jums įvesti užmokesčio padidėjimus jums keičiant įsigaliojimo datą naujo užmokesčio padidėjimui.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Darbo srauto peržiūra gali būti pradėta daugiau nei kartą (467541)

Šiuo pakeitimu galite tik vieną kartą pradėti peržiūros darbo srauto vykdymą. Vadovo būsena neberodo parinkties peržiūros pradėjimui.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Atostogų užklausos darbo srautas pasibaigia klaida, jei patvirtinta atostogų užklausa yra atšaukiama (472063)

Šiame leidime, jums atšaukiant patvirtintą atostogų užklausą, užklausos būsena nebėra patvirtinta ir darbo srautas bus tęsiamas.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Sistema siūlo išėjusius darbuotojus kuriant naują peržiūros formos šabloną (460624)

Šiuo pakeitimu, išėję darbuotojai nebėra prieinami sukuriant naujus leidimus šablone. Galite sukurti darbuotojų peržiūras, kurie nepatenka į jų darbo datas.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Hierarchijos padėčių apykaitos ataskaitos aptikimas (415879)

Šiuo pakeitimu, padėties hierarchijos apykaitos ataskaitos aptikimas yra apribotas iki vieno taško laike. Galite vykdyti apykaitos ataskaitos aptikimą skirtingoms datoms tam, kad patvirtintumėte, ar ataskaitos struktūra neturi apykaitos ataskaitų.

## <a name="buy-and-sell-leave"></a>Atostogų pirkimas ir pardavimas 

Kai kurios organizacijos suteikia išmoką, kuri leidžia darbuotojams pirkti ar parduoti savo atostogas. Šis procesas dažnai valdomas neautomatiniu būdu. Ši funkcija automatizuoja žmogiškųjų išteklių departamento valdymo strategijas ir užklausas. Ji supaprastina atostogų valdymo procesą ir padeda pašalinti klaidas. Daugiau informacijos ieškokite:

- [Leisti darbuotojams pirkti ir parduoti atostogas](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) „Dynamics 365 2020“ leidimo 2 bangos planui
- [Atostogų pirkimo ir pardavimo strategijų valdymas](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atostogų pirkimas ir pardavimas](./hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Atostogų kaupimas vienai įmonei arba vienam planui

Klientai gali apdoroti vienoje įmonėje sukauptas atostogas, vienkartines atostogas ir neatvykimų planą. Ši galimybė suteikia aiškumo padidėjimo procesui klientams su skirtingais atostogų metais ar atostogų kaupimo politikomis. Norėdami sužinoti daugiau, skaitykite [Sukauptos atostogos įmonėje ar atostogų planas](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Įtraukite priedus į laiko prašymus

Galimybė pridėti priedus prie patvirtintų atostogų prašymų yra itin svarbi dabartinėje COVID-19 situacijoje. Dabar darbuotojai gali pridėti šiuos priedus. Jie taip pat turi daugiau įžvalgų apie atostogų prašymų naujinimų kūrimą. Norėdami sužinoti daugiau, skaitykite [Priedo prie esamo prašymo pridėjimas](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Priežasties kodo pridėjimas į kaupimo sustabdymus 

Į kaupimo sustabdymus įtraukti priežasties kodai.

## <a name="carry-forward-rules"></a>Perkėlimo taisyklės 

Galite nurodyti perkėlimo atostogų tipą, skirtą perkėlimo balansams ir į kurį perkeliami perkeliamų balansų koregavimai. Pavyzdžiui, jei darbuotojas perkelia 10 dienų, toms 10 dienų galite pasirinkti kitą atostogų tipą. Daugiau informacijos žr. [Atostogų ir neatvykimų tipų konfigūravimas](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Atostogų kaupimo sustabdymas konkretiems atostogų tipams

Galite sukurti taisyklę sustabdyti darbuotojų, įvedusių neapmokamų atostogų prašymus, atostogų kaupimą. Neapmokamos atostogos gali būti tipas, tačiau tai neprivaloma. Galite sustabdyti bet kokias atostogas, pagrįstas kitu atostogų tipu.

## <a name="in-preview"></a>Peržiūros režimu

### <a name="mandatory-fields"></a>Privalomi laukai

Galite nustatyti laukelius privalomais naudodami Žmogiškųjų išteklių personalizavimo galimybes. Šiai funkcijai reikia **Įrašyti rodiniai**. Dėl platesnės informacijos apie įrašytas peržiūras, žr.:

- [Įrašytos peržiūras - bendras prieinamumas](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) „Dynamics 365 2020“ leidime bangos 2 planas
- [Formų, kurios visiškai išnaudoja įrašytus rodinius, kūrimas](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>„Human Resources“ programa programoje „Teams“

Darbuotojai gali peržiūrėti ir prašyti atostogų programoje „Microsoft Teams“. Jie gali bendrauti su robotu, kad sukurtų atostogų prašymą. Daugiau informacijos ieškokite:

- [Darbuotojo atostogų ir nebuvimo patirtis „Microsoft Teams“](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) „Dynamics 365“ 2020 leidime bangos 1 plane
- [„Human Resources“ programa „Teams“](./hr-admin-teams-leave-app.md)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF objektas pasiekiamas kaupimo sustabdymams

DMF objektas dabar pasiekiamas kaupimo sustabdymams.

## <a name="coming-soon"></a>Jau greitai

## <a name="checklist-entities-included-in-dataverse"></a>Kontrolinio sąrašo objektai, nurodyti „Dataverse”

Tikrinimo objektai Įtraukimo, Atleidimo, Perleidimo ir Verslo procesams bus greitai prieinami „Dataverse“.

## <a name="known-issues"></a>Žinomos problemos

**Ateities valdymas** darbo sritis gali rodyti funkcijas, kurios yra išjungtos kaip peržiūros funkcijos joms bendrai esant įjungtoms. Toliau pateiktas bendras esamų funkcijų sąrašas, rodantis neteisingą statusą. 

1.  Išmokų valdymas
2.  Atvejų valdymas
3.  Duomenų įrašymas (auditavimas)
4.  Atostogų skaičiavimas vienai bendrai ar vienam planui
5.  Atostogų ir nebuvimo skaičiavimo sustabdymas
6.  Balanso keitimo priežasties kodas ir komentaras
7.  Atostogų pirkimas ir pardavimas
8.  Atostogų ir nebuvimo kalendorius
9.  Atostogų turėjimo perdavimo taisyklės
10. Atostogų skaičiavimo auditas
11. Atostogų skaičiavimo pašalinimas
12. Atostogų skaičiavimo apvalinimas
13. Konfigūruoti keletą atostogų tipų viename atostogų plane
14. Atnaujinti nedirbamo laiko papildymus
15. Naudoti darbuotojo FTE apskaičiavimams
16. Kryžminės bendrovės kompensavimo peržiūra
17. Veiklos efektyvumo vertinimų spausdinimas
18. Atostogų skaičiavimo patikslinimai

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2019 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]