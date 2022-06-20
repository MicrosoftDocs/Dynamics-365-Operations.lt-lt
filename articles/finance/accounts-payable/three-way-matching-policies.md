---
title: Trišalės atitikimo strategijos
description: Šiame straipsnyje pateikiami trišalio atitikimo pavyzdžiai.
author: abruer
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: twheeloc
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d6d98164766e81625bd9eeb9e504e5f0683151e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904936"
---
# <a name="three-way-matching-policies"></a>Trišalės atitikimo strategijos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami trišalio atitikimo pavyzdžiai.

## <a name="example-three-way-matching-for-items"></a>Pavyzdys: trišalis prekių atitikimas

**Suvestinė:** Ken yra valdytojas juridinio subjekto, kurio pavadinimas yra „Fabrikam“, įmonės būstinėje. Ken nusprendžia, kad visos pirkimo užsakymais pagrįstos tiekėjo SF turi atitikti pirkimo užsakymo eilutes (dvišalis atitikimas). Už įsigytas prekes, kurios bus naudojamos kaip ilgalaikis turtas, sąskaita faktūra turi atitikti pirkimo užsakymo eilutes ir produkto gavimo kvito eilutes (trišalis atitikimas).

„Fabrikam“ veikia su keliais juridiniais subjektais ir darbuotojais visuose pasaulio kraštuose. Didėjant operacijų kiekiui, daugėja ir neatitikimų tarp gavimo dokumentų ir SF. Dėl to tenka nurašyti turtą. Tiekėjų SF apmokama, tačiau šis procesas neapima neatitikimų identifikavimo gavus mažiau prekių nei buvo užsakyta, arba kai prekės visai negaunamos. Išlaidos taip pat didėja, nes darbuotojams vis tiek reikia įrankių ir kitų medžiagų jų darbui atlikti. Ken nori įsitikinti, kad tiekėjai siunčia tuos produktus, kurie užsakyti ir prekes gauna „Fabrikam“ darbuotojai. Todėl Ken reikia dvišalio ir trišalio atitikimo visiems organizacijos juridiniams subjektams. Sąskaitos faktūros gretinimas padeda užtikrinti, kad problemas su dingusiomis arba negautomis prekėmis galima sekti ir išspręsti. 

Šiame pavyzdyje pateikiamos sąskaitos faktūros atitikimo strategijos padeda žmonėms su šiais vaidmenimis atitikti šiuos tikslus:

-   Ken yra „Fabrikam“ įmonės valdytojas. Kenas gali padėti savo organizacijos žmonėms identifikuoti ir išspręsti problemas dėl užsakymo, gavimo ir mokėjimo už prekes (prekes ir paslaugas) iš tiekėjų.
-   Phyllis ir April yra „Fabrikam“ Jungtinių Valstijų padalinio mokėtinų sumų skyriaus apskaitos vadovai. Jie gali taikyti įmonės strategiją ir įsitikinti, kad sąskaitos faktūros apmokamos tik tada, kai jos suderinamos su pirkimo užsakymu ir prekių ir paslaugų gavimo dokumentais, kur tai taikoma.
-   Tony yra „Fabrikam“ Jungtinių Valstijų padalinio gamybos vadovas. Tonis ir kitas gamybos personalas gali užtikrinti, kad prekės gaunamos kaip buvo užsakytos iš tiekėjų ir yra apskaitytos, kad darbuotojai turi tai, ką jie turi turėti, kad galėtų atlikti savo darbą.

### <a name="prerequisites"></a>Būtinieji komponentai

-   Ken nustato atitikimo **strategiją** juridinio subjekto lygiu kaip trijinį **atitikimą**.
-   Ken nustato būseną **Automatiškai atnaujinti antraštės atitikimo būseną** juridiniame subjekte kaip **Taip**.
-   Ken nustato juridinio subjekto bendrųjų **gre tavimo kainų sumų lauką kaip procentinę** **dalį ir įveda 15% kaip leistino nuokrypio** procentinę dalį **.**
-   Ken nustato atitikimo strategiją prekės 1500 prekės lygiu –²icron Machine yra **triačiu atitikimu**. Ši prekė yra turto prekė, „Fabrikam“ naudojama gamyboje. Šios prekės sąskaitos faktūros yra sugretinamos su pirkimo užsakymo eilutėmis dėl kainos ir su produkto gavimo kvitais dėl kiekio.
-   Tony įveda paraišką penkiems „CNC Milicron“ įrenginiams. Alicia, „Fabrikam“ pirkimo užsakymų klerkas, išduoda pirkimo užsakymą tiekti prekes juridiniam subjektui, kurio vardas yra Contoso.

    | Prekės numeris                 | Kiekis | Vnt. kaina | Grynoji suma | Išlaidų kodas        | Išlaidų vertė |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – „CNC Milicron“ įrenginys | 5        | 8 000,00   | 40 000,00  | Siuntimas ir tvarkymas | 3 000,00      |

