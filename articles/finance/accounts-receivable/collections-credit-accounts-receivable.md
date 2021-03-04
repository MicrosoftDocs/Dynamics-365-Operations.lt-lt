---
title: Surinkimas gautinų sumų modulyje
description: Gautinų sumų surinkimo informacija valdoma viename centriniame rodinyje naudojant „Microsoft Dynamics 365 Finance“ puslapį Surinkimas. Naudodami šį centrinį rodinį kredito ir surinkimo vadovai gali valdyti surinkimą. Surinkimo agentai pradėti surinkimo procesą gali iš klientų sąrašų, kurie sugeneruojami naudojant iš anksto apibrėžtus surinkimo kriterijus, arba iš puslapio Klientai.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustAgingSnapshot, CustBankAccounts, CustCollections, CustCollectionsActivitiesListPage, CustCollectionsAgent, CustCollectionsCaseListPage, CustCollectionsPool, CustCollectionsPoolsListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3061
ms.assetid: fd851520-8d93-434b-845b-be127d6ac3a6
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c150eb7283b34c82e728da36ed0e1e6643eff46a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445866"
---
# <a name="collections-in-accounts-receivable"></a>Surinkimas gautinų sumų modulyje

[!include [banner](../includes/banner.md)]

Gautinų sumų surinkimo informacija valdoma viename centriniame rodinyje naudojant „Microsoft Dynamics 365 Finance“ puslapį Surinkimas. Naudodami šį centrinį rodinį kredito ir surinkimo vadovai gali valdyti surinkimą. Surinkimo agentai pradėti surinkimo procesą gali iš klientų sąrašų, kurie sugeneruojami naudojant iš anksto apibrėžtus surinkimo kriterijus, arba iš puslapio Klientai.

Prieš pradėdami kurti ar dirbti su mokėjimų priežiūra, turite susipažinti su šiomis sąvokomis:
-   Klientų skirstymo pagal terminus momentinėje kopijoje yra skirstymo pagal terminus likučio informacija tam tikru metu
-   Klientų mokėjimų priežiūros telkiniai padės organizuoti darbą
-   Mokėjimų priežiūros agentai gali turėti savo klientų telkinius
-   Sąrašų puslapiuose organizuojami mokėjimų priežiūros klientai, veikla ir atvejai
-   Visa mokėjimų priežiūros informacija klientui yra viename puslapyje, ir iš šio puslapio galite imtis veiksmų
-   Atsisakyti, grąžinti arba atšaukti palūkanas ir mokesčius galima vienu veiksmu
-   Sukurti nurašymo operacijas galima vienu veiksmu
-   Apdoroti nepakankamų lėšų (NSF), mokėjimus galima vienu veiksmu

Šiuose skyriuose aprašyta kiekviena sąvoka.

## <a name="customer-aging-snapshots"></a>Klientų skirstymo pagal terminus momentinės kopijos
Skirstymo pagal terminus momentinėje kopijoje yra kliento skirstymo pagal terminus likučio informacija tam tikru metu. Ši informacija rodoma pagal terminus suskirstytų likučių puslapyje mokėjimų priežiūros puslapyje. Skirstymo pagal terminus momentinę kopiją reikia sukurti prieš peržiūrint mokėjimų priežiūros sąrašo puslapius. 

Kiekvienam klientui, skirstymo pagal terminus momentinė kopija turi skirstymo pagal terminus momentinės kopijos antraštę ir duomenų įrašus, kurie atitinka kiekvieną skirstymo pagal terminus laikotarpį skirstymo pagal terminus laikotarpio apibrėžime. 

Skirstymo pagal terminus momentinės kopijos antraštėje yra bendra mokėtina suma, kredito limitas, važtaraščio suma, pardavimo užsakymo suma, ginčijamų operacijų skaičius ir bendra ginčijamų operacijų suma kliento sąskaitoje. Visos kliento operacijos yra įtrauktos į šių sumų apskaičiavimą. Bendra suma, kredito limitas, važtaraščio suma ir pardavimo užsakymo suma yra rodoma Kredito informacijos „FactBox“ mokėjimų priežiūros puslapyje. 

Kiekvienam skirstymo pagal terminus laikotarpiui skirstymo pagal terminus laikotarpio apibrėžime sukuriamas skirstymo pagal terminus momentinės kopijos duomenų įrašas. Kiekviename skirstymo pagal terminus momentinės kopijos duomenų įraše yra skirstymo pagal terminus laikotarpio ID ir bendra suma operacijų, kurių datos patenka į skirstymo pagal terminus laikotarpį. Operacijos priskirtos skirstymo pagal terminus laikotarpiui, pavyzdžiui, pradelsta 30 dienų. Data atitinka skirstymą pagal terminus nuo dienos, kuri nurodoma sukuriant skirstymo pagal terminus momentinę kopiją. Ši informacija rodoma pagal terminus suskirstytų likučių puslapyje ir pagal terminus suskirstytų likučių „FactBox“ mokėjimų priežiūros puslapyje.

