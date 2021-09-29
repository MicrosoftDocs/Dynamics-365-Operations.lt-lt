---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. rugsėjo 6 d.
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. rugsėjo 6 d.
author: marcelbf
ms.date: 09/06/2021
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
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2add53b4b014cb65caacff03bf175078d2b70d8f
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485912"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. rugsėjo 6 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Microsoft Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4443 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
|---|---|---|
| Įgalinti neatvykimų vadovą valdyti atostogas | [Įgalinti neatvykimų vadovą valdyti atostogas](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Naudodami šį leidimą mes atnaujiname neatvykimo vadybininko darbo srities rodinį. Daugiau informacijos žr. [Konfigūruoti nebuvimo vadovo vaidmenį](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Konfigūruoti priedo reikalavimus atostogų tipui | [Konfigūruoti priedo reikalavimus atostogų tipui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Atostogų ir neatvykimų tipų konfigūravimas](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Konfigūruoti atostogų vienetus kiekvienam atostogų tipui | [Konfigūruoti atostogų vienetus kiekvienam atostogų tipui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Atostogų ir neatvykimų tipų konfigūravimas](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema | Aprašas |
|---|---|---|
| 610128 | Klaida publikuojant duomenis naudojant „HcmDiscussionOverallCommentEntity” | Kai duomenys yra publikuojami iš „Excel” darbaknygės į objektą „HcmDiscussionOverralCommentEntity”, įvyksta toliau nurodyta klaida: „Nepavyko rasti duomenų šaltinio įrašo, kurio tipas HcmTopicOverrall.” |
| 589073 | EEO-1 ataskaitoje skaičiuojamos „Nekonkrečios” ir tuščios lauko **Lytis** reikšmės, kai reikšmė yra „Moteris”. | Jei **Vyras** nėra nurodytas lauke **Lytis**, EEO-1 ataskaita sugeneruoja numatytąją reikšmę **Moteris**. |
| 589617 | Išleidimo iš darbo laiko kortelės likutis, Galimi pirkti ir Galimi parduoti balansai nerodomi, kai vartotojų vaidmenis gali naudoti tik tam tikras juridinis subjektas. | Jei vartotojas (darbuotojo vaidmuo) apribotas konkrečiam juridiniam subjektui, balansai nerodomi teisingai **Išleidimo iš darbo laiko balansai** ir **Galimi pirkti** bei **Galimi parduoti** laukuose. |
| 604310 | Neatvykimų vadovo skirtukas turėtų būti paslėptas, kai vartotojui nepriskirta neatvykimo hierarchija. | Pasirinkto juridinio subjekto **Neatvykimų vadovo** skirtukas turi būti paslėptas savitarnos portale, nebent būtų įgalintas kelių įmonių parametras ir bent viena neatvykimo hierarchija yra susieta su vartotoju. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie tai, kaip įjungti ar išjungtas funkcijas, rasite [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
|---|---|---|
| Įgalinti supaprastintą algalapio integravimą (algalapio integravimo API) | [Įjunkite supaprastintas integraciją su mokėjimo tiekėjais](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algalapių integravimo API](hr-admin-integration-payroll-api-introduction.md) |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui | [Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Parengta mokėti](/dynamics365/human-resources/hr-compensation-payroll) |
| Pasirinktiniai Tinkamumo laukai |[Pasirinktinių laukų palaikymas tinkamumo apdorojime](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Pasirinktinių laukų naudojimas tinkamumo apdorojime](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Jau greitai

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkcija | Informacija |
|---|---|
| Platformos atnaujinimas 10.0.21 (45) | Platformos atnaujinimo atmetimas 10.0.21 yra suplanuotas pasirodyti su nauju leidimu 2021 m. spalio 4 d. Dėl daugiau informacijos, žr. [Platformos atnaujinimas „Finance and Operations“ programos 10.0.21 versijai (2021 m. spalio mėn.)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Išmokų išrašas | Išmokų išrašas, skirtas dabartiniams darbuotojo išmokų išrinkimams peržiūrėti. Daugiau informacijos ieškokite [Išmokų išraše](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) Leidimo bangos dokumente. |

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
