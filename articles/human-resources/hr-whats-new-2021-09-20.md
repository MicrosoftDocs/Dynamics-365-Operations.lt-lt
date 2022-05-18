---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. rugsėjo 20 d.
description: Šioje temoje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. rugsėjo 20 d.
author: marcelbf
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3fd8705c7735cb3c0945f71651fafa767a7addf
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691588"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Human Resources“ 2021 m. rugsėjo 20 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Microsoft Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4464 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
|---|---|---|
| Įgalinti supaprastintą algalapio integravimą (algalapio integravimo API) | [Įjunkite supaprastintas integraciją su mokėjimo tiekėjais](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algalapių integravimo API](hr-admin-integration-payroll-api-introduction.md) |
| Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui | [Įgalinkite darbuotojus būtų pažymėtiems kaip pasiruošusius apmokėjimui](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Parengta mokėti](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema | Aprašymas |
|---|---|---|
| 619774 | Adreso aprašymo redagavimas nesinchronizuojamas „Dataverse“ su realiuoju laiku. | Redaguojant darbuotojo adreso aprašymą, atnaujintas aprašas nesinchronizuojamas realiuoju „Dataverse“ laiku. Logistikos vietos **lentelės abonementas** buvo atnaujintas, kad būtų galima siųsti naujinimą. |
| 614603| Kai **nepasirinktas** parametro **Darbuotojo personalo veiksmai** puslapyje Darbuotojas įvyko klaida. | Pasamdant naują darbuotoją arba pereinant į puslapį **Darbuotojas** rodoma toliau nurodyta klaida: „Laukelis **Personalo veiksmų tipas** turi būti užpildytas", net jei **Personalo veiksmai** yra išjungti. |
| 615367 | **Patvirtintas laiko išjungimo** skirtukas rodo perspėjimą ir neteisingai rodo. | Jei atostogų vienetas nustatytas kaip **Dienos** prieš įgalinant funkciją **Konfigūruoti atostogų vienetus pagal atostogų tipą**, skirtukas **Patvirtintas laiko išjungimas** rodomas netinkamas įspėjimas ir neteisingi stulpeliai. |


## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie tai, kaip įjungti ar išjungtas funkcijas, rasite [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
|---|---|---|
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |
| Pasirinktiniai Tinkamumo laukai |[Pasirinktinių laukų palaikymas tinkamumo apdorojime](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Pasirinktinių laukų naudojimas tinkamumo apdorojime](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Išmokų išrašas |[Išmokų pareiškimas](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Išmokų išrašas](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Išmokų pareiškimo žinomos problemos

| Problema | Aprašymas |
|---|---|
| **Netinkamas išmokų** puslapyje **išrašo darbuotojų savitarnos** ataskaitos parametrų puslapis. | Kai darbuotojų savitarnoje naršote **išmokų išrašą** esantį **Darbuotojų savitarnos**, puslapyje **Ataskaitos parametrai** rodomas **Įtrauktini įrašai** ir **Vykdyti fone** „FastTab“.  Šiuos poreikius reikia pašalinti. |
| Uždaryti ir būsimi laikotarpiai rodomi išmokų **išrašo ataskaitų** parametrų puslapyje. | Kai pereinate į išmokų išrašo ataskaitos paskirties puslapį, vartotojas gali pasirinkti uždaromo arba būsimo išmokų planų laikotarpius, dėl kurių **bus tuščias puslapis**. Sąraše turėtų būti rodomas tik dabartinis išmokų plano laikotarpis. |
|Siunčiamų laiškų ataskaitos naudojant GER ataskaitos paskirties vietą klaida. | Išmokų išrašą galima nustatyti naudoti el. pašto parametrus **GER ataskaitos paskirties** puslapyje. Atlikus nustatymą ir spausdinant ataskaitą, vartotojas gaus formatavimo klaidą ir išmokų išrašas nebus išsiųstas.|


## <a name="coming-soon"></a>Jau greitai

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkcija | Informacija |
|---|---|
| Platformos atnaujinimas 10.0.21 (45) | Platformos atnaujinimo atmetimas 10.0.21 yra suplanuotas pasirodyti su nauju leidimu 2021 m. spalio 4 d. Daugiau informacijos rasite finansų ir operacijų [programėlių 10.0.21 versijos (2021 m. spalio mėn.) platformos naujinimus](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Našumo žurnalų išplėstinių ataskaitų rodinys | Numatyta, kad ši funkcija bus įgalinta kito iškėjimo metu. |


## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
