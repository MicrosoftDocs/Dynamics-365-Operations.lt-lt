---
title: "Analitinės ataskaitos neatnaujinamos"
description: "Šioje temoje paaiškinama, ką daryti, jei kliento duomenų keitimai nerodomi jokioje darbo srityje."
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
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a>Analitinės ataskaitos neatnaujinamos

[!include [banner](includes/banner.md)]

**Problema**

Kliento duomenų keitimai nerodomi jokios kliento darbo srities skirtuke **Analizė**.

**Priežastis**

Pagal numatytuosius nustatymus „Microsoft Power BI“ ataskaitos atnaujinamos kas keturias valandas pagal matavimo vieneto paketinės užduoties visuotinio diegimo grafiką.

**Skiriamoji geba**

Ši problema gali būti tik laikina. Norėdami paleisti paketinę užduotį ir atnaujinti analizės darbo sritis, atlikite šiuos veiksmus.

1. Atidarykite puslapį **Paketinės užduotys**, esantį **Sistemos administravimas \> Saitai \> Paketinės užduotys \> Paketinės užduotys**. Arba naudokite iešką ir įveskite **Paketinės užduotys**.
1. Sąraše raskite užduotį **Matavimo vieneto visuotinis diegimas**.
1. Puslapio viršuje pasirinkite **Redaguoti** ir nustatykite suplanuotos paleidimo datos arba laiko vertę, pagal kurią analizė bus atnaujinta arčiau dabartinio laiko.

![Paketinės užduotys](media/batch-jobs.png)

