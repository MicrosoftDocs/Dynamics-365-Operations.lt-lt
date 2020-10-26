---
title: Savikainos elemento dimensijos narių susiejimas į bendrą dimensijos narių rinkinį
description: Susiedami skirtingus savikainos elemento dimensijos narius su bendruoju savikainos elemento dimensijos narių rinkiniu jūs suliejate duomenis į bendrąjį analizės tikslais naudojamą formatą.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6a9618a762d3af840beb05d86518b3588118e80
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976360"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Savikainos elemento dimensijos narių susiejimas į bendrą dimensijos narių rinkinį

[!include [banner](../includes/banner.md)]

Susiedami skirtingus savikainos elemento dimensijos narius su bendruoju savikainos elemento dimensijos narių rinkiniu jūs suliejate duomenis į bendrąjį analizės tikslais naudojamą formatą.

Jeigu esate pasaulinė įmonė ir atitinkate nustatytus apskaitos reikalavimus, galite naudoti kelis sąskaitų planus. Importuodami savikainos elemento dimensijos narius iš skirtingų sąskaitų planų galite gauti sąskaitų rinkinį. Tačiau šios sąskaitos iš tiesų gali būti to paties pobūdžio ir jūs ko gero norėsite jas analizuoti ir paskirstyti joms savikainą naudodami bendrąjį formatą.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Susieti savikainos elemento dimensijos narius su bendruoju formatu
Toliau pateikiamame pavyzdyje nurodoma, kaip jūs, kadangi esate savikainos valdytojas, savikainos apskaitoje galite sukurti naują savikainos elemento dimensiją, kurią naudojant savikainos elemento dimensijos nariai iš JAV sąskaitų plano struktūros ir Prancūzijos sąskaitų plano struktūros susiejami su bendruoju savikainos elemento dimensijos narių rinkiniu. Po to naudodami bendrąjį savikainos elemento dimensijos narių rinkinį galite analizuoti savikainos apskaitos didžiojoje knygoje pateiktus savikainos duomenis iš šių dviejų juridinių subjektų.

| Šaltinis: JAV sąskaitų planas                                          | Šaltinis: Prancūzijos sąskaitų planas                                          | Naujas bendrasis savikainos elemento dimensijos narių rinkinys                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Savikainos elemento dimensijos nariai importuoti iš JAV sąskaitų plano | Savikainos elemento dimensijos nariai importuoti iš Prancūzijos sąskaitų plano | JAV ir Prancūzijos savikainos elemento dimensijos narių susiejimas su bendruoju rinkiniu |
| 5001: Pardavimai                                                           | 5001: Pardavimai ir reklama                                               | 5000: Pardavimai ir reklama                                             |
| 5030: Reklama                                                     | 6390: atsargų pirkimas\*                                                    | 7000: Valymo išlaidos                                                 |
| 7001: Valymo išlaidos                                               | 7001: Kelionės išlaidos                                                      | 7001: Kelionės išlaidos                                                   |

\*Atsargų pirkimo Prancūzijos savikainos elemento dimensijos narys nesusietas.

## <a name="currency-conversion"></a>Valiutos konvertavimas
Įvairūs jūsų naudojami sąskaitų planai gali būti nustatyti naudoti skirtingas valiutas. Šiuo atveju būtinai nurodykite valiutos keitimo kursą, kad savikainos duomenys būtų apdorojami naudojant teisingą valiutą, nurodytą savikainos apskaitos didžiojoje knygoje, kurioje naudojami savikainos elemento dimensijos nariai. Kaip nurodoma pirmiau pateiktame pavyzdyje, jeigu savikainos apskaitos didžiojoje knygoje naudojami JAV doleriai (USD), norėdami apdoroti susietų savikainos elemento dimensijos narių operacijas turite sukurti valiutos konvertavimą iš USD į eurus (EUR).

## <a name="update-mappings-at-any-time"></a>Naujinti susiejimus bet kuriuo metu
Savikainos elemento dimensijos susiejimo apibrėžimus galite atnaujinti bet kuriuo metu. Kadangi susiejimai įsigalioja ne nuo tam tikros datos, pakeitimai taikomi kitą kartą apdorojant savikainos operacijas arba atliekant savikainos skaičiavimus.



