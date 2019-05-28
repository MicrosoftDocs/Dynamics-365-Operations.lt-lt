---
title: Sąskaitų faktūrų apmokėjimo scenarijų nustatymas
description: Šioje temoje aprašoma, kaip sukonfigūruoti „Dynamics 365 for Retail“, kad būtų palaikomi įvairūs scenarijai, susiję su sąskaitų faktūrų apmokėjimu.
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
ms.openlocfilehash: 158d8ca8a97c473e940f76dd3f35cecc4e9dd7f4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517125"
---
# <a name="set-up-pay-invoice-scenarios"></a>Sąskaitų faktūrų apmokėjimo scenarijų nustatymas

[!include [banner](includes/banner.md)]

„Dynamics 365 for Retail“ funkcija Apmokėti sąskaitą faktūrą išplėsta ir palaiko tolesnius scenarijus.

- Kelių pardavimo užsakymų sąskaitų faktūrų apmokėjimas atliekant vieną EKA operaciją.
- Įvairių tipų kliento SF, įskaitant laisvos formos sąskaitas faktūras, projektines sąskaitas faktūras ir kredito pažymas, apmokėjimas.

Norint įjungti šiuos scenarijus reikia sukonfigūruoti parduotuvių funkcijų profilį taip, kaip nurodyta toliau.

1. Eikite į **Mažmeninė prekyba \> Kanalų sąranka \> EKA sąranka \> EKA profiliai \> Funkcijų profiliai** ir pasirinkite profilį, susietą su parduotuvėmis, kurioms norite atlikti keitimus.
2. Skirtuke **Funkcijos** pagal poreikį sukonfigūruokite tolesnius parametrus.

    - **Pardavimo užsakymo sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias pardavimo užsakymu paremtas sąskaitas faktūras.
    - **Laisvos formos sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias laisvos formos sąskaitas faktūras.
    - **Projekto sąskaita faktūra** – pasirinkite **Taip**, jei vartotojams norite leisti atliekant vieną EKA operaciją apmokėti vieną ar kelias projektines sąskaitas faktūras.
    - **Pardavimo užsakymo kredito pažyma** – pasirinkite **Taip**, jei vartotojams norite leisti pagal atidarytas sąskaitas faktūras sudengti kelias pardavimo užsakymu paremtas kredito pažymas arba apdoroti pinigų grąžinimą klientui už atidarytą kredito pažymą.

> [!NOTE]
> Galimybės apmokėti ar sudengti dalines sumas dar nėra.
