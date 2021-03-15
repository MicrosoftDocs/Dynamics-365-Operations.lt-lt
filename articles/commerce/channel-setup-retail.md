---
title: Mažmeninės prekybos kanalo nustatymas
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują mažmeninės prekybos kanalą.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 100822ecea03d03267f98654c66e74f2f5924bd9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997730"
---
# <a name="set-up-a-retail-channel"></a>Mažmeninės prekybos kanalo nustatymas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ sukurti naują mažmeninės prekybos kanalą.

## <a name="overview"></a>Peržiūrėti

„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus. Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis). Kiekviename mažmeninės prekybos parduotuvės kanale gali būti naudojami savi mokėjimo būdai, kainų grupės, elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai. Prieš kurdami mažmeninės prekybos parduotuvės kanalą, turite nustatyti visus šiuos elementus. 

Prieš kurdami mažmeninės prekybos kanalą, įsitikinkite, kad išpildėte [kanalo būtinąsias sąlygas](channels-prerequisites.md).

## <a name="create-and-configure-a-new-retail-channel"></a>Naujo mažmeninės prekybos kanalo kūrimas ir konfigūravimas

1. Naršymo srityje eikite **Moduliai \> Kanalai \> Parduotuvės \> Visos parduotuvės**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **Pavadinimas** įveskite naujo kanalo pavadinimą.
1. Lauke **Parduotuvės numeris** pateikite unikalų parduotuvės numerį. Numeris gali būti raidinis-skaitinis, bet ne daugiau kaip iš 10 simbolių.
1. Išplečiamajame sąraše **Juridinis subjektas** įveskite atitinkamą juridinį subjektą.
1. Išplečiamajame sąraše **Sandėlis** įveskite atitinkamą sandėlį.
1. Lauke **Parduotuvės laiko juosta** pasirinkite atitinkamą laiko juostą.
1. Išplečiamajame sąraše **PVM grupė** pasirinkite atitinkamą parduotuvės PVM grupę.
1. Lauke **Valiuta** pasirinkite atitinkamą valiutą.
1. Lauke **Kliento adresų knygelė** nurodykite galiojančią adresų knygelę.
1. Lauke **Numatytasis klientas** pateikite galiojantį numatytąjį klientą.
1. Lauke **Funkcijų šablonas** pasirinkite funkcijų šabloną, jei taikoma.
1. Lauke **El. paštu siunčiamo pranešimo šablonas** pateikite galiojantį el. siunčiamo pranešimo šabloną.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas naujo mažmeninės prekybos kanalo kūrimas.

![Naujas mažmeninės prekybos kanalas](media/channel-setup-retail-1.png)

Toliau pateiktame vaizde parodytas mažmeninės prekybos kanalo pavyzdys.

