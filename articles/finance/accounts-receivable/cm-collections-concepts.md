---
title: Pagrindinės mokėjimų priežiūros valdymo koncepcijos
description: Temose apibrėžiamos pagrindinės mokėjimų priežiūros valdymo koncepcijos.
author: JodiChristiansen
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ba64910498732855303e14d3884618597d21510d
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753951"
---
# <a name="collections-management-key-concepts"></a>Pagrindinės mokėjimų priežiūros valdymo koncepcijos

[!include [banner](../includes/banner.md)]

Prieš pradėdami kurti ar dirbti su surinkimu, turite susipažinti su šiomis sąvokomis:

- Klientų skirstymo pagal terminus momentinėje kopijoje yra skirstymo pagal terminus balanso informacija konkrečiu metu.
- Klientų surinkimo telkiniai padės organizuoti darbą.
- Surinkimo agentai gali turėti savo klientų telkinius.
- Sąrašų puslapiuose organizuojami surinkimo klientai, veikla ir atvejai.
- Visa kliento surinkimo informacija yra viename puslapyje, ir iš šio puslapio galite imtis veiksmų.
- Atsisakyti, grąžinti arba atšaukti palūkanas ir mokesčius galima vienu veiksmu.
- Sukurti nurašymo operacijas galima sukurti vienu veiksmu.
- Apdoroti lėšų trūkumo (NSF) mokėjimus galima vienu veiksmu.

Šioje temoje aprašoma kiekviena koncepcija.

## <a name="customer-aging-snapshots"></a>Klientų skirstymo pagal terminus momentinės kopijos

Skirstymo pagal terminus momentinėje kopijoje yra kliento skirstymo pagal terminus balanso informacija konkrečiu metu. Ši informacija rodoma sąrašo puslapyje **Pagal terminus suskirstyti balansai** ir puslapyje **Mokėjimų priežiūra**. Reikia sukurti skirstymo pagal terminus momentinę kopiją, kad būtų galima peržiūrėti informaciją apie surinkimų sąrašo puslapius (**Pagal terminus suskirstyti balansai**, **Mokėjimų priežiūros veiklos** ir **Mokėjimų priežiūros atvejai**).

Kiekvienam klientui, skirstymo pagal terminus momentinė kopija turi skirstymo pagal terminus momentinės kopijos antraštę ir duomenų įrašus, kurie atitinka kiekvieną skirstymo pagal terminus laikotarpį skirstymo pagal terminus laikotarpio apibrėžime.

Skirstymo pagal terminus momentinės kopijos antraštėje yra bendra pradelsta mokėtina suma, kredito limitas, važtaraščio suma, pardavimo užsakymo suma, ginčijamų operacijų skaičius ir bendra ginčijamų operacijų suma kliento sąskaitoje. Visos kliento operacijos yra įtrauktos į šių sumų apskaičiavimą. Bendra pradelsta mokėtina suma, kredito limitas, važtaraščio suma ir pardavimo užsakymo suma yra rodoma „FactBox“ **Kredito informacija** puslapyje **Mokėjimų priežiūra**.

Kiekvienam skirstymo pagal terminus laikotarpiui skirstymo pagal terminus laikotarpio apibrėžime sukuriamas skirstymo pagal terminus momentinės kopijos duomenų įrašas. Kiekviename skirstymo pagal terminus momentinės kopijos duomenų įraše yra skirstymo pagal terminus laikotarpio ID ir bendra suma operacijų, kurių datos patenka į skirstymo pagal terminus laikotarpį. Operacijos priskirtos skirstymo pagal terminus laikotarpiui, pavyzdžiui, pradelsta 30 dienų. Data atitinka **Skirstymas pagal terminus nuo** datos reikšmę, kurią nurodote kurdami skirstymo pagal terminus momentinę kopiją. Ši informacija rodoma puslapyje **Suskirstyti pagal terminus balansai** ir „FactBox“ **Suskirstyti pagal terminus balansai** puslapyje **Mokėjimų priežiūra**.

## <a name="collections-customer-pools"></a> Mokėjimų priežiūros klientų telkiniai

Klientų telkiniai yra užklausos, apibrėžiančios klientų įrašų grupę. Galite naudoti šiuos sugrupuotus įrašus norėdami peržiūrėti įtrauktų kliento sąskaitų informaciją ir vietoje jų tvarkyti mokėjimų priežiūrą arba skirstymo pagal terminus procesus. Galite naudoti klientų telkinius, norėdami filtruoti informaciją mokėjimų priežiūros puslapiuose. Norėdami filtruoti klientų sąskaitas, kurios yra įtraukiamos, kai sukuriamos skirstymo pagal terminus momentinės kopijos, taip pat juos galite naudoti.

## <a name="collections-agents"></a>Mokėjimų priežiūros agentai

