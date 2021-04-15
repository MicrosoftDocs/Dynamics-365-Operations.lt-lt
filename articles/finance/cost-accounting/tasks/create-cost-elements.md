---
title: 'Išlaidų elementų kūrimas  '
description: Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c4c1e2aee7ba98c1cca378286afb643eaca1600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810083"
---
# <a name="create-cost-elements"></a>Išlaidų elementų kūrimas   

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]