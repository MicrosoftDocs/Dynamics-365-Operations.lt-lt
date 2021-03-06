---
title: EUR-00011, ES pardavimo sąrašo ataskaitos generavimas.
description: Ši procedūra padeda generuoti ES pardavimų sąrašo ataskaitą.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ce3fa3eaae48499e58228d9d6dbf7ce7e97d2bd8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821836"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a>EUR-00011, ES pardavimo sąrašo ataskaitos generavimas.

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda generuoti ES pardavimų sąrašo ataskaitą. Tai apima ES vidaus prekybos operacijų perkėlimą į ES pardavimų sąrašą ir ataskaitos vykdymą. Ši procedūra taip pat apima ES vidaus prekybos operacijos kūrimą demonstraciniais tikslais. Daugiau informacijos apie ES pardavimo sąrašų ataskaitas, įskaitant būtinąsias sąlygas, žr. žinyne.

Ši procedūra taikoma visoms Europos šalims / regionams. Procedūra buvo sukurta naudojant demonstracinių duomenų įmonę DEMF ir dėl to kaip šalies / regiono pavyzdį naudojant Vokietiją. Procedūroje taip pat kaip ES šalies / regiono pavyzdys naudojama Portugalija. Prieš atlikdami šią procedūrą, turite sukonfigūruoti ES pardavimų sąrašo ataskaitas.

Ši procedūra skirta buhalteriams.


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a>Kurti ES vidaus pardavimo operaciją demonstraciniais tikslais
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite „PRT-001“.
4. Spustelėkite GERAI.
5. Lauke „Prekės numeris“ įveskite „D0001“.
6. Išplėskite skyrių Eilutės informacija.
7. Spustelėkite skirtuką Nustatymas.
8. Lauke Prekės PVM grupė įveskite 'VISAS'.
9. Spustelėkite Pridėti eilutę.
10. Lauke „Prekės numeris“ įveskite „D0003“.
11. Lauke Prekės PVM grupė įveskite 'RAUDONA'.
12. Spustelėkite Įrašyti.
13. Veiksmų srityje spustelėkite Sąskaita faktūra.
14. Spustelėkite Sąskaita faktūra.
15. Išplėskite skyrių Parametrai.
16. Lauke Kiekis pasirinkite Visi.
17. Išplėskite skyrių Nustatymas.
18. Lauke SF data nustatykite datą '01/11/2016'.
19. Spustelėkite GERAI.
20. Spustelėkite GERAI.

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a>Perkelti ES vidaus prekybos operacijas į ES pardavimų sąrašą
1. Eikite į Mokestis > Deklaracijos > Užsienio prekyba > ES pardavimų sąrašas.
2. Spustelėkite Perkelti.
3. Lauke Prekė pasirinkę Taip perkelsite prekės operacijas.
4. Lauke Paslauga pasirinkę Taip perkelsite paslaugos operacijas.
    * Taip pat galite nurodyti papildomus filtrus ES vidaus prekybos operacijoms perkelti.  
5. Spustelėkite Perkelti.
    * Patvirtinkite, kad ES vidaus pardavimo operacija sėkmingai perkelta į ES pardavimo sąrašą.  

## <a name="generate-the-eu-sales-list-report"></a>Generuoti ES pardavimo sąrašo ataskaitą
1. Spustelėkite Ataskaitos.
2. Lauke Ataskaitinis laikotarpis pasirinkite 'Mėnesinis'.
3. Lauke Pradžios data nustatykite datą '01/01/2016'.
4. Lauke Generuoti failą pasirinkite Taip.
5. Lauke Generuoti ataskaitą pasirinkite Taip.
6. Lauke Failo pavadinimas įveskite 'EUSalesList'.
7. Lauke Ataskaitos failo pavadinimas įveskite 'EUSalesList'.
8. Lauke ES pardavimo sąrašo registracijos ID įveskite '123'..
    * Šis laukas galimas tik Vokietijai.  
    * Be to, galite nurodyti papildomus norimus įtraukti į ataskaitą filtrus ES vidaus prekybos operacijoms.  
9. Spustelėkite GERAI.
    * Patikrinkite, ar laikinieji langai rodomi patvirtinti, ir kad failas ir kontrolės ataskaita atsisiunčiami.  

## <a name="mark-eu-sales-list-lines-as-reported"></a>Pažymėti ES pardavimų sąrašo eilutes kaip Paskelbtas
1. Spustelėkite Žymėti.
2. Spustelėkite Pažymėti kaip baigtus.
3. Sąraše pasirinkite lauko SF data eilutę.
4. Lauke Kriterijai įveskite '01/01/2016... 01/31/2016'.
5. Sąraše pasirinkite lauko Ataskaitos būsena eilutę.
6. Lauke Kriterijai pasirinkite 'Įtraukta'.
    * Be to, galite nurodyti papildomus norimus pažymėti kaip Paskelbtus filtrus ES vidaus prekybos operacijoms.  
7. Spustelėkite GERAI.
8. Lauke Pasirinkimas pasirinkite 'Ataskaita paruošta'.

## <a name="mark-eu-sales-list-lines-as-closed"></a>Pažymėti ES pardavimų sąrašo eilutes kaip Uždarytas
1. Spustelėkite Žymėti.
2. Spustelėkite Pažymėti kaip uždarytus.
3. Sąraše pažymėkite lauko SF data eilutę.
4. Lauke Kriterijai įveskite '01/01/2016... 01/31/2016'.
5. Sąraše pažymėkite lauko Ataskaitos būsena eilutę.
6. Lauke Kriterijai pasirinkite „Ataskaita paruošta“.
    * Be to, galite nurodyti papildomus norimus pažymėti kaip Uždarytus filtrus ES vidaus prekybos operacijoms.  
7. Spustelėkite GERAI.
8. Lauke Pasirinkimas pasirinkite 'Uždaryta'.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]