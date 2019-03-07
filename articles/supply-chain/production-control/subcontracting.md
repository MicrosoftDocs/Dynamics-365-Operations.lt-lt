---
title: Subranga
description: Šioje temoje paaiškinama, kaip sukurti subrangos vadovą kai gamyboje naudojama „Microsoft Dynamics 365 for Finance and Operations“.
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55b516f928eadea9b7ddbb1192db79f3ab7fa204
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "336709"
---
# <a name="subcontracting"></a>Subranga

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sukurti subrangos vadovą kai gamyboje naudojama „Microsoft Dynamics 365 for Finance and Operations“. Pirmoje šios temos dalyje aprašoma duomenų sąranka. Antroje dalyje aprašomi apžvalgos veiksmai.

## <a name="target-audience"></a>Tikslinė auditorija

Šioje temoje sužinosite, kaip nustatyti subrangą gamyboje. Naudokite esamus duomenis juridiniame subjekte HQUS norėdami atlikti pagrindinę subrangos veiklos srauto sąranką. Demonstraciniai duomenys juridiniame subjekte HQUS apima sąrankos parametrus, kurie buvo iš anksto nustatyti, kad būtų galima atlikti apžvalgos veiksmus. Nors apžvalgoje nurodyti įvairiems vaidmenims skirti klausimai ir problemos, apžvalgos veiksmus gali atlikti sistemos administratorius.

## <a name="demo-scenario"></a>Demonstracinis scenarijus

Juridiniame subjekte HQUS gaminami aukštos kokybės garsiakalbiai. Garsiakalbių gamybos procesą sudaro trys toliau nurodytos operacijos.

- **Išankstinis surinkimas** – surenkama garsiakalbio dėžė. Dėžės medžiaga paimama medžiagų sandėlyje prieš operacijos pradžią.
- **Padengimas** – surinktą garsiakalbio dėžę reikia padengti. Šią operaciją atlieka tiekėjas (rangovas). Iš anksto surinkta garsiakalbio dėžė siunčiama padengimo subrangovui kartu su dviem medžiagomis.
- **Baigimas** – kai subrangovas padengia iš anksto surinktą garsiakalbio dėžę, ji grąžinama juridiniam subjektui HQUS, kad būtų galima baigti galutinius surinkimo veiksmus.

Toliau pateiktoje iliustracijoje parodytos tys operacijos ir medžiagos, sunaudojamos jas atliekant.

