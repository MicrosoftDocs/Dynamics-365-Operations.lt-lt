---
title: Einamoji vidutinė savikaina
description: Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje. Tačiau, prieš vykdant atsargų uždarymą, sistema apskaičiuoja einamąją vidutinę savikainą, kuri paprastai naudojama užregistruojant išdavimo operacijas.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 871b3ffce45848f95d132eff3fd327295bc5084c
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092194"
---
# <a name="running-average-cost-price"></a>Einamoji vidutinė savikaina

[!include [banner](../includes/banner.md)]

Atsargų uždarymo procesas sudengia išdavimo operacijas su gavimo operacijomis, remiantis atsargų vertinimo metodu, pasirinktu prekės modelių grupėje. Tačiau, prieš vykdant atsargų uždarymą, sistema apskaičiuoja einamąją vidutinę savikainą, kuri paprastai naudojama užregistruojant išdavimo operacijas.

Sistema įvertina šią prekės naudojamą savikainą naudodama toliau pateiktą formulę.

Įvertinta kaina = (Faktinė suma + Finansinė suma) ÷ (Faktinis kiekis + Finansinis kiekis)

## <a name="default-item-cost"></a>Numatytoji prekės kaina

Išleisto produkto numatytąją prekės kainą galima konfigūruoti vienu iš dviejų būdų **Išleista produkto informacija** puslapis:

- Sukurkite standartinę kainą pasirinkdami **Prekės kaina** viduje konors **Nustatyti** grupė ant **Valdykite išlaidas** Veiksmų srities skirtuką. Jei naudojate šį metodą, turite naudoti standartinę išlaidų apskaičiavimo versiją, o kaina turi būti suaktyvinta.
- Apibrėžkite numatytąją išleisto produkto prekės savikainą, įvesdami vertę **Kaina** lauke ant **Valdykite išlaidas** FastTab.

Galite ne tik įvesti arba sukurti kainą, bet ir pasirinkti **Naudokite naujausią savikainą** žymimąjį laukelį ant **Valdykite išlaidas** Greitasis skirtukas **Išleista produkto informacija** puslapį. Tokiu atveju sistema automatiškai atnaujins **Kaina** kai skelbiate finansinį atnaujinimą. Pavyzdžiui, jei registruojate pirkimo užsakymo sąskaitą faktūrą, lauke bus nustatyta pirkimo kaina iš tos sąskaitos faktūros.

Jei turite savikainą aktyvioje apmokestinimo versijoje ir įvedate kainą **Valdykite išlaidas** „FastTab“, sistema naudos kainą iš aktyvios sąnaudų apskaičiavimo versijos prieš pradėdama naudoti kainą, apibrėžtą **Valdykite išlaidas** FastTab.

## <a name="using-the-running-average-cost-price"></a>Einamosios vidutinės savikainos naudojimas

Šioje lentelėje rodoma, kai sistema užregistruoja atsargų operacijas naudodama einamąją vidutinę savikainą, ir kai naudojama savikaina, nustatyta prekės pagrindiniame įraše.

| Sąlyga | Sistema naudoja įvertintą einamąją vidutinę savikainą. | Sistema naudoja numatytąją prekės savikainą |
| --- | --- | --- |
| Ir skaitiklis\*, ir vardiklis\*\* yra teigiami. | Taip | Ne |
| Skaitiklis\*, vardiklis\*\* arba abu yra neigiami. | Ne | Taip |
| Vardiklis\*\* yra 0 (nulis). | Ne | Taip |

\* Skaitiklis = (fizinė suma + finansinė suma)  
\*\* Vardiklis = (fizinis kiekis + finansinis kiekis)

