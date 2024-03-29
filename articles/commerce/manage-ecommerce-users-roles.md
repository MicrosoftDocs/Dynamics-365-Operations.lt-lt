---
title: Tvarkyti el. prekybos vartotojus ir vaidmenis
description: Šiame straipsnyje paaiškinama, kaip vartotojams suteikti prieigą prie jūsų svetainės kūrimo Microsoft Dynamics 365 Commerce aplinkos.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 180fc5c0a9c9e247d5bd6ec7f469f313463526df
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279508"
---
# <a name="manage-e-commerce-users-and-roles"></a>Tvarkyti el. prekybos vartotojus ir vaidmenis


[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip vartotojams suteikti prieigą prie jūsų svetainės kūrimo Microsoft Dynamics 365 Commerce aplinkos.

Siekiant padėti valdyti vartotojo prieigą ir suteikti vartotojams teisę atlikti konkrečias užduotis, svetainės kūrimo aplinkoje naudojamos saugos grupės, sukurtos tarnyboje „Microsoft Azure Active Directory“ („Azure AD“). Pirmiausia kūrimo aplinkoje kiekvienam vaidmeniui priskiriate naują arba esamą saugos grupę iš „Azure AD“. Tada suteikiate arba panaikinate teises atskiriems vartotojams įtraukdami šiuos vartotojus į reikiamą saugos grupę arba pašalindami juos iš saugos grupės.

## <a name="overview-of-roles-in-the-authoring-environment"></a>Kūrimo aplinkos vaidmenų apžvalga

„Dynamics 365 for Commerce“ kūrimo aplinkoje palaikomi šie vaidmenys.

| Vaidmuo                 | Aprašymas |
|----------------------|-------------|
| Sistemos administratorius | Vartotojai, turintys šį vaidmenį, turi visas teises visiems įrankiams bei visiems įvertinimams ir apžvalgoms. Jie taip pat gali kurti svetaines. |
| Administratorius   | Vartotojai, turintys šį vaidmenį, turi visas teises visiems įrankiams ir registravimo ir sprendimo paslaugai konkrečioje svetainės struktūroje. |
| Žiniatinklio svetainių kūrėjas         | Šiuos vaidmenis turintys vartotojai gali kurti puslapius, fragmentus ir šablonus, įkelti ir tvarkyti išteklius bei papildyti produktus ir kategorijas. |
| Skaitytojas               | Vartotojai, turintys šį vaidmenį, gali peržiūrėti puslapius, šablonus, išteklius, fragmentus, struktūras ir parametrus, bet negali nieko keisti. |
| Registravimo ir sprendimo moderatorius        | Vartotojai, turintys šį vaidmenį, gali moderuoti produktų apžvalgas. |

## <a name="system-administrator-role"></a>Sistemos administratoriaus vaidmuo

Kai sukonfigūruojate „Dynamics 365 Commerce“, esančią „Microsoft Dynamics“ „Lifecycle Services“ (LCS) aplinkoje, būsite paprašyti pateikti saugos grupę vaidmeniui **Sistemos administratorius**. Šis vaidmuo automatiškai taikomas visoms svetainėms, kurias kuriate konfigūruodami aplinką. Šio vaidmens saugos grupę galima atnaujinti tik LCS portale. Visų svetainių puslapyje **Svetainės administravimas** jis yra tik skaitomas ir skirtas tik informaciniams tikslams.

## <a name="administrator-role"></a>Administratoriaus vaidmuo

Kai sukuriate naują svetainę „Commerce“ programoje, būsite paprašyti pateikti saugos grupę vaidmeniui **Administratorius**. Norėdami peržiūrėti teises, kurias suteikia šis vaidmuo, žr. anksčiau šiame straipsnyje pateiktą lentelę.

## <a name="add-or-update-security-groups"></a>Saugos grupių įtraukimas arba naujinimas

Sukūrus svetainę, tik tie vartotojai, kurie yra saugos grupėse, susietose su vaidmenimis **Sistemos administratorius** ir **Administratorius**, gali turėti prieigą prie tos svetainės kūrimo aplinkos. Norėdami priskirti vartotojus vaidmenims **Žiniatinklio svetainės kūrėjas**, **Registravimo ir sprendimo moderatorius** ir **Skaitytojas**, turite priskirti saugos grupes šiems vaidmenims. Norėdami vaidmeniui pridėti saugos grupę arba atnaujinti saugos grupę, kuri šiuo metu priskirta vaidmeniui, atlikite šiuos veiksmus.

1. Eikite į svetainę, kurią norite atnaujinti.
1. Dalyje **Svetainės valdymas** atidarykite puslapį **Sauga**.
1. Pasirinkite vaidmenį, kurį norite modifikuoti.
1. Įtraukite saugos grupes į vaidmenis arba pašalinkite saugos grupes iš vaidmenų.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)

[Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei](search-engine-optimization-considerations.md)

[Tvarkyti turinio saugos strategiją (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
