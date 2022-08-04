---
title: Kas nauja arba pasikeitė 2021 m. balandžio 5 d. „Dynamics 365 Human Resources”
description: Šiame straipsnyje aprašomos naujos arba pasikeitusios „Microsoft Dynamics 365 Human Resources” funkcijos 2021 m. balandžio 5 d.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9388b2f43762bedf07c89a7a565935d2043ee90c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068008"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Kas nauja arba pasikeitė 2021 m. balandžio 5 d. „Dynamics 365 Human Resources”

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašomos priemonės, kurios yra naujos, pakeistos arba tuoj pat Dynamics 365 Human Resources.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir jų numatomas bendro pasiekiamumo datas žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra toliau pateiktos naujos funkcijos ir klaidų ištaisymai. Pakeitimai taikomi 8.1.4074 komponavimo versijai.

### <a name="new-features"></a>Naujos funkcijos

Šiame leidime bendrai prieinamos toliau pateiktos funkcijos.

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Apribokite darbuotojų galimybes redaguoti įmonės kontaktinius duomenis | [Darbuotojų galimybių redaguoti įmonės kontaktinius duomenis ribojimas](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Asmeninės informacijos redagavimo apribojimas](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šį straipsnį, kad būtų įtrauktos pataisos, kurios buvo sukurtas po to, kai buvo publikuotas šis straipsnis.

| Problemos numeris | Problema |  Aprašymas |
| --- | --- | --- |
| 550852 | **Patvirtinimo** mygtukas nepatvirtina privalomų laukų, nustatytų **Peržiūrėti** formoje. | Kai formoje **Peržiūrėti** nustatote lauką kaip privalomą ir paskelbiate pakeitimus Vadovo vaidmeniui, forma nėra patvirtinama, kaip tikėtasi. |
| 559564 | Darbuotojų veiksmų dėl pastovios atlyginimo dalies pakeitimų retrospektyva išmeta klaidą nutrauktiems vartotojams. | Išėjusio darbuotojo atlyginimo dalies darbuotojo veiksmas išmeta klaidą. Kai darbuotojas nebedirba, darbuotojo paaukštinimo veiksmas prieš darbo nutraukimą išmeta klaidą. |
| 560074 | Išplečiamasis įdarbinimo kategorijų sąrašas nėra filtruojamas pagal **Darbuotojo tipą** ir rodo darbuotojų ir rangovų kategorijas. | Išplečiamojo sąrašo **Įdarbinimo kategorija** formoje **Darbuotojas** turėtų būti rodomos arba darbuotojo, arba rangovo kategorijos, priklausomai nuo darbininko tipo. |
| 567388 | Dalis naujai sukurtų darbuotojų informacijos nėra iš karto sinchronizuojama į „Dataverse” lentelę **„cdm_worker”**. | Kai kuriate naują darbuotojo įrašą, naujas įrašas sinchronizuojasi į „Dataverse” lentelę **„cdm_worker”**, tačiau į „Dataverse” įrašą bus įtrauktos ne visos ypatybės. |
| 563837 | Funkcijos, kurios nėra galimos Personalo valdymo rodinyje. | Keletas funkcijų, kurios netaikomos Personalo valdymo rodiniui, esančiam Funkcijų valdyme. Dabar šios funkcijos yra pašalintos iš funkcijų, prieinamų įgalinimui Personalo valdyme. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie funkcijų įjungimą ir išjungimą žr. [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
| --- | --- | --- |
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Jau greitai

| Funkcija | Informacija |
| --- | --- |
| Vadovo įvesti įgūdžiai savo darbuotojams gali būti automatiškai patvirtinami darbo eigos | Greitai bus išleista. |
| Platformos atnaujinimas 10.0.17 (41) | Platformos atnaujinimas 10.0.17 yra suplanuotas pasirodyti su nauju leidimu 2021 m. balandžio 19 d. Daugiau informacijos rasite finansų ir [operacijų programėlių 10.0.17 versijos platformos atnaujinimų (2021 m. balandžio mėn.)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Norėdami gauti visą planuojamų funkcijų ir jų suplanuotų leidimų sąrašą, žr. [„Dynamics 365 Human Resources” 2021 m. 1-os leidimo bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Taip pat žiūrėkite

[Kas nauja ar pasikeitė „Human Resources”](hr-admin-whats-new.md)</br>
[„Dynamics 365 Human Resources“ 2021 m. leidimo 1 bangos apžvalga](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Atnaujinimo procesas](hr-admin-setup-update-process.md)</br>
[Funkcijų valdymas](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
