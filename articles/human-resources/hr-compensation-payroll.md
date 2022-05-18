---
title: Parengta mokėti
description: Šioje temoje parodyta, kaip pažymėti darbuotoją kaip paruoštą mokėti „Dynamics 365 Human Resources” programoje.
author: twheeloc
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 62d86de9c0ad6d6d7ee8375f7664f96e2a30783d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693814"
---
# <a name="ready-to-pay"></a>Parengta mokėti


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!NOTE]
> Jei norite pažymėti darbuotoją kaip paruoštą mokėti, pirmiausia turite įgalinti funkciją **(Peržiūrėti) algalapio integravimą** Funkcijų valdyme. Daugiau informacijos apie peržiūros versijos funkcijų įjungimą žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).

Ši funkcija leidžia žmogiškųjų išteklių specialistams suprasti, kurie darbuotojai yra pasirengę algalapio apdorojimui ir kuriems reikia atlikti veiksmą prieš pateikiant juos trečiosios šalies algalapio teikėjui.

## <a name="mark-employee-as-ready-to-pay"></a>Pažymėti darbuotoją kaip pasirengusį mokėti

Darbuotojų informacijos rinkimas ir tikrinimas gali užimti daug laiko ir sukelti klaidų. Suteikdami galimybę žmogiškųjų išteklių specialistams peržiūrėti ir lengvai atnaujinti darbuotojų informaciją, „Dynamics 365 Human Resources” padeda sutrumpinti laiką, praleistą algalapio apdorojimo parengimui.

Norėdami pažymėti darbuotoją kaip pasirengusį mokėti:

1. Atidarykite **Kompensacijų valdymas**. Darbo srityje yra dvi plytelės: 
    - **Darbuotojai pasirengę mokėti**
    - **Darbuotojai nepasirengę mokėti**
    ![Kompensacijų valdymo darbo sritis.](./media/hr-ready-to-pay-1-workspace.png)

2. Pasirinkite **Darbuotojai nepasirengę mokėti** plytelę.

3. Pasirinkite darbuotojus, kurie bus tikrinami. **Algalapio skirtuko** grupėje **Paruošta mokėti** pasirinkite **Tikrinti**.
    ![Darbuotojų patikrinimas.](./media/hr-ready-to-pay-2-validate.png)

4. Norėdami peržiūrėti rezultatus, **Algalapio skirtuko** grupėje **Paruošta mokėti** pasirinkite **Rezultatai**.

## <a name="validation"></a>Patikrinimas

Prieš pažymint darbuotoją kaip paruoštą mokėti, bus patikrintas darbuotojo profilio užbaigtumas.

![Patikrinkite rezultatus.](./media/hr-ready-to-pay-3-results.png)

| Patikrinimas | Informacija |
| --- | --- |
| **Adreso paskirties parametras** | Patvirtina, kad parametras **Naudoti algalapio adresų paskirtį** yra pasirinktas. |
| **Algalapio adresas** | Patvirtina, kad darbuotojo profilyje yra bent vienas adresas su paskirtimi **Algalapio gyvenamoji vieta** arba **Algalapio darbo vieta**, ir tai, ar vienai paskirčiai yra tik vienas adresas. |
| **Įdarbinimas** | Patvirtina, kad darbuotojas turi bent vieną įdarbinimą (dabartinį, ankstesnį ar būsimą). |
| **Identifikavimo numeris** | Patvirtina, kad laukas **Naudoti identifikavimo tipus algalapio apdorojime** nustatytas į **Taip** puslapyje **Žmogiškųjų išteklių parametrai** ir tai, ar parametre nurodytas identifikavimo tipas yra užpildytas darbuotojo profilyje. |
| **Vardas ir pavardė** | Patvirtina, kad užpildyti **Vardo** ir **Pavardės** laukai.|
| **Pozicija** | Patvirtina, kad darbuotojui yra priskirtos pareigos. |
| **Gimimo data** | Patvirtina, kad užpildytas **Gimtadienio** laukas. |
| **Kompensacija** | Patvirtina, kad darbuotojas yra įtrauktas į pastoviosios atlyginimo dalies planą. |

Jei nors vienas iš šių tikrinimų nepavyksta, negalite pažymėti darbuotojo kaip pasirengusio mokėti.

Jei laukas **Paruošta mokėti** yra **Ne**, tai reiškia, kad turite atlikti veiksmą, užtikrinantį darbuotojo profilio užbaigimą. Tai nesustabdys duomenų parodymo bet kuriame duomenų objekte. 

## <a name="process-automation"></a>Proceso automatizavimas

Galite automatizuoti visų darbuotojų tikrinimą naudodami [procesų automatizavimą](/dynamics365/fin-ops-core/dev-itpro/sysadmin/process-automation). Kompensavimo valdymo **darbo srityje** eikite į **Saitų**\> **parametrų** \>**procesų automatizavimas**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapių integravimo API įžanga](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
