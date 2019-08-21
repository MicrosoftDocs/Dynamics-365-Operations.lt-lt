---
title: Kurti vienkartinio tiekėjo pirkimo užsakymą
description: Šia procedūra parodoma, kaip neautomatiniu būdu kurti vienkartinio tiekėjo pirkimo užsakymą.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26c62aa72a7919c780bb709b185b48c97066c538
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836317"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Kurti vienkartinio tiekėjo pirkimo užsakymą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra parodoma, kaip neautomatiniu būdu kurti vienkartinio tiekėjo pirkimo užsakymą. Tiekėjas yra automatiškai sukuriamas kartu su pirkimo užsakymu, užuot tiekėjo kodą kūrus neautomatiškai. Pirkimo užsakymus paprastai kuria pirkimo agentas. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Būtina vienkartinį tiekėjo kodą nustatyti puslapyje Mokėtinų sumų parametrai.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Kurti vienkartinio tiekėjo pirkimo užsakymą
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Vienkartinis tiekėjas pasirinkite Taip.
    * Tiekėjo kodas automatiškai sukuriamas ir priskiriamas pirkimo užsakymui. Tiekėjo kodas sukuriamas pagal šabloną, kuris nurodytas puslapio Mokėtinų sumų parametrai skirtuke Bendra.  
4. Lauke Pavadinimas įveskite tiekėjo pavadinimą.
5. Spustelėkite GERAI.
    * Dabar pirkimo užsakymą galima baigti ir apdoroti kaip bet kurį kitą užsakymą. Nėra jokių specialių charakteristikų, susijusių su tuo, kaip tai daroma. SF bus apskaityta apmokėtina tiekėjo kodo, sukurto kartu su užsakymu, operacija ir tada mokėjimas bus apdorotas. Tai atlikus, tiekėjo kodą galima panaikinti. Paprastai tai atlieka mokėtinų sumų padalinys.  

