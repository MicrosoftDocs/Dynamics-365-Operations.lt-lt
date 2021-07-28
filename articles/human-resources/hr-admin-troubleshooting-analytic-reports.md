---
title: Analizės ataskaitų trikčių diagnostika
description: Šiame straipsnyje paaiškinama, ką daryti, jei kliento duomenų keitimai nerodomi jokioje darbo srityje.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 382780405b2496cc655451790ef4a99ef60ba129
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354257"
---
# <a name="troubleshoot-analytic-reports"></a>Analizės ataskaitų trikčių diagnostika

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Išduoti**

Kliento duomenų keitimai nerodomi jokios kliento darbo srities skirtuke **Analizė**.

**Priežastis**

Pagal numatytuosius nustatymus „Microsoft Power BI“ ataskaitos atnaujinamos kas keturias valandas pagal matavimo vieneto paketinės užduoties visuotinio diegimo grafiką.

**Skiriamoji geba**

Ši problema gali būti tik laikina. Norėdami paleisti paketinę užduotį ir atnaujinti analizės darbo sritis, atlikite šiuos veiksmus.

1. Atidarykite puslapį **Paketinės užduotys**, esantį **Sistemos administravimas \> Saitai \> Paketinės užduotys \> Paketinės užduotys**. Arba naudokite iešką ir įveskite **Paketinės užduotys**.
1. Sąraše raskite užduotį **Matavimo vieneto visuotinis diegimas**.
1. Puslapio viršuje pasirinkite **Redaguoti** ir nustatykite suplanuotos paleidimo datos arba laiko vertę, pagal kurią analizė bus atnaujinta arčiau dabartinio laiko.

![Paketinės užduotys.](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]