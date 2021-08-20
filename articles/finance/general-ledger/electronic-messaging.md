---
title: Elektroniniai pranešimai
description: Šioje temoje pateikiama „ Microsoft Dynamics 365 Finance“ elektroninių pranešimų apžvalga ir nustatymo informacija.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 191abc37b7c349aaf3c9e871fe2f1885eec9fc896271d6fac27e5caa0b0fe3b0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768344"
---
# <a name="electronic-messaging"></a>Elektroniniai pranešimai

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama **Elektroninių pranešimų** (EM) apžvalga ir nustatymo informacija.

Neseniai įvairių šalių ir regionų vyriausybės bei teisės aktų leidybos institucijos visame pasaulyje įvykdė tose šalyse ar regionuose registruotų įmonių ataskaitų teikimo reikalavimus. Reikalavimų tikslas – įgalinti gauti duomenis iš tų įmonių elektroniniu formatu tiesiogiai iš sistemų, kuriose jie buvo apskaičiuoti, saugomi ir apdoroti.

EM funkcionalumas „Microsoft Dynamics 365 Finance” platformoje palaiko įvairius procesus vykdant elektroninę veiklą tarp „Finance“ ir sistemų, kurias vyriausybės ir teisės aktų leidybos institucijos siūlo ataskaitoms teikti bei oficialiai informacijai teikti ir gauti.

EM funkcija yra integruota į **Elektroninių ataskaitų** (ER) modulį. Elektroniniams pranešimams galite nustatyti ER formatus. Daugiau informacijos žr. [Elektroninės ataskaitos (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>Pagrindiniai EM funkcijų konceptai

EM funkcijos yra pagrįstos šiais objektais:

- **Elektroninis pranešimas** – ataskaita arba deklaracija, kuri turi būti pateikiama ar perduodama viduje, pavyzdžiui, ataskaita, siunčiama mokesčių inspekcijai.
- **Elektroninio pranešimo elementai** – įrašai, kurie turi būti įtraukti į pateikiamą pranešimą.
- **Elektroninių pranešimų apdorojimas** – veiksmų grandinė, kuri turi būti vykdoma norint surinkti reikiamus duomenis, generuoti ataskaitas, saugoti duomenis „Azure“ didelių dvejetainių objektų saugykloje, perduoti ataskaitas ne sistemoje, gauti atsakymus ne iš sistemos bei, remiantis gauta informacija, atnaujinti duomenų bazę. Grandinės veiksmai gali būti susieti arba atsieti.

Tolesnėje iliustracijoje pateiktas EM duomenų srautas.

![Elektroninių pranešimų duomenų srautas.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>Scenarijai, kuriuos palaiko EM funkcijos

Em funkcija palaiko toliau nurodytus scenarijus:

- Rankiniu būdu kurti pranešimus ir generuoti ataskaitas, grindžiamas susietais įvairių tipų ER eksportavimo formatais. Šie tipai yra „Microsoft Excel”, XML, „JavaScript”, objekto notacija (JSON), PDF, tekstas ir „Microsoft Word”.
- Automatiškai kurti ir apdoroti pranešimus, grindžiamus informacija, kurios buvo prašoma, ir informacija, gauta iš institucijos naudojant susietą ER importavimo formatą.
- Rinkti ir apdoroti informaciją iš duomenų šaltinio kaip pranešimo elementų. Duomenų šaltinis yra „Finance“ lentelė.
- Saugoti papildomą informaciją ir įvertinti įvairias vertes, iškviečiant konkrečiai apibrėžtas vykdomąsias klases, susijusias su pranešimais ar pranešimų elementais.
- Sujungti surinktą į pranešimo elementus informaciją, išskaidyti šią informaciją pagal pranešimą ir generuoti ataskaitas, kurios susietos ER eksportavimo formatais.
- Sugeneruotas ataskaitas perduoti žiniatinklio tarnybai naudojant saugos informaciją, saugomą „Azure“ raktų saugykloje.
- Gauti atsakymą iš žiniatinklio tarnybos, interpretuoti atsakymą ir atitinkamai atnaujinti „Finance“ duomenis.
- Saugoti ir peržiūrėti visas sugeneruotas ataskaitas.
- Saugoti ir peržiūrėti visą žurnalo informaciją, susijusią su veiksmais, vykdomais pranešimui ar pranešimo elementui.
- Valdyti apdorojimo procesą naudojant įvairias pranešimo ir pranešimo elementų būsenas.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Reguliavimo priemonės pagal šalį, palaikomos EM funkcijų

Toliau esančioje lentelėje pateikiama informacija apie kai kurias reguliavimo priemones pagal šalį, kurias palaiko EM funkcijos.

| Šalis     | Funkcijos pavadinimas | Bandomojo įrašymo funkcija |
|-------------|--------------|------------------------|
| Ispanija       | [Tiesioginis PVM informacijos tiekimas („Suministro Inmediato de Información del IVA”, SII)](../localizations/emea-esp-sii.md) | |
| Vengrija     | [Internetinė sąskaitų faktūrų išrašymo sistema](../localizations/emea-hun-online-invoicing.md) | |
| Jungtinė Karalystė | [Įrašų pavertimas skaitmeniniais(MTD) – PVM išrašo pateikimas](../localizations/emea-gbr-mtd-vat-integration.md) | [„Finance and Operations”: JK skaitmeninis mokestis – PVM deklaracija „Dynamics 365”](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Lietuva   | [i.SAF ataskaitos](../localizations/emea-ltu-isaf.md) | |
| Lenkija      | [PVM deklaracija su registrais (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [„Dynamics 365 Finance”: „SAF/JPK” PVM audito registrai](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nyderlandai | [PVM deklaracija, skirta Nyderlandams](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Čekijos Respublika | [PVM deklaracija](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brazilija      | [„SPED-Reinf”](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rusija      | [PVM deklaracija](../localizations/rus-vat-declaration.md) | |
| Rusija      | [Apskaitos ataskaitos elektroniniu formatu](../localizations/rus-accounting-reporting.md) | |
| Rusija      | [Pelno mokesčio deklaracija](../localizations/rus-profit-tax-declaration.md) | |
| Rusija      | [Apskaičiuoto mokesčio deklaracija](../localizations/rus-assessed-tax-declaration.md) | |
| Rusija      | [Transporto mokesčio deklaracija](../localizations/rus-transport-tax-declaration.md) | |
| Rusija      | [Žemės mokesčio deklaracija](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

