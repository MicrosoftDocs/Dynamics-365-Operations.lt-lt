---
title: Nuomos parametrų konfigūravimas (peržiūros versija)
description: Šiame straipsnyje aprašomi turto naudojimo konfigūracijos parametrai, pvz., saugos informacija ir apskaitos parametrai.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e878fa7634cfdcc6c0db19a91e771757c545505b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895086"
---
# <a name="configure-lease-parameters"></a>Nuomos parametrų konfigūravimas

[!include [banner](../includes/banner.md)]

Keletas konfigūracijos parametrų lemia modulio Turto nuoma veikimą. Šie parametrai apima žurnalų pavadinimus, bendruosius parametrus ir registravimo šablonų parametrus.

1. Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.
2. Skirtuke **Nuomos** pasirinkite „FastTab“ **Bendra**.

    Parametras **Leisti neautomatinį klasifikacijos keitimą** nurodo, ar nuomos klasifikaciją galima pakeisti prieš patvirtinant mokėjimo grafiką.

    Kryžminio **subjekto paketo** parametras nustato, ar galite registruoti kitiems dabartinio juridinio subjekto juridiniams subjektams. Jei šis parametras įjungtas, galite kurti juridinių subjektų, prie kurių turite prieigą, žurnalo įrašus.

3. Nustatykite **parinktį Leisti naikinti patvirtintas nuomą** kaip **Taip**, kad būtų galima naikinti nuomą, kuri patvirtino mokėjimo grafikus. Nuomų negalima panaikinti, jei su jomis susietos užregistruotos arba neužregistruotos operacijos, nepaisant šios pasirinkties parametro. Po to, kai nuomos įrašas panaikinamas, jo atkurti negalima. Jei nusiunčiate panaikintos nuomos įrašų neautomatiniu būdu arba per duomenų objektus, nusiųsta informacija laikoma nauja, o ne esamos nuomos atnaujinimu.

    Jei šią parinktį nustatote kaip **Taip**, o knygos perėjimo tipas yra **Kaupiamoji atgalinės datos A arba B parinktis**, sistema nustato lauką **Apskaičiuota skolinimosi palūkanų norma** kaip puslapio **Knygų sąranka** lauko **Apskaičiuota skolinimosi palūkanų norma pereinant** reikšmę. Jei ši parinktis nustatyta kaip **Ne**, pagrindinės nuomos norma nustatoma kaip puslapio **Knygų informacija** lauko **Apskaičiuota skolinimosi palūkanų norma** reikšmė, neatsižvelgiant į knygos perėjimo tipą.

4. Norėdami atšaukti **nusidėvėjimo išlaidų operacijas, uždarytos** knygos **pasirinktį** Leisti atšaukti nusidėvėjimą nustatykite kaip Taip. Išlaidų operacijos gali būti atšauktos net uždarius knygos versiją.

    > [!NOTE]
    > Rekomenduojame šią pasirinktį palikti nustatytą kaip **Ne**. Šios parinkties nustatymas naudojamas kaip patikra ir valdiklis, siekiant apsaugoti uždarytos knygos versiją nuo netyčinio nusidėvėjimo. Palikdami parametrą nustatytą kaip **Ne**, padėsite išsaugoti tikslią balansinę vertę ir būsimus nusidėvėjimo skaičiavimus.

5. Nustatykite **parinktį Leisti mokėjimo sumos paskirstymą** **kaip** Taip, **kad** būtų galima paskirstyti mokėjimo sumas puslapio Nuomos grafiko **eilutėse** "FastTab". Mokėjimo paskirstymo tipai apibrėžiami puslapio **Mokėjimo** sumos tipai **dalyje** Nustatymas. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
