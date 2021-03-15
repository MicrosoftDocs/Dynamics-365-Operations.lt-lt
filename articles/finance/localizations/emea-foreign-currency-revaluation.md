---
title: Užsienio valiutos kurso pasikeitimas banko sąskaitoms
description: Šioje temoje pateikiama informacija apie užsienio valiutos kurso pasikeitimą banko sąskaitoms.
author: panolte
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 11464
ms.search.region: Czech Republic, Estonia, Latvia, Lithuania, Poland
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db8dab0aef0349632d19ad407336a18641c358d1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002976"
---
# <a name="foreign-currency-revaluation-for-bank-accounts"></a>Užsienio valiutos kurso pasikeitimas banko sąskaitoms

[!include [banner](../includes/banner.md)]

## <a name="revalue-foreign-currency-amounts-for-bank-account-transactions"></a>Su banko sąskaita susijusių operacijų užsienio valiutos sumų perkainojimas

> [!IMPORTANT]
> Šis skyrius taikomas tik juridiniams subjektams, kurių pagrindinis adresas yra Lenkijoje.

Galite perkainoti su banko sąskaita susijusių operacijų užsienio valiutos sumas. Tada galite sukurti ataskaitą, kad peržiūrėtumėte banko operacijas, kuriose atlikta užsienio valiutos pasikeitimų koregavimų.

1. Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Periodinės užduotys** &gt; **Bankas – valiutos kurso koregavimas (FIFO/LIFO)**.
2. Lauke **Nustatytai datai** įveskite pasikeitimo pabaigos datą. Į skaičiavimą įtraukiamos tik tos operacijos, kurių data yra ankstesnė už nurodytą.
3. Pasirinkite **Įtrauktini įrašai** &gt; **Filtras** &gt; **Įtraukti** ir įtraukite banko sąskaitą. Jei nenurodote banko sąskaitos, sumos perkainojamos visose banko sąskaitose.
4. Pasirinkite **Gerai** ir uždarykite užklausos puslapį.
5. Puslapyje **Užsienio valiutos kurso pasikeitimas** pasirinkite žymės langelį **Perskaičiavimas** ir perkainokite visų atvirų laikotarpių užsienio valiutos sumas.

## <a name="create-a-report-to-view-bank-transactions-that-have-adjustments-for-foreign-currency-revaluations"></a>Sukurkite ataskaitą, kad peržiūrėtumėte banko operacijas, kuriose atlikta užsienio valiutos pasikeitimų koregavimų.

> [!IMPORTANT]
> Šis skyrius taikomas tik juridiniams subjektams, kurių pagrindinis adresas yra Lenkijoje.

1. Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Bankas – kurso koregavimo ataskaita**.
2. Pasirinkite **Įtrauktini įrašai** &gt; **Filtras** ir raskite vieną ar daugiau banko sąskaitų, kurių informaciją norite peržiūrėti.
3. Pasirinktinai: lauke **Banko sąskaita** pasirinkite banko sąskaitą. Jei šį lauką paliksite tuščią, ataskaitoje bus nurodyta visų banko sąskaitų banko operacijos informacija.
4. Pasirinkite **Gerai**, kad sugeneruotumėte šią ataskaitą. 

## <a name="calculate-exchange-rate-adjustments-for-bank-account-transactions"></a>Banko sąskaitos operacijų valiutos kurso koregavimo skaičiavimas

> [!IMPORTANT]
> Šis skyrius taikomas tik juridiniams subjektams, kurių pagrindinis adresas yra Čekijos Respublikoje, Estijoje, Lietuvoje ar Latvijoje.

Jus turi iš naujo įvertinti ir koreguoti banko sąskaitas, jei yra valiutos kurso skirtumas tarp apskaitos valiutos ir ataskaitų valiutos. Ši užduotis padeda apskaičiuoti tinkamą banko sąskaitų balansą tiek apskaitos, tiek ir finansinės atskaitomybės valiuta.

1. Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų ir banko valdymo parametrai**.
2. Skirtuko **Numeracijos** lauke **Nuoroda** pasirinkite nuorodos **Bankas – derinimas dėl valiutos kurso** numeraciją.
3. Uždarykite puslapį.
4. Pasirinkite **DK** &gt; **Sąranka** &gt; **Valiuta** &gt; **Valiutų kursai**. Puslapyje **Valiutų kursai** galite nurodyti valiutos kursą tarp dviejų valiutų ar valiutų porą.
5. Baigę uždarykite puslapį.
6. Pasirinkite **DK** &gt; **Sąranka** &gt; **DK**. Laukuose **Negautas pelnas** ir **Nepatirtas nuostolis** pasirinkite pagrindinę sąskaitą, kuriai valiutų keitimo kursai yra registruojami.
7. Uždarykite puslapį.
8. Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Periodinės užduotys** &gt; **Užsienio valiutos kurso pasikeitimas**.
9. Lauke **Nustatytai datai** pasirinkite pasikeitimo datą arba koregavimo datą.
10. Lauke **Iš valiutos** pasirinkite dabartinės valiutos kodą. Lauke **Į valiutą** pasirinkite valiutą, kurią reikia pakoreguoti.
11. Pasirinkite **Įtrauktini įrašai** &gt; **Filtras** ir raskite banko sąskaitą, tada pasirinkite **Gerai**.
12. Puslapyje **Užsienio valiutos kurso pasikeitimas** pasirinkite **Gerai**. Banko sąskaitos operacijų koregavimas apskaičiuojamas pasirinktai dienai.

> [!NOTE]
> Didžiojoje knygoje galite peržiūrėti dvi atskiras operacijas: apskaitos valiuta ir ataskaitų valiuta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]