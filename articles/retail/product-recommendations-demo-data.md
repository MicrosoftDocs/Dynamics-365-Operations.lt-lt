---
title: Daugiakanalių produktų rekomendacijų demonstraciniai duomenys
description: Šiuo dokumentu siekiama pateikti patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872331"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Daugiakanalių produktų rekomendacijų demonstraciniai duomenys

Šiuo dokumentu siekiama pateikti patarimų, kaip naudoti daugiakanales produktų rekomendacijas 1 pakopos vieno lauko aplinkose, naudojant iš anksto paruoštus, tinkinamus demonstracinius duomenis.

Daugiakanalės produktų rekomendacijos pateikia atrinktų arba programiškai sugeneruotų užsakytų produktų surikiuotą sąrašą. Šiuos sąrašus galima naudoti keliuose scenarijuose, atsižvelgiant į verslo poreikį. Daugiau informacijos apie produktų rekomendacijų sąrašus rasite [produkto rekomendacijų apžvalgoje.](../commerce/product-recommendations.md)

Antros ir aukštesnių pakopų „Dynamics“ aplinkose produktų rekomendacijos automatiškai apskaičiuojamos pagal kliento duomenis.
Naudojant produktų rekomendacijų demonstracinius duomenis, produktų rekomendacijų sprendimas, kuris jau parengtas aplinkoje, ir išlaidos, susijusios su jo naudojimu, neišjungiamos.

Pirmos pakopos aplinkose produktų rekomendacijos yra paremtos tik statiniais demonstraciniais duomenimis, saugomais CSV faile.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Produktų rekomendacijų demonstracinių duomenų įgalinimas aplinkoje

Klientai turi įdiegti **„Dynamics 365 Commerce“ peržiūros demonstracinį plėtinį** į atitinkamą aplinką, kuris automatiškai įgalina produktų rekomendacijų demonstracinius duomenis.

## <a name="default-demo-data"></a>Numatytieji demonstraciniai duomenys
Kiekviena „Onebox“ tipo aplinka pateikiama su iš anksto įkeltu produktų rekomendacijų demonstracinių duomenų rinkiniu, saugomu kableliais atskirtame faile **„reco_demo_data.csv“**, esančiame „Retail Server“, viename aplanke su šiuo dokumentu.

Šie duomenys suskirstyti į šiuos stulpelius

| Stulpelio pavadinimas         | Privalomas          | Aprašymas                                                                                                                                 | Galimos reikšmės                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Konkretus produktų rekomendacijų sąrašo tipas, kurį turi sugeneruoti demonstracinių duomenų elementas.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Konkretus valdymo vieneto numeris, kuriame turėtų būti pateikiamos produktų rekomendacijos.                                        |                                                                              |
| Kategorija            |                    |    Kategorija, kuriai turėtų būti pateiktas konkretus sąrašas. Jei kategorija nenurodyta, sąrašas yra skirtas tik naršymo hierarchijos viršutinei daliai.    |                                                                              |
| SeedItemId          |                    |    Sąrašų, kuriuose reikia pateikti pirminę reikšmę (RecoPeopleAlsoBuy ir RecoCart), produktų sąraše turėtų būti rodomi papildomi produktai.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Vienas arba daugiau produktų, kuriuos dėl to reikia grąžinti, atskirti **„;“**.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Tinkinti demonstracinius duomenis
Klientai gali redaguoti numatytuosius demonstracinius duomenis, naudodami bet kokią produkto ir kategorijos informaciją, sukonfigūruotą būstinėje. Atnaujinus CSV failą, klientams pateikiamose produktų rekomendacijose iš karto rodomi keitimai.

Plėtinyje yra duomenų failas, pavadintas RecoMockDataset.csv, kuri leidžia klientui kontroliuoti duomenų rinkinį, naudojamą, norint gauti netikrus rekomendacijų rezultatus. Failo pavadinimą galima kontroliuoti naudojant plėtinio konfigūraciją ir parametrą **ext.Recommendations.DemoFilePath**. Tai leidžia klientams turėti keletą duomenų rinkinių, kuriuos galima lengvai perjungti naudojant konfigūraciją.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](../commerce/product-recommendations.md)

[Aplinkos planavimas](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
