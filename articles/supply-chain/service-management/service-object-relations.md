---
title: Aptarnavimo objekto ryšiai
description: Galite sukurti aptarnavimo objekto ryšius tarp aptarnavimo objekto ir aptarnavimo sutarties arba aptarnavimo užsakymo.
author: sorenva
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 831db29589826904666049edbc8be0c38e1d02a5
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676641"
---
# <a name="service-object-relations"></a>Aptarnavimo objekto ryšiai 

[!include [banner](../includes/banner.md)]

Galite sukurti aptarnavimo objekto ryšius tarp aptarnavimo objekto ir aptarnavimo sutarties arba aptarnavimo užsakymo. Kurdami ryšį, aptarnavimo objektą pridėkite prie aptarnavimo sutarties arba aptarnavimo užsakymo.

Sukūrę ryšį, aptarnavimo objektą galite pridėti prie bet kurių aptarnavimo sutarties arba aptarnavimo užsakymo eilučių.

## <a name="template-boms"></a>KS šablonai

Taip pat galite nurodyti objekto ryšio KS šabloną. KS šablonas yra objekto, kuriam atliekate aptarnavimą, komplektacijos specifikacija. Aptarnavimo vizito metu pakeitę aptarnavimo objekto komponento dalį, šį pakeitimą galite užregistruoti aptarnavimo KS, naudodami formą Aptarnavimo objektai.

## <a name="example"></a>Pavyzdys

Sukuriate dviejų liftų aptarnavimo kliento pageidaujamoje teritorijoje sutartį.
Aptarnavimo sutarties identifikatorius yra ID SAL-001.

Liftai formoje Aptarnavimo objektai nustatomi kaip objektai, EL-S/1000 ir EL-L/1000.

Prie aptarnavimo sutarties pridedate aptarnavimo objektus, EL-S/1000 ir EL-L/1000.

Keisdami komponentų dalis, norite registruoti aptarnavimo objekto KS pakeitimus, todėl prie aptarnavimo objekto ryšio pridedate aptarnavimo KS, kaip apibrėžta šioje lentelėje.

| Aptarnavimo objektas | Ryšys – Aptarnavimo sutartis | Aptarnavimo KS   |
|----------------|------------------------------|---------------|
| EL-S/1000      | ID SAL-001                   | KS-EL-S/1000 |
| EL-L/1000      | ID SAL-001                   | KS-EL-L/1000 |

Kadangi egzistuoja sutarties aptarnavimo objekto ryšiai, dabar galite sukurti aptarnavimo sutarties eilutes su šiais objektais, kaip parodyta šioje lentelėje.

| Operacijos tipas | Kategorija           | Aptarnavimo objektas |
|------------------|--------------------|----------------|
| Valandos             | Patikrinimas         | EL-S/1000      |
| Valandos             | Pavarų dėžės valymas  | EL-S/1000      |
| Prekė             | Valymo medžiagos | EL-S/1000      |
| Valandos             | Patikrinimas         | EL-L/1000      |
| Valandos             | Pavarų dėžės valymas   | EL-L/1000      |
| Prekė             | Valymo medžiagos | EL-L/1000      |

Vykstant aptarnavimo vizitui, turite pakeisti lifto EL-S/1000 pavarų dėžę. Norėdami pakeisti objekto komponento dalį, galite pereiti į KS konstruktorių, naudodami nustatytą dabartinio aptarnavimo sutarties aptarnavimo objekto ryšį.

Prieiga prie KS konstruktoriaus, naudojant aptarnavimo objekto ryšį

1. Aptarnavimo sutartys
2. Dukart spustelėkite aptarnavimo sutartį arba spustelėkite Aptarnavimo sutartis, kad sukurtumėte naują aptarnavimo sutartį.
3. Spustelėkite skirtuką Nustatymas.
4. Norėdami prie aptarnavimo sutarties pridėti KS šabloną, spustelėkite Aptarnavimo objektai.
5. Formoje Aptarnavimo objektai spustelėkite Kūrimo įrankis – atidarysite kūrimo įrankio formą, kurioje galėsite keisti šabloninę KS.

## <a name="automatically-created-service-orders"></a>Automatiškai kuriami aptarnavimo užsakymai

Jei automatiškai kuriate aptarnavimo sutarties aptarnavimo užsakymus, sutartyje esantys aptarnavimo objekto ryšiai taip pat sukuriami aptarnavimo užsakymuose.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]