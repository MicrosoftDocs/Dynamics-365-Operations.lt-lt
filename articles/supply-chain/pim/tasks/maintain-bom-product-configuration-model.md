---
title: Prižiūrėti produkto konfigūracijos modelio KS
description: Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bf4854b8c596abd45eb2cffd21cf03adff68982
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147646"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Prižiūrėti produkto konfigūracijos modelio KS

[!include [banner](../../includes/banner.md)]

Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis. Šiai procedūrai sukurti naudojamas demonstracinės įmonės USMF aukščiausios kokybės garsiakalbio modelis.


## <a name="add-a-bom-line"></a>Įtraukti KS eilutę
1. Spustelėkite Produkto varianto modelio aprašą.
2. Spustelėkite Produkto konfigūracijos modeliai.
3. Sąraše raskite ir pasirinkite norimą įrašą.
    * Šiai procedūrai pasirinkite aukščiausios kokybės garsiakalbį.  
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Išplėskite KS eilučių skyrių.
6. Spustelėkite Pridėti.
7. Lauke Pavadinimas surinkite reikšmę.
8. Lauke Aprašas įveskite reikšmę.
9. Spustelėkite Įrašyti.

## <a name="add-bom-line-details"></a>Įtraukti KS eilutės informaciją
1. Spustelėkite KS eilutės informacija.
2. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
    * Pvz., galite pasirinkti prekę M0055.  
    * Kiekvienai KS eilutės ypatybei galite pasirinkti, ar jai priskiriama fiksuota vertė, ar ji susieta su atributu.  
3. Pažymėkite žymės langelį Nustatyti.
4. Lauke Skaičiavimas pasirinkite Taip.
    * Skaičiavimo ypatybę nustačius į Taip, užtikrinama, kad KS eilutė bus įtraukta į išlaidų skaičiavimą.  
5. Spustelėkite skirtuką Nustatymas.
6. Pažymėkite žymės langelį Nustatyti.
7. Lauke Kiekis įveskite skaičių.
    * Kiekio laukas nustato, kiek yra prekės, kuri bus įtraukta į KS. Tai gali būti aiškus kandidatas į atributo susiejimą.  
8. Spustelėkite skirtuką Dimensija.
    * Patikrinkite, ar kuri nors prekės dimensija yra aktyvi, ir todėl privalo turėti priskirtą vertę arba atributą.  
9. Spustelėkite GERAI.

