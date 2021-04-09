---
title: Įplaukų pripažinimas pardavimo užsakymuose
description: Šioje temoje aprašomos pagrindinės pardavimo užsakymų ir SF įplaukų pripažinimo funkcijos. Įplaukų pripažinimas galimas pardavimo užsakyme ir atitinkamoje SF, sukuriamoje iš pardavimo užsakymo.
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: e9c6423a7fb604005d4fb7f1eca05a1ef7d210e5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817226"
---
# <a name="revenue-recognition-on-sales-orders"></a>Įplaukų pripažinimas pardavimo užsakymuose

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Įplaukų pripažinimo funkcija negali būti įjungta naudojant funkcijų valdymą. Dabar norėdami ją įjungti, turite naudoti konfigūracijos raktus.

Šioje temoje aprašomos pagrindinės pardavimo užsakymų ir SF įplaukų pripažinimo funkcijos. Įplaukų pripažinimas galimas pardavimo užsakyme ir atitinkamoje SF, sukuriamoje iš pardavimo užsakymo. Pardavimo užsakymą taip pat galima sukurti naudojant laiko ir medžiagų projektą.

> [!NOTE]
> Šios temos iliustracijose stulpeliai buvo paslėpti arba įtraukti į tinklelius, kad būtų geriau rodomos koncepcijos. Todėl iliustracijų puslapiai ir duomenys gali skirtis nuo to, ką matote produkte.

## <a name="enter-a-sales-order"></a>Įvesti pardavimo užsakymą

Įvedamas šis pardavimo užsakymas ir įtraukiamos trys prekės, nustatytos įplaukų pripažinimui.

