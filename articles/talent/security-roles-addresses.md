---
title: Prieiga prie asmeninių adresų pagal saugos vaidmenį
description: Šioje temoje aiškinama, kaip išspręsti problemą, kai klientas negali pasiekti privačių adresų.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "305425"
---
# <a name="access-to-private-addresses-by-security-role"></a>Prieiga prie asmeninių adresų pagal saugos vaidmenį

[!include [banner](includes/banner.md)]

**Problema**

Klientui sukūrus saugos vaidmens dublikatų ir prisijungus naujuoju vaidmeniu, nerodomi adresai, kurie buvo pažymėti kaip privatūs.

**Skiriamoji geba**

Norėdamas išspręsti šią problemą, klientas turi atlikti nurodytus besidubliuojančio saugos vaidmens veiksmus.

1. Eikite į **Organizacijos administravimas \> Visuotinė adresų knygelė \> Visuotinės adresų knygelės parametrai**.
2. Skirtuke **Privačios vietos sauga** naują saugos vaidmenį iš sąrašo **Galimi vaidmenys** perkelkite į sąrašą **Pasirinkti vaidmenys**.
3. Pasirinkite **Įrašyti**.

![Visuotinės adresų knygelės parametrų puslapis](media/GAD-parameters.png)
