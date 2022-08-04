---
title: Elektroniniai pranešimai
description: Šiame straipsnyje pateikta elektroninių pranešimų "365 Finance" apžvalga Microsoft Dynamics ir nustatymo informacija.
author: liza-golub
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4e765c6d56e0ab6d209c27a70fd4b7e52273c103
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069887"
---
# <a name="electronic-messaging"></a>Elektroniniai pranešimai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama elektroninių pranešimų **(EM) funkcijų** nustatymo informacija ir apžvalga.

Neseniai įvairių šalių ir regionų vyriausybės bei teisės aktų leidybos institucijos visame pasaulyje įvykdė tose šalyse ar regionuose registruotų įmonių ataskaitų teikimo reikalavimus. Reikalavimų tikslas – įgalinti gauti duomenis iš tų įmonių elektroniniu formatu tiesiogiai iš sistemų, kuriose jie buvo apskaičiuoti, saugomi ir apdoroti.

EM funkcijos Microsoft Dynamics programoje 365 Finansai palaiko įvairius procesus, siekiant užtikrinti finansų ir sistemų, kurios pateikia ataskaitas, teikia ir gauna oficialią informaciją, elektroninio sąveikos procesus.

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

## <a name="security-privileges"></a>Saugos teisės

Galimos šios elektroninių pranešimų saugos teisės.

| Saugos teisė           | Prieigos lygis | Susiejimas |
|------------------------------|--------------|-------------|
| Tvarkyti el. pranešimus | Ši teisė suteikia visą prieigą prie EM funkcijų. Jei turite šią teisę, galite nustatyti elektroninius pranešimus ir vykdyti visą apdorojimą. | Ši teisė yra įtraukta į **tvarkyti PVM operacijų saugos muito** mokestį. Paeiliui ši pareiga įtraukiama į **buhalterio** saugos vaidmenį. |
| Peržiūrėti el. pranešimus     | Ši teisė suteikia visą skaitymo prieigą prie EM funkcijų. Jei turite šią teisę, galite peržiūrėti elektroninius pranešimus ir nustatyti visą apdorojimą. Tačiau jūs negalite nustatyti ar vykdyti nieko. | Ši teisė yra įtraukta į **Gauti PVM operacijų operacijos būsenos** mokestį. Paeiliui ši pareiga įtraukiama į tokį saugos vaidmenį:<ul><li>Mokėjimų priežiūros vadovas</li><li>Gautinų sumų klerkas</li><li>Gautinų sumų vadovas</li><li>Mokesčių apskaitininkas</li><li>Buhalteris</li><li>Apskaitos vadovas</li><li>Apskaitos prižiūrėtojas</li><li>Pardavimo vadybininkas</li><li>Mokėtinų sumų klerkas</li></ul> |
| Valdyti el. pranešimus  | Ši teisė suteikia prieigą tik prie **elektroninių pranešimų** ir **elektroninių pranešimų elementų** puslapių. Jei turite šią teisę, galite vykdyti visą apdorojimą, kuris iškvievietas iš tų puslapių. | Ši teisė įtraukiama į elektroninių pranešimų **valdymo saugos pareigą**. Paeiliui ši pareiga įtraukiama į **Elektroninių pranešimų operatoriaus** saugos vaidmenį. |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Reguliavimo priemonės pagal šalį, palaikomos EM funkcijų

Toliau esančioje lentelėje pateikiama informacija apie kai kurias reguliavimo priemones pagal šalį, kurias palaiko EM funkcijos.

| Šalis     | Funkcijos pavadinimas | Bandomojo įrašymo funkcija |
|-------------|--------------|------------------------|
| Ispanija       | [Tiesioginis PVM informacijos tiekimas („Suministro Inmediato de Información del IVA”, SII)](../localizations/emea-esp-sii.md) | |
| Vengrija     | [Internetinė sąskaitų faktūrų išrašymo sistema](../localizations/emea-hun-online-invoicing.md) | |
| Jungtinė Karalystė | [Įrašų pavertimas skaitmeniniais(MTD) – PVM išrašo pateikimas](../localizations/emea-gbr-mtd-vat-integration.md) | [Finansai ir operacijos: JK skaitmeninis mokestis – PVM deklaracija "Dynamics 365"](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Lietuva   | [i.SAF ataskaitos](../localizations/emea-ltu-isaf.md) | |
| Lenkija      | [PVM deklaracija su registrais (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | ["Dynamics 365" finansai: JPEG/JPEGK PVM audito registrai](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Nyderlandai | [PVM deklaracija, skirta Nyderlandams](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Čekijos Respublika | [PVM deklaracija](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brazilija      | [„SPED-Reinf”](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rusija      | [PVM deklaracija](../localizations/rus-vat-declaration.md) | |
| Rusija      | [Apskaitos ataskaitos elektroniniu formatu](../localizations/rus-accounting-reporting.md) | |
| Rusija      | [Pelno mokesčio deklaracija](../localizations/rus-profit-tax-declaration.md) | |
| Rusija      | [Apskaičiuoto mokesčio deklaracija](../localizations/rus-assessed-tax-declaration.md) | |
| Rusija      | [Transporto mokesčio deklaracija](../localizations/rus-transport-tax-declaration.md) | |
| Rusija      | [Žemės mokesčio deklaracija](../localizations/rus-land-tax-declaration.md) | |
| Norvegija      | [PVM grąžinimas su tiesioginiu pateikimu „Altinn“](../localizations/emea-nor-vat-return.md) | [Naujas PVM grąžinimas su tiesioginiu pateikimu Alt alt alt į "Dynamics 365" finansus](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| Prancūzija      | [PVM deklaracija (Prancūzija)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| Austrija     | [PVM deklaracija (Austrija)](../localizations/emea-aut-vat-declaration-austria.md) | |
| Vokietija     | [PVM deklaracija (Vokietija)](../localizations/emea-deu-vat-declaration-germany.md) | |
| Nyderlandai | [PVM deklaracija, skirta Nyderlandams](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Švedija      | [PVM deklaracija (Švedija)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| Šveicarija | [PVM deklaracija (Šveicarija)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


