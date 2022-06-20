---
title: Ilgalaikių išteklių įsigijimų siūlymas
description: Šiame straipsnyje aprašoma, kaip gauti ilgalaikį turtą naudojant įsigijimo pasiūlymą ilgalaikio turto žurnale.
author: moaamer
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35d2171dc828cb0227f310e81be1d3e3359f41c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909075"
---
# <a name="propose-fixed-asset-acquisitions"></a>Ilgalaikių išteklių įsigijimų siūlymas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip gauti ilgalaikį turtą naudojant įsigijimo pasiūlymą ilgalaikio turto žurnale. Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys. Siekiant gauti fiksuotą turtą per fiksuoto turto pasiūlymo žurnalą, pirmiausia turite sukurti fiksuoto turto įrašą ir tuomet nustatyti įsigijimo kainą turto knygoje.

## <a name="create-an-asset-acquisition-proposal"></a>Kurti turto įsigijimo pasiūlymą

Norėdami sukurti turto įsigijimo pasiūlymą atlikite šiuos veiksmus. 

1. Naršymo srityje eikite į **Moduliai > Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.
4. Veiksmų srityje pasirinkite **Eilutės**.
5. Pasirinkite **Pasiūlymai**.
6. Pasirinkite **Siūlymas įsigyti**. 
7. Pasirinkite **Filtras**. Spustelėkite **Nustatyti iš naujo**, kad išvalytumėte ankstesnes reikšmes.
8. Pasirinkite eilutę **Ilgalaikio turto numeris**.
9. Lauke **Kriterijai** įveskite arba pasirinkite reikšmę. Nustatykite likusius ilgalaikio turto, kurį norite įsigyti šiuo pasiūlymu, kriterijus.  
10. Norėdami išeiti iš srities, dukart pasirinkite **Gerai**.
- Patikrinkite, ar operacijų eilutės buvo sukurtos.  
- Įsigijimo pasiūlyme bus įtrauktas tik ilgalaikis turtas su knygoje nustatyta įsigijimo data ir įsigijimo kaina.  
11. Kurkite knygas puslapyje **Knygos**.
12. Pasirinkite **Registruoti**.

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>Įtraukti numatytąsias finansines dimensijas į įsigijimo pasiūlymą

Įsigijimo operaciją galima sukurti naudojant Excel papildinį, nueidami į Ilgalaikis turtas > Žurnalo įrašai **> Ilgalaikio turto** žurnalas. Sukurkite naują žurnalą ir perkelkite į puslapio skyrių Eilutės, pasirinkite **piktogramą** „Excel“, tada pasirinkite ilgalaikio turto žurnalo eilutę. Sistema sukurs ir atidarys „Excel“ šabloną, nurodantį žurnalo eilutes. Galite pridėti žurnalo eilučių, kurias įtraukiate į šabloną, duomenis ir paskelbti tą informaciją atgal į sistemą. 

Jei nustatytos pasirinktos turto knygos ir atitinkamo ilgalaikio turto, įvesto Excel šablone, numatytosios finansinės dimensijos bus iškviestos iš turto knygos pagrindinių duomenų, kai žurnalas publikuojamas iš „Excel“ į sistemą. Norint finansines dimensijas automatiškai įtraukti į turto knygą publikuojant ilgalaikio turto žurnalą iš „Excel" priedo, numatytosios dimensijos turi būti nustatytos iš anksto.  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
