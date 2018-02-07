--- 
title: " Mažmeninės prekybos išrašų parduotuvės konfigūracijos"
description: "Ši procedūra nurodo mažmeninės prekybos parduotuvės konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 45aa0caf6fcef4cc49952557a251dd78f816125e
ms.contentlocale: lt-lt
ms.lasthandoff: 11/14/2017

---
# <a name="store-configurations-for-retail-statements"></a> Mažmeninės prekybos išrašų parduotuvės konfigūracijos

[!include[task guide banner](../includes/task-guide-banner.md)]

Ši procedūra nurodo mažmeninės prekybos parduotuvės konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami mažmeninės prekybos išrašai. Mažmeninės prekybos parduotuvių finansinės dimensijos aprašytos kitoje procedūroje. Šioje procedūroje naudojama demonstracinė įmonė USRT.

1. Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės > Visos mažmeninės prekybos parduotuvės.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Sekcijos Išrašas / uždarymas parametrai turi įtakos kuriant, tvirtinant ir registruojant parduotuvės išrašus.  Atidarykite sekciją Išrašas / uždarymas.  
    * Pasirinkite būdą, kuriuo norite grupuoti išrašo eilutes.  
    * Pasirinkite „Taip“, jei per dieną turi būti kuriamas tik vienas išrašas, kai išrašai kuriami atliekant išrašų kūrimo paketinę užduotį.  
    * Laukas Mokėjimo priemonių deklaravimo skaičiavimas nurodo, ar mokėjimo priemonių deklaravimai turi būti įtraukti kartu, ar paskutinysis turėtų būti naudojamas.  
    * Pasirinkite, į kurią DK sąskaitą registruoti apvalinimo skirtumus.  
    * Lauke Didžiausias apvalinimo skirtumas galite įvesti didžiausią galimą apvalinimo skirtumą.  
    * Lauke Registravimas galite įvesti bendrą didžiausią galimą išrašo registravimo skirtumą.  
    * Lauke Pamaina galite įvesti bendrą didžiausią galimą išrašo pamainos skirtumą.  
    * Lauke Operacija galite įvesti bendrą didžiausią galimą išrašo eilutės skirtumą.  
    * Lauke Uždarymo metodas galite nurodyti, ar operacijos, kurios bus įtrauktos į išrašą, turėtų būti uždarytos pamainos dalis, ar jos gali būti bet kurios nurodytos datos / laiko intervalo operacijos.  
    * Lauke Darbo dienos pabaiga galite įvesti laiką, jei po vidurnakčio atliktos operacijos turėtų būti registruojamos su ankstesnės dienos data.  
    * Pasirinkite „Taip“, jei po vidurnakčio atliktos operacijos turėtų būti registruojamos kaip ankstesnės dienos operacijos.  
    * Pasirinkite „Taip“, jei norite, kad būtų sukurti kiekvieno nurodyto išrašo metodo išrašai. Tai gali būti naudinga, jei registravimo efektyvumą reikia tobulinti parduotuvėse, kuriose atliekama daug operacijų, nes tokiu atveju būtų sukurta daug mažesnių išrašų, kuriuos galima apdoroti lygiagrečiai.  
    * Lauke Numatytasis klientas galite pasirinkti kliento sąskaitą, skirtą naudoti pardavimo operacijose su į parduotuvę atėjusiais klientais.  


