---
title: Platinti klausimynus naudojant planavimą
description: Klausimyno planavimo funkcija suteikia galimybę planuoti ir platinti klausimynus keliems respondentams.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2336cafe7e2c914c2592c91c888b1e0ae1bc608
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728681"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Platinti klausimynus naudojant planavimą

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Klausimyno planavimo funkcija suteikia galimybę planuoti ir platinti klausimynus keliems respondentams. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.

## <a name="create-a-questionnaire-schedule"></a>Klausimyno grafiko kūrimas

1. Eikite į **·** > **klausimyno** > **platinimo grafikus**.

2. Spustelėkite **Naujas**.

3. Lauke **Planavimas** įveskite vertę.

4. Lauke **Aprašo laukas** surinkite reikšmę.
    * Nustatyti grafiką kaip **·** Anoniminis, jei atsakymai turėtų būti įrašomi be pavadinimų, susietų su atsakymu.  
    * Parinktį Leisti anoniminius rezultatus pirmiausia reikia nustatyti personalo parametruose.  

5. Lauke **·** Tipas pasirinkite planavimo tipą.  Šiame pavyzdyje mes naudosime patenkinimo **·** tipą.

6. Sąraše raskite ir pasirinkite norimą įrašą.

7. Sąraše spustelėkite saitą pasirinktoje eilutėje.

8. Lauke **Data** įveskite datą.

9. Išplėskite **darbuotojų savitarnos skyriaus** el. laišką.

10. Lauke **Tema** įveskite reikšmę.

    * Pavyzdys: galimas klausimynas  

11. Lauke **Tekstas** įveskite el. laiško tekstą. Atkreipkite dėmesį, kad kintamasis gali būti naudojamas sistemos reikšmėms pakeisti.

    * Pavyzdys: Gerb. %P%, prisijunkite prie darbuotojų savitarnos, kad užpildytumėte klausimyną apie darbuotojų sveikatą.  Contoso  

12. Spustelėkite **Įrašyti**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Naudokite sąrankos informaciją klausimynui (-ams) parinkti ir teikti užklausas respondentams pasirinkti.

1. Spustelėkite **nustatymo** informaciją.

2. Sąraše pasirinkite užklausą klausimyno respondentams sistemoje ieškoti.

    * Pavyzdys: darbuotojai  

3. Spustelėkite **Peržiūrėti arba modifikuoti užklausą, kad** pasirinktumėte konkrečius žmones arba koreguotumėte užklausą, kad rastumėte konkrečius kriterijus atitinkančius žmones.

    * Atkreipkite dėmesį, kad visi respondentai turi būti sistemos vartotojai.  

4. Sąraše pažymėkite asmens eilutę.

5. Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.

    * Pasirinkite Julia Funderburk  

6. Sąraše pasirinkite Julia Funderburk

7. Spustelėkite **Gerai**.

8. Spustelėkite **skirtuką** Klausimynai.

9. Medyje išplėskite klausimyno tipo Patikrinimas dėl patenkinimo **·** mazgą.

10. Medyje pažymėkite Darbuotojų sveikatos įvertinimas.

11. Spustelėkite **Gerai**.

12. Spustelėkite **Suplanuotas atsakymų seansas.**

    * Atkreipkite **dėmesį, kad** suplanuoti atsakymų seansai buvo sukurti kiekvienam pasirinktam / užklausuotam vartotojui.  

13. Uždarykite puslapį.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Pradėkite klausimyno grafiką, kad respondentai galėtų klausimyną užpildyti.

1. spustelėkite **Funkcijos**.

2. Spustelėkite **Pradėti**.

3. Spustelėkite **Gerai**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Siųskite respondentams el. laišką, informuojantį apie galimą klausimyną.

1. spustelėkite **Funkcijos**.

2. Spustelėkite Siųsti **el.** laišką.

3. Spustelėkite **Atšaukti**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Naudokite funkciją Suplanuotas atsakymų seansas, norėdami stebėti, kas turi užpildyti klausimyną.

1. Spustelėkite **Suplanuotas atsakymų seansas.**

    * Panaikinkite visus likusius suplanuotus atsakymų seansus, kai esate pasirengę baigti suplanuotą seansą.  

2. Spustelėkite **Naikinti**.

3. Spustelėkite **Taip**.

4. Uždarykite puslapį.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Baikite grafiką, kai visi respondentai užpildė klausimyną ir (arba) panaikinti visi likę suplanuoti atsakymų seansai.

1. spustelėkite **Funkcijos**.
2. Spustelėkite **·** Baigti.
3. Spustelėkite **Gerai**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
