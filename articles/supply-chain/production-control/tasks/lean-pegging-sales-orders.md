---
title: „Lean“ iškvietimas iš pardavimo užsakymų
description: Ši procedūra padės iškvietimo medį patikrinti iš pardavimo eilutės, kurioje prekė gaminama naudojant „kanban“.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6a18d24be85e20a7e5824c334855aa94fe61cb5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245978"
---
# <a name="lean-pegging-from-sales-orders"></a>„Lean“ iškvietimas iš pardavimo užsakymų

[!include [banner](../../includes/banner.md)]

Ši procedūra padės iškvietimo medį patikrinti iš pardavimo eilutės, kurioje prekė gaminama naudojant „kanban“. Patikrinus iškvietimo medį, suplanuojamos visos „kanban“ užduotys. Tai naudinga užsakymų scenarijuose, kai užsakymo priėmėjas turi užtikrinti, kad gamybą galima pradėti iš karto. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta detalesnio užsakymo priėmėjui, dirbančiam „lean“ įmonėje.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Kurti „kanban“ valdomos prekės pardavimo užsakymą
1. Eikite į Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
    * Naudokite US-001.  
4. Spustelėkite GERAI.
5. Lauke „Prekės numeris“ įveskite „L0001“.
6. Nustatykite kiekį – 30.
    * Kiekis būtinai turi būti didesnis nei 24, kad įvykio „kanban“ taisyklė būtų paleista.  

## <a name="open-a-pegging-tree"></a>Atidaryti iškvietimo medį 
1. Spustelėkite Produktas ir tiekimas.
2. Spustelėkite Peržiūrėti iškvietimo medį.
    * Atkreipkite dėmesį, kad iškvietimo medyje rodomi visi reikiami pardavimo užsakymo eilutės iškvietimo lygiai. Šiuo atveju rodomi du „kanban“ lygiai ir visi būtini komponentai.  

## <a name="plan-the-pegging-tree"></a>Planuoti iškvietimo medį
1. Medyje pasirinkite „Pardavimo eilutė 000832 \ „kanban“ 000558“.
2. Išplėskite sekciją „Kanban“ užduotys.
    * Atkreipkite dėmesį, kad „kanban“ užduoties būsena yra Nesuplanuota.  
3. Spustelėkite Planuoti visą iškvietimo medį.
    * Šiuo būdu bus suplanuotos visos iškvietimo medžio „kanban“ taisyklės ir užduočių būsenos bus pakeistos iš Nesuplanuota į Suplanuota.  
4. Atnaujinkite puslapį.
    * Atkreipkite dėmesį, kad „kanban“ užduoties būsena iš Nesuplanuota pasikeitė į Suplanuota.  
5. Medyje pasirinkite „Pardavimo eilutė 000832 \ „Kanban“ 000558 \ Išdavimas, skirtas L0001 \ „Kanban“ 000559“.
    * Antroji „kanban“ taisyklė taip pat suplanuota, nes suplanuotas visas iškvietimo medis. Atkreipkite dėmesį, kad „kanban“ užduoties būsena iš Nesuplanuota pasikeitė į Suplanuota.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]