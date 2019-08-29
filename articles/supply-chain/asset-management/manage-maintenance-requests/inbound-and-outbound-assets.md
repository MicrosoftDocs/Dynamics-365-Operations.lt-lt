---
title: Gaunamas ir siunčiamas turtas
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas užregistruoti gaunamą ir siunčiamą turtą.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62998da7f541379296d5ac325ae29f24a42f9b7c
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847556"
---
# <a name="inbound-and-outbound-assets"></a>Gaunamas ir siunčiamas turtas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Jei jūsų įmonė vykdo iš kitų vietų ar klientų gauto turto remonto darbus ar priežiūros užduotis, modulyje Turto valdymas galima sekti ir gaunamą turtą, kuris yra pakeliui į jūsų įmonę, ir siunčiamą turtą, kuris yra grąžinamas.

> [!NOTE]
> Jei norite naudoti gaunamas ir siunčiamas ciklo būsenas gaunamam ir grąžinamam turtui valdyti, turite nustatyti priežiūros užklausų ciklo būsenas ir ciklo modelius, kad šie veiksmai būtų palaikomi. Daugiau informacijos žr. skyriuje [Priežiūros užklausų konfigūracija](../setup-for-maintenance-requests/requests.md).

Turto valdymo konfigūracija nulemia, ar galite dirbti su gaunamu ir siunčiamu turtu.

## <a name="register-assets-as-inbound"></a>Gaunamo turto registravimas

1. Pasirinkite**Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.
2. Pasirinkite priežiūros užklausą.
3. Pasirinkite **Atnaujinti priežiūros užklausos būseną**.
4. Pasirinkite **Gaunamas** (arba kitą sukurtą gaunamo turto ciklo būseną), tada pasirinkite **Gerai**.

![1 paveikslėlis](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Gaunamo turto kaip gauto registravimas

1. Pasirinkite **Turto valdymas** \> **Dažnas** \> **Pirmyn atgal** \> **Atvykstamasis turtas**.
2. Pasirinkite turtą arba priežiūros užklausą.
3. Pasirinkite **Gauti turtą**.
4. Lauke **Gauta** įveskite datą ir laiką. Tada pasirinkite **Gerai**. Įrašas pašalinamas iš sąrašo puslapio **Inbound assets**.

![2 paveikslėlis](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Siunčiamo turto registravimas

Atlikę priežiūros arba remonto užduotį, galite užregistruoti turtą kaip grąžintą.

1. Pasirinkite**Asset management** \> **Common** \> **Maintenance requests** \> **Active maintenance requests**.
2. Pasirinkite priežiūros užklausą.
3. Pasirinkite **Atnaujinti priežiūros užklausos būseną**.
4. Pasirinkite **Siunčiamas** (arba kitą sukurtą siunčiamo turto ciklo būseną), tada pasirinkite **Gerai**.

## <a name="register-outbound-assets-as-delivered"></a>Siunčiamo turto kaip pristatyto registravimas

1. Pasirinkite **Turto valdymas** \> **Dažnas** \> **Pirmyn atgal** \> **Siunčiamas turtas**.
2. Pasirinkite turtą arba priežiūros užklausą.
3. Pasirinkite **Pristatyti turtą**.
4. Lauke **Pristatyta** įveskite datą ir laiką. Tada pasirinkite **Gerai**. Įrašas pašalinamas iš sąrašo puslapio **Outbound assets**.