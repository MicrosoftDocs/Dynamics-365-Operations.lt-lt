---
title: Efektyvumo optimizavimas naudojant automatinio valymo užduotis
description: Šiame straipsnyje paaiškinama, kaip išspręsti tam tikras našumo problemas naudojant „Microsoft Dynamics 365 Human Resources“, valant paketinių užduočių retrospektyvą.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a983fde8ba393ab25f2b330014e04a1379f0e4d0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419666"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Našumo optimizavimas naudojant automatinio valymo užduotis

**Išduoti**

Naudojant „Microsoft“ „Dynamics 365 Human Resources“, gali kilti našumo problemų, jei paketinių užduočių retrospektyva tampa per ilga.

**Priežastis**

Jei paketinės užduotys vykdomos dažnai, paketinių užduočių retrospektyva gali pernelyg pailgėti. Tai gali sukelti našumo problemų. 

**Nutarimas**

Suplanuokite automatinę užduotį, kad išvalytumėte paketinių užduočių retrospektyvą. Rekomenduojame nustatyti, kad užduotis būtų vykdoma kas savaitę, tačiau, atsižvelgiant į jūsų aplinką, gali reikėti valyti dažniau ar rečiau. Šioje procedūroje pateikiami rekomenduojami parametrai, tačiau juos galite keisti pagal poreikius.

1. Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.

2. Juostoje **Ieška** įveskite **Paketinių užduočių retrospektyvos valymas**.

   ![Paketinių užduočių retrospektyvos valymo ieška](media/talent-batch-history-cleanup-search-bar.png)

3. Lauke **Retrospektyvos riba (dienos)** įveskite **30**.

   ![30 dienų retrospektyvos ribos nustatymas](media/talent-batch-history-cleanup-history-limit.png)

4. Pasirinkite **Vykdyti fone**, tada pasirinkite **Pasikartojimas**.

   ![Pasikartojimo nustatymas](media/talent-batch-history-cleanup-recurrence.png)

5. Dalyje **Nurodyti pasikartojimą** nustatykite parinktis **Pradžios data** ir **Pradžios laikas**, kad valymas būtų vykdomas po darbo arba savaitgalį, paskui pasirinkite **NĖRA PABAIGOS DATOS**. 

   ![Pasikartojimo pradžios datos ir laiko nurodymas](media/talent-batch-history-cleanup-define-recurrence.png)

6. Dalyje **KARTOJIMAS** pasirinkite **Dienos** ir nustatykite parinkties **PAKARTOTI PO NURODYTO INTERVALO** reikšmę **7**.

   ![Nustatymas, kad valymas būtų kartojamas kas savaitę](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Pasirinkite **Gerai**.

8. Jei reikia, dalyje **Vykdyti fone** pakeiskite kitus parametrus, tada pasirinkite **Gerai**.

