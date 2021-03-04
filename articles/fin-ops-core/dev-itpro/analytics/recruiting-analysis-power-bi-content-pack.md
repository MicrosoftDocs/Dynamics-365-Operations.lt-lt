---
title: „Power BI“ turinys Įdarbinimas
description: Šioje temoje aprašomas „Power BI“ turinys Įdarbinimas. Jame paaiškinta, kaip pasiekti ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 524b1c29d204c1b013546008b1be7868cbf8db06
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680567"
---
# <a name="recruiting-power-bi-content"></a>„Power BI“ turinys Įdarbinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI“ turinys **Įdarbinimas**. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Įdarbinimas** rodomas darbo srityje **Įdarbinimo valdymas**.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Ataskaitos ir vaizdiniai elementai darbo srityje Įdarbinimo valdymas
Darbo srityje **Įdarbinimo valdymas** yra skirtukas **Analizė**. Šiame skirtuke pateikiamas įdėtasis „Power BI“ įdarbinimo turinys. Turinį sudaro apžvalgos skirtukas ir papildomi skirtukai su išsamia informacija. Tolesnėje lentelėje aprašomos kiekvieno skirtuko ataskaitos.

| Ataskaita               | Turinys |
|----------------------|----------|
| Įdarbinimo apžvalga | Kitų ataskaitų suvestinė |
| Pretendento analizė   | Bendrasis pretendentų skaičius, pretendentai pagal darbo vietą, pretendentų šaltiniai, pretendentų vyrų ir moterų santykis bei pretendentai pagal vietą |
| Pretendento būsena     | Pretendentai pagal tipą ir būseną ir pretendento būsena |
| Įdarbinimo analizė  | Grynasis samdos koeficientas, vidutinis pasamdyti reikiamų dienų skaičius, netinkamos samdos procentas, įdarbinimo išlaidos, įdarbinimo projektų skaičius, pasamdytų ir pretendavusių asmenų santykis ir pretendentai, palyginti su laisvomis darbo vietomis pagal įdarbinimo projektą |

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Toliau pateiktoje lentelėje nurodomi objektai, kuriais buvo pagrįstas „Power BI“ turinys **Įdarbinimas**.

| Objektas               | Turinys                                                         | Ryšiai su kitais objektais |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Pretendentas            | Pretendentai, pasamdyti pretendentai, grynosios samdos koeficientas ir išlaidos          | Pretendento vardas, pavardė, įmonė, kalendoriaus poslinkis, data, geografinė vieta, demografiniai duomenys, darbo vieta, medija, įdarbinimo projektas |
| Pretendento vardas, pavardė       | Pretendento vardas, pavardė ir vardas bei pavardė                   | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Kalendoriaus poslinkis      | Kalendoriaus poslinkiai ataskaitoms skaidyti                                | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Įmonė              | Įmonės, pagal kurias filtruojamos ataskaitos                                   | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Data                 | Dienos, savaitės, mėnesiai ir metai                                   | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Demografiniai duomenys         | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis         | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Dirbantis pretendentas   | Pretendentas, veiklos efektyvumas, pradžios data ir pretendento tipas           | Įmonė, kalendoriaus poslinkis, data, geografinė vieta, pretendento vardas, pavardė, įdarbinimas, našumas, darbo vieta, medija, įdarbinimo projektas |
| Užimtumas           | Pradžios data, pabaigos data ir perėjimo data                        | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Geografinė vieta  | Miestas, seniūnija, pašto kodas ir šalis arba regionas                 | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Darbas                  | Funkcija, tipas ir pareigos                                        | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Publikavimo kanalai                | Pretendentų šaltinis                                             | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Našumas          | Įvertinimas, aprašas ir įvertinimo modelis                            | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Įdarbinimo projektas  | Projekto aprašas, projekto būsena ir laisvos vietos                | Pretendentas, dirbantis pretendentas, atleistas pretendentas |
| Atleistas pretendentas | Atleisti pretendentai, priežastis, veiklos efektyvumas ir atleidimo data | Įmonė, kalendoriaus poslinkis, data, geografinė vieta, našumas, demografiniai duomenys, įdarbinimas, medija, įdarbinimo projektas, pretendento vardas, pavardė |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]