Pagal numatytuosius parametrus vartotojai gali peržiūrėti visą informaciją apie klientą mokėjimų priežiūros sąrašų puslapiuose. Mokėjimų priežiūros agentas leidžia jums nustatyti klientų telkinius, kuriuose galima filtruoti informaciją apie mokėjimų priežiūros sąrašų puslapiuose ir puslapyje **Mokėjimų priežiūra**.

Mokėjimų priežiūros agentas dirba su klientais siekdamas užtikrinti, kad mokėjimai yra surenkami laiku. Jie yra darbuotojai, priskirti vartotojams puslapyje **Vartotojo nustatymas**.

## <a name="collections-list-pages"></a> Mokėjimų priežiūros puslapiai 

Šie sąrašų puslapiai padės organizuoti mokėjimų priežiūros informaciją.

- **Pagal terminus suskirstyti balansai** – stulpeliai šiame sąrašų puslapyje rodo klientų likučius ir pagal terminus suskirstytas sumas pagal skirstymo pagal terminus laikotarpį. Ši informacija saugoma skirstymo pagal terminus momentinėje kopijoje. Skirstymo per terminus laikotarpiai nustatomi pagal naudojamą skirstymo pagal terminus laikotarpio apibrėžimą. Skirstymo pagal terminus laikotarpio apibrėžimas imamas iš klientų telkinio, jei kliento telkinys buvo nurodytas telkinio užklausoje. Jei telkinys neturi skirstymo pagal terminus laikotarpio apibrėžimo, pagal nutylėjimą skirstymo pagal terminus laikotarpio apibrėžimas yra nurodytasis puslapyje **Gautinų sumų parametrai**. Jei nenurodyta jokia numatytoji skirstymo pagal terminus laikotarpio apibrėžtis, naudojama pirmoji puslapyje **Skirstymo pagal terminus laikotarpio apibrėžtys** nurodyta skirstymo pagal terminus laikotarpio apibrėžtis.
- **Mokėjimų priežiūros veiklos** – stulpeliai šiame sąrašų puslapyje rodo veiklą, kuri yra nustatyta kaip mokėjimų priežiūros veikla. Šios veiklos sukurtos naudojant puslapį **Mokėjimų priežiūra**. Naudodamiesi veiklomis sekite darbą, kurį atliekate vykdydami mokėjimų priežiūrą.
- **Mokėjimų priežiūros atvejai** – stulpeliai šiame sąrašų puslapyje rodo informaciją, susijusią su atvejais, turinčiais atvejo kategoriją, kurios atvejo tipas yra **Mokėjimų priežiūra**.

### <a name="aging-snapshots"></a>Skirstymo pagal terminus momentinės kopijos

Skirstymo pagal terminus momentinę kopiją reikia sukurti prieš peržiūrint mokėjimų priežiūros sąrašo puslapius. Informacija rodoma tik tiems klientams, kuriems buvo sukurta skirstymo pagal terminus momentinė kopija. Sąrašo puslapyje rodomus įrašus galima papildomai filtruoti toliau nurodytu būdu.

- Pagal nutylėjimą vartotojai turi prieigą prie visų klientų, kurie turi skirstymo pagal terminus momentinę kopiją.
- Jeigu yra klientų telkinys, vartotoją reikia nustatyti kaip mokėjimų priežiūros agentą, kad būtų galima naudoti telkinius filtruoti informacijai apie mokėjimų priežiūros sąrašų puslapius. Informacija apsiriboja klientais, kurie yra įrašyti į pasirinktą klientų telkinį.
- Jeigu vartotojas yra nustatytas tik kaip mokėjimų priežiūros agentas, sąrašų puslapyje bus tik telkiniai, kurie yra atrinkti tam mokėjimų priežiūros agentui. Jei puslapyje **Mokėjimų priežiūros agentas** yra pasirinkta parinktis **Leisti agentui peržiūrėti visus klientų telkinius**, tam agentui yra prieinami visi telkiniai.

## <a name="collections-page"></a> Mokėjimų priežiūros puslapis 

Galite naudoti puslapį **Mokėjimų priežiūra** peržiūrėti, valdyti ir imtis veiksmų dėl mokėjimų priežiūros informacijos, veiklos ir klientų atvejų.

Viršutiniame puslapio skyriuje pateikiami pasirinkto kliento atvejai, viduriniame skyriuje rodomos kliento operacijos, o apatiniame skyriuje rodomos kliento veiklos. Galite kurti mokėjimų priežiūros atvejus ir sekti mokėjimų priežiūros informaciją vienai ar daugiau operacijų ir veiklų. Informacija viršutiniame ir apatiniame skyriuose gali būti filtruojama pagal atvejį.

„FactBoxes“ rodo pagal terminus suskirstytus balansus ir kredito limito informaciją pasirinktam klientui. Ši informacija saugoma skirstymo pagal terminus momentinėje kopijoje. Jei reikia, galite atnaujinti skirstymo pagal terminus momentinę kopiją su dabartine informacija.

