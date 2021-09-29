---
title: 'LT-00003: generuoti ilgalaikio turto perkėlimo iš vieno sandėlio į kitą dokumentą'
description: Perkelkite ilgalaikį turtą iš vieno padalinio į kitą ir patvirtinkite perkėlimą su važtaraščiu.
author: anasyash
ms.date: 09/15/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VehicleModelTable_W, LtInvoiceAutoNumberingGroups, LtInvoiceAutonumberingTable, AssetWarehouseTransfer, HcmWorkerLookUp, SysQueryForm, LtAssetPackingSlip, TransportationDocument, LogisticsPostalAddressLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Lithuania
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e24feee33a963e4c3db0e30bc82c731c0bdf70b
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500261"
---
# <a name="lt-00003-generate-a-fixed-asset-transfer-between-warehouses-document"></a>LT-00003: generuoti ilgalaikio turto perkėlimo iš vieno sandėlio į kitą dokumentą

[!include [banner](../../includes/banner.md)]

Jei jūsų organizacijai reikia perkelti ilgalaikį turtą iš vieno padalinio į kitą ir du padaliniai nėra toje pačioje vietoje, perkėlimas turi būti patvirtintas važtaraščiu. Taip pat reikia generuoti perkėlimo važtaraštį pakeitus darbuotoją, atsakingą už ilgalaikio turto perdavimą. Priklausomai nuo įgalintų parametrų, važtaraštis gali būti numeruojamas automatiškai arba neautomatiniu būdu.

Ši procedūra taikoma tik Lietuvai skirtoms funkcijoms. 

Procedūra buvo sukurta naudojant demonstracinių duomenų įmonę USMF, todėl prieš pradedant reikia rankiniu būdu pakeisti USMF juridinio subjekto pirminį adresą į LTU. 

Ši procedūra skirta už ilgalaikį turtą atsakingiems buhalteriams.

## <a name="preset-vehicle-models"></a>Iš naujo nustatyti transporto priemonių modelius
1. Eikite į **Organizacijos administravimas** > **Nustatymas** > **Transporto priemonė** > **Transporto priemonių modeliai**.
2. Pasirinkite **Naujas** ir lauke **Modelis** įveskite reikšmę. Ši vertė bus spausdinama važtaraštyje.
3. Lauke **Aprašas** įveskite reikšmę ir pasirinkite **Įrašyti**.


## <a name="set-up-packing-slip-auto-numbering"></a>Nustatyti automatinį važtaraščio numeravimą
1. Eikite į **Organizacijos administravimas** > **Numeracijos** > **Skaitiklių valdymas**.
2. Pasirinkite **Redaguoti**.
3. Lauke **Modulis** pasirinkite parinktį.
4. Lauke **Sąskaitos kodas** pasirinkite parinktį.
5. Pasirinkite **Automatinis numeravimas** žymės langelį ir **Įrašyti**.
6. Eikite į **Organizacijos administravimas** > **Numeracijos** > **SF numeravimo nustatymas**.
7. Pasirinkite **Redaguoti**.
8. Lauke **Numeravimas** įveskite reikšmę.
9. Lauke **Modulis** pasirinkite parinktį.
10. Lauke **Numeracijos kodas** įveskite arba pasirinkite vertę. Jūsų pasirinkta numeracija turi būti naudojama automatiniam važtaraščio numeravimui.  
11. Lauke **Sąskaitos kodas** pasirinkite parinktį.
12. Pasirinkite **Tęsti** žymės langelį ir **Įrašyti**.


## <a name="generate-packing-slip"></a>Generuoti važtaraštį

### <a name="specify-transportation-details"></a>Nurodyti transportavimo informaciją
1. Eikite į **Ilgalaikis turtas** > **Užklausos ir ataskaitos** > **Važtaraščiai**.
2. Veiksmų srityje spustelėkite **Bendra**.
3. Pasirinkite **Transportavimo informacija**.
4. Pasirinkite **Redaguoti**.
5. Lauke **Spausdinti transportavimo informaciją** pasirinkite **Taip**. Transportavimo informacija, kurią galite nurodyti šiame puslapyje, bus atspausdinta važtaraštyje.  
6. Lauke **Išduotos prekės** įveskite arba pasirinkite vertę.
7. Lauke **Paketas** įveskite reikšmę.
8. Lauke **Vežėjo tipas** pasirinkite parinktį.
9. Lauke **Vežėjas** įveskite arba pasirinkite reikšmę.
10. Lauke **Modelis** įveskite arba pasirinkite reikšmę.
11. Lauke **Registracijos numeris** įveskite reikšmę.
12. Lauke **Priekabos registracijos numeris** įveskite vertę.
13. Lauke **Vairuotojas** įveskite arba pasirinkite reikšmę.
14. Lauke **Vairuotojo vardas ir pavardė** įveskite reikšmę.
15. Lauke **Pakrovimo data ir laikas** įveskite datą ir laiką.
16. Lauke **Pakrovimo adresas** įveskite arba pasirinkite reikšmę.
17. Pasirinkite **Įrašyti**. Baigę turto iškrovimo procesą, įveskite arba pasirinkite važtaraščio iškrovimo informaciją.  
18. Lauke **Iškrovimo data ir laikas** įveskite datą ir laiką.
19. Lauke **Iškrovimo adresas** įveskite arba pasirinkite reikšmę.
20. Pasirinkite **Išsaugoti** ir uždarykite puslapį.


### <a name="verify-the-packing-slip-report"></a>Patikrinti važtaraščio ataskaitą
1. Veiksmų srityje spustelėkite **Bendra**.
2. Pasirinkite **Ilgalaikio turto važtaraštis**.
3. Pasirinkite **Gerai**. Sugeneravus ataskaitą bus spausdinama visa transportavimo informacija.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
