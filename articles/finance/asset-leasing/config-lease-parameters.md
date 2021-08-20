---
title: Nuomos parametrų konfigūravimas (peržiūros versija)
description: Šioje temoje aprašomi modulio Turto nuoma konfigūracijos parametrai, pvz., saugos informacijos ir apskaitos parametrai.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e5f0aeddfa9d3f27500b033d4b4fb0fb1731105a28be4a6934b2328d62df6ec1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779043"
---
# <a name="configure-lease-parameters"></a>Nuomos parametrų konfigūravimas

[!include [banner](../includes/banner.md)]

Keletas konfigūracijos parametrų lemia modulio Turto nuoma veikimą. Šie parametrai apima žurnalų pavadinimus, bendruosius parametrus ir registravimo šablonų parametrus.

1. Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.
2. Skirtuke **Nuomos** pasirinkite „FastTab“ **Bendra**.

    Parametras **Leisti neautomatinį klasifikacijos keitimą** nurodo, ar nuomos klasifikaciją galima pakeisti prieš patvirtinant mokėjimo grafiką.

    Parametras **Kelių objektų paketas** nurodo, ar galite registruoti į kitus juridinius subjektus iš dabartinio juridinio subjekto. Jei šis parametras įjungtas, galite kurti juridinių subjektų, prie kurių turite prieigą, žurnalo įrašus.

3. Nustatykite parinktį **Leisti panaikinti patvirtintas nuomas** kaip **Taip**, kad būtų galima panaikinti patvirtintų mokėjimo grafikų nuomas. Nuomų negalima panaikinti, jei su jomis susietos užregistruotos arba neužregistruotos operacijos, nepaisant šios pasirinkties parametro. Po to, kai nuomos įrašas panaikinamas, jo atkurti negalima. Jei nusiunčiate panaikintos nuomos įrašų neautomatiniu būdu arba per duomenų objektus, nusiųsta informacija laikoma nauja, o ne esamos nuomos atnaujinimu.

    Jei šią parinktį nustatote kaip **Taip**, o knygos perėjimo tipas yra **Kaupiamoji atgalinės datos A arba B parinktis**, sistema nustato lauką **Apskaičiuota skolinimosi palūkanų norma** kaip puslapio **Knygų sąranka** lauko **Apskaičiuota skolinimosi palūkanų norma pereinant** reikšmę. Jei ši parinktis nustatyta kaip **Ne**, pagrindinės nuomos norma nustatoma kaip puslapio **Knygų informacija** lauko **Apskaičiuota skolinimosi palūkanų norma** reikšmė, neatsižvelgiant į knygos perėjimo tipą.

4. Nustatykite parinktį **Leisti nusidėvėjimo atšaukimus uždarytos knygos versijoje** kaip **Taip**, kad būtų galima atšaukti nusidėvėjimo išlaidų operacijas. Išlaidų operacijos gali būti atšauktos net uždarius knygos versiją.

    > [!NOTE]
    > Rekomenduojame šią pasirinktį palikti nustatytą kaip **Ne**. Šios parinkties nustatymas naudojamas kaip patikra ir valdiklis, siekiant apsaugoti uždarytos knygos versiją nuo netyčinio nusidėvėjimo. Palikdami parametrą nustatytą kaip **Ne**, padėsite išsaugoti tikslią balansinę vertę ir būsimus nusidėvėjimo skaičiavimus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
