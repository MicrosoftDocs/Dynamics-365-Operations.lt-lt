---
title: Perkėlimo užsakymų kūrimas iš sandėlio programos
description: Šiame straipsnyje aprašoma, kaip kurti ir apdoroti perkėlimo užsakymus naudojant sandėlio valdymo mobiliąją programą
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 45cbf7aca431c19e58de75355579304baef3cf7d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336462"
---
# <a name="create-transfer-orders-from-the-warehouse-app"></a>Perkėlimo užsakymų kūrimas iš sandėlio programos

[!include [banner](../includes/banner.md)]

Ši funkcija leidžia sandėlio darbuotojams kurti ir apdoroti perkėlimo užsakymus tiesiai iš sandėlio valdymo mobiliųjų įrenginių programėlės. Darbuotojas pirmiausia pasirenka paskirties sandėlį, o tada gali nuskaityti vieną ar daugiau numerio lentelių naudodami programą, kad į perkėlimo užsakymą būtų įtrauktos numerio lentelės. Kai sandėlio darbuotojas pasirenka **Užbaigti užsakymą**, paketinė užduotis sukuria reikiamą perkėlimo užsakymą ir užsakymo eilutes pagal turimas atsargas, užregistruotas toms numerio lentelėms.

## <a name="turn-on-this-feature-and-its-prerequisites"></a><a name="enable-create-transfer-order-from-warehouse-app"></a> Įjungti šią funkciją ir jos būtinąsias sąlygas

Norėdami pasinaudoti šia funkcija, ją ir jos būtinąsias sąlygas turite įjungti savo sistemoje. Administratoriai gali naudoti [funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį, kad patikrintų funkcijos būseną ir įjungtų ją, jei reikia.

1. Įgalinkite šias dvi priemones (nurodyta) funkcijų [valdymo darbo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) srityje. Kaip ir tiekimo grandinės valdymo versija 10.0.25, abi šios priemonės įjungiamos pagal numatytuosius nustatymus.
    1. *Apdoroti sandėlio programos įvykius*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima.)
    1. *Kurti ir apdoroti perkėlimo užsakymus naudojant sandėlio programą*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima.)
1. Norėdami automatizuoti siunčiamų siuntų apdorojimą, turite įgalinti [*siunčiamų siuntų patvirtinimo iš paketinių užduočių funkciją*](confirm-outbound-shipments-from-batch-jobs.md). (Kaip ir tiekimo grandinės valdymo versija 10.0.21, ši funkcija įjungiama pagal numatytąjį nustatymą. Kadangi tiekimo grandinės valdymas yra 10.0.25, ši funkcija yra privaloma ir jos išjungti negalima.)

## <a name="set-up-a-mobile-device-menu-item-to-create-transfer-orders"></a><a name="setup-warehouse-app-menu"></a>Mobiliojo įrenginio meniu elemento nustatymas perkėlimo užsakymams kurti

Toliau pateikiami bendrieji nurodymai, kaip nustatyti mobiliojo įrenginio meniu elementą perkėlimo užsakymui kurti. Atsižvelgiant į jūsų automatizavimo lygio, nustatomo vartotojams kuriant perkėlimo užsakymus iš aukšto, verslo reikalavimus, bus įjungtos skirtingos konfigūracijos. Šio dokumento scenarijuje bus aprašyta viena tokia konfigūracija.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Pasirinkite **Naujas**, norėdami įtraukti naują meniu elementą. Tada nustatykite toliau pateiktus parametrus, kad pradėtumėte.

    - **Meniu elemento pavadinimas** – priskirkite pavadinimą, kuris turi būti rodomas „Supply Chain Management”.
    - **Pavadinimas** – priskirkite meniu pavadinimą, kuris turi būti pateikiamas darbuotojams sandėlio valdymo mobiliųjų įrenginių programėlėje.
    - **Režimas** – nustatykite į *Netiesioginis* (šis meniu elementas nekurs darbo).
    - **Veiklos kodas** – nustatykite į *Kurti perkėlimo užsakymą iš numerio lentelių*, kad sandėlio darbuotojai galėtų sukurti perkėlimo užsakymą, pagrįstą viena ar daugiau nuskaitytų numerio plokštelių.

1. Naudokite parametrą **Perkėlimo užsakymo eilutės kūrimo strategija**, norėdami valdyti, kaip bus kuriamos šio meniu elemento perkėlimo užsakymo eilutės. Eilutės bus kuriamos / naujinamos pagal turimas atsargas, užregistruotas nuskaitytoms numerio lentelėms. Pasirinkite vieną iš toliau pateiktų reikšmių.

    - **Nėra rezervavimo** – perkėlimo užsakymo eilutės nebus rezervuotos.
    - **Pagal numerio lentelę ir eilutės rezervaciją** – perkėlimo užsakymo eilutės bus rezervuotos ir naudos strategijos Pagal numerio lentelę parinktį, kurioje saugomi su užsakymo eilutėmis susieti atitinkami numerio lentelių ID. Rastos numerio lentelės ID reikšmės gali būti vėliau panaudotos kaip darbo kūrimo perkėlimo užsakymo eilutėms dalis.

