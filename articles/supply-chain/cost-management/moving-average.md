---
title: Slankusis vidurkis
description: Slankusis vidurkis yra nuolatinis įkainojimo metodas, paremtas vidurkio principu, kai kintant pirkimo išlaidoms išduodamų atsargų savikainos nekinta. Skirtumas kapitalizuojamas ir pagrindžiamas proporcingu skaičiavimu. Likusi suma įtraukiama į išlaidų sąskaitą.
author: AndersGirke
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0472a0d2ac9b552cd16e4d6bf516a876ea4a0e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433434"
---
# <a name="moving-average"></a>Slankusis vidurkis

[!include [banner](../includes/banner.md)]

Slankusis vidurkis yra nuolatinis įkainojimo metodas, paremtas vidurkio principu, kai kintant pirkimo išlaidoms išduodamų atsargų savikainos nekinta. Skirtumas kapitalizuojamas ir pagrindžiamas proporcingu skaičiavimu. Likusi suma įtraukiama į išlaidų sąskaitą.

Taikant slankųjį vidurkį, atsargų sudengimai ir atsargų žymėjimas nepalaikomi. Atsargų uždarymas neturi įtakos produktams, kuriems slankusis vidurkis taikomas kaip atsargų modelio grupei, ir jam esant nesukuriami sudengimai tarp operacijų.

Toliau nurodytos sąlygos, būtinos slankiojo vidurkio savikainą taikant kaip įkainojimo metodą.

1. Puslapyje **Prekių modelių grupės** nustatykite prekių modelių grupę, kurios lauke **Atsargų modelis** pasirinkta **Slankusis vidurkis**.

    > [!NOTE]
    > Pagal numatytuosius nustatymus, pasirinkus **Slankusis vidurkis**, laukai **Registruoti faktines atsargas** ir **Registruoti finansines atsargas** taip pat pažymėti.

1. Puslapyje **Registravimas** priskirkite sąskaitas **Slankiojo vidurkio kainų skirtumas**. Naudokite sąskaitą **Slankiojo vidurkio kainų skirtumas**, kai savikaina turi būti proporcingai nurodoma kaip išlaidos. Taip atsitinka toliau pateiktuose dviejuose scenarijuose.
    - Yra išlaidų skirtumas tarp pirkimo kvito ir pirkimo SF, nes yra skirtumas tarp pradinio atsargų kiekio ir dabartinio turimo kiekio.
    - Operacijos atkuria atsargų lygį iš neigiamo į nulį ir yra skirtumas tarp operacijų išlaidų ir dabartinio slankiojo vidurkio savikainos.

1. Puslapyje **Registravimas** priskirkite sąskaitas skirtuko **Atsargos** sąskaitai **Slankiojo vidurkio išlaidų pakartotinis įvertinimas**. Sąskaitą **Slankiojo vidurkio išlaidų pakartotinis įvertinimas** naudokite, kai norite pakoreguoti produkto slankiojo vidurkio savikainą pagal naują vieneto kainą.

1. Puslapyje **Patvirtinti produktai** produktui priskirkite slankiojo vidurkio prekių modelių grupę.

    > [!NOTE]
    > Atsargų uždarymo procesas uždaro tik ataskaitinį laikotarpį. Tai neturi įtakos produktams, kuriems kaip prekių modelių grupė priskirtas slankusis vidurkis.

## <a name="convert-to-the-moving-average-costing-method"></a>Konvertuoti į slankiojo vidurkio savikainos metodą

Produktus galima konvertuoti, kad būtų galima naudoti slankiojo vidurkio atsargų vertinimo metodą. Toks konvertavimas dažniausiai atliekamas metų pabaigoje, uždarius paskutinį einamųjų metų mėnesį. Tai atliekama naudojant dabartinį produkto įkainojimo modelį. Galite keisti savo atsargų įkainojimo metodą iš įkainojimo metodo, pagrįsto vidutine savikaina arba standartine savikaina į metodą, pagrįstą slankiuoju vidurkiu.

Jei keičiate įkainojimo metodą iš standartinės savikainos metodo į slankiojo vidurkio metodą, turite atlikti šias užduotis:

1. Pakoreguokite, kad atsargų kiekis ir vertės būtų 0 (nulis).
1. Kai atsargų vertė ir kiekis bus 0 (nulis), pakeiskite atsargų modelio grupės metodą į slankiojo vidurkio.
1. Pakoreguokite, kad kiekis ir vertė būtų grąžinti į atsargas.

Negalima keisti atsargų įkainojimo metodas iš slankiojo vidurkio metodo į „pirmasis į, pirmasis iš“ (FIFO) metodą, „paskutinis į, pirmasis iš“ (LIFO) metodą arba svertinio vidurkio metodą.

