---
title: Fiksuota gavimo kaina
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti ir naudoti fiksuotas gavimo kainas "Microsoft"Dynamics 365 Supply Chain Management.
author: raprofit
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup, InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: 2630952f395d1a18202698b4d73b67ef4b760194
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907586"
---
# <a name="fixed-receipt-price"></a>Fiksuota gavimo kaina

[!include [banner](../includes/banner.md)]

**Fiksuota gavimo kaina** yra pasirinktis *, kurią galite pasirinkti prekių modelių grupėje, kai naudojate kitą atsargų modelį, nei Standartinė savikaina arba slankusis* *vidurkis*. Ankstesnėse versijose ši Microsoft Dynamics AX pasirinktis buvo pavadinta Standartinė **savikaina**. Jis buvo pervardytas **Fiksuotos gavimo** kainos, kai dynamics 2012 buvo pristatytas AX naujas standartinių išlaidų atsargų modelis. Šiame straipsnyje paaiškinama, kaip konfigūruoti ir naudoti fiksuotas gavimo kainas.Dynamics 365 Supply Chain Management

## <a name="about-fixed-receipt-prices"></a>Apie fiksuotas gavimo kainas

Prekių modelių grupės **puslapyje** **pažymėjus** prekės fiksuotos gavimo kainos žymės langelį, sistema naudoja gavimo kainą kaip standartines atsargų gavimo išlaidas. Jei produkto pirkimo kaina ir numatytoji prekės savikaina, sukonfigūruota produktui, skiriasi, **·** **·** **·** **skirtumas** užregistruojamas fiksuotos gavimo kainos pelno arba fiksuotos gavimo kainos nuostolio sąskaitoje ir yra korespondentinė sąskaita, kurią nurodėte atsargų registravimo šablono puslapyje.

**Fiksuotos** gavimo kainos pasirinktis naudojama kartu su skirtingais atsargų modeliais (pavyzdžiui, "pirmasis į, pirmasis iš" (FIFO); paskutinis į, pirmas iš (LIFO); ir svertinis *vidurkis*), **atsargų** uždarymo ir koregavimo procesas vis tiek sukurs sudengimą ir koregavimus pagal atsargų principą, kurį pasirenkate prekių modelių grupės puslapyje. Tačiau atliekami tik atsargų išduodami koregavimai.

Pavyzdžiui, sukonfigūravote **·** *produktą su prekių modelių grupe, kur atsargų modelio lauke nustatyta FIFO* ir pasirinkta fiksuotos **gavimo** kainos parinktis. Kai atsargas gaunate iš pirkimo užsakymo, atsargų vertė nustatoma į prekės numatytosios savikainos vertę gavimo dokumento metu. Jei išrašote pirkimo užsakymo SF, jei SF kaina skiriasi, sistema registruoja numatytąją išleisto produkto savikainą atsargų sąskaitoje. Jis registruoja skirtumą fiksuotos gavimo kainos pelno arba nuostolio sąskaitoje. Vėliau, kai parduodate produktą arba naudojate jį, tuo metu, kai buvo užregistruota pardavimo užsakymo SF, sistema naudoja prekės einamą vidurkį (nebent naudojate žymėjimą).

Kai vykdote atsargų uždarymo *ir koregavimo procesą*, sistema sukuria sudengimą su pirmu išdavimu pagal pirmą gavimą. Skirtumas tarp gavimo kainos, kuri buvo naudojama gavimu, ir einamuoju vidurkiu, kuris buvo naudojamas išduodant, užregistruojamas naujame kvite.

## <a name="enable-fixed-receipt-prices"></a>Įjungti fiksuotas gavimo kainas

Norėdami įjungti fiksuotas prekės gavimo kainas, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargos \> Prekių modelių grupės**.
2. Sukurkite naują prekės modelio grupę arba pasirinkite esamą modelių grupę.
3. Įkainojimo **metode &išlaidų atpažinimo** "FastTab" pažymėkite žymės langelį **Fiksuota** gavimo kaina.

    > [!NOTE]
    > Jei atsargų modelio lauke nustatyta standartinė **savikaina** **arba** slankusis vidurkis, žymės langelio Fiksuota *gavimo kaina* pažymėti *negalima.*

4. Uždarykite puslapį.

Įgalinę pasirinktį **Fiksuotos gavimo** kainos, turite atnaujinti savo atsargų registravimo šabloną, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Sąranka \> Registravimas \> Registravimas**.
1. Skirtuko Pirkimo **užsakymas stulpelyje** **Pasirinkti pasirinkite** Fiksuotos gavimo **kainos pelnas**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį.
1. Nustatykite naują eilutę taip, kad ji būtų taikoma prekių modelių grupei, kurios fiksuotą gavimo kainodarą įgalinote, ir nurodykite pagrindinę sąskaitą, kuri naudojama pirkimo užsakymų fiksuotos gavimo kainos pelnui įrašyti. Konfigūruokite kitus parametrus taip, kaip reikia.
1. Stulpelyje **Pasirinkti** pasirinkite Fiksuotos gavimo **kainos nuostolis**. Įtraukite naują eilutę, kuri taikoma prekių modelių grupei, kurios fiksuotą gavimo kainodarą įgalinote, ir nurodykite pagrindinę sąskaitą, kuri naudojama pirkimo užsakymų fiksuotos gavimo kainos nuostoliams įrašyti. Konfigūruokite kitus parametrus taip, kaip reikia.
1. Stulpelyje **Pasirinkti pasirinkite** Fiksuotos gavimo **kainos korespondentinė sąskaita**. Įtraukite naują eilutę, kuri taikoma prekių modelių grupei, kurios fiksuotą gavimo kainodarą įgalinote, ir nurodykite pagrindinę sąskaitą, kuri naudojama pirkimo užsakymų fiksuotos gavimo kainos korespondentams įrašyti. Konfigūruokite kitus parametrus taip, kaip reikia.
1. Skirtuko Atsargos **stulpelyje** Pasirinkti **pasirinkite Fiksuotos** gavimo **kainos pelnas**. Įtraukite naują eilutę, kuri taikoma prekių modelių grupei, kurios fiksuotą gavimo kainodarą įgalinote, ir nurodykite pagrindinę sąskaitą, kuri naudojama fiksuotos gavimo kainos pelnui įrašyti atsargoms. Konfigūruokite kitus parametrus taip, kaip reikia.
1. Stulpelyje **Pasirinkti** pasirinkite Fiksuotos gavimo **kainos nuostolis**. Įtraukite naują eilutę, kuri taikoma prekių modelių grupei, kurios fiksuotą gavimo kainodarą įgalinote, ir nurodykite pagrindinę sąskaitą, kuri naudojama fiksuotos gavimo kainos nuostoliams įrašyti atsargomis. Konfigūruokite kitus parametrus taip, kaip reikia.

> [!NOTE]
> Paprastai rekomenduojame, kad laukai Fiksuotos **gavimo kainos pelnas ir** **Fiksuotos** gavimo kainos nuostolis pirkimo užsakymams ir atsargomis naudos tą pačią pagrindinę sąskaitą.

> [!IMPORTANT]
> Kai **pakeičiate** **puslapio** Išleisti produktai lauko Kaina vertę tvarkyti išlaidas "FastTab **·**", sistema automatiškai neįvertėja turimų atsargų. Kaip neautomatinį darbą atidarykite uždarymo **ir** koregavimo puslapį **\>** ir veiksmų srityje pasirinkite Turimo koregavimo funkcija. Tada pasirinkite prekes, kurios yra, ir koreguokite jas pagal dabartinę kainą. Vienas aiškus standartinių išlaidų atsargų modelio naudojimo pranašumas – sistema automatiškai perkainoja turimų atsargų atsargas.
