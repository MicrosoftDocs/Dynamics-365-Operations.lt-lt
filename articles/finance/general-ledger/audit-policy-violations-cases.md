---
title: Audito strategijos pažeidimai ir atvejai
description: Šiame straipsnyje paaiškinta, kaip sugeneruoti audito atvejus iš audito strategijos taisyklių pažeidimų. Jame taip pat pateikta informacija apie įvairius būdus, kokiais audito strategijoms naudojamas dokumentų pasirinkimo datų diapazonas.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ddd403bfe82b1a7d3c0c5999f89bde19f1bba5e8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022110"
---
# <a name="audit-policy-violations-and-cases"></a>Audito strategijos pažeidimai ir atvejai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip sugeneruoti audito atvejus iš audito strategijos taisyklių pažeidimų. Jame taip pat pateikta informacija apie įvairius būdus, kokiais audito strategijoms naudojamas dokumentų pasirinkimo datų diapazonas.

<a name="how-audit-cases-are-generated"></a>Kaip generuojami audito atvejai
-----------------------------

Audito strategijos naudojamos nustatant, kurios išlaidų ataskaitos, pirkimo užsakymai ir tiekėjo SF neatitinka verslo taisyklių, kurios nustatomos ir konfigūruojamos kaip audito strategijos taisyklės. 

Audito strategijos vykdomos paketiniu režimu. Vykdant audito strategiją, visos strategijos taisyklės, kurios yra tos strategijos dalis, yra vykdomos tuo pačiu metu.

Kiekviena strategijos taisyklė įvertina dokumentų rinkinį. Strategijos taisyklė pasirenka dokumentus, kurie patenka į dokumentų pasirinkimo datų diapazoną ir kurie atitinka nurodytus kriterijus. Pavyzdžiui, viena strategijos taisyklė gali pasirinkti išlaidų ataskaitas, kuriose yra valgiai, kainuojantys daugiau nei 50,00. Kita strategijos taisyklė gali pasirinkti tiekėjo SF, kurios mokamos konkrečiam tiekėjui. Sugeneruojami kiekvieno rinkinyje pasirinkto dokumento pažeidimai. Toks pažeidimas yra įrašas, kad konkretus dokumentas, pvz., SF 12345, neatitinka strategijos taisyklės. 

Keli audito pažeidimų įrašai sugrupuojami ir susiejami su audito atvejais. Pagal numatytuosius nustatymus kiekvienos audito strategijos atvejus grupuoja audito strategijos taisyklė. Jei norite, galite pasirinkti kitus grupavimo kriterijus naudodami puslapį **Atvejų grupavimo kriterijai**. Pavyzdžiui, galite grupuoti išlaidų antraštes pagal projekto ID, o tiekėjo SF pagal tiekėjo sąskaitą. Tokiu atveju, visi išlaidų antraščių pažeidimai, kurie turi tą patį projekto ID, bus sugrupuoti pagal tą patį atvejį, o visos tiekėjų SF, kurios turi tą pačią tiekėjo sąskaitą, taip pat bus sugrupuotos pagal tą patį atvejį. 

> [!NOTE]
> Audito strategijos taisyklių, kurios paremtos užklausos tipu **Dublikatas**, pažeidimai nėra grupuojami pagal strategijos taisyklę arba pagal kriterijus, nurodytus puslapyje **Atvejų grupavimo kriterijai**. Vietoj to, jie bus grupuojami pagal kriterijus, kurie yra integruoti į audito strategijos taisyklę. Pavyzdžiui, jei strategijos taisyklė įvertina išlaidų ataskaitas dėl besidubliuojančių tos pačios sumos išlaidų, prekybininko ID ir datos, visos išlaidos, kurios šiuose laukose turės vienodas reikšmes, bus vienas atvejis. Išlaidos, kurios turi skirtingas reikšmes, bus atskiri atvejai.

Sugeneravus audito atvejus, jie tvarkomi įprastais atvejų valdymo procesais.

## <a name="document-selection-date-ranges"></a>Dokumentų pasirinkimo datų diapazonai
Vykdant audito strategiją, kiekviena strategijos taisyklė pasirenka nurodyto tipo dokumentus, kurių data patenka į dokumento pasirinkimo datų diapazoną. Dokumento pasirinkimo datų diapazonas nurodytas puslapyje **Papildomos parinktys**. Daug dokumentų turi daugiau nei vieną su jais siejamą datą. Datos laukas, kurį naudoja audito strategijos taisyklė, nurodytas puslapyje **Strategijos taisyklės tipas**.

Štai keli būdai, kaip audito strategija naudoja dokumentų pasirinkimo datų diapazoną:

-   Strategija naudoja kiekvienos strategijos taisyklės versiją, kuri galioja paskutinę dokumentų pasirinkimo datų diapazono dieną. Galite peržiūrėti kiekvienos strategijos taisyklės galiojimo datas sąrašo puslapyje **Audito strategijos**.
-   Strategija naudoja organizacijos mazgus, kurie susiejami su strategija paskutinę dokumentų pasirinkimo datų diapazono dieną. Sąrašo puslapyje **Audito strategijos** rodomi tik tie organizacijos mazgai, kurie šiuo metu susieti su strategija.
-   Strategijos taisyklių, kurios paremtos užklausos tipu **Sąrašo paieška**, atveju strategija vertina dokumentuose esančius stebimus objektus, kurie tokiais būna paskutinę dokumentų pasirinkimo datų diapazono dieną.


Daugiau informacijos žr. dalyje [Audito strategijos taisyklės](audit-policy-rules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]