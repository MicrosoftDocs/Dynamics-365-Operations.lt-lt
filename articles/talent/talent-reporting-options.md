---
title: "Ataskaitų parinktys sprendime „Talent“"
description: "Šioje temoje aiškinama, kaip išspręsti problemą, kai klientas nori tinkinti „Microsoft Dynamics 365 for Talent“ ataskaitas arba sukurti naujų ataskaitų."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a>Ataskaitų parinktys sprendime „Talent“

[!include [banner](includes/banner.md)]

**Aplinkos informacija**

Ši problema taikoma visoms aplinkoms.

**Požymis**

Klientas nori tinkinti „Microsoft Dynamics 365 for Talent“ ataskaitas arba sukurti naujų ataskaitų.

**Problema**

Vartotojui nepavyksta tinkinti įdėtųjų „Microsoft Power BI“ ataskaitų.

**Sprendimas**

- „Core HR“ duomenis, kurių srautai juda į „Common Data Service for Apps“, skirtą programoms, galima paskelbti naudojantis „PowerApps“ CDS jungtimi su „Power BI Desktop“. Atminkite, kad „Common Data Service“, skirtoje programoms, pateikiamas „Core HR“ duomenų subrinkinys. Daugiau informacijos apie „Power BI“ ir ataskaitų sritis ieškokite temoje [„Power BI“ ataskaitų ir ataskaitų sričių, naudojant „PowerApps Common Data Service“, kūrimas](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).
- Elektronines ataskaitas (ER) galima naudoti kai kurioms „Talent“ ataskaitoms. Kliento kuriamus tinkinimus galima atlikti per ER konfigūravimo pasirinktis.
- Duomenis į „Microsoft Excel“ arba „Microsoft Word“ galima eksportuoti naudojant įvairius duomenų objektus, pateikiamus „Talent“ integravus jį su „Microsoft Office“.

**Ilgalaikis sprendimas**

Bus pasiekiama papildomų „Power BI“ parinkčių, o „Common Data Service“, skirtai programoms, priklausys daugiau duomenų ir objektų.
