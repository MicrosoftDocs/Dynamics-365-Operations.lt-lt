---
title: Einamoji vidutinė savikaina
description: Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje. Tačiau, prieš vykdant atsargų uždarymą, sistema apskaičiuoja einamąją vidutinę savikainą, kuri paprastai naudojama užregistruojant išdavimo operacijas.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d324324312ce9e47b07de8e3de952b8d7c53647
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672184"
---
# <a name="running-average-cost-price"></a>Einamoji vidutinė savikaina

[!include [banner](../includes/banner.md)]

Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje. Tačiau, prieš vykdant atsargų uždarymą, sistema apskaičiuoja einamąją vidutinę savikainą, kuri paprastai naudojama užregistruojant išdavimo operacijas.

Sistema įvertina šią prekės naudojamą savikainą naudodama toliau pateiktą formulę.

Įvertinta kaina = (Faktinė suma + Finansinė suma) ÷ (Faktinis kiekis + Finansinis kiekis)

## <a name="default-item-cost"></a>Numatytoji prekės savikaina

Išleisto produkto numatytąją prekės savikainą galima konfigūruoti vienu iš dviejų būdų puslapyje **Išleisto produkto** informacija:

- Kurkite standartines išlaidas **veiksmų srities** **skirtuko Tvarkyti** išlaidas **dalyje** Nustatymas pasirinkdami Prekės kaina. Jei naudojate šį metodą, turite naudoti standartinę įkainojimo versiją ir išlaidos turi būti aktyvintos.
- Nurodyti išleisto produkto numatytąją prekės savikainą, įvedant **vertę lauke Kaina** **išlaidų** valdymo "FastTab".

Galite ne tik įvesti ar sukurti kainą, **·** **bet** ir pažymėti žymės langelį Naudoti naujausią savikainą, kuris yra informacijos puslapio Tvarkyti išlaidas "**FastTab**". Tokiu atveju, kai registruosite finansinį **atnaujinimą**, sistema automatiškai atnaujins lauką Kaina. Pavyzdžiui, jei registruojate pirkimo užsakymo SF, laukas bus nustatytas kaip pirkimo kaina iš tos SF.

Jei turite savikainą aktyvioje įkainojimo versijoje ir **įvedate** kainą "FastTab" Valdyti išlaidas, prieš jai naudojant kainą, nurodytą "FastTab" Valdyti išlaidas, **sistema** naudos aktyvios įkainojimo versijos kainą.

## <a name="using-the-running-average-cost-price"></a>Einamosios vidutinės savikainos naudojimas

Šioje lentelėje rodoma, kai sistema užregistruoja atsargų operacijas naudodama einamąją vidutinę savikainą, ir kai naudojama savikaina, nustatyta prekės pagrindiniame įraše.

| Sąlyga | Sistema naudoja įvertintą einamąją vidutinę savikainą. | Sistema naudoja numatytąją prekės savikainą |
| --- | --- | --- |
| Ir skaitiklis\*, ir vardiklis\*\* yra teigiami. | Taip | Ne |
| Skaitiklis\*, vardiklis\*\* arba abu yra neigiami. | Ne | Taip |
| Vardiklis\*\* yra 0 (nulis). | Ne | Taip |

\* Skaitiklis = (faktinė suma + finansinė suma)  
\*\* Vardiklis = (faktinis kiekis + finansinis kiekis)

