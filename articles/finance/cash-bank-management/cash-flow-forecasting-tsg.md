---
title: Trikčių šalinimo grynųjų eigos prognozės nustatymai
description: Šiame straipsnyje pateikiami atsakymai į klausimus, kurie gali būti, kai konfigūruojate pinigų srautų prognozę. Jame aptariami dažnai užduodami klausimai (DUK) apie grynųjų eigos nustatymą, grynųjų eigos naujinimus ir grynųjų eigą „Power BI“.
author: angelad116
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 807a1da1906bdefec38954cea02ed29b0157d69e
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151408"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a>Trikčių šalinimo grynųjų eigos prognozės nustatymai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami atsakymai į klausimus, kurie gali būti, kai konfigūruojate pinigų srautų prognozę. Jame aptariami dažnai užduodami klausimai (DUK) apie grynųjų eigos nustatymą, grynųjų eigos naujinimus ir grynųjų eigą „Power BI“.

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a>Kodėl grynųjų eida yra rodoma tik vienam juridiniam asmeniui?

Grynų eigos prognozės konfigūruojama ir skaičiuojama vienam juridiniam asmeniu. „Power BI“ ataskaitos ir grynų eigos prognozės galimybės „Finance insights“ rodo rezultatus.

Grynųjų eigos prognozės turi būti nustatytas kiekvienam juridiniam asmeniui, kuriam norite matyti prognozę. Peržiūrėkite grynųjų eigos prognozės konfigūravimą visuose juridiniuose asmenyse. Kitu atveju, peržiūrėkite visų juridinių asmenų konfigūravimą grynų eigos prognozei ir įsitikinkite, kad jie yra nustatyti kaip norite.

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a>Kodėl „Power BI“ rodo visus darbo eigos duomenis?

Būtina atlikti kelis žingsnius prieš grynų eigos prognozes, kurios gali pasirodyti „Power BI“ rodiniuose. Peržiūrėkite tolesnį patikrų sąrašą ir įsitikinkite, kad kiekvienas žingsnis buvo atliktas:

- Nustatykite grynų eigą kiekvienam juridiniam asmeniui.
- Bendros sąskaitų knygos parametruose nustatykite sistemos valiutą ir sistemos keitimo kurso tipą.
- Nustatykite apskaitos knygos valiutą ir keitimo kurso tipą.
- Įveskite keitimo kursus tarp transakcijos valiutos ir apskaitos valiutos.
- Įveskite keitimo kursus tarp apskaitos valiutos ir sistemos valiutos.
- Įveskite keitimo kursus tarp apskaitos valiutos ir kiekvienos tuščios valiutos.

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a>Kodėl grynųjų eigos „Power BI“ veikia ankstesnėse versijose, o dabar yra tuščios?

Patikrinkite, ar „Grynųjų eigos matmuo V2" ir „LedgerCovLiquidityMeasurement" matmenys iš objekto parduotuvės buvo sukonfigūruoti. Daugiau informacijos apie tai, kaip dirbti su duomenimis įrašo saugykloje, žr. [„Power BI“ integravimas su objekto parduotuve](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Patikrinkite, ar atlikti visi veiksmai, kurie „Power BI“ būtini turiniui peržiūrėti. Daugiau informacijos žr. [„Power BI“ turinys Grynųjų pinigų apžvalga](Cash-Overview-Power-BI-content.md).

## <a name="have-the-entity-store-entities-been-refreshed"></a>Ar Objekto parduotuvės objektai buvo atnaujinti?

Turite periodiškai atnaujinti jūsų objektus siekiant užsitikrinti, kad duomenys būtų dabartiniai ir tikslūs. Norėdami rankiniu būdu atnaujinti konkretų objektą, eikite į **Sistemos administravimas \> Nustatymai \> Objekto parduotuvė**, rinkitės objektą ir tada **Naujinti**. Duomenys taip pat gali būti naujinami automatiniu būdu. Puslapyje **Objekto parduotuvė** nustatykite **Automatinis naujinimas įjungtas** parinktį į **Taip**.

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a>Kurį skaičiavimo metodą naudoti skaičiuojant pinigų srautų prognozes?

Pinigų srautų prognozės skaičiavimo metodas turi dvi svarbias pasirinkimo pasirinktis. Nauja pasirinktis apskaičiuos naujų dokumentų ir dokumentų, kurie pasikeitė po paskutinės paketinės užduoties **vykdymo**, pinigų srautų prognozes. Ši pasirinktis paleiskite greičiau, nes ji apdoroja mažesnį dokumentų pogrupį. Pasirinktis **Bendra** perskaičiuos kiekvieno sistemos dokumento pinigų srautų prognozes. Šiai pasirinktii atlikti reikia daugiau laiko, nes jai atlikti reikia daugiau darbo.

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a>Kaip pagerinti pasikartojančios paketinės užduoties pinigų srautų prognozavimo našumą?

Rekomenduojame kiekvieną dieną vykdyti savo pinigų srautų prognozę ne piko valandomis, naudojant **naują** skaičiavimo metodą. Mes patariame naudoti šį būdą šešias dienas per savaitę. Tada kiekvieną savaitę vykdyti pinigų srautų prognozę naudojant **bendrą** skaičiavimo metodą dieną, naudojant mažiausiai veiklos sumą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

