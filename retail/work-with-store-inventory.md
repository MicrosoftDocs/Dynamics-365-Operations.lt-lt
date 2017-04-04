---
title: "Valdyti parduotuvės atsargas"
description: "Šiame straipsnyje aprašoma rūšių dokumentų, kuriuos naudodami galite valdyti atsargas."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Valdyti parduotuvės atsargas

Šiame straipsnyje aprašoma rūšių dokumentų, kuriuos naudodami galite valdyti atsargas.

Valdyti savo organizacijos atsargoms galite naudoti tolesnius dokumentų tipus.

## <a name="purchase-orders"></a>Pirkimo užsakymai
Pirkimo užsakymai kuriami pagrindiniame biure. Jeigu mažmeninės prekybos sandėlis yra įtrauktas į pirkimo užsakymo antraštė, užsakymą galima gauti parduotuvėje naudojant šiuolaikinės POS (MPOS) arba debesies POS Microsoft Dynamics 365 operacijų - mažmeninės prekybos. Įvedę kiekius, gautus į parduotuvę, jie gali būti išsaugotas vietos papildomų pakeitimų. Taip pat kiekiai gali būti fiksuojami ir siunčiami į pagrindinį biurą. Pagrindiniame biure, kiekiai, kurie buvo gauti parduotuvėje rodomos Dynamics 365 operacijoms, kad **gauti dabar** lauko pirkimo užsakymą.

## <a name="transfer-orders"></a>Perkėlimo užsakymai
Perkėlimo užsakyme galima nurodyti, kad tam tikra parduotuvė yra vieta, iš kurios gali būti siunčiamos prekės. Tokiu atveju perkėlimo užsakymo atrodo parduotuvėje kaip MPOS arba debesies POS išrinkimo užklausa. Po to, kai kiekiai, kuriuos prašoma skinami, jie padarė ir išsiųstas į pagrindinį biurą. Pagrindiniame biure, kiekiai, kurie buvo surinkti parduotuvėje rodomos Dynamics 365 operacijoms, kad **siųsti dabar** lauko perkėlimo užsakyme. Perkėlimo užsakyme galima nurodyti, kad tam tikra parduotuvė yra vieta, į kurią gali būti siunčiamos prekės. Tokiu atveju perkėlimo užsakymo atrodo parduotuvėje kaip MPOS arba debesies POS gauna prašymą. Įvedę kiekius, gautus į parduotuvę, jie gali būti išsaugotas vietos papildomų pakeitimų. Taip pat kiekiai gali būti fiksuojami ir siunčiami į pagrindinį biurą. Pagrindiniame biure, kiekiai, kurie buvo gauti parduotuvėje rodomos Dynamics 365 operacijoms, kad **gauti dabar** lauko perkėlimo užsakymo.

## <a name="stock-counts"></a>Inventorizacijos
Inventorizacijos gali būti planinės arba neplaninės. Planinės inventorizacijos inicijuojamos pagrindiniame biure, kuris nurodo, kurias prekes reikia skaičiuoti. Pagrindinis biuras sukuria apskaitos dokumentą, kurią gali gauti į parduotuvę, kur faktiškai turimų išteklių kiekį įrašyti į MPOS arba debesies POS. Neplaninės inventorizacijos inicijuojamos parduotuvėje ir faktinės turimų atsargų kiekiai yra atnaujinami MPOS arba debesies POS. Skirtingai nuo planinės inventorizacijos neplanines inventorizacijas neturi numatytojo sąrašo elementų. Alikus bet kurio tipo inventorizaciją, ji fiksuojama ir siunčiama į pagrindinį biurą. Pagrindiniame biure inventorizacija patikrinama ir registruojama.




