---
title: Užduočių vedlių įrašymas į LCS ir pakartotinis leidimas
description: Šiame straipsnyje aiškinama, kaip įrašyti užduoties vedlius į „Microsoft Dynamics Lifecycle Services“ (LCS) ir leisti juos pakartotinai.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d6102bafc9b55f9eff05bfc4a63c177c6548694
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463267"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Užduočių vedlių įrašymas į LCS ir pakartotinis leidimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Aplinkos informacija** 

„Microsoft Dynamics 365 Human Resources“, įdiegtas naudojant „Microsoft Dynamics Lifecycle Services“ (LCS)

**Išduoti**

Klientas nori įrašyti naują užduoties įrašą į savo LCS projektą, tada pakartotinai leisti įrašytus užduoties vedlius.

**Skiriamoji geba**

Norėdami įrašyti užduoties įrašą į LCS, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie LCS ir pasirinkite projektą.
2. Pasirinkite plytelę **Verslo procesų modeliavimo įrankis**.
3. Peržiūrėti puslapį atnaujintoje BPM programoje.
4. Pasirinkite biblioteką, tada – **Kopijuoti**.
5. Įveskite Verslo procesų modeliavimo įrankio (BPM) modelio pavadinimą.
6. Prisijunkite prie „Human Resources“ iš LCS.
7. Lauke **Ieškoti** įveskite **žinynas**. Bus atidarytas „Lifecycle Services“ žinynas.
8. Pasirinkite mygtuką **Atnaujinti**, kad galėtumėte konfigūruoti „Lifecycle Services“ žinyną.

    Turėtų būti rodoma jūsų nauja BPM biblioteka. Ji turėtų būti aktyvi.

9. Uždarykite puslapį.
10. Sukurkite užduoties įrašą.
11. Baigę pasirinkite **Įrašyti į „Lifecycle Services“**.

    ![Įrašyti į „Lifecycle Services“](media/task-guides.png)

12. Pasirinkite BPM biblioteką ir mazgą, į kuriuos norite įrašyti užduoties įrašą.

Norėdami pakartotinai paleisti LCS užduoties vedlį, atlikite toliau nurodytus veiksmus.

1. Paleiskite užduočių įrašymo priemonę.
2. Pasirinkite **Atidaryti iš LCS**.
3. Pasirinkite biblioteką ir BPM mazgą, kuriame yra įrašytas užduoties vedlys.
4. Atidarykite užduoties vedlį.


[!INCLUDE[footer-include](../includes/footer-banner.md)]