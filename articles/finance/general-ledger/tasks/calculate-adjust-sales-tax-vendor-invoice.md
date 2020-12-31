---
title: PVM tiekėjo sąskaitoje faktūroje skaičiavimas ir koregavimas
description: Šioje temoje aiškinama, kaip koreguoti PVM tiekėjo SF, esančioje Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03313d875d23489b3293376dd94f808c73a4bd15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445820"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>PVM tiekėjo sąskaitoje faktūroje skaičiavimas ir koregavimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip koreguoti PVM tiekėjo SF. Jei pradiniame šaltinio dokumente rodomos mokesčių sumos skiriasi nuo apskaičiuotų, šias sumas prieš registruodami galite koreguoti. Šioje užduotyje naudojama demonstracinė įmonė DEMF.

1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > SF > SF žurnalas**.
2. Pasirinkite **Naujas**.
3. Naujos eilutės lauke **Pavadinimas** pasirinkite išplečiamajame meniu esančią parinktį.
4. Veiksmų srityje pasirinkite **Eilutės**.
5. Lauke **Sąskaita** nustatykite norimas reikšmes.
6. Lauke **Sąskaita faktūra** įveskite reikšmę.
7. Lauke **Kreditas** įveskite skaičių.
8. Lauke **Korespondentinė sąskaita** nustatykite norimas reikšmes.
9. Pasirinkite **PVM**.
10. Lauke **Visa faktinė PVM suma** įveskite skaičių.
11. Skirtuke **Koregavimas** PVM sumas galima koreguoti pagal PVM kodą.
12. Pasirinkite **Iš naujo nustatyti faktinius dydžius pagal apskaičiuotas sumas**.
13. Pasirinkite **Gerai**.
14. Pasirinkite **Įrašyti**.

