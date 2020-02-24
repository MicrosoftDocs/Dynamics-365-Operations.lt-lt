---
title: Bendrieji integruoto tiekėjo duomenys
description: Šioje temoje aprašomas tiekėjo duomenų integravimas tarp „Finance and Operations“ programų ir „Common Data Service“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019914"
---
# <a name="integrated-vendor-master"></a>Bendrieji integruoto tiekėjo duomenys

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Terminas *Tiekėjas* reiškia tiekėjo organizaciją arba įmonės savininką, kuris yra tiekimo grandinės proceso dalis ir kuris tiekia prekes verslui. Nors *tiekėjas* yra apibrėžta koncepcija „Finance and Operations“ programose, tiekėjo koncepcijos nėra kitose „Dynamics 365“ programose. Vietoje to kai kuriose įmonėse naudojamas paskyros objektas, skirtas saugoti kliento ir tiekėjo informaciją. Kitos įmonės naudoja pasirinktinę tiekėjo koncepciją. „Common Data Service“ integracija palaiko abu šiuos modelius. Todėl galima įjungti bet kurį modelį, atsižvelgiant į savo verslo scenarijų.

Tiekėjo duomenų integravimas tarp „Finance and Operations“ programų ir kitų „Dynamics 365” programų suteikia galimybę valdyti duomenis. Neatsižvelgiant į tiekėjo duomenų kilmę, jis integruojamas fone už programų ribų ir infrastruktūros skirtumų. 

### <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas

Jei tiekėjo valdymui norite naudoti kitas „Dynamics 365” programas ir pageidaujate atskirti tiekėjo informaciją nuo kliento informacijos, galite naudoti naująjį tiekėjo modelį.

![Tiekėjo duomenų srautas](media/dual-write-vendor-data-flow.png)

Jei tiekėjo valdymui norite naudoti kitas „Dynamics 365” programas ir pageidaujate toliau naudoti paskyros objektą tiekėjo informacijai saugoti, galite naudoti naująjį išplėstąjį tiekėjo modelį. Šiame modelyje išplėsta tiekėjo informacija, pvz., tiekėjų grupė ir tiekėjo registravimo profilis, saugoma tiekėjo informacijoje.

![Išplėstas tiekėjo duomenų srautas](media/dual-write-vendor-detail.jpg)

Tiekėjo kontaktinė informacija primena kliento kontaktinę informaciją. Fone kontaktinio asmens informacija saugoma ir gaunama iš tų pačių objektų.

## <a name="templates"></a>Šablonai

Tiekėjo duomenys apima visą informaciją apie tiekėją, pvz., tiekėjų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį. Objektų schemų rinkinys veikia kartu interaktyviai naudojant tiekėjų duomenis, kaip parodyta tolesnėje lentelėje.

„Finance and Operations” programėlės | Kitos „Dynamics 365” programos         | Aprašymas
----------------------------|---------------------------------|------------
V2 tiekėjas               | Paskyra | Įmonės, kurios naudoja paskyros objektą, kad galėtų saugoti tiekėjo informaciją, gali ir toliau jį naudoti tokiu pačiu būdu. Jos taip pat gali naudotis aiškiomis tiekėjo funkcijomis, kurios teikiamos pasitelkus „Finance and Operations“ programų integraciją.
V2 tiekėjas               | Msdyn\_vendors | Įmonės, kurios naudoja pasirinktinį sprendimą tiekėjams, gali pasinaudoti pradine tiekėjo koncepcija, kuri yra pristatyta „Common Data Service“ ir teikiama dėl „Finance and Operations“ programų integracijos. 
Tiekėjų grupės | msdyn_vendorgroups | Naudojant šį šabloną sinchronizuojama tiekėjų grupių informacija.
Tiekėjo mokėjimo būdas | msdyn_vendorpaymentmethods | Naudojant šį šabloną sinchronizuojama tiekėjų mokėjimo būdų informacija.
CDS kontaktai V2             | kontaktai                        | Naudojant [kontaktų](customer-mapping.md#cds-contacts-v2-to-contacts) šabloną sinchronizuojama visa tiek klientų, tiek tiekėjų pirminė, antrinė ir tretinė kontaktinė informacija.
Mokėjimo grafiko eilutės      | msdyn_paymentschedulelines      | Naudojant [mokėjimo grafiko eilučių](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) šabloną sinchronizuojami klientų ir tiekėjų nuorodos duomenys.
Mokėjimo grafikas            | msdyn_paymentschedules          | Naudojant [mokėjimo grafikų](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų nuorodos duomenys.
Mokėjimo dienos eilutės CDS V2    | msdyn_paymentdaylines           | Naudojant [mokėjimo dienos eilučių](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) šabloną sinchronizuojami klientų ir tiekėjų mokėjimo dienos eilučių nuorodos duomenys.
Mokėjimo dienos CDS            | msdyn_paymentdays               | Naudojant [mokėjimo dienų](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų nuorodos duomenys.
Mokėjimo sąlygos            | msdyn_paymentterms              | Naudojant [mokėjimo sąlygų](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo sąlygų nuorodos duomenys.
Pavadinimo afiksai                | msdyn_nameaffixes               | Naudojant [pavadinimų afiksų](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) šabloną sinchronizuojami tiek klientų, tiek tiekėjų pavadinimų afiksų nuorodos duomenys.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
