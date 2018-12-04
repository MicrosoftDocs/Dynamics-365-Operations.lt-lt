---
title: "Ataskaita Užregistruotų ilgalaikio turto keitimų taikymas"
description: "Šioje temoje paaiškinama, kaip naudoti ataskaitą Užregistruotų ilgalaikio turto keitimų taikymas."
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 16f7c199fb4c9905c465e5d4596d3eaa90104b83
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Ataskaita Užregistruotų ilgalaikio turto keitimų taikymas

[!include [banner](../includes/banner.md)]

Ataskaitoje **Užregistruotų ilgalaikio turto keitimų taikymas** lengvai skaitomu „Microsoft Excel“ formatu teikiami išsamūs ilgalaikio turto duomenys, kurių reikia uždarant laikotarpius, finansinėse ataskaitose ir mokesčių ataskaitose. Į ataskaitą įtraukiami ilgalaikio turto pradžios ir pabaigos balansai bei laikotarpio vertinimo judėjimas ir visas per laikotarpį įvykęs naujas turto įsigijimas bei likvidavimas. Rengiamos atskiro ilgalaikio turto duomenų ataskaitos ir apibendrinamos ilgalaikio turto grupių bei juridinio subjekto reikšmės.

Ataskaitoje **Užregistruotų ilgalaikio turto keitimų taikymas** naudojama elektroninių ataskaitų (ER) sistema. Kad galėtumėte vykdyti ataskaitą, iš „Microsoft Dynamics Lifecycle Services“ (LCS) reikia importuoti konfigūracijas Ilgalaikio turto modelis ir Užregistruotų ilgalaikio turto keitimų taikymas. Instrukcijų ieškokite [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Ši ataskaita pasiekiama sprendime „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3“ arba kaip „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) karštoji pataisa. Aplinkose su 2017 m. liepos mėn. leidimu reikia pritaikyti tris tolesnes karštąsias pataisas.

- **KB 4041754:** iš LCS nepavyksta atsisiųsti elektroninių ataskaitų (ER) konfigūracijos, nes, pritaikius platformos naujinimo paketą, dabartinei programos versijai tai netaikytina
- **KB 4056107:** elektroninių ataskaitų (GER) 5 kaupiamasis naujinimas
- **KB 4056353:** ilgalaikio turto ataskaitos Išrašas ir Pastabos neatitinka GAAP ir IFRS reikalavimų

Toliau pateikiamoje lentelėje aprašomi laukai, kuriuos galima naudoti ataskaitoje.