![Išankstinio surinkimo, padengimo ir baigimo operacijos bei medžiagos, sunaudojamos jas atliekant](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Sąranka

Prieš pradėdami apžvalgos veiksmus, turite nustatyti duomenis.

### <a name="set-up-the-finished-product"></a>Baigto produkto sąranka

Šios procedūros metu bus nustatytas išleistas produktas D8100, „Padengta dėžė“.

1. Pasirinkite **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**, kad atidarytumėte puslapį **Išleisto produkto informacija**.
2. Sparčiojo filtro lauke įveskite **D8100**, kad rastumėte esamą išleistą produktą.

    ![Išleisto produkto D8100 filtravimas puslapyje Išleisto produkto informacija](./media/subcontract02_filtering-released-products.png)

3. Veiksmų srities skirtuke **Inžinierius** pasirinkite **Maršrutas**, kad atidarytumėte puslapį **Maršrutas**.

    Puslapyje **Maršrutas** rodomos aštuonios išleisto produkto D8100 maršruto versijos. Aštuonios maršruto versijos paskirstomos keturiems maršrutams 1 ir 5 vietose. Maršrutas 000400 naudojamas įkainojimo metu, maršrutas 00041 naudojamas atliekant padengimo operaciją viduje, o maršrutas 00042 naudojamas atliekant padengimo operaciją išorėje.

    ![Aštuonios maršruto versijos puslapyje Maršrutas](./media/subcontract03_route-page.png)

4. Viršutinės srities tinklelyje **Versijos** pasirinkite maršruto versiją **00042**, skirtą **5** vietai.
5. Apatinės srities skirtuke **Apžvalga**, tinklelyje pasirinkite **20** operaciją (**Cbnt CtSc**).

    ![Pasirinkta 00042 maršruto versijos operacija, skirta 5 vietai](./media/subcontract04_route-version-operation.png)

6. Pasirinkite skirtuką **Bendra**.

    Atkreipkite dėmesį, kad laukas **Maršruto tipas** nustatytas į parinktį **Tiekėjas**. Ši vertė nurodo, kad 20 operacija („Cbnt CtSc“) yra subrangos operacija.

    ![Skirtuko Bendra laukas Maršruto tipas nustatytas į parinktį Tiekėjas](./media/subcontract05_general-tab.png)

7. Pasirinkite skirtuką **Išteklių reikalavimai**.

    Galimybės bus naudojamos siekiant rasti tinkama išteklių gamybos planavimo metu. Atlikdami 20 operaciją („Cbnt CtSc“) atkreipkite dėmesį, kad būtinas išteklius, kuriam priskirtos dvi galimybės, **Padengimas** ir **Padengtos dėžės**.

    ![Skirtuko Išteklių reikalavimai galimybės Padengimas ir Padengtos dėžės](./media/subcontract06_resource-requirements-tab.png)

8. Pasirinkite **Taikomi ištekliai**, kad atidarytumėte dialogo langą **Taikomi ištekliai**.

    Rasti trys išteklių, atitinkantys operacijos išteklių reikalavimus. Atkreipkite dėmesį, kad ištekliai 8851 ir 8852 yra tipo **Tiekėjas**.

    ![Trys taikomi ištekliai dialogo lange Taikomi ištekliai](./media/subcontract07_applicable-resources-dialog.png)

9. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Taikomi ištekliai** ir vėl atidarytumėte puslapį **Maršrutas**.
10. Uždarykite puslapį **Maršrutas**, kad vėl atidarytumėte puslapį **Išleisto produkto informacija**.

    ![Puslapis Išleisto produkto informacija](./media/subcontract08_released-product-details-page.png)

11. Veiksmų srities skirtuke **Inžinierius** pasirinkite **KS versijos**, kad atidarytumėte puslapį **KS versijos**.

    Puslapyje **KS versijos** rodomos keturios komplektavimo specifikacijos (KS) versijos, skirtos išleistam produktui D8100. KS 000040 naudojama įkainojimo ir planavimo metu, KS 000041 naudojama, jei padengimo operacija atliekama įmonėje, o KS 000042 ir 000043 naudojamos, jei padengimo operaciją atlieka subrangovai.

    Atkreipkite dėmesį, kad prekė S8050 yra produktas, kurio prekės tipas yra **Paslauga**. Ši prekė nurodo subrangovo darbą.

    ![Keturios KS versijos puslapyje KS versijos](./media/subcontract09_bom-versions-page.png)

12. „FastTab“ **KS eilutės** pasirinkite **Redaguoti**, kad atidarytumėte dialogo langą **Redaguoti KS eilutę**.

    Kai išleisto produkto D8100 gamybos užsakymas yra sukurtas ir nustatytas, automatiškai sugeneruojamas prekės S8050 pirkimo užsakymas. Šis pirkimo užsakymas bus susietas su gamybos užsakymu. Tam, kad pirkimo užsakymai būtų automatiškai generuojami, laukas **Eilutės tipas** turi būti nustatytas į parinktį **Tiekėjas** ir turi būti pasirinkta subrangovo tiekėjo sąskaita. Šiuo atveju tiekėjo sąskaita yra US-801.

    Atkreipkite dėmesį, kad KS eilutė yra susieta su operacija Padengimas naudojant operacijos numerį (šiuo atveju – 20).

    ![Dialogo lango KS eilutė redagavimas](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Sandėlio darbuotojų slaptažodžio kūrimas

Turite nustatyti slaptažodį, skirtą sandėlio darbuotojams, kurie naudoja rankinius įrenginius.

1. Pasirinkite **Sandėlio valdymas \> Sąranka \> Darbuotojas**, kad atidarytumėte puslapį **Darbo vartotojai**.
2. „FastTab“ **Vartotojai** pasirinkite eilutę, skirtą vartotojui **51**.

    ![Puslapis Darbo vartotojai](./media/subcontract11_work-users-page.png)

3. Pasirinkite **Iš naujo nustatyti slaptažodį**.
4. Laukuose **Slaptažodis** ir **Patvirtinkite slaptažodį** įveskite **1**.
5. Pasirinkite **Nustatyti slaptažodį**.

## <a name="step-by-step-walkthrough"></a>Nuosekli apžvalga

**Scenarijus ir apžvalga**

Sukuriamas 10 vienetų gamybos užsakymas, skirtas produktui D8100, kuris vadinasi „Padengta dėžė“. Dėžių padengimas yra subrangos operacija, kurią atlieka tiekėjas US-801, „Perfect Coating Solutions“. Gamybos užsakymas susideda iš trijų operacijų. Pirmoji operacija yra išankstinio dėžės surinkimo operacija, atliekama įmonėje. Medžiagos, iš kurių iš anksto surenkama dėžė, paruošiamos paimti žaliavų sandėlyje. Baigus išankstinio surinkimo operaciją, iš anksto surinkta dėžė siunčiama „Perfect Coating Solutions“ kartu su dviem medžiagomis, kurių reikia padengimo operacijai atlikti. Kai padengta dėžė gaunama iš tiekėjo, atliekama galutinė surinkimo operacija įmonėje prieš paskelbiant operaciją baigta.

1. Pasirinkite **Gamybos kontrolė \> Gamybos užsakymai \> Visi gamybos užsakymai**, kad atidarytumėte puslapį **Visi gamybos užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas gamybos užsakymas**, kad atidarytumėte dialogo langą **Kurti gamybos užsakymą**.

    ![Dialogo langas Kurti gamybos užsakymą](./media/subcontract12_create-production-order-dialog.png)

3. Lauke **Prekės numeris** pasirinkite **D8100**.
4. Atsargų dimensijų laukai rodomi pasirinkus prekės numerį. Lauke **Spalva** pasirinkite **Chromuota**.

    Pasirodys pranešimo langas, kuriame klausiama, ar įterpti aktyvias KS ir maršruto versijas.

    ![Pranešimo laukas](./media/subcontract13_message-box.png)

5. Pasirinkite **Taip**. 

    Dialogo lange **Kurti gamybos užsakymą** aktyvios KS ir maršruto versijos, skirtos produktui D8100, yra automatiškai pasirenkamos laukuose **KS numeris** ir **Maršruto numeris** atitinkamai. Šiuo atveju pasirenkami KS **000040** ir maršrutas **000040**.
    
    > [!NOTE]
    > KS ir maršruto versija 000040 naudojama įkainojimo ir planavimo metu.

6. Lauke **Vieta** pasirinkite **5**.
7. Lauke **Sandėlis** pasirinkite **51**.
8. Laukuose **KS numeris** ir **Maršruto numeris** pakeiskite reikšmę, kuri buvo automatiškai pasirinkta, į **000042**.

    > [!NOTE]
    > KS ir maršruto versija 000042 naudojama teikiant dėžės padengimo subrangos užduotį tiekėjui US-801.

    ![Dialogo lange Kurti gamybos užsakymą nustatomos reikšmės](./media/subcontract14_create-production-order-dialog-set.png)

9. Pasirinkite **Kurti**, kad sukurtumėte gamybos užsakymą ir atidarytumėte puslapį **Visi gamybos užsakymai**.

    ![Naujas gamybos užsakymas puslapyje Visi gamybos užsakymai](./media/subcontract15_new-production-order.png)

10. Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **Įvertinti**, kad atidarytumėte dialogo langą **Įvertinti**.

    ![Dialogo langas Įvertinti](./media/subcontract16_estimate-dialog.png)

11. Pasirinkite **Gerai**, kad patvirtintumėte įvertinimą ir atidarytumėte puslapį **Visi gamybos užsakymai**.

    > [!NOTE]
    > Vertinant gamybos užsakymą, aptarnavimo prekės S8050 pirkimo užsakymas generuojamas pasirenkant tiekėją US-801.

12. Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **KS**, kad atidarytumėte puslapį **KS**, kuriame galite peržiūrėti gamybos užsakymo KS eilutes.

    Aptarnavimo prekė S8050: atkreipkite dėmesį, kad pateikta nuoroda į pirkimo užsakymą, kuri buvo sugeneruota įvertinant gamybos užsakymą.

    ![Gamybos užsakymo KS eilutės KS puslapyje](./media/subcontract17_production-order-bom-lines.png)

13. Uždarykite puslapį **KS**, kad vėl atidarytumėte puslapį **Visi gamybos užsakymai**.
14. Veiksmų srities skirtuke **Grafikas** pasirinkite **Grafiko užduotys**, kad atidarytumėte dialogo langą **Užduočių planavimas**.
15. Nurodykite toliau nurodytas reikšmes.

    - Lauke **Planavimo kryptis** pasirinkite **Pradedant nuo rytojaus**.
    - Nustatykite parinktį **Ribotas pajėgumas** į **Taip**.

    ![Dialogo langas Užduočių planavimas](./media/subcontract18_job-scheduling-dialog.png)

16. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Užduočių planavimas** ir vėl atidarytumėte puslapį **Visi gamybos užsakymai**.
17. Veiksmų srities skirtuke **Grafikas** pasirinkite **Gantt**, kad atidarytumėte puslapį **Gantt diagrama – išteklių rodinys**.

    Gantt diagramoje pateikiama vaizdinė gamybos užduočių planavimo ir priskyrimo ištekliams apžvalga. Atkreipkite dėmesį, kad išorės operacija Padengimas susideda iš trijų užduočių: apdorojimo užduoties, transportavimo užduoties ir laukimo eilėje laiko užduoties.

    ![Ganto diagrama Gantt diagramoje – išteklių peržiūros puslapis](./media/subcontract19_gantt-chart.png)

18. Uždarykite puslapį **Gantt diagrama – išteklių peržiūra**, kad vėl atidarytumėte puslapį **Visi gamybos užsakymai**.
19. Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **Išleisti**, kad atidarytumėte dialogo langą **Išleisti**.

    ![Dialogo langas Išleisti](./media/subcontract20_release-dialog.png)

20. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Išleisti**.
21. Pasirinkite **Gamybos kontrolė \> Periodinės užduotys \> Išleidimas į sandėlį \> Automatinis KS ir formulės eilučių išleidimas**, kad atidarytumėte dialogo langą **Automatinis KS ir formulės eilučių išleidimas**.

    ![Dialogo langas Automatinis KS ir formulių eilučių išleidimas](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Pasirinkite **Gerai**, kad paleistumėte automatinio KS ir formulės eilučių išleidimo užduotį.

    Ši užduotis išleidžia žaliavų paėmimo iš sandėlio užduotį.

23. Pasirinkite **Gamybos kontrolė \> Gamybos užsakymai \> Visi gamybos užsakymai**, kad atidarytumėte puslapį **Visi gamybos užsakymai**.
24. Naudokite sparčiojo filtro lauką, kad pasirinktumėte gamybos užsakymą, su kuriuo dirbote.
25. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Darbo informacija**, kad atidarytumėte puslapį **Darbas**.

    Atkreipkite dėmesį, kad puslapyje rodomi du žaliavų paėmimo darbo rinkiniai. Pirmasis darbas yra medžiagų M8100 ir M8101 paėmimas. Šios medžiagos vartojamos atliekant 10 operaciją. Antrasis darbas yra medžiagų M8202 ir M8250 paėmimas. Šios medžiagos vartojamos atliekant 20 operaciją, kuri yra subrangos operacija.

    ![Puslapyje Darbas rodomi du žaliavų paėmimo darbo rinkiniai](./media/subcontract22_work-page.png)

26. Paleiskite sandėlio programą, kad apdorotumėte 10 operacijos sandėlio darbą.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Pasirinkite **Gamybos kontrolė \> Gamybos užsakymai \> Visi gamybos užsakymai**, kad atidarytumėte puslapį **Visi gamybos užsakymai**.
28. Naudokite sparčiojo filtro lauką, kad pasirinktumėte gamybos užsakymą, su kuriuo dirbote.
29. Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **Pradėti**, kad atidarytumėte dialogo langą **Pradėti**.
30. Skirtuke **Bendra** įveskite toliau nurodytas reikšmes.

    - Lauke **Šaltinio oper. nr.** pasirinkite **10**.
    - Lauke **Paskirties oper. nr.** pasirinkite **10**.

    ![Skirtuke Bendra nustatomos reikšmės](./media/subcontract23_start-dialog.png)

31. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Pradėti** ir vėl atidarytumėte puslapį **Visi gamybos užsakymai**.

    Atkreipkite dėmesį, kad dabar gamybos užsakymo būsena yra **Pradėtas**. 10 operacijos medžiagos naudojamos vykdant automatinį išrinkimo žurnalo registravimą. 10 operacijos laiko sąnaudos užregistruojamos vykdant automatinį maršruto kortelės žurnalo registravimą.

32. Paleiskite sandėlio programą, kad apdorotumėte 20 operacijos sandėlio darbą.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. Veiksmų srities skirtuke **Gamybos užsakymas** pasirinkite **Pradėti**, kad atidarytumėte dialogo langą **Pradėti**.
34. Skirtuke **Bendra** įveskite toliau nurodytas reikšmes.

    - Lauke **Šaltinio oper. nr.** pasirinkite **20**.
    - Lauke **Paskirties oper. nr.** pasirinkite **20**.
    - Lauke **Kiekis** įveskite **10**.
    - Nustatykite lauko **Registruoti išrinkimo dokumentą dabar** parinktį **Ne**.

    ![Skirtuke Bendra nustatomos reikšmės](./media/subcontract24_general-tab.png)

35. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Pradėti** ir vėl atidarytumėte puslapį **Visi gamybos užsakymai**.

    Sukuriamas medžiagų, kurios naudojamos atliekant padengimo operaciją, ir aptarnavimo prekės išrinkimo dokumentas. Aptarnavimo prekė nurodo subrangos operacijos savikainą.

36. Veiksmų srities skirtuke **Rodinys** pasirinkite **Išrinkimo dokumentas**, kad atidarytumėte puslapį **Išrinkimo dokumentas**.
37. Pasirinkite išrinkimo dokumentą, kuris nėra užregistruotas, tada pasirinkite žurnalo numerį, kad peržiūrėtumėte žurnalo eilutes.

    ![Žurnalo eilutės puslapyje Išrinkimo dokumentas](./media/subcontract25_picking-list.png)

38. Veiksmų srityje pasirinkite **Spausdinti** \> **Išrinkimo dokumento ataskaita**, kad atidarytumėte dialogo langą **Išrinkimo dokumento ataskaita**.
39. Nustatykite parinktį **Naudoti pristatymo pažymos maketą** į **Taip**.

    ![Dialogo langas Išrinkimo dokumento ataskaita](./media/subcontract26_picking-list-report-dialog.png)

40. Pasirinkite **Gerai**, kad generuotumėte ataskaitą **Išrinkimo dokumentas**.

    Šiuo atveju tiekėjo pristatymo pažyma išspausdinta iš gamybos išrinkimo dokumento žurnalo. Pristatymo pažymoje nurodomos medžiagos, siunčiamos tiekėjui, kuris atliks operaciją Padengimas.

    ![Išrinkimo dokumentų ataskaita](./media/subcontract27_picking-list-report.png)

41. Uždarykite ataskaitą **Išrinkimo dokumentas**, kad vėl atidarytumėte puslapį **Išrinkimo sąrašas**.
42. Veiksmų srityje pasirinkite **Registruoti**, kad atidarytumėte dialogo langą **Registruoti žurnalą**.

    ![Dialogo langas Registruoti žurnalą](./media/subcontract28_post-journal-dialog.png)

43. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Registruoti žurnalą**.
44. Atidarykite pirkimo užsakymą.

    ![Puslapis Pirkimo užsakymas](./media/subcontract29_purchase-order-page.png)

45. Veiksmų srities skirtuke **Pirkimas** pasirinkite **Patvirtinti**.
46. Pasirinkite **Registruoti**, kad atidarytumėte dialogo langą **Registruoti žurnalą**.
47. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą **Registruoti žurnalą** ir vėl atidarytumėte puslapį **Pirkimo užsakymas**.
48. Pakeiskite vieneto kainą **33** į **40**.

    ![Vieneto kaina pakeista puslapyje Pirkimo užsakymas](./media/subcontract30_unit-price.png)

49. Patvirtinkite pirkimo užsakymą dar kartą.
50. Gavimo kvitas.

    ![Dialogo langas Gavimo dokumento registravimas](./media/subcontract31_posting-product-receipt-dialog.png)

51. Pirkimo SF.
52. Atnaujinkite gretinimo būseną.

    ![Puslapis Tiekėjo SF](./media/subcontract32_vendor-invoice-page.png)

53. Skelbkite baigtu.

    ![Dialogo langas Skelbimas baigtu](./media/subcontract33_report-as-finished-dialog.png)

54. Baikite.

    ![Dialogo langas Baigimas](./media/subcontract34_end-dialog.png)

55. Savikainos palyginimas.

    ![Savikainos palyginimo diagramos](./media/subcontract35_cost-comparison-charts.png)

Trūksta sąrankos duomenų.
