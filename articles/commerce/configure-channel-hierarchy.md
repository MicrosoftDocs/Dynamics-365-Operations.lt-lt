---
title: Kanalo siekiant naudoti kanalų naršymo hierarchiją konfigūravimas
description: Šiame straipsnyje aprašoma, kaip konfigūruoti kanalą, kad būtų galima naudoti kanalo naršymo hierarchiją Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b15e6eee86880f0315f42b34056385f718cc6bf1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280399"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Kanalo siekiant naudoti kanalų naršymo hierarchiją konfigūravimas


[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti kanalą, kad būtų galima naudoti kanalo naršymo hierarchiją Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Peržiūra

Kanalo naršymo hierarchijos naudojamos, norint skirstyti produktus į kategorijas, kad produktus būtų galima naršyti el. prekybos svetainėje arba elektroniniame kasos aparate (EKA). Mažmeninės prekybos ir internetiniai kanalai turi būti sukonfigūruoti naudojant kanalo naršymo hierarchijas.

## <a name="configure-the-channel"></a>Kanalo konfigūravimas

Norėdami sukonfigūruoti kanalą, kad būtų galima naudoti kanalo naršymo hierarchiją, atlikite tokius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalų kategorijos ir produktų atributai**.
1. Pasirinkite konfigūruotiną kanalą.
1. Veiksmų srityje pasirinkite **Nustatyti atributų metaduomenis**.
1. Išskleidžiamajame sąraše **Kategorijų hierarchija** pasirinkite atitinkamą kanalo naršymo hierarchiją.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Dalyje **Atributų grupė** įtraukite bet kurias atributų grupes, kurios bus visų mazgų visuotiniai atributai.

Toliau pateiktame vaizde parodoma, kaip sukonfigūruoti kanalą, kad būtų galima naudoti kanalo naršymo hierarchiją.

![Kanalo konfigūravimo pavyzdys.](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Nustatyti atributo metaduomenis

Nustačius atributų metaduomenis bus galima konfigūruoti kiekvieno mazgo atributus.

Norėdami nustatyti atributų metaduomenis, atlikite toliau nurodytus veiksmus.

1. Veiksmų srityje pasirinkite **Nustatyti atributų metaduomenis**.
1. Kiekvienam mazgui pasirinkite **Kanalo produktų atributai**.
1. Nustatykite **Rodyti atributus kanale** į **Taip** ir **Galima patikslinti** į **Taip**, kad būtų įjungtos to kanalo tikslinimo priemonės.
1. Sukonfigūravę kiekvieną mazgą taip, kaip pageidaujate, **Veiksmų sritis** pasirinkite mygtuką **Įrašyti**, kad įrašytumėte.
1. Viršutiniame dešiniajame kampe pasirinkite **X**, kad išeitumėte iš šio ekrano ir grįžtumėte į puslapį **Kanalų kategorijos ir produktų atributai**.

Toliau pateiktame paveiksle parodyti kanalo produktų atributų, sukonfigūruotų kanalų kategorijos mazge, pavyzdžiai.

![Kanalo atributai kanalo kategorijos mazge.](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Skelbti pakeitimus

Kad atlikti pakeitimai įsigaliotų, turite juos publikuoti.

Norėdami publikuoti keitimus, atlikite toliau nurodytus veiksmus.

1. Veiksmų srityje pasirinkite **Publikuoti kanalo naujinimus**.
1. Veiksmų srityje **Publikuoti kanalo naujinimus** pasirinkite **Gerai**.

Toliau pateiktame paveiksle parodyta, kaip publikuoti kanalo naujinimus.

![Publikuoti kanalo naujinimus.](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Kanalų naršymo hierarchijos kūrimas](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
