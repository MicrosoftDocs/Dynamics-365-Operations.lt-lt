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
ms.openlocfilehash: 4885c11f0cb508edb8ebf3aef14748e819113264
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067407"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Platinti klausimynus naudojant planavimą


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Klausimyno planavimo funkcija suteikia galimybę planuoti ir platinti klausimynus keliems respondentams. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.

## <a name="create-a-questionnaire-schedule"></a>Klausimyno grafiko kūrimas

1. Eiti į **Klausimynas** > **Paskirstyti** > **Anketų tvarkaraščiai**.

2. Spustelėkite **Naujas**.

3. Viduje konors **Planavimas** lauke įveskite reikšmę.

4. Lauke **Aprašo laukas** surinkite reikšmę.
    * Nustatykite tvarkaraštį į **Anoniminis** jei atsakymai turėtų būti įrašyti be su atsakymu susijusių pavadinimų.  
    * Parinktį Leisti anoniminius rezultatus pirmiausia reikia nustatyti personalo parametruose.  

5. Viduje konors **Tipas** lauke, pasirinkite planavimo tipą.  Šiame pavyzdyje mes naudosime **Pasitenkinimas** tipo.

6. Sąraše raskite ir pasirinkite norimą įrašą.

7. Sąraše spustelėkite saitą pasirinktoje eilutėje.

8. Lauke **Data** įveskite datą.

9. Išplėskite **El. paštas darbuotojo savitarnai** skyrius.

10. Lauke **Tema** įveskite reikšmę.

    * Pavyzdys: galimas klausimynas  

11. Viduje konors **Tekstas** laukelyje įveskite savo el. laiško turinį. Atkreipkite dėmesį, kad kintamasis gali būti naudojamas sistemos reikšmėms pakeisti.

    * Pavyzdys: Gerb. %P%, prisijunkite prie darbuotojų savitarnos, kad užpildytumėte klausimyną apie darbuotojų sveikatą.  Contoso  

12. Spustelėkite **Įrašyti**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Naudokite sąrankos informaciją klausimynui (-ams) parinkti ir teikti užklausas respondentams pasirinkti.

1. Spustelėkite **Išsami sąrankos informacija**.

2. Sąraše pasirinkite užklausą klausimyno respondentams sistemoje ieškoti.

    * Pavyzdys: darbuotojai  

3. Spustelėkite **Peržiūrėkite arba keiskite užklausą** norėdami pasirinkti konkrečius žmones arba koreguoti užklausą, kad rastumėte konkrečius kriterijus atitinkančius žmones.

    * Atkreipkite dėmesį, kad visi respondentai turi būti sistemos vartotojai.  

4. Sąraše pažymėkite eilutę Asmuo.

5. Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.

    * Pasirinkite Julia Funderburk  

6. Sąraše pasirinkite Julia Funderburk

7. Spustelėkite **Gerai**.

8. Spustelėkite **Klausimynai** skirtukas.

9. Medyje išplėskite klausimyno tipo mazgą **Pasitenkinimo tyrimas**.

10. Medyje pažymėkite Darbuotojų sveikatos įvertinimas.

11. Spustelėkite **Gerai**.

12. Spustelėkite **Suplanuota atsakymų sesija**.

    * Prisimink tai **Suplanuotos atsakymų sesijos** buvo sukurti kiekvienam pasirinktam / užklaustam vartotojui.  

13. Uždarykite puslapį.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Pradėkite klausimyno grafiką, kad respondentai galėtų klausimyną užpildyti.

1. spustelėkite **Funkcijos**.

2. Spustelėkite **Pradėti**.

3. Spustelėkite **Gerai**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Siųskite respondentams el. laišką, informuojantį apie galimą klausimyną.

1. spustelėkite **Funkcijos**.

2. Spustelėkite **Siųsti laišką**.

3. Spustelėkite **Atšaukti**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Naudokite funkciją Suplanuotas atsakymų seansas, norėdami stebėti, kas turi užpildyti klausimyną.

1. Spustelėkite **Suplanuota atsakymų sesija**.

    * Panaikinkite visus likusius suplanuotus atsakymų seansus, kai esate pasirengę baigti suplanuotą seansą.  

2. Spustelėkite **Naikinti**.

3. Spustelėkite **Taip**.

4. Uždarykite puslapį.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Baikite grafiką, kai visi respondentai užpildė klausimyną ir (arba) panaikinti visi likę suplanuoti atsakymų seansai.

1. spustelėkite **Funkcijos**.
2. Spustelėkite **Pabaiga**.
3. Spustelėkite **Gerai**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
