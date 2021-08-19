---
title: Parengta mokėti
description: Šioje temoje parodyta, kaip pažymėti darbuotoją kaip paruoštą mokėti „Dynamics 365 Human Resources” programoje.
author: marcelbf
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 70b3f31db459fe021caf08fe09b2e44a597294d1992ee16a69efd8745941a4bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732422"
---
# <a name="ready-to-pay"></a>Parengta mokėti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Jei norite pažymėti darbuotoją kaip paruoštą mokėti, pirmiausia turite įgalinti funkciją **(Peržiūrėti) algalapio integravimą** Funkcijų valdyme. Daugiau informacijos apie peržiūros versijos funkcijų įjungimą žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).

Ši funkcija leidžia žmogiškųjų išteklių specialistams suprasti, kurie darbuotojai yra pasirengę algalapio apdorojimui ir kuriems reikia atlikti veiksmą prieš pateikiant juos trečiosios šalies algalapio teikėjui.

## <a name="mark-employee-as-ready-to-pay"></a>Pažymėti darbuotoją kaip pasirengusį mokėti

Darbuotojų informacijos rinkimas ir tikrinimas gali užimti daug laiko ir sukelti klaidų. Suteikdami galimybę žmogiškųjų išteklių specialistams peržiūrėti ir lengvai atnaujinti darbuotojų informaciją, „Dynamics 365 Human Resources” padeda sutrumpinti laiką, praleistą algalapio apdorojimo parengimui.

Norėdami pažymėti darbuotoją kaip pasirengusį mokėti:

1. Atidarykite **Kompensacijų valdymas**. Darbo srityje yra dvi plytelės 
    - **Darbuotojai pasirengę mokėti**
    - **Darbuotojai nepasirengę mokėti**
    ![Kompensacijų valdymo darbo sritis.](./media/hr-ready-to-pay-1-workspace.png)

2. Pasirinkite **Darbuotojai nepasirengę mokėti** plytelę.

3. Pasirinkite darbuotojus, kurie bus tikrinami. **Algalapio skirtuko** grupėje **Paruošta mokėti** pasirinkite **Tikrinti**.
    ![Darbuotojų patikrinimas.](./media/hr-ready-to-pay-2-validate.png)

4. Norėdami peržiūrėti rezultatus, **Algalapio skirtuko** grupėje **Paruošta mokėti** pasirinkite **Rezultatai**.

## <a name="validation"></a>Patikrinimas

Prieš pažymėdama darbuotoją kaip paruoštą mokėti, sistema atliks pagrindinį profilio užbaigimo patikrinimą.

![Patikrinkite rezultatus.](./media/hr-ready-to-pay-3-results.png)

Šioje lentelėje pateikiama informacija apie kiekvieną atliekamą patikrinimą. 

| Patikrinimas | Informacija |
| --- | --- |
| Adreso paskirties parametras | Patikrina, ar parametras **Naudoti algalapio adresų paskirtį** yra įjungtas. |
| Algalapio adresas | Patikrina, ar darbuotojo profilyje yra bent vienas adresas su paskirtimi „Algalapio gyvenamoji vieta” arba „Algalapio darbo vieta” ir tai, ar vienai paskirčiai yra tik vienas adresas. |
| Įdarbinimas | Patikrinkite, ar darbuotojas turi bent vieną įdarbinimą (dabartinį, ankstesnį ar būsimą). |
| Identifikavimo numeris | Patikrina, ar parametras „Naudoti identifikavimo tipus algalapio apdorojime” yra „taip” ir tai, ar parametre nurodytas identifikavimo tipas yra užpildytas darbuotojo profilyje. |
| Vardas ir pavardė | Patikrina, ar darbuotojo profilis yra tinkamas, tikrina, ar **Vardo** ir **Pavardės** laukai yra užpildyti.|
| Pozicija | Patikrinkite, ar darbuotojui yra priskirtos pareigos. |
| Gimimo data | Patikrina, ar darbuotojo profilis yra tinkamas, tikrina, ar **Gimtadienio** laukas yra užpildytas. |
| Kompensacija | Patikrinkite, ar darbuotojas yra įtrauktas į pastoviosios atlyginimo dalies planą. |

Jei nors vienas iš šių tikrinimų nepavyksta, negalite pažymėti darbuotojo kaip pasirengusio mokėti.

Jei laukas **Paruošta mokėti** yra **Ne**, tai reiškia, kad turite atlikti veiksmą, užtikrinantį darbuotojo profilio užbaigimą. Tai nesustabdys duomenų parodymo bet kuriame duomenų objekte. 

## <a name="known-issues"></a>Žinomos problemos

- Turite išjungti funkciją **Supaprastintas darbuotojo įrašas** Funkcijų valdyme. Plytelės kompensacijų valdymo darbo srityje neveiks tinkamai, jei naudosite šią funkciją.
- Darbuotojo formoje **Algalapio skirtuko** grupė **Paruošta mokėti** yra pasiekiama bet kuriam vartotojo vaidmeniui. 

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
