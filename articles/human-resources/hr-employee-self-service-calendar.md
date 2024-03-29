---
title: Komandos kalendoriaus kūrimas
description: Peržiūrėti ir kurti komandų kalendorius „Dynamics 365 Human Resources“.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6dffcb265030922e5134cfab1310027be43d87ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904165"
---
# <a name="view-team-and-company-calendars"></a>Komandos ir įmonių kalendorių peržiūra

>[!Important]
>Šiame straipsnyje parodytos funkcijos šiuo metu yra galimos klientams autonominiu metu Dynamics 365 Human Resources. Kai kurios arba visos funkcijos bus prieinamos kaip būsimo „Finance“ infrastruktūros leidimo dalis po to, kai bus išleistas „Finance“ leidimas 10.0.26.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite peržiūrėti komandos ir įmonės kalendorius „Dynamics 365 Human Resources“. Komandų kalendoriuose rodomos tik tiesioginės ataskaitos, kaip nurodyta eilutės hierarchijoje.

## <a name="view-your-team-calendar-as-an-employee"></a>Peržiūrėkite komandos kalendorių kaip darbuotojas

- **Darbuotojo savitarnos** darbo srityje pasirinkite **Komandos nebuvimo kalendorius** skyriuje **Santrauka**.

## <a name="view-your-team-calendar-as-a-manager"></a>Peržiūrėkite komandos kalendorių kaip vadovas

1. Darbo srityje **Darbuotojo savitarna** pasirinkite **Mano komanda**.

2. Pasirinkite **Atostogos ar nebuvimas** ir tuomet pasirinkite **Peržiūrėti vadovo nebuvimo kalendorių**.

Vadovai taip pat gali turėti prieigą prie komandos kalendoriaus skirtukuose **Laukiami mano komandos atostogų prašymai**, **Patvirtintos atostogos** ir **Atostogų užklausos**. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Peržiūrėkite savo neatvykimų vadovo kalendorių kaip neatvykimo vadovas

> [!NOTE]
> Norėdami peržiūrėti neatvykimų vadovo kalendorių, pirmiausia turite įjungti funkciją **(Peržiūrėti) Neatvykimų vadovas atostogų valdymui** Funkcijų valdyme. Daugiau informacijos apie tai, kaip įjungti peržiūros funkcijas, rasite [Funkcijų valdymas](hr-admin-manage-features.md).

Vartotojai, turintys neatvykimų vadovo vaidmenį, gali peržiūrėti išleidimo iš darbo užklausas savo kalendoriuje. Atlikite toliau nurodytus veiksmus, jei norite pasiekti atostogų kalendorių.

1. Darbo srityje **Darbuotojo savitarna** pasirinkite **Atostogų valdymas**, o tada **Neatvykimų vadovo kalendorius**.

2. Lauke **Data** įveskite norimas datas.

3. Jei reikia, atnaujinkite rodinio parinktis.

Neatvykimų vadovo kalendoriuje rodomi visi darbuotojų, kurie yra atskaitingi neatvykimų vadovui, įrašai Atostogų hierarchijoje.

## <a name="view-a-company-calendar"></a>Peržiūrėti įmonės kalendorių

Žmonės, turintys „Human Resources“ vaidmenis, gali peržiūrėti įmonės kalendorius. Įmonės kalendoriuose rodomi visi darbuotojai. Pagal numatytuosius nustatymus kalendoriuje rodoma šiandienos data ir dar 28 dienos, bet galite keisti datų diapazoną. Taip pat galite filtruoti kalendorių pagal **pavadinimą**, **darbuotojo numerį** ir **atostogų tipą**.

1. Darbo srityje **Atostogos ir neatvykimai** pasirinkite **Saitai**.

2. Pasirinkite **Atostogų ir neatvykimų kalendorius**.

Turintys vaidmenį Personalas taip pat gali turėti prieigą prie įmonės kalendoriaus skirtukuose **Prašymai dėl atostogų ir leidimo neatvykti**, **Patvirtintos atostogos** ir **Atostogų užklausos**. 

Dabar kalendoriuose yra papildomi filtrai ir parinktys. Visuose kalendoriuose yra peržiūros parinktys, skirtos:

- Patvirtinti prašymai
- Laukiantys prašymai
- Darbuotojai, turintys atostogų prašymų
- Darbuotojai, neturintys atostogų prašymų
- Darbuotojų gimtadieniai
- Prašymus išleisti iš darbo 
- Prašymai dėl atostogų laiko

Kalendoriaus konfigūravimas **atostogų ir neatvykimų parametruose** nustato galimas peržiūros parinktis.

Taip pat galite filtruoti kalendorius pagal vadovą arba padalinį. Pagrindinis pareigų priskyrimas nustato darbuotojus, rodomus nustačius šiuos filtrus. 

> [!IMPORTANT]
> Galite įjungti funkciją **Visos įmonės atostogų rodinį** Funkcijų valdyme. Tada turite įjungti funkciją puslapyje **Žmogiškųjų išteklių bendrinti parametrai** tam, kad būtų rodomas juridinio asmens filtras kalendoriuose. Dėl daugiau informacijos, žr. [Konfigūruoti atostogų ir nebuvimo parametrus](hr-leave-and-absence-parameters.md).
> 
> Galite filtruoti kalendorių pagal juridinį asmenį. Tam, kad peržiūrėtumėte visus darbuotojus nepriklausomai nuo juridinio asmens, pašalinkite filtro lauką ir pasirinkite **Įvesti**. 

Informacijos apie kalendoriaus parametrus žr. skyriuje [Kalendoriaus parametrų konfigūravimas](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
