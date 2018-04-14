---
title: "Aptarnavimo objekto ryšiai"
description: "Galite sukurti aptarnavimo objekto ryšius tarp aptarnavimo objekto ir aptarnavimo sutarties arba aptarnavimo užsakymo."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: 0e54a0dc9b643077d45fe76e073772e81f99ea44
ms.contentlocale: lt-lt
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-relations"></a>Aptarnavimo objekto ryšiai 

[!INCLUDE [banner](../includes/banner.md)]

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
5. Formoje Aptarnavimo objektai spustelėkite Kūrimo įrankis – atidarysite kūrimo įrankio formą, kuruoje galėsite keisti šabloninę KS.

## <a name="automatically-created-service-orders"></a>Automatiškai kuriami aptarnavimo užsakymai

Jei automatiškai kuriate aptarnavimo sutarties aptarnavimo užsakymus, sutartyje esantys aptarnavimo objekto ryšiai taip pat sukuriami aptarnavimo užsakymuose.