> [!NOTE]
> Konvertavimas iš standartinės savikainos metodo į slankiojo svertinio vidurkio metodą yra neautomatinis procesas.

Toliau pateikti pavyzdžiai rodo slankiojo vidurkio įkainojimo metodo poveikį. Yra keturios konfigūracijos:

- Pirkimo užsakymo ir proporcingai išlaidomis laikomos savikainos skirtumas
- Produkto ir atsargų slankiojo vidurkio koregavimas
- Slankusis vidurkis ir produkcija
- Slankusis vidurkis ir operacija atgaline data

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Pirkimo užsakymo ir proporcingai išlaidomis laikomos savikainos skirtumas

Pasirinkus slankiojo vidurkio metodą, produkto savikaina priklauso nuo pirkimo kvito. Kai užregistruojama pirkimo SF, jei tarp pirkimo kvito ir pirkimo SF yra savikainos skirtumas, jis nustatomas proporcingai pakoregavus pagal sandėlyje esančių produktų kiekį, o bet kokia likusi suma įtraukiama į išlaidų sąskaitą.

Šiame pavyzdyje pirkimo užsakymas sukurtas ir gaunamas esant vienai savikainai, o pirkimo SF užregistruojama esant kitai savikainai.

1. Sukurkite pirkimo užsakymą, kurio kiekis 2, o vieneto kaina 10,00.
1. Sukurkite produkto pirkimo kvitą.
1. Sukurkite pardavimo užsakymą, kurio kiekis 1, o vieneto kaina 10,00.
1. Sukurkite pirkimo sąskaitą faktūrą, kurios kiekis 2, o vieneto kaina 12,00.

Vieneto kainos skirtumas, 2,00, registruojamas sąskaitoje Slankiojo vidurkio kainų skirtumas, kai užregistruojama pirkimo SF. Priežastis ta, kad buvo įsigyti du produktai už 20,00. Vienas iš produktų buvo parduotas už 10,00. Pateikta pirkimo sąskaita faktūra, kurioje nurodomas kiekis 2, o vieneto kaina – 12,00. Produkto vieneto kaina negali būti 14,00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Produkto ir atsargų slankiojo vidurkio koregavimas

Jei reikia koreguoti produkto slankiojo vidurkio kainą, atsargų koregavimus leidžiama atlikti pagal šiandienos datą. Negalima atgaline data koreguoti atsargų siekiant ištaisyti produkto slankiojo vidurkio savikainą. Negali būti išlaidų srauto per vėlesnes operacijas.

Šiame pavyzdyje slankiojo vidurkio savikaina pakoreguota pagal produktą.

1. Pasirinkite produktą, kurio slankiojo vidurkio savikainą norite koreguoti. 

 > [!NOTE]
 > Puslapyje **Slankiojo vidurkio pakartotinis įvertinimas** tikrinamos turimos produkto atsargos. Pasirinkto produkto užregistruotas kiekis yra 1, užregistruota vertė 12,00, užregistruota vieneto savikaina 12,00 ir vieneto kaina 12,00.
    
1. Atnaujinkite lauko **Vieneto savikaina** vertę į 16,00. Sistema apskaičiuoja likusius formos laukus.
1. Koregavimas užregistruojamas.

> [!NOTE]
> Galite koreguoti slankiojo vidurkio savikainą tik nurodydami šiandienos datą.

Puslapyje **Sudengimai pagal kvitą** matyti, kad sąskaitoje Slankiojo vidurkio išlaidų pakartotinis įvertinimas užregistruotas koregavimas 4,00.

## <a name="moving-average-with-production"></a>Slankusis vidurkis ir produkcija

Slankiojo vidurkio funkcija palaiko pagamintas prekes. Jei planuojate naudoti slankiojo vidurkio funkciją gamybos aplinkoje, puslapyje **Gamybos kontrolės parametrai** pasirinkite **Naudoti įvertintą savikainą**. Tai reiškia, kad naudojama savikaina, apskaičiuojama vertinimo metu, vietoje faktinės KS apskaičiuotos savikainos.

## <a name="moving-average-with-a-backdated-transaction"></a>Slankusis vidurkis ir operacija atgaline data

Operacijos atgaline data priskiriamos dabartinei slankiojo vidurkio savikainai ir atnaujinamas faktinis produkto kiekis, bet produkto slankiojo vidurkio savikaina nepaveikiama. Šiame slankiojo vidurkio pavyzdyje registruojamas produkto slankusis vidurkis atliekant operaciją atgaline data.

1. Sukurkite produkto slankiojo vidurkio atsargų koregavimą, kai kiekis 1, o kaina 20,00.
1. Produkto atsargų operacijos retrospektyva būtų panaši į nurodytą toliau:
    - 1 produkto atsargų operacija, vieneto kaina 16,00, registravimo data sausio 15 d. ir operacijos data sausio 15 d.
    - 1 produkto atsargų koregavimas, vieneto kaina 20,00, registravimo data sausio 1 d. ir operacijos data sausio 15 d.
