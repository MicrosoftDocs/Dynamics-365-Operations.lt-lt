---
title: Kurti vienkartinio tiekėjo pirkimo užsakymą
description: Šia procedūra parodoma, kaip neautomatiniu būdu kurti vienkartinio tiekėjo pirkimo užsakymą.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e6c8283290564d930418c1832bbd285532445ff0e69db8f78d13542c8232e97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720305"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Kurti vienkartinio tiekėjo pirkimo užsakymą

[!include [banner](../../includes/banner.md)]

Šia procedūra parodoma, kaip neautomatiniu būdu kurti vienkartinio tiekėjo pirkimo užsakymą. Tiekėjas yra automatiškai sukuriamas kartu su pirkimo užsakymu, užuot tiekėjo kodą kūrus neautomatiškai. Pirkimo užsakymus paprastai kuria pirkimo agentas. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Būtina vienkartinį tiekėjo kodą nustatyti puslapyje Mokėtinų sumų parametrai.


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>Kurti vienkartinio tiekėjo pirkimo užsakymą
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo užsakymai > Visi pirkimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Vienkartinis tiekėjas pasirinkite Taip.
    * Tiekėjo kodas automatiškai sukuriamas ir priskiriamas pirkimo užsakymui. Tiekėjo kodas sukuriamas pagal šabloną, kuris nurodytas puslapio Mokėtinų sumų parametrai skirtuke Bendra.  
4. Lauke Pavadinimas įveskite tiekėjo pavadinimą.
5. Spustelėkite GERAI.
    * Dabar pirkimo užsakymą galima baigti ir apdoroti kaip bet kurį kitą užsakymą. Nėra jokių specialių charakteristikų, susijusių su tuo, kaip tai daroma. SF bus apskaityta apmokėtina tiekėjo kodo, sukurto kartu su užsakymu, operacija ir tada mokėjimas bus apdorotas.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]