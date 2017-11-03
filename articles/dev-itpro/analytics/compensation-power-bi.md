---
title: "„Power BI“ turinys Kompensacija"
description: "Šioje temoje aprašomas „Power BI‟ turinys Kompensacija. Jame paaiškinta, kaip pasiekti ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: daf7232f13b5a2d4262a46f302bfd9e7efd60ead
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="compensation-power-bi-content"></a>„Power BI“ turinys Kompensacija

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomas „Microsoft Power BI‟ turinys **Kompensacija**. Jame paaiškinta, kaip pasiekti ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“ turinys **Kompensacija** rodomas darbo srityje **Kompensacijos valdymas**, jei naudojate vieną iš toliau nurodytų produktų.

- „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.)
- „Microsoft Dynamics 365 for Talent“

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos
Į „Power BI“ turinį **Kompensacija** įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                     | Turinys |
|----------------------------|----------|
| Kompensacijos apžvalga      | Kitų ataskaitų suvestinė |
| Kompensacijos analizė      | Valandiniai ir etatiniai įmonės darbuotojai, visų darbuotojų pagal kompensaciją planas, darbuotojai vyrai ir moterys pagal kompensacijų planą ir darbuotojo kompensacija pagal skyrių |
| Pareigų mokėjimų analizė      | Didžiausias ir mažiausias valandinis ir etatinis atlyginimas, pareigos, kurias užimant atlyginimas didžiausias ir mažiausias ir visą darbo dieną arba ne visą darbo dieną užimamos pareigos |
| Kompensacijos plano analizė | Darbuotojo registravimas pagal pasirinktą išmoką |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>„Power BI“ turinio išplėtimas
Jei naudojate „Microsoft Dynamics 365 for Operations“ versiją 1611 arba „Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.), „Power BI“ turinį **Kompensacija** galite rasti LCS bibliotekoje Bendrai naudojamas turtas. Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinį ir įdiegti jį savo organizacijoje, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md). Norėdami peržiūrėti demonstracinius duomenis, kuriuose parodoma, kaip diegti „Power BI“ turinį, žr. „Office Mix“ [„Power BI“ turinys iš „Microsoft“ ir partnerių „Dynamics Lifecycle Services“](https://mix.office.com/watch/9puyb1b2xs1w).

Įsitikinkite, kad atsisiunčiate tą „Power BI“ turinį **Kompensacija**, kuris taikomas jūsų naudojamai „Microsoft Dynamics 365‟ versijai.

>[!NOTE]
>.pbix failai, kurie pateikiami „Lifecycle Services“, taikomi tik „Finance and Operations“.

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Tolesniais duomenimis pildomos „Power BI‟ turinio **Kompensacija** ataskaitos. Šioje lentelėje nurodomi objektai, kuriais pagrįstas turinys.

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
| Atleistas darbuotojas      | Atleisti darbuotojai, atleidimo data, pareigos ir užduotis                                             | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), kalendoriaus poslinkis, data, darbuotojo pareigos, demografiniai duomenys, darbas, užduotis, pareigos, išmokos |
| Išmokos                 | Galiojimo data, išmokos parinktis, išmokos planas ir išmokos tipas                                             | Dabartinis vardas ir pavardė, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojo vardas ir pavardė            | Vardas, pavardė ir vardas bei pavardė                                                                       | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojo pareigos           | Pareigos ir paaukštinimo data                                                                                   | Dabartinis darbuotojas, atleistas darbuotojas, darbuotojo tendencija |
| Darbuotojų tendencija           | Darbuotojai per tam tikrą laiką, darbuotojų skaičius, įmonė ir pareigos                                                        | Įmonė, kompensacija, geografinė vieta, darbuotojo vardas ir pavardė, atskaitingas (kam), kalendoriaus poslinkis, data, darbuotojo pareigos, demografiniai duomenys, darbas, užduotis, išmokos |

Šie objektai buvo naudojami skaičiuojamiems matams duomenų modelyje sukurti. Tada šie skaičiuojami matai naudojami skaičiuojant pagrindinius efektyvumo indikatorius (KPI) ir ataskaitas, naudojamas turinyje. Jei norite į ataskaitas ir ataskaitų sritį įtraukti papildomų skaičiavimų, galite iš LCS atsisiųsti ir modifikuoti failą .pbix. Šis failas yra numatytasis duomenų modelis, kuris buvo naudojamas turiniui kurti. Atlikę keitimus, galite kurti organizacinį turinio paketą ir ataskaitų sritį, kuriuose yra jūsų įtraukta informacija.

