---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources” 2021 m. liepos 26 d
description: Šioje temoje aprašomos naujos ar pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. liepos 26 d.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 810511c42cd690579d8c8b6ebcc17b0cf7fcb9eb2b999822dc2226fabd127cc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771520"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources” 2021 m. liepos 26 d

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4384 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Platformos „update 10.0.20“ | -- | [Platformos naujinimai, skirti 10.0.20 „Finance and Operations” programų versijai (2021 m. rugpjūčio mėn.)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema |  Aprašas |
| --- | --- | --- |
| 600422 | Algalapio adreso tikrinimo nepavyksta nustatyti kaip Parengta mokėti. | Tikrinimas atnaujintas taip, kad būtinas tik vienas adresas, kurių tipas 'Atlyginimų vieta' ir tik vienas adresas, kurių tipas 'Atlyginimų darbo vieta'. |
| 601226 | Duomenų integravimo problema: algalapio integravimo eksportavimo projekte nėra parinkties visiškai stumti | Algalapio integravimą į Ceriforce DayForce užuot stūmimo didėjusi. Ceri to reikia visada atnaujinti visą pajėgumą. Ši problema dabar yra fiksuota, duomenų eksportavimo projekto objektai nebebus konvertuojami į didėjančią sąsmę. |
| 602272 | Prie darbuotojų savitarnos darbo srities pridėtos per daug darbo srities, todėl prie jos nieko nebegalima pridėti | Išs nustatome darbuotojų savitarnos paslaugos personalizavimo problemą. Nauja darbo dalis gali būti įtraukta į rodinį ir bet koks esamas personalizavimas bus matomas vartotojams |
| 600711 | Įgalintas pusės dienos apibrėžimo pasirinkimo laukas, skirtas visos dienos atostogų užklausoms | Šis išdavimas yra fiksuotas, o pusės dienos apibrėžimo laukas bus įgalintas tik tada, kai darbuotojai pasirinks atostogų tipą, turiį pusiau dienos apibrėžimą, o pusdienį – kaip pasirinktą sumos vertę |
| 602208 | Kaupimo koeficiento vienetai, kuriuose rodomos valandos vietoj dienų | Šis išdavimas dabar yra fiksuotas. Formoje **Laiko išjungimas** bus rodomas tinkamas atostogų vienetas (valandos arba dienos), skirtas stulpeliui **Kaupimo koeficientas**. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Įgalinti supaprastintą algalapio integravimą (algalapio integravimo API) | [Įjunkite supaprastintas integraciją su mokėjimo tiekėjais](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algalapių integravimo API](hr-admin-integration-payroll-api-introduction.md)|
|  Įgalinti neatvykimų vadovą valdyti atostogas | [Įgalinti neatvykimų vadovą valdyti atostogas](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Naudodami šį leidimą mes atnaujiname neatvykimo vadybininko darbo srities rodinį. Daugiau informacijos žr. [Konfigūruoti nebuvimo vadovo vaidmenį](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  Konfigūruoti priedo reikalavimus atostogų tipui | [Konfigūruoti priedo reikalavimus atostogų tipui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Atostogų ir neatvykimų tipų konfigūravimas](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Konfigūruoti atostogų vienetus kiekvienam atostogų tipui | [Konfigūruoti atostogų vienetus kiekvienam atostogų tipui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Atostogų ir neatvykimų tipų konfigūravimas](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui | [Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Parengta mokėti](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Jau greitai

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
