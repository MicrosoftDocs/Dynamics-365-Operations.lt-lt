---
title: Numatytojo kliento kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti numatytąjį klientą, naudotiį kuriant kanalą dalyje Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 79e145c21be9178622b7c105afefecb78062e3b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273591"
---
# <a name="create-a-default-customer"></a>Numatytojo kliento kūrimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti numatytąjį klientą, naudotiį kuriant kanalą dalyje Microsoft Dynamics 365 Commerce.

Kuriant kanalą, reikės pateikti numatytąjį klientą. Numatytąjį klientą galima lengvai sukurti, pirma sukūrus klientų grupę ir klientų adresų knygelė.

## <a name="create-a-customer-group"></a>Klientų grupės kūrimas

Jei klientų grupių dar nėra, galite ją sukurti. Pavyzdžiui, gali būti grupių, apimančių skirtingas klientų grupes, pvz., didmeninė prekyba, mažmeninė prekyba, internetas, darbuotojai ir pan.

Norėdami sukurti klientų grupę, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Klientai \> Klientų grupės**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Langelyje **Klientų grupė** įveskite klientų grupės ID.
1. Langelyje **Aprašas** įveskite tinkamą aprašą.
1. Langelyje **Mokėjimo sąlygos** įveskite tinkamą vertę.
1. Langelyje **Laikotarpis nuo SF termino iki mokėjimo datos** įveskite tinkamą vertę.
1. Langelyje **Numatytoji mokesčių grupė** įveskite mokesčių grupę, jei taikoma.
1. Pažymėkite žymės langelį **Kainos su PVM**, jei taikoma.
1. Langelyje **Numatytojo nurašymo priežastis** įveskite tinkamą vertę, jei taikoma.

Toliau pateiktame vaizde parodytos kelios sukonfigūruotos klientų grupės.

![Klientų grupės.](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>Klientų adresų knygelės kūrimas

Klientas turi būti susietas su adresų knygele. Jeigu adresų knygelė dar nesukurta, reikės ją sukurti.

Norėdami sukurti klientų adresų knygelę, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Adresų knygelės**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Langelyje **Pavadinimas** įveskite pavadinimą.
1. Langelyje **Aprašas** įveskite aprašą.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas adresų knygelės pavyzdys.

![Adresų knygelė.](media/address-book.png)

## <a name="create-a-default-customer"></a>Numatytojo kliento kūrimas

Norėdami sukurti numatytąjį klientą, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Klientai \> Visi klientai**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Išplečiamajame sąraše **Tipas** pasirinkite „Asmuo“.
1. Išplečiamajame sąraše **Kliento sąskaita** pasirinkite arba įveskite sąskaitos numerį (pvz., „100001“).
1. Išplečiamajame sąraše **Vardas** pasirinkite arba įveskite vardą (pavyzdžiui, „Numatytasis“).
1. Išplečiamajame sąraše **Antras vardas** pasirinkite arba įveskite vardą (pavyzdžiui, „Mažmeninė prekyba“).
1. Išplečiamajame sąraše **Pavardė** pasirinkite arba įveskite vardą (pavyzdžiui, „Klientas“).
1. Išplečiamajame sąraše **Valiuta** pasirinkite arba įveskite valiutą (pavyzdžiui, „JAV doleris“).
1. Išplečiamajame sąraše **Valiuta** pasirinkite anksčiau sukurtą klientų grupę.
1. Išplečiamajame sąraše **Adresų knygelės** pasirinkite esamą kliento adresų knygelę.
1. Pasirinkite **Įrašyti**, kad įrašytumėte ir grįžtumėte į naujo kliento informacijos ekraną.

> [!NOTE]
> Nebūtina įtraukti numatytojo kliento adreso.

Toliau pateiktame vaizde parodytas kliento kūrimo pavyzdys.

![Numatytojo kliento kūrimas.](media/default-customer-creation.png)

Toliau pateiktame vaizde parodytas numatytojo kliento konfigūravimas.

![Kliento konfigūravimo pavyzdys.](media/default-customer-configuration1.png)

Dauguma numatytųjų verčių kliento informacijos ekrane gali likti, bet dvi vertes reikia pakeisti.

1. Kliento informacijos ekrane išplėskite **Pardavimo užsakymo numatytieji nustatymai**.
1. Išplečiamajame sąraše **Svetainė** pasirinkite arba įveskite iš anksto sukonfigūruotą svetainę.
1. Išplečiamajame sąraše **Sandėlis** pasirinkite arba įveskite iš anksto sukonfigūruotą sandėlį.

Toliau pateiktame vaizde parodytas kliento konfigūravimo pavyzdys.

![Kliento konfigūravimo pavyzdys.](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Kanalų apžvalga](channels-overview.md)

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
