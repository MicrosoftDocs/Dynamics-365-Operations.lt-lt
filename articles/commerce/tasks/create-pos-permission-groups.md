---
title: EKA teisių grupių kūrimas
description: Šioje temoje aiškinama, kaip sukurti POS teisių grupę.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2439d1912b3ca013f4a524f3354923d2a3f76ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221286"
---
# <a name="create-pos-permission-groups"></a>EKA teisių grupių kūrimas

[!include [banner](../includes/banner.md)]

Šioje temoje aiškinama, kaip sukurti POS teisių grupę. Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USRT. Ši užduotis skirta prekybos operacijų vadovo vaidmeniui.

1. Naršymo srityje eikite į **Moduliai > Mažmeninė prekyba ir prekyba > Darbuotojai > Teisių grupės**.
2. Pasirinkite **Naujas**.
3. Lauke **POS teisių grupės ID** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Pažymėkite **Taip** lauke **Peržiūrėti laiko laikrodžio įrašus**. Dabar galite įjungti arba uždrausti įvairias savo EKA teisių grupės teises. Galite nustatyti kai kurių teisių reikšmę, kuri bus naudojama siekiant įvertinti, ar EKA vartotojas gali atlikti veiksmą. Šiame užduočių vadove įjungiamos kelios teisės, kurias galima suteikti kasininkui.  
6. Pažymėkite **Taip** lauke **Leisti kurti užsakymą**.
7. Pažymėkite **Taip** lauke **Leisti redaguoti užsakymą**.
8. Pažymėkite **Taip** lauke **Leisti nuskaityti užsakymą**.
9. Pažymėkite **Taip** lauke **Leisti keisti slaptažodį**.
10. Pažymėkite **Taip** lauke **Leisti anoniminį uždarymą**.
11. Pasirinkite **Įrašyti**. Įrašius keitimus, reikia paleisti darbuotojų paskirstymo grafiką, kad keitimai būtų taikomi prekybos kanalams. 
12. Naršymo srityje eikite į **Moduliai > Žmogiškieji ištekliai > Darbai > Darbai**.
13. Dabar mes priskirsime EKA teisių grupę užduočiai. Sąraše raskite ir pasirinkite norimą įrašą.
14. Pasirinkite **Redaguoti**.
15. Išplėskite skyrių **Darbų klasifikacija**.
16. Lauke EKA teisių grupė įveskite arba pasirinkite reikšmę. Visi darbuotojai su šios užduoties pareigomis naudos šios EKA teisių grupės parametrus, nebent darbuotojų EKA teisių nepaisoma pareigų lygyje.  
17. Pasirinkite **Įrašyti**. Įrašius keitimus, reikia paleisti darbuotojų paskirstymo grafiką, kad keitimai būtų taikomi kanalams.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]