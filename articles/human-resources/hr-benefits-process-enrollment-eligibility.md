---
title: Registracijos tinkamumo apdorojimas
description: Šioje temoje paaiškinama, kaip vykdyti registracijos tinkamumo apdorojimą.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c83753c17721487ba6adbf822c994a71ae0a0e6
ms.sourcegitcommit: 4f9c889e5cf72f34dd9746a322f8c0d6b983037b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/25/2021
ms.locfileid: "7417489"
---
# <a name="process-enrollment-eligibility"></a>Registracijos tinkamumo apdorojimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje paaiškinama, kaip vykdyti registracijos tinkamumo apdorojimą.

1. Darbo srities **Išmokų valdymas** dalyje **Apdorojimas** pasirinkite **Registracijos tinkamumo apdorojimas**.

2. Dialogo lange **Vykdyti registracijos išmokoms gauti tinkamumo apdorojimą** nurodykite šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Registracijos laikotarpis** | Ragistracijos tinkamumo apdorojimo registracijos laikotarpis. |
   | **Juridinis subjektas** | Registracijos tinkamumo apdorojimo juridinis subjektas. |
   | **Darbininkas** | Registracijos tinkamumo apdorojimo darbininkas. Jei paliksite šį lauką tuščią, visų darbuotojų registracijos tinkamumas bus apdorojamas. |
   | **Išmokų planas** | Registracijos tinkamumo apdorojimo išmokų planas.

3. Jei norite vykdyti procesą fone, pasirinkite **Vykdyti fone** ir atlikite šias užduotis:

   1. Įveskite proceso informaciją.

   2. Norėdami nustatyti pasikartojančią užduotį, pasirinkite **Pasikartojimas**, įveskite pasikartojimo informaciją ir pažymėkite **Gerai**.

   3. Norėdami nustatyti užduoties įspėjimą, pasirinkite **Įspėjimai**, pasirinkite gautinus įspėjimus, tada pažymėkite **Gerai**.

   4. Pasirinkite **Gerai**. Procesas bus vykdomas naudojant jūsų nustatytus parametrus.

4. Pasirinkite **Gerai**.

## <a name="view-process-results"></a>Proceso rezultatų peržiūra

Šioje temoje paaiškinama, kaip peržiūrėti tinkamumo proceso rezultatus.

1.  Darbo srities **Išmokų valdymas** dalyje **Apdorojimas** pasirinkite **Proceso rezultatai**.

2.  Puslapy **Proceso rezultatai** nurodyti toliau pateikti laukai:

   | Laukas | Aprašas |
   | --- | --- |
   | **Eigos ID** | Unikalus darbuotojo, juridinio subjekto ir proceso vykdymo derinio ID. |
   | **Proceso tipas** | Taip identifikuojamas procesas, kuris buvo vykdomas. Pvz.: registracija. |
   | **Laiko antspaudas** | Tinkamumo proceso vykdymo laikas. |
   | **Juridinis subjektas** | Registravimo proceso metu nurodytas juridinis subjektas. |
   | **Darbuotojas** | Darbuotojas, kuris buvo apdorotas. |
   | **Planas | Išmokų planas, dėl kurio buvo bandyta registracija. |
   | **Tinkamumo taisyklė** | Apdorota tinkamumo taisyklė. Jei prieš tinkamumo vykdymą įvyko klaida, šis laukas bus tuščias. Pvz.: jei darbuotojo kompensacija nebuvo nustatyta, tinkamumo procesas nebus vykdomas, o šis laukas liks tuščias. |
   | **Rezultato būsena** | Ji bus Tinkama arba Netinkama. Rezultato būsena bus Netinkama, jei darbuotojas neatitinka tinkamumo taisyklės kriterijų, jei trūksta būtinos darbuotojo informacijos, pvz., mokėjimo dažnumo arba pastoviosios atlyginimo dalies, arba jei trūksta informacijos apie išmokų planą ir tai neleidžia darbuotojams būti užregistruotiems. |
   | **Rezultato pranešimas** | Nurodo, kodėl darbuotojas netinkamas išmokų planui gauti arba kad buvo išlaikyta tinkamumo taisyklė. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
