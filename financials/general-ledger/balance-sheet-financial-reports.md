---
title: "Balanso finansinės ataskaitos"
description: "Šiame straipsnyje aprašytos numatytosios balanso lapų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 1e5d04c7baacab33c5a20a59aea8209f9c638aec
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="balance-sheet-financial-reports"></a>Balanso finansinės ataskaitos

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašytos numatytosios balanso lapų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai. 

<a name="default-balance-sheet-reports"></a>Numatytosios balanso finansinės ataskaitos
-----------------------------

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

 

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Finansinės ataskaitos](financial-reporting-getting-started.md)

[Peržiūrėti finansines ataskaitas](view-financial-reports.md)

[„Dynamics‟ Finansinių ataskaitų tinklaraštis](http://blogs.msdn.com/b/dynamics_financial_reporting/)




