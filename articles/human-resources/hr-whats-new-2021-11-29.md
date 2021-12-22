---
title: Kas naujo arba pakeista Dynamics 365 Human Resources 2021 m. lapkričio 19 d.
description: Šioje temoje aprašomos priemonės, kurios yra naujos arba pakeistos Dynamics 365 Human Resources 2021 m. lapkričio 19 d. Microsoft.
author: marcelbf
ms.date: 12/03/2021
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
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a86c1c24fbc758f4e3d0fd8b052e02078bee41e
ms.sourcegitcommit: 88f8a0369ce66b82314db9639491b695e18a7e5c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902972"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Kas naujo arba pakeista Dynamics 365 Human Resources 2021 m. lapkričio 19 d.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Microsoft Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Daugiau informacijos apie naujas funkcijas ir numatomas bendras užimtumo datas ieškokite [Dynamics 365 Human Resources 2021 išleidimo bangoje 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Šiame leidime yra šios klaidos pataisos. Pakeitimai taikomi 8.1.4591 komponavimo versijai.

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema | Aprašymas |
|---|---|---|
| 626178 | Vadybininko savitarnoje trūksta **naršymo** | Šis išdavimas dabar yra fiksuotas. Naršymą galima peržiūrėti išsamią ataskaitos informaciją vadybininko **savitarnoje**. |
| 632573 | Įrašant kursą tikrinimo klaidos **nėra** | Šis išdavimas dabar yra fiksuotas. Kuriant kursą, kuriame minimalus dalyvių skaičius didesnis nei 0, vis dar buvo leidžiama įrašyti net tada, kai maksimalus dalyvių skaičius **yra** **0**. |
| 615955 | Kuriant naują **įdarbinimo užklausos vietą įvyko klaida** "Laukas Paskirtis turi būti užpildyta". | Kuriant naujos įdarbinimo užklausos vietos adresą, rodoma klaida: reikia užpildyti lauką Paskirtis. Tačiau **puslapyje** laukas Paskirtis negalimas. |
| 620797 | Ne **besilydinga** gimtinės lauko klaida | Kai neįvedami asmeninio kontakto lytis, ataskaitoje rodoma "Spustelėkite arba spustelėkite čia, norėdami įvesti tekstą", – šiame lauke nieko negalima įvesti kaip klaidingo. |
| 620800 | Išmokų išrašo saitas paslėptas | Pagal numatytuosius nustatymus darbuotojų savitarnoje išmokų **išrašo peržiūrėti** negalima.  Saitas buvo pridėtas dešinėje darbuotojų **savitarnos paslaugos dalyje** **Saitai** |
| 629778 | Efektyvumo problema su CDS integravimą. | Dėl su autorizavimu susijusios užklausos buvo išduotas našumas. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie tai, kaip įjungti ar išjungtas funkcijas, rasite [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
|---|---|---|
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Jau greitai
Išsamų suplanuotų funkcijų ir jų paleidimų sąrašą rasite ["Dynamics 365" ir pramonės debesyse: 2021 išleidimo banga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) 2.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
