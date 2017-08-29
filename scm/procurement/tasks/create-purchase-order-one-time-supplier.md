--- 
title: "Kurti vienkartinio tiekėjo pirkimo užsakymą"
description: "Šia procedūra parodoma, kaip neautomatiniu būdu kurti vienkartinio tiekėjo pirkimo užsakymą."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 580dfe3680c36a32a24999bc8c266a38a07177fd
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Kurti vienkartinio tiekėjo pirkimo užsakymą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra parodoma, kaip neautomatiniu būdu kurti vienkartinio tiekėjo pirkimo užsakymą. Tiekėjas yra automatiškai sukuriamas kartu su pirkimo užsakymu, užuot tiekėjo kodą kūrus neautomatiškai. Pirkimo užsakymus paprastai kuria pirkimo agentas. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Būtina vienkartinį tiekėjo kodą nustatyti puslapyje Mokėtinų sumų parametrai.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Kurti vienkartinio tiekėjo pirkimo užsakymą
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Vienkartinis tiekėjas pasirinkite Taip.
    * Tiekėjo kodas automatiškai sukuriamas ir priskiriamas pirkimo užsakymui. Tiekėjo kodas sukuriamas pagal šabloną, kuris nurodytas puslapio Mokėtinų sumų parametrai skirtuke Bendra.  
4. Lauke Pavadinimas įveskite tiekėjo pavadinimą.
5. Spustelėkite GERAI.
    * Dabar pirkimo užsakymą galima baigti ir apdoroti kaip bet kurį kitą užsakymą. Nėra jokių specialių charakteristikų, susijusių su tuo, kaip tai daroma. SF bus apskaityta apmokėtina tiekėjo kodo, sukurto kartu su užsakymu, operacija ir tada mokėjimas bus apdorotas. Tai atlikus, tiekėjo kodą galima panaikinti. Paprastai tai atlieka mokėtinų sumų padalinys.  


