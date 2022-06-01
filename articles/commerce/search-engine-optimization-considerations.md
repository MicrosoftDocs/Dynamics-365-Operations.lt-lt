---
title: Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei
description: Šioje temoje aptariamos ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei, pradedant kūrimu, baigiant gamyba.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 2f90581766dba3d3a671df52ec08339a1a0fd7dc
ms.sourcegitcommit: 9dd2d32fc303023a509d58ec7b5935f89d1e9c6d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2022
ms.locfileid: "8806410"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei


[!include [banner](includes/banner.md)]

Šioje temoje aptariamos ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei, pradedant kūrimu, baigiant gamyba.

## <a name="a-site-that-is-under-development"></a>Svetainė, kuri vis dar kuriama

Norėdami užtikrinti, kad paieškos sistemos neindeksuos **kūrimo svetainės, visuose svetainės puslapiuose turėtų būti noindex** ir **"nofollow"** metaduomenų žymės. Geriausia sukurti fragmentą [, pagrįstą metatagų](metatags-module.md) moduliu, kuriame būtų šis metaduomenų žymės įrašas, ir užtikrinti, kad fragmentas būtų įtrauktas į visų jūsų svetainėje naudojamų šablonų HTML \<head\> skyrių.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Svetainės peržiūros versijos paleidimas

Paleidus svetainės peržiūros versiją svetainė pateikiama ribotai auditorijai arba rinkai prieš paleidžiant visą svetainę. Jei iš dalies paleidžiate savo svetainę, turėtumėte apsvarstyti galimybę **palikti noindex** metaduomenų žymes vietoje. Taip padėsite užtikrinti, kad peržiūros versija bus prieinama tik ribotai auditorijai, kurią norite pasiekti.

## <a name="a-site-that-is-in-production"></a>Svetainė, kuri yra gamybos etape

Kai svetainė yra gamybos etape, reikėtų įsitikinti, kad visi svetainės puslapiai yra teisingai pažymėti. „Microsoft Dynamics 365 Commerce“ naudoja puslapyje įvestą informaciją, kad tame puslapyje sugeneruotų visą SEO informaciją. Šias funkcijas turi šie moduliai: kategorijos puslapių suvestinė, sąrašo puslapių suvestinė ir produkto puslapių suvestinė.

Ieškos modulio indeksavimui optimizuoti generavimo sistema naudoja ir informaciją iš „Dynamics 365 Commerce“ konfigūruojamų SEO ypatybių, ir konkretaus modulio informaciją. Dėl svetainės, kuri yra gamybos etape, turėtumėte įsitikinti, kad failas robots. txt leidžia indeksuoti visą svetainę ir kad jame yra saitų į jūsų publikuotą svetainės struktūros dokumentą. Turėtumėte įjungti svetainės struktūros generavimo funkcijas dalyje **Svetainės parametrai \> Įjungta svetainės struktūra**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Puslapio SEO parametrai vidinei peržiūrai, ribotoms auditorijoms ir visoms auditorijoms

Kadangi „Dynamics 365 Commerce“ palaikomos „ką matote, tą ir gaunate“ (WYSIWYG) autentifikuotos peržiūros vizualinėje puslapio daryklėje, autoriai gali paruošti savo puslapio turinį nesirūpindami dėl to, kad informacija gali tapti matoma svetainės lankytojams. Jei puslapis turi būti publikuotas, bet jo poveikis turi būti ribotas, **jis turi turėti noindex** metaduomenų žymę, kad jo indeksuotų ieškos puslapiai. Tada, kai puslapis bus paruoštas visoms auditorijoms, turėtų būti visi pagrindiniai SEO metaduomenys, siekiant maksimaliai padidinti ieškos modulio indeksavimo efektyvumą. Be to, reikia **pašalinti** skyriklį metaduomenų žymę.

## <a name="additional-resources"></a>Papildomi ištekliai

[El. prekybos vartotojų ir vaidmenų valdymas](manage-ecommerce-users-roles.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)

[Tvarkyti turinio saugos strategiją (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
