---
title: Biudžeto sukūrimas iš operacijų sąskaitų ir bendrųjų sąskaitų sumų
description: Šiame straipsnyje pateikta biudžetų kūrimo pagal bendrąsias sąskaitas proceso apžvalga. Jame taip pat paaiškinta, kaip įjungti bendrųjų sąskaitų biudžeto kontrolę, jei biudžeto kontrolė reikalinga.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09c9fc38360dcf82ceb317edc7195d826f56d86f
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594941"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Biudžeto sukūrimas iš operacijų sąskaitų ir bendrųjų sąskaitų sumų

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta biudžetų kūrimo pagal bendrąsias sąskaitas proceso apžvalga. Jame taip pat paaiškinta, kaip įjungti bendrųjų sąskaitų biudžeto kontrolę, jei biudžeto kontrolė reikalinga.

Biudžeto plano ir biudžeto registro įrašų dokumentai leidžia sudaryti biudžetus pagrindinėse sąskaitose, kurių pagrindinės sąskaitos tipas yra **Bendra suma**. Faktines sumas galima registruoti tik pagrindinėse operacinėse sąskaitose. 

Periodiniam procesui **Generuoti biudžeto planą iš didžiosios knygos** skirtuke **Šaltinis** galite kaip kriterijų nurodyti pagrindinės sąskaitos tipą **Iš viso**. Tokiu atveju kiekviena bendros sumos pagrindinė sąskaita bus įtrauktas į tikslinį biudžeto planą ir suma bus lygi bendrai pasirinktų pagrindinių sąskaitų diapazono sumai. 

Galite suaktyvinti **Bendra suma** tipo pagrindinių sąskaitų biudžeto kontrolę. Ši funkcija palaikoma naudojant biudžeto grupes. Kiekvienai bendros sumos pagrindinei sąskaitai biudžetas, kurį turi kontroliuoti biudžeto grupė, turi būti kuriamas puslapyje **Biudžeto kontrolės konfigūracija**. Jūsų nurodomi kriterijai turi apimti bendros sumos pagrindinę sąskaitą ir sąskaitų diapazoną. Norėdami paspartinti biudžeto grupių kūrimo procesą, galite pasinaudoti biudžeto kontrolės grupių duomenų objektu. 

Kai biudžetas naudojamas teikiant ataskaitas, pvz., finansines ataskaitas, bendrosios sąskaitos biudžeto sumą sudaro tokios sumos:

-   Biudžetai, kurie sukurti iš kiekvienos operacijos DK sąskaitos, patenkantys į bendrosios sąskaitos intervalą.
-   Biudžeto suma, kuri įvedama tiesiai į bendrąją sąskaitą.

Todėl galite kurti atskirus svarbiausių operacijų sąskaitų, patenkančių į bendrosios sąskaitos intervalą, biudžetus ir pridėti turimą biudžeto sumą prie bendrosios sąskaitos.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
