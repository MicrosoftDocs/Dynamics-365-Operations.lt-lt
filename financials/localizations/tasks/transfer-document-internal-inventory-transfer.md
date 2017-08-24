--- 
title: "Atsargų perkėlimo įmonės viduje perkėlimo dokumentų generavimas"
description: "Šioje procedūroje parodoma, kaip kurti prekių perkėlimo įmonės viduje perdavimo dokumentus."
author: ShylaThompson
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0fe3d735d6309bf87047a27f9e68c579ca052012
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Atsargų perkėlimo įmonės viduje perkėlimo dokumentų generavimas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti prekių perkėlimo įmonės viduje perdavimo dokumentus. Šią procedūrą gali atlikti tik juridiniai subjektai, kurių pagrindinis adresas yra Lietuvoje. Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Lietuvoje. Prieš atlikdami šią procedūrą, turite atlikti procedūrą „Prekių perkėlimo įmonės viduje perdavimo dokumentų nustatymas“. Ši procedūra skirta atsargų buhalteriams. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="create-a-transfer-order"></a>Perdavimo užsakymo kūrimas
1. Pasirinkite Atsargų valdymas > Gaunami užsakymai > Perkėlimo užsakymas.
2. Spustelėkite Naujas.
3. Lauke Iš sandėlio įveskite arba pasirinkite vertę.
4. Lauke Į sandėlį įveskite arba pasirinkite vertę.
5. Spustelėkite Pridėti.
6. Sąraše pažymėkite pasirinktą eilutę.
7. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Perkėlimo užsakymo transportavimo informacijos įvedimas
1. Spustelėkite Įrašyti.
2. Veiksmų srityje spustelėkite Siųsti.
3. Spustelėkite Transportavimo informacija.
4. Lauke Spausdinti transportavimo informaciją pasirinkite Taip.
5. Lauke Išduotos prekės įveskite arba pasirinkite vertę.
6. Lauke Paketas įveskite reikšmę.
7. Lauke Krovinio pavojingumas įveskite reikšmę.
8. Lauke Vežėjas įveskite arba pasirinkite reikšmę.
9. Lauke Modelis įveskite arba pasirinkite reikšmę.
10. Lauke Registracijos numeris įveskite reikšmę.
11. Lauke Priekabos registracijos numeris įveskite vertę.
12. Lauke Vairuotojas įveskite arba pasirinkite reikšmę.
13. Lauke Vairuotojo vardas ir pavardė įveskite reikšmę.
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Neužregistruoto perkėlimo užsakymo važtaraščio peržiūra
1. Spustelėkite Važtaraštis.
2. Spustelėkite GERAI.
3. Uždarykite puslapį.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Užregistruoto perkėlimo užsakymo važtaraščio peržiūra
1. Veiksmų srityje spustelėkite Perkėlimo užsakymas.
2. Veiksmų srityje spustelėkite Siųsti.
3. Spustelėkite Siuntimo perkėlimo užsakymas.
4. Spustelėkite skirtuką Bendra.
5. Lauke Naujinti pasirinkite parinktį.
6. Spustelėkite skirtuką Peržiūra.
7. Lauke Važtaraštis surinkite reikšmę.
8. Spustelėkite GERAI.
9. Veiksmų srityje spustelėkite Siųsti.
10. Spustelėkite Važtaraštis.
11. Spustelėkite GERAI.

