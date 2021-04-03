---
title: Darbo užsakymai ir ilgalaikis turtas
description: Šioje temoje aiškinami darbo užsakymai ir ilgalaikis turtas modulyje „Turto valdymas”.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 678bfae5d0b4ea469a91fc89306be40c39cb082d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223439"
---
# <a name="work-orders-and-fixed-assets"></a>Darbo užsakymai ir ilgalaikis turtas

[!include [banner](../../includes/banner.md)]


Modulyje „Turto valdymas” turtas gali būti susietas su ilgalaikiu turtu ir tokiam turtui galite sukurti darbo užsakymus. Naudodamiesi šiomis funkcijomis galite gauti išsamią ilgalaikio turto, susijusių investicijų projektų ir investiciniuose projektuose registruotų išlaidų apžvalgą moduliuose **Projektų valdymas ir apskaita** ir **Ilgalaikis turtas**, esančiuose „Microsoft Dynamics 365 for Finance and Operations“.

>[!NOTE]
>Darbo užsakymo užduoties projekto laukas **Ilgalaikio turto numeris** nurodomas tik tuo atveju, jeigu darbo užsakymo užduoties projekte pasirenkamas projekto tipas **Investicija**.

Toliau pateiktame paveikslėlyje parodytas ryšys tarp investicijų projekto modulyje **Projektų valdymas ir apskaita** ir darbo užsakymo užduoties projekto.

![1 pav.](media/24-work-orders.png)

Toliau nurodyta procedūra apibūdinama turto, darbo užsakymų, darbo užsakymo užduočių projektų ir ilgalaikio turto sąsaja.

1. Kuriate turtą, kurį susiejate su ilgalaikiu turtu.

![2 pav.](media/25-work-orders.png)

2. Kai puslapyje **Darbo užsakymų tipai** nustatote darbo užsakymų tipus (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Darbo užsakymų tipai**), kuriate darbo užsakymo tipą darbui su investicijomis. Taip pat žr. [Darbo užsakymų tipai](../setup-for-work-orders/work-order-types.md).

![3 pav.](media/26-work-orders.png)

3. Kai darbo užsakymų projektų grupes nustatote skirtuke **Projektų grupė**, esančiame puslapyje **Darbo užsakymo projekto sąranka** (**Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Projekto nustatymai**), kuriate ryšį tarp investicijoms naudojamo darbo užsakymo tipo ir projektų grupės, sukurtos investicijoms puslapyje **Projektų grupės**, priklausančiame moduliui **Projektų valdymas ir apskaita** (**Projektų valdymas ir apskaita** > **Sąranka** > **Registravimas** > **Projektų grupės**).

![4 pav.](media/27-work-orders.png)

4. Kai kuriate darbo užsakymą, susijusį su ilgalaikiu turtu, pasirenkate darbui su investicijomis naudojamą darbo užsakymo tipą, pvz., **Investicija**.

5. Sukūrus darbo užsakymą, susijęs darbo užsakymo tipas rodomas puslapyje **Visi darbo užsakymai**.

![5 pav.](media/28-work-orders.png)

6. Sukūrus darbo užsakymą, projektas, susijęs su darbo užsakymu, sukuriamas puslapyje **Visi projektai**, priklausančiame moduliui **Projektų valdymas ir apskaita** (**Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai**). Norėdami peržiūrėti su projektu susijusią informaciją, pasirinkite saitą lauke **Projekto ID**, esančiame skirtuke **Bendra**, „FastTab“ **Eilutės informacija**, puslapio **Visi darbo užsakymai** informacijos rodinyje, modulyje **Turto valdymas** (**Turto valdymas** > **Bendra** > **Darbo užsakymai** > **Visi darbo užsakymai**).

![6 pav.](media/29-work-orders.png)

7. Norėdami peržiūrėti projektus, susijusius su ilgalaikiu turtu, pasirinkite **Ilgalaikis turtas** > **Ilgalaikis turtas** > **Ilgalaikis turtas**, o tada lauke **Ilgalaikio turto numeris** pasirinkite ilgalaikio turto saitą, kad atidarytumėte informacijos rodinį. Išskleiskite dešinėje puslapio pusėje esančią sritį **Susijusi informacija** ir pasirinkite „FastTab“ **Susiję projektai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]