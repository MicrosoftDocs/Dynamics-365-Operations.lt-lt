---
title: Juridinių subjektų ilgalaikio turto nusidėvėjimo skaičiavimas
description: Ilgalaikio turto nusidėvėjimą tarp juridinių subjektų galima vykdyti vienu veiksmu.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85a1e71967fb126be29a76a8a29ea5e4ae2b2199
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818469"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]