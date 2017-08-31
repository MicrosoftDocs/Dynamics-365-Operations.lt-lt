---
title: "Bandomojo balanso finansinės ataskaitos"
description: "Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 86e8e91f2af474999d89bb63ac9e2afad7843c8a
ms.contentlocale: lt-lt
ms.lasthandoff: 06/13/2017

---

# <a name="trial-balance-financial-reports"></a>Bandomojo balanso finansinės ataskaitos

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai. 

<a name="default-trial-balance-reports"></a>Numatytosios bandomojo balanso finansinės ataskaitos
-----------------------------

„Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimo modulyje Finansinės ataskaitos pateikiamos trys bandomojo balanso ataskaitos.

| Numatytoji ataskaita                                 | Kuo ji naudinga                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Išsamus bandomasis balansas – numatyt.               | Joje pateikiama visų sąskaitų balanso informaciją ir debeto bei kredito balansai ir jų grynosios reikšmės, taip pat operacijos data, kvitas ir žurnalo aprašymas.                  |
| Bandomojo balanso suvestinė – numatyt.                | Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų grynasis skirtumas.                                        |
| Bandomojo balanso suvestinė metams bėgant – numatyt. | Pateikiama visų sąskaitų balanso informacija ir pradinis bei galutinis balansai, taip pat debeto ir kredito balansai ir jų šių ir praėjusių metų grynasis skirtumas. |

## <a name="building-blocks"></a>Kūrimo blokai
Bandomojo balanso finansinėse ataskaitose naudojami toliau nurodyti kūrimo blokai.

| Numatytoji ataskaita                                 | Eilutės apibrėžimas          | Stulpelio aprašas                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Išsamus bandomasis balansas – numatyt.               | Bandomasis balansas – Numatytasis | Išsamus bandomasis balansas – numatyt.               |
| Bandomojo balanso suvestinė – numatyt.                | Bandomasis balansas – Numatytasis | Bandomojo balanso suvestinė – Numatytoji                |
| Bandomojo balanso suvestinė metams bėgant – numatyt. | Bandomasis balansas – Numatytasis | Bandomojo balanso suvestinė metams bėgant – Numatytoji |

### <a name="row-definition"></a>Eilutės apibrėžimas

Eilutės apibrėžime Bandomasis balansas – numatytasis yra viena eilutė, į kurią įtrauktos visos pagrindinės sąskaitos. Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų. Kai peržiūrite ataskaitą, detalizuojate vieną eilutę, kad pamatytumėte išsamią informaciją apie kiekvieną sąskaitą. Galite keisti eilutės apibrėžimą, kad į ją būtų įtraukta daugiau informacijos. Norėdami keisti eilutės Bandomasis balansas – Numatytasis apibrėžimą, kad į ją būtų įtrauktos visų sąskaitų eilutės, atlikite šiuos veiksmus.

1.  Spustelėkite **Redaguoti**, tada spustelėkite **Įterpti eilutes iš dimensijų**. Komanda **Įterpti eilutes iš dimensijų** leidžia pasirinkti, kokias dimensijas norite turėti savo eilutės apibrėžime. Šiam eilutės apibrėžimui naudosite **Pagrindinė sąskaita**.
2.  Įsitikinkite, kad dalyje **Pagrindinė sąskaita** yra visi konjunkcijos ženklai (&), tada spustelėkite **Gerai**.

Dabar eilutės apibrėžime yra visos jūsų numatytojo juridinio subjekto pagrindinės sąskaitos.

### <a name="column-definition"></a>Stulpelio aprašas

Kiekvienoje bandomojo balanso ataskaitoje naudojamas kitas stulpelio aprašas. Norint pateikti skirtingus informacijos ir finansinių duomenų lygius, šiuose stulpelio aprašuose nurodomi skirtingi stulpelių tipai.

-   **Išsamus bandomasis balansas – Numatytieji stulpelių tipai:**
    -   **DESC** – Eilutės apibrėžimo aprašymas
    -   **ACCT** – Sąskaitų kodai
    -   **ATTR (3)** – Atributai:
        -   Operacijos data
        -   Kvitas
        -   Žurnalo aprašymas
    -   **FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas
    -   **FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas
    -   **CALC** – Grynasis skirtumas
-   **Bandomojo balanso suvestinė – Numatytieji stulpelių tipai:**
    -   **ACCT** – Sąskaitų kodai
    -   **DESC** – Eilutės apibrėžimo aprašymas
    -   **ATTR** – Atributas:
        -   Kvitas
    -   **FD** – Pradžios balanso finansiniai duomenys
    -   **FD** – Finansiniai duomenys, kuriuose pateikiamas tik debetas
    -   **FD** – Finansiniai duomenys, kuriuose pateikiamas tik kreditas
    -   **CALC** – Grynasis skirtumas
    -   **CALC** – Galutinis balansas
-   **Bandomojo balanso suvestinė metams bėgant – Numatytoji:**
    -   **ACCT** – Sąskaitų kodai
    -   **DESC** – Eilutės apibrėžimo aprašymas
    -   **ATTR** – Atributas
        -   Kvitas
    -   **FD** – Pradžios balanso šių metų finansiniai duomenys
    -   **FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų debetas
    -   **FD** – Finansiniai duomenys, kuriuose pateikiamas tik šių metų kreditas
    -   **CALC** – Grynasis skirtumas
    -   **CALC** – Galutinis balansas
    -   **FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų debetas
    -   **FD** – Finansiniai duomenys, kuriuose pateikiamas tik praėjusių metų kreditas

 

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Finansinės ataskaitos](financial-reporting-getting-started.md)

[Finansinių ataskaitų peržiūra](view-financial-reports.md)

[„Dynamics‟ Finansinių ataskaitų tinklaraštis](http://blogs.msdn.com/b/dynamics_financial_reporting/)




