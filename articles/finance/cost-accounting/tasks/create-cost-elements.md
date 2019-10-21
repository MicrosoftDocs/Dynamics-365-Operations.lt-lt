---
title: 'Išlaidų elementų kūrimas  '
description: Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cceec1d52e1b5b2a05525c8d96f46dece17363b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187802"
---
# <a name="create-cost-elements"></a>Išlaidų elementų kūrimas   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais. Šioje procedūroje parodoma, kaip kurti išlaidų elementus importuojant pagrindines sąskaitas per duomenų jungtį. Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai kaštų apskaitos funkcijai aprašyti.


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
