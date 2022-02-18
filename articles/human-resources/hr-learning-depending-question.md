---
title: Sukurti klausimą pagal atsakymą į ankstesnį klausimą
description: Sąlyginiai klausimai leidžia nurodyti, kokie kiti klausimai bus pateikiami respondentui, atsižvelgiant į atsakymą į ankstesnį klausimą.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f28f75a902121f23c92a919b539517dbdb191447
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066730"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Sukurti klausimą pagal atsakymą į ankstesnį klausimą


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Sąlyginiai klausimai leidžia nurodyti, kokie kiti klausimai bus pateikiami respondentui, atsižvelgiant į atsakymą į ankstesnį klausimą. Pvz., jei klausiate „Kas labiau patinka, kava ar arbata?“, logiškas kitas klausimas gali būti nustatytas atsižvelgiant į tai, ar respondentas savo atsakyme pasirenka kavą ar arbatą. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="find-the-existing-questionnaire"></a>Rasti esamą klausimyną
1. Eiti į **Klausimynas** > **Dizainas** > **Klausimynai**.
2. Sąraše pasirinkite „WorkFH“ klaisimyną.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Įtraukti visus klausimus ir papildomus klausimus į klausimyną
1. Spustelėkite **Klausimai**.
2. Spustelėkite **Naujas**.
3. Viduje konors **Klausimas** laukelyje pasirinkite klausimo numerį 00016.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite **Įrašyti**.
7. Uždarykite puslapį.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Nustatyti sąlyginę klausimyno seką ir padaryti klausimą priklausomą nuo atitinkamo atsakymo
1. Spustelėkite **Redaguoti**.
2. Išplėskite skyrių **Sąranka**.
3. Viduje konors **Klausimų tvarka** lauke pasirinkite „Sąlyginis“.
4. Spustelėkite **Sąlyginis** klausimas.
5. Medyje pasirinkite „Klausimai \ Paaiškinkite, kodėl pasirinkote tokį atsakymą į ankstesnį klausimą“.
6. Viduje konors **Pirminis klausimas** lauke, pasirinkite klausimą 00009.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Viduje konors **Atsakymas** lauke įveskite atsakymo parinkties, nuo kurios norite nustatyti klausimą, atsakymų sekos ID. Pvz., įveskite 1 pasirinkdami pirmąjį atsakymą.
9. Spustelėkite **Įrašyti**.
10. Medyje pasirinkite „Klausimai \ Ar man sąžiningai atlyginama už mano atliekamą darbą?“.
    * Atkreipkite dėmesį, kad atsinaujino klausimų medis parodydamas priklausomybę.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
