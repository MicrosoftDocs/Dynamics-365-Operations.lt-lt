---
title: Suplanuotų užsakymų priežiūra
description: Šiame straipsnyje pateikiama informacija apie tai, kaip valdyti suplanuotus užsakymus. Jame aprašoma, kaip galite atnaujinti suplanuotų užsakymų būseną, juos patvirtinti ir filtruoti suplanuotus užsakymus, kurių būsena tokia pati, kaip pasirinkto suplanuoto užsakymo.
author: t-benebo
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9df39d271ae61c304f70c38a23e4249eb5920b29
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740798"
---
# <a name="maintain-planned-orders"></a>Suplanuotų užsakymų priežiūra

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie tai, kaip valdyti suplanuotus užsakymus. Jame aprašoma, kaip galite atnaujinti suplanuotų užsakymų būseną, juos patvirtinti ir filtruoti suplanuotus užsakymus, kurių būsena tokia pati, kaip pasirinkto suplanuoto užsakymo.

Suplanuotus užsakymus galite valdyti naudodami darbo sritį **Bendrasis planavimas**, sąrašą **Suplanuoti užsakymai** arba sąrašus **Suplanuoti gamybos užsakymai**, **Suplanuoti pirkimo užsakymai** ir **Suplanuotas perkėlimas**. 

## <a name="planned-order-status"></a>Suplanuoto užsakymo būsena
Galite naudoti lauką **Būsena** progresui sekti. Naudojamos toliau nurodytos reikšmės.

-   Kai bendrasis planavimas sugeneruoja suplanuotus užsakymus, suplanuotų užsakymų būsena yra **Neapdorota**.
-   Jei nenorite patvirtinti suplanuoto užsakymo, galite jam nustatyti būseną **Baigta**.
-   Jei norite patvirtinti suplanuotą užsakymą, galite pakeisti būseną į **Patvirtinta**. Suplanuoti užsakymai, kurių būsena yra **Patvirtinta**, neliečiami bendrojo planavimo metu, kad nebūtų modifikuojami ar panaikinami vėlesnio pagrindinio planavimo vykdymo metu. Norint tai pasiekti, planavimo logika kopijuoja **patvirtintus** suplanuotus užsakymus iš senosios plano versijos į naująją plano versiją bendrojo planavimo metu.

## <a name="firming-planned-orders"></a>Suplanuotų užsakymų patvirtinimas 
Patvirtinant suplanuotus užsakymus, sukuriami realūs užsakymai. Jie taip pat vadinami *pateiktais* arba *atvirais užsakymais*. Kai suplanuotas užsakymas patvirtinamas, jis perkeliamas į atitinkamo modulio užsakymų dalį.

Galite pasirinkti dvi patvirtinimo parinktis iš puslapio **Suplanuoti užsakymai**:

-   **Patvirtinti** – patvirtinti vieną ar kelis pasirinktus suplanuotus užsakymus.
-   **Patvirtinti visus** – patvirtinti visus filtruojamus suplanuotus užsakymus. Naudojant **Patvirtinti visus**, jums nereikia pasirinkti suplanuoto užsakymo, nes visi filtruojami suplanuoti užsakymai bus patvirtinti. Ši pasirinktis gali būti naudinga, jei jūs norite patvirtinti daug suplanuotų užsakymų.

> [!NOTE]
> Galite sekti suplanuotą užsakymą, kuris buvo patvirtintas iš **Patvirtinimų retrospektyvos**, esančios **suplanuotų užsakymų formoje > Peržiūrėti > Patvirtinimų retrospektyva**.

## <a name="parallelize-firming"></a>Sugretinti tvirtinimą
Jeigu planuojate patvirtinti daug užsakymų tuo pačiu metu, lygiagretus vykdymas gali sutrumpinti apdorojimo laiką arba padidinti efektyvumą. Ši pasirinktis pasiekiama patvirtinant kelis suplanuotus užsakymus pasirinkus **Patvirtinti** arba **Patvirtinti visus**. Galimi tolesni parametrai.

-   **Lygiagretinti patvirtinimą** – jei reikšmė yra **Taip**, lygiagretinimo procesas bus atliekamas naudojant gijų skaičių, nurodytą **Gijų skaičius**.
-   **Gijų skaičius** – kontroliuoja gijų skaičių, naudojamą patvirtinimo procesui lygiagretinti. Parametras rodomas tik tada, kai nustatyta **Lygiagretinti patvirtinimą** reikšmė **Taip**.

> [!NOTE]
> Parinktis **Lygiagretinti patvirtinimą** rodoma tik tada, kai turite daugiau nei vieną suplanuotą užsakymą, kurį pasirinkote patvirtinti.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Bendrųjų planų apžvalga](master-plans.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]