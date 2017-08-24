--- 
title: "Sukurti klausimą pagal atsakymą į ankstesnį klausimą"
description: "Sąlyginiai klausimai leidžia nurodyti, kokie kiti klausimai bus pateikiami respondentui, atsižvelgiant į atsakymą į ankstesnį klausimą."
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6e532241d719aa013fcbc0c03f88fbda9cc06b99
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Sukurti klausimą pagal atsakymą į ankstesnį klausimą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Sąlyginiai klausimai leidžia nurodyti, kokie kiti klausimai bus pateikiami respondentui, atsižvelgiant į atsakymą į ankstesnį klausimą. Pvz., jei klausiate „Kas labiau patinka, kava ar arbata?“, logiškas kitas klausimas gali būti nustatytas atsižvelgiant į tai, ar respondentas savo atsakyme pasirenka kavą ar arbatą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="find-the-existing-questionnaire"></a>Rasti esamą klausimyną
1. Pasirinkite Klausimynas > Kūrimas > Klausimynai.
2. Sąraše pasirinkite „WorkFH“ klaisimyną.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Įtraukti visus klausimus ir papildomus klausimus į klausimyną
1. Spustelėkite „Klausimai“.
2. Spustelėkite Naujas.
3. Lauke „Klausimas“ pasirinkite klausimą numeris 00016.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Nustatyti sąlyginę klausimyno seką ir padaryti klausimą priklausomą nuo atitinkamo atsakymo
1. Spustelėkite Redaguoti.
2. Išplėskite skyrių Nustatymas.
3. Lauke „Klausimų tvarka“ pasirinkite „Sąlyginis“.
4. Spustelėkite „Sąlyginis klausimas“.
5. Medyje pasirinkite „Klausimai \ Paaiškinkite, kodėl pasirinkote tokį atsakymą į ankstesnį klausimą“.
6. Lauke „Pirminis klausimas“ pasirinkite klausimą 00009.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke „Atsakymas“ įveskite atsakymo pasirinkimo, nuo kurio norite padaryti klausimą priklausomą, atsakymo sekos ID. Pvz., įveskite 1 pasirinkdami pirmąjį atsakymą.
9. Spustelėkite Įrašyti.
10. Medyje pasirinkite „Klausimai \ Ar man sąžiningai atlyginama už mano atliekamą darbą?“.
    * Atkreipkite dėmesį, kad atsinaujino klausimų medis parodydamas priklausomybę.  

