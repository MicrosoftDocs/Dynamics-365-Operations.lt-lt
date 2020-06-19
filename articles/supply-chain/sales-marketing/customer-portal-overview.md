---
title: „Dynamics 365 Supply Chain Management“ skirto kliento portalo apžvalga
description: Šioje temoje pristatomas kliento portalas ir paaiškinama, kas turėtų jį naudoti ir kaip jis veikia.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6b57365d8042c1d791ee2c50c5458a6595a58270
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413989"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>„Dynamics 365 Supply Chain Management“ skirto kliento portalo apžvalga

## <a name="what-is-the-customer-portal"></a>Kas yra kliento portalas?

Šiuolaikinės tiekimo grandinių sistemos yra priklausomos nuo integracijos. Joms svarbu, kad atsargų, klientų poreikių ir pardavimo padaliniai būtų integruoti, o ne atskirti vieni nuo kitų. Kliento portalas padeda organizacijoms, kurios naudoja „Microsoft Dynamics 365 Supply Chain Management“, pagerinti šią integraciją ir efektyviau informuoti klientus.

Kliento portalas yra [„Power Apps“ portalų](https://docs.microsoft.com/powerapps/maker/portals/overview) šablonas, kuris leidžia įmonėms sukurti išorinę „verslo verslui“ (B2B) svetainę su pardavimo užsakymų apdorojimu susijusiems atvejams. Šablone naudojamas [dvigubas rašymas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), „Supply Chain Management“ ir „Power Apps“ portalai, kad išoriniai įmonės klientai galėtų peržiūrėti ir kurti duomenis įmonės „Dynamics 365“ aplinkoje.

Kliento portalo šablonas turi visas tinkinimo galimybes, kurias siūlo „Power Apps“ portalų funkcija. Šabloną galima lengvai modifikuoti, kad būtų atstovaujamas įmonės prekės ženklas, pridėti daugiau funkcijų ir keisti vartotojo patirtį. Visas funkcijas, kurias šablonas turi iš karto, galima modifikuoti pagal poreikį.

> [!IMPORTANT]
> Nesitikima, kad šablonas pats savaime bus visiškai funkcionalus. Jis tik leidžia klientams sukurti išorinę svetainę, kad įmonės klientai galėtų pasiekti duomenis naudodami „Supply Chain Management“.

> [!NOTE]
> Kliento portalo dokumentacija yra skirta administratoriams, tinkintojams ir sistemos integratoriams, kurie nustatys „Supply Chain Management“ sistemos kliento portalą. Joje naudojami terminai _klientas_ir _vartotojas_, siekiant apibūdinti žmones, kurie yra „Supply Chain Management“ sistemą naudojančios organizacijos klientai ir kurie naudos galutinį portalą.

## <a name="who-should-use-it"></a>Kas turėtų jį naudoti?

Klientų portalas yra skirtas įmonėms, kurios naudoja „Supply Chain Management“ ir kurioms būdingos toliau išvardytos charakteristikos.

- Jos nori sukurti išorinę svetainę, kurioje įmonės klientams prieinama informacija apie užsakymo apdorojimą (pvz., užsakymo būsena ar sąskaitos informacija) tiesiai iš įmonės „Supply Chain Management“ sistemos.
- Įmonė pereina iš „Dynamics AX 2012“ į „Supply Chain Management“ ir anksčiau naudojo [AX 2012 klientų savitarnos portalą](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Toliau pateiktų tipų organizacijos **nėra** geros kandidatės įsidiegti kliento portalą.

- Įmonės, kurios nori sukurti svetainę ne įmonės klientams. Šios įmonės turėtų apsvarstyti galimybę susikurti [„Dynamics 365 Commerce“ elektroninės prekybos tinklalapį](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site).
- Įmonės, kurios jau naudoja „Power Apps“ portalų svetainę panašiu tikslu. Šios įmonės negaus jokios papildomos naudos iš kliento portalo. Kliento portalas pristatomas kaip šablonas, kuris veikia kaip vadovas ir pradinis taškas klientams, norintiems sujungti dvigubą rašymą, „Supply Chain Management“ ir Power Apps portalus. Jei jau turite šią paskirtį turinčią svetainę, gali būti nenaudinga naudoti kliento portalo šabloną tai svetainei pakartotinai parengti.

## <a name="how-does-it-work"></a>Kaip tai veikia?

Kliento portalas pateikiamas kaip „Power Apps“ portalų šablonas. Jis priklauso nuo „Power Apps“ portalų ir dvigubo rašymo.

[„Power Apps“ portalai](https://docs.microsoft.com/powerapps/maker/portals/overview) yra funkcija, kuri leidžia vartotojams sukurti išorinę svetainę, prie kurios gali prisijungti organizacijai nepriklausantys asmenys. Kuriant portalus nereikia arba beveik nereikia kodavimo. Kliento portalas yra vienas iš daugelio [„Dynamics 365“ portalų šablonų](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365), kuriuos teikia „Microsoft“.

[Dvigubas rašymas](https://docs.microsoft.com/powerapps/maker/portals/overview) yra parengtas naudoti infrastruktūros produktas, kuris beveik realiuoju laiku leidžia sąveiką tarp „Dynamics 365” esančių modeliu pagrįstų programų ir „Finance and Operations“ programų. Dvigubas rašymas suteikia dvikryptės integracijos tarp „Finance and Operations” programų ir „Common Data Service” galimybę. Todėl šis produktas suteikia integruotą vartotojo patirtį susietose programose. Kliento portalas priklauso nuo objektų, sinchronizuojamų naudojant dvigubą rašymą. Prieš naudojant „Supply Chain Management“ duomenis kliento portale, visiems atitinkamiems objektams reikia įjungti dvigubo rašymo funkciją.

![![Kliento portalo priklausomybes](media/customer-portal-elements.png "Kliento portalo priklausomybes")](media/customer-portal-elements.png "Customer portal dependencies")

Kliento portalas veikia kaip atspirties taškas organizacijoms, kurios nori naudotis „Power Apps“ portalais ir sukurti išorinę svetainę, naudojančią duomenis iš organizacijos „Supply Chain Management“ sistemos. Jis padeda organizacijoms sujungti dvigubo rašymo funkciją, „Supply Chain Management“ ir „Power Apps“ portalus.