## <a name="collections-customer-pools"></a> Mokėjimų priežiūros klientų telkiniai
Klientų telkiniai yra užklausos, nustatančios klientų įrašų grupę, kurią galima rodyti ir valdyti mokėjimų priežiūros ar skirstymo pagal terminus procesams. Naudokite klientų telkinius, norėdami filtruoti informaciją sąrašo puslapiuose Pagal terminus suskirstyti balansai, Mokėjimų priežiūros veiklos rūšys ir Rinkinių atvejai. Taip pat klientų telkinius galima naudoti filtruoti klientų sąskaitas, kurios įtraukiamos kuriant skirstymo pagal terminus momentines kopijas.

## <a name="collections-agents"></a>Mokėjimų priežiūros agentai
Pagal numatytuosius parametrus vartotojai gali peržiūrėti visą informaciją apie klientą mokėjimų priežiūros sąrašų puslapiuose. Galite naudoti mokėjimų priežiūros agento įrašus, norėdami nustatyti klientų telkinius, kuriuose galima filtruoti informaciją apie mokėjimų priežiūros sąrašų puslapius ir informaciją mokėjimų priežiūros puslapyje. 

Mokėjimų priežiūros agentas yra asmuo, kuris dirba su klientais siekdamas užtikrinti, kad mokėjimai yra surenkami laiku. Mokėjimų priežiūros agentai yra darbuotojai, paskirti vartotojams vartotojo nustatymų puslapyje.

## <a name="collections-list-pages"></a> Mokėjimų priežiūros puslapiai 
Šie sąrašų puslapiai padės organizuoti mokėjimų priežiūros informaciją.
-   Pagal terminus suskirstyti likučiai – stulpeliai sąrašų puslapyje rodo klientų likučius ir pagal terminus suskirstytas sumas pagal skirstymo pagal terminus laikotarpį. Ši informacija saugoma skirstymo pagal terminus momentinėje kopijoje. Skirstymo per terminus laikotarpiai nustatomi pagal naudojamą skirstymo pagal terminus laikotarpio apibrėžimą. Skirstymo pagal terminus laikotarpio apibrėžimas imamas iš klientų telkinio, jei jis buvo nurodytas telkinio užklausoje. Jei telkinys neturi skirstymo pagal terminus laikotarpio apibrėžimo, pagal nutylėjimą skirstymo pagal terminus laikotarpio apibrėžimas yra nurodytasis naudojamame gautinų sumų parametrų puslapyje. Jei skirstymo pagal terminus laikotarpio apibrėžimas nenurodytas, naudojamas pirmasis skirstymo pagal terminus laikotarpio apibrėžimas skirstymo pagal terminus laikotarpio puslapyje.
-   Mokėjimų priežiūros veikla – stulpeliai sąrašų puslapyje rodo veiklą, kuri yra nustatyta kaip mokėjimų priežiūros veikla. Ši veikla sukurta naudojant mokėjimų priežiūros puslapį. Naudodamiesi veiklomis sekite darbą, kurį atliekate vykdydami mokėjimų priežiūrą.
-   Mokėjimų priežiūros atvejai – stulpeliai sąrašų puslapyje, su informacija atvejams, turintiems atvejo kategoriją, kurios atvejo tipas yra „Mokėjimų priežiūra“.

> [!NOTE]
> Skirstymo pagal terminus momentinę kopiją reikia sukurti prieš peržiūrint šiuos sąrašo puslapius. Informacija rodoma tik tiems klientams, kuriems buvo sukurta skirstymo pagal terminus momentinė kopija. Sąrašo puslapyje rodomus įrašus galima papildomai filtruoti toliau nurodytu būdu.
> <li>Pagal numatytuosius parametrus „Finance and Operations“ vartotojai turi prieigą prie visų klientų, kurie turi skirstymo pagal terminus momentinę kopiją.</li>
> <li>Jeigu yra klientų telkinys, vartotoją reikia nustatyti kaip mokėjimų priežiūros agentą, kad būtų galima naudoti telkinius filtruoti informacijai apie mokėjimų priežiūros sąrašų puslapius. Informacija apsiriboja klientais, kurie yra įrašyti į pasirinktą klientų telkinį.</li>
> <li>Jeigu vartotojas yra nustatytas tik kaip mokėjimų priežiūros agentas, sąrašų puslapyje bus tik telkiniai, kurie yra atrinkti tam mokėjimų priežiūros agentui. Mokėjimų priežiūros agentų puslapyje mokėjimų priežiūros agentui pasirinkus klientų telkinių perjungimą, tam agentui yra prieinami visi telkiniai.</li>


## <a name="collections-page"></a> Mokėjimų priežiūros puslapis 
Naudokite mokėjimų priežiūros puslapį peržiūrėti, valdyti ir imtis veiksmų dėl mokėjimų priežiūros informacijos, veiklos ir klientų atvejų. 

