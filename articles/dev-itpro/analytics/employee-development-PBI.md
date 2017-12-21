---
title: "„Power BI“ turinys Darbuotojo tobulėjimas"
description: "Šioje temoje aprašomas „Power BI‟ turinys Darbuotojo tobulėjimas. Jame paaiškinta, kaip pasiekti ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
author: jcart1106
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: f8ba7a968a1a5b376bac52106671607247f061d9
ms.contentlocale: lt-lt
ms.lasthandoff: 12/01/2017

---

# <a name="employee-development-power-bi-content"></a>„Power BI“ turinys Darbuotojo tobulėjimas

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI‟ turinys **Darbuotojo tobulėjimas**. Jame paaiškinta, kaip pasiekti ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio

Turinio paketą **Darbuotojų tobulėjimas** galite rasti bendrai naudojamo turto bibliotekoje „Microsoft Dynamics Lifecycle Services“ (LCS). Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie savo duomenų, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos
Į „Power BI“ turinį **Darbuotojo tobulėjimas** įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                        | Turinys |
|-------------------------------|----------|
| Darbuotojų tobulėjimo apžvalga | Kitų ataskaitų suvestinė |
| Darbuotojų įgūdžių analizė       | Darbuotojų įgūdžių tipai ir darbuotojų įgūdžiai pagal tipą |
| Darbuotojų įgūdžių lygių analizė | Darbuotojų įgūdžių lygiai pagal skyrių, darbuotojai pagal įgūdžių lygį ir įgūdžių tipą ir mažiausia ir didžiausia įgūdžių lygio reikšmės |
| Įgūdžių šablonas                 | Pasirinkto darbuotojo įgūdžių šablonas |
| Įgūdžių analizė                | Įgūdžiai pagal tipą ir įvertinimą |
| Našumo vertinimo analizė   | Darbuotojai pagal mažiausią ir didžiausią darbo įvertinimą, darbuotojų įvertinimai pagal skyrių, darbuotojai pagal įvertinimą ir pareigų tipą bei didžiausi ir mažiausi įvertinimai pagal pareigas  |
| Darbuotojų našumo analizė | Vadybininko pasirinkti darbuotojo įvertinimai |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
| Objektas                   | Turinys                                                                                                   | Ryšiai su kitais objektais |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalendoriaus poslinkis          | Kalendoriaus poslinkiai ataskaitoms skaidyti                                                                          | Buvusių pareigų priskyrimas, pareigų tendencija, darbuotojo tendencija, atleistas darbuotojas 
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
| Darbas                      | Funkcija, tipas ir pareigos                                                                                      | Dabartinis darbuotojas, dabartinės pareigos, darbuotojo tendencija, darbui reikiami įgūdžiai, ankstesnių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas |
| Darbui reikiamas įgūdis      | Svarba, įvertinimas, įgūdis ir įgūdžio lygis                                                                 | Darbas |
| Darbuotojų įgūdžių analizė  | Patvirtintas, lygis, lygio data ir įgūdis                                                                    | Darbuotojo vardas ir pavardė, įgūdis |  
| Našumas              | Įvertinimas, aprašas ir įvertinimo modelis                                                                      | Dabartinis darbuotojas, dabartinės pareigos, darbuotojo tendencija, darbui reikiami įgūdžiai, ankstesnių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas |
|  Įgūdis                   | Įgūdis, įgūdžio tipas ir įvertinimas                                                                              | Darbuotojo įgūdžių analizė, darbui reikiamii įgūdžiai |                                                                                                                        

Šie objektai buvo naudojami skaičiuojamiems matams duomenų modelyje sukurti. Tada šie skaičiuojami matai naudojami skaičiuojant pagrindinius efektyvumo indikatorius (KPI) ir „Power BI‟ turinyje naudojamas ataskaitas. Jei norite į ataskaitas ir ataskaitų sritį įtraukti papildomų skaičiavimų, galite iš LCS atsisiųsti ir modifikuoti failą .pbix. Šis failas yra numatytasis duomenų modelis, kuris buvo naudojamas „Power BI‟ turiniui kurti. Atlikę keitimus, galite kurti organizacinį turinio paketą ir ataskaitų sritį, kuriuose yra jūsų įtraukta informacija.

