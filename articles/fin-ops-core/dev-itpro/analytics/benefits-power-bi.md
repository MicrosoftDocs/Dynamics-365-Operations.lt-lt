---
title: „Power BI“ turinys Išmokos
description: Šioje temoje aprašomas „Power BI“ turinys Išmokos.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5a894ebfb79eab4888178c930b9e7d55cf735c91
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093086"
---
# <a name="benefits-power-bi-content"></a>„Power BI“ turinys Išmokos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI“ turinys **Išmokos**. Joje paaiškinama, kaip pasiekti į turinį įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudotus turiniui kurti.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Išmokos** rodomas darbo srityje **Išmokų valdymas**, jei naudojate vieną iš toliau nurodytų produktų.

- „Microsoft Dynamics 365 Finance“
- „Microsoft Dynamics 365 Human Resources“

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos
Į „Power BI“ turinį **Išmokos** įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                      | Turinys                                                                                       |
|-----------------------------|------------------------------------------------------------------------------------------------|
| Registracijos išmokoms gauti apžvalga | Daugiausiai ir mažiausiai įtraukti planai, registracija pagal darbuotojų grupę ir pasirinkto išmokų plano parinktys |
| Darbuotojų išmokos           | Darbuotojo registravimas pagal pasirinktą išmoką                                                        |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Tolesniais duomenimis pildomos „Power BI“ turinio **Išmokos** ataskaitos. Šioje lentelėje nurodomi objektai, kuriais pagrįstas turinys.

| Objektas                   | Turinys                                                                                                   | Ryšiai su kitais objektais |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalendoriaus poslinkis          | Kalendoriaus poslinkiai ataskaitoms skaidyti                                                                          | Buvusių pareigų priskyrimas, pareigų tendencija, darbuotojo tendencija, atleistas darbuotojas |
| Įmonė                  | Įmonės, pagal kurias filtruojamos ataskaitos                                                                             | Dabartinė kompensacija, dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Kompensacija             | Užmokesčio tarifas ir dažnis per tam tikrą laikotarpį                                                                           | Dabartinė kompensacija, dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Dabartinė kompensacija     | Užmokesčio tarifas ir dažnis dabartinę dieną                                                              | Įmonė, kompensacija, demografiniai duomenys, darbas, pareigos |
| Dabartinės pareigos         | Pareigos dabartinę datą, viso etato ekvivalentas (FTE), laisvos darbo vietos ir laisvos / užimtos darbo vietos | Darbas, pareigos |
| Dabartinis darbuotojas         | Darbuotojai dabartinę dieną, amžius ir darbuotojų skaičius                                                         | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), darbuotojo pareigos, demografiniai duomenys, užduotis, darbas, pareigos, išmokos |
| Data                     | Dienos, savaitės, mėnesiai ir metai                                                                             | Buvusių pareigų priskyrimas, pareigų tendencija, atleistas darbuotojas, darbuotojo tendencija |
| Demografiniai duomenys             | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis                                                   | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Užimtumas               | Pradžios data, pabaigos data ir perėjimo data                                                                  | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Geografinė vieta      | Miestas, seniūnija, pašto kodas ir šalis arba regionas                                                           | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbas                      | Funkcija, tipas ir pareigos                                                                                  | Dabartinės pareigos, dabartinis darbuotojas |
| Ankstesnis pareigų priskyrimas | Priskyrimo priežastis, pradžios data, pabaigos data ir užduotis                                                           | Kalendoriaus poslinkis, data, darbas, pareigos |
| Pozicija                 | Padalinys, FTE, pareigos, pareigų tipas ir pareigos                                                        | Dabartinės pareigos, dabartinis darbuotojas |
| Pareigų tendencija           | Pareigos per tam tikrą laikotarpį, FTE ir užduotis                                                                          | Kalendoriaus poslinkis, data, darbas, pareigos |
| Ataskaitos               | Vardas, pavardė ir vardas bei pavardė                                                                       | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Atleistas darbuotojas      | Atleisti darbuotojai, atleidimo data, pareigos ir užduotis                                           | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), kalendoriaus poslinkis, data, darbuotojo pareigos, demografiniai duomenys, darbas, užduotis, pareigos, išmokos |
| Išmokos                 | Galiojimo data, išmokos parinktis, išmokos planas ir išmokos tipas                                             | Dabartinis vardas ir pavardė, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojo vardas ir pavardė            | Vardas, pavardė ir vardas bei pavardė                                                                       | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojo pareigos           | Pareigos ir paaukštinimo data                                                                                   | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojų tendencija           | Darbuotojai per tam tikrą laiką, darbuotojų skaičius, įmonė ir pareigos                                                        | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), kalendoriaus poslinkis, data, darbuotojo pareigos, demografiniai duomenys, darbas, užduotis, išmokos |