-   Arnie, „Contoso“ gautinų sumų klerkas, peržiūri savaitės siuntas. Arnie pasirenka siuntos operacijas, kurių sąskaitas faktūras išrašyti „Fabrikam“ už „CNC Milicron“ įrenginių pristatymą. Arnie įtraukia mokestį už siuntimą ir tvarkymą. „Fabrikam“ atsižvelgs į mokestį kaip į turto savikainos dalį.

### <a name="scenario"></a>Scenarijus

1.  Sammy, „Fabrikam“ gavimo padalinio darbuotojas, gavo visą kiekį įrenginių, išsiųstų iš „Contoso“. Produkto gavimo dokumente Samė įveda kiekį 5. Kadangi gautas visas pirkimo užsakymas, pirkimo užsakymo būsena pasikeičia į Gauta.
2.  April, „Fabrikam“ mokėtinų sumų koordinatorė, įveda ir patikrina sąskaitą faktūrą, kurią pateikė „Contoso“. Ji patikrina šią informaciją:
    -   Prekėms, kurioms reikalingas trišalis atitikimas, ar kiekis sąskaitos faktūros eilutėje atitinka gautą kiekį. Gautas kiekis nurodytas produkto gavimo kvite, kuris sugretintas su sąskaita faktūra.
    -   Prekių, kurioms reikia dvi dalių arba triaipų atitikimų, Microsoft Dynamics SF eilutėje nurodytos kainos atitinka leistinus nuokrypius, nustatytus 365 finansuose. Tai apima toliau nurodytus kainų gretinimo tipus.
        -   Grynosios vieneto kainos gretinimas – grynoji vieneto kaina sąskaitos faktūros eilutėje atitinka grynąją vieneto kainą pirkimo užsakymo eilutėje leistino nuokrypio procento ribose. Šiame pavyzdyje grynosios vieneto kainos leistinas nuokrypis yra + 8 %.
        -   Kainų grynųjų sumų gretinimas – grynoji suma sąskaitos faktūros eilutėje atitinka grynąją sumą pirkimo užsakymo eilutėje leistino nuokrypio procento, sumos arba procento ir sumos ribose. Šiame pavyzdyje kainų grynųjų sumų leistinas nuokrypis yra + 15 %.

Popierinėje „Contoso“ sąskaitoje faktūroje pateikta ši informacija.

| Prekė                        | Kiekis | Vnt. kaina | Grynoji suma |
|-----------------------------|----------|------------|------------|
| 1500 – „CNC Milicron“ įrenginys | 5        | 8 100,00   | 40,500.00  |
| Siuntimas ir tvarkymas       |          |            | 4,000.00   |
| Mokesčiai                         |          |            | 0,00       |
| Bendroji suma                       |          |            | 44,500.00  |

Sąskaitos faktūros eilutėje pateikiama toliau nurodyta informacija.

| Prekės Nr.                 | Kiekis | Vnt. kaina | Grynoji eilutės suma | Atitikimo strategija    | Gavimo dokumentų kiekio sugretinimas | Kainos gretinimas | Kainos sumos gretinimas |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – „CNC Milicron“ įrenginys | 5        | 8 100,00   | 40 500,00       | Tripusis atitikimas | Įvykdyta sėkmingai                         | Įvykdyta sėkmingai      | Įvykdyta sėkmingai            |

