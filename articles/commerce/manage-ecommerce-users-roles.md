---
title: Tvarkyti el. prekybos vartotojus ir vaidmenis
description: Šioje temoje paaiškinama, kaip suteikti vartotojams prieigą prie „Microsoft Dynamics 365 Commerce“ svetainės kūrimo aplinkos.
author: bicyclingfool
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a1f9abae20d0f2e71790a3b27337338dc042b52
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003538"
---
# <a name="manage-e-commerce-users-and-roles"></a>Tvarkyti el. prekybos vartotojus ir vaidmenis


[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip suteikti vartotojams prieigą prie „Microsoft Dynamics 365 Commerce“ svetainės kūrimo aplinkos.

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

Kai sukuriate naują svetainę „Commerce“ programoje, būsite paprašyti pateikti saugos grupę vaidmeniui **Administratorius**. Žiūrėkite anksčiau šioje temoje pateiktą lentelę, kad peržiūrėtumėte teises, kurias teikia šis vaidmuo.

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
