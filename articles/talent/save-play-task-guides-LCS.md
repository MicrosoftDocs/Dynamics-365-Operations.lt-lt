---
title: "Užduočių vedlių įrašymas į LCS ir pakartotinis leidimas"
description: "Šioje temoje aiškinama, kaip įrašyti užduoties vedlius į „Microsoft Dynamics Lifecycle Services“ (LCS) ir leisti juos pakartotinai."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a>Užduočių vedlių įrašymas į LCS ir pakartotinis leidimas

[!include [banner](includes/banner.md)]

**Aplinkos informacija** 

„Microsoft Dynamics 365 for Talent“, įdiegtas naudojant „Microsoft Dynamics Lifecycle Services“ (LCS)

**Problema**

Klientas nori įrašyti naują užduoties įrašą į savo LCS projektą, tada pakartotinai leisti įrašytus užduoties vedlius.

**Skiriamoji geba**

Norėdami įrašyti užduoties įrašą į LCS, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie LCS ir pasirinkite projektą.
2. Pasirinkite plytelę **Verslo procesų modeliavimo įrankis**.
3. Peržiūrėti puslapį atnaujintoje BPM programoje.
4. Pasirinkite biblioteką, tada – **Kopijuoti**.
5. Įveskite Verslo procesų modeliavimo įrankio (BPM) modelio pavadinimą.
6. Būdami prisijungę LCS prisijunkite prie „Talent“.
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

