---
title: „Power BI“ turinys Kompensacija
description: Šioje temoje aprašomas „Power BI“ turinys Kompensacija. Jame paaiškinta, kaip pasiekti ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmCompensationWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 64b4f27b4a1fa3762169a18746c6b0933bddf3ca
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687187"
---
# <a name="compensation-power-bi-content"></a>„Power BI“ turinys Kompensacija

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI“ turinys **Kompensacija**. Jame paaiškinta, kaip pasiekti ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Kompensacija** rodomas darbo srityje **Kompensacijos valdymas**, jei naudojate vieną iš toliau nurodytų produktų.

- „Finance and Operations” programėlės
- „Microsoft Dynamics 365 Human Resources“

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos
Į „Power BI“ turinį **Kompensacija** įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                     | Turinys |
|----------------------------|----------|
| Kompensacijos apžvalga      | Kitų ataskaitų suvestinė |
| Kompensacijos analizė      | Valandiniai ir etatiniai įmonės darbuotojai, visų darbuotojų pagal kompensaciją planas, darbuotojai vyrai ir moterys pagal kompensacijų planą ir darbuotojo kompensacija pagal skyrių |
| Pareigų mokėjimų analizė      | Didžiausias ir mažiausias valandinis ir etatinis atlyginimas, pareigos, kurias užimant atlyginimas didžiausias ir mažiausias ir visą darbo dieną arba ne visą darbo dieną užimamos pareigos |
| Kompensacijos plano analizė | Darbuotojo registravimas pagal pasirinktą išmoką |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Tolesniais duomenimis pildomos „Power BI“ turinio **Kompensacija** ataskaitos. Šioje lentelėje nurodomi objektai, kuriais pagrįstas turinys.

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
