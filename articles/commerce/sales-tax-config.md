---
title: Konfigūruoti PVM internetiniams užsakymams
description: Šioje temoje pateikta PVM grupės parinkimo skirtingiems interneto užsakymų tipams apžvalga „Dynamics 365 Commerce“.
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: fff4f39703a146412b460dacc3805fde097ab756
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021445"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigūruoti PVM internetiniams užsakymams

[!include [banner](includes/banner.md)]

Šioje temoje pateikta PVM pasirinkimo skirtingiems internetinių užsakymų tipams, naudojant paskirties vieta arba kliento paskyra pagrįstus mokesčių parametrus, apžvalga. 

Galbūt norėsite, kad jūsų e-komercijos kanalas palaikytų tokias parinktis, kaip interneto užsakymų pristatymas ar paėmimas. PVM taikymas yra paremtas parinktimi, kurią pasirinko jūsų internetiniai klientai. 

## <a name="destination-based-taxes-for-online-orders"></a>Paskirties vieta pagrįsti mokesčiai, taikomi internetiniams užsakymams

Bendrai, mokesčiai interneto užsakymams, kurie siunčiami kliento adresu yra nustatyti pagal paskirties vietą. Visos PVM grupės turi mažmeninę paskirties vieta pagrįstą konfigūraciją, kurioje jūsų verslas gali nustatyti paskirties vietos išsamią informaciją, tokią kaip šalis arba regionas, valstybė, valstija ir miestas hierarchine tvarka.

### <a name="orders-delivered-to-customer-address"></a>Užsakymai, pristatyti kliento adresu

Padarius internetinį užsakymą, „Commerce“ mokesčių variklis naudoja kiekvienos eilutės prekės užsakymo pristatymo adresą ir suranda PVM grupes su atitinkamais paskirties vieta pagrįstais mokesčių kriterijais. Pavyzdžiui, interneto užsakymui su eilutės prekės pristatymo adresu į San Franciską, Kaliforniją, mokesčių variklis suras PVM grupę ir kodą Kalifornijai ir tada apskaičiuos mokesčiu kiekvienai eilutės prekei atitinkamai.

### <a name="order-pick-up-in-store"></a>Užsakymų atsiėmimas parduotuvėje

Užsakymo eilutėms su nurodytu atsiėmimu parduotuvėje ar per langelį, bus taikoma mokesčių grupė iš pasirinktos atsiėmimo parduotuvės. Daugiau informacijos apie tai, kaip nustatyti PVM parinktai parduotuvei, rasite [Nustatyti kitas mokesčių parinktis parduotuvėms](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Kliento paskyra pagrįsti mokesčiai, taikomi internetiniams užsakymams

Gali būti toks verslo scenarijus, kuriame norėsite konfigūruoti PVM grupę konkrečiai kliento paskyrai „Commerce” būstinėje. Būstinėje yra dvi vietos, kuriose galite konfigūruoti PVM pagal kliento paskyrą. Norėdami jas pasiekti, pirmiausia turėsite pasiekti išsamios kliento informacijos puslapį eidami į **Mažmeninė prekyba ir komercija \> Klientai \> Visi klientai** ir tada pasirinkdami klientą.

Dvi vietos, kuriose galite konfigūruoti PVM pagal kliento paskyrą, yra:

- **PVM grupė**, esanti kliento išsamios informacijos puslapio „FastTab” **Sąskaita faktūra ir pristatymas**. 
- **PVM**, esanti puslapio **Tvarkyti adresus** „FastTab” **Bendra**. Norėdami nusigauti ten iš išsamios kliento informacijos puslapio, pasirinkite konkretų adresą iš „FastTab” **Adresai** ir tada pasirinkite **Išplėstiniai**.

> [!TIP]
> Jeigu internetiniams klientų užsakymams norite taikyti tik paskirties vieta pagrįstus mokesčius ir išvengti kliento paskyra pagrįstų mokesčių, įsitikinkite, kad laukas **PVM grupė** yra tuščias išsamios kliento informacijos puslapio „FastTab” **Sąskaita faktūra ir pristatymas**. Norėdami užtikrinti, kad nauji klientai, kurie registruojasi naudodami interneto kanalą, nepaveldėtų PVM grupės parametrų iš numatytųjų klientų ar klientų grupės parametrų, užtikrinkite, kad laukas **PVM grupė** taip pat būtų tuščias internetinio kanalo numatytiesiems kliento ir kliento grupės parametrams (**Mažmeninė prekyba ir komercija \> Klientai \> Klientų grupės**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Paskirties vieta arba kliento paskyra pagrįstų mokesčių taikomumo nustatymas 

Šioje lentelėje paaiškinama, ar internetiniams užsakymams taikomi mokesčiai yra pagrįsti paskirties vieta ar kliento paskyra. 

| Kliento tipas | Siuntimo adresas                   | Klientas > Sąskaita faktūra ir pristatymas > PVM grupė? | Kliento paskyros adresas būstinėje? | Kliento adresas > Išplėstiniai > Bendra > PVM grupė?                                              | Pritaikyta PVM grupė      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Svečias         | Manhatanas, NY                      | Ne (tuščia)                                                | Ne (tuščia)                              | Ne (tuščia)                                                                                                   | NY (paskirties vieta pagrįsti mokesčiai) |
| Prisijungta     | Ostinas, TX                          | Ne (tuščia)                                             | Taip                               | Nėra<br/><br/>Naujas adresas pridėtas per interneto kanalą.                                                            | TX (paskirties vieta pagrįsti mokesčiai) |
| Prisijungta     | San Fransiskas, CA (Atsiėmimas parduotuvėje) | Taip (NY)                                            | Netaikoma                              | Netaikoma                                                                                                    | CA (paskirties vieta pagrįsti mokesčiai) |
| Prisijungta     | Hiustonas, TX                         | Taip (NY)                                            | Taip                               | Taip (NY)<br/><br/>Naujas adresas pridėtas per interneto kanalą ir PVM grupė perimta iš kliento paskyros. | NY (kliento paskyra pagrįsti mokesčiai)  |
| Prisijungta     | Ostinas, TX                          | Taip (NY)                                            | Taip                               | Taip (NY)<br/><br/>Naujas adresas pridėtas per interneto kanalą ir PVM grupė perimta iš kliento paskyros. | NY (kliento paskyra pagrįsti mokesčiai)  |
| Prisijungta     | Sarasota, Fl                       | Taip (NY)                                            | Taip                               | Taip (WA)<br/><br/>Rankiniu būdu nustatyta į WA.                                                                          | WA (kliento paskyra pagrįsti mokesčiai)  |
| Prisijungta     | Sarasota, Fl                       | Ne (tuščia)                                                | Taip                               | Taip (WA)<br/><br/>Rankiniu būdu nustatyta į WA.                                                                          | WA (kliento paskyra pagrįsti mokesčiai)  |

## <a name="additional-resources"></a>Papildomi ištekliai

[Mokesčių nustatymas internetinėms parduotuvėms pagal vietą](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[PVM apžvalga](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[PVM skaičiavimo metodai lauke Kilmė](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[ PVM priskyrimas ir perrašymai​](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[PVM kodų skaičiavimo parinktys Visa suma ir Intervalas](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Atleidimo nuo mokesčių skaičiavimas](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]