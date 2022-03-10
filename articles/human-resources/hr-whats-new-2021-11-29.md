---
title: Kas naujo ar pakeista Dynamics 365 Human Resources 2021 m. lapkričio 19 d
description: Šioje temoje aprašomos funkcijos, kurios yra naujos arba pakeistos atskiroje Microsoft Dynamics 365 Human Resources 2021 m. lapkričio 19 d.
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
ms.openlocfilehash: 618d90f95637002f444b334e16d3fef466dda65e
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087479"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Kas naujo ar pakeista Dynamics 365 Human Resources 2021 m. lapkričio 19 d

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje aprašomos naujos, pasikeitusios ar netrukus pasirodysiančios „Microsoft Dynamics 365 Human Resources“ funkcijos.

Daugiau informacijos apie mūsų atnaujinimo procesą ir grafiką žr. [Atnaujinimo procesas](hr-admin-setup-update-process.md).

Norėdami gauti daugiau informacijos apie naujas funkcijas ir numatomas bendras jų pasiekiamumo datas, žr [Dynamics 365 Human Resources 2021 m. išleidimo banga 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šiame leidime

Į šį leidimą įtraukti šie klaidų pataisymai. Pakeitimai taikomi 8.1.4591 komponavimo versijai.

### <a name="bug-fixes"></a>Klaidų ištaisymai

Toliau nurodyti klaidų ištaisymai įtraukti į šį leidimą.

> [!NOTE]
> Siekiame kuo greičiau pateikti jums šią informaciją. Galime atnaujinti šią temą, kad būtų įtraukti klaidų ištaisymai, įtraukti į komponavimo versiją publikavus šią temą.

| Problemos numeris | Problema | Aprašymas |
|---|---|---|
| 626178 | Darbuotojo išklotinėse nėra naršymo **Vadovo savitarna** | Šis išdavimas dabar yra fiksuotas. Naršymas pasiekiamas norėdami pamatyti išsamią ataskaitos informaciją **Vadovo savitarna**. |
| 632573 | Įrašant nėra patvirtinimo klaidos **Kursas** | Šis išdavimas dabar yra fiksuotas. Kurdami kursą su **Minimalus dalyvių skaičius** į didesnį nei 0 vis tiek buvo leista išsaugoti net tada, kai **Maksimalus dalyvių skaičius** yra 0. |
| 615955 | Klaida „Laukas **Tikslas** turi būti užpildytas kuriant naują įdarbinimo užklausos vietą. | Kurdami adresą naujai įdarbinimo užklausos vietai, gausite klaidą: „Reikia užpildyti lauką „Tikslas“. Tačiau, **Tikslas** laukelis puslapyje nepasiekiamas. |
| 620797 | Tuščias **Lytis** lauko klaida yra klaidinanti | Kai asmeninio kontakto lytis neįvedama, ataskaitoje rodoma „Spustelėkite arba bakstelėkite čia norėdami įvesti tekstą“ – tai klaidina, nes lauke nieko negalima įvesti. |
| 620800 | Privalumų ataskaitos nuoroda paslėpta | Pagal numatytuosius nustatymus naudos ataskaita nematoma **Darbuotojų savitarna**.  Dešinėje pusėje buvo pridėta nuoroda **Darbuotojų savitarna** pagal **Nuorodos** skyrius |
| 629778 | CDS integravimo našumo problema. | Su įgaliojimu susijusi užklausa sukėlė našumo problemą. |

## <a name="in-preview"></a>Peržiūros režimu

Toliau pateiktos naujos funkcijos yra peržiūrimos. Daugiau informacijos apie tai, kaip įjungti ar išjungtas funkcijas, rasite [Funkcijų valdymas](hr-admin-manage-features.md).

| Funkcija | Leidimo planas | Dokumentacija |
|---|---|---|
| Išmokų valdymo darbo sritis | [Išmokų valdymo darbo sritis (peržiūra)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Išmokų valdymo darbo sritis](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Jau greitai
Išsamų planuojamų funkcijų sąrašą ir suplanuotus jų leidimus žr [„Dynamics 365“ ir pramonės debesys: 2021 m. 2 išleidimo banga](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