|                    Laukas                    |                                                                                                                                aprašymas                                                                                                                                |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|              Balansai: pradiniai              |                                                                                           Ilgalaikio turto balansinė vertė dieną „nuo“, kuri nurodyta ataskaitoje.                                                                                           |
|              Balansai: galutiniai              |                                                                                            Ilgalaikio turto balansinė vertė dieną „iki“, kuri nurodyta ataskaitoje.                                                                                            |
|         Įsigijimai: pradinė vertė         |                                                 Visų tipų <strong>Įsigijimas</strong> ir <strong>Įsigijimo koregavimas</strong> operacijų suma iki dienos „nuo“, kuri nurodyta ataskaitoje.                                                  |
|      Įsigijimai: laikotarpio įsigijimai      |                                                 Visų tipų <strong>Įsigijimas</strong> ir <strong>Įsigijimo koregavimas</strong> operacijų, registruotų ataskaitos datų intervale, suma.                                                  |
|       Įsigijimai: laikotarpio likvidavimai        |                                                                        Visų registruotų įsigijimų atšaukimų, su kuriais ataskaitos datų intervale buvo atlikta likvidavimo operacija, suma.                                                                        |
|         Įsigijimai: galutinė vertė         |                                                  Visų tipų <strong>Įsigijimas</strong> ir <strong>Įsigijimo koregavimas</strong> operacijų suma iki dienos „iki“, kuri nurodyta ataskaitoje.                                                   |
|        Nusidėvėjimas: pradinė vertė         | Visų tipų <strong>Nusidėvėjimas</strong>, <strong>Nusidėvėjimo koregavimas</strong>, <strong>Specialioji nusidėvėjimo nuolaida</strong> ir <strong>Visiškas nusidėvėjimas</strong> operacijų suma iki dienos „nuo“, kuri nurodyta ataskaitoje. |
|     Nusidėvėjimas: laikotarpio nusidėvėjimas     |                         Visų tipų <strong>Nusidėvėjimas</strong>, <strong>Nusidėvėjimo koregavimas</strong> ir <strong>Visiškas nusidėvėjimas</strong> operacijų, registruotų ataskaitos datų intervale, suma.                          |
| Nusidėvėjimas: specialusis laikotarpio nusidėvėjimas |                                                              Visų tipo <strong>Specialioji nusidėvėjimo nuolaida</strong> operacijų, registruotų ataskaitos datų intervale, suma.                                                               |
|       Nusidėvėjimas: laikotarpio likvidavimai       |                                                                       Visų registruotų nusidėvėjimo atšaukimų, su kuriais ataskaitos datų intervale buvo atlikta likvidavimo operacija, suma.                                                                        |
|        Nusidėvėjimas: galutinė vertė         |  Visų tipų <strong>Nusidėvėjimas</strong>, <strong>Nusidėvėjimo koregavimas</strong>, <strong>Specialioji nusidėvėjimo nuolaida</strong> ir <strong>Visiškas nusidėvėjimas</strong> operacijų suma iki dienos „iki“, kuri nurodyta ataskaitoje.  |
|    Vertės padidinimas / sumažinimas: pradinė vertė     |                              Visų tipų <strong>Vertės padidinimo koregavimas</strong>, <strong>Vertės sumažinimo koregavimas</strong> ir <strong>Perkainojimas</strong> operacijų suma iki dienos „nuo“, kuri nurodyta ataskaitoje.                               |
|   Vertės padidinimas / sumažinimas: laikotarpio vertės padidinimas   |                                                                    Visų tipo <strong>Vertės padidinimo koregavimas</strong> operacijų, registruotų ataskaitos datų intervale, suma.                                                                    |
|  Vertės padidinimas / sumažinimas: laikotarpio vertės sumažinimas  |                                                                   Visų tipo <strong>Vertės sumažinimo koregavimas</strong> operacijų, registruotų ataskaitos datų intervale, suma.                                                                   |
| Vertės padidinimas / sumažinimas: laikotarpio perkainojimas  |                                                                        Visų tipo <strong>Perkainojimas</strong> operacijų, registruotų ataskaitos datų intervale, suma.                                                                        |
|   Vertės padidinimas / sumažinimas: laikotarpio likvidavimai   |                                                           Visų registruotų vertės padidinimo, sumažinimo ir perkainojimo atšaukimų, su kuriais ataskaitos datų intervale buvo atlikta likvidavimo operacija, suma.                                                           |
|    Vertės padidinimas / sumažinimas: galutinė vertė     |                               Visų tipų <strong>Vertės padidinimo koregavimas</strong>, <strong>Vertės sumažinimo koregavimas</strong> ir <strong>Perkainojimas</strong> operacijų suma iki dienos „iki“, kuri nurodyta ataskaitoje.                                |
|          Likvidavimai: likvidavimo data           |                                                                                                                Ilgalaikio turto knygos likvidavimo data.                                                                                                                |
|    Likvidavimai: balansinė vertė likviduojant    |                                                                                                    Ilgalaikio turto knygos balansinė vertė likvidavimo metu.                                                                                                    |
|            Likvidavimai: pardavimo vertė            |                                                                                               Ilgalaikio turto knygos su likvidavimo – pardavimo operacija pardavimo vertė.                                                                                                |
|           Likvidavimai: likvidacinė vertė            |                                                                                               Ilgalaikio turto knygos su likvidavimo – nurašymo operacija likvidacinė vertė.                                                                                               |
|           Likvidavimai: pelnas / nuostolis            |                                                                                 Pelno arba nuostolio vertė, apskaičiuojama atliekant ilgalaikio turto knygos likvidavimo operaciją.                                                                                 |


