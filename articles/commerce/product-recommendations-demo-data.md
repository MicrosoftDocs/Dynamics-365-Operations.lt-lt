---
title: Rekomendacijų su demonstraciniais duomenimis kūrimas
description: Šioje temoje pateikiama patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 59b4dd7a29af739d92a20f6fe55eff9f201fcb6d
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454561"
---
# <a name="create-recommendations-with-demo-data"></a>Rekomendacijų su demonstraciniais duomenimis kūrimas

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.

Daugiakanalės produktų rekomendacijos pateikia atrinktų arba programiškai sugeneruotų produktų surikiuotą sąrašą. Šiuos sąrašus galima naudoti keliuose scenarijuose, atsižvelgiant į verslo poreikį. Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produktų rekomendacijų apžvalgoje](product-recommendations.md).

Antros ir aukštesnių pakopų „Dynamics 365“ aplinkose produktų rekomendacijos automatiškai apskaičiuojamos pagal kliento duomenis. Naudojant produktų rekomendacijų demonstracinius duomenis, produktų rekomendacijų sprendimas, kuris jau parengtas aplinkoje, ir išlaidos, susijusios su jo naudojimu, neišjungiamos.

Pirmos pakopos aplinkose produktų rekomendacijos yra paremtos tik statiniais demonstraciniais duomenimis, saugomais .csv faile.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Produktų rekomendacijų demonstracinių duomenų įgalinimas aplinkoje
Klientai turi įdiegti „Dynamics 365 Commerce“ peržiūros demonstracinį plėtinį į atitinkamą aplinką, automatiškai įgalinančiu produktų rekomendacijų demonstracinius duomenis. Tai atlikus automatiškai įgalinami produkto rekomendacijų demonstraciniai duomenys.

## <a name="default-demo-data"></a>Numatytieji demonstraciniai duomenys
Kiekvienoje „OneBox“ tipo aplinkoje yra iš anksto įkeltų produktų rekomendacijų rinkinys, skirtas demonstraciniams duomenims, saugomiems kableliu atskirtame „reco_demo_data.csv“ faile, esančiame „Commerce Scale Unit“.

Šie duomenys suskirstyti į šiuos stulpelius.

| Stulpelio pavadinimas         | Privalomas          | aprašymas                                                                                                                                 | Galimos reikšmės                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Konkretus produktų rekomendacijų sąrašo tipas, kurį turi sugeneruoti demonstracinių duomenų elementas.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Konkretus valdymo vieneto numeris, kuriame turėtų būti pateikiamos produktų rekomendacijos.                                        |                                                                              |
| Kategorija            |                    |    Kategorija, kuriai turėtų būti pateiktas konkretus sąrašas. Jei kategorija nenurodyta, sąrašas yra skirtas tik naršymo hierarchijos viršutinei daliai.    |                                                                              |
| SeedItemId          |                    |    Sąrašų, kuriuose reikia pateikti pirminę reikšmę (RecoPeopleAlsoBuy ir RecoCart), produktų sąraše turėtų būti rodomi papildomi produktai.            |                                                                              |
| Kliento ID          |                    |    Sąrašai, kuriems reikia kliento identifikatoriaus (RecoPicks).  Numatytoji vertė 0 taikoma visiems klientams.          |                                                                              |
| ItemIds             | :heavy_check_mark: | Vienas arba daugiau produktų, kuriuos dėl to reikia grąžinti, atskirti „;“.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Tinkinti demonstracinius duomenis
Galite redaguoti numatytuosius demonstracinius duomenis, naudodami bet kokią produkto ir kategorijos informaciją, sukonfigūruotą būstinėje. Atnaujinus .csv failą, klientams pateikiamose produktų rekomendacijose iš karto rodomi keitimai.

Plėtinyje yra duomenų failas, pavadintas „RecoMockDataset.csv“, kuriuo galite kontroliuoti duomenų rinkinį, naudojamą, norint gauti netikrus rekomendacijų rezultatus. Failo pavadinimą galima kontroliuoti naudojant plėtinio konfigūraciją ir parametrą **ext.Recommendations.DemoFilePath**. Tai jums leidžia turėti keletą duomenų rinkinių, kuriuos galima lengvai perjungti naudojant konfigūraciją.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[AI-ML rekomendacijų rezultatų koregavimas](modify-product-recommendation-results.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)
