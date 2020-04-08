---
title: Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas
description: Ilgalaikio turto nusidėvėjimą tarp juridinių subjektų galima vykdyti vienu veiksmu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142920"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas

[!include [banner](../../includes/banner.md)]

Ilgalaikio turto nusidėvėjimą tarp juridinių subjektų galima vykdyti vienu veiksmu. Šioje procedūroje rodoma, kaip nustatyti ir vykdyti kelių juridinių subjektų procesą. Joje naudojamas vaidmuo Buhalteris ir USMF juridinio subjekto demonstraciniai duomenys.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Visos įmonės nusidėvėjimo vykdymo žurnalų nustatymas
1. Eikite į Ilgalaikis turtas > Nustatymas > Ilgalaikio turto parametrai.
2. Išplėskite ilgalaikio turto pasiūlymų skyrių.
3. Spustelėkite Pridėti.
4. Lauke Registravimo sluoksnis įveskite arba pasirinkite reikšmę.
5. Lauke Žurnalo pavadinimas įveskite arba pasirinkite reikšmę.
    * Žurnalo nustatymą pakartokite kiekvieno juridinio subjekto parametrų puslapyje Ilgalaikis turtas.  

## <a name="depreciation-run"></a>Nusidėvėjimo vykdymas
1. Pasirinkite Ilgalaikis turtas > Žurnalo įrašai > Kurti nusidėvėjimo pasiūlymą.
2. Lauke Registravimo sluoksnis įveskite arba pasirinkite reikšmę.
    * Pagal numatytąsias nuostatas, bus naudojamas ilgalaikio turto parametruose nurodytas žurnalo pavadinimas. Šioje parinktyje galima keisti kiekvieno esamo juridinio subjekto pavadinimą.  
3. Lauke Pabaigos data įveskite datą.
    * Pasirinkite juridinių subjektų, kurie bus įtraukti į nusidėvėjimo vykdymą.  
    * Sąraše bus rodomi tik ilgalaikio turto parametrų puslapyje pateikti ilgalaikio turto pasiūlymams nustatyti žurnalai.  
4. Lauke Registruoti žurnalus pasirinkite Taip.
    * Filtravimo laukai apima visą šiam nusidėvėjimo vykdymui pasirinktų juridinių subjektų ilgalaikį turtą, grupes ir knygas.  
    * Parinktis Paketinis vykdymas įgalinta pagal numatytuosius nustatymus. Kai ši parinktis įgalinta, nusidėvėjimo žurnalo kūrimas ir registravimas bus vykdomi fone.  
5. Spustelėkite Kurti žurnalą.
6. Eikite į Ilgalaikis turtas > Žurnalo įrašai > Ilgalaikio turto žurnalas.

