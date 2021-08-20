---
title: Prižiūrėti produkto konfigūracijos modelio KS
description: Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 173022d40a5c1354cbe05c171a8921e733d908d065b10889f9cbe0e87f3e98fa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781470"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a>Prižiūrėti produkto konfigūracijos modelio KS

[!include [banner](../../includes/banner.md)]

Norint paleisti šią procedūrą, reikalingas esamas produkto konfigūracijos modelis. Šiai procedūrai sukurti naudojamas demonstracinės įmonės USMF aukščiausios kokybės garsiakalbio modelis.

## <a name="add-a-bom-line"></a>Įtraukti KS eilutę

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Produkto konfigūracijos modeliai**.
1. Sąraše raskite ir pasirinkite norimą įrašą.
    * Šiai procedūrai pasirinkite aukščiausios kokybės garsiakalbį.  
1. Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.
1. Išplėskite **BOM eilučių** skyrių.
1. Pasirinkite **Įtraukti**.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Lauke **Aprašo laukas** surinkite reikšmę.
1. Pasirinkite **Įrašyti**.

## <a name="add-bom-line-details"></a>Įtraukti KS eilutės informaciją

1. Pasirinkite **BOM eilutės** informaciją.
2. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
    * Pvz., galite pasirinkti prekę M0055.  
    * Kiekvienai KS eilutės ypatybei galite pasirinkti, ar jai priskiriama fiksuota vertė, ar ji susieta su atributu.  
3. Pažymėkite **Nustatyti** laukelį.
4. Lauke *Skaičiavimas* pasirinkite **Taip**.
    * Skaičiavimo **ypatybę** nustačius į *Taip* užtikrinama, kad KS eilutė bus įtraukta į išlaidų skaičiavimą.  
5. Pasirinkite skirtuką **Nustatymas**.
6. Pažymėkite **Nustatyti** laukelį.
7. Lauke **Kiekis** įveskite skaičių.
    * Kiekio laukas nustato, kiek yra prekės, kuri bus įtraukta į KS. Tai gali būti aiškus kandidatas į atributo susiejimą.  
8. Pažymėkite skirtuką **Matmenys**.
    * Patikrinkite, ar kuri nors prekės dimensija yra aktyvi, ir todėl privalo turėti priskirtą vertę arba atributą.  
9. Pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]