---
title: „Power BI“ turinys Darbuotojo tobulėjimas
description: Šioje temoje aprašomas „Power BI“ turinys Darbuotojo tobulėjimas.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9524be3b56efce4ef587f118fcec3567416b3195
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751267"
---
# <a name="employee-development-power-bi-content"></a>„Power BI“ turinys Darbuotojo tobulėjimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas **Darbuotojų tobulėjimo** „Microsoft Power BI“ turinys.

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
| Dabartinis darbuotojas         | Darbininkų dabartinę dieną, amžius ir darbininkų skaičius                                                         | Įmonė, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), darbuotojo pareigos, demografiniai duomenys, užduotis, darbas, pareigos |
| Data                     | Dienos, savaitės, mėnesiai ir metai                                                                             | Buvusių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas, darbuotojo tendencija |
| Demografiniai duomenys             | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis                                                   | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Užimtumas               | Pradžios data, pabaigos data ir perėjimo data                                                                  | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Geografinė vieta      | Miestas, seniūnija, pašto kodas ir šalis arba regionas                                                           | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbas                      | Funkcija, tipas ir pareigos                                                                                  | Dabartinės pareigos, dabartinis darbuotojas |
| Ankstesnis pareigų priskyrimas | Priskyrimo priežastis, pradžios data, pabaigos data ir užduotis                                                           | Kalendoriaus poslinkis, data, darbas, pareigos |
| Pozicija                 | Padalinys, FTE, pareigos, pareigų tipas ir pareigos                                                        | Dabartinės pareigos, dabartinis darbuotojas |
| Pareigų tendencija           | Pareigos per tam tikrą laikotarpį, FTE ir užduotis                                                                          | Kalendoriaus poslinkis, data, darbas, pareigos |
| Ataskaitos               | Vardas, pavardė ir vardas bei pavardė                                                                       | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Atleistas darbuotojas      | Atleisti darbininkai, atleidimo data, pareigos ir užduotis                                             | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), kalendoriaus poslinkis, data, darbuotojo pareigos, demografiniai duomenys, darbas, užduotis, pareigos |
| Darbuotojo vardas ir pavardė            | Vardas, pavardė ir vardas bei pavardė                                                                       | Dabartinis darbininkas, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojo pareigos           | Pareigos ir paaukštinimo data                                                                                   | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojų tendencija           | Darbininkai per tam tikrą laiką, darbininkų skaičius, įmonė ir pareigos                                                        | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), kalendoriaus poslinkis, data, darbuotojo pareigos, demografiniai duomenys, darbas, užduotis |
| Darbas                      | Funkcija, tipas ir pareigos                                                                                  | Dabartinis darbuotojas, dabartinės pareigos, darbuotojo tendencija, darbui reikiami įgūdžiai, ankstesnių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas |
| Darbui reikiamas įgūdis      | Svarba, įvertinimas, įgūdis ir įgūdžio lygis                                                                 | Darbas |
| Darbuotojų įgūdžių analizė  | Patvirtintas, lygis, lygio data ir įgūdis                                                                    | Darbuotojo vardas ir pavardė, įgūdis |
| Našumas              | Įvertinimas, aprašas ir įvertinimo modelis                                                                      | Dabartinis darbuotojas, dabartinės pareigos, darbuotojo tendencija, darbui reikiami įgūdžiai, ankstesnių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas |
| Įgūdis                    | Įgūdis, įgūdžio tipas ir įvertinimas                                                                              | Darbuotojo įgūdžių analizė, darbui reikiamii įgūdžiai |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]