1. Koregavimo registravimas.

Puslapyje **Atsargų operacijos** matyti, kad dabartinio produkto slankusis vidurkis yra 16,00, o 4,00 įtraukiama į išlaidų sąskaitą. Galite registruoti praeityje, bet savikainos skirtumas įtraukiamas į išlaidų sąskaitą, todėl slankusis vidurkis nepaveikiamas.

## <a name="negative-inventory-balances"></a>Neigiamų atsargų balansai

Operacijos atliekamos skirtingai, atsižvelgiant į tai, ar naujas turimų kiekis po operacijos yra neigiamas, nulis, ar teigiamas.

### <a name="new-balance-is-negative-or-zero"></a>Naujas balansas yra neigiamas arba nulis

Jei naujas turimas kiekis yra neigiamas arba nulis, operacija bus įkainota dabartinėmis vidutinėmis savikainomis. Jei yra skirtumas tarp pirkimo kainos ir dabartinių vidutinių savikainų, užregistruojama į **Slankiojo vidurkio kainų skirtumas**.

### <a name="new-balance-is-positive"></a>Naujas balansas yra teigiamas

Jei po operacijos naujas turimas kiekis teigiamas, operacija padalinama į dvi dalis, kurios bus įkainotos skirtingai, kaip apibendrinta toliau pateiktoje lentelėje.

| Dalis | Aprašas |
|---|---|
| Kiekio atkūrimas iš neigiamo į nulį | Atsargose naudojama dabartinė slankiojo vidurkio savikaina, o ne gavimo kiekio dalies, atkuriančios turimo kiekio balansą iš neigiamo į nulį, operacijos išlaidos. Skirtumas tarp operacijos išlaidų ir dabartinės slankiojo vidurkio savikainos užregistruojamas į **Slankiojo vidurkio kainų skirtumas**. |
| Kiekio atkūrimas iš nulio į teigiamą | Atsargose naudojamos gavimo kiekio dalies, atkuriančios turimo kiekio balansą iš nulio į teigiamą, operacijos išlaidos.                                                  |

## <a name="inventory-value-report"></a>Atsargų vertės ataskaita

Šiame slankiojo vidurkio pavyzdyje atsargų vertės ataskaita spausdinama siekiant palaikyti esamą produkto slankiojo vidurkio skaičiavimą. Naudojant atsargų vertės ataskaitą operacijas galima spausdinti chronologine tvarka, kartu su savikaina, kad būtų palaikomas produkto slankiojo vidurkio savikainos skaičiavimas. Ataskaitoje rodoma produkto slankiojo vidurkio savikaina. Dialogo lange **Atsargų vertės ataskaitos** datos intervalas leidžia pasirinkti **Operacijos laikas** arba **Registravimo data** ir pagal tai rūšiuoti ataskaitą. Paprastai ataskaita spausdinama nustačius parinktį **Registravimo data**. Parinktis **operacijos laikas** yra faktinė data, kurią pranešama apie operaciją ir atnaujinama produkto slankiojo vidurkio savikaina. Atsargų vertės ataskaitą galite spausdinti naudodami parinktį **Rūšiavimas pagal operacijos laiką**, jei norite pamatyti slankiojo vidurkio savikainos apskaičiavimą per tam tikrą laiką. Toliau pateiktoje lentelėje rodomos produktų operacijos, kurioms spausdinama ataskaita, kai naudojama parinktis **Rūšiavimas pagal operacijos laiką**.

| Operacijos laikas | Data         | Operacijos tipas           | Kiekis | Suma | Vidutinė vieneto savikaina |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | Spalio 1 d.    | Pradžios balansas          | 0        | 0,00   | 0,00              |
| Spalio 8 d.        | Rugsėjo 28 d. | Kvitas atgaline data          | 1        | 16,00  | 16,00             |
| Spalio 3 d.        | Spalio 3 d.    | Pirkimo kvitas           | 2        | 20,00  | 12,00             |
| Spalio 5 d.        | Spalio 5 d.    | Pardavimo užsakymas                | -1       | –10,00 | 13,00             |
| Spalio 7 d.        | Spalio 7 d.    | Pirkimo SF           |          | 2,00   | 14,00             |
| Spalio 8 d.        | Spalio 8 d.    | Perkeliamas vidutinis perkainojimas |          | 4.00   | 16.00             |
|                  | Spalio 31 d.   | Bendroji suma                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Negalite suderinti su atsargų DK naudodami parinktį **Rūšiavimas pagal operacijos laiką**. Ataskaita turi būti spausdinama naudojant parinktį **Registravimo data**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]