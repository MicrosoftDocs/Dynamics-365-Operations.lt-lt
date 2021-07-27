---
title: Bendrieji integruoto tiekėjo duomenys
description: Šioje temoje aprašomas tiekėjo duomenų integravimas tarp „Finance and Operations“ programų ir „Dataverse“.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7e6ac62b2b289ef818a083b9ae4d1d74946ae3fc
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346501"
---
# <a name="integrated-vendor-master"></a>Bendrieji integruoto tiekėjo duomenys

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Terminas *tiekėjas* reiškia tiekėjų organizaciją arba individualų savininką, kuris tiekia prekes ar teikia paslaugas verslui. Nors *tiekėjas* yra nusistovėjusi „Microsoft Dynamics 365 Supply Chain Management“ sąvoka, „Dynamics 365“ modeliuose veikiančiose programose nėra tiekėjo sąvokos. Tačiau galite perkrauti lentelę **Paskyra / Kontaktai**, kad galėtumėte saugoti informaciją apie tiekėją. Integruotas tiekėjas pristato aiškią tiekėjo sąvoką modeliais paremtose programose, esančiose „Dynamics 365“. Galite naudoti naują tiekėjo dizainą arba saugoti tiekėjo duomenis lentelėje **Paskyra / Kontaktai**. Dvejopas rašymas palaiko abu būdus.

Abiem būdais tiekėjo duomenys yra integruoti tarp „Dynamics 365 Supply Chain Management“, „Dynamics 365 Sales“, „Dynamics 365 Field Service“ ir „Power Apps“ portalų. „Supply Chain Management“ yra duomenų apie tokias darbo eigas, kaip pirkimo paraiškos ir pirkimo užsakymai.

## <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas

Jei nenorite saugoti tiekėjo duomenų lentelėje **Paskyra / Kontaktai**, esančioje „Dataverse“, galite naudoti naują tiekėjo dizainą.

![Tiekėjo duomenų srautas.](media/dual-write-vendor-data-flow.png)

Jei norite ir toliau saugoti tiekėjo duomenis lentelėje **Paskyra / Kontaktai**, galite naudoti išplėstinį tiekėjo dizainą. Norėdami naudoti išplėstinį tiekėjo dizainą, turite sukonfigūruoti tiekėjo darbo eigas dvejopo rašymo sprendimų pakete. Daugiau informacijos rasite [„Tiekėjo dizaino keitimas“](vendor-switch.md).

![Išplėstas tiekėjo duomenų srautas.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Jei savitarnos paslaugų tiekėjams naudojate „Power Apps“ portalus, tiekėjo informacija gali būti tiesiogiai nukreipta į „Finance and Operations“ programas.

## <a name="templates"></a>Šablonai

Tiekėjo duomenys apima visą informaciją apie tiekėją, pvz., tiekėjų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį. Lentelių schemų rinkinys veikia kartu interaktyviai naudojant tiekėjų duomenis, kaip parodyta tolesnėje lentelėje.

„Finance and Operations” programėlės | Kitos „Dynamics 365” programos     | aprašymas
----------------------------|-----------------------------|------------
V2 tiekėjas                   | Paskyra                     | Įmonės, naudojančios Paskyros lentelę tiekėjo informacijai saugoti, gali ir toliau ją naudoti tokiu pačiu būdu. Jos taip pat gali naudotis aiškiomis tiekėjo funkcijomis, kurios teikiamos pasitelkus „Finance and Operations“ programų integraciją.
V2 tiekėjas                   | Msdyn\_vendors              | Įmonės, kurios naudoja pasirinktinį sprendimą tiekėjams, gali pasinaudoti pradine tiekėjo koncepcija, kuri yra pristatyta „Dataverse“ ir teikiama dėl „Finance and Operations“ programų integracijos. 
Tiekėjų grupės               | msdyn\_vendorgroups         | Naudojant šį šabloną sinchronizuojama tiekėjų grupių informacija.
Tiekėjo mokėjimo būdas       | msdyn\_vendorpaymentmethods | Naudojant šį šabloną sinchronizuojama tiekėjų mokėjimo būdų informacija.
CDS kontaktai V2             | kontaktai                    | Naudojant [kontaktų](customer-mapping.md#cds-contacts-v2-to-contacts) šabloną sinchronizuojama visa tiek klientų, tiek tiekėjų pirminė, antrinė ir tretinė kontaktinė informacija.
Mokėjimo grafiko eilutės      | msdyn\_paymentschedulelines | Naudojant [mokėjimo grafiko eilučių](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) šabloną sinchronizuojami klientų ir tiekėjų nuorodos duomenys.
Mokėjimo grafikas            | msdyn\_paymentschedules     | Naudojant [mokėjimo grafikų](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų nuorodos duomenys.
Mokėjimo dienos eilutės CDS V2    | msdyn\_paymentdaylines      | Naudojant [mokėjimo dienos eilučių](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) šabloną sinchronizuojami klientų ir tiekėjų mokėjimo dienos eilučių nuorodos duomenys.
Mokėjimo dienos CDS            | msdyn\_paymentdays          | Naudojant [mokėjimo dienų](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų nuorodos duomenys.
Mokėjimo sąlygos            | msdyn\_paymentterms         | Naudojant [mokėjimo sąlygų](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo sąlygų nuorodos duomenys.
Pavadinimo afiksai                | msdyn\_nameaffixes          | Naudojant [pavadinimų afiksų](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) šabloną sinchronizuojami tiek klientų, tiek tiekėjų pavadinimų afiksų nuorodos duomenys.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]