---
title: Einamoji vidutinė savikaina
description: Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje. Tačiau, prieš vykdant atsargų uždarymą, sistema apskaičiuoja einamąją vidutinę savikainą, kuri paprastai naudojama užregistruojant išdavimo operacijas.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75dfd2f23034bbd222e020b532027e60ef215241
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830272"
---
# <a name="running-average-cost-price"></a>Einamoji vidutinė savikaina

[!include [banner](../includes/banner.md)]

Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje. Tačiau, prieš vykdant atsargų uždarymą, sistema apskaičiuoja einamąją vidutinę savikainą, kuri paprastai naudojama užregistruojant išdavimo operacijas.

Sistema įvertina šią prekės naudojamą savikainą naudodama toliau pateiktą formulę. 

Įvertinta kaina = (Faktinė suma + Finansinė suma) ÷ (Faktinis kiekis + Finansinis kiekis)

## <a name="using-the-running-average-cost-price"></a>Einamosios vidutinės savikainos naudojimas
Šioje lentelėje rodoma, kai sistema užregistruoja atsargų operacijas naudodama einamąją vidutinę savikainą, ir kai naudojama savikaina, nustatyta prekės pagrindiniame įraše.

| Sąlyga                                               | Sistema naudoja įvertintą einamąją vidutinę savikainą. | Sistema naudoja savikainą, nustatytą prekės pagrindiniame įraše. |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Ir skaitiklis\*, ir vardiklis\*\* yra teigiami.  | Taip                                                      | Nr.                                                                |
| Skaitiklis\*, vardiklis\*\* arba abu yra neigiami. | Nr.                                                       | Taip                                                               |
| Vardiklis\*\* yra 0 (nulis).                        | Nr.                                                       | Taip                                                               |

\* Skaitiklis = (Faktinė suma + Finansinė suma) \*\* Vardiklis = (Faktinis kiekis + Finansinis kiekis) 

**Pastaba.** Jei prekės parinktis **Įtraukti faktinę vertę** nepasirinkta, sistema taiko 0 (nulis) ir faktinei sumai, ir faktiniam kiekiui. Informacijos apie šią parinktį rasite [Įtraukti faktinę vertę](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Kainos nepadidinimas
Retais atvejais sistema įkainoja kelis išdavimus neturėdama pakankamai gavimų kainai pagrįsti. Tokiu atveju įvertinta einamoji vidutinė savikaina gali būti nustatoma per didelė. Tačiau yra veiksmų, kuriuos galite atlikti, kad išvengtumėte kainos padidinimo, arba sumažintumėte jo poveikį jam įvykus. **Scenarijus** Su preke, kuriai parinkote parinktį **Įtraukti faktinę vertę**, atliekamos tolesnės operacijos.

1.  Finansiškai gaunate kiekį 100, po 100,00 USD.
2.  Finansiškai išduodate kiekį 200.
3.  Faktiškai gaunate kiekį 101, po 202,00 USD.

Tikrindami įvertintą einamąją vidutinę prekės savikainą, tikitės, kad ji bus 1,51 USD. Tačiau matote, kad įvertinta einamoji vidutinė savikaina yra 102,00 USD, apskaičiuota pagal šią formulę: įvertinta kaina = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102. Kaina taip padidėja dėl to, kad, kai 2 veiksmu finansiškai išduodama 200 prekių, 100 iš jų sistema turi įkainoti dar neturėdama atitinkamų gavimų. Dėl tokios situacijos atsargos tampa neigiamos. Kaip galima tikėtis, tada sistema vieneto kainą įvertina 1,00 USD. Tačiau, gavus atitinkamus 100 gavimų, kiekvieno jų kaina yra 2,00 USD. 

**Pastaba.** Nors dėl išdavimų sukuriamas neigiamas atsargų kiekis, išdavimo kainos apskaičiavimo metu atsargų kiekis yra teigiamas. Todėl naudojama einamoji vidutinė savikaina, o ne pagrindiniame prekės įraše esanti kaina. Šiuo momentu sistema turi atsargų vertės 100,00 USD korespondavimą. Nors tas poslinkis susidarė dėl 100 prekių, kai vieno vieneto poslinkis buvo 1,00 USD, atsargose dabar turime tik vieną prekę. Todėl šiai vienai prekei priskiriamas 100,00 USD poslinkis. Viso to rezultatas – nustatyta per didelė įvertinta savikaina. 

**Pastaba:** Palyginimui, atkreipkite dėmesį, kad, jei scenarijuje 2 ir 3 veiksmai sukeičiami, 200 prekių išduodamos 1,51 USD kaina, o vienos prekės vieneto kaina lieka 1,51 USD. Kadangi šis kainos padidinimo scenarijus gali įvykti, kai įtrauktas neigiamas atsargų kiekis, jo sunku išvengti tolesniais atvejais.

-   Turite įvertinti išdavimo kainas pagal turimas atsargas ir kiekį.
-   Turite pakoreguoti turimų atsargų vertę ir kiekį išdavimuose ir gavimuose.
-   Jūsų verslo modelis leidžia išsiųsti arba nustatyti kainas didesniam prekių kiekiui nei turite.
-   Turite priimti visų jums pateiktų kvitų vertes ir kiekius.

Tačiau, jeigu jūsų verslo modelis leidžia taikyti tolesnę praktiką, ji gali padėti išvengti neigiamų kiekių, dėl kurių tampa įmanomas kainos padidinimo scenarijus.

-   Jei pasirenkate prekės parinktį **Įtraukti faktinę vertę**, puslapyje **Prekių modelių grupės** atžymėkite žymės langelį **Faktinės neigiamos atsargos**.
-   Jei prekės parinkties **Įtraukti faktinę vertę** *nepasirenkate*, puslapyje **Prekių modelių grupės** atžymėkite parinktį **Finansinės neigiamos atsargos**.

Taip pat turėkite omenyje, kad didžiausias jūsų faktinio atsargų kiekio poslinkis ribojamas pagal faktinių operacijų skaičių ir skirtumą tarp faktinių ir finansinių kainų. Jei visos faktinės operacijos finansiškai atnaujinamos, faktinė vertė negali pakilti labai aukštai. Galiausiai atminkite, kad padidinimo poveikis pastebimai sumažėja sukauptą poslinkį paskirsčius keliems, o ne vienam, turimų atsargų vienetams.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]