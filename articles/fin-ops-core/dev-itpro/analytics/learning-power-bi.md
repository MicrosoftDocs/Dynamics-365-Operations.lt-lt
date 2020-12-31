---
title: „Power BI“ turinys Mokymasis
description: Šioje temoje aprašomas „Power BI“ turinys Mokymasis.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 46b7a442470d1fe78ebc5c9d5a0c6e155c0d9918
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685254"
---
# <a name="learning-power-bi-content"></a>„Power BI“ turinys Mokymasis

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI“ turinys **Mokymasis**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos

Į „Power BI“ turinį **Mokymasis** įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                | Turinys |
|-----------------------|----------|
| Mokymosi peržiūra     | Kitų ataskaitų suvestinė |
| Kurso analizė       | Registracija pagal vietą, dalyvis pagal būseną, kursai įmonei pagal tipą ir kursų lankomumas pagal užduotį |
| Registracijos analizė | Registracijos sąrašas |
| Kursų tipai          | Kursų tipai pagal įgūdžius |
| Dėstytojo analizė   | Kursų koeficientas dėstytojams, dėstytojus skaičius, kursai pagal dėstytoją, vienam dėstytojui tenkantys kursai ir kursų darbotvarkė pagal instruktorių |
| Siūlomi kursai       | Kursų sąrašas |
| Kursų dizainas        | Kurso darbotvarkė |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

Tolesniais duomenimis pildomos „Power BI“ turinio **Mokymasis** ataskaitos. Šioje lentelėje nurodomi objektai, kuriais pagrįstas turinys.

| Objektas           | Turinys                                                         | Ryšiai su kitais objektais |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalendoriaus poslinkis  | Kalendoriaus poslinkiai ataskaitoms skaidyti                                | Kurso darbotvarkė, kurso dalyviai |
| Įmonė          | Įmonės, pagal kurias filtruojamos ataskaitos                                   | Kurso darbotvarkė, kurso dalyviai |
| Kursas           | Kursai, aprašas, dėstytojo vardas, vieta, kabinetas ir būsena | Kurso darbotvarkė, kurso dalyviai, kurso įgūdis |
| Kurso darbotvarkė    | Darbotvarkė, kursas, pradžios ir pabaigos laikas                          | Įmonė, kalendoriaus poslinkis, data, kursas |
| Kurso dalyviai | Vardas, būsena, užduotis ir registracijos data                         | Įmonė, kalendoriaus poslinkis, data, kursas, demografiniai duomenys, informacija apie įdarbinimą, kursas, darbuotojo vardas, darbuotojo pareigos, užduotis, padėtis |
| Kurso įgūdis     | Įgūdis, įgūdžio tipas ir lygis                                     | Kursas |
| Data             | Dienos, savaitės, mėnesiai ir metai                                   | Kurso darbotvarkė, kurso dalyviai |
| Demografiniai duomenys     | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis         | Kurso darbotvarkė, kurso dalyviai |
| Užimtumas       | Pradžios data, pabaigos data ir perėjimo data                        | Kurso darbotvarkė, kurso dalyviai |
| Darbas              | Funkcija, tipas ir pareigos                                        | Kurso darbotvarkė, kurso dalyviai |
| Pozicija         | Pareigos ir etato ekvivalentas (FTE)                  | Kurso darbotvarkė, kurso dalyviai |
| Darbuotojo vardas ir pavardė    | Vardas, pavardė ir vardas bei pavardė                             | Kurso dalyviai |
| Darbuotojo pareigos   | Pareigos ir paaukštinimo data                                         | Kurso dalyviai |
