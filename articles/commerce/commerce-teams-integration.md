---
title: „Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9289aca4f53eb2ae8f1fa06d5f80b7ee0bbab8e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908472"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga.

„Dynamics 365 Commerce” yra integruojama su „Teams” tam, kad padėtų klientams ir jų darbuotojams padidinti produktyvumą sinchronizuojant užduočių valdymą tarp dviejų programų. Vientisas užduočių valdymas, kurį suteikia „Commerce” ir „Teams” integravimas, leidžia parduotuvių vadovams ir darbuotojams kurti užduočių sąrašus, priskirti užduotis kelioms parduotuvėms ir sekti parduotuvių užduočių būseną iš bet kurios šių programų.

„Commerce” ir „Teams” integravimas prieinamas „Commerce” 10.0.18 versijos leidime.

## <a name="key-features"></a>Pagrindinės funkcijos

Štai keletas pagrindinių funkcijų, kurias suteikia „Commerce” ir „Microsoft Teams” integravimas:

- „Teams” konfigūravimas naudojantis gerai apibrėžta informacija iš „Commerce”, pavyzdžiui, organizacinė struktūra ir informacija apie parduotuves, darbuotojus, teises bei veiklos kontekstą.
- Lengvas vykstančių pakeitimų sinchronizavimas (pavyzdžiui, naujų parduotuvių pridėjimas arba naujų darbuotojų samdymas) tarp „Commerce” ir „Teams”, tačiau „Commerce” turi išlikti pagrindinis organizacinės struktūros duomenų šaltinis.
- Užduočių valdymo integravimas tarp „Commerce” ir „Teams” siekiant padėti parduotuvių darbuotojams, vadovams, regioninėms vadovams ir komunikacijos vadovams tvarkytis su užduočių valdymu iš bet kurios šių programų.

## <a name="prerequisites-for-using-integration-features"></a>Būtinosios integravimo funkcijų naudojimo sąlygos

Prieš pradėdami naudoti „Microsoft Teams” integravimo funkcijas, užtikrinkite šias būtinąsias sąlygas:

- „Microsoft 365 Business Standard” licenciją (Ši licencija apima „Teams”.)
- „Azure Active Directory” ( „Azure AD”) paskyras visiems parduotuvių vadovams ir darbuotojams
- Elektroninio kasos aparato (EKA) sistemas, sukonfigūruotas naudojant „Azure AD” autentifikavimą

## <a name="conceptual-architecture"></a>Koncepcinė architektūra

Šioje iliustracijoje pateikta koncepcinė „Dynamics 365 Commerce” ir „Microsoft Teams” integravimo architektūra, naudojanti San Fransisko parduotuvę kaip pavyzdį. Tiek „Teams”, tiek „Commerce” EKA programa naudoja „Microsoft Planner” kaip saugyklą, kad publikuotos užduotys iš „Teams” atsirastų EKA programoje, o specialiosios užduotys, sukurtos parduotuvių vadovų EKA programoje, atsirastų „Teams”, taip sukuriama vientisa užduočių valdymo patirtis tarp programų.    

![„Commerce” ir „Teams” integravimo architektūra](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas](enable-teams-integration.md)

[„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”](provision-teams-from-commerce.md)

[Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA](synchronize-tasks-teams-pos.md)

[Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje](manage-user-roles-teams.md)

[Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje](map-stores-existing-teams.md)

[„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK](teams-integration-faq.md)
