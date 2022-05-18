---
title: „Power BI“ Kredito ir mokėjimų priežiūros valdymas
description: Šioje temoje paaiškinama, kas įtraukta į „Power BI“ turinį Kredito ir mokėjimų priežiūros valdymas. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.
author: ShivamPandey-msft
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 291eeddf754ef86bf7eb8f534ac36b1151e39b3a
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713506"
---
# <a name="credit-and-collections-management-power-bi-content"></a>„Power BI“ Kredito ir mokėjimų priežiūros valdymas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kas įtraukta į **Kredito ir mokėjimų priežiūros valdymo** „Microsoft Power BI“ turinį. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinys **Kredito ir mokėjimų priežiūros valdymas** buvo sukurtas kredito ir mokėjimų priežiūros vadybininkams ir mokėjimų priežiūros darbuotojams. Jame pateikiamos pagrindinės kredito ir mokėjimų priežiūros metrikos, pavyzdžiui, neapmokėta suma, pradelstas likutis, kredito ekspozicija ir kredito limitą viršiję klientai. Jame naudojami operaciniai duomenys ir pateikiami sujungti visų įmonių kredito ir mokėjimų priežiūros duomenų rodiniai. Jame taip pat pateikiamas paskirstymas kiekvienai įmonei, klientų grupei ir klientui.

Šį „Power BI“ turinį sudaro 10 puslapių ataskaita:

- dviejų puslapių peržiūra (vienas puslapis skirtas kredito peržiūrai, o kitas puslapis – mokėjimų peržiūrai)
- aštuoni išsamios informacijos puslapiai, kuriuose pateikiama informacija apie įvairiose dimensijose paskirstytas kredito ir mokėjimų priežiūros metrikas

Visos sumos rodomos sistemos valiuta. Sistemos valiutą galite nustatyti puslapyje **Sistemos parametrai**.

Pagal numatytuosius nustatymus rodomi šios įmonės kredito ir mokėjimų priežiūros duomenys. Norėdami pamatyti visų įmonių duomenis, vaidmeniui priskirkite pareigą **CustCollectionsBICrossCompany**.

## <a name="setup-needed-to-view-power-bi-content"></a>Norint peržiūrėti „Power BI“ turinį reikia atlikti sąranką

Kad duomenys būtų rodomi **Klientų kredito ir mokėjimų priežiūra** „Power BI“ vizualizacijose, reikia atlikti toliau nurodytą sąranką.

1. Eikite į **Sistemos administravimas > Sąranka > Sistemos parametrai** ir nustatykite **Sistemos valiuta** ir **Sistemos valiutos kursas**.
2. Eikite į **Didžioji knyga > Kalendoriai > Fiskaliniai kalendoriai** tam, kad patvirtintumėte fiskalinio kalendoriaus datas priskirtas aktyviam laikotarpiui.
3. Eikite į **Didžioji knyga > Sąranka > Didžioji knyga** ir nustatykite **Apskaitos valiuta** ir **Valiutos kurso tipas**.
4. Nustatykite valiutų keitimo kursus tarp perlaidų valiutų ir apskaitos valiutos, apskaitos valiutą ir sistemos valiutą. Norėdami tai padaryti, eikite į **Didžioji knyga > Valiutos > Valiutų kursai**.
5. Eikite į **Sistemos administravimas > Sąranka > Objektų saugykla** ir atnaujinkite agreguotą matavimo vienetą **CustCollectionsBIMeasurementsV2**.

>[!NOTE] 
> Skirstymo pagal terminus laikotarpio apibrėžimai turi būti nustatyti dalyje **Gautinų sumų parametrai > Mokėjimų priežiūra > Numatytoji mokėjimų peržiūra**, kad būtų įgalinti „Power BI” turinio skirstymo pagal terminus duomenys.

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio

„Power BI“ turinys **Kreditų ir mokėjimų priežiūros valdymas** rodomas darbo srityje **Klientų kredito ir mokėjimų priežiūra**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos ataskaitos

„Power BI“ turinio pakete **CustCollectionsBICrossCompany** yra ataskaita, sudaryta iš metrikų rinkinio. Šios metrikos vaizduojamos kaip diagramos, plytelės ir lentelės Toliau pateiktoje lentelėje pateikiama „Power BI“ turinio **CustCollectionsBICrossCompany** vizualizacijų apžvalga.

