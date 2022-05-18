---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” 2021 m. liepos 12 d
description: Šioje temoje aprašomos naujos ar pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. liepos 12 d.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c01d00e7ede44c20e64fc4a8cd8646201caa3992
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686805"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” 2021 m. liepos 12 d

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4353 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
|  Tarnybos metų rodymo perjungiklis | |Ši funkcija suteikia parinktį naudoti skirtingas datas, kad būtų galima apskaičiuoti tarnybos metus, kurie rodomi **Supaprastinto darbuotojo įrašo** ir **Žmonių** puslapiuose.  Tai bus galima [Personalo parametruose](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema |  Aprašas |
| --- | --- | --- |
| 595871 | Žmogiškųjų išteklių srityje „Apie” naudojama neteisinga „Dataverse” terminologija | Pertvarkius „Common Data Service” į „Dataverse”, terminologija buvo atnaujinta „Microsoft Dynamics 365 Human Resources” informacijos srityje (**Pagalba ir palaikymas > Apie**). |
| 598676 | Tai, kad supaprastintų darbuotojų įrašų forma nepaiso užduoties, gali sukurti klaidą, kai naudojama Įrašytame rodinyje| **Darbuotojo** puslapyje, jei įjungta „Supaprastinto darbuotojo įrašo” funkcija, programa gali nepavykti, jei **Visada atidaryti redagavimui** yra nustatyta įrašytame rodinyje. |
| 592344 |Darbuotojų kompensacijų skyrius pareigose turi būti tik skaitomas, kai įgalintas išmokų valdymas | Darbuotojų kompensacijų informacija sukuriama naudojant senstelėjusią išmokų funkciją.  Kai išmokų valdymas yra įgalintas, laukai bus tik skaitomi. Kai išmokų valdymas yra įjungtas, o **Slėpti senstelėjusias išmokų formas** nustatyta į **Taip** Personalo bendrintuose parametruose, **Darbuotojų kompensacijos** skirtukas bus paslėptas. |
| 598617 | **Hcm Diskusijos** formos aktyvavimo skirtukas sukelia neribotą ciklą, kai taikomi suasmeninimai | Kai tiek tinklelio, tiek informacijos rodiniuose įjungta **Visada atidaryti redagavimui** funkcija, perrašytos užduoties metodo skirtuką suaktyvinantis kodas nesuderinamas su suasmeninimu, nustatant pagrindinį valdiklį ir taip sukuriamas nesibaigiantis ciklas. |
| 593553 | Efektyvumo žurnalo laukas Žurnalo data rodomas UTC formatu | Efektyvumo žurnalų lauke **Žurnalo data** rodoma UTC laiko juosta, o ne laiko juosta, apibrėžta sistemos datos nustatyme, dėl to data kai kurioms laiko juostoms gali būti netinkama. |
| 586930 | Efektyvumo tikslų veiklų atidarymas atidaro visiškai kitą įrašą | Kai funkcija „Išplėstinis efektyvumo žurnalų ataskaitų rodinys” įjungta Funkcijų valdyme, pasirenkant efektyvumo tikslus **Darbuotojo savitarnos** skirtuke **Mano komanda** atidaromi darbuotojų, o ne pasirinkto darbuotojo tikslai. |
| 569959 |  „HcmPositionWorkerAssignmentV2” objektas nepriskiria darbuotojo pareigoms | Vartotojai gaudavo klaidą pridėdami pareigų priskyrimo įrašą iš objekto, o publikavimas nepavykdavo. |
| 582259 | „VETS 4212” ataskaita naudoja 2017 formą, o ne 2020 formą | Atnaujinta į 2020 formatą.  Norėdami įkelti naują formatą, eikite į **Ataskaitos konfigūracijos** ir panaikinkite „VETS-4212” atskaitą kairiajame stulpelyje. Eikite į **Elektroninės ataskaitos – Saugyklos – Personalo ištekliai** ir pasirinkite **Atidaryti**.  Pasirinkite **„VETS-4212” PDF spaudinį** ir **Importuoti**.|


## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Įgalinti supaprastintą algalapio integravimą (algalapio integravimo API) | [Įjunkite supaprastintas integraciją su mokėjimo tiekėjais](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algalapių integravimo API](hr-admin-integration-payroll-api-introduction.md)|
|  Įgalinti neatvykimų vadovą valdyti atostogas | [Įgalinti neatvykimų vadovą valdyti atostogas](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Konfigūruoti neatvykimų vadovo vaidmenį](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Konfigūruoti priedo reikalavimus atostogų tipui | [Konfigūruoti priedo reikalavimus atostogų tipui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Atostogų ir neatvykimų tipų konfigūravimas](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Konfigūruoti atostogų vienetus kiekvienam atostogų tipui | [Konfigūruoti atostogų vienetus kiekvienam atostogų tipui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Atostogų ir neatvykimų tipų konfigūravimas](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui | [Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Parengta mokėti](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Jau greitai

| Funkcija | Informacija |
| --- | --- |
| Platformos atnaujinimas 10.0.20 (44) | Platformos atnaujinimas 10.0.20 yra suplanuotas pasirodyti su nauju leidimu 2021 m. liepos 26 d. Daugiau informacijos rasite finansų ir [operacijų programėlių 10.0.20 versijos (2021 m. rugpjūčio mėn.) platformos naujinimus](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 1 bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
