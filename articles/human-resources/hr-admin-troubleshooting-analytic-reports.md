---
title: Analizės ataskaitų trikčių diagnostika
description: Šiame straipsnyje paaiškinama, kaip spręsti ir diagnozės problemas, jei kliento duomenų pakeitimai neateis į bet kurią kliento darbo sritį.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e6ae8931679feb2103172eb1a21649734acd995
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902233"
---
# <a name="troubleshoot-analytic-reports"></a>Analizės ataskaitų trikčių diagnostika


[!INCLUDE [PEAP](../includes/peap-2.md)]

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