1. Jei reikia, naudokite parametrą **Siunčiamos siuntos strategija**, norėdami į siunčiamos perkėlimo užsakymo siuntos procesą įtraukti daugiau automatizavimo. Kai darbuotojas pasirenka mygtuką **Užbaigti užsakymą**, programa sukuria sandėlio programos įvykį *Užbaigti užsakymą*, kuris įrašo reikšmę, kurią pasirenkate lauke **Siunčiamos siuntos strategija**, kiekvienai eilutei, esančiai dabartiniame perkėlimo užsakyme. Vėliau, kai paketinė užduotis apdoroja įvykių eilę, kad būtų sukurtas perkėlimo užsakymas, paketinė užduotis gali nuskaityti šiame lauke saugomą vertę, todėl gali valdyti, kaip ta užduotis apdoroja kiekvieną eilutę. Pasirinkite vieną iš šių parinkčių:

    - **Nėra** – nevykdomas automatizuotas apdorojimas.
    - **Išleidimas į sandėlį** – automatizuoja išleidimo į sandėlį procesą.
    - **Siuntos patvirtinimas** – automatizuoja siuntos patvirtinimo procesą.
    - **Išleidimo ir siuntos patvirtinimas** – automatizuoja ir išleidimo į sandėlį procesą, ir siuntos patvirtinimo procesą.

## <a name="add-the-mobile-device-menu-item-to-a-menu"></a>Mobiliojo įrenginio meniu elemento įtraukimas į meniu

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**
1. Pasirinkite **Redaguoti**.
1. Pasirinkite esamą meniu, tada pasirinkite naują meniu elementą dalyje **Galimi meniu ir meniu elementai**. Įtraukite meniu elementą pasirinkdami rodyklės dešinėn mygtuką.

## <a name="create-a-transfer-order-based-on-license-plates"></a>Perkėlimo užsakymo kūrimas pagal numerio lenteles

Sandėlio valdymo mobiliųjų įrenginių programėlėje galima vykdyti paprastą perkėlimo užsakymų kūrimo pagal numerio lentelės procesą. Norėdamas jį vykdyti, darbuotojas turi atlikti toliau pateiktus veiksmus naudodamas sandėlio valdymo mobiliųjų įrenginių programėlę.

1. Sukurti perkėlimo užsakymą ir nustatyti paskirties sandėlį.
1. Nustatyti kiekvieną numerio lentelę, kurią reikia išsiųsti.
1. Pasirinkite **Užbaigti užsakymą**.