> [!NOTE]
> Jei **Įtraukite fizinę vertę** parinktis prekei nepasirinkta, sistema naudoja 0 (nulis) ir fiziniam kiekiui, ir fiziniam kiekiui. Informacijos apie šią parinktį rasite [Įtraukti faktinę vertę](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Kainos nepadidinimas

Retais atvejais sistema įkainoja kelis išdavimus neturėdama pakankamai gavimų kainai pagrįsti. Tokiu atveju įvertinta einamoji vidutinė savikaina gali būti nustatoma per didelė. Tačiau yra veiksmų, kuriuos galite atlikti, kad išvengtumėte kainos padidinimo, arba sumažintumėte jo poveikį jam įvykus.

**Scenarijus:** Šios operacijos atliekamos su preke, kurią pasirinkote **Įtraukite fizinę vertę** variantas:

1. Finansiškai gaunate kiekį 100, po 100,00 USD.
2. Finansiškai išduodate kiekį 200.
3. Faktiškai gaunate kiekį 101, po 202,00 USD.

Tikrindami įvertintą einamąją vidutinę prekės savikainą, tikitės, kad ji bus 1,51 USD. Vietoje to rasite apskaičiuotą einamąjį USD 102.00 vidurkį, pagrįstą šia formule:

Numatoma kaina =\[ 202 + (-100)\] ÷\[ 101 + (-100)\] = 102 ÷ 1 = 102

Šis kainų padidėjimas atsiranda todėl, kad kai 2 veiksme finansiškai išduodama 200 prekių, sistema turi įkainoti 100 prekių prieš gaudama atitinkamus kvitus. Dėl tokios situacijos atsargos tampa neigiamos. Tada sistema apskaičiuoja USD 1.00 vieneto kainą, kaip galite tikėtis. Tačiau, gavus atitinkamus 100 gavimų, kiekvieno jų kaina yra 2,00 USD.

> [!NOTE]
> Nors emisijos sukuria neigiamas atsargas, atsargos yra teigiamos, kai apskaičiuojama emisijos kaina. Todėl naudojama einamoji vidutinė savikaina, o ne pagrindiniame prekės įraše esanti kaina. Šiuo momentu sistema turi atsargų vertės 100,00 USD korespondavimą. Nors šis poslinkis buvo sudarytas daugiau nei 100 vienetų, kurių kiekvienas buvo po USD 1.00 vienetu, dabar atsargose turite tik vieną vienetą. Todėl šiai vienai prekei priskiriamas 100,00 USD poslinkis. Viso to rezultatas – nustatyta per didelė įvertinta savikaina.
>
> Palyginimui, atkreipkite dėmesį, kad jei scenarijuje 2 ir 3 veiksmai bus pakeisti, 200 prekių bus išleista už USD 1.51 vieneto kainą, o vienas gabalas liks su USD 1.51 vieneto kaina. Kadangi šis kainos padidinimo scenarijus gali įvykti, kai įtrauktas neigiamas atsargų kiekis, jo sunku išvengti tolesniais atvejais.
>
> - Turite įvertinti išdavimo kainas pagal turimas atsargas ir kiekį.
> - Turite pakoreguoti turimų atsargų vertę ir kiekį išdavimuose ir gavimuose.
> - Jūsų verslo modelis leidžia išsiųsti arba nustatyti kainas didesniam prekių kiekiui nei turite.
> - Turite priimti visų jums pateiktų kvitų vertes ir kiekius.

Tačiau, jeigu jūsų verslo modelis leidžia taikyti tolesnę praktiką, ji gali padėti išvengti neigiamų kiekių, dėl kurių tampa įmanomas kainos padidinimo scenarijus.

- Jei pasirinksite **Įtraukite fizinę vertę** elemento parinktį, išvalykite **Fizinis neigiamas inventorius** žymimąjį laukelį ant **Prekių modelių grupės** puslapį.
- Jei prekės parinkties **Įtraukti faktinę vertę** **nepasirenkate**, puslapyje **Prekių modelių grupės** atžymėkite parinktį **Finansinės neigiamos atsargos**.

Taip pat turėkite omenyje, kad didžiausias jūsų faktinio atsargų kiekio poslinkis ribojamas pagal faktinių operacijų skaičių ir skirtumą tarp faktinių ir finansinių kainų. Jei visos faktinės operacijos finansiškai atnaujinamos, faktinė vertė negali pakilti labai aukštai. Galiausiai atminkite, kad padidinimo poveikis pastebimai sumažėja sukauptą poslinkį paskirsčius keliems, o ne vienam, turimų atsargų vienetams.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Išspręsdami problemas venkite nulinės savikainos

Kai **Įtraukite fizinę vertę** parinktis nepasirinkta **Prekių modelių grupė** puslapyje, leidimas iš atsargų gali turėti nulinę savikainą, jei atsargose nėra finansiškai atnaujintų kvitų. Kad išvengtumėte šio scenarijaus, apsvarstykite šias parinktis:

- Pasirinkite **Įtraukite fizinę vertę** parinktis ant **Prekių modelių grupė** puslapį. Ši parinktis neleis nulinės savikainos, jei kvitas bus fiziškai atnaujintas. Jei neleidžiate neigiamų fizinių atsargų, problemos apskaičiuos einamąjį vidurkį iš fiziškai atnaujintų operacijų.
- Sukurkite numatytąją prekės savikainą suaktyvinę įkainių versiją su standartine kaina arba įveskite kainą **Valdykite išlaidas** Greitasis skirtukas **Išleista produkto informacija** puslapį. Ši parinktis geriausia, kai **Įtraukite fizinę vertę** parinktis nepasirinkta **Prekių modelių grupė** puslapį, nes sistema visada turės atsarginę kainą.
- Pasirinkite **Naudokite naujausią savikainą** parinktis ant **Valdykite išlaidas** Greitasis skirtukas **Išleista produkto informacija** puslapį. Ši parinktis išsaugos **Kaina** laukas atnaujinamas kiekvieną kartą, kai finansiškai atnaujinate kvitą. Jei pasirinksite šią parinktį, bet neįvesite numatytosios kainos arba nesuaktyvinsite mokesčio standartinėje apmokestinimo versijoje, vis tiek galite turėti nulinę problemą.

Jei turite sandorių, kurių kaina yra nulinė, *Atsargų uždarymas ir derinimas* procesas ištaisys savikainą sukurdamas koregavimą po to, kai bus finansiškai atnaujintos kvitai. Atminkite, kad finansinis laikotarpis, kai įvyksta šis atnaujinimas, gali skirtis nuo finansinio laikotarpio, kai prekės buvo fiziškai gautos arba išleistos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
