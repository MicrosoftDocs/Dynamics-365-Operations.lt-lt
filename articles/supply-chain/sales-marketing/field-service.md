---
title: Integravimas su „Microsoft Dynamics 365 for Field Service“
description: Šioje temoje pateikiama integravimo su „Microsoft Dynamics 365 for Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: efda4e39f63155785386ecec6d21973e01a0f69f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564030"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integravimas su „Microsoft Dynamics 365 for Field Service“

[!include[banner](../includes/banner.md)]

„Microsoft Dynamics 365 for Finance and Operations“ suteikia galimybę sinchronizuoti „Finance and Operations“ ir „Microsoft Dynamics 365 for Field Service“ verslo procesus. Integravimo scenarijai sukonfigūruojami naudojant išplečiamuosius duomenų integratoriaus šablonus ir „Common Data Service“ (CDS), kad būtų galima sinchronizuoti verslo procesus.
Standartiniai šablonai gali būti naudojami, siekiant sukurti pasirinktinius integravimo projektus, kuriuose papildomus standartinius ir pasirinktinius laukus bei objektus būtų galima susieti norint pakoreguoti integravimą ir atitikti specifinius verslo reikalavimus. 

Vietinių aptarnavimo darbuotojų integracija remiasi esamomis kliento pavertimo pinigais funkcijomis.

![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/field-service-integration.png)

Pirmasis integravimo tarp „Field Service“ ir „Finance and Operations“ etapas orientuotas į darbo užsakymų ir sutarčių įgalinimą „Field Service“, kad „Finance and Operations“ būtų galima išrašyti SF. Palaikomas srautas pradedamas „Field Service“, kai darbo užsakymų informacija su „Finance and Operations“ sinchronizuojama kaip pardavimo užsakymai. Programoje „Finance and Operations“ pardavimo užsakymams išrašomos SF, kad būtų sugeneruoti SF dokumentai. Be to, „Field Service“ pateikiama sutarčių SF informacija sinchronizuojama su „Finance and Operations“. „Microsoft Dynamics 365“ duomenų integratorius sinchronizuoja duomenis panaudodamas pritaikomus projektus. Standartiniai šablonai gali būti naudojami, siekiant sukurti pasirinktinius integravimo projektus, kuriuose papildomus standartinius ir pasirinktinius laukus bei objektus būtų galima susieti norint pakoreguoti integravimą ir atitikti specifinius reikalavimus.

Pirmame integravimo tarp „Field Service“ ir „Finance and Operations“ etape galima sinchronizuoti toliau nurodytus elementus elementus.

- [„Finance and Operations“ produktus su „Field Service“ produktais, kuriuose pateikiama produkto tipo informacija](field-service-product.md)
- [„Field Service“ darbo užsakymus su „Finance and Operations“ pardavimo užsakymais](field-service-work-order.md)
- [„Field Service“ SF su „Finance and Operations“ laisvos formos SF.](field-service-invoice.md)

Norėdami pamatyti pavyzdį, kaip galima sinchronizuoti darbo užsakymą tarp „Field Service“ ir „Finance and Operations“, peržiūrėkite trumpą „YouTube“ vaizdo įrašą [Kaip sinchronizuoti darbo užsakymą su „Microsoft Dynamics 365“ integravimu](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integravimas su „Microsoft Dynamics 365 for Field Service“, įskaitant atsargų ir projekto informaciją

Papildomos funkcijos šiame antrajame etape skirtos suteikti vietiniams aptarnavimo darbuotojams įžvalgų apie atsargų informaciją iš „Finance and Operations“, todėl jie gali atnaujinti atsargų lygius ir atlikti medžiagų perkėlimus. Be to, įmonės, montuojančios ar aptarnaujančios parduotas prekes, galės geriau kontroliuoti ir matyti visą pardavimo ir aptarnavimo procesą, naudodamosios projektų integracija.

### <a name="functionality-includes-integration-of"></a>Funkcijos apima šių aspektų integravimą:
- Sandėlių informacija
- Informacija apie turimas atsargas
- Atsargų perkėlimas
- Atsargų koregavimas
- „Dynamics 365 for Finance and Operations“ projektai, susieti su „Dynamics 365 for Field Service“ darbo užsakymais
- „Dynamics 365 for Field Service“ darbo užsakymai, nurodantys „Dynamics 365 for Finance and Operations“ projektus, taiko šį projekto numerį „Dynamics 365 for Finance and Operations“ pardavimo užsakymui, kad būtų galima išrašyti projekto SF. 

![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>Antrame integravimo tarp „Field Service“ ir „Finance and Operations“ etape galima sinchronizuoti su toliau nurodytais šablonais:
- Sandėliai („Fin and Ops“ su „Field Service“) – sandėliai iš „Finance and Operations“ su „Field Service“ [išplėstinės užklausos] 
- Produktų atsargos („Fin and Ops“ su „Field Service“) – atsargų lygio informacija iš „Finance and Operations“ su „Field Service“ [išplėstinės užklausos] 
- Atsargų koregavimas („Fin and Ops“ su „Field Service“) – atsargų koregavimas iš „Finance and Operations“ su „Field Service“ [išplėstinės užklausos] 
- Atsargų perkėlimas („Fin and Ops“ su „Field Service“) – atsargų perkėlimas iš „Finance and Operations“ su „Field Service“ [išplėstinės užklausos] 
- Projektai („Fin and Ops“ su „Field Service“) – projektų sąrašas iš „Finance and Operations“ su „Field Service“ 
- Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“) – darbo užsakymai, esantys „Field Service“ su pardavimo užsakymais, esančiais „Finance and Operations“; palaikomas projektas [išplėstinė užklausa] 
- „Field Service“ produktai su atsargų vienetu („Fin and Ops“ su „Sales“) – „Finance and Operations“ „Parduotini išleisti produktai“ su pardavimo produktais, skirtais „Field Service“, įskaitant atsargų vienetą. 

## <a name="system-requirements"></a>Sistemos reikalavimai

### <a name="system-requirements-for-finance-and-operations"></a>„Finance and Operations“ sistemos reikalavimai
„Field Service“ integravimas palaikomas toliau nurodytose versijose.

- „Dynamics 365 for Finance and Operations“ 8.1.2 versija (2018 m. gruodžio mėn.) išleista 2018 m. gruodį ir jos programos versijos numeris yra 8.1.195, o platformos atnaujinimas – 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>„Field Service“ sistemos reikalavimai
Norėdami naudoti sprendimą „Field Service“, turite įdiegti toliau nurodytus komponentus.

- „Field Service for Dynamics 365“ (8.2.0.286 versija) arba naujesnė versija programoje „Dynamics 365 9.1.x“ – išleista 2018 m. lapkričio mėn.
- „Dynamics 365“ skirtą sprendimą „Potencialūs klientai ir grynieji pinigai“ (P2C), 1.15.0.1 arba naujesnė versija. Sprendimą galima atsisiųsti iš [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- „Dynamics 365“ skirtas „Field Service“ integravimo, projekto ir atsargų sprendimas, 2.0.0.0 arba naujesnė versija. Sprendimą galima atsisiųsti iš [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).
