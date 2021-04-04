---
title: Sinchronizavimas su „Supply Chain Management“ kainodaros mechanizmu pareikalavus
description: Šioje temoje aprašoma, kaip naudoti „Dynamics 365 Sales” kainodaros mechanizmą programoje „Microsoft Dynamics 365 Supply Chain Management”.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e2067e83d3f0c98e986873b8eaf1b817de912c0f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570145"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Sinchronizavimas su „Supply Chain Management“ kainodaros mechanizmu pareikalavus

[!include [banner](../../includes/banner.md)]



„Microsoft Dynamics 365 Supply Chain Management” apima kainodaros mechanizmą, kuris tvarko prekybos sutartis, kainoraščius, kliento lojalumo programas, akcijas ir nuolaidas. Kainodaros mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pasiūlymo ar užsakymo kainą. Kai naudojate dvigubą rašymą, naudojate statinę kainodarą arba kainodaros mechanizmą iš „Dynamics 365 Supply Chain Management”, esantį programos „Dynamics 365 Sales” pasiūlymo ir užsakymo puslapiuose.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Kainodaros mechanizmo iš „Supply Chain Management”, esančio „Sales“ programoje, naudojimas

1. Programoje „Sales“ eikite į **Pardavimas \>Užsakymai**.
2. Norėdami sukurti užsakymą pasirinkite **Naujas** arba sąraše **Mano užsakymai** pasirinkite esamą užsakymą.
3. Įtraukite naują užsakymo eilutę.
4. Jei kuriate naują užsakymą, veiksmų srityje pasirinkite **Kainos užsakymas**. Jei atnaujinate esamą užsakymą, veiksmų srityje pasirinkite **Perskaičiuoti**.

    Automatiškai užpildomi šie stulpeliai:

    + Išsami suma
    + Nuolaida %
    + Nuolaida
    + Suma be transportavimo mokesčio
    + Suma su transportavimo mokesčiu
    + Bendra mokesčių suma
    + Iš viso
    
5. Norėdami užtikrinti, kad sistema skaičiuodama kainą atsižvelgtų į prekybos ir pardavimo sutartis, atlikite tolesnius veiksmus.
    1. Pereikite į „Supply Chain Management” aplinką.
    2. Eikite į **Gautinos sumos \> Nustatymai \> Gautinų sumų parametrai**.
    3. Pasirinkite šoninės naršymo juostos skirtuką **Kainos**.
    4. „FastTab“ **Prekybos sutarties vertinimas** atžymėkite parinktį **Įvedimas rankiniu būdu**.

## <a name="how-it-works"></a>Kaip tai veikia

Kai pasirenkate „Sales“ programoje **Kainos užsakymas**, tada funkcija **Bendrosios sumos**, esanti „Supply Chain Management” skirtuke **Pardavimo užsakymas \> Peržiūrėti**, iškviečiama susietam pardavimo užsakymui. „Sales“ programoje užsakymo bendrosios sumos reikšmės yra naudojamos užpildyti atitinkamus „Supply Chain Management” stulpelius.

Kai pardavimo užsakymo bendroji suma apskaičiuojama programoje „Supply Chain Management”, skaičiavimu įvertinamos esamos kliento prekybos sutartys ir pardavimo sutartys bei produktai, kurie išvardyti pardavimo užsakyme. Ši informacija naudojama apskaičiuoti bendrąsias sumas. Pasirinkus **Kainos užsakymas**, „Sales“ automatiškai rodo visus parametrus, nustatytus programoje „Supply Chain Management”.

## <a name="limitations"></a>Apribojimai

Kai užpildyti „Sales“ stulpeliai, taikomi šie apribojimai:

+ „Supply Chain Management” mokesčių ir išlaidų paskirstymo sąranka nėra dubliuojama programoje „Sales“.
+ Kainodaroje neatsižvelgiama į specialią mažmeninės prekybos kainodarą, nurodytą l **Mažmeninės prekybos kanalas** stulpelyje, esančiame „Supply Chain Management” pardavimo užsakymo eilutės puslapyje.
+ Neatsižvelgiama į nuolaidas, nurodytas „Supply Chain Management” skyriuje **Prekybos nuolaidų valdymas**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]