---
title: Papildymas išėmimų „kanban“
description: Šioje temoje aprašoma, kaip išėmimo „kanban“ naudojama medžiagų papildymui gamybos veikloje.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanFlow, KanbanRules, WHSKanbanWaveTable, WHSKanbanWaveTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b90e4699c440d0dd753cd16ff17cf958507e7872138a7f2c2c84f645f713d3db
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742589"
---
# <a name="replenishment-with-withdrawal-kanbans"></a>Papildymas išėmimų „kanban“

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip išėmimo „kanban“ naudojama medžiagų papildymui gamybos veikloje.

## <a name="workflow-for-material-replenishment-that-uses-the-withdrawal-kanban"></a>Darbo eigos medžiagų papildymas, kuriame naudojamas išėmimo „kanban“

Išėmimo „kanban“ galima naudoti norint perkelti vienos prekės „kanban“ tarp sandėlių ir gamybos vietų, kur medžiaga naudojama. Išėmimo „kanban“ palaiko atgalinio planavimo medžiagų papildymo sprendimą, kuriame tam, kad būtų suaktyvintas tiekimas pagal tam tikrą poreikį, reikia atgalinio planavimo signalo. 

Toliau pateiktame scenarijuje parodyta atgalinio planavimo papildymo sistema, kurioje atgalinio planavimo signalas suaktyvina „kanban“ kūrimą, siekiant gamybos procesą papildyti medžiagomis. 

[![Atgalinio planavimo signalas suaktyvina „kanban“ kūrimą, siekiant gamybos procesą papildyti medžiagomis.](./media/material-replenishment-with-withdrawal-kanban.png)](./media/material-replenishment-with-withdrawal-kanban.png)

1.  Išėmimo „kanban“
2.  „Kanban“ vieta „nuo“ ir sandėlio darbo padėjimo vieta
3.  „Kanban“ vieta „į“ ir gamybos įvesties vieta
4.  Gamybos procesas
5.  Sandėlio darbas „kanban“ paėmimui
6.  Sandėlio vietos žaliavoms
7.  Medžiagų sandėlis
8.  Gamybos sandėlis

Šiuo atveju gamybos proceso metu (4) gamybos sandėlyje (8) naudojamos medžiagos iš gamybos įvesties vietos (3). Kai suvartojamas medžiagos sandėliavimo vienetas („kanban“), jis registruojamas kaip tuščias. Sukuriami papildymo signalai prekės kilmei ir sukuriamas naujas „kanban“ (1). Šiuo atveju prekės kilmę sudaro vietos medžiagų sandėlyje (7). „Kanban“ medžiagos paimamos ir padedamos į tame pačiame sandėlyje esančią vietą (2). Kai medžiagos paimamos, jos yra paruoštos būti perkėlimui iš vietos 2 į gamybos įvesties vietą (3) gamybos sandėlyje (8).

## <a name="configure-warehouse-work-for-kanban-picking-for-the-withdrawal-kanban"></a>Sandėlio darbo konfigūravimas „kanban“ paėmimui, skirtam išėmimo„kanban“

Norėdami įgalinti žaliavų paėmimą išėmimo „kanban“, sukonfigūruokite bangos šablonus, darbo šablonus ir vietos nurodymus darbo užsakymo tipui **„Kanban“ paėmimas**. Šis darbo užsakymo tipas palaiko ne tik paėmimo procesą išėmimo „kanban“. Jis taip pat palaiko paėmimo procesą gamybos „kanban“. Tačiau galite konfigūruoti atskirą paėmimo procesą kiekvieno tipo „kanban“, atskirdami bangos šablonus, darbo šablonus ir vietos nurodymus. Norėdami atskirti bangos šablonus, darbo šablonus ir vietos nurodymus, nustatykite veiklos tipo kriterijus (**Apdoroti** arba **Perkelti**) šių objektų užklausose.

## <a name="configure-the-withdrawal-kanban"></a>Išėmimo „kanban“ konfigūravimas

Perkėlimo veikla, naudojama išėmimo „kanban“, yra sukonfigūruota kaip suaktyvinto veiklos plano „Lean“ gamybos eigoje dalis. Konfigūruodami perkėlimo veiklą, nurodote toliau perkėlimo vietas „iš“ ir „į“. Sukonfigūravę perkėlimo veiklą, galite ją priskirti tipo **Išėmimas** „kanban“ taisyklei. „Kanban“ taisyklė nustato strategijas ir išėmimo „kanban“ konfigūracijas. „Kanban“ skaičius nurodo, kiek sandėliavimo vieneto vienetų „kanban“ perkelia perkėlimo proceso metu. Pasirinkus fiksuoto papildymo strategiją, naudojamas fiksuotas „kanban“ kiekis. Šis kiekis nurodo, kiek „kanban“ reikia, kad būtų išvengta atsargų ar kuriamų atsargų pasibaigimo poreikio šaltinyje. Fiksuotas kiekis gali būti apskaičiuotas pagal faktinį poreikį, praeities poreikį ir paslaugų lygius. Šiuose dviejuose atvejuose aprašoma, kaip galite valdyti medžiagų papildymą, kuriame naudojama išėmimo „kanban“.

