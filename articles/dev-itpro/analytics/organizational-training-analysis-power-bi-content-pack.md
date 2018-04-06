---
title: "Organizacinio mokymo „Power BI“ turinys"
description: "Šioje temoje aprašytas „Finance and Operations“ organizacinio mokymo „Power BI“ turinys."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 18567a3241fce02e17df368f544e545fad93e1d9
ms.contentlocale: lt-lt
ms.lasthandoff: 03/23/2018

---

# <a name="organizational-training-power-bi-content"></a>Organizacinio mokymo „Power BI“ turinys

[!include[banner](../includes/banner.md)]


Šioje temoje aprašytas „Finance and Operations“ organizacinio mokymo „Power BI“ turinys. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Į turinio paketą įtrauktos ataskaitos
Prijungus turinio paketą prie „Finance and Operations“ duomenų, ataskaitose rodomi jūsų organizacijos duomenys. Jei niekada nenaudojote „Microsoft Power BI“, daugiau apie tai galite sužinoti temoje [„Power BI“ mokymosi vedlio puslapis](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Į turinio paketą įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita          | Turinys                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurso analizė | Registravimas pagal vietą, kurso dalyvius pagal jų būseną ir registracijos sąrašą |
| Kursų tipai    | Kursų tipai pagal įgūdžius                                                       |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
„Finance and Operations“ duomenys naudojami ataskaitoms organizacinio mokymo turinio pakete užpildyti. Toliau pateiktoje lentelėje nurodomi objektai, kuriais turinio paketas pagrįstas.

| Objektas                    | Turinys                                                         | Ryšiai su kitais objektais                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Kalendoriaus poslinkiai ataskaitoms skaidyti                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | Įmonės, pagal kurias filtruojamos ataskaitos                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | Kursai, aprašas, dėstytojo vardas, vieta, kabinetas ir būsena | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Darbotvarkė, kursas, pradžios ir pabaigos laikas                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | Vardas, būsena, užduotis ir registracijos data                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Įgūdis, įgūdžio tipas ir lygis                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | Dienos, savaitės, mėnesiai ir metai                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | Pradžios data, pabaigos data ir perėjimo data                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | Funkcija, tipas ir pareigos                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | Pareigos ir etato ekvivalentas (FTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | Vardas, pavardė ir vardas bei pavardė                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Pareigos ir paaukštinimo data                                         | Training\_CourseAttendees                                                                                                                                                                          |





