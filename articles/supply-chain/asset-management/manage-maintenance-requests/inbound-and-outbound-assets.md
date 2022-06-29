---
title: Gaunami ir siunčiami ištekliai
description: Šiame straipsnyje paaiškinama, kaip registruoti gaunamo ir siunčiamo turto valdymo dalyje.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd7482cfe943347840e9fb070151d66fbe5ef9ca
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016542"
---
# <a name="inbound-and-outbound-assets"></a>Gaunamas ir siunčiamas turtas

[!include [banner](../../includes/banner.md)]

 

Jei jūsų įmonė vykdo iš kitų vietų ar klientų gauto turto remonto darbus ar priežiūros užduotis, modulyje Turto valdymas galima sekti ir gaunamą turtą, kuris yra pakeliui į jūsų įmonę, ir siunčiamą turtą, kuris yra grąžinamas.

> [!NOTE]
> Jei norite naudoti gaunamas ir siunčiamas ciklo būsenas gaunamam ir grąžinamam turtui valdyti, turite nustatyti priežiūros užklausų ciklo būsenas ir ciklo modelius, kad šie veiksmai būtų palaikomi. Daugiau informacijos žr. [Priežiūros užklausos](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview).

Turto valdymo konfigūracija nulemia, ar galite dirbti su gaunamu ir siunčiamu turtu.

## <a name="register-assets-as-inbound"></a>Gaunamo turto registravimas

1. Pasirinkite **turto valdymo priežiūros** \> **užklausas** \> **Aktyvios priežiūros užklausos**.
2. Pasirinkite priežiūros užklausą.
3. Pasirinkite **Atnaujinti priežiūros užklausos būseną**.
4. Pasirinkite **Gaunamas** (arba kitą sukurtą gaunamo turto ciklo būseną), tada pasirinkite **Gerai**.

![Turto registravimas kaip gaunamo.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Gaunamo turto kaip gauto registravimas

1. Pasirinkite **turto valdymo** \> **gaunama/siunčiamas gaunamas** \> **turtas.**
2. Pasirinkite turtą arba priežiūros užklausą.
3. Pasirinkite **Gauti turtą**.
4. Lauke **Gauta** įveskite datą ir laiką. Tada pasirinkite **Gerai**. Įrašas pašalinamas iš **Gaunamas turtas** sąrašo puslapio.

![Gaunamo turto kaip gauto registravimas.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Siunčiamo turto registravimas

Atlikę priežiūros arba remonto užduotį, galite užregistruoti turtą kaip grąžintą.

1. Pasirinkite **turto valdymo priežiūros** \> **užklausas** \> **Aktyvios priežiūros užklausos**.
2. Pasirinkite priežiūros užklausą.
3. Pasirinkite **Atnaujinti priežiūros užklausos būseną**.
4. Pasirinkite **Siunčiamas** (arba kitą sukurtą siunčiamo turto ciklo būseną), tada pasirinkite **Gerai**.

## <a name="register-outbound-assets-as-delivered"></a>Siunčiamo turto kaip pristatyto registravimas

1. Pasirinkite **turto valdymo** \> **gaunamo/siunčiamo siunčiamo** \> **turto.**
2. Pasirinkite turtą arba priežiūros užklausą.
3. Pasirinkite **Pristatyti turtą**.
4. Lauke **Pristatyta** įveskite datą ir laiką. Tada pasirinkite **Gerai**. Įrašas pašalinamas iš **Siunčiamas turtas** sąrašo puslapio.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]