---
title: Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei
description: Šioje temoje aptariamos ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei, pradedant kūrimu, baigiant gamyba.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b35d0cb606e1b17a0258ea3fcb6287988d83091c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698216"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aptariamos ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei, pradedant kūrimu, baigiant gamyba.

## <a name="a-site-that-is-under-development"></a>Svetainė, kuri vis dar kuriama

Kai svetainė vis dar kuriama, visi svetainės puslapiai turėtų turėti metažymes **NOINDEX** ir **NOFOLLOW**, kad ieškos moduliai savo talpyklose neindeksuotų jūsų svetainės puslapių ir nesaugotų jos kūrimo versijų. Norint tai sukonfigūruoti, į svetainės puslapio šabloną reikia įtraukti numatytųjų metažymių modulį. Tada numatytųjų metažymių ypatybės bus pasiekiamos puslapio rengyklės SEO ypatybių dalyje. Galite naudoti šias ypatybes metažymėms tvarkyti.

## <a name="soft-launch-of-a-site"></a>Svetainės peržiūros versijos paleidimas

Paleidus svetainės peržiūros versiją svetainė pateikiama ribotai auditorijai arba rinkai prieš paleidžiant visą svetainę. Jei paleisite svetainės peržiūros versiją, turėtumėte palikti metažymes **NOINDEX**. Taip padėsite užtikrinti, kad peržiūros versija bus prieinama tik ribotai auditorijai, kurią norite pasiekti.

## <a name="a-site-that-is-in-production"></a>Svetainė, kuri yra gamybos etape

Kai svetainė yra gamybos etape, reikėtų įsitikinti, kad visi svetainės puslapiai yra teisingai pažymėti. „Microsoft Dynamics 365 Commerce“ naudoja puslapyje įvestą informaciją, kad tame puslapyje sugeneruotų visą SEO informaciją. Šias funkcijas turi šie moduliai: kategorijos puslapių suvestinė, sąrašo puslapių suvestinė ir produkto puslapių suvestinė.

Ieškos modulio indeksavimui optimizuoti generavimo sistema naudoja ir informaciją iš „Dynamics 365 Commerce“ konfigūruojamų SEO ypatybių, ir konkretaus modulio informaciją. Dėl svetainės, kuri yra gamybos etape, turėtumėte įsitikinti, kad failas robots. txt leidžia indeksuoti visą svetainę ir kad jame yra saitų į jūsų publikuotą svetainės struktūros dokumentą. Turėtumėte įjungti svetainės struktūros generavimo funkcijas dalyje **Svetainės parametrai \> Įjungta svetainės struktūra**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Puslapio SEO parametrai vidinei peržiūrai, ribotoms auditorijoms ir visoms auditorijoms

Kadangi „Dynamics 365 Commerce“ palaikomos „ką matau, tą gaunu“ (WYSIWYG) autentifikuotos peržiūros, autoriai gali paruošti savo puslapio turinį nesirūpindami dėl to, kad informacija gali tapti matoma svetainės lankytojams. Jei puslapis turi būti publikuojamas, bet jo matomumas turi būti apribotas, puslapis turi turėti metažymę **NOINDEX**, kad ieškos moduliai jo neindeksuotų. Tada, kai puslapis bus paruoštas visoms auditorijoms, turėtų būti visi pagrindiniai SEO metaduomenys, siekiant maksimaliai padidinti ieškos modulio indeksavimo efektyvumą. Be to, reikia pašalinti metažymę **NOLIMIT**.

## <a name="additional-resources"></a>Papildomi ištekliai

[El. prekybos vartotojų ir vaidmenų valdymas](manage-ecommerce-users-roles.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)

[Tvarkyti turinio saugos strategiją (CSP)](manage-csp.md)
