---
title: Bandomojo balanso finansinės ataskaitos
description: Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: kfend
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26d2ec261720499fc309a5fb850de2cb796bd8b
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802613"
---
# <a name="trial-balance-financial-reports"></a>Bandomojo balanso finansinės ataskaitos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašytos numatytosios bandomųjų balansų ataskaitos. Be to, jame aprašyti su šiomis ataskaitomis susieti kūrimo blokai ir ataskaitų modifikavimo pagal verslo poreikius būdai. 

## <a name="default-trial-balance-reports"></a>Numatytosios bandomojo balanso finansinės ataskaitos

Finansinėse ataskaitose galimos trys bandomojo balanso ataskaitos.

| Numatytoji ataskaita                                 | Kuo ji naudinga                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------|
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

> [!NOTE] 
> Vykdydami **Bandomojo balanso** ataskaitą „Financial reporting”, būtinai pasirinkite žymės langelius **Rodyti eilutes be sumų** ir **Rodyti ataskaitas be aktyvių eilučių**, esančius **Parametrų** skirtuke.

### <a name="row-definition"></a>Eilutės apibrėžimas

Eilutės apibrėžime Bandomasis balansas – numatytasis yra viena eilutė, į kurią įtrauktos visos pagrindinės sąskaitos. Todėl bet kas gali generuoti ataskaitą, nes nereikia atlikti jokių pakeitimų. Kai peržiūrite ataskaitą, detalizuojate vieną eilutę, kad pamatytumėte išsamią informaciją apie kiekvieną sąskaitą. Galite keisti eilutės apibrėžimą, kad į ją būtų įtraukta daugiau informacijos. Norėdami keisti eilutės Bandomasis balansas – Numatytasis apibrėžimą, kad į ją būtų įtrauktos visų sąskaitų eilutės, atlikite šiuos veiksmus.

1.  Spustelėkite **Redaguoti**, tada iš dimensijų **spustelėkite Įterpti eilutes**. Įterpimo **eilutės iš** dimensijų komandos leidžia pasirinkti dimensijas, kurios turėtų būti savo eilutės apibrėžime. Šiame eilutės apibrėžime ketinate naudoti pagrindinę **sąskaitą**.
2.  Įsitikinkite, **kad pagrindinėje** sąskaitoje yra visi ampers (>), tada spustelėkite **Gerai**.

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

## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinių ataskaitų apžvalga](financial-reporting-getting-started.md)

[Finansinių ataskaitų peržiūra](view-financial-reports.md)

[„Dynamics‟ Finansinių ataskaitų tinklaraštis](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
