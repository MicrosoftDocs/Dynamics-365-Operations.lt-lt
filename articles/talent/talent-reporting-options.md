---
title: Ataskaitų parinktys sprendime „Talent“
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai klientas nori tinkinti „Microsoft Dynamics 365 Talent“ ataskaitas arba sukurti naujų ataskaitų.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897953"
---
# <a name="reporting-options-in-talent"></a>Ataskaitų parinktys sprendime „Talent“

**Aplinkos informacija**

Ši problema taikoma visoms aplinkoms.

**Požymis**

Klientas nori tinkinti „Microsoft Dynamics 365 Talent“ ataskaitas arba sukurti naujų ataskaitų.

**Išduoti**

Vartotojui nepavyksta tinkinti įdėtųjų „Microsoft Power BI“ ataskaitų.

**Sprendimas**

- „Core HR“ duomenis, kurių srautai juda į „Common Data Service“, galima paskelbti naudojantis „Power Apps“ „Common Data Service“ jungtimi su „Power BI Desktop“. Atminkite, kad „Common Data Service“ pateikiamas „Core HR“ duomenų subrinkinys. Daugiau informacijos apie „Power BI“ ir ataskaitų sritis ieškokite temoje [„Power BI“ ataskaitų ir ataskaitų sričių, naudojant „Power Apps Common Data Service“, kūrimas](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).
- Elektronines ataskaitas (ER) galima naudoti kai kurioms „Talent“ ataskaitoms. Kliento kuriamus tinkinimus galima atlikti per ER konfigūravimo pasirinktis.
- Duomenis į „Microsoft Excel“ arba „Microsoft Word“ galima eksportuoti naudojant įvairius duomenų objektus, pateikiamus „Talent“ integravus jį su „Microsoft Office“.

**Ilgalaikis sprendimas**

Bus pasiekiama papildomų „Power BI“ parinkčių, o „Common Data Service“ priklausys daugiau duomenų ir objektų.
