---
title: Balanso finansinės ataskaitos
description: Šiame straipsnyje aprašytos numatytosios balanso lapų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64e3624b387820bea3bfea9c2a4b2f48b0aa9822
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189026"
---
# <a name="balance-sheet-financial-reports"></a>Balanso finansinės ataskaitos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašytos numatytosios balanso lapų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai. 

## <a name="default-balance-sheet-reports"></a>Numatytosios balanso finansinės ataskaitos

Yra dvi numatytosios balanso ataskaitos. Vienoje ataskaitoje skyriai suspausti. Kitoje ataskaitoje skyriai yra vienas šalia kito.

| Numatytoji ataskaita                       | Kuo ji naudinga                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Balansas – numatyt.              | Pateikiamas organizacijos metų finansinės padėties rodinys.                                                                 |
| Sugretintas balansas – numatyt. | Pateikiamas organizacijos metų finansinės padėties rodinys. Turtas, įsipareigojimai ir akcininko kapitalas yra vienas šalia kito. |

## <a name="building-blocks"></a>Kūrimo blokai
Balanso finansinėse ataskaitose naudojami toliau nurodyti kūrimo blokai.

| Numatytoji ataskaita                       | Eilutės apibrėžimas                       | Stulpelio aprašas             |
|--------------------------------------|--------------------------------------|-------------------------------|
| Balansas – Numatytasis              | Balansas – Numatytasis              | Nuo šių metų pradžios ir nuokrypis – Numatytasis    |
| Sugretintas balansas – numatyt. | Sugretintas balansas – numatyt. | Stulpelis Nuo šių metų pradžios – Numatytasis |

### <a name="row-definition"></a>Eilutės apibrėžimas

Abiejų balanso ataskaitų eilučių apibrėžimuose pateikiami skyriai, skirti kiekvienai įprastinio balanso daliai. Ataskaitoje, kurioje duomenys nurodomi vienas šalia kito, pateikiamas stulpelio lūžis, kad įsipareigojimai ir savininko kapitalas būtų rodomi šalia turto. Pagrindinės sąskaitos kategorijos dimensija naudojama norint sukurti abiejų eilučių aprašus. Todėl bet kas gali generuoti ataskaitas, nes nereikia atlikti jokių pakeitimų.

### <a name="column-definition"></a>Stulpelio aprašas

Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, stulpelio aprašuose nurodomi skirtingi stulpelių tipai.

-   **Nuo šių metų pradžios ir nuokrypis – Numatytieji stulpelių tipai:**
    -   **DESC** – Eilutės apibrėžimo aprašymas
    -   **FD** – finansiniai duomenys nuo šių metų pradžios
    -   **FD** – finansiniai duomenys nuo praėjusių metų pradžios
    -   **CALC** – nuokrypis, gautas nuo šių metų atėmus praėjusius metus

<!-- -->

-   **Stulpelis Nuo šių metų pradžios – Numatytasis:**
    -   **DESC** – Eilutės apibrėžimo aprašymas
    -   **FD** – finansiniai duomenys nuo šių metų pradžios



## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinių ataskaitų apžvalga](financial-reporting-getting-started.md)

[Finansinių ataskaitų peržiūra](view-financial-reports.md)

[„Dynamics‟ Finansinių ataskaitų tinklaraštis](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]