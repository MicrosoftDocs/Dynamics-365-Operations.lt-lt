---
title: Darbo užsakymai ir ilgalaikis turtas
description: Šioje temoje aiškinami darbo užsakymai ir ilgalaikis turtas modulyje „Turto valdymas”.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f03b7fa073c4e5338b7b5681ba7b8c9fe00a657b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875792"
---
# <a name="work-orders-and-fixed-assets"></a>Darbo užsakymai ir ilgalaikis turtas


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Modulyje „Turto valdymas” turtas gali būti susietas su ilgalaikiu turtu ir tokiam turtui galite sukurti darbo užsakymus. Naudodamiesi šiomis funkcijomis galite gauti išsamią ilgalaikio turto, susijusių investicinių projektų ir registruotų investicinių projektų išlaidų apžvalgą modulyje **Projektų valdymas ir apskaita** ir modulyje **Ilgalaikis turtas** Dynamics 365 for Finance and Operations.

>[!NOTE]
>Darbo užsakymo užduoties projekto laukas **Ilgalaikio turto numeris** pildomas tik tuo atveju, jeigu darbo užsakymo užduoties projekte pasirenkamas projekto tipas „Investicija”.

![1 pav.](media/24-work-orders.png)

Toliau nurodyta procedūra apibūdinama turto, darbo užsakymų, darbo užsakymo užduočių projektų ir ilgalaikio turto sąsaja.

1. Toliau pateiktame paveikslėlyje parodyta, kaip sukurti turtą, kuris siejamas su ilgalaikiu turtu.

![2 pav.](media/25-work-orders.png)

2. Kai nustatomi darbo užsakymų tipai (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Darbo užsakymų tipai**), sukuriamas investicijų valdymo darbo užsakymo tipas. Taip pat žr. [Darbo užsakymų tipai](../setup-for-work-orders/work-order-types.md).

![3 pav.](media/26-work-orders.png)

3. Kai nustatomos darbo užsakymų projektų grupės (nuoroda **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Projekto sąranka** > **Projektų grupė**), modulyje **Projektų valdymas ir apskaita** sukuriama investicijoms naudojamo darbo užsakymo tipo ir investicijoms sukurtos projektų grupės sąsaja (**Projektų valdymas ir apskaita** > **Sąranka** > **Registravimas** > **Projektų grupės**).

![4 pav.](media/27-work-orders.png)

4. Kai nustatomas darbo užsakymas, susijęs su ilgalaikio turto objektu, pasirenkamas investicijų valdymo darbo užsakymo tipas, pvz., „Investicija”.

5. Kai sukuriamas darbo užsakymas, susijęs darbo užsakymo tipas rodomas pasirinkus **Visi darbo užsakymai**.

![5 pav.](media/28-work-orders.png)

6. Kai sukuriamas darbo užsakymas, su darbo užsakymu susijęs projektas sukuriamas **Projektų valdymas ir apskaita** > **Visi projektai**. Su projektu susijusią informaciją galite rasti darbo užsakyme spustelėję nuorodą **Projekto ID** (modulyje **Turto valdymas** pasirinkite rodinį „Išsami informacija apie darbo užsakymą” > „FastTab” **Eilutės informacija** > skirtukas **Bendroji informacija** > laukas **Projekto ID**).

![6 pav.](media/29-work-orders.png)

7. Pasirinkę **Ilgalaikis turtas**, galite pamatyti su ilgalaikiu turtu susijusių projektų apžvalgą (**Ilgalaikis turtas** > **Ilgalaikis turtas** > **Ilgalaikis turtas** > pasirinkite ilgalaikį turtą lauke **Ilgalaikio turto numeris** > peržiūrėkite turinį srityje **Susijusi informacija** > skyrius **Susiję projektai**).

