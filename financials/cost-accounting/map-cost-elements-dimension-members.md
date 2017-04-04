---
title: "Žemėlapyje skirtingų sąnaudų elementas dimensijos nariais į bendrą rinkinį dimensijos nariais"
description: "Susiedami skirtingus savikainos elemento dimensijos narius su bendruoju savikainos elemento dimensijos narių rinkiniu jūs suliejate duomenis į bendrąjį analizės tikslais naudojamą formatą."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-11-01 13 - 45 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a1e9817b6ee596ad516531d7597a2a39e115749c
ms.lasthandoff: 03/31/2017


---

# <a name="map-different-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Žemėlapyje skirtingų sąnaudų elementas dimensijos nariais į bendrą rinkinį dimensijos nariais

Susiedami skirtingus savikainos elemento dimensijos narius su bendruoju savikainos elemento dimensijos narių rinkiniu jūs suliejate duomenis į bendrąjį analizės tikslais naudojamą formatą.

Jeigu esate pasaulinė įmonė ir atitinkate nustatytus apskaitos reikalavimus, galite naudoti kelis sąskaitų planus. Importuodami savikainos elemento dimensijos narius iš skirtingų sąskaitų planų galite gauti sąskaitų rinkinį. Tačiau šios sąskaitos iš tiesų gali būti to paties pobūdžio ir jūs ko gero norėsite jas analizuoti ir paskirstyti joms savikainą naudodami bendrąjį formatą.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Susieti savikainos elemento dimensijos narius su bendruoju formatu
Toliau pateikiamame pavyzdyje nurodoma, kaip jūs, kadangi esate savikainos valdytojas, savikainos apskaitoje galite sukurti naują savikainos elemento dimensiją, kurią naudojant savikainos elemento dimensijos nariai iš JAV sąskaitų plano struktūros ir Prancūzijos sąskaitų plano struktūros susiejami su bendruoju savikainos elemento dimensijos narių rinkiniu. Po to naudodami bendrąjį savikainos elemento dimensijos narių rinkinį galite analizuoti savikainos apskaitos didžiojoje knygoje pateiktus savikainos duomenis iš šių dviejų juridinių subjektų.

| Šaltinis: JAV sąskaitų planas                                          | Šaltinis: Prancūzijos sąskaitų planas                                          | Naujas bendrasis savikainos elemento dimensijos narių rinkinys                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Savikainos elemento dimensijos nariai importuoti iš JAV sąskaitų plano | Savikainos elemento dimensijos nariai importuoti iš Prancūzijos sąskaitų plano | JAV ir Prancūzijos savikainos elemento dimensijos narių susiejimas su bendruoju rinkiniu |
| 5001: Pardavimai                                                           | 5001: Pardavimai ir reklama                                               | 5000: Pardavimai ir reklama                                             |
| 5030: Reklama                                                     | 6390: akcijų pirkimo\*                                                    | 7000: Valymo išlaidos                                                 |
| 7001: Valymo išlaidos                                               | 7001: Kelionės išlaidos                                                      | 7001: Kelionės išlaidos                                                   |

\*Vertybinių popierių pirkimo prancūzų sąnaudų elementas dimensijos valstybės nėra perkoduojama.

## <a name="currency-conversion"></a>Valiutos konvertavimas
Įvairūs jūsų naudojami sąskaitų planai gali būti nustatyti naudoti skirtingas valiutas. Šiuo atveju būtinai nurodykite valiutos keitimo kursą, kad savikainos duomenys būtų apdorojami naudojant teisingą valiutą, nurodytą savikainos apskaitos didžiojoje knygoje, kurioje naudojami savikainos elemento dimensijos nariai. Kaip nurodoma pirmiau pateiktame pavyzdyje, jeigu savikainos apskaitos didžiojoje knygoje naudojami JAV doleriai (USD), norėdami apdoroti susietų savikainos elemento dimensijos narių operacijas turite sukurti valiutos konvertavimą iš USD į eurus (EUR).

## <a name="update-mappings-at-any-time"></a>Naujinti susiejimus bet kuriuo metu
Savikainos elemento dimensijos susiejimo apibrėžimus galite atnaujinti bet kuriuo metu. Kadangi susiejimai įsigalioja ne nuo tam tikros datos, pakeitimai taikomi kitą kartą apdorojant savikainos operacijas arba atliekant savikainos skaičiavimus.


