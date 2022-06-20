---
title: Peržiūrėti, tvarkyti ir tvirtinti suplanuotus užsakymus
description: Šiame straipsnyje pateikiama informacija apie tai, kaip peržiūrėti, tvarkyti ir tvirtinti suplanuotus užsakymus planavimo optimizavime.
author: t-benebo
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 22c690222cdb72e2113ea137a05da21f315e5a33
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887434"
---
# <a name="view-manage-and-approve-planned-orders"></a>Peržiūrėti, tvarkyti ir tvirtinti suplanuotus užsakymus

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie tai, kaip peržiūrėti, tvarkyti ir tvirtinti suplanuotus užsakymus planavimo optimizavime.

## <a name="view-and-manage-planned-orders"></a><a name="view-planned-orders"></a>Peržiūrėti ir tvarkyti suplanuotus užsakymus

Galite peržiūrėti ir tvarkyti suplanuotus užsakymus bet kuriame suplanuotų užsakymų sąrašo puslapyje. Pereikite į vieną iš šių vietų, atsižvelgiant į suplanuotų užsakymų, su kuriuos norite dirbti, tipą:

- Bendrojo planavimo \> darbo sričių \> bendrasis planavimas
- Bendrasis planavimas \> Bendrasis planavimas \> Suplanuoti užsakymai
- Eikite į Gamybos kontrolė \> Gamybos užsakymai \> Suplanuoti gamybos užsakymai.
- Pasirinkite Įsigijimas ir šaltinio pasirinkimas \> pirkimo užsakymai \> Suplanuoti pirkimo užsakymai
- Atsargų valdymas \> Gaunami užsakymai \> Suplanuoti perkėlimai
- Atsargų valdymas \> Siunčiami užsakymai \> Suplanuoti perkėlimai

## <a name="view-and-edit-the-status-of-planned-orders"></a>Peržiūrėkite ir redaguoti suplanuotų užsakymų būseną

Galite naudoti kiekvieno **suplanuoto** užsakymo lauką Būsena, kad būtų galima sekti progresą arba pakeisti suplanuoto užsakymo eigą. Galimos šios **Būsenos** reikšmės:

- **Neapdorota** - Kai bendrasis planavimas sugeneruoja suplanuotus užsakymus, pagal jų būseną. Šios būsenos suplanuoti užsakymai bus panaikinti kito planavimo vykdymo metu.
- **Baigta** – ši būsena nurodo, kad suplanuotas užsakymas baigtas. Jei nenorite patvirtinti suplanuoto užsakymo, galite rankiniu būdu nustatyti būseną *Baigta*. Atkreipkite dėmesį, kad sistema valdo *Neapdorota* ir *Baigta* būsenas vienodai.
- **Patvirtinta** – ši būsena nurodo, kad suplanuotas užsakymas patvirtintas patvirtinti. Jei norite patvirtinti suplanuotą užsakymą, galite pakeisti būseną į *Patvirtinta*. Jei norite palikti suplanuoto užsakymo redagavimus arba jei planuojate patvirtinti suplanuotą užsakymą, pakeiskite jo būseną į *Patvirtinta*. Suplanuoti užsakymai, kurių būsena Yra *Patvirtinta*, bendrojo planavimo metu laikomi fiksuotais ir tikėtinais tiekimo užsakymais. Todėl vėliau vykdant bendrąjį planavimą jos nėra modifikuojami ar naikinami. Norint tai pasiekti, planavimo logika kopijuoja *patvirtintus* būseną turinčius suplanuotus užsakymus iš senosios plano versijos į naująją plano versiją bendrojo planavimo metu. Atkreipkite dėmesį, kad suplanuoti užsakymai, turintys *Patvirtinta* būseną, yra laikomi numatyto tiekimo tik konkrečiame pagrindiniame plane.

Norėdami pakeisti vieno suplanuoto užsakymo būseną, atidarykite bet kurį suplanuotų užsakymų sąrašo puslapį, atidarykite užsakymą ir [atlikite](#view-planned-orders) vieną iš šių veiksmų:

- **Bendrajame** „FastTab“ pakeiskite lauko Būsena **vertę**.
- Veiksmų juostoje skirtuke **Suplanuotą užsakymą** grupėje **Apdorojimas** grupėje rinkitės **Keisti būseną**.
- Norėdami pažymėti užsakymą kaip patvirtintą, veiksmų srityje pasirinkite **Tvirtinti**.

Norėdami vienu metu pakeisti kelių suplanuotų užsakymų būseną, atidarykite bet kurį suplanuotų užsakymų sąrašo puslapį, pažymėkite kiekvieno norimo keisti užsakymo žymės langelį, tada atlikite [vieną](#view-planned-orders) iš šių veiksmų:

- Veiksmų juostoje skirtuke **Suplanuotą užsakymą** grupėje **Apdorojimas** grupėje rinkitės **Keisti būseną**.
- Norėdami pažymėti užsakymus kaip patvirtintus, veiksmų srityje pasirinkite **Tvirtinti**.

## <a name="approve-planned-orders"></a>Suplanuotų užsakymų tvirtinimas

Atkreipkite dėmesį, kad suplanuotų užsakymų patvirtinimas yra pasirinktinis veiksmas, skirtas sukurti patvirtintą suplanuotą užsakymą.

Šioje iliustracijoje parodyta, kaip galite naudoti **būsenos** vertę, priskirtą kiekvienam suplanuotam užsakymui, norėdami įdiegti patvirtinimo darbo eigą. Norėdami įdiegti patvirtinimo procesą, rankiniu būdu koreguokite **kiekvieno** suplanuoto užsakymo būsenos vertę, kaip aprašyta ankstesniame skyriuje.

![Suplanuoto užsakymo srautas.](media/approved-planned-orders-1.png)

> [!TIP]
> Rekomenduojame patvirtinti bet kuriuos modifikuotus suplanuotus užsakymus. Kitu atveju redagavimų bus nepaisoma ir perrašoma kito planavimo metu.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Galutinai suplanuoti užsakymai](planned-order-firming.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
