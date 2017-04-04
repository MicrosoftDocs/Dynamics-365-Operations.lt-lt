---
title: "Audito strategijos pažeidimai ir atvejai"
description: "Šiame straipsnyje paaiškinta, kaip sugeneruoti audito atvejus iš audito strategijos taisyklių pažeidimų. Jame taip pat pateikta informacija apie įvairius būdus, kokiais audito strategijoms naudojamas dokumentų pasirinkimo datų diapazonas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: ecd32549b6067ed4c1211996e846e210f77f5013
ms.openlocfilehash: 77f72c9414f1fad720055e58e3f704b9c713072f
ms.lasthandoff: 03/31/2017


---

# <a name="audit-policy-violations-and-cases"></a>Audito strategijos pažeidimai ir atvejai

Šiame straipsnyje paaiškinta, kaip sugeneruoti audito atvejus iš audito strategijos taisyklių pažeidimų. Jame taip pat pateikta informacija apie įvairius būdus, kokiais audito strategijoms naudojamas dokumentų pasirinkimo datų diapazonas.

<a name="how-audit-cases-are-generated"></a>Kaip generuojami audito atvejai
-----------------------------

Audito strategijos naudojamos nustatant, kurios išlaidų ataskaitos, pirkimo užsakymai ir tiekėjo SF neatitinka verslo taisyklių, kurios nustatomos ir konfigūruojamos kaip audito strategijos taisyklės. 

Audito strategijos vykdomos paketiniu režimu. Vykdant audito strategiją, visos strategijos taisyklės, kurios yra tos strategijos dalis, yra vykdomos tuo pačiu metu.

Kiekviena strategijos taisyklė įvertina dokumentų rinkinį. Strategijos taisyklė pasirenka dokumentus, kurie patenka į dokumentų pasirinkimo datų diapazoną ir kurie atitinka nurodytus kriterijus. Pavyzdžiui, viena strategijos taisyklė gali pasirinkti išlaidų ataskaitas, kuriose yra valgiai, kainuojantys daugiau nei 50,00. Kita strategijos taisyklė gali pasirinkti tiekėjo SF, kurios mokamos konkrečiam tiekėjui. Sugeneruojami kiekvieno rinkinyje pasirinkto dokumento pažeidimai. Toks pažeidimas yra įrašas, kad konkretus dokumentas, pvz., SF 12345, neatitinka strategijos taisyklės. 

Keli audito pažeidimų įrašai sugrupuojami ir susiejami su audito atvejais. Pagal numatytuosius nustatymus kiekvienos audito strategijos atvejus grupuoja audito strategijos taisyklė. Jei norite, galite pasirinkti kitus grupavimo kriterijus naudodami puslapį **Atvejų grupavimo kriterijai**. Pavyzdžiui, galite grupuoti išlaidų antraštes iš projekto ID ir tiekėjo SF iš tiekėjo sąskaitą. Šiuo atveju visos išlaidų antraštės pažeidimus, kurie turi tą patį projekto ID bus galima sugrupuoti toje pačioje byloje ir visus tiekėjo SF, kurios yra paties tiekėjo sąskaitą bus galima sugrupuoti toje pačioje byloje. 

> [!NOTE]
> Audito politikos taisykles, kurios remiasi į **dubliuoti** užklausos tipas, pažeidimų nėra sugrupuoti politikos taisyklės ar kriterijai, kurie nurodomi šie į **atveju grupavimo kriterijus** puslapis. Vietoj to, jie bus grupuojami pagal kriterijus, kurie yra integruoti į audito strategijos taisyklę. Pavyzdžiui, jei strategijos taisyklė įvertina išlaidų ataskaitas dėl besidubliuojančių tos pačios sumos išlaidų, prekybininko ID ir datos, visos išlaidos, kurios šiuose laukose turės vienodas reikšmes, bus vienas atvejis. Išlaidos, kurios turi skirtingas reikšmes, bus atskiri atvejai.

Sugeneravus audito atvejus, jie tvarkomi įprastais atvejų valdymo procesais.

## <a name="document-selection-date-ranges"></a>Dokumentų pasirinkimo datų diapazonai
Vykdant audito strategiją, kiekviena strategijos taisyklė pasirenka nurodyto tipo dokumentus, kurių data patenka į dokumento pasirinkimo datų diapazoną. Dokumento pasirinkimo datų diapazonas nurodytas puslapyje **Papildomos parinktys**. Daug dokumentų turi daugiau nei vieną su jais siejamą datą. Datos laukas, kurį naudoja audito strategijos taisyklė, nurodytas puslapyje **Strategijos taisyklės tipas**.

Štai keli būdai, kaip audito strategija naudoja dokumentų pasirinkimo datų diapazoną:

-   Strategija naudoja kiekvienos strategijos taisyklės versiją, kuri galioja paskutinę dokumentų pasirinkimo datų diapazono dieną. Galite peržiūrėti kiekvienos strategijos taisyklės galiojimo datas sąrašo puslapyje **Audito strategijos**.
-   Strategija naudoja organizacijos mazgus, kurie susiejami su strategija paskutinę dokumentų pasirinkimo datų diapazono dieną. Sąrašo puslapyje **Audito strategijos** rodomi tik tie organizacijos mazgai, kurie šiuo metu susieti su strategija.
-   Strategijos taisyklių, kurios paremtos užklausos tipu **Sąrašo paieška**, atveju strategija vertina dokumentuose esančius stebimus objektus, kurie tokiais būna paskutinę dokumentų pasirinkimo datų diapazono dieną.


Daugiau informacijos rasite [audito tvarkos taisykles](audit-policy-rules.md)


