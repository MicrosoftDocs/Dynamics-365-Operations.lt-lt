---
title: " Mažmeninės prekybos išrašų parduotuvės konfigūracijos"
description: Ši procedūra nurodo parduotuvės konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami prekybos išrašai.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b73282abd2df92b3f466f7c1c6c210173001fd7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023394"
---
# <a name="store-configurations-for-retail-statements"></a> Mažmeninės prekybos išrašų parduotuvės konfigūracijos

[!include[task guide banner](../includes/task-guide-banner.md)]

Ši procedūra nurodo parduotuvės konfigūracijas, kurios turi įtakos, kaip kuriami ir registruojami prekybos išrašai. Parduotuvių finansiniai aspektai aprašyti kitoje procedūroje. Šioje procedūroje naudojama demonstracinė įmonė USRT.

1. Pasirinkę **Naršymo sritis** eikite į **Moduliai > Mažmeninė prekyba ir prekyba > Kanalai > Parduotuvės > Visos parduotuvės**.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Spustelėkite **Redaguoti**.
5. „fastTab“ **Išrašas / uždarymas** parametrai taikomi kuriant, tikrinant ir skelbiant parduotuvės išrašus. Išplėskite „fastTab“ **Išrašas / uždarymas**.  
6. Lauke **Išrašo metodas** pasirinkite metodą, kurį norite naudoti išrašo eilutėms grupuoti.  
7. Lauke **Vienas išrašas per dieną** pasirinkite Taip, jei kuriant išrašus pagal išrašų kūrimo paketinę užduotį per dieną turėtų būti sukuriamas tik vienas išrašas.  
8. Lauke **Mokėjimo priemonių deklaravimo skaičiavimas** nustatyta, ar mokėjimo priemonių deklaracijos turėtų būti sudedamos kartu, ar turėtų būti naudojama paskutinė deklaracija.  
9. Lauke **Apvalinimas** pasirinkite didžiosios knygos sąskaitą, kurioje bus skelbiami apvalinimo skirtumai.  
10. Lauke **Didžiausias apvalinimo skirtumas** įveskite didžiausią leidžiamą apvalinimo skirtumą.
11. Lauke **Registravimas** įveskite didžiausią bendrą registravimo skirtumą, leidžiamą išrašui.
12. Lauke **Pamaina** įveskite didžiausią bendrą pamainos skirtumą išraše.  
13. Lauke **Operacija** įveskite didžiausią bendrą skirtumą išrašo eilutėje.  
14. Lauke **Uždarymo metodas** nustatykite, ar operacijos, kurios bus įtrauktos į išrašą, turėtų priklausyti uždarytai pamainai, ar tai gali būti bet kokios operacijos nustatytu datos ir (arba) laiko intervalu.  
15. Lauke **Darbo dienos pabaiga** įveskite laiką, jei operacijos, įvykusios po vidurnakčio, turėtų būti registruojamos ankstesnę dieną.  
16. Pasirinkite parinkties **Registruoti kaip darbo dieną** nuostatą Taip, jei operacijos, įvykusios po vidurnakčio, turėtų būti registruojamos ankstesnę dieną.  
17. Pasirinkite parinkties **Skaidyti pagal išrašo metodą** nuostatą Taip, kad išrašai būtų sukurti pagal kiekvieną nustatytą išrašų metodą. Tai gali būti naudinga, jei registravimo efektyvumą reikia tobulinti parduotuvėse, kuriose atliekama daug operacijų, nes tokiu atveju būtų sukurta daug mažesnių išrašų, kuriuos galima apdoroti lygiagrečiai.  
18. „fastTab“ **Bendra**, lauke **Numatytasis klientas**, galite pasirinkti kliento sąskaitą, skirtą naudoti pardavimui atėjusiems klientams.  