Kadangi ši eilutė pereina sąskaitos faktūros gretinimo procesą, sąskaitą faktūrą galima registruoti.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a> Pavyzdys: trišalis prekės ir tiekėjo kombinacijų atitikimas
Suvestinė: Ken yra valdytojas juridinio subjekto, kurio pavadinimas yra „Fabrikam“, įmonės būstinėje. Ken nusprendžia, kad visos pirkimo užsakymais pagrįstos sąskaitos faktūros turi atitikti pirkimo užsakymo eilutes (dvišalis atitikimas). Cassie yra „Fabrikam“ Malaizijos skyriaus finansininkė. Ji nurodo, kad pasirinktos prekės, kurios užsakytos iš tam tikrų tiekėjų Malaizijoje, turi būti sugretintos su pirkimo užsakymo eilutėmis ir produkto gavimo dokumento eilutėmis (trišalis atitikimas). Ji taip pat gali nepaisyti atitikimo strategijos su aukštesnio lygio konkrečių pirkimo užsakymų atitikimu. 

Kiekis ir sumos yra mažos, kilo problemų su pristatymu iš kai kurių tiekėjų Malaizijoje. Dėl šių priežasčių Cassie nustato kontrolės lygį tam tikriems prekių ir tiekėjų kombinacijoms, kurios įsigytos Malaizijoje, iki trišalio atitikimo. 

Šiame pavyzdyje pateikiamos sąskaitos faktūros atitikimo strategijos padeda žmonėms su šiais vaidmenimis atitikti šiuos tikslus:
-   Ken yra „Fabrikam“ įmonės valdytojas. Kenas gali padėti savo organizacijos žmonėms identifikuoti ir išspręsti problemas dėl užsakymo, gavimo ir mokėjimo už prekes (prekes ir paslaugas) iš tiekėjų.
-   Cassie yra „Fabrikam“ Malaizijos skyriaus finansininkė. Jie gali taikyti įmonės strategiją ir įsitikinti, kad sąskaitos faktūros apmokamos tik tada, kai jos sugretinamos su pirkimo užsakymo eilutėmis ir produkto gavimo kvitais, nurodančiais prekių ir paslaugų gavimą. Ji taip pat gali padidinti konkrečių prekių kontrolės lygį iki trišalio atitikimo, siekiant kontroliuoti veiklos išlaidas.

### <a name="prerequisites"></a>Būtinieji komponentai

-   Ken juridinio **subjekto** lygyje nustato atitikimo strategiją kaip **dvi savaites atitinkančią**.
-   Ken nustato juridinio **subjekto bendrųjų** gre tavimo kainų sumų lauką kaip **procentinę** **dalį ir įveda 10% kaip** leistino nuokrypio **procentinę dalį.**
-   Ken nustato vieneto kainos leistiną nuokrypį visoms prekėms iki 2 %.
-   "Įmonės" nustato **prekės** ir tiekėjo derinio lygio atitikimo strategiją – PREKĖS CONTOSO2500 – kompiuterio ir tiekėjo "Contoso" triaipipuoju **atitikimu**.
-   Alicia, pirkimo užsakymo klerkas „Fabrikam“ Malaizijos padalinyje, „Contoso“ išduoda pirkimo užsakymus tiekti tris prekes, kaip parodyta toliau pateiktoje lentelėje. Kai kuria pirkimo užsakymą, ji **panaikina** atitikimo strategiją, pagal kuria pelės žymeklis turi būti trijuose atitikmens parametruose, o ne dvi parinktame atitikmenyje.

    | Prekės numeris           | Kiekis | Vnt. kaina | Grynoji suma | Atitikimo strategija (numatytasis įrašas) | Atitikimo strategija (nurodyta pirkimo užsakymo eilutėje) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – kompiuteris     | 2        | 2 500,00   | 5 000,00   | Tripusis atitikimas              | Tripusis atitikimas                           |
    | MM01 – belaidė pelė | 2        | 40,00      | 80,00      | Dvipusis atitikimas                | Tripusis atitikimas                           |
    | USB atmintukas             | 200      | 10,00      | 2 000,00   | Dvipusis atitikimas                | Dvipusis atitikimas                             |

### <a name="scenario"></a>Scenarijus