Veiksmų srityje yra mygtukai, kuriuos naudojant galima peržiūrėti susijusią pasirinkto kliento, atvejo, operacijos arba veiklos informaciją. Taip pat galite atlikti bendrus veiksmus, pavyzdžiui, keisti operacijos mokėjimų priežiūros būseną, siųsti el. laiškus per integraciją su savo elektroninio pašto teikėju, atlyginti klientams, apdoroti NSF mokėjimus ir nurašyti nebeatgautinus balansus.

## <a name="waiving-reinstating-or-reversing-interest-and-fees"></a>Atsisakyti, grąžinti arba atšaukti palūkanas ir mokesčius

Galite atsisakyti, atkurti arba pakeisti visas delspinigių pažymas, mokesčius ir operacijų palūkanas, kurios yra nurodytos delspinigių pažymose. Skirtuke **Surinkti** sąrašų puslapio veiksmų srityje **Visi klientai** pasirinkite **Delspinigių pažyma**, **Operacijos palūkanos** arba **Mokestis**.

Šie patikslinimai įtakoja tik pažymėtas palūkanų notas, palūkanas ir į jas įtrauktus mokesčius. Norėdami gauti daugiau informacijos apie tai, kaip nurašyti visas kliento skoloms taikomas išlaidas, žr. šios temos skyrių [Nurašymo operacijų kūrimas](#creating-write-off-transactions).

Daugiau informacijos žr. Kurti palūkanų kodą su intervalu ir Apdoroti palūkanas.

## <a name="creating-write-off-transactions"></a>Nurašymo operacijų kūrimas

Galite nurašyti blogas skolas pasirinkdami **Nurašyti** puslapyje **Mokėjimų priežiūra** ir mokėjimų priežiūros sąrašų puslapiuose.

Kai nurašote kliento operacijas, visos šio kliento operacijos yra automatiškai pažymimos atsiskaitymui. Nurašoma suma priklauso nuo pažymėtų operacijų grynosios sumos. Nurašymo operacija kuriama bendrajame žurnale, ją gali sudaryti iki trijų žurnalo eilučių tipų.

- Pirmojo tipo žurnalo eilutėje yra kliento nurašymo įrašas. Jeigu pažymėtai operacijai yra keli valiutos kodų deriniai, dimensijos ir registravimo profiliai, kiekvienam deriniui sukuriama atskira žurnalo eilutė.
- Antrojo tipo žurnalo eilutėje yra didžiosios knygos nurašymo įrašas. Jeigu pažymėtai operacijai yra keli valiutos kodų deriniai, dimensijos ir registravimo profiliai, kiekvienam deriniui sukuriama atskira žurnalo eilutė.
- Trečiojo tipo žurnalo eilutėje yra didžiosios knygos nurašymo pardavimo mokesčių nurašymo informacija. Ši žurnalo eilutė sukuriama tik jei parinktis **Atskirti PVM** pasirinkta puslapyje **Gautinų sumų parametrai**. Jeigu pažymėtai operacijai yra keli mokėtinos sąskaitos pardavimo mokesčio deriniai, dimensijos ir pardavimo mokesčio kodai, kiekvienam deriniui sukuriama atskira žurnalo eilutė. Nurašymo operacija sukuriama operacijos valiuta. Daugiau informacijos žr. Kurti kliento nurašymo žurnalą

## <a name="process-nsf-payments"></a>NSF mokėjimų vykdymas

NSF mokėjimus galite tvarkyti pasirinkę **NSF mokėjimas** puslapyje **Mokėjimų priežiūra**. Kai paspausite šį mygtuką, mokėjimas bus atšauktas. Jei klientui taikomas NSF mokestis, sukuriama mokesčio operacija mokėjimo žurnale. Mokesčio suma grindžiama automatinių mokesčių parametrais. NSF mokėjimams automatiškai taikomi mokesčiai, kurie nurodomi pagal mokesčių grupę, pasirenkamą puslapyje **Banko sąskaitos** atitinkamai banko sąskaitai.

## <a name="additional-resources"></a>Papildomi ištekliai

[Klientų kredito valdymo parametrų nustatymas](./cm-credit-mgmt-setup.md)

[Informacija apie klientų kredito valdymo sąranką](./cm-setup-information.md)

[Kliento kredito tvarkymo informacijos įtraukimas](./cm-add-credit-mgmt-information-customer.md)

[Kliento kredito grupės](./cm-customer-credit-groups.md)

[Kliento kredito limito koregavimai](./cm-credit-limit-adjustments.md)

[Pardavimo užsakymų kredito sulaikymai](./cm-sales-order-credit-holds.md)

[Periodinės kliento kredito valdymo užduotys](./cm-periodic-tasks.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
