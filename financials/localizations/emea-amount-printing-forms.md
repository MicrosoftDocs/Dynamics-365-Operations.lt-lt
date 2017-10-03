---
title: "Sumų rodymo ataskaitose ir dokumentuose būdo naujinimas"
description: "Šioje temoje pateikiama informacija apie tai, kaip naujinti sumų rodymą ataskaitose ir kituose dokumentuose, skirtuose Estijai, Latvijai, Lietuvai, Lenkijai, Čekijos Respublikai, Vengrijai, ir Rusijai."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3aa3d3e6cff9f3a6ebdbdbab63392dd1ef2cc192
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Sumų rodymo ataskaitose ir dokumentuose būdo naujinimas

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie tai, kaip naujinti sumų rodymą ataskaitose ir kituose dokumentuose, skirtuose Estijai, Latvijai, Lietuvai, Lenkijai, Čekijos Respublikai, Vengrijai, ir Rusijai.

Jei pagrindinis juridinio subjekto adresas yra Estijoje,Latvijoje, Lietuvoje, Lenkijoje, Čekijos Respublikoje, Vengrijoje arba Rusijoje, galite nustatyti valiutos vienetų ir antrinių vienetų visus pavadinimus bei trumpus pavadinimus. Šiuos pavadinimus galima naudoti norint pakeisti sumų rodymo dokumentuose ir ataskaitose būdą. Pvz., **100,20 LT** suma gali būti rodoma kaip **100 litų ir 20 centų**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Valiutos vienetų ir antrinių vienetų visų pavadinimų bei trumpų pavadinimų nustatymas
Norėdami nustatyti valiutos vienetų ir antrinių vienetų visus pavadinimus bei trumpus pavadinimus, atlikite tolesnius veiksmus.

1.  Atidarykite puslapį **Valiutos**.
2.  Pasirinkite valiutą.
3.  Veiksmų srityje spustelėkite **Linksniavimas**.
4.  Norėdami įtraukti kalbos visą ir trumpą pavadinimus, spustelėkite **Naujas** ir užpildykite tolesnius laukus.
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Laukas**                                                 | **Aprašas**                                                                                                                                                                                                    |
    | **Kalba**                                              | Pasirinkti šio teksto kalbą.                                                                                                                                                                          |
    | **Vienaskaitos vardininkas (laukų grupė Vienetų pavadinimas)**       | Įveskite valiutos pavadinimą vienaskaitos forma. Pvz., valiutos litas vienaskaitos forma yra litas.                                                                                                                         |
    | **Daugiskaitos vardininkas (laukų grupė Vienetų pavadinimas)**         | Įveskite valiutos pavadinimą daugiskaitos forma. Pavyzdžiui, įveskite litai. **Pastaba**: laukai **Vienaskaitos kilmininkas** ir **Daugiskaitos kilmininkas** rodomi atsižvelgiant į lauke **Kalba** pasirinktą kalbą. |
    | **Laukas Vienaskaitos vardininkas (laukų grupė Dalių pavadinimas)** | Įveskite valiutos antrinio vieneto pavadinimą vienaskaitos forma.                                                                                                                                                            |
    | **Daugiskaitos vardininkas (laukų grupė Dalių pavadinimas)**         | Įveskite valiutos antrinio vieneto pavadinimą daugiskaitos forma.                                                                                                                                                              |
    | **Trumpas vienetų pavadinimas (laukų grupė Trumpas pavadinimas)**       | Įveskite ISO kodą, kad identifikuotumėte valiutą. Pavyzdžiui, įveskite LTL identifikuoti litui..                                                                                                                             |
    | **Trumpas dalių pavadinimas (laukų grupė Trumpas pavadinimas)**      | Įveskite valiutos antrinio vieneto nominaliąją vertę. Pavyzdžiui, įveskite centas.                                                                                                                                         |
    | **Jungtukas „ir“ tarp vienetų ir dalių**             | Pažymėkite, jei norite spausdinti jungtuką „ir“ tarp valiutos vienetų ir vieneto dalių. Pvz., SF ir ataskaitose 100,20 LTL suma rodoma kaip 100 litų ir 20 centų.                      |

5.  Spustelėkite **Įrašyti**.





