---
title: Nustatyti TDS grupę, PAN ir TAN informaciją tiekėjams ir klientams
description: Šioje temoje aiškinama, kaip nustatyti informaciją apie grupę Išskaičiuotas mokestis pagal šaltinį (TDS), nuolatinės sąskaitos numerį (PAN) ir mokesčių sąskaitos numerį (TAN) tiekėjams ir pirkėjams.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f4add6d32c34993338b0e587723df12d0a33ce43
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358271"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Nustatyti TDS grupę, PAN ir TAN informaciją tiekėjams ir klientams

[!include [banner](../includes/banner.md)]

Šioje temoje aiškinama, kaip nustatyti informaciją apie grupę Išskaičiuotas mokestis pagal šaltinį (TDS), nuolatinės sąskaitos numerį (PAN) ir mokesčių sąskaitos numerį (TAN) tiekėjams ir pirkėjams.

1. Eikite į **Mokėtinos sumos \> Tiekėjai \> Visi tiekėjai** ar **Gautinų sumų \> pirkėjai \> Visi pirkėjai**.

    [![Puslapis Visi tiekėjai.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Veiksmų juostoje rinkitės **Naujas** norėdami sukurti tiekėją ar klientą ir įveskite reikiamą informaciją. Arba pasirinkite esamą tiekėją arba klientą.
3. „FastTab“ **Sąskaita ir pristatymas** esančiame **Mokesčio atskaičiavimas** skyriuje nustatykite **Skaičiuoti atskaitomą mokestį** parinktį į **Taip** tam, kad apskaičiuotumėte atskaičiuojamą mokestį TDS ar surinktą mokestį šaltinyje (TCS) tiekėjui ar klientui.
4. Pirkimo SF TDS apskaičiuojama pagal numatytąją TDS grupę, kuri nustatyta tiekėjui arba klientui. Lauke **TDS grupė** pasirinkite numatyta TDS grupė.

    > [!NOTE]
    > Kai pasirenkate TDS grupę **TDS grupės** laukelyje, **Atskaitomo mokesčio grupė** ir **TCS grupė** laukeliai tampa nebeprieinami.

5. „FastTab“ **Mokesčių informacija** skyriuje **PAN informacija** lauke **Būsena** pasirinkite tiekėjo arba pirkėjo nuolatinės sąskaitos numerio būseną:

    - **Nepasiekiama** – tiekėjas arba klientas neturi PAN.
    - **Gauta** – tiekėjas arba klientas turi PAN.
    - **Taikoma** – tiekėjas arba klientas kreipėsi dėl PAN.
    - **Netinkamas** – tiekėjas arba klientas turi PAN, bet jis negalioja.

6. Jei lauke **Būsena** pasirinkote **Gauta**, kad nurodytumėte, jog tiekėjas arba pirkėjas turi PAN, lauke įveskite PAN **numerį**. PAN turi sudaryti penki raidiniai simboliai, tada keturi skaitiniai simboliai, o tada vienas abėcėlinis simbolis. Toliau pateikiamas pavyzdys: **ABCDE1260A**.
7. Jei lauke **Taikoma** pasirinkote **Gauta**, kad nurodytumėte, jog tiekėjas arba pirkėjas taiko PAN numerį, įvedamas nuorodos numeris **Nuorodos numerio** laukelyje.
8. Lauke **Vertinamo produkto** pobūdis pasirinkite vertinamo kliento kategorijos, kuriai priklauso tiekėjas arba klientas, pobūdį:

    - Įmonė
    - HUF
    - Patvirtinti
    - Individualus
    - AOP
    - KKI
    - Vietos valdžia
    - Kita

    [![Mokesčių informacijos „FastTab“.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Tada, veiksmų juostoje **Tiekėjas** skirtuke, grupėje **Registracija** rinktiės **Registracijos ID** tam, kad atvertumėte **Valdyti adresus** puslapį.
10. Puslapio **Tvarkyti adresus** „FastTab“ **Mokesčių informacija** pasirinkite **Įtraukti** arba **Redaguoti,** kad atidarytumėte puslapį **Tvarkyti mokesčių informaciją**, kuriame galite tvarkyti mokesčių registracijos įrašą.
11. Puslapio **Tvarkyti mokesčių informaciją** „FastTab“ **Išskaitomas mokestis** lauke **Mokesčių sąskaitos numeris (TAN)** įveskite TAN. TAN turi sudaryti keturi raidiniai simboliai, tada penki skaitiniai simboliai, o tada vienas abėcėlinis simbolis. Toliau pateikiamas pavyzdys: **AFGH54821T**.
12. Uždarykite puslapį.
