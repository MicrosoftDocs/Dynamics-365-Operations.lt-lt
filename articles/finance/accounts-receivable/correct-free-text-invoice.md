---
title: Laisvos formos SF taisymas
description: Šiame straipsnyje paaiškinama, kaip ištaisyti laisvos formos SF, kuri buvo užregistruota, ir pakartotinai ją išduoti kaip pataisytą SF.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71b94e6fa4faafdc5fbe68e89635ec79616164bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217535"
---
# <a name="correct-a-free-text-invoice"></a>Laisvos formos SF taisymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip ištaisyti laisvos formos SF, kuri buvo užregistruota, ir pakartotinai ją išduoti kaip pataisytą SF.

Norėdami ištaisyti jau užregistruotą laisvos formos SF, atidarykite užregistruotą laisvos formos SF. Puslapyje **SF** pasirinkite **Atšaukti** ir tada pasirinkite **Taisyti SF**. Pasirinkite priežasties kodą, pridėkite komentarų ir pasirinkite naujos pataisytos SF datą. Pataisytą SF galite modifikuoti ir užregistruoti. 

Kai registruojate pataisytą SF, kredito sumai, kuri lygi pradinei SF sumai, sukuriama atšaukiamoji SF. Todėl kombinuotasis pradinės SF ir atšaukiamosios SF balansas yra 0 (nulis). Atšaukiamoji SF sudengiama pagal pradinę SF. 

Užregistravę pataisytą SF, turėsite toliau nurodytas tris SF.

-   **Pradinė SF** – SF, kuri apima informaciją, kurią taisote.
-   **Atšaukiamoji SF** – sistemos sugeneruota kredito SF, kuri sukurta norint atšaukti SF, kuri buvo paskiausiai pataisyta.
-   **Pataisyta SF** – SF, kurioje yra pataisyta SF informacija.

Atšaukiamąją ir pataisytą SF galite identifikuoti toliau nurodytais dviem būdais.

-   **Visų laisvos formos SF** puslapyje yra **Taisymo** stulpelis, kuriame galite matyti, kurios SF yra atšaukiamosios, o kurios – pataisytos.
-   Laisvos formos SF antraštėje rodoma būsena  **Atšaukiamoji SF \[SF numeris\]** arba **Pataisyta SF \[SF numeris\]**.

> [!NOTE]
> Ši funkcija prieinama tik jei pasirinktas konfigūracijos raktą **Laisvos formos SF taisymas**. Daugiau informacijos apie tai, kaip įgalinti konfigūracijos raktus, rasite skyriuje Konfigūracijos raktų įjungimas (arba išjungimas), temoje [Priežiūros režimas](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]