---
title: "Atnaujinti kaip sumos atvaizduojamos ataskaitų ir dokumentų"
description: "Šioje temoje pateikta informacija apie tai, kaip atnaujinti kaip sumos atvaizduojamos ataskaitų ir kitų dokumentų dėl Estijos, Latvijos, Lietuvos, Lenkijos, Čekijos Respublikos, Vengrijos ir Rusijos."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264254
ms.assetid: 70b32d8d-6fa7-4617-ba74-a74bc6568d6e
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 870341b81e49c9fc677052e9ef87a580892f486f
ms.lasthandoff: 03/31/2017


---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Atnaujinti kaip sumos atvaizduojamos ataskaitų ir dokumentų

Šioje temoje pateikta informacija apie tai, kaip atnaujinti kaip sumos atvaizduojamos ataskaitų ir kitų dokumentų dėl Estijos, Latvijos, Lietuvos, Lenkijos, Čekijos Respublikos, Vengrijos ir Rusijos.

Juridiniams asmenims – Estijos, Latvijos, Lietuvos, Lenkijos, Čekijos Respublikos, Vengrijos ir Rusijos, gali nustatyti vardus, pavardes ir trumpi vardai valiutos vienetų ir padaliniuose. Šiuos pavadinimus galima transformuoti, kaip sumos atvaizduojamos dokumentus ir ataskaitas. Pvz: suma **100,20 lt** gali būti rodomas kaip **100 litų 20 Centas**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Nustatyti valiutos vienetų ir padaliniuose ir trumpoji būdvardžio pavadinimus
Norėdami nustatyti ir trumpoji būdvardžio valiutos vienetų pavadinimai ir padaliniuose už kalbą, atlikite šiuos veiksmus:

1.  Atviros, **valiutų** puslapis.
2.  Pasirinkite valiutą.
3.  Veiksmų srityje spustelėkite **linksniavimas**.
4.  Norėdami įtraukti visas pavadinimas ir trumpas pavadinimas kalba, spustelėkite **naujas** ir užpildykite šiuos laukelius.
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Field**                                                 | **Description**                                                                                                                                                                                                    |
    | **Language**                                              | Pasirinkti šio teksto kalbą.                                                                                                                                                                          |
    | **Vienaskaitos vardininkas (vienetų lauke grupės pavadinimas)**       | Įvesti valiutos vienaskaitos forma. Pvz., vienaskaitos forma litų yra Litas.                                                                                                                         |
    | **Daugiskaitos vardininkas (vienetų lauke grupės pavadinimas)**         | Įvesti valiutos daugiskaitos formą. Pavyzdžiui, įveskite Litai. **Pastaba**: Į **vienaskaitos kilmininkas** ir **Daugiskaitos kilmininkas** laukai galimi pagal pasirinktos kalbos, **kalbos** srityje. |
    | **Vienaskaitos vardininkas srityje (dalis lauke grupės pavadinimas)** | Įvesti valiutos subvienetą vienaskaitos forma.                                                                                                                                                            |
    | **Daugiskaitos vardininkas (dalis lauke grupės pavadinimas)**         | Įveskite daugiskaitos forma kiekviename valiutos.                                                                                                                                                              |
    | **Nuorodos pavadinimas vienetų (trumpasis pavadinimas lauke grupė)**       | Įveskite nustatyti valiutos ISO kodą. Pavyzdžiui, įveskite LTL identifikuoti litui..                                                                                                                             |
    | **Nuorodos pavadinimas dalims (trumpasis pavadinimas lauke grupė)**      | Įvesti valiutos subvienetą pavadinimų. Pavyzdžiui, įveskite Centas.                                                                                                                                         |
    | **Conjunction 'and' between units and parts**             | Pasirinkite, jei norite spausdinti jungtukas "ir" tarp valiutos vienetų ir baldų dalys. Pvz., sąskaitų faktūrų ar ataskaitų, 100,20 lt, suma bus rodoma kaip 100 litų ir 20 Centas.                      |

5.  Click **Save**.



