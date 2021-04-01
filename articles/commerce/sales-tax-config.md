---
title: Konfigūruoti pardavimo mokesčius interneto užsakymams
description: Šioje temoje pateikta pardavimo mokesčių grupės parinkimo skirtingiems interneto užsakymų tipams apžvalga „Dynamics 365 Commerce“.
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 36dd3e8a3d47f02eed5b9c8bb79d773d98069376
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254846"
---
# <a name="configure-sales-tax-for-online-orders"></a>Konfigūruoti pardavimo mokesčius interneto užsakymams

[!include [banner](includes/banner.md)]

Šioje temoje pateikta pardavimo mokesčių grupės parinkimo skirtingiems interneto užsakymų tipams apžvalga. 

Jūsų e-komercijos kanalas gali palaikyti parinktis tokias kaip interneto užsakymų pristatymas ar paėmimas. Pardavimo mokesčių taikymas yra paremtas parinktimi, kurią pasirinko jūsų interneto vartotojai. Kai saito klientas pasirenka įsigyti prekę internetu ir gauna ją atsiųstą pasirinktu adresu, pardavimo mokesčiai yra nustatomi pagal siuntėjo siuntimo adreso mokesčių grupės nustatymus. Kai klientas pasirenka atsiimti įsigytą prekę iš parduotuvės, pardavimo mokesčiai yra nustatomi pagal paėmimo parduotuvės mokesčių grupės nustatymą. 

## <a name="orders-shipped-to-a-customer-address"></a>Užsakymai siųsti kliento adresu 

Bendrai, mokesčiai interneto užsakymams, kurie siunčiami kliento adresu yra nustatyti pagal paskirties vietą. Visos pardavimo mokesčių grupės turi mažmenos paskirties mokesčių tikslais konfigūravimą, kuriame jūsų verslas gali nustatyti paskirties vietos išsamią informaciją, tokią kaip šalis/regionas, valstija, valstybė ir miestas hierarchine tvarka. Padarius interneto užsakymą, „Commerce“ mokesčių variklis naudoja kiekvienos eilutės prekės užsakyme pristatymo adresą ir suranda pardavimo mokesčių grupes su atitinkančiais paskirties vietos pagrįstais mokesčių kriterijais. Pavyzdžiui, interneto užsakymui su eilutės prekės pristatymo adresu į San Franciską, Kaliforniją, mokesčių variklis suras pardavimo mokesčių grupę ir kodą Kalifornijai ir tada apskaičiuos mokesčiu kiekvienai eilutės prekei atitinkamai.  

## <a name="customer-based-tax-groups"></a>Klientu pagrįsta mokesčių grupė

„Commerce“ štabe, esama dviejų vietų, kuriose kliento mokesčio grupės yra sukonfigūruotos:

- **Kliento profilis**
- **Kliento siuntimo adresas**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Jei kliento profilis turi sukonfigūruotą mokesčių grupę

Kliento profilio įrašas štabe gali turėti sukonfigūruotą pardavimo mokesčių grupę, nepaisant to interneto užsakymams pardavimo mokesčių grupė sukonfigūruota kliento profilyje nebus naudojama mokesčių variklio. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Jei kliento siuntimo adresas turi sukonfigūruotą mokesčių grupę

Jei kliento siuntimo adreso įrašas turi kitą sukonfigūruotą mokesčių grupę ir interneto užsakymą (ar eilutės prekę) siunčiamą kliento siuntimo adresu, sukonfigūruota mokesčių grupė kliento adreso įraše bus naudojama mokesčių variklio mokesčių apskaičiavimui.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Konfigūruoti mokesčių grupę kliento siuntimo adreso įrašui

Norėdami Konfigūruoti mokesčių grupę kliento siuntimo adreso įrašui „Commerce“ štabe, atlikite šiuos žingsnius.

1. Eikite į **Visi klientai** ir tada rinkitės norimą klientą. 
1. „FastTab“ **Adresa** pasirinkite norimą adresą ir tada rinkitės **Daugiau parinkčių \> Papildomos**. 
1. Skirtuke **Bendri** puslapyje **Valdyti adresus**, nustatykite pardavimo mokesčių vertę, kaip būtina.

> [!NOTE]
> Mokesčių grupė yra nustatoma naudojant užsakymo eilutės pristatymo adresą ir paskirties vieta pagrįstus mokesčius, kurie sukonfigūruojami pačioje mokesčių grupėje. Dėl išsamesnės informacijos, žr. [Nustatyti mokesčius interneto parduotuvėms pagrįstoms paskirties vietoms](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Užsakymo atsiėmimas parduotuvėje

Užsakymo eilutėms su atsiėmimu parduotuvėje ar per langelį, bus taikoma mokesčių grupė iš pasirinktos atsiėmimo parduotuvės. Dėl informacijos apie tai, kaip konfigūruoti mokesčių grupę parinktai parduotuvei, žr. [Nustatyti kitas mokesčių parinktis parduotuvėms](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Kai užsakymo eilutė yra atsiimama parduotuvėje, kliento adreso mokesčių nustatymai (jei nustatyti) bus ignoruojami mokesčių variklio ir bus taikomi atsiėmimo parduotuvėje mokesčiai. 

## <a name="additional-resources"></a>Papildomi ištekliai

[PVM apžvalga](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[PVM skaičiavimo metodai lauke Kilmė](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ PVM priskyrimas ir perrašymai​](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[PVM kodų skaičiavimo parinktys Visa suma ir Intervalas](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Atleidimo nuo mokesčių skaičiavimas](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]