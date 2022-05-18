---
title: Parengti juridinį asmenį konsolidavimo procesui
description: Konsolidavimo metu renkate transakcija iš kelių juridinių asmenų rinkinių sąskaitų į vieną juridinių asmenų sąskaitų rinkinį. Šioje temoje paaiškinama, kaip parengti juridinį asmenį konsolidavimui.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 0ef6736046748b92357c41d27eeedfc88c610d33
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722044"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Parengti juridinį asmenį konsolidavimo procesui

[!include [banner](../includes/banner.md)]

Konsolidavimo metu renkate transakcija iš kelių juridinių asmenų rinkinių sąskaitų į vieną juridinių asmenų sąskaitų rinkinį. Šioje temoje paaiškinama, kaip parengti juridinį asmenį konsolidavimui.

> [!NOTE]
> Rekomenduojame naudoti "Management Reporter for Microsoft Dynamics 365 Finance", kad būtų sujungti keleto juridinių subjektų finansiniai rezultatai konsoliduotu formatu. "Management Reporter" leidžia kurti konsoliduotas finansines ataskaitas tarp juridinių subjektų, naudoti Excel, norint importuoti konsolidavimo duomenis iš kitų šaltinių ir išversti sumas į bet kokį ataskaitų valiutų skaičių, nereikia vykdyti konsolidavimo proceso "Dynamics 365" finansuose.

Galite spausdinti ataskaitas, tokias kaip finansinės ataskaitos iš konsoliduoto juridinio asmens. Nepaisant to, negalite naudoti konsoliduoto juridinio asmens kasdienėms transakcijoms.

Galite konsoliduoti duomenis iš juridinių asmenų, kurie naudoja kitas duomenų bazes nei konsoliduotas juridinis asmuo. Toks konsolidavimo procesas yra vadinamas *importuoti konsolidavimą*. Kitu atveju, juridiniai asmenys gali naudot tą pačią duomenų bazę kaip konsoliduotas juridinis asmuo. Toks konsolidavimo procesas yra vadinamas *internetiniu konsolidavimu*.

Konsoliduotas juridinis asmuo renka dukterinių bendrovių rezultatus ir balansus. Norėdami parengti konsoliduotą juridinį asmenį konsolidavimui, vadovaukitės šiais žingsniais.

1. Eikite į **Bendra buhalterinė knyga \> Nustatymai \> Organizacija \> Jurdiniai asmenys**.
2. Rinkitės **Naujas** norėdami sukurti juridinį asmenį, kuris bus konsoliduotas juridinis asmuo.
3. Rinkitės **Naudoti finansinio konsolidavimo proceso** žymimą laukelį ir tuomet įveskite informaciją apie konsoliduotą juridinį asmenį. Įsitikinkite, kad įvedėte šią informaciją tiksliai kaip norite ją parodyti konsoliduoto juridinio asmens finansinėse ataskaitose.
4. Uždarykite puslapį.
5. Rinkitės konsoliduotą juridinį asmenį laukelyje dešiniame viršutiniame puslapio kampe ir tada rinkitės **Gerai**.
6. Eikite į **Bendra buhalterinė knyga \> Nustatymai \> Buhalterinė knyga**.
7. Rinkitės sąskaitų grafikus, mokesčių kalendorių, apskaitos valiutą, pasirenkamą ataskaitos valiutą ir numatytą keitimo kurso tipą konsoliduotam juridiniam asmeniui. 
8. Eikite į **Buhalterinė knyga \> Nustatymai \> Valiuta \> Keitimo kurso valiuta**.
9. Nustatykite valiutos keitimo kursus atitinkamiems dukterinių juridinių asmenų valiutų laikotarpiams.
10. Uždarykite puslapį.
11. Jei konsoliduotas juridinis asmuo turi dukterinių įmonių, naudojančių užsienio valiutas, atlikite šiuos veiksmus:

    1. Eikite į **Bendra buhalterinė knyga \> Nustatymai \> Publikavimas \> Sąskaitos automatinėms transakcijoms**.
    2. Laukelyje **Publikavimo tipas** rinkitės atitinkamą sąskaitą:

        - Jei juridinis asmuo turi užsienio dukterines įmones, kurios yra finansiškai ar savo veikla priklausomos nuo valdančio juridinio asmens, rinkitės atitinkamą sąskaitą **Pelno ir nuostolių sąskaitą konsolidavimo skirtumams** publikavimo tipą.
        - Jei konsoliduojate dukterinę įmonę, kuri yra finansiškai ir savo veikla nepriklausoma nuo valdančio juridinio asmens ar juridinio asmens, turinčio kelių dukterinių įmonių rezultatus, finansiškai ir savo veikla nepriklausančių nuo valdančio juridinio asmens ir jei naudojate vertimo metodus siekiant konsoliduoti duomenis, rinkitės atitinkamą sąskaitą **Balanso sąskaita konsolidavimo skirtumams** publikavimo tipą.

    3. Laukelyje **Pagrindinė sąskaitą**, rinkitės pagrindines sąskaitas, kurios turi būti naudojamos užsienio valiutos pakartotinio įvertinimo keitimams.
    4. Uždarykite puslapį.

    Jei sukuriate konsoliduotą juridinį asmenį periodo pradžioje, galite iš naujo įvertinti užsienio valiutos sumas kaip keitimo valiutų kursą konsolidavimo metu.

Konsoliduotas juridinis asmuo dabar yra nustatytas **Konsolidavimo** periodiniame darbe. Galite importuoti konsolidavimą ar atlikti konsolidavimą internete.

- Norėdami atlikti importavimo konsolidavimą, eikite į **Bendra buhalterinė knyga \> Periodinis \> Konsoliduoti \> Konsoliduoti \[importuoti iš\]**.
- Norėdami konsoliduoti internetu, eikite į **Bendra buhalterinė knyga \> Periodinis \> Konsoliduoti \> Konsoliduoti \[internetu\]**.

> [!NOTE]
> Prieš tai, kai galite sutvarkyti konsolidavimą, turite parengti dukterinį juridinį asmenį konsolidavimui. Dėl daugiau informacijos, žr. [Nustatykite dukterinį juridinį asmenį konsolidavimui](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
