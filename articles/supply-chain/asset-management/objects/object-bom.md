---
title: Turto KS
description: Šioje temoje aprašomos turto KS turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 02686c97a19fa86c3ea93d7c400067f0855b5c4d
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571489"
---
# <a name="asset-boms"></a>Turto KS

[!include [banner](../../includes/banner.md)]

 

Šioje temoje aprašomos turto KS turto valdyme. Puslapyje **Turto KS** rodomas visų elementų (atsarginių dalių ir kitų elementų), naudojamų turtui visą jo ciklą, sąrašas. Kuriant naują turtą reikėtų apsvarstyti turto KS nustatymą kaip sąrankos procedūros dalį. Tokiu būdu galima sekti turto elementų retrospektyvą nuo sukūrimo datos.

Atlikus priežiūros užduotį ir užregistravus elemento suvartojimą darbo užsakyme galima sekti turto atsarginių dalių ir kitų elementų suvartojimą. Ši funkcija leidžia išlaikyti viso turto išsamų elementų suvartojimo įrašą. Pavyzdžiui, galima naudoti įrašą siekiant stebėti, ar konkreti atsarginė dalis dažnai keičiama, sekti atsargines dalis ar kitus elementus, kurie šiuo metu naudojami turtui.

> [!NOTE]
> Darbo užsakyme elementų suvartojimas gali apimti atsargines dalis ir kitus papildomus elementus, pvz., tepalus, varžtus ir tarpiklius.

Turto KS galima automatiškai atnaujinti atsižvelgiant į turto valdymo sąranką. Jei darbo užsakymo ciklo būsena sukurta tvarkyti baigtus darbo užsakymus ir jeigu tos darbo užsakymo ciklo būsenos parinktis **Naujinti turto KS** nustatyta į **Taip** puslapyje **Darbo užsakymo ciklo būsenos**, visi darbo užsakyme naudojami elementai bus automatiškai atnaujinti puslapyje **Turto KS**, kai darbo užsakymas atnaujinamas į tą ciklo būseną. 


Taip pat galima atnaujinti turto KS rankiniu būdu sukuriant naujas elementų eilutes puslapyje **Turto KS**.

Užregistravus elemento suvartojimą darbo užsakyme, puslapyje **Turto KS** galima sekti turto atsarginių dalių retrospektyvą. Jei norite naudoti šią funkciją, turite pasirinkti elementų grupes, kurios turėtų būti naudojamos atsarginių dalių registravimui puslapyje **Atsarginių dalių elementų grupės**.

Norėdami naudoti turto KS funkcijas, pirmiausia turite nustatyti reikiamas atsarginių dalių elementų grupes. Jei norite, kad baigus darbo užsakymą turto KS būtų atnaujinama automatiškai, galite nustatyti, kad šį naujinimą valdytų darbo užsakymo ciklo būsena. 


## <a name="set-up-spare-parts-item-groups"></a>Atsarginių dalių elementų grupių nustatymas

Atsarginių dalių retrospektyvos nustatymas pagrįstas elementų grupėmis, sukurtomis modulyje **Atsargų ir sandėlio valdymas**. Dalyje Turto valdymas nustatomos elementų grupės, kad būtų galima sekti pasirinktų elementų grupių atsarginių dalių retrospektyvą.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \>**Turtas** \> **Atsarginių dalių elementų grupės**.
2. Pasirinkite **Nauja**, kad nustatytumėte elementų grupę.
3. Lauke **Elementų grupė** pasirinkite grupę. Grupės pavadinimas automatiškai įvedamas lauke **Pavadinimas**.

## <a name="view-and-update-asset-boms"></a>Turto KS peržiūra ir naujinimas

Užregistravus elemento suvartojimą darbo užsakyme galima peržiūrėti užregistruoto elemento suvartojimą puslapyje **Turto KS**.

1. Pasirinkite **Turto valdymas** \> **Bendra** \> **Turtas** \> **Aktyvus turtas**. Sąraše pasirinkite turtą, tada pasirinkite **Turto KS**.

    > [!NOTE]
    > Norėdami peržiūrėti visas elemento suvartojimo registracijas visuose turtuose, pasirinkite **Turto valdymas** \> **Užklausos** \> **Turtas** \> **Turto KS**.

2. Pasirinkite **Naujinti turto KS**. Pasirinkus **Pasirinkti** į naujinimą galima įtraukti turtą, turto tipus ir išteklius. Pasirinkite **Gerai**, kad pradėtumėte naujinimą. Taip pat galite nustatyti funkciją Naujinti kaip paketinę užduotį.
3. Jei norite matyti daugiau su elementais susijusios informacijos, galite įtraukti atsargų dimensijas. Pasirinkite **Atsargos** \> **Dimensijų rodymas**, tada pažymėkite dimensijų, kurias norite matyti, žymės langelius. Jei norite, kad šis nustatymas būtų taikomas visam turtui puslapyje **Turto KS**, parinktį **Įrašyti sąranką** nustatykite į **Taip**.
4. Jei norite apžvelgti, kur turto valdyme naudojamas elementas pasirinktoje eilutėje atsižvelgiant į turtą, užduoties tipo numatytąsias reikšmes, atsargines dalis ir darbo užsakymus, pasirinkite **Elementas, kuris naudojamas**. 
5. Jei norite matyti tik aktyvių elementų eilutes, pasirinkite **Rodinys** \> **Dabartinis**. Norėdami peržiūrėti visų elementų eilutes, įskaitant eilutes, kuriose galiojimo pabaigos data yra ankstesnė už dabartinę datą, pasirinkite **Rodinys** \> **Visi**.

> [!NOTE]
> Jeigu baigus darbo užsakymą baigėsi kai kurių elementų ar atsarginių dalių, susijusių su tuo turtu, galiojimas arba jos buvo pakeistos kitais elementais ar atsarginėmis dalimis, rekomenduojame atitinkamai atnaujinti turto KS.

## <a name="create-a-new-item-line-in-an-asset-bom"></a>Naujos elemento eilutės turto KS kūrimas

Turto elementų eilutes galima kurti rankiniu būdu.

1. Puslapyje **Turto KS** pasirinkite **Nauja**.
2. Lauke **turtas** pasirinkite turtą, į kurį norite įtraukti elemento eilutę.
3. Lauke **Eilutės numeris** įveskite eilutės sekos numerį.
4. Lauke **Galioja** įveskite elemento pradžios datą.
5. Jei elementas nustos galioti, lauke **Galiojimo pabaiga** įveskite pabaigos datą.
6. Lauke **Elemento numeris** pasirinkite elementą. Pavadinimas automatiškai įvedamas lauke **Produkto pavadinimas**.
7. Lauke **Kiekis** įveskite naudojamą kiekį. Laukas **Vienetas** atnaujinamas automatiškai.
