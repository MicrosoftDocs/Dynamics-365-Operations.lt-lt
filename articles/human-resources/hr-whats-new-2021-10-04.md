---
title: Kas nauja ar pasikeitė „Dynamics 365 Human Resources“ 2021 m. spalio 5 d.
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos Microsoft Dynamics 365 Human Resources 2021 m. spalio 5 d.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba24afd16a471abb36a6f7bc9a8610acec374190
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067978"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Kas nauja ar pasikeitė „Dynamics 365 Human Resources“ 2021 m. spalio 5 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomos priemonės, kurios yra naujos, pakeistos arba netrukus programoje "Microsoft"Dynamics 365 Human Resources.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4485 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
|---|---|---|
| Platformos atnaujinimas 10.0.21 (45) | -- | [Finansų ir operacijų programėlių 10.0.21 versijos platformos naujinimai (2021 m. spalio mėn.)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Mes galime atnaujinti šį straipsnį, kad būtų įtrauktos pataisos, kurios buvo sukurtas po to, kai buvo publikuotas šis straipsnis.

| Problemos numeris | Problema | Aprašymas |
|---|---|---|
| 598896 | Darbuotojo suma nerodoma tol, kol darbuotojas neužbaigė registracijos | **Darbuotojų savitarnos** puslapyje, darbuotojo išmokų suma nėra nurodyta. **Išmokų savitarnos** puslapyje dabar rodoma darbuotojo suma.  |
| 613440 | Neįmanoma eksportuoti duomenų iš **Duomenų valdymo** | Eksportuojant duomenis **Duomenų valdymas** projektui, atsiranda netikėta eksportavimo klaida. |
| 618327 | Uždaryti ir būsimi laikotarpiai rodomi išmokų **Išrašo ataskaitų** parametrų puslapyje | Kai darbuotojų savitarnoje naršote **išmokų išrašą** esantį **Darbuotojų savitarnos**, puslapyje **Ataskaitos parametrai** rodomas **Įtrauktini įrašai** ir **Vykdyti fone** „FastTab“. Šios grafos buvo pašalintos.|
| 618326 | Netinkamas **Išrašų parametrai** puslapis rodomas **Darbuotojų savitarnos** išmokų ataskaitos puslapyje.| Kai pereinate į **Išmokų išrašo ataskaitos** paskirties puslapį, vartotojas gali pasirinkti uždaromo arba būsimo išmokų planų laikotarpius, dėl kurių bus tuščias puslapis. Sąraše turėtų būti rodomas tik dabartinis išmokų plano laikotarpis. |

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
|Siunčiamų laiškų ataskaitos naudojant **GER ataskaitos paskirties vietą** | Išmokų išrašą galima nustatyti naudoti el. pašto parametrus **GER ataskaitos paskirties** puslapyje. Atlikus nustatymą ir spausdinant ataskaitą, vartotojas gaus formatavimo klaidą ir išmokų išrašas nebus išsiųstas.|

## <a name="feature-management-changes"></a>Funkcijų valdymo pakeitimai

| Funkcija | Aprašymas |
|---|---|
|Našumo žurnalų išplėstinių ataskaitų rodinys | Ši funkcija šiame leidime bus įjungta pagal numatytuosius nustatymus. |

## <a name="coming-soon"></a>Jau greitai

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 2-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkcija | Informacija |
|---|---|
| Platformos atnaujinimas 10.0.22 (46) | Platformos atnaujinimo atmetimas 10.0.22 yra suplanuotas pasirodyti su nauju leidimu 2021 m. lapkričio 1 d. Norėdami gauti daugiau informacijos, žr. [10.0.22 finansų ir operacijų programėlių versijos (2021 m. lapkričio mėn.) platformos naujinimus](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 2 bangos apžvalga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

