---
title: Prekių perkėlimo įmonės viduje perkėlimo dokumentų nustatymas
description: Šioje procedūroje parodoma, kaip nustatyti prekių perkėlimo įmonės viduje perdavimo dokumentus.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
ms.openlocfilehash: 333c5b5e5cfa25e705c9864542517f8ec5532dfe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282341"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>Prekių perkėlimo įmonės viduje perkėlimo dokumentų nustatymas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip kurti prekių perkėlimo įmonės viduje perdavimo dokumentus. Šią procedūrą gali atlikti tik juridiniai subjektai, kurių pagrindinis adresas yra Lietuvoje. Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kurios pirminis adresas yra Lietuvoje. Prieš baigdami šią procedūrą, turite atlikti procedūrą „Nustatyti prekių perkėlimo dokumentus įmonės viduje“. Ši procedūra skirta atsargų buhalteriams. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
