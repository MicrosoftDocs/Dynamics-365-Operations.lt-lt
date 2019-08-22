---
title: „Power BI“ turinys Darbuotojo tobulėjimas
description: Šioje temoje aprašomas „Power BI“ turinys Darbuotojo tobulėjimas.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2e13b43812e0d6f8b50cb3fcf65f277afbe9e806
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849768"
---
# <a name="employee-development-power-bi-content"></a>„Power BI“ turinys Darbuotojo tobulėjimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI“ turinys **Darbuotojo tobulėjimas**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos
Į „Power BI“ turinį **Darbuotojo tobulėjimas** įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                        | Turinys |
|-------------------------------|----------|
| Darbuotojų tobulėjimo apžvalga | Kitų ataskaitų suvestinė |
| Darbuotojų įgūdžių analizė       | Darbuotojų įgūdžių tipai ir darbuotojų įgūdžiai pagal tipą |
| Darbuotojų įgūdžių lygių analizė | Darbuotojų įgūdžių lygiai pagal skyrių, darbuotojai pagal įgūdžių lygį ir įgūdžių tipą ir mažiausia ir didžiausia įgūdžių lygio reikšmės |
| Įgūdžių šablonas                 | Pasirinkto darbuotojo įgūdžių šablonas |
| Įgūdžių analizė                | Įgūdžiai pagal tipą ir įvertinimą |
| Našumo vertinimo analizė   | Darbuotojai pagal mažiausią ir didžiausią darbo įvertinimą, darbuotojų įvertinimai pagal skyrių, darbuotojai pagal įvertinimą ir pareigų tipą bei didžiausi ir mažiausi įvertinimai pagal pareigas |
| Darbuotojų našumo analizė | Vadybininko pasirinkti darbuotojo įvertinimai |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas

| Objektas                   | Turinys                                                                                                   | Ryšiai su kitais objektais |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalendoriaus poslinkis          | Kalendoriaus poslinkiai ataskaitoms skaidyti                                                                          | Buvusių pareigų priskyrimas, pareigų tendencija, darbuotojo tendencija, atleistas darbuotojas |
| Įmonė                  | Įmonės, pagal kurias filtruojamos ataskaitos                                                                             | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Dabartinės pareigos         | Pareigos dabartinę datą, viso etato ekvivalentas (FTE), laisvos darbo vietos ir laisvos / užimtos darbo vietos | Darbas, pareigos |
| Dabartinis darbuotojas         | Darbuotojai dabartinę dieną, amžius ir darbuotojų skaičius                                                         | Įmonė, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), darbuotojo pareigos, demografiniai duomenys, užduotis, darbas, pareigos |
| Data                     | Dienos, savaitės, mėnesiai ir metai                                                                             | Buvusių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas, darbuotojo tendencija |
| Demografiniai duomenys             | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis                                                   | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Užimtumas               | Pradžios data, pabaigos data ir perėjimo data                                                                  | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Geografinė vieta      | Miestas, seniūnija, pašto kodas ir šalis arba regionas                                                           | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbas                      | Funkcija, tipas ir pareigos                                                                                  | Dabartinės pareigos, dabartinis darbuotojas |
| Ankstesnis pareigų priskyrimas | Priskyrimo priežastis, pradžios data, pabaigos data ir užduotis                                                           | Kalendoriaus poslinkis, data, darbas, pareigos |
| Pozicija                 | Padalinys, FTE, pareigos, pareigų tipas ir pareigos                                                        | Dabartinės pareigos, dabartinis darbuotojas |
| Pareigų tendencija           | Pareigos per tam tikrą laikotarpį, FTE ir užduotis                                                                          | Kalendoriaus poslinkis, data, darbas, pareigos |
| Ataskaitos               | Vardas, pavardė ir vardas bei pavardė                                                                       | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Atleistas darbuotojas      | Atleisti darbuotojai, atleidimo data, pareigos ir užduotis                                             | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), kalendoriaus poslinkis, data, darbuotojo pareigos, demografiniai duomenys, darbas, užduotis, pareigos |
| Darbuotojo vardas ir pavardė            | Vardas, pavardė ir vardas bei pavardė                                                                       | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojo pareigos           | Pareigos ir paaukštinimo data                                                                                   | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojų tendencija           | Darbuotojai per tam tikrą laiką, darbuotojų skaičius, įmonė ir pareigos                                                        | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), kalendoriaus poslinkis, data, darbuotojo pareigos, demografiniai duomenys, darbas, užduotis |
| Darbas                      | Funkcija, tipas ir pareigos                                                                                  | Dabartinis darbuotojas, dabartinės pareigos, darbuotojo tendencija, darbui reikiami įgūdžiai, ankstesnių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas |
| Darbui reikiamas įgūdis      | Svarba, įvertinimas, įgūdis ir įgūdžio lygis                                                                 | Darbas |
| Darbuotojų įgūdžių analizė  | Patvirtintas, lygis, lygio data ir įgūdis                                                                    | Darbuotojo vardas ir pavardė, įgūdis |
| Našumas              | Įvertinimas, aprašas ir įvertinimo modelis                                                                      | Dabartinis darbuotojas, dabartinės pareigos, darbuotojo tendencija, darbui reikiami įgūdžiai, ankstesnių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas |
| Įgūdis                    | Įgūdis, įgūdžio tipas ir įvertinimas                                                                              | Darbuotojo įgūdžių analizė, darbui reikiamii įgūdžiai |