![Mažmeninės prekybos kanalas](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Kiti parametrai

Yra daug kitų pasirinktinių parametrų, kuriuos galima nustatyti skyriuose **Išrašas / uždarymas** ir **Įvairūs** pagal mažmeninės prekybos parduotuvės poreikius.

Be to, žr. [Elektroninio kasos aparato (EKA) ekrano maketai](pos-screen-layouts.md), kur pateikta informacijos, kaip nustatyti numatytąjį ekrano maketą skyriuje **Ekrano maketas** ir [„Retail Hardware Station“ konfigūravimas ir diegimas](retail-hardware-station-configuration-installation.md), kur pateikta skyriaus **Aparatūros stotys** sąrankos informacija.

Toliau pateiktame vaizde parodytas mažmeninės prekybos kanalo sąrankos konfigūravimas.

![Mažmeninės prekybos kanalo konfigūravimo pavyzdys](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Papildoma kanalų sąranka

Yra papildomų kanalo elementų, kuriuos reikia nustatyti, juos galima rasti dalyje **Veiksmų sritis** skyriuje **Nustatymas**.

Papildomos užduotys, reikalingos interneto kanalo sąrankai, apima mokėjimo metodų, grynųjų pinigų deklaracijų, pristatymo būdų, pajamų / išlaidų sąskaitų, skyrių, vykdymo grupių priskyrimo ir seifų nustatymą.

Šiame vaizde rodomos įvairios papildomos mažmeninės prekybos kanalo nustatymo parinktys skirtuke **Nustatymas**.

![Kanalo nustatymas](media/channel-setup-retail-4.png)

### <a name="set-up-payment-methods"></a>Nustatyti mokėjimo būdus

Norėdami nustatyti kiekvieno mokėjimo tipo, palaikomo šiame kanale, mokėjimo metodus, atlikite toliau nurodytus veiksmus.

1. Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Mokėjimo metodai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Naršymo srityje pasirinkite pageidaujamą mokėjimo metodą.
1. Skyriuje **Bendri** nurodykite **Operacijos pavadinimas** ir konfigūruokite kitus pageidaujamus nustatymus.
1. Konfigūruokite visus papildomus parametrus, kurių reikia mokėjimo tipui.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas mokėjimas grynaisiais pinigais pavyzdys.

![Mokėjimo metodų pavyzdys](media/channel-setup-retail-5.png)

### <a name="set-up-cash-declaration"></a>Grynųjų pinigų deklaravimo nustatymas

1. Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Grynųjų pinigų deklaracija**.
1. Veiksmų **srityje pasirinkite naujas** ir sukurkite visą **taikytiną monetų** ir **pastabų** nominalą.

Toliau pateiktame vaizde parodytas grynųjų pinigų deklaracijos pavyzdys.

![Grynųjų pinigų deklaravimo nustatymas](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Nustatyti pristatymo būdus

Galite peržiūrėti sukonfigūruotus pristatymo būdus pasirikdami **Pristatymo būdai** skirtuke **Nustatymas**, esančiame **Veiksmų sritis**.  

Norėdami pakeisti arba įtraukti pristatymo būdą, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Atsargų valdymas \> Pristatymo būdai**.
1. Veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte naują pristatymo režimą, arba pasirinkite esamą režimą.
1. Skyriuje **Mažmeninės prekybos kanalai** pasirinkite **Įtraukti eilutę**, kad galėtumėte įtraukti kanalą. Kanalų įtraukimas naudojant organizacijos mazgus, užuot įtraukus kiekvieną kanalą atskirai, gali racionalizuoti kanalų įtraukimą.

Toliau pateiktame vaizde parodytas pristatymo būdo pavyzdys.

![Nustatyti pristatymo būdus](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Pajamų/išlaidų sąskaitos nustatymas

Norėdami nustatyti produktų pajamų / išlaidų sąskaitą, atlikite toliau pateikiamus veiksmus.

1. Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Pajamų / išlaidų sąskaita**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Dalyje **Pavadinimas** įveskite pavadinimą.
1. Dalyje **Ieškos pavadinimas** įveskite ieškos pavadinimą.
1. Dalyje **Sąskaitos tipas** įveskite sąskaitos tipą.
1. Įveskite tekstą **1 pranešimų eilutė**, **2 pranešimų eilutė**, **1 kvito tekstas** ir **2 kvito tekstas**, kaip reikia.
1. Dalyje **Registravimas** įveskite registravimo informaciją.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame paveiksle parodytas pajamų / išlaidų sąskaitos pavyzdys.

![Pajamų / išlaidų sąskaitų nustatymas](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Skyrių nustatymas

Norėdami nustatyti skyrius, atlikite tolesnius veiksmus.

1. Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada spustelėkite **Skyriai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Dalyje **Skyriaus numeris** įveskite skyriaus numerį.
1. Dalyje **Aprašas** įveskite aprašą.
1. Dalyje **Skyriaus dydis** įveskite skyriaus dydį.
1. Jei reikia, konfigūruokite parametrus **Bendri** ir **Pardavimo statistika**.
1. Veiksmų srityje pasirinkite **Įrašyti**.

### <a name="set-up-a-fulfillment-group-assignment"></a>Vykdymo grupės priskyrimo nustatymas

Norėdami nustatyti vykdymo grupės priskyrimą, atlikite toliau nurodytus veiksmus.

1. Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada pasirinkite **Vykdymo grupės priskyrimas**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Išplečiamajame sąraše **Vykdymo grupė** pasirinkite vykdymo grupę.
1. Išplečiamajame sąraše **Aprašas** įveskite aprašą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas vykdymo grupės priskyrimo sąrankos pavyzdys.

![Vykdymo grupės priskyrimų nustatymas](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Seifų nustatymas

Norėdami nustatyti seifus, atlikite tolesnius veiksmus.

1. Veiksmų srityje pasirinkite skirtuką **Nustatymas**, tada spustelėkite **Seifai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Įveskite seifo pavadinimą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kanalų apžvalga](channels-overview.md)

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)

[Interneto kanalo nustatymas](channel-setup-online.md)

[Skambučių centro kanalo nustatymas](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]