[![Įvesti pardavimo užsakymą](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

Yra dvi įplaukų pripažinimo koncepcijos:

- **Nustatyti įplaukų vertę.** Įplaukų vertė skaičiuojama pagal išleistų produktų nustatymus. Įplaukų vertė niekuomet nebus rodoma klientui, ji naudojama tik pardavimo užsakymo SF apskaitai. Pardavimo užsakymo eilutėse ir dokumentuose, išspausdintuose kaip pardavimo dalis, ir toliau rodomi vieneto / sąrašo kainą.
- **Apibrėžti, kada turi būti atliekamas įplaukų pripažinimas.** Įplaukų grafikas naudojamas apibrėžti, kada turi būti pripažįstamos įplaukos.

    Šiame pavyzdyje pirmoji prekė S0001 priskiriama **1O** (vieno pasikartojimo) įplaukų grafike. Šioje eilutėje rodomas etapo tipo scenarijus, kurio įplaukos bus pripažįstamos po diegimo ateityje. Todėl įplaukos bus atidedamos, kol diegimas bus baigtas.

    Antroji prekė S0008 yra aptarnavimo prekė, nustatyta kaip palaikymo pasibaigus sutarčiai (PCS) prekė. Ilgalaikės inžinerinės paslaugos klientui teikiamos per 12 mėnesių laikotarpį. Todėl, pagal numatytuosius nustatymus produktui priskiriamas **12 mėn.** įplaukų grafikas. Kadangi ši prekė yra PCS prekė, turi būti apibrėžtos sutarties pradžios ir pabaigos datos. Pagal numatytuosius nustatymus sutarties pradžios ir pabaigos datos yra prekės išsamioje informacijoje – skirtuke „Nustatymai“. Įplaukų grafike **12 mėn.** nustatymai apibrėžiami taip, kad sutarties sąlygos būtų automatiškai įrašomos, kaip parodyta šioje iliustracijoje.

    [![Įplaukų grafikai](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    Trečia prekė S0012 yra aparatūra ir įplaukų grafikas jai nėra priskirtas pagal numatytuosius nustatymus. Aparatūros įplaukos pripažįstamos iš karto, kai išrašoma prekės SF.

## <a name="confirm-the-sales-order"></a>Patvirtinti pardavimo užsakymą

Norėdami peržiūrėti papildomą informaciją apie įplaukų vertę ir įplaukų grafiką, naudokite mygtukus, esančius grupėje **Įplaukų pripažinimas**, skirtuke **Tvarkyti**, esančiame pardavimo užsakymo veiksmų srityje. Kadangi šiuo metu pardavimo užsakymas nepatvirtintas, mygtukai, naudojami įplaukoms pripažinti, yra neprieinami. Šie mygtukai tampa prieinami arba neprieinami, nes pardavimo užsakymas vyksta etapais, kurie lemia vykdymą.

[![Pardavimo užsakymo antraštė](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

Pirmi trys mygtukai pateikia išsamią informaciją apie priekių įplaukų vertę pardavimo užsakymo nustatymuose įplaukų pripažinimui.

- **Įplaukų vertės paskirstymas** – šis mygtukas tampa pasiekiamas patvirtinus pardavimo užsakymą arba užregistravus SF. Patvirtinus pardavimo užsakymą arba užregistravus SF, apskaičiuojamos pripažintinų įplaukų vertė, kuri bus pripažinta arba atidėta apskaitos įraše. Priklausomai nuo nustatymų, apskaičiuota įplaukų vertė gali skirtis nuo klientui rodomos vieneto kainos.
- **Perskirstyti vertę naujose užsakymo eilutėse** – šis mygtukas tampa pasiekiamas patvirtinus pardavimo užsakymą arba užregistravus SF. Perskirstymo procesas naudojamas įplaukoms, kurios turi būti pripažintos po to, kai nauja eilutė įtraukiama į esamą pardavimo užsakymą, po to, kai išrašoma jo SF, perskaičiuoti, arba naujame pardavimo užsakyme. Abiem atvejais, pridėjus naują prekę, keičiama sutartis. Todėl reikia perskirstyti įplaukų vertę.
- **Atnaujinti įplaukų vertės paskirstymą** – šis mygtukas tampa pasiekiamas patvirtinus pardavimo užsakymą, bet jis tampa nepasiekiamas, kai išrašoma pardavimo užsakymo SF. Naujinimas naudojamas norint iš naujo paleisti įplaukų vertės paskirstymą netvirtinant pardavimo užsakymo. Išrašius pardavimo užsakymo SF, įplaukų vertės perskaičiuoti negalima.

Paskutiniai du mygtukai pateikia išsamią informaciją apie šių pardavimo užsakymo, kuriame yra įplaukų grafikas, prekių įplaukų grafiką.

- **Numatomas įplaukų pripažinimo grafikas** – šis mygtukas tampa pasiekiamas patvirtinus pardavimo užsakymą, bet jis tampa nepasiekiamas, kai išrašoma pardavimo užsakymo SF. Atidaromas puslapis, kuriame rodomas numatomas įplaukų grafikas. Galutinis grafikas gali pasikeisti, nes numatomame grafike naudojama pageidaujama siuntimo data, o galutiniame grafike naudojama faktinė siuntimo data.
- **Įplaukų pripažinimo grafikas** – šis mygtukas tampa pasiekiamas, kai išrašoma pardavimo užsakymo SF. Galutinis įplaukų pripažinimo grafikas nesukuriamas, kai gaunamas patvirtinimas arba sukuriamas važtaraštis. Jis sukuriamas tik tada, kai išrašoma pardavimo užsakymo SF.

Šiame pavyzdyje įplaukų vertės paskirstymas įvyko patvirtintus pardavimo užsakymą. Atkreipkite dėmesį, kad, net jei įplaukų vertės yra paskirstytos skirtingai, bendroji suma, esanti lauke **Pripažintinos įplaukos** turi sutapti su pardavimo užsakymo eilučių, kurių SF išrašyta klientui, suma. Pavyzdžiui, pardavimo užsakymo eilučių suma, neįskaitant mokesčių, yra 1499 $. Todėl **Pripažintinos įplaukos** verčių suma taip pat turi būti 1499 $.

[![Įplaukų vertės paskirstymas](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

Taip pat sukuriamas numatomas įplaukų pripažinimo grafikas. Įplaukų grafike naudojama **Pripažintinos įplaukos** vertė kaip atidėtina suma. Prekės S0001 atidedama suma yra 321,21 $ vietoje 300 $, o prekės S0008 atidedama suma yra 160,61 $ vietoje 100 $. Prekė S0012 nėra rodoma numatomame grafike, nes įplaukos nėra atidėtos. Vykdant registravimą, registruojama prekės S0012 1 017,18 $ tiesiogiai įplaukų DK sąskaitoje.

[![Numatomas įplaukų pripažinimo grafikas](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>Kurti važtaraštį

Toliau galima sukurti pardavimo užsakymo važtaraštį. Užregistravus važtaraštį, įplaukos nepripažįstamos. Jei pardavimo užsakymas nebuvo patvirtintas, važtaraščio registravimas nesuaktyvina įplaukų vertės skaičiavimo. Jis taip pat nesuaktyvina numatyto arba galutinio įplaukų pripažinimo grafiko kūrimo. Jei prekių modelių grupė nustatoma atidėti įplaukas važtaraštyje, ji ir toliau bus registruojama naudojant esamas registravimo šablono DK sąskaitas, o ne naujas atidėtų įplaukų sąskaitas, kurios naudojamos registruojant SF.

## <a name="create-the-invoice"></a>Kurti SF

Paskutinis veiksmas yra pardavimo užsakymo SF išrašymas. Peržiūrėdami SF kvitą, pastebėsite, kad prekių S0001 ir S0008 įplaukos buvo atidėtos (321,21 $ + 160,61 $ = 481,82 $), o likusi prekės S0012 suma užregistruota įplaukoms (1 017,18 $). Šios vertės sudaro 1 499 $ sumą, kuri atitinka pardavimo užsakymo eilučių sumą.

[![Kvitų operacijos](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

Sukūrus SF, mygtukai **Įplaukų vertės paskirstymas**, **Perskirstyti vertę naujose užsakymo eilutėse** ir **Įplaukų pripažinimo grafikas**, skirti įplaukų pripažinimui, tampa prieinami, o mygtukai **Naujinti įplaukų vertės paskirstymą** ir **Numatomas įplaukų pripažinimo grafikas** tampa neprieinami.

[![Galimo įplaukų pripažinimo mygtuko prieinamumas](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

Mygtukas **Įplaukų vertės paskirstymas** vis dar prieinamas, kad galėtumėte peržiūrėti įplaukų vertės skaičiavimą. Jei pardavimo užsakyme niekas nepasikeitė po to, kai jis buvo patvirtintas, SF registravimas nekeis apskaičiuotos sumos lauke **Pripažintinos įplaukos**.

Numatomas įplaukų pripažinimo grafikas pašalinamas ir pakeičiamas galutiniu įplaukų pripažinimo grafiku. Kiekvieno pardavimo užsakymo eilutės įplaukų grafiko informacija tvarkoma ir naudojama atidėtoms įplaukoms priskaičiuoti prie faktinių įplaukų, kai įvykdomi sutartiniai įsipareigojimai.

[![Galutinis įplaukų pripažinimo grafikas](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]