Viršutinėje srityje rodomi pasirinkto kliento atvejai. Vidurinėje srityje rodomos kliento operacijos. Apatinė sritis rodo veiklą klientui. Galite kurti mokėjimų priežiūros atvejus ir sekti mokėjimų priežiūros informaciją vienai ar daugiau operacijų ir veiklų. Informacija viršutiniame ir apatiniame lauke gali būti filtruojama pagal atvejį. 

„FactBoxes“ rodo pagal terminus suskirstytus likučius ir kredito limito informaciją pasirinktam klientui. Ši informacija saugoma skirstymo pagal terminus momentinėje kopijoje. Jei reikia, galite atnaujinti skirstymo pagal terminus momentinę kopiją su dabartine informacija. 

Veiksmų srityje yra mygtukai, kuriais galima parodyti susijusią pasirinkto kliento, atvejo, operacijos arba veiklos informaciją. Taip pat galite atlikti bendrus veiksmus, pavyzdžiui, keisti operacijos mokėjimų priežiūros būseną, siųsti el. laiškus per integraciją su savo elektroninio pašto teikėju, atlyginti klientams, apdoroti NSF mokėjimus ir nurašyti nebeatgautinus likučius.

## <a name="waive-reinstate-or-reverse-interest-and-fees"></a> Atsisakyti, grąžinti arba atšaukti palūkanas ir mokesčius 
Galite atsisakyti, atkurti arba pakeisti baigtas procentų notas, mokesčius ir operacijų palūkanas, kurios yra nurodytos procentų notose. Tai galite padaryti mokėjimų priežiūros skirtuke, veiksmų lange, visų klientų sąrašo puslapyje paspaudę „Palūkanų nota“, „Operacijų palūkanos“, arba „Mokestis“. 

Šie patikslinimai įtakoja tik pažymėtas palūkanų notas, palūkanas ir į jas įtrauktus mokesčius. Naudokite veiksmus iš „Sukurti nurašymo operacijas vienu veiksmu“ skyriaus, norėdami nurašyti visus mokesčius, kuriuos klientas turi sumokėti.

Daugiau informacijos žr. [Kurti palūkanų kodą su intervalu](tasks/create-interest-code-range.md) ir [Apdoroti palūkanas](tasks/process-interest.md). 

## <a name="create-writeoff-transactions"></a>Nurašymo operacijų kūrimas
Beviltiškas skolas galite nurašyti, paspaudę „Nurašyti“ „Mokėjimų priežiūros“ formoje, „Pagal terminus suskirstyti likučiai“, „Klientai“ ir „Atidaryti klientų sąskaitų sąrašą“ puslapiuose. 

Kai nurašote operacijas klientui, visos operacijos klientui yra automatiškai pažymimos atsiskaitymui. Nurašoma suma priklauso nuo pažymėtų operacijų grynosios sumos. Nurašymo operacija kuriama bendrajame žurnale, ją gali sudaryti iki trijų žurnalo eilučių tipų.

-   Pirmojo tipo žurnalo eilutėje yra kliento nurašymo įrašas. Jeigu pažymėtai operacijai yra keli valiutos kodo deriniai, dimensija ir registravimo profilis, kiekvienam deriniui sukuriama atskira žurnalo eilutė.
-   Antrojo tipo žurnalo eilutėje yra didžiosios knygos nurašymo įrašas. Jeigu pažymėtai operacijai yra keli valiutos kodo deriniai, dimensija ir registravimo profilis, kiekvienam deriniui sukuriama atskira žurnalo eilutė.
-   Trečiojo tipo žurnalo eilutėje yra didžiosios knygos nurašymo pardavimo mokesčių nurašymo informacija. Šis žurnalo eilutė sukuriama tik, jei gautinų sumų parametrų puslapyje yra pasirinktas atskiras pardavimo mokesčio keitimas. Jeigu pažymėtai operacijai yra keli mokėtinos sąskaitos pardavimo mokesčio deriniai, dimensija ir pardavimo mokesčio kodas, kiekvienam deriniui sukuriama atskira žurnalo eilutė.

Nurašymo operacija sukuriama operacijos valiuta.

Daugiau informacijos žr. [Kurti kliento nurašymo žurnalą](tasks/create-write-off-journal-customer.md)

<a name="process-not-sufficient-funds-nsf-payments"></a>Apdoroti lėšų trūkumo (NSF) mokėjimus  
--------------------------------------------

NSF mokėjimus galite tvarkyti paspaudę NSF mokėjimą Mokėjimų priežiūros puslapyje. Kai paspausite šį mygtuką, mokėjimas bus atšauktas. Jei klientui taikomas NSF mokestis, sukuriama mokesčio operacija mokėjimo žurnale. Mokesčio suma grindžiama automatinių mokesčių parametrais. NSF mokėjimams automatiškai taikomi mokesčiai, kurie nurodomi pagal mokesčių grupę, pasirenkamą banko sąskaitų puslapyje atitinkamai banko sąskaitai.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]