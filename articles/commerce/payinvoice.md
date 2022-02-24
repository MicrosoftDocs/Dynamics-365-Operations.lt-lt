---
title: Sąskaitų faktūrų apmokėjimo scenarijų nustatymas
description: Šioje temoje aprašoma, kaip sukonfigūruoti „Dynamics 365 Commerce“, kad būtų palaikomi įvairūs scenarijai, susiję su sąskaitų faktūrų apmokėjimu.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9fe8fde32549568812a724311781d3515ef7036c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459579"
---
# <a name="set-up-pay-invoice-scenarios"></a>Sąskaitų faktūrų apmokėjimo scenarijų nustatymas

[!include [banner](includes/banner.md)]

„Dynamics 365 Commerce“ funkcija Apmokėti sąskaitą faktūrą išplėsta ir palaiko tolesnius scenarijus.

- Kelių pardavimo užsakymų sąskaitų faktūrų apmokėjimas atliekant vieną EKA operaciją.
- Įvairių tipų kliento SF, įskaitant laisvos formos sąskaitas faktūras, projektines sąskaitas faktūras ir kredito pažymas, apmokėjimas.

Norint įjungti šiuos scenarijus reikia sukonfigūruoti parduotuvių funkcijų profilį taip, kaip nurodyta toliau.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Funkcijų profiliai** ir pasirinkite profilį, susietą su parduotuvėmis, kurioms norite atlikti keitimus.
2. Skirtuke **Funkcijos** pagal poreikį sukonfigūruokite tolesnius parametrus.

    - **Pardavimo užsakymo sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias pardavimo užsakymu paremtas sąskaitas faktūras.
    - **Laisvos formos sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias laisvos formos sąskaitas faktūras.
    - **Projekto sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias projektines sąskaitas faktūras.
    - **Pardavimo užsakymo kredito pažyma** – pasirinkite **Taip**, jei vartotojams norite leisti pagal atidarytas sąskaitas faktūras sudengti kelias pardavimo užsakymu paremtas kredito pažymas arba apdoroti pinigų grąžinimą klientui už atidarytą kredito pažymą.

> [!NOTE]
> Galimybės apmokėti ar sudengti dalines sumas dar nėra.