## <a name="scenario-1-replenish-a-production-input-location-by-using-a-fixed-withdrawal-kanban"></a>1 atvejis. Papildymas gamybos įvesties vietoje, naudojant fiksuotą išėmimo „kanban“

Gamybos proceso metu naudojamos įsigytos žaliavos iš gamybos įvesties vietos, kurios yra gamybos sandėlyje. Kai iš tiekėjo gaunamos žaliavos, jos saugomos medžiagų sandėlio vietose. Kadangi medžiagų poreikis yra laikomas stabiliu per tam tikrą laikotarpį, nustatyta produkciją tiekti fiksuoto kiekio „kanban“ srautu. Kai „kanban“ gamybos įvesties vietoje suvartojamas, užregistruojamas signalas Tuščias ir prie srauto pridedamas to paties tipo naujas „kanban“. 

Galima sukonfigūruoti, kad signalas Tuščias automatiškai atsirastų, kai „kanban“ baigtas. Taip pat signalą Tuščias galima nustatyti kaip neautomatinę sąveiką, kuri pateikiama iš „Kanban“ perkėlimo srities arba rankinio įrenginio meniu. „Kanban“ perkėlimo sritis yra darbo sritis, kurioje valdomos visos „kanban“ ciklo veiklos. 

Sukūrus „kanban“, žaliavos bangos eilutė pridedama prie medžiagų sandėlio „kanban“ bangos. „Kanban“ perkėlimo srities skyriuje Išrinkimo dokumentas galima stebėti medžiagų būseną ir susijusius sandėlio procesus nuo bangos kūrimo iki darbo kūrimo, kol medžiagos turimos vietoje „perkelti iš“ ir yra paruoštos perkėlimui į gamybos įvesties vietas. „Kanban“ galima atlikti „Kanban“ perkėlimo srityje arba naudojant rankinio įrenginio meniu. 

Šiuo atveju paėmimo darbas medžiagų sandėlyje vykdomas kaip viena veikla. Perkėlimo veikla tarp medžiagų sandėlio ir gamybos sandėlio vykdoma kaip atskira veikla. Šis metodas gali būti naudingas, pavyzdžiui, jei tarp dviejų sandėlių yra didelis fizinis atstumas. Šiuo atveju „kanban“ perkėlimo veikla gali reikšti sunkvežimio krovinį. 

Jei atstumas tarp sandėlių vietų ir gamybos įvesties vietos yra nedidelis, gali būti efektyviau į paėmimo procesą įtraukti perkėlimo veiklą. Tada, kai medžiagos yra paimtos, jos gali būti padėtos tiesiai į gamybos įvesties vietą. Siekiant palaikyti šį procesą, galite konfigūruoti perkėlimo veiklą, kad ji būtų automatiškai baigta, kai įvykdomas išėmimo „kanban“ paėmimo darbas.

## <a name="scenario-2-automatically-complete-the-transfer-activity-when-kanban-picking-work-is-processed"></a>2 atvejis. Automatinis perkėlimo veiklos užbaigimas, įvykdžius „kanban“ paėmimo darbą

Šiuo atveju išėmimo „kanban“ perkėlimo veikla sukonfigūruota perkelti tarp dviejų vietų, esančių tame pačiame sandėlyje. Išėmimo „kanban“ perkėlimo veikla nustatyta taip, kad būtų baigta automatiškai. 

[![Perkėlimo veikla baigiama automatiškai, kai įvykdomas „kanban“ paėmimo darbas.](./media/transfer-activities-when-processing-kanban-picking.png)](./media/transfer-activities-when-processing-kanban-picking.png)

1.  Bendrai naudojamas sandėlis, skirtas žaliavoms ir gamybai
2.  Sandėlio vietos žaliavoms
3.  „Kanban“ vieta „nuo“ ir sandėlio darbo padėjimo vieta
4.  Išėmimo „kanban“
5.  Gamybos įvesties vieta
6.  Gamybos procesas

Kai „kanban“ gamybos įvesties vietoje suvartojamas, „kanban“ užregistruojamas kaip Tuščias ir prie srauto pridedamas naujas „kanban“. Sukūrus „kanban“, bangos eilutė pridedama prie „kanban“ bangos. Apdorojus „kanban“ bangą, sukuriamas sandėlio darbas „kanban“ paėmimui. Sandėlio darbininkas vykdo „kanban“ paėmimą ir vadovaudamasis darbu paima medžiagas „kanban“ sandėlio vietoje. Šiam sandėlio darbininkui patvirtinus paėmimą, „kanban“automatiškai užbaigiamas, o sandėlio darbininkui nurodoma padėti medžiagas į gamybos įvesties vietą.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]