---
title: Neteisinga lauko vertė „TaxTrans“
description: Šioje temoje pateikiama informacija apie neteisingų „TaxTrans“ laukų verčių trikčių šalinimą.
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 5c1c034c6037d2e8920d9744903debebb2dc537f2644093d5e1eef66f2681191
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746349"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Neteisinga lauko vertė „TaxTrans“

[!include [banner](../includes/banner.md)]

Jei TaxTrans lauko vertė neteisinga, norėdami pabandyti išspręsti problemą naudokite šios **temos** informaciją.

## <a name="overview-of-values"></a>Verčių apžvalga
Šiame sąraše parodyta,  **kaip** „TaxTrans“ **TaxUncommitted** ir **TmpTaxWorkTrans yra panašūs** duomenų rinkiniai, tačiau veikia kitaip.

  - **TaxTrans** yra galutinis užregistruotas mokesčio operacijos rezultatas, išlieka duomenų bazėje.
  - **TaxUncommitted** yra tarpinis apskaičiuotas mokesčio rezultatas, išliekamas duomenų bazėje (jei taikoma), kuri bus naudojama vėliau registruojant.
  - **TmpTaxWorkTrans yra laikinas apskaičiuotas mokesčių rezultatas atminties lentelėje** (lentelės tipas = InMemory).

Jei radote neteisingo TaxTrans stulpelio šakninį priežastį, taip pat radote **neteisingo** TaxUncommitted **arba** **TmpTaxWorkTrans stulpelio šakninį** priežastį. Taip yra todėl, kad trys stulpeliai yra nukopijuoti vienas nuo kito.

Paprastai skaičiuojant mokesčius **sugeneruojamas TmpTaxWorkTrans,** tada, jei taikoma, **sugeneruojamas TaxUncommitted**. Registruojant mokesčius **sugeneruojamas** „TaxTrans“.


## <a name="add-breakpoints"></a>Įtraukti stabdos taškus
Norėdami įtraukti pertrūkio taškus, užbaikite tolesnius žingsnius: 

1. Įtraukite plėtinius ir stabdos taškus *įterpimo* () *ir atnaujinimo ()* plėtinius, kaip parodyta toliau.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Arba galite tiesiogiai pridėti stabdos taškus, kai **TaxUncommitted** neįtraukta.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Perkurti ir derinti

Nustačius stabdos taškus, derinant visi duomenų pastovumo pokyčiai matomi. Norėdami rasti neteisingo **TaxTrans**, **TaxUncommitted arba** **TmpTaxWorkTrans** stulpelio šakninį priežastį, peržiūrėkite ir atkreipkite dėmesį į šiuos elementus:

- Paskutinis stabdos taškas, kuriame stulpelis teisingas.
- Pirmasis stabdos taškas, kuriame stulpelis neteisingas.
- Kas atsitinka tarp šių dviejų taškų.

## <a name="determine-whether-customization-exists"></a>Nustatyti, ar yra tinkinimas
Jei atlikote veiksmus ankstesniuose skyriuose, bet negalėjote išspręsti problemos, nustatykite, ar yra tinkinimas. Jei tinkinimo nėra, pagalbos kreipkitės į "Microsoft" palaikymo tarnybą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

