---
title: SF fiksavimo sprendimo papildomi parametrai
description: Šiame straipsnyje pateikiama informacija apie papildomus SF fiksavimo sprendimo parametrus.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: a1e24b700d0f30fd90f2619dd6e6687736a86774
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691001"
---
# <a name="invoice-capture-solution-advanced-settings"></a>SF fiksavimo sprendimo papildomi parametrai

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikiama informacija apie papildomus SF fiksavimo sprendimo parametrus.

## <a name="create-additional-connections-for-channels"></a>Papildomų kanalų ryšių kūrimas

Turite sukurti ryšius su el. pašto ar failų saugykla, kad būtų galima stebėti gaunamas SF iš skirtingų kanalų. Iš pradžių turite užregistruoti ryšius, kad būtų galima suteikti prieigą prie sprendimų naudojamų automatinių srautų.

Šie ryšio tipai naudojami SF importuoti:

- Office 365 Outlook
- Outlook.com
- „OneDrive“
- „SharePoint“

SF importavimo kanalas naudos ryšius, kaip atlikti tolesnius konfigūravimo veiksmus. Kad vartotojai galėtų kurti konkretaus ryšio kanalą, **jiems** turi būti suteiktas administratoriaus saugos vaidmuo ir sukurti ryšius.

Norėdami sukurti ryšį, atlikite Microsoft Dataverse šiuos veiksmus.

1. Eiti į **administratoriaus sistemos \> numatytąjį sprendimą**.
2. Pasirinkite **Naujas**, tada pasirinkite **Ryšio nuoroda**.
3. **Lauke Rodomas pavadinimas** įveskite pavadinimą.
4. Pasirinkti **Microsoft Dataverse** kaip jungtį.
5. Jei ryšį nustatote pirmą kartą, pasirinkite Naujas **ryšys**.
6. Rodomame dialogo lange sukurkite ryšį Dataverse ir pasirinkite **Kurti**.
7. Įveskite abonementą Dataverse ir slaptažodį.
8. Atlikus tikrinimą, eikite į ryšio puslapį, pasirinkite **Atnaujinti**, pasirinkite abonementą, tada pasirinkite **Kurti**.

Norėdami sukurti el. pašto arba rinkmenos saugyklos ryšį, atlikite šiuos veiksmus.

1. **Ryšio kūrimo puslapio** lauke Ryšio **tipas** pasirinkite **Office 365 Outlook**.
2. Norėdami prisijungti prie el. pašto, kaip **jungtį Outlook.com** arba **Office 365 "Outlook** ". Norėdami prisijungti prie rinkmenos saugyklos galite pasirinkti arba **OneDrive** **SharePoint**.

Norėdami peržiūrėti esamus ryšius, eikite į numatytųjų **sprendimo \> objektų \> ryšio nuorodas**. Kanalus kuriantiems vartotojams turi būti bent vienas ryšys kartu Dataverse su konkrečiais el. pašto ar failų saugyklos ryšiais. Naujo kanalo kūrėjas turėtų būti ryšio savininkas.
