---
title: Integravimo su „Microsoft Dynamics 365 Field Service“ apžvalga
description: Šioje temoje pateikiama integravimo su „Microsoft Dynamics 365 Field Service“ apžvalga.
author: ChristianRytt
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1b1f88c77ed891839adb57c2ba5e2f72f35fda6d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998483"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Integravimo su „Microsoft Dynamics 365 Field Service“ apžvalga

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

„Supply Chain Management“ leidžia sinchronizuoti verslo procesus tarp „Dynamics 365 Supply Chain Management“ ir „Dynamics 365 Field Service“. Integravimo scenarijai sukonfigūruojami naudojant išplečiamuosius duomenų integratoriaus šablonus ir „Microsoft Dataverse“, kad būtų galima sinchronizuoti verslo procesus.
Standartiniai šablonai gali būti naudojami, siekiant sukurti pasirinktinius integravimo projektus, kuriuose papildomus standartinius ir pasirinktinius stulpelius bei lenteles būtų galima susieti norint pakoreguoti integravimą ir atitikti specifinius verslo reikalavimus. 

Vietinių aptarnavimo darbuotojų integracija remiasi esamomis kliento pavertimo pinigais funkcijomis.

![Verslo procesų sinchronizavimas tarp „Supply Chain Management“ ir „Field Service“](./media/field-service-integration.png)

Pirmasis integravimo tarp „Field Service“ ir „Supply Chain Management“ etapas orientuotas į darbo užsakymų ir sutarčių įgalinimą „Field Service“, kad „Supply Chain Management“ būtų galima išrašyti SF. Palaikomas srautas pradedamas „Field Service“, kai darbo užsakymų informacija su „Supply Chain Management“ būtų sinchronizuojama kaip pardavimo užsakymai. Dirbant su „Supply Chain Management“ išrašomos pardavimo užsakymų SF dokumentams generuoti. Be to, „Field Service“ pateikiama sutarčių SF informacija sinchronizuojama su „Supply Chain Management“. „Microsoft Dynamics 365“ duomenų integratorius sinchronizuoja duomenis panaudodamas pritaikomus projektus. Standartiniai šablonai gali būti naudojami, siekiant sukurti pasirinktinius integravimo projektus, kuriuose papildomus standartinius ir pasirinktinius stulpelius bei lenteles būtų galima susieti norint pakoreguoti integravimą ir atitikti specifinius reikalavimus.

Pirmame integravimo tarp „Field Service“ ir „Supply Chain Management“ etape galima sinchronizuoti toliau nurodytus elementus.

- [Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Field Service“ produktais](field-service-product.md)
- [„Field Service“ darbo užsakymų sinchronizavimas su „Supply Chain Management“ pardavimo užsakymais](field-service-work-order.md)
- [Sinchronizuokite „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF](field-service-invoice.md)

Norėdami pamatyti pavyzdį, kaip galima sinchronizuoti darbo užsakymą tarp „Field Service“ ir „Supply Chain Management“, peržiūrėkite trumpą „YouTube“ vaizdo įrašą [Kaip sinchronizuoti darbo užsakymą su „Microsoft Dynamics 365 Integration“](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integravimas su „Field Service“, įskaitant atsargų ir projekto informaciją

Papildomos funkcijos šiame antrajame etape skirtos suteikti vietiniams aptarnavimo darbuotojams įžvalgų apie atsargų informaciją iš „Supply Chain Management“, todėl jie gali atnaujinti atsargų lygius ir atlikti medžiagų perkėlimus. Be to, įmonės, montuojančios ar aptarnaujančios parduotas prekes, galės geriau kontroliuoti ir matyti visą pardavimo ir aptarnavimo procesą, naudodamosios projektų integracija.

### <a name="functionality-includes-integration-of"></a>Funkcijos apima šių aspektų integravimą:
- Sandėlių informacija
- Informacija apie turimas atsargas
- Atsargų perkėlimas
- Atsargų koregavimas
- „Supply Chain Management“ projektai, susiję su „Dynamics 365 Field Service“ darbo užsakymais
- „Dynamics 365 Field Service“ darbo užsakymai, su nuoroda į „Supply Chain Management“ projektus, naudoja šį projekto numerį pardavimo užsakymui, kad būtų galima išrašyti projekto SF. 

![Verslo procesų sinchronizavimas tarp „Supply Chain Management“ ir „Field Service“](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>Antrame integravimo tarp „Field Service“ ir „Supply Chain Management“ etape galima sinchronizuoti su toliau nurodytais šablonais:
- Sandėliai („Supply Chain Management“ su „Field Service“) – sandėliai iš „Supply Chain Management“ su „“Field Service [Išplėstinė užklausa] 
- Produkto atsargos („Supply Chain Management“ su „Field Service“) – produkto lygio informacija iš „Supply Chain Management“ su „“Field Service [Išplėstinė užklausa] 
- Atsargų koregavimas („Field Service“ su „Supply Chain Management“) – atsargų koregavimai iš „Field Service“ su „Supply Chain Management“ [Išplėstinė užklausa] 
- Atsargų perkėlimas („Field Service“ su „Supply Chain Management“) – atsargų perkėlimai iš „Field Service“ su „Supply Chain Management“ [Išplėstinė užklausa] 
- Projektai („Supply Chain Management“ su „Field Service“) – projektų sąrašas iš „Supply Chain Management“ su „Field Service“ 
- Darbo užsakymai su projektu („Field Service“ į „Supply Chain Management“) – darbo užsakymai, esantys „Field Service“ su pardavimo užsakymais, esančiais „Supply Chain Management“; palaikomas projektas [išplėstinė užklausa] 
- „Field Service“ produktai su atsargų vienetu („Supply Chain Management“ su „Sales“) – „Supply Chain Management“ „Parduotini išleisti produktai“ su pardavimo „produktais“, skirtais „Field Service“, įskaitant atsargų vienetą. 

## <a name="system-requirements"></a>Sistemos reikalavimai

### <a name="system-requirements-for-supply-chain-management"></a>„Supply Chain Management“ sistemos reikalavimai
„Field Service“ integravimas palaikomas toliau nurodytose versijose.

- „Dynamics 365 for Finance and Operations“ 8.1.2 versija (2018 m. gruodžio mėn.) išleista 2018 m. gruodį ir jos programos versijos numeris yra 8.1.195, o platformos atnaujinimas – 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>„Field Service“ sistemos reikalavimai
Norėdami naudoti sprendimą „Field Service“, turite įdiegti toliau nurodytus komponentus.

- „Field Service“ (8.2.0.286 versija) arba naujesnė versija programoje „Dynamics 365 9.1.x“ – išleista 2018 m. lapkričio mėn.
- „Dynamics 365“ skirtą sprendimą „Potencialūs klientai ir grynieji pinigai“ (P2C), 1.15.0.1 arba naujesnė versija. Sprendimą galima atsisiųsti iš [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- „Dynamics 365“ skirtas „Field Service“ integravimo, projekto ir atsargų sprendimas, 2.0.0.0 arba naujesnė versija. Sprendimą galima atsisiųsti iš [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]