---
title: Bendrieji integruoto tiekėjo duomenys
description: Šiame straipsnyje aprašomas tiekėjo duomenų integravimas tarp finansų ir operacijų programėlių ir Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a2c32ef546a5bc74e090591c0ac9d51529299041
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112209"
---
# <a name="integrated-vendor-master"></a>Bendrieji integruoto tiekėjo duomenys

[!include [banner](../../includes/banner.md)]



Terminas *tiekėjas* reiškia tiekėjų organizaciją arba individualų savininką, kuris tiekia prekes ar teikia paslaugas verslui. Nors *tiekėjas* yra nusistovėjusi „Microsoft Dynamics 365 Supply Chain Management“ sąvoka, „Customer Engagement“ programose nėra tiekėjo sąvokos. Tačiau galite perkrauti lentelę **Paskyra / Kontaktai**, kad galėtumėte saugoti informaciją apie tiekėją. Integruotas tiekėjas pristato aiškią tiekėjo sąvoką „Customer Engagement” programose. Galite naudoti naują tiekėjo dizainą arba saugoti tiekėjo duomenis lentelėje **Paskyra / Kontaktai**. Dvejopas rašymas palaiko abu būdus.

Abiem būdais tiekėjo duomenys yra integruoti tarp „Dynamics 365 Supply Chain Management“, „Dynamics 365 Sales“, „Dynamics 365 Field Service“ ir „Power Apps“ portalų. „Supply Chain Management“ yra duomenų apie tokias darbo eigas, kaip pirkimo paraiškos ir pirkimo užsakymai.

## <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas

Jei nenorite saugoti tiekėjo duomenų lentelėje **Paskyra / Kontaktai**, esančioje „Dataverse“, galite naudoti naują tiekėjo dizainą.

![Tiekėjo duomenų srautas.](media/dual-write-vendor-data-flow.png)

Jei norite ir toliau saugoti tiekėjo duomenis lentelėje **Paskyra / Kontaktai**, galite naudoti išplėstinį tiekėjo dizainą. Norėdami naudoti išplėstinį tiekėjo dizainą, turite sukonfigūruoti tiekėjo darbo eigas dvejopo rašymo sprendimų pakete. Daugiau informacijos rasite [„Tiekėjo dizaino keitimas“](vendor-switch.md).

![Išplėstas tiekėjo duomenų srautas.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Jei naudojatės savitarnos Power Apps tiekėjų portalais, tiekėjo informacija gali būti tiesiogiai skirta finansų ir operacijų programoms.

## <a name="templates"></a>Šablonai

Tiekėjo duomenys apima visą informaciją apie tiekėją, pvz., tiekėjų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį. Lentelių schemų rinkinys veikia kartu interaktyviai naudojant tiekėjų duomenis, kaip parodyta tolesnėje lentelėje.

„Finance and operations” programos | „Customer engagement“ programos     | Aprašas
----------------------------|-----------------------------|------------
[CDS kontaktai V2](mapping-reference.md#115) | kontaktai | Naudojant šį šabloną sinchronizuojama visa tiek klientų, tiek tiekėjų pirminė, antrinė ir tretinė kontaktinė informacija.
[Pavadinimo afiksai](mapping-reference.md#155) | msdyn_nameaffixes | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų pavadinimų afiksų nuorodos duomenys.
[Mokėjimo dienos eilutės CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų eilučių nuorodos duomenys.
[Mokėjimo dienos CDS](mapping-reference.md#158) | msdyn_paymentdays | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų nuorodos duomenys.
[Mokėjimo grafiko eilutės](mapping-reference.md#159) | msdyn_paymentschedulelines | Sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų eilučių nuorodos duomenys.
[Mokėjimo grafikas](mapping-reference.md#160) | msdyn_paymentschedules | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų nuorodos duomenys.
[Mokėjimo sąlygos](mapping-reference.md#161) | msdyn_paymentterms | Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo sąlygų nuorodos duomenys.
[Tiekėjai V2](mapping-reference.md#202) | msdyn_vendors | Įmonės, kurios naudoja pasirinktinį Dataverse sprendimą tiekėjams, gali pasinaudoti nedingo tiekėjo sąvoka, kuri įvedama dėl finansų ir operacijų programėlių integravimo.
[Tiekėjų grupės](mapping-reference.md#200) | msdyn_vendorgroups | Naudojant šį šabloną sinchronizuojama tiekėjų grupių informacija.
[Tiekėjo mokėjimo būdas](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Naudojant šį šabloną sinchronizuojama tiekėjų mokėjimo būdų informacija.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