> [!NOTE]
> Jei pasirinktis **Įtraukti fizinę** vertę prekei nėra pasirinkta, sistema naudoja 0 (nulis) ir faktinei sumai, ir faktiniam kiekiui. Informacijos apie šią parinktį rasite [Įtraukti faktinę vertę](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Kainos nepadidinimas

Retais atvejais sistema įkainoja kelis išdavimus neturėdama pakankamai gavimų kainai pagrįsti. Tokiu atveju įvertinta einamoji vidutinė savikaina gali būti nustatoma per didelė. Tačiau yra veiksmų, kuriuos galite atlikti, kad išvengtumėte kainos padidinimo, arba sumažintumėte jo poveikį jam įvykus.

**Scenarijus:** Su preke, kurią pasirinkote pasirinktimi Įtraukti fizinę **vertę, įvyksta** šios operacijos:

1. Finansiškai gaunate kiekį 100, po 100,00 USD.
2. Finansiškai išduodate kiekį 200.
3. Faktiškai gaunate kiekį 101, po 202,00 USD.

Tikrindami įvertintą einamąją vidutinę prekės savikainą, tikitės, kad ji bus 1,51 USD. Geriau surandate įvertintą einamą USD 102.00 pagal šią formulę:

Įvertinta kaina = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Šis kainos didinimas vyksta todėl, kad kai 2 žingsnyje išduodama 200 prekių, sistema turi nustatyti kainą 100 prekių prieš ji turi turėti bet kokius atitinkamus gavimus. Dėl tokios situacijos atsargos tampa neigiamos. Tada sistema įvertina vieneto kainą USD 1.00, kurios tikitės. Tačiau, gavus atitinkamus 100 gavimų, kiekvieno jų kaina yra 2,00 USD.

> [!NOTE]
> Nors išdavimai sukuria neigiamas atsargas, skaičiuojant išdavimo kainą atsargos yra teigiamos. Todėl naudojama einamoji vidutinė savikaina, o ne pagrindiniame prekės įraše esanti kaina. Šiuo momentu sistema turi atsargų vertės 100,00 USD korespondavimą. Nors šis korespondavimas buvo sukurtas 100 vienetų, kur kiekvieno vieneto USD 1.00 buvo korespondentinė sąskaita, atsargose turite tik vieną vienetą. Todėl šiai vienai prekei priskiriamas 100,00 USD poslinkis. Viso to rezultatas – nustatyta per didelė įvertinta savikaina.
>
> Palyginimui, pastebkite, kad scenarijuje 2 ir 3 žingsniai atšaukiami, 200 prekių išduodamos USD 1.51, o vienos dalies vieneto kaina lieka USD 1.51. Kadangi šis kainos padidinimo scenarijus gali įvykti, kai įtrauktas neigiamas atsargų kiekis, jo sunku išvengti tolesniais atvejais.
>
> - Turite įvertinti išdavimo kainas pagal turimas atsargas ir kiekį.
> - Turite pakoreguoti turimų atsargų vertę ir kiekį išdavimuose ir gavimuose.
> - Jūsų verslo modelis leidžia išsiųsti arba nustatyti kainas didesniam prekių kiekiui nei turite.
> - Turite priimti visų jums pateiktų kvitų vertes ir kiekius.

Tačiau, jeigu jūsų verslo modelis leidžia taikyti tolesnę praktiką, ji gali padėti išvengti neigiamų kiekių, dėl kurių tampa įmanomas kainos padidinimo scenarijus.

- Jei prekei pasirenkate **pasirinktį Įtraukti** fizinę vertę, išvalykite **faktinių neigiamų** **atsargų žymės langelį prekių modelių grupių** puslapyje.
- Jei prekės parinkties **Įtraukti faktinę vertę** **nepasirenkate**, puslapyje **Prekių modelių grupės** atžymėkite parinktį **Finansinės neigiamos atsargos**.

Taip pat turėkite omenyje, kad didžiausias jūsų faktinio atsargų kiekio poslinkis ribojamas pagal faktinių operacijų skaičių ir skirtumą tarp faktinių ir finansinių kainų. Jei visos faktinės operacijos finansiškai atnaujinamos, faktinė vertė negali pakilti labai aukštai. Galiausiai atminkite, kad padidinimo poveikis pastebimai sumažėja sukauptą poslinkį paskirsčius keliems, o ne vienam, turimų atsargų vienetams.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Išvengti išduodamos nulinės savikainos

Kai **pasirinktis** **Įtraukti** fizinę vertę nėra pasirinkta prekių modelių grupės puslapyje, atsargų išdavimas gali turėti nulinę savikainą, jei atsargose nėra finansiškai atnaujintų gavimų. Norėdami išvengti šio scenarijaus, atsižvelkite į šias pasirinktis:

- Prekių modelių **grupės puslapyje pasirinkite** pasirinktį **Įtraukti fizinę** vertę. Ši pasirinktis apsaugo nuo nulinės išdavimo savikainos, jei gavimas yra faktiškai atnaujintas. Jei neleidžiate neigiamų faktinių atsargų, pagal faktiškai atnaujintas operacijas išduodamų prekių vidurkis bus apskaičiuojamas.
- Sukurkite numatytąją prekės savikainą suaktyvindami įkainojimo versiją, kuri turi standartines išlaidas, arba įveskite kainą puslapyje Tvarkyti išlaidas "FastTab **",** **kuris yra Paleistas** produkto informacijos puslapis. Ši pasirinktis geriausia, **·** **kai** pasirinktis Įtraukti fizinę vertę nėra pasirinkta prekių modelių grupės puslapyje, nes sistema visada turės naudoti atsarginę kainą.
- Pasirinkite parinktį **Naudoti naujausią savikainą**, puslapio **Išleisto** produkto informacija "**FastTab**" Tvarkyti išlaidas. Kiekvieną kartą, kai **finansiškai** atnaujinate gavimą, ši pasirinktis atnaujins lauką Kaina. Jei pasirenkate šią pasirinktį, bet neįvesite numatytosios kainos ar nesuaktyvinsite standartinės įkainojimo versijos išlaidų, išdavimo išlaidos vis tiek gali būti nulinės.

Jei yra išdavimo operacijų, kurių kaina lygi nuliui, *atsargų* uždarymo ir koregavimo procesas pataisys savikainą, sukurdama koregavimą po gavimų finansiškai atnaujintų. Atkreipkite dėmesį, kad finansinis laikotarpis, kai šis atnaujinimas vyksta, gali skirtis nuo finansinio laikotarpio, kai prekės buvo faktiškai gautos arba išduotos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
