---
title: Užregistruotų ilgalaikio turto keitimų taikymo ataskaita
description: Šiame straipsnyje paaiškinama, kaip naudoti ilgalaikio turto keitimų pirmyn ataskaitą.
author: moaamer
ms.date: 01/08/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: a4d423b149957e624269231aede510190f0c14c7
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068787"
---
# <a name="fixed-assets-roll-forward-report"></a>Užregistruotų ilgalaikio turto keitimų taikymo ataskaita

[!include [banner](../includes/banner.md)]

Ataskaitoje **Užregistruotų ilgalaikio turto keitimų taikymas** lengvai skaitomu „Microsoft Excel“ formatu teikiami išsamūs ilgalaikio turto duomenys, kurių reikia uždarant laikotarpius, finansinėse ataskaitose ir mokesčių ataskaitose. Į ataskaitą įtraukiami ilgalaikio turto pradžios ir pabaigos balansai bei laikotarpio vertinimo judėjimas ir visas per laikotarpį įvykęs naujas turto įsigijimas bei likvidavimas. Rengiamos atskiro ilgalaikio turto duomenų ataskaitos ir apibendrinamos ilgalaikio turto grupių bei juridinio subjekto reikšmės.

Ataskaitoje **Užregistruotų ilgalaikio turto keitimų taikymas** naudojama elektroninių ataskaitų (ER) sistema. Kad galėtumėte vykdyti ataskaitą, iš „Microsoft Dynamics Lifecycle Services“ (LCS) reikia importuoti konfigūracijas Ilgalaikio turto modelis ir Užregistruotų ilgalaikio turto keitimų taikymas. Instrukcijų ieškokite [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Ši ataskaita yra Microsoft Dynamics galima 365 finansų, įmonės leidimas 7.3 arba Microsoft Dynamics kaip karštoji pataisa, skirta 365 finansų, įmonės leidimas (2017 m. liepos mėn.). Aplinkose su 2017 m. liepos mėn. leidimu reikia pritaikyti tris tolesnes karštąsias pataisas.

- **KB 4041754:** iš LCS nepavyksta atsisiųsti elektroninių ataskaitų (ER) konfigūracijos, nes, pritaikius platformos naujinimo paketą, dabartinei versijai tai netaikytina
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

