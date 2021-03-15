---
title: Gavimų apžvalga
description: Šioje temoje pateikiama informacija apie Gavimų apžvalgos funkciją. Gavimų apžvalgos puslapyje, kuris yra šios funkcijos dalis, pateikiama visų numatomų pristatyti prekių, kaip gaunamų prekių, peržiūra.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 89f885cbbe6a5001b507cd9fb1516733f8faee0f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005282"
---
# <a name="arrival-overview"></a>Gavimų apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie Gavimų apžvalgos funkciją. Gavimų apžvalgos puslapyje, kuris yra šios funkcijos dalis, pateikiama visų numatomų pristatyti prekių, kaip gaunamų prekių, peržiūra.

Puslapyje **Gavimų apžvalga** pateikiama visų numatomų gaunamų prekių peržiūra. Jame taip pat rodomi gavimai, kuriuos galima inicijuoti remiantis peržiūra. Šioje temoje dėmesys skiriamas gavimo procesui.

## <a name="business-scenario"></a>Verslo scenarijus
Atsižvelkite į toliau pateiktą gavimo procesų scenarijų.

[![Verslo scenarijus](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Sammy, gavimo klerkas, nori sužinoti, ką šią dieną numatoma gauti. Puslapyje **Gavimų apžvalga** Sammy gali peržiūrėti esamas užduotis ir apytikriai įvertinti kiekius, tūrį, svorį, skirtingus užsakymo tipus ir t. t. Vėliau užsakymas pristatomas į vieną iš atvežimo rampų ir Sammy gauna pristatymo sąrašą. Puslapyje **Gavimų apžvalga** Sammy gali atlikti toliau nurodytas užduotis.

-   Nustatyti atitinkamą gavimo užsakymą ir registruoti gavimą kaip **Vykdomas**. Registracijai reikalingos eilutės generuojamos automatiškai, o gavimą galima stebėti, net jei operacijos dar neužregistruotos kaip **Užregistruota**.
-   Pasiekti atitinkamą gavimo žurnalo nuorodą (t. y. žurnalą **Prekių gavimas** arba **Gamybos įvestis**) ir identifikuoti gavimo dokumentui naujinti paruoštus žurnalus.

## <a name="arrival-overview-page"></a>Gavimų apžvalgos puslapis
Norėdami atidaryti puslapį **Gavimų apžvalga**, spustelėkite **Atsargų valdymas** &gt; **Gaunami užsakymai** &gt; **Gavimų apžvalga**. Galite peržiūrėti numatomų gauti užsakymų sąrašą. Peržiūra padalinta į antraštę ir eilutes. Antraštės informacija sugrupuota pagal užsakymo tipą, numatomą gavimo datą ir pristatymo paskirtį. Pasirinkus gavimui skirtą antraštės eilutę, visos su gavimo nuoroda susijusios informacijos eilutės pasirenkamos gavimui skirtoje puslapio eilutės informacijos dalyje. Užregistravus visas susijusias žurnalo eilutes, ši informacija nerodoma.

### <a name="arrival-overview-profiles"></a>Gavimo apžvalgos šablonai

Puslapyje **Gavimų apžvalga** pateikiama numatomų pristatyti prekių peržiūra ir data. Vykdant gavimo procesą galima naudoti kelis asmeninių parametrų rinkinius. Savo asmeninius parametrus atskiri vartotojai gali nustatyti puslapyje **Gaunamų prekių apžvalgos profiliai**.

### <a name="set-up-item-arrival"></a>Nustatyti prekių gavimą

Pateiktame pavyzdyje Sammy nori nustatyti naują kompiuterį vietoje, kuri bus naudojama pagamintoms prekėms iš 1 gamybos vietos gauti. Puslapyje **Gaunamų prekių apžvalgos profiliai** Sammy sukuria naują nustatymą, pavadintą **1 gamybos vieta**, ir nurodo šiuos parametrus.

1.  „FastTab” skirtuko **Gavimo parinktys** laukų grupėje **Diapazonas** įveskite informaciją apie dienos intervalą ir sandėlius, kurie bus įtraukti į peržiūrą.
2.  „FastTab” skirtuko **Gavimo parinktys** laukų grupėje **Žurnalas** įveskite gavimo sandėlį, vietą ir žurnalo pavadinimą (prekių gavimo / gamybos įvesties).
3.  „FastTab” skirtuko **Gavimo užklausos informacija** laukų grupės **Vieta** lauke **Apriboti į vietą** įveskite vietą, kurioje reikia apriboti rodomą peržiūros sritį.
4.  „FastTab” skirtuko **Gavimo užklausos informacija** laukų grupės **Rodomi operacijų tipai** parinktį **Gamybos užsakymai** nustatykite į **Taip**.
5.  „FastTab” skirtuko **Gavimo užklausos informacija** grupės **Įvairūs** parinktį **Atnaujinti paleidžiant** nustatykite į **Taip**, jei paleisties metu reikia automatiškai atnaujinti rodinį. Parinktį **Atnaujinti keičiant diapazoną** nustatykite į **Taip**, jei pakeitus diapazono reikšmes reikia automatiškai atnaujinti rodinį.

Šiuo atveju laukas **Gaunamų prekių apžvalgos profilio pavadinimas** „FastTab“ skirtuke **Gavimo parinktys**, esančiame puslapyje **Gavimų apžvalga**, nustatytas kaip **1 gamybos vieta**.

### <a name="prerequisites-for-arrival-journals"></a>Būtinos gavimo žurnalų sąlygos

Norėdami automatiškai kurti gavimo žurnalus puslapyje **Gavimų apžvalga**, turite nurodyti atitinkamą informaciją laukų grupėje **Žurnalas**, esančioje „FastTab“ skirtuke **Gavimo parinktys**.

-   Norėdami sukurti žurnalą turite nurodyti žurnalo pavadinimą.

[![Nurodomas žurnalo pavadinimas](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Jei nurodote laukų **Sandėlis** ir **Vieta** reikšmes, jos taikomos žurnalo eilutėse. Jei nenurodote reikšmių, sistemoje naudojamos atsargų operacijose nurodytų dimensijų reikšmės.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Prekės, gautos iš numatomo gavimo užsakymo

„FastTab“ skirtuke **Gavimai** Sammy pasirenka eilutę ir tada spusteli **Pradėti gavimo žurnalą**. Visos susijusios nurodyto diapazono ir registruojamo kiekio eilutės pasirenkamos automatiškai. Generuojamas prekių gavimo žurnalas sutampa su numatomu gavimo užsakymu ir žurnalu. Kiekis inicijuojamas automatiškai visose sukurtose eilutėse.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Prekės, gautos iš daugiau nei vieno numatomo gavimo užsakymo

„FastTab“ skirtuke **Gavimai** Sammy pasirenka kelias eilutes ir tada spusteli **Pradėti gavimo žurnalą**. Generuojamas prekių gavimo žurnalas sutampa su visais numatomais gavimo užsakymais ir žurnalu. Visos eilutės kuriamos vienoje prekių gavimo žurnalo antraštėje, o kiekis inicijuojamas automatiškai.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Gauti prekes iš vieno ar daugiau numatomų gavimo užsakymų

#### <a name="view-information"></a>Peržiūrėti informaciją

Norėdamas peržiūrėti numatomus tam tikro laikotarpio gavimus Sammy įveda šią informaciją „FastTab“ skirtuko **Gavimo parinktys**, esančio puslapyje **Gavimų apžvalga**, laukuose ir tada spusteli **Naujinti**, kad atnaujintų rodinį:

-   Gaunamų prekių apžvalgos profilio pavadinimas: **Užklausa**
-   Rodyti eilutes: **Visi**
-   Dienos, skaičiuojant atgal: (tuščia)
-   Dienos, skaičiuojant pirmyn: **0**
-   Sandėliai: **GW, MW**

Sammy gali peržiūrėti šią informaciją:

-   Visus susijusius sistemos datos ir neriboto dienų, skaičiuojant atgal nuo sistemos datos, skaičiaus gavimo užsakymus (**InventTrans.StatusDate** intervalu), taip pat sandėlių GW ir MW gavimus, neatsižvelgiant į jų būseną.
-   Išsamią daugiau nei vieno užsakymo eilutės informaciją. Peržiūros metu Sammy gali pasirinkti kelias antraštės eilutes, o tada spustelėti **Rodyti visas pasirinktas**, kad peržiūrėtų išsamią visų atitinkamų eilučių informaciją, skirtą visiems pasirinktiems užsakymams.
-   Informacija apie konkretų pirkimo užsakymą. Norėdamas rodyti tik informaciją, susijusią su konkrečiu nuorodos numeriu peržiūroje, Sammy gali įvesti sąskaitos numerį lauke **Sąskaitos numeris** ir užsakymo numerį lauke **Nuorodos numeris**.
-   Visoms prekių gavimo žurnale sukurtoms, bet dar neužregistruotoms užsakymo eilutėms reikiamų registravimo užduočių peržiūra. Norėdamas peržiūrėti šią informaciją Sammy gali pasirinkti būseną **Vykdoma**, esančią lauke **Rodyti eilutes**.

### <a name="update-journals"></a>Naujinti žurnalus

Norėdamas užregistruoti vieną ar daugiau užsakymo eilučių, kurias reikia apdoroti, Sammy gali pasirinkti eilutes peržiūros arba eilučių tinklelyje, o tada spustelėti **Žurnalai** &gt; **Rodyti gavimų žurnalus pagal gavimus**. Rodomos eilutes atitinkančios prekių gavimo antraštės. Norėdamas atnaujinti užregistruotų prekių pirkimo užsakymo gavimo dokumentą, Sammy gali pasiekti paruoštas naujinti prekių gavimo žurnalo antraštes. Norėdamas pasiekti šias prekių gavimo žurnalo antraštes jis spusteli **Žurnalai** &gt; **Paruošti gavimo dokumentų žurnalai**. Rodomos visos antraštės eilutės, paruoštos gavimo dokumentui nurodyto sandėlio diapazone naujinti. (Rodomos antraštės eilutės nėra susijusios su dienos intervalu).

### <a name="start-an-arrival-registration"></a>Pradėti pristatymo registravimą

Pasirinkęs kelias eilutes puslapyje **Gavimų apžvalga**, Sammy gali pradėti daugiau nei vienos gavimo nuorodos pristatymą. Pasirinkus gavimų peržiūros eilutę, pasirenkama atitinkamos eilutės informacija. Jei pateiktas registracijos kiekis, galima naudoti mygtuką **Pradėti gavimo žurnalą**. Pradėti pristatymo registravimą Sammy gali dviem būdais:

-   Filtruoti puslapį taip, kad lauke **Tiekėjo nuoroda** būtų rodomi tik nurodytus kriterijus atitinkantys įrašai, ir iš tiekėjo nuskaityti nuorodos numerį, pvz., pristatymo pažymos brūkšninį kodą.
-   Puslapio **Gavimų apžvalga** peržiūros arba informacijos dalyje rankiniu būdu pasirinkti pristatymo registravimo įrašus ar juos atšaukti. Po to, kai Sammy spusteli **Pradėti gavimo žurnalą**, pasirinkti įrašai prekių gavimo žurnale sukuriami automatiškai. Įrašai apima eilutės informaciją ir priskirtų visų unikalių laukų informaciją.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Atnaujinti gavimo informaciją ir apdoroti gavimo dokumentą
Kai visos prekės užregistruotos, sandėlio vadybininkas arba pirkimo vadybininkas gali atnaujinti gautas prekes gavimo dokumentu, kad pridėtų faktines išlaidas. Norėdami atnaujinti gavimo informaciją ir užregistruoti gavimo dokumentą, atlikite toliau nurodytus veiksmus.

1.  Spustelėkite **Atsargų valdymas** &gt; **Gaunami užsakymai** &gt; **Gavimų apžvalga**.
2.  Puslapyje **Gavimų apžvalga** spustelėkite **Žurnalai** &gt; **Paruošti gavimo dokumentų žurnalai**, kad būtų rodomas žurnalų, paruoštų gavimo dokumentui naujinti, sąrašas.
3.  Pasirinkite žurnalus, kuriuos reikia atnaujinti, ir spustelėkite **Funkcijos** &gt; **Gavimo dokumentas**.
4.  Puslapyje **Registravimas** įveskite gavimo dokumento numerį žurnale, jei to dar nepadarėte, ir tada spustelėkite **Gerai** gavimo dokumentui apdoroti.

## <a name="summary"></a>Suvestinė
Naudodami **Gavimų apžvalgos** puslapį sandėlio vadovas ir darbuotojai gali lengviau peržiūrėti numatomus darbus, kuriuos reikės atlikti kaip gavimo proceso dalį. Puslapį taip pat galima naudoti prekių gavimo procesui pradėti ir siekiant užtikrinti, kad prekės yra sekamos pirmuoju įvežimu į sandėlį.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]