1.  Prekės pristatomos. Sammy, „Fabrikam“ gavimo skyriaus Malaizijoje darbuotojas, sutrukdomas, todėl produkto gavimo kvitą užregistruoja ne iš karto.
2.  April, „Fabrikam“ mokėtinų sumų koordinatorė, įveda ir patikrina sąskaitą faktūrą, kurią pateikė „Contoso“. Ji patikrina šią informaciją:
    -   Prekėms, kurioms reikalingas trišalis atitikimas, ar kiekis sąskaitos faktūros eilutėje atitinka gautą kiekį. Gautas kiekis nurodytas produkto gavimo kvite, kuris sugretintas su sąskaita faktūra.
    -   Prekių, kurioms reikalingas dvišalis arba trišalis atitikimas, sąskaitos faktūros eilutės kainos patenka į leistinus nuokrypius, kurie apibrėžti programoje. Tai apima toliau nurodytus kainų gretinimo tipus.
        -   Grynosios vieneto kainos gretinimas – grynoji vieneto kaina sąskaitos faktūros eilutėje atitinka grynąją vieneto kainą pirkimo užsakymo eilutėje leistino nuokrypio procento ribose. Šiame pavyzdyje grynosios vieneto kainos leistinas nuokrypis yra + 2 %.
        -   Kainų grynųjų sumų gretinimas – grynoji suma sąskaitos faktūros eilutėje atitinka grynąją sumą pirkimo užsakymo eilutėje leistino nuokrypio procento, sumos arba procento ir sumos ribose. Šiame pavyzdyje kainų grynųjų sumų leistinas nuokrypis yra + 10 %.

Popierinėje „Contoso“ sąskaitoje faktūroje pateikta ši informacija.

| Prekė                  | Kiekis | Vnt. kaina | Grynoji suma |
|-----------------------|----------|------------|------------|
| PH2500 – kompiuteris     | 2        | 2 500,00   | 5 000,00   |
| MM01 – belaidė pelė | 2        | 41.00      | 82.00      |
| USB atmintukas             | 200      | 10.05      | 2,010.00   |
| Visa SF         |          |            | 7,092.00   |

Sąskaitos faktūros eilutėje pateikiama toliau nurodyta informacija.

| Prekės Nr.           | Kiekis | Vnt. kaina | Grynoji eilutės suma | Atitikimo strategija    | Gavimo dokumentų kiekio sugretinimas | Kainos gretinimas | Kainos sumos gretinimas |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – kompiuteris     | 2        | 2 500,00   | 5 000,00        | Tripusis atitikimas | Nepavyko                         | Įvykdyta sėkmingai      | Įvykdyta sėkmingai            |
| MM01 – belaidė pelė | 2        | 41,00      | 82,00           | Tripusis atitikimas | Nepavyko                         | Nepavyko      | Įvykdyta sėkmingai            |
| USB atmintukas             | 200      | 10,05      | 2010,00         | Dvipusis atitikimas   |                                | Įvykdyta sėkmingai      | Įvykdyta sėkmingai            |

Atkreipkite dėmesį į toliau nurodytas prekes:
-   PH2500 – kompiuterio eilutės produkto gavimo kiekio sugretinimo stulpelyje yra įspėjamoji piktograma, nes sąskaitos faktūros eilutė nesugretinta su produkto gavimo kvitu.
-   MM01 – belaidės pelės eilutės produkto gavimo kiekio sugretinimo stulpelyje yra įspėjamoji piktograma, nes sąskaitos faktūros eilutė nesugretinta su produkto gavimo kvitu. Stulpelyje Vieneto kainos gretinimas yra įspėjamoji piktograma, nes viršytas 2 % vieneto kainos leistinas nuokrypis.
-   USB atmintinės eilutės Produkto gavimo kiekio gretinimo stulpelis yra tuščias, nes dvipusis atitikimas neatitinka sąskaitos faktūros eilutės ir produkto gavimo kvito eilutės kiekių.

Jei reikia SF, kurios turi būti registruojamos su gretinimo nesutapimų, **·** **patvirtinimo** registravimo gretinimo nesutapimų puslapyje turi būti pasirinkta SF gretinimo informacijos puslapyje, kad SF būtų užregistruota su kainų gretinimo klaidomis ir kiekio gretinimo klaidomis. Jei patvirtinimo nereikia, sąskaitos faktūros apdorojimą galima tęsti, jei nėra jokių kitų registravimo klaidų.


Daugiau informacijos žr. [Mokėtinų sumų SF gretinimo apžvalga](accounts-payable-invoice-matching.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
