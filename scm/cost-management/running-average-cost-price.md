---
title: "Einamoji vidutinė savikaina"
description: "Atsargos uždaryti procesą nusėda išdavimo operacijas į gavimo operacijos, remiantis atsargų vertinimo metodas, kuris pažymėtas prekės atsargų modelio grupė. Tačiau, kol atsargos yra paleisti, sistema apskaičiuoja veikia vidutinę savikainą, kuri paprastai naudojama registruojant išdavimo operacijas."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Einamoji vidutinė savikaina

Atsargos uždaryti procesą nusėda išdavimo operacijas į gavimo operacijos, remiantis atsargų vertinimo metodas, kuris pažymėtas prekės atsargų modelio grupė. Tačiau, kol atsargos yra paleisti, sistema apskaičiuoja veikia vidutinę savikainą, kuri paprastai naudojama registruojant išdavimo operacijas.

Sistema įvertina tai veikia vidutinė savikaina prekės pagal šią formulę: apskaičiuota kaina = (fizinio dydžio ir kiekio) ÷ (faktinio kiekio ir finansų kiekio)

## <a name="using-the-running-average-cost-price"></a>Einamosios vidutinės savikainos naudojimas
Toliau esančioje lentelėje rodo, kada sistema užregistruoja atsargų operacijas naudojant veikia vidutinė savikaina, ir kai ji naudoja savikainą, kuri apibrėžiama prekės pagrindinis įrašas vietoj.

| Sąlyga                                               | Sistema naudoja numatomą veikia vidutinė savikaina | Sistema naudoja savikainą, kuri apibrėžiama prekės Master |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Abu skaitiklis\* ir vardikliu\*\* yra teigiami.  | Taip                                                      | Nr.                                                                |
| Skaitiklis\*, vardiklis\*\*, arba abu yra neigiamas. | Nr.                                                       | Taip                                                               |
| Vardiklis\*\* 0 (nulis).                        | Nr.                                                       | Taip                                                               |

\*Skaitiklis = (fizinės suma ir suma) \*\*vardiklis = (faktinio kiekio ir finansų kiekio) **Pastaba:** jei su **įtraukti faktinę vertę** parinktis nėra pasirinkta prekės, sistema naudoja 0 (nulis) fizinis dydis ir faktinis kiekis. Informacijos apie šią parinktį rasite [Įtraukti faktinę vertę](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Kainos nepadidinimas
Retais atvejais sistemos kainos keletą klausimų iki jo nepakanka gavimų grįsti kaina. Tokiu atveju įvertinta einamoji vidutinė savikaina gali būti nustatoma per didelė. Tačiau yra veiksmų, kuriuos galite atlikti, kad išvengtumėte kainos padidinimo, arba sumažintumėte jo poveikį jam įvykus. **Scenarijus** Su preke, kuriai parinkote parinktį **Įtraukti faktinę vertę**, atliekamos tolesnės operacijos.

1.  Finansiškai gaunate kiekį 100, po 100,00 USD.
2.  Finansiškai išduodate kiekį 200.
3.  Faktiškai gaunate kiekį 101, po 202,00 USD.

Tikrindami įvertintą einamąją vidutinę prekės savikainą, tikitės, kad ji bus 1,51 USD. Vietoj to, galite rasti maždaug veikia vidutiniškai, USD 102.00, pagal šią formulę: apskaičiuota kaina = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 šį kainodaros amplifikacijos kyla todėl, kad, išduodant 200 vienetų finansiškai 2 veiksme, sistema turi kaina 100 prekių, prieš ją turi visos atitinkamos pajamos. Dėl tokios situacijos atsargos tampa neigiamos. Sistema tada sąmatos vieneto kaina buvo USD 1.00, kaip mes gali tikėtis. Tačiau, gavus atitinkamus 100 gavimų, kiekvieno jų kaina yra 2,00 USD. **Pastaba.** Nors dėl išdavimų sukuriamas neigiamas atsargų kiekis, išdavimo kainos apskaičiavimo metu atsargų kiekis yra teigiamas. Todėl naudojama einamoji vidutinė savikaina, o ne pagrindiniame prekės įraše esanti kaina. Šiuo metu sistema turi atsargų vertės poslinkis, USD 100.00. Nors tas poslinkis susidarė dėl 100 prekių, kai vieno vieneto poslinkis buvo 1,00 USD, atsargose dabar turime tik vieną prekę. Todėl šiai vienai prekei priskiriamas 100,00 USD poslinkis. Viso to rezultatas – nustatyta per didelė įvertinta savikaina. **Pastaba:** Palyginimui, atkreipkite dėmesį, kad, jei scenarijuje 2 ir 3 veiksmai sukeičiami, 200 prekių išduodamos 1,51 USD kaina, o vienos prekės vieneto kaina lieka 1,51 USD. Kadangi šis kainos padidinimo scenarijus gali įvykti, kai įtrauktas neigiamas atsargų kiekis, jo sunku išvengti tolesniais atvejais.

-   Turite įvertinti išdavimo kainas pagal turimas atsargas ir kiekį.
-   Turite pakoreguoti turimų atsargų vertę ir kiekį išdavimuose ir gavimuose.
-   Jūsų verslo modelis leidžia išsiųsti arba nustatyti kainas didesniam prekių kiekiui nei turite.
-   Turite priimti visų jums pateiktų kvitų vertes ir kiekius.

Tačiau, jeigu jūsų verslo modelis leidžia taikyti tolesnę praktiką, ji gali padėti išvengti neigiamų kiekių, dėl kurių tampa įmanomas kainos padidinimo scenarijus.

-   Jei pasirenkate prekės parinktį **Įtraukti faktinę vertę**, puslapyje **Prekių modelių grupės** atžymėkite žymės langelį **Faktinės neigiamos atsargos**.
-   Jei prekės parinkties **Įtraukti faktinę vertę** *nepasirenkate*, puslapyje **Prekių modelių grupės** atžymėkite parinktį **Finansinės neigiamos atsargos**.

Taip pat turėkite omenyje, kad didžiausias jūsų faktinio atsargų kiekio poslinkis ribojamas pagal faktinių operacijų skaičių ir skirtumą tarp faktinių ir finansinių kainų. Jei visos faktinės operacijos finansiškai atnaujinamos, faktinė vertė negali pakilti labai aukštai. Galiausiai atminkite, kad padidinimo poveikis pastebimai sumažėja sukauptą poslinkį paskirsčius keliems, o ne vienam, turimų atsargų vienetams.


