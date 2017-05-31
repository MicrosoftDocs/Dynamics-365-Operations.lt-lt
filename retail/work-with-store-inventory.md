---
title: "Valdyti parduotuvės atsargas"
description: "Šiame straipsnyje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5e5043d5951015fc14d29989ef4cab20a8b24f3b
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="manage-store-inventory"></a>Valdyti parduotuvės atsargas

[!include[banner](includes/banner.md)]


Šiame straipsnyje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai.

Valdyti savo organizacijos atsargoms galite naudoti tolesnius dokumentų tipus.

## <a name="purchase-orders"></a>Pirkimo užsakymai
Pirkimo užsakymai kuriami pagrindiniame biure. Jei mažmeninės prekybos sandėlis įtrauktas į pirkimo užsakymo antraštę, užsakymą parduotuvėje galima gauti naudojant modernų EKA (MPOS) arba debesies EKA, esančius programos „Microsoft Dynamics 365 for Operations“ – versijoje „Retail“. Kai parduotuvės pageidauti kiekiai įvedami, juos galima įrašyti vietoje ir papildomai modifikuoti. Taip pat kiekiai gali būti fiksuojami ir siunčiami į pagrindinį biurą. Pagrindiniame biure parduotuvėje gauti kiekiai rodomi programoje „Dynamics 365 for Operations“, pirkimo užsakymo lauke **Dabartinis gavimas** .

## <a name="transfer-orders"></a>Perkėlimo užsakymai
Perkėlimo užsakyme galima nurodyti, kad tam tikra parduotuvė yra vieta, iš kurios gali būti siunčiamos prekės. Šiuo atveju perkėlimo užsakymas parduotuvėje rodomas kaip MPOS arba debesies EKA paėmimo užklausa. Kai pageidauti kiekiai paimami, jie fiksuojami ir siunčiami į pagrindinį biurą. Pagrindiniame biure parduotuvėje paimti kiekiai rodomi programoje „Dynamics 365 for Operations‟, perkėlimo užsakymo lauke **Dabartinis siuntimas**. Perkėlimo užsakyme galima nurodyti, kad tam tikra parduotuvė yra vieta, į kurią gali būti siunčiamos prekės. Šiuo atveju perkėlimo užsakymas parduotuvėje rodomas kaip MPOS arba debesies EKA gavimo užklausa. Kai parduotuvės pageidauti kiekiai įvedami, juos galima įrašyti vietoje ir papildomai modifikuoti. Taip pat kiekiai gali būti fiksuojami ir siunčiami į pagrindinį biurą. Pagrindiniame biure parduotuvėje gauti kiekiai rodomi programoje „Dynamics 365 for Operations“, perkėlimo užsakymo lauke **Dabartinis gavimas** .

## <a name="stock-counts"></a>Inventorizacijos
Inventorizacijos gali būti planinės arba neplaninės. Planinės inventorizacijos inicijuojamos pagrindiniame biure, kuris nurodo, kurias prekes reikia skaičiuoti. Pagrindinis biuras sukuria inventorizavimo dokumentą, kurį galima gauti parduotuvėje, kurioje faktinių turimų atsargų kiekiai įvedami į MPOS arba debesies EKA. Neplaninės inventorizacijos inicijuojamos parduotuvėje, o faktinių turimų atsargų kiekiai atnaujinami MPOS arba debesies EKA. Skirtingai nei planinės inventorizacijos, neplaninės inventorizacijos neturi iš anksto apibrėžto prekių sąrašo. Alikus bet kurio tipo inventorizaciją, ji fiksuojama ir siunčiama į pagrindinį biurą. Pagrindiniame biure inventorizacija patikrinama ir registruojama.






