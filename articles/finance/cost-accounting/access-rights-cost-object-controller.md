---
title: Savikainos objekto valdiklių prieigos teisės
description: Šiame straipsnyje pateikta informacija apie išlaidų objektų valdiklių prieigos teises.
author: AndersGirke
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c40be758c5e5d1d1fb025630ed8321ae46251892
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903195"
---
# <a name="access-rights-for-cost-object-controllers"></a>Savikainos objekto valdiklių prieigos teisės

[!include [banner](../includes/banner.md)]

Darbo sritis **Savikainos kontrolė** yra centrinis taškas, kuriame vadybininkai gali peržiūrėti savo savikainos objektų našumą. Naudodamiesi šia sritimi vadybininkai gali naudoti kaštų apskaitos duomenis net jei jie nėra išlaidų buhalterijai. Saugumo sumetimais vadybininkams turi būti leidžiama matyti tik tuos kaštų apskaitos duomenis, kurie yra susiję su konkrečiais savikainos objektais, už kuriuos jie atsakingi.

Yra keturi unikalūs kaštų apskaitos vaidmenys.

| Vaidmens pavadinimas               | Licencija      |
|-------------------------|--------------|
| Savikainos apskaitos vadovas | Veikla     |
| Išlaidų buhalteris         | „Operations‟   |
| Išlaidų apskaitininkas   | „Operations‟   |
| Savikainos objekto valdiklis  | Komandos nariai |

Šiame straipsnyje paaiškinama, kaip vadybininkui **priskirti išlaidų** objekto kontrolieriaus vaidmenį.

Kai vaidmuo **Savikainos objekto valdiklis** priskirtas vadybininkui, vadybininkas gali atlikti šias užduotis:

- Įjunkite darbo sritį **Savikainos kontrolė** (kliente).

    - Detalizuokite ir peržiūrėkite prieigą prie puslapių, palaikančių detalizavimo patirtį.

- Įjunkite darbo sritį **Savikainos kontrolė** (mobiliojoje programoje).

> [!NOTE]
> Vaidmuo **Savikainos objekto valdiklis** nekontroliuoja, kuriuos savikainos objektus gali įjungti vartotojas ir kurių duomenis jis gali peržiūrėti. Eilutės lygio sauga teikiama per dimensijų hierarchijas ir prieigos sąrašo hierarchiją.

## <a name="grant-access-rights"></a>Suteikti prieigos teises
Toliau pateiktame pavyzdyje parodyta, kaip gali atrodyti dimensijų hierarchija.

**Dimensijų hierarchijos informacija**

| Dimensijų hierarchijos pavadinimas | Dimensija    | Dimensijų hierarchijos tipo pavadinimas      | Prieigos sąrašo hierarchija |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organizacija             | Išlaidų centrai | Dimensijų klasifikavimo hierarchija | **Taip**               |

Naudodami „FastTab“ skirtuką **Vartotojai** hierarchijos dizaino įrankyje kiekviename mazge galite įterpti vieną ar kelis vartotojų ID.

|             Mazgai                 | Vartotojai            | Iš dimensijos nario     |   Į dimensijos narį   |
|-----------------------------------|------------------|---------------------------|-------------------------|
| Organizacija                      | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Administratorius                 | Balandžio            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finansai   | Alicia           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personalas        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Gamyba            | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Pakuotės | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Surinkimas  | Chris            | CC006                     | CC006                   |

> [!NOTE]
> Išlaidų buhalteriai turi būti priskirti aukščiausiam hierarchijos lygiui, kad galėtų matyti visus kaštų apskaitos įrašus.

Prieš taikant prieigos sąrašo hierarchiją ir jos saugos parametrus, puslapio **Savikainos apskaitos parametrai** (**Kaštų apskaita** > **Sąranka** > **Parametrai**) skirtuke **Bendra** turi būti nustatyta funkcijos **Įgalinti savikainos objekto dimensijos narių peržiūros prieigą** parinktis **Taip**.

Prieigos sąrašo hierarchijos parametrai naudojami norint valdyti toliau nurodytose srityse rodomus duomenis.

- **Savikainos kontrolės** darbo sritis (kliente):

    - Detalizavimui naudojamų puslapių duomenys

- **Savikainos kontrolės** darbo sritis (mobiliojoje programoje):

    - Likučiai kortelėse

- „Microsoft Power BI“:

    - Atliekant „Power BI“ vizualizavimą rodomi duomenys
    - Duomenų Power BI vizualizacijos, įdėtos į "Dynamics 365" finansų klientą

> [!IMPORTANT]
> - Tam, kad prieigos sąrašo hierarchija galėtų turėti įtakos „Power BI“, turi būti susieta prieigos sąrašo hierarchija ir „Power BI“ eilučių lygio sauga. Daugiau informacijos rasite dalyje [Kaštų apskaitos turinio paketo saugos nustatymas](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Šiame straipsnyje pateikiamos būtinosios sąlygos, kurios turi būti, kad būtų galima naudoti išlaidų **kontrolės darbo** sritį.

Papildomi ištekliai

- [Savikainos kontrolės darbo sritis](cost-control-workspace.md)
- [Dimensijų hierarchija](dimension-hierarchy.md)
- [Kaštų apskaitos turinio paketo saugos nustatymas](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