| Ataskaitų puslapis                 | Vizualizacija |
|-----------------------------|---------------|
| Mokėjimų priežiūros peržiūra        | <ul><li>Klientai, kurių terminas praėjęs</li><li>Klientai, viršijantys kredito limitą</li><li>DSO 30 dienų</li><li>Atviri atvejai</li><li>Dienų iki atvejo uždarymo vidurkis</li><li>Atvira veikla</li><li>Dienų iki veiklų uždarymo vidurkis</li><li>Atidarytos delspinigių pažymos</li><li>Atidaryti mokėjimų priežiūros laiškai</li><li>Kliento sulaikymas</li><li>Pardavimo sulaikymas</li><li>Suskirstyti pagal terminus balansai</li><li>Mokėjimų priežiūros būsenos sumos</li><li>Mokėjimų priežiūros kodo sumos</li><li>Nurašymas pagal priežastį</li><li>Skolos likutis pagal regioną</li><li>Numatyti mokėjimai</li></ul> |
| Kredito peržiūra             | <ul><li>Klientai, kurių terminas praėjęs</li><li>Kredito limitas ir skolos likutis</li><li>Klientai, viršijantys kredito limito tinklelį</li><li>Klientai, viršijantys kredito limitą, pagal įmonę</li><li>Išnaudotas kreditas ir bendras kredito limitas</li><li>Kredito limitas, palyginti su išnaudotu kreditu pagal regioną</li><li>Klientai pagal kredito vertinimą</li></ul> |
| Kredito limitas                | <ul><li>Kredito limitas</li><li>Informacija apie kredito limitą</li><li>Kiekvieno kliento kredito limitas</li><li>Kredito limitas pagal klientų grupę</li><li>Kredito limitas pagal kredito vertinimą pagal įmonę</li><li>Kredito limitas, palyginti su išnaudotu kreditu pagal regioną</li></ul> |
| Klientai, viršijantys kredito limitą | <ul><li>Klientai, viršijantys kredito limitą</li><li>Informacija apie klientus, viršijančius kredito limitą</li><li>Klientai, viršijantys kredito limitą, pagal įmonę</li><li>Klientas, viršijantis kredito limitą, pagal klientų grupę</li><li>Klientai, viršijantys kredito limitą, pagal regioną</li></ul> |
| Klientai, kurių terminas praėjęs          | <ul><li>Klientai, kurių terminas praėjęs</li><li>Informacija apie klientą, kurio terminas praėjęs</li><li>Kliento pradelsimai pagal įmonę</li><li>Klientas, pradelsęs terminą, pagal klientų grupę</li><li>Klientas, kurio terminas praėjęs, pagal regioną</li></ul> |
| Suskirstyti pagal terminus balansai               | <ul><li>Suskirstyti pagal terminus balansai</li><li>Informacija apie pagal terminus suskirstytus likučius</li><li>Suskirstyti pagal terminus balansai pagal įmonę</li><li>Suskirstyti pagal terminus balansai pagal klientų grupę</li></ul> |
| Numatyti mokėjimai           | <ul><li>Numatyti mokėjimai</li><li>Informacija apie numatytus mokėjimus</li><li>Numatyti mokėjimai pagal įmonę</li><li>Numatyti mokėjimai pagal klientų grupę</li><li>Numatyti mokėjimai pagal regioną</li></ul> |
| Nurašymai                  | <ul><li>Nurašymai pagal regioną</li><li>Nurašymų informacija</li><li>Nurašymai pagal pagrindinę sąskaitą</li><li>Nurašymai pagal įmonę</li><li>Nurašymai pagal klientų grupę</li><li>Nurašymai pagal regioną</li></ul> |
| Mokėjimų priežiūros būsena          | <ul><li>Užginčyta</li><li>Pažadas sumokėti sulaužytas</li><li>Pažadas sumokėti</li><li>Informacija apie mokėjimų priežiūros būseną</li><li>Mokėjimų priežiūros būsenos sumos</li><li>Atviri atvejai</li><li>Atvira veikla</li></ul> |
| Priminimo laiškai         | <ul><li>Priminimo laiško kodo sumos</li><li>Priminimo laiško kodo sumos informacija</li><li>Priminimo laiško suma pagal įmonę</li><li>Priminimo laiško suma pagal klientų grupę</li><li>Priminimo laiško suma pagal regioną</li></ul> |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Norėdami eksportuoti vizualiai apibendrintus pagrindinius duomenis, taip pat galite naudoti pagrindinių duomenų eksportavimo funkciją.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
