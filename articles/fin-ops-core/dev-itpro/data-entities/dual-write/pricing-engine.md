---
title: Sinchronizavimas pagal poreikį naudojant „Dynamics 365 Supply Chain Management” kainodaros mechanizmą
description: Šioje temoje aprašoma, kaip naudoti „Dynamics 365 Sales” kainodaros mechanizmą programoje „Microsoft Dynamics 365 Supply Chain Management”.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 5ffc0358ff58b2a05aa84b4467a27d88b5e1ec42
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270341"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Sinchronizavimas pagal poreikį naudojant „Dynamics 365 Supply Chain Management” kainodaros mechanizmą

[!include [banner](../../includes/banner.md)]



„Microsoft Dynamics 365 Supply Chain Management” apima kainodaros mechanizmą, kuris tvarko prekybos sutartis, kainoraščius, kliento lojalumo programas, akcijas ir nuolaidas. Kainodaros mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pasiūlymo ar užsakymo kainą. Kai naudojate dvigubą rašymą, naudojate statinę kainodarą arba kainodaros mechanizmą iš „Dynamics 365 Supply Chain Management”, esantį programos „Dynamics 365 Sales” pasiūlymo ir užsakymo puslapiuose.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Kainodaros mechanizmo iš „Supply Chain Management”, esančio „Sales“ programoje, naudojimas

1. Programoje „Sales“ eikite į **Pardavimas \>Užsakymai**.
2. Norėdami sukurti užsakymą pasirinkite **Naujas** arba sąraše **Mano užsakymai** pasirinkite esamą užsakymą.
3. Įtraukite naują užsakymo eilutę.
4. Jei kuriate naują užsakymą, veiksmų srityje pasirinkite **Kainos užsakymas**. Jei atnaujinate esamą užsakymą, veiksmų srityje pasirinkite **Perskaičiuoti**.

    Automatiškai užpildomi šie laukai:

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

Kai pasirenkate „Sales“ programoje **Kainos užsakymas**, tada funkcija **Bendrosios sumos**, esanti „Supply Chain Management” skirtuke **Pardavimo užsakymas \> Peržiūrėti**, iškviečiama susietam pardavimo užsakymui. „Sales“ programoje užsakymo bendrosios sumos reikšmės yra naudojamos užpildyti atitinkamus „Supply Chain Management” laukus.

Kai pardavimo užsakymo bendroji suma apskaičiuojama programoje „Supply Chain Management”, skaičiavimu įvertinamos esamos kliento prekybos sutartys ir pardavimo sutartys bei produktai, kurie išvardyti pardavimo užsakyme. Ši informacija naudojama apskaičiuoti bendrąsias sumas. Pasirinkus **Kainos užsakymas**, „Sales“ automatiškai rodo visus parametrus, nustatytus programoje „Supply Chain Management”.

## <a name="limitations"></a>Apribojimai

Kai užpildyti „Sales“ laukai, taikomi šie apribojimai:

+ „Supply Chain Management” mokesčių ir išlaidų paskirstymo sąranka nėra dubliuojama programoje „Sales“.
+ Kainodaroje neatsižvelgiama į specialią mažmeninės prekybos kainodarą, nurodytą lauke **Mažmeninės prekybos kanalas**, esančiame „Supply Chain Management” pardavimo užsakymo eilutės puslapyje.
+ Neatsižvelgiama į nuolaidas, nurodytas „Supply Chain Management” skyriuje **Prekybos nuolaidų valdymas**.
