---
title: "Atsargų kiekių rezervavimas"
description: "Šioje temoje aprašomos skirtingos atsargų rezervavimo parinktys, kurias galima naudoti."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7c351618f4d710062dd8f369c5319cdce79f7339
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="reserve-inventory-quantities"></a>Atsargų kiekių rezervavimas

[!include[banner](../includes/banner.md)]


Šioje temoje aprašomos skirtingos atsargų rezervavimo parinktys, kurias galima naudoti.

Atsargas konkretiems pardavimo užsakymams galite rezervuoti automatiškai. Tai reiškia, kad rezervuotų atsargų kitiems užsakymams iš sandėlio paimti negalima, jei atsargų rezervavimas arba dalis rezervavimo nėra atšaukti.

Toliau pateikiama keletas galimų atsargų rezervavimo priežasčių.
-   Pirmiausia užsakyta, pirmiausia pristatyta – galimas prekes klientai gauna tokia pačia tvarka, kaip pateikia užsakymus.
-   Prekių trūkumas dėl ilgo arba nežinomo pristatymo iš tiekėjo laiko. Galbūt norėsite užtikrinti, kad konkretiems klientams arba pagal konkrečius užsakymus būtų pristatomos pirmos galimos prekės.
-   Konkretūs klientai ir konkretūs užsakymų tipai turi pristatymo pirmenybę.
-   Prekės su serijos ir paketo numeriais. Galite pažymėti konkrečias prekes, kurios buvo arba bus pristatytos pagal konkrečius užsakymus.
-   Specialiai užsakytos prekės, rezervuotos konkretiems užsakymams.
-   Gamybos užsakymai. Pavyzdžiui, galite pažymėti prekes, kurios gaminamos arba pritaikomos konkretiems užsakymams.

Atsargas galima rezervuoti automatiniu būdu, kai sukuriama nauja užsakymo eilutė, arba neautomatiniu būdu individualiems užsakymams. Taip pat galima rezervuoti atsargų skirtinguose gamybos proceso etapuose. Galima rezervuoti tik laikomus produktus. Aptarnavimo rezervuoti negalima, nes nėra jų turimų atsargų. Galima rezervuoti ir faktines turimas atsargas, ir užsakytas, bet dar negautas atsargas. Jei rezervuojamas didesnis kiekis nei turimos atsargos, rodomas pranešimas, kuriame sakoma, kad tokio didelio kiekio rezervuoti negalima. Tada galite vis tiek rezervuoti nurodytą kiekį arba pakeisti užsakomą kiekį. Kiekį galima rezervuoti arba pakeisti. Jei rezervuojama daugiau prekių, nei galima, trūkumas padengiamas kitą kartą, kai atsiranda galimų pristatyti prekių.

## <a name="inventory-reservation-policies"></a>Atsargų rezervavimo strategijos
Atsargų rezervavimo strategijos nustatomos puslapiuose **Prekių modelių grupės**, **Atsargų ir sandėlio valdymo parametrai** ir **Gamybos parametrai**.
### <a name="policies-on-the-item-model-groups-page"></a>Puslapyje Prekės modelių grupės nustatomos strategijos

Dalyje **Atsargų strategijos** pateikiamos toliau nurodytos rezervavimo strategijos.
|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Rezervavimo strategija**  | **Aprašymas**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| FIFO kontrolė pagal datą    | Jei pasirinksite parinktį **FIFO kontrolė pagal datą**, atsargų rezervavimą kontroliuos rūšiavimo data pagal FIFO principą. Paketai rezervuojami naudojant anksčiausią prekių gavimo datą pagal principą „pirmasis į, pirmasis iš“ (FIFO).                                                                                                                                                                                                                                                                       |
| Atgal nuo siuntimo datos | Šią parinktį galima naudoti pažymėjus parinktį **FIFO kontrolė pagal datą**. Jei pasirinksite **Atgal nuo siuntimo datos**, atsargos rezervuojamos atgal pageidaujamos siuntimo datos pagal principą „pirmasis į, pirmasis iš“ (FIFO). Jei iki siuntimo datos nėra galimų kvitų, naudojamas FIFO rezervavimas.                                                                                                                                                                                                           |
| Prekių pardavimo rezervacija  | Nustato, ar prekių rezervavimas vykdomas automatiniu, ar neautomatiniu būdu. Jei rezervavimas vykdomas automatiškai. atsargos rezervuojamos kuriant užsakymo eilutes. Galima rezervuoti KS (parinktis **Automatinis**) arba atskirų KS elementų (parinktis **Išskleidimas**) prekės numerio lygiu. Numatytoji reikšmė **Prekės pardavimo rezervacija** gali būti nuskaityta iš **Gautinų sumų parametrai.** Tame puslapyje reikšmė nustatoma lauke Rezervavimas, kuris yra skirtuko **Bendra** **skyriuje** **Numatytosios pardavimo reikšmės**. |
| To paties paketo parinkimas    | To paties paketo rezervavimas leidžia pardavimo užsakymo eilutės atsargas rezervuoti pagal vieną atsargų paketą. Jei norite naudoti šią parinktį, taip pat turite nustatyti parinktį **Konsoliduoti reikalavimą** į **Taip**. Yra papildomų parametrų, kurių reikia sekimo dimensijų grupei ir saugojimo dimensijų grupei. Daugiau informacijos rasite puslapyje [To paties pardavimo užsakymo paketo rezervavimas](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Konsoliduoti reikalavimą | Ši pasirinktis yra panašu į parinktį **To paties paketo parinkimas** ir ji konsoliduoja rezervuotas pardavimo užsakymo eilučių atsargas į vieną reikalavimą.                                                                                                                                                                                                                                                                                                                                                                                      |
| FEFO kontrolė pagal datą    | Naudojant šią parinktį galima rezervuoti paketus, kurių galiojimo data arba galiojimo pabaigos data yra arti. Taip pat turite nustatyti lauką **Paėmimo kriterijai**, pasirinkdami parinktį **Galiojimo data** arba **Galiojimo pabaigos data**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>FIFO kontrolės pagal datą ir parinkties Atgal nuo siuntimo datos pavyzdžiai

Šiame pavyzdyje pateikiamos trijų skirtingų paketų numerių prekės numerio A turimos atsargos.
| Prekės Nr. | Paketo numeris | Kiekis | Data             |
|-------------|--------------|----------|------------------|
| A           | 1000         | 5        | 2016 m. vasario 2 d. |
| A           | 1001         | 3        | 2016 m. sausio 1 d.  |
| A           | 1002         | 7        | 2016 m. kovo 3 d.    |

Pardavimo užsakymas, kuris turėtų būti automatiškai rezervuotas ir pristatytas 2016 m. balandžio 4 d., rezervuoja toliau nurodytą paketą.
-   Jei atžymėti žymės langeliai **FIFO kontrolė pagal datą** ir **Atgal nuo siuntimo datos**, rezervuojamas paketas 1000, nes jo numeris yra mažiausias.
-   Jei žymės langelis **FIFO kontrolė pagal datą** pažymėtas, o žymės langelis **Atgal nuo siuntimo datos** nepažymėtas, rezervuojamas paketas 1001, nes nustatyta šio paketo data yra pirma gavimo data (FIFO).
-   Jei žymės langeliai **FIFO kontrolė pagal datą** ir **Atgal nuo siuntimo datos** pažymėti, rezervuojamas paketas 1002, nes šio paketo gavimas yra artimiausias pardavimo užsakymo siuntimo datai.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Puslapyje Atsargų ir sandėlio valdymo parametrai pateikiamos strategijos

Galima naudoti dvi toliau nurodytas parinktis, susijusias su rezervavimais puslapyje **Atsargų ir sandėlio valdymo parametrai**.
-   Naudojant skirtuko **Bendra** parinktį **Rezervuoti užsakytas prekes** galite rezervuoti prekių gavimus, kurie užsakomi su prekių išdavimais gautinose sumose, projektų valdyme ir apskaitoje bei gamybos kontrolėje. Jei nepasirinksite šios parinkties, galėsite rezervuoti tik faktiškai gautas prekes. Jei nustatyta priimti tam tikros prekės neigiamas atsargas, šis laukas nėra aktualus.
-   Skirtuko **Transportavimas** parinktis **Rezervuoti prekes automatiškai** nustato numatytąjį parametrą, jei perkėlimo užsakymų prekės rezervuojamos automatiškai. Numatytąjį parametrą galima perrašyti atskiruose perkėlimo užsakymuose.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Puslapyje Gamybos parametrai pateikiamos atsargų rezervavimo strategijos

Puslapio **Gamybos parametrai** skirtuko **Bendra** lauko **Rezervavimas** reikšmė nustato numatytąjį gamybos proceso momentą, kada atsargos turėtų būti rezervuotos. Pvz., atsargos gali būti rezervuotos suplanavus arba pradėjus darbą.