>[!NOTE]
> Keli darbuotojai gali priskirti tam pačiam perkėlimo užsakymui skirtas numerio lenteles, naudodami mygtuką **Pasirinkti perkėlimo užsakymą**, kad pasirinktų esamą neapdorotą perkėlimo užsakymo numerį iš sandėlio programos įvykių eilės. Informacijos apie tai, kaip rasti perkėlimo užsakymo numerio vertes, žr. [Užklausos dėl sandėlio programos įvykių pateikimas](#inquire-the-warehouse-app-events).

## <a name="example-scenario"></a>Pavyzdinis scenarijus

Šiame scenarijuje pateikiama perkėlimo užsakymų, sukurtų ir automatiškai apdorotų pagal turimas atsargas, užregistruotas pasirinktoms numerio lentelėms, gavimo proceso apžvalga.

Norėdami dirbti pagal šį scenarijų ir naudoti siūlomas reikšmes, turite dirbti su sistema, kurioje įdiegti demonstraciniai duomenys, ir prieš pradėdami pasirinkti *USMF* juridinį subjektą.

Šiame scenarijuje laikoma, kad jau įjungėte [funkciją Kurti ir apdoroti perkėlimo užsakymus iš sandėlio programos](#enable-create-transfer-order-from-warehouse-app) ir [sandėlio programos įvykių apdorojimo](warehouse-app-events.md) funkciją.

Be to, reikia ne tik nustatyti perkėlimo užsakymo kūrimą mobiliojo įrenginio meniu elementuose, bet ir nustatyti bei įjungti papildomus šablonus, vietos nurodymus ir paketines užduotis.

### <a name="example-scenario-blueprint"></a>Scenarijaus pavyzdžio planas

Esate pardavėjas ir turite kelias numerio lenteles, o kiekvienoje iš jų yra prekių, padėtų konkrečioje vieno iš jūsų sandėlių vietoje, mišinys (*Sandėlis 51*). Norite įjungti procesą, leidžiantį darbuotojams sukurti perkėlimo užsakymą į kitą sandėlį (*Sandėlis 61*), kad būtų galima rinkti nuskaitytas numerio lenteles. Perkėlimo užsakymas bus automatiškai išsiųstas / atnaujintas, kai tik bus nustatyta paskutinė užsakymo numerio lentelė.

![Automatizuoto perkėlimo užsakymo apdorojimo pavyzdys.](media/create-transfer-order-from-app-example.png "Automatizuoto perkėlimo užsakymo apdorojimo pavyzdys")

### <a name="create-a-mobile-device-menu-item-for-creating-transfer-orders"></a>Mobiliojo įrenginio meniu elemento kūrimas perkėlimo užsakymams kurti

Šiame skyriuje aprašoma, kaip sukurti naują mobiliojo įrenginio meniu elementą, skirtą perkėlimo užsakymams kurti. Nustatykite **Režimas** į *Netiesioginis*, o **Veiklos kodas** į *Kurti perkėlimo užsakymą iš numerio lentelių*.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.
1. Pasirinkite **Naujas**.
1. Lauke **Meniu elemento pavadinimas** įveskite pavadinimą *TO kūrimas*.
1. Lauke **Pavadinimas** įveskite aprašą *TO kūrimas*.
1. Lauke **Režimas** pasirinkite *Netiesioginis*.
1. Dalyje **Veiklos kodas** pasirinkite *Kurti perkėlimo užsakymą iš numerio lentelių*
1. Dalyje **Užsakymo eilutės kūrimo strategija** pasirinkite *Pagal numerio lentelę ir eilutės rezervaciją*.
1. Dalyje **Siunčiamos siuntos strategija** pasirinkite *Išleidimo ir siuntos patvirtinimas*.
1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu**.
1. Pasirinkite **Redaguoti**.
1. Pasirinkite esamą meniu **Atsargos**, tada pasirinkite naują meniu elementą dalyje **Galimi meniu ir meniu elementai**. Įtraukite meniu elementą į meniu **Atsargos** pasirinkdami rodyklės dešinėn mygtuką.

### <a name="set-up-work-templates-to-auto-process-and-break-work-by-located-license-plate"></a>Darbo šablonų nustatymas siekiant automatiškai apdoroti ir nutraukti darbą pagal rastą numerio lentelę

Šiame skyriuje paaiškinama, kaip įjungti darbo šabloną, kad darbas, kurį sukūrė šablonas išleidus bangą, būtų automatiškai apdorojamas.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Darbas \> Darbo šablonai**.
1. Lauke **Darbo užsakymo tipas** pasirinkite *Perkėlimo išdavimas*.
1. Pasirinkite **Naujas** tam, kad sukurtumėte naują darbo šabloną.
1. Lauke **Darbo šablonas** įveskite *51 automatinio apdorojimo LP*.
1. Lauke **Darbo šablono aprašas** įveskite *51 automatinio apdorojimo LP*.
1. Pažymėkite žymės langelį **Automatiškai apdoroti**. Jis turi būti parinktas, kad būtų galima apdoroti bet kokius automatizavimo veiksmus.
1. Demonstraciniuose duomenyse jau yra darbo šablonas *51 perkėlimas*, redaguokite lauką **Sekos numeris**, kad naujo darbo šablono sekos numeris būtų mažesnis nei esamo darbo šablono *51 perkėlimas*.
1. Įrankių juostoje pasirinkite **Įrašyti**, kad būtų įjungtas „FastTab“ **Darbo šablono išsami informacija**.
1. „FastTab“ **Darbo šablono išsami informacija** įrankių juostoje pasirinkite **Naujas**. Bus įtrauktos dvi eilutės.
1. Lauke **Darbo tipas** pasirinkite *Pasirinkti*.
1. Lauke **Darbo klasės ID** pasirinkite *TransfOut*.
1. Įrankių juostoje **Darbo šablono informacija** pasirinkite **Naujas**.
1. Lauke **Darbo tipas** pasirinkite *Padėjimas*.
1. Lauke **Darbo klasės ID** pasirinkite *TransfOut*.
1. Pasirinkite **Įrašyti**, kad būtų įjungtas laukas **Nurodymo kodas**.
1. Dalyje **Darbo tipas**, eilutėje *Padėti*, pasirinkite **nurodymo kodą** *Baydoor*. Įsitikinkite, kad šis naujas darbo šablonas turi žemiausią **sekos numerį**.
1. Norėdami atidaryti užklausų rengyklę, įrankių juostoje pasirinkite **Redaguoti užklausą**.
1. Skirtuke **Diapazonas** pasirinkite **Įtraukti**.
1. Įtrauktos eilutės dalyje **Laukas** pasirinkite *Sandėlis*.
1. Lauke **Kriterijai** pasirinkite *51*.
1. Pasirinkite skirtuką **Rūšiavimas**.
1. Pasirinkite **Įtraukti** ir nustatykite **Laukas** į *Rastas numerio lentelės ID*. Pasirinkus šį lauką bus įjungtas įrankių juostos mygtukas **Darbo antraštės lūžiai**.
1. Pasirinkite **Gerai**, tada – **Taip**, norėdami iš naujo nustatyti grupavimą ir grįžti į puslapį **Darbo šablonai**.
1. Pasirinkite **Darbo antraštės lūžiai**, įjunkite **Grupuoti pagal šį lauką** dalyje **Rastas numerio lentelės ID** ir uždarykite.

> [!NOTE]
> Ne visi nustatymai gali būti apdorojami automatiškai, pvz., esamo svorio prekės ir mišrių sekimo dimensijų naudojimas.

### <a name="set-up-location-directives-for-the-license-plate-guided-strategy"></a>Vietos nurodymų nustatymas strategijai Pagal numerio lentelę

Šiame skyriuje paaiškinama, kaip nustatyti paėmimo vietos nurodymų procesą norint naudoti strategiją **Pagal numerio lentelę**.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Pasirinkite **Redaguoti**.
1. Naršymo sąrašo antraštėje pasirinkite **darbo užsakymo tipą** *Perkėlimo išdavimas*.
1. Naršymo sąraše pasirinkite esamą vietos nurodymą **51 TO paėmimas**.
1. „FastTab” **Eilutės** pasirinkite žymės langelį **Leisti skaidyti**.
1. „FastTab“ **Vietos nurodymo veiksmai** pasirinkite **Naujas**, norėdami įtraukti naują veiksmo eilutę.
1. Lauke **Pavadinimas** įveskite *Pagal LP*.
1. Lauke **Strategija** pasirinkite *Pagal numerio lentelę*. Šiam veiksmui reikia mažiausio sekos numerio.
1. Įrankių juostoje pasirinkite **Įrašyti**.
1. Įrankių juostoje pasirinkite puslapio **Atnaujinti** piktogramą.
1. „FastTab“ **Vietos nurodymo veiksmai** pasirinkite eilutę *TOPick*.
1. Įrankių juostoje **Vietos nurodymo veiksmai** pasirinkite **Perkelti žemyn**, kad pakeistumėte sekos numerį į didesnį nei ką tik sukurto veiksmo *Pagal LP* sekos numeris.

> [!NOTE]
> Strategija Pagal numerio lentelę bandys rezervuoti ir sukurti paėmimo darbą pagal vietas, kuriose yra pageidaujamos numerio lentelės, susijusios su perkėlimo užsakymo eilutėmis. Tačiau jei to padaryti negalima, o jūs vis tiek norite sukurti paėmimo darbą, turite grįžti į kitą vietos nurodymo veiksmų strategiją ir galbūt ieškoti atsargų kitoje sandėlio vietoje, atsižvelgdami į jūsų verslo proceso poreikius.

### <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Sandėlio programos įvykių apdorojimo paketinės užduoties konfigūravimas

Šiame skyriuje paaiškinama, kaip nustatyti suplanuotą paketinę užduotį norint apdoroti sandėlio programos įvykius.

1. Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Apdoroti sandėlio programos įvykius**.
2. Dialogo lange įjunkite **Paketinis vykdymas** dalyje **Vykdyti fone**.
3. Pasirinkite **Pasikartojimas** ir nustatykite paketinę užduotį, kuri bus vykdoma pagal jūsų verslui reikalingą intervalą.
4. Pasirinkite **Gerai**, norėdami sugrįžti į pagrindinį dialogo langą.
5. Pagrindiniame dialogo lange pasirinkite **Gerai**, kad įtrauktumėte užduotį į paketinių užduočių eilę.

### <a name="set-up-a-batch-job-to-release-transfer-orders-automatically"></a>Paketinės užduoties nustatymas siekiant automatiškai išleisti perkėlimo užsakymus

Šiame skyriuje paaiškinama, kaip nustatyti suplanuotą paketinę užduotį, kad būtų išleisti perkėlimo užsakymai, pažymėti kaip „Paruošti išleidimui”.

1. Eikite į **Sandėlio valdymas \> Išleidimas į sandėlį \> Automatinis perkėlimo užsakymų išleidimas**.
1. Dialogo lange išplėskite sekciją **Įtrauktini įrašai**.
1. Sekcijoje **Įtrauktini įrašai** pasirinkite **Filtruoti**.
1. Užklausos puslapio **WHSTransferAutoRTWQuery** skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad į užklausą būtų įtraukta nauja eilutė.
1. Naujos eilutės lauke **Lentelė** pasirinkite išplečiamąjį meniu ir pasirinkite lentelę **Perkėlimo eilutės išleidimas į sandėlį**.
1. Išplečiamajame meniu **Laukas** pasirinkite **Siunčiamos siuntos strategija**.
1. Lauke **Kriterijai** pasirinkite **Išleidimo ir siuntos patvirtinimas**.
1. Eilutės, kurioje **Laukas** nustatytas į *Iš sandėlio*, lauke **Kriterijai** pasirinkite *51*.
1. Pasirinkite **Gerai**, norėdami sugrįžti į pagrindinį dialogo langą.
1. Išplėskite sekciją **Vykdyti fone**, norėdami nustatyti paketinį vykdymą.
1. Įjunkite **Paketinis vykdymas** dalyje **Vykdyti fone**.
1. Pasirinkite **Pasikartojimas** ir nustatykite paketinę užduotį, kuri bus vykdoma pagal jūsų verslui reikalingą intervalą.
1. Pasirinkite **Gerai**, norėdami sugrįžti į pagrindinį dialogo langą.
1. Pagrindiniame dialogo lange pasirinkite **Gerai**, kad užduotis būtų įtraukta į paketinių užduočių eilę.

### <a name="set-up-the-process-outbound-shipment-batch-job"></a>Paketinės užduoties „Siunčiamos siuntos apdorojimas” nustatymas

Šiame skyriuje paaiškinama, kaip nustatyti suplanuotą paketinę užduotį norint vykdyti siunčiamų siuntų patvirtinimą, skirtą kroviniams, kurie paruošti siuntimui ir yra susiję su perkėlimo užsakymo eilutėmis, kurios „Paruoštos siuntimui”.

1. Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Išorės siuntimų apdorojimas**.
1. Išplėskite dalį **Įtrauktini įrašai**.
1. Pasirinkite **Filtras**.
1. Užklausoje **WHSLoadShipConfirm** pasirinkite skirtuką **Sujungimai**.
1. Išplėskite lentelių hierarchiją, kad būtų išplėstos dalys **Kroviniai** ir **Krovinio informacija**.
1. Pasirinkite lentelę **Krovinio informacija**.
1. Pasirinkite mygtuką **Įtraukti lentelės sujungimą**.
1. Lentelių ryšių sąrašo stulpelyje **Ryšys** filtruokite arba ieškokite *Perkėlimo užsakymo eilutės (nuoroda)*.
1. Suaktyvinkite lentelės ryšį sąraše ir paspauskite mygtuką **Pasirinkti**.
1. Pasirinkite lentelę **Perkėlimo užsakymo eilutės**.
1. Pasirinkite mygtuką **Įtraukti lentelės sujungimą**.
1. Lentelių ryšių sąrašo stulpelyje **Ryšys** filtruokite arba ieškokite *Papildomi atsargų perkėlimo laukai (Record-ID)*.
1. Suaktyvinkite lentelės ryšį sąraše ir paspauskite mygtuką **Pasirinkti**.
1. Pasirinkite skirtuką **Diapazonas**.
1. Užklausos lentelėse **Diapazonas** nustatysite tris užklausos kriterijų diapazonus. Pasirinkite mygtuką **Įtraukti**, norėdami įtraukti eilutę.
1. Įtraukite lentelės **Kroviniai** diapazoną. Nustatykite **Laukas** į *Krovinio būsena*, o **Kriterijai** – į *Pakrauta*.
1. Įtraukite kitą lentelės **Papildomi atsargų perkėlimo laukai** diapazoną. Nustatykite **Laukas** į *Siunčiamos siuntos strategija*, o **Kriterijai** – į *Išleidimo ir siuntos patvirtinimas*.
1. Įtraukite kitą lentelės **Krovinio informacija** diapazoną. Nustatykite **Laukas** į *Nuoroda*, o **Kriterijai** – į *Perkėlimo užsakymo siuntimas*.
1. Pasirinkite **Gerai**, norėdami sugrįžti į pagrindinį dialogo langą.
1. Išplėskite skyrių **Vykdyti fone**.
1. Įgalinkite **paketinį vykdymą**.
1. Pasirinkite **Pasikartojimas** ir nustatykite paketinę užduotį, kuri bus vykdoma pagal jūsų verslui reikalingą intervalą.
1. Pasirinkite **Gerai**, norėdami sugrįžti į pagrindinį dialogo langą.
1. Pagrindiniame dialogo lange pasirinkite **Gerai**, kad užduotis būtų įtraukta į paketinių užduočių eilę.

> [!NOTE]
> Daugiau informacijos žr. [Siunčiamų siuntų patvirtinimas naudojant paketines užduotis](confirm-outbound-shipments-from-batch-jobs.md).

## <a name="processing-the-example-for-create-transfer-order-from-the-warehouse-app"></a>Funkcijos „Kurti perkėlimo užsakymą iš sandėlio programos” pavyzdžio apdorojimas

### <a name="add-on-hand-on-a-license-plate"></a>Turimų atsargų įtraukimas į numerio lentelę

Pradedant šį scenarijų, jums reikia turėti numerio lentelę, kurioje yra faktinių turimų atsargų.

| Produktas | Sandėlis | Atsargų būsena | Buvimo vieta | Numerio lentelė | Kiekis |
| --- | --- | --- | --- | --- | --- |
| A0001 | 51 | Turima | LP-010 | LP10 | 1 |
| A0002 | 51 | Turima | LP-010 | LP10 | 2 |

Įtraukite faktinius turimus atsargų kiekius naudodami toliau pateiktas vertes.

> [!NOTE]
> Jums reikės sukurti numerio lentelę ir naudoti vietas, leidžiančias gabenti skirtingas prekes, pvz., LP-010.

### <a name="create-and-process-transfer-orders-from-the-warehouse-app"></a>Kurti ir apdoroti perkėlimo užsakymus naudojant sandėlio programą

1. Atidarykite programą ir prisijunkite kaip vartotojas *51*. Dabartinis vartotojo sandėlis bus 51.
1. Pasirinkite meniu elementą **TO kūrimas** iš meniu vietos, į kurią jį įtraukėte atliekant sąranką.
1. Pradėkite perkėlimo užsakymo kūrimą įvesdami paskirties sandėlį (Į sandėlį) lauke **Sandėlis**; įveskite *61*. Naujas perkėlimo užsakymas bus perkeltas iš dabartinio sandėlio 51 (Iš sandėlio) į paskirties sandėlį *61*.
1. Pasirinkite **Gerai**.
1. Nuskaitykite numerio lentelės ID lauke **Numerio lentelė**. Įveskite ankstesniame veiksme įtrauktų atsargų numerio lentelę *LP10*.
1. Pasirinkite **Gerai**.
1. Pasirinkite meniu mygtuką, tada pasirinkite **Užbaigti užsakymą**, norėdami užbaigti sandėlio programos perkėlimo užsakymo kūrimą.

Pirmiau pateiktame pavyzdyje naudojami du **sandėlio programos įvykiai** (*Kurti perkėlimo užsakymą* ir *Užbaigti perkėlimo užsakymą*).

### <a name="inquire-the-warehouse-app-events"></a><a name="#inquire-the-warehouse-app-events"></a>Užklausos dėl sandėlio programos įvykių pateikimas

Sandėlio valdymo mobiliųjų įrenginių programėlės sugeneruotą įvykių eilę ir įvykių pranešimus galite peržiūrėti nuėję į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Mobiliojo įrenginio žurnalai \> Sandėlio programos įvykiai**.

Įvykio *Sukurti perkėlimo užsakymą* pranešimų būsena taps *Laukiama*, o tai reiškia, kad paketinė užduotis **Apdoroti sandėlio programos įvykius** negaus ir neapdoros įvykio pranešimų. Atnaujinus įvykio pranešimo būseną į *Eilėje*, paketinė užduotis apdoros įvykius. Tai įvyks tuo pačiu metu, kai bus sukurtas įvykis *Užbaigti perkėlimo užsakymą* (darbuotojui pasirinkus mygtuką **Užbaigti užsakymą**, esantį sandėlio valdymo mobiliųjų įrenginių programėlėje). Apdorojus įvykio *Kurti perkėlimo užsakymą* pranešimus, būsena atnaujinama į *Baigta* arba *Nepavyko*. Kai *Užbaigti perkėlimo užsakymą* būsena atnaujinama į *Baigta*, visi susiję įvykiai panaikinami iš eilės.

Kadangi paketinė užduotis neapdoros **sandėlio programos įvykių**, skirtų perkėlimo užsakymo duomenims kurti, prieš atnaujinant pranešimus į būseną *Eilėje*, jums reikės ieškoti pageidaujamo perkėlimo užsakymo numerių kartu su lauku **Identifikatorius**. Laukas **Identifikatorius** yra puslapio **Sandėlio programos įvykiai** antraštėje.

Vykdant sandėlio įvykio apdorojimą, perkėlimo užsakymo eilutės kūrimas gali nepavykti. Tokiu atveju įvykio pranešimo būsena atnaujinama į *Nepavyko* ir galima naudoti **paketo žurnalo** informaciją norint sužinoti, kodėl taip atsitiko, bei ištaisyti problemas.

Įprastos problemos gali būti susijusios su trūkstama proceso sąranka, pvz., trūksta tranzito sandėlio, skirto įvykiui *Kurti perkėlimo užsakymą*. Tokiu atveju galite įtraukti tranzito sandėlį į siuntimo sandėlį ir naudoti parinktį **Nustatyti iš naujo**, kad pakeistumėte visų sandėlio programos įvykių pranešimų būsenas iš *Nepavyko* į *Eilėje*, o tai reiškia, kad paketinė užduotis apdoros įvykių pranešimus iš naujo po sąrankos duomenų pataisymo.

Gamybos aplinkose šios išimtys bus labiau susijusios su procesu, pvz., pageidaujamos numerio lentelės, kuri paketinės užduoties apdorojimo metu yra tuščia, todėl nesukuriamos perkėlimo užsakymo eilutės, turėjimu. Šis nepavykusio įvykio pranešimas gali būti pašalintas naudojant parinktį **Naikinti** arba galima į numerio lentelę įtraukti reikalingas faktines turimas atsargas ir visiems susijusių įvykių pranešimams taikyti parinktį **Nustatyti iš naujo**.

Daugiau informacijos žr. [Sandėlio programos įvykių apdorojimas](warehouse-app-events.md).

### <a name="follow-up-on-the-example-scenario-processing"></a>Scenarijaus pavyzdžio apdorojimo vykdymas

Šio scenarijaus metu įvyko toliau pateikti veiksmai.

1. Naudodami sandėlio valdymo mobiliųjų įrenginių programėlę, pasirinkote meniu elementą, naudojantį veiklos kodą **Kurti perkėlimo užsakymą iš numerio lentelių**.
1. Programa paragino jus pasirinkti perkėlimo užsakymo paskirties sandėlį. Šaltinio sandėlis visada yra tas, prie kurio šiuo metu esate prisijungę kaip darbuotojas.
1. Pasirenkant paskirties sandėlį, sistema rezervavo būsimo perkėlimo užsakymo ID numerį (pagal jūsų sistemoje nurodytą perkėlimo užsakymo numeraciją), bet dar nesukūrė perkėlimo užsakymo.
1. Nuskaitant numerio lentelę *LP10*, kurioje yra turimos atsargos, kurios turi būti perkeltos į naują sandėlį, **sandėlio programos įvykis** buvo įtrauktas į įvykių eilę, kad būtų apdorotas vėliau. Šiame sandėlio įvykyje buvo išsami pranešimo informacija apie nuskaitymą, įskaitant numatomą perkėlimo užsakymo numerį.
1. Sandėlio valdymo mobiliųjų įrenginių programėlėje pasirinkus mygtuką **Užbaigti užsakymą**, buvo sukurtas naujas sandėlio programos įvykis **Užbaigti perkėlimo užsakymą**, o susijusio esamo įvykio **Kurti perkėlimo užsakymą** būsena pakeista į **Eilėje**.
1. Vidiniame serveryje **paketinė užduotis Apdoroti sandėlio programos įvykius** gavo įvykį **Eilėje** ir surinko turimas atsargas, susijusias su nuskaityta numerio lentele. Remiantis turimomis atsargomis, buvo sukurtas faktinis perkėlimo užsakymo įrašas ir susietos eilutės. Užduotis taip pat užpildė perkėlimo užsakymo lauką **Siunčiamos siuntos strategija** konfigūruota reikšme *Išleidimo ir siuntos patvirtinimas* ir susiejo numerio lentelę pagal strategijos **Pagal numerio lentelę** eilutes.
1. Atsižvelgdama į perkėlimo užsakymo eilutės lauko **Siunčiamos siuntos strategija** reikšmę, **paketinės užduoties Automatinis perkėlimo užsakymų išleidimas** užklausa išleido perkėlimo užsakymą į siuntimo sandėlį. Be to, darbui buvo atlikti automatiniai apdorojimai dėl naudojamo **bangos šablono**, **darbo šablono** ir **vietos nurodymų** sąrankos, o **Krovinio būsena** buvo atnaujinta į *Pakrauta*.
1. Įvykdyta krovinio **paketinė užduotis Siunčiamos siuntos apdorojimas**, dėl kurios išsiųstas perkėlimo užsakymas ir sugeneruotas išankstinio siuntimo pranešimas (ASN).
1. Visų šių įvykių laikas priklauso nuo sukurtų paketinių užduočių parametrų **Pasikartojimas**.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="mobile-device-menu-item-setup"></a>Mobiliojo įrenginio meniu elemento nustatymas

#### <a name="why-cant-i-see-create-transfer-order-from-license-plate-in-the-menu-item-work-activity-drop-down-list"></a>Kodėl meniu elemento darbo veiklos išplečiamajame sąraše nematau „Sukurti perkėlimo užsakymą iš numerio lentelės”?

Funkcija *Kurti ir apdoroti perkėlimo užsakymus iš sandėlio programos* turi būti įjungta. Daugiau informacijos žr. [Perkėlimo užsakymų kūrimo iš sandėlio programos įjungimas](#enable-create-transfer-order-from-warehouse-app).

### <a name="warehouse-management-mobile-app-processes"></a>Sandėlio valdymo mobiliųjų įrenginių programėlės procesai

#### <a name="why-cant-i-see-the-menu-button-complete-order"></a>Kodėl nematau meniu mygtuko „Užbaigti užsakymą”?

Turite turėti bent vieną numerio lentelę, priskirtą perkėlimo užsakymui.

#### <a name="can-several-warehouse-management-mobile-app-users-add-license-plates-to-the-same-transfer-order-at-the-same-time"></a>Ar gali keli sandėlio valdymo mobiliųjų įrenginių programėlės vartotojai įtraukti numerio lenteles į tą patį perkėlimo užsakymą tuo pačiu metu?

Taip, keli sandėlio darbuotojai gali nuskaityti numerio lenteles į tą patį perkėlimo užsakymą.

#### <a name="can-the-same-license-plate-be-added-to-different-transfer-orders"></a>Ar galima tą pačią numerio lentelę įtraukti į skirtingus perkėlimo užsakymus?

Ne, numerio lentelę vienu metu galima įtraukti tik į vieną perkėlimo užsakymą.

#### <a name="after-having-selected-the-complete-order-button-can-i-then-add-more-license-plates-for-that-transfer-order"></a>Ar pasirinkus mygtuką „Užbaigti užsakymą” galima įtraukti daugiau to perkėlimo užsakymo numerio lentelių?

Ne, į perkėlimo užsakymą, kuriame yra sandėlio programos įvykis **Užbaigti perkėlimo užsakymą**, negalima įtraukti daugiau numerio lentelių.

#### <a name="how-can-i-find-existing-transfer-orders-to-be-used-via-the-select-transfer-order-button-in-the-warehouse-management-mobile-app-if-the-order-has-not-yet-been-created-in-the-backend-system"></a>Kaip rasti esamus perkėlimo užsakymus, kurie bus naudojami sandėlio valdymo mobiliųjų įrenginių programėlėje, naudojant mygtuką „Pasirinkti perkėlimo užsakymą”, jei užsakymas dar nesukurtas vidinio serverio sistemoje?

Naudodami duomenų užklausos galimybę, galite nustatyti, kad darbuotojai galėtų ieškoti perkėlimo užsakymų numerių sandėlio valdymo [mobiliojoje](warehouse-app-data-inquiry.md) programoje. Pavyzdžiui, galite sukurti atsieto mobiliojo įrenginio meniu elementą, kuris pateikia užklausas apie duomenis, [rodomus](warehouse-app-detours.md) žiniatinklio kliento sandėlio app įvykių puslapyje (**) kaip** užsakymo Select order - MobileDeviceQueueMessageCollectionIdentifierId`WHSMobileDeviceQueueMessageCollection` veiksmo dalį.*·* Perkėlimo užsakymo numeris atitinka vertę, rodomą lauke **Identifikatorius**. Taip pat žr [. užklausą dėl sandėlio programų įvykių](#inquire-the-warehouse-app-events).

#### <a name="can-i-manually-select-the-transfer-order-number-to-be-used-from-the-warehouse-management-mobile-app"></a>Ar galima rankiniu būdu pasirinkti perkėlimo užsakymo numerį, kuris bus naudojamas sandėlio valdymo mobiliųjų įrenginių programėlėje?

Palaikomi tik automatiškai sugeneruoti perkėlimo užsakymų numeriai naudojant numeracijas. Taip pat žiūrėkite atsakymą į ankstesnį klausimą, kaip nustatyti mygtuką **Pasirinkti perkėlimo** užsakymą. Daugiau informacijos apie perkėlimo užsakymo numerių ieškokite sandėlio [programų įvykių užklausoje](#inquire-the-warehouse-app-events).

### <a name="background-processing"></a>Foninis apdorojimas

#### <a name="how-should-i-clean-up-records-in-my-warehouse-app-events-queue-message-tables"></a>Kaip valyti mano sandėlio programos įvykių eilės pranešimų lentelėse esančius įrašus?

Juos galite peržiūrėti ir tvarkyti puslapyje **Sandėlio programos įvykiai**. Daugiau informacijos žr. [Užklausos dėl sandėlio programos įvykių pateikimas](#inquire-the-warehouse-app-events).

#### <a name="why-is-the-transfer-order-receipt-date-not-updated-according-to-my-delivery-date-control-setup"></a>Kodėl perkėlimo užsakymo „Gavimo data” nėra atnaujinta pagal mano „Pristatymo datos valdymas” nustatymą?

Perkėlimo užsakymai kuriami nenaudojant **Pristatymo datos valdymas** galimybių.

#### <a name="can-i-use-a-license-plate-having-physical-negative-inventory-on-hand"></a>Ar galima naudoti numerio lentelę, kurioje faktinės turimos atsargos yra neigiamos?

Ši priemonė palaiko tik teigiamus faktinius turimų prekių kiekius numerio lentelės lygiu, bet priskirdami numerio lentelę perkėlimo užsakymams galite turėti faktinius neigiamus kiekius aukštesniuose sandėlio ir atsargų būsenos lygiuose.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]