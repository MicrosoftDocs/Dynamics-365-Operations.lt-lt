---
title: 'Išlaidų elementų kūrimas  '
description: Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779695"
---
# <a name="create-cost-elements"></a>Išlaidų elementų kūrimas   

[!include [banner](../../includes/banner.md)]

Kaštų apskaitoje išlaidų elementus galima kurti keliais būdais. Šioje procedūroje parodoma, kaip kurti išlaidų elementus importuojant pagrindines sąskaitas per duomenų jungtį. Kuriant šią procedūrą buvo naudojama demonstracinių duomenų įmonė USMF. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai kaštų apskaitos funkcijai aprašyti.


## <a name="create-new-cost-elements"></a>Naujų išlaidų elementų kūrimas
1. Pereikite į **kaštų apskaitos > dimensijų > Išlaidų elemento dimensijos**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** įveskite reikšmę.
4. **Dimensijos narių lauke duomenų jungtį** įveskite arba pasirinkite vertę.
5. Lauke **Aprašo laukas** surinkite reikšmę.
6. Spustelėkite **Įrašyti**.

## <a name="configure-the-data-connector"></a>Duomenų jungties konfigūravimas
1. Spustelėkite Konfigūruoti **dimensijos nario teikėją**.
2. **Sąskaitų plano lauke** įveskite arba pasirinkite vertę.
    * Pasirinkite Bendrai **naudojama** sąskaitų diagramai naudoti.  
3. Spustelėkite **Naujas**.
4. Sąraše pažymėkite pasirinktą eilutę.
    * Taikydami sąskaitų filtrus galite nustatyti savo kriterijus.  
5. **Lauke Iš pagrindinės sąskaitos** įveskite arba pasirinkite vertę.
6. Lauke Į **pagrindinę sąskaitą** įveskite arba pasirinkite vertę.
7. Spustelėkite **Gerai**.

## <a name="import-main-accounts"></a>Importuoti pagrindines sąskaitas
1. Spustelėkite **Importuoti dimensijos narius**.
    * Pagrindinės sąskaitos bus importuotos į savikainos apskaitą ir naudojamos kaip savikainos elementai.  
2. Spustelėkite **Gerai**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Peržiūrėkite importuotas sąskaitas kaip išlaidų elementus
1. Spustelėkite **Peržiūrėti dimensijos narius**.
    * Peržiūrėkite importuotas DK sąskaitas kaip savo verslo išlaidų elementus, į kuriuos galima perkelti išlaidas.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
