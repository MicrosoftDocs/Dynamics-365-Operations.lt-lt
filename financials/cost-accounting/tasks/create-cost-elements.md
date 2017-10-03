--- 
title: "Išlaidų elementų kūrimas  "
description: "Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0b1045610881bc272798f1176fbca58731e5d43b
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-elements"></a>Išlaidų elementų kūrimas   

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais. Šioje procedūroje parodoma, kaip kurti išlaidų elementus importuojant pagrindines sąskaitas per duomenų jungtį. Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF. Ši procedūra yra skirta kaštų apskaitos funkcijai, įtrauktai į „Microsoft Dynamics 365 for Operations“ 1611 versiją.


## <a name="create-new-cost-elements"></a>Naujų išlaidų elementų kūrimas
1. Pasirinkite Kaštų apskaita > Dimensijos > Išlaidų elemento dimensijos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Dimensijos narių duomenų jungtis įveskite arba pasirinkite reikšmę.
5. Lauke Aprašas įveskite reikšmę.
6. Spustelėkite Įrašyti.

## <a name="configure-the-data-connector"></a>Duomenų jungties konfigūravimas
1. Spustelėkite Konfigūruoti dimensijos nario teikimo įrankį.
2. Lauke Sąskaitų planas įveskite arba pasirinkite reikšmę.
    * Pasirinkite Bendrai naudojamas, norėdami naudoti bendrai naudojamą sąskaitų planą.  
3. Spustelėkite Naujas.
4. Sąraše pažymėkite pasirinktą eilutę.
    * Taikydami sąskaitų filtrus galite nustatyti savo kriterijus.  
5. Lauke Iš pagrindinės sąskaitos įveskite arba pasirinkite reikšmę.
6. Lauke Į pagrindinę sąskaitą įveskite arba pasirinkite reikšmę.
7. Spustelėkite GERAI.

## <a name="import-main-accounts"></a>Importuoti pagrindines sąskaitas
1. Spustelėkite Importuoti dimensijos narius.
    * Pagrindinės sąskaitos bus importuotos į savikainos apskaitą ir naudojamos kaip savikainos elementai.  
2. Spustelėkite GERAI.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Peržiūrėkite importuotas sąskaitas kaip išlaidų elementus
1. Spustelėkite Peržiūrėti dimensijos narius.
    * Peržiūrėkite importuotas DK sąskaitas kaip savo verslo išlaidų elementus, į kuriuos galima perkelti išlaidas.  


