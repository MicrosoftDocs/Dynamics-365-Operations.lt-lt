---
title: Inžinerinių keitimų valdymo funkcijos gairės
description: Šiame straipsnyje pateikiamas pradžios ir pabaigos pradžios numeris, kuriame parodyta, kaip dirbti naudojant inžinerijos pakeitimų valdymą.
author: t-benebo
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 65ff30632a54b0b7cadbfe663698d466d41abe47
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334902"
---
# <a name="engineering-change-management-feature-walkthrough"></a>Inžinerinių keitimų valdymo funkcijos gairės

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamas pradžios ir pabaigos pradžios numeris, kuriame parodyta, kaip dirbti naudojant inžinerijos pakeitimų valdymą. Jos tinka visais svarbiausiais scenarijais:

- Pagrindinis funkcijos konfigūravimas
- Kaip inžinerijos bendrovė sukuria naują inžinerinį produktą
- Kaip inžinerijos bendrovė išleidžia inžinerinį produktą į vietinę bendrovę
- Kaip vietinė bendrovė gali peržiūrėti ir priimti produktą, kuris buvo išleistas į inžinerinę bendrovę
- Kaip vietinė bendrovė gali panaudoti inžinerinį produktą standartinėse perlaidose
- Kaip įtraukti inžinerinį produktą į prekybos užsakymą
- Kaip prašyti pakeitimų inžineriniam produktui sukuriant inžinerinio pokyčio užklausą
- Kaip suplanuoti ir įdiegti užklausos pakeitimus sukuriant inžinerinių keitimų užsakymą
- Kaip išleisti produktą, kuris buvo pakeistas

Visi šiame straipsnyje atlikti manai naudojami standartiniai pavyzdiniai duomenys, skirti "Microsoft"Dynamics 365 Supply Chain Management. Taip pat, kiekvienas praktikos kūrimas ankstesnėje praktinėje užduotyje. Dėl to, rekomenduojame jums dirbti per praktikas užsakyme nuo pradžios iki galo, ypač jei niekada nenaudojote inžinerinių keitimų valdymo funkcijas anksčiau. Tokiu būtu, visiškai suprasite funkciją.

## <a name="set-up-for-the-sample-scenario"></a>Nustatykite pavyzdžio scenarijų

Norėdami vadovautis pavyzdiniu scenarijumi, kuris pateiktas šiame straipsnyje, pirmiausia turite paruošti funkciją, kad būtų galima naudoti demonstracinius duomenis ir įtraukti keletą pasirinktinių įrašų.

Prieš bandydami atlikti bet kuriuos likusius šio straipsnio veiksmus, vadovaukitės visų toliau pateiktų poskyrių instrukcijomis. Šie poskyriai taip pat įtraukia keletą svarbių nustatymų puslapių, kuriuos naudosite nustatydami inžinerijos pokyčio valdymą savo organizacijai.

### <a name="make-standard-demo-data-available"></a>Padarykite standartinius demonstracinius duomenis prieinamus

Darbas sistemoje, kurioje įdiegti standartiniai [demonstraciniai](../../fin-ops-core/fin-ops/get-started/demo-data.md) duomenys. Standartiniai demonstraciniai duomenys įtraukia duomenis keliems demonstraciniams juridiniams asmenims (įmonėms ir organizacijoms). Kadangi dirbate per praktiką, naudosite įmonės parinkiklį dešinėje pusėje naršymo juostos, kad perjungtumėte tarp vienos bendrovės (*DEMF*) nustatytos kaip *inžinerijos organizacijos* ir kitos (*USMF*) kuri nustatyta kaip *veikianti organizacija*.

### <a name="set-up-an-engineering-organization"></a>Nustatykite inžinerijos organizaciją

Inžinerijos organizacijoje yra inžinieriniai duomenys ir ji atsakinga už produkto kūrimą ir keitimus. Norėdami nustatyti savo inžinerijos organizacijas, atlikite šiuos žingsnius.

1. Eikite į **Inžinerijos keitimo valdymą &gt; Nustatymus &gt; Inžinerijos organizacijos**.
1. Rinkitės **Naujas** tam, kad įtrauktumėte į tinklelį eilutę ir nustatytumėte tolesnes vertes jai:

    - **Inžinerijos organizacija:** *DEMF*
    - **Organizacijos pavadinimas:** *„Contoso Entertainment System Germany“*

    ![Įtraukite inžinerijos organizaciją.](media/engineering-org.png "Įtraukite inžinerijos organizaciją")

### <a name="set-up-the-version-product-dimension-group"></a>Nustatykite produkto matmenų grupės versiją

1. Eikite į **Produkto informacijos valdymą &gt; Nustatymai &gt; Matmenys ir varianto grupės &gt; Produkto matmenų grupės**.
1. Rinkitės **Naujas** tam, kad sukurtumėte produkto matmenų grupę.
1. Nustatykite **Pavadinimo** laukelį į *Versija*.
1. Rinkitės **Įrašyti** tam, kad įrašytumėte naujus matmenis ir įkeltumėte vertes į **Produkto matmenų** „FastTab“.
1. „FastTab“ **Produkto matmenys** nustatykite **Versija** kaip veikiančio produkto matmenis.

    ![Produkto matmenų grupės įtraukimas.](media/product-dimension-groups.png "Produkto matmenų grupės įtraukimas")

### <a name="set-up-product-lifecycle-states"></a>Nustatykite produkto gyvavimo ciklo būsenas

Kadangi inžinerijos produktas eina per savo gyvavimo ciklą, svarbu, kad galėtumėte valdyti, kurios perlaidos leidžiamos kiekvienoje gyvavimo ciklo būsenoje. Norėdami nustatyti produkto gyvavimo ciklo būsenas, atlikite šiuos žingsnius.

1. Eikite į **Inžinerijos keitimo valdymą &gt; Nustatymus &gt; Produkto gyvavimo ciklo būsena**.
1. Rinkitės **Naujas** tam, kad įtrauktumėte į gyvavimo ciklo būseną ir nustatytumėte tolesnes vertes jai:

    - **Būsena:** *Operacinė*
    - **Aprašas:** *Operacinė*

1. Rinkitės **Įrašyti** tam, kad įrašytumėte naują gyvavimo ciklo būseną ir įkeltumėte vertes į **Įjungti verslo procesai** „FastTab“.
1. „FastTab“ **Įjungti verslo procesai** pasirinkite verslo procesus, kurie turi būti prieinami. Šiame pavyzdyje palikite **Politika** laukelį nustatytą į *Įjungta* visiems verslo procesams.

    ![Verslo procesų įjungimas gyvavimo ciklo būsenai.](media/product-lifecycle-states-1.png "Verslo procesų įjungimas gyvavimo ciklo būsenai")

1. Rinkitės **Naujas** tam, kad įtrauktumėte kitą gyvavimo ciklo būseną ir nustatytumėte tolesnes vertes jai:

    - **Būsena:** *Prototipas*
    - **Aprašas:** *Prototipas*

1. Rinkitės **Įrašyti** tam, kad įrašytumėte naują gyvavimo ciklo būseną ir įkeltumėte vertes į **Įjungti verslo procesai** „FastTab“.
1. „FastTab“ **Įjungti verslo procesai** pasirinkite verslo procesus, kurie turi būti prieinami. Šiame pavyzdyje nustatykite **Politika** laukelį nustatytą į *Įjungta su įspėjimu* visiems verslo procesams.

    ![Verslo procesų įjungimas (su įspėjimais) gyvavimo ciklo būsenai.](media/product-lifecycle-states-2.png "Verslo procesų įjungimas (su įspėjimais) gyvavimo ciklo būsenai")

### <a name="set-up-a-version-number-rule"></a>Nustatykite versijos skaičiaus taisyklę

1. Eikite į **Inžinerijos keitimo valdymą &gt; Nustatymus &gt; Produkto versijos skaičiaus taisyklė**.
1. Rinkitės **Naujas** tam, kad įtrauktumėte į taisyklę ir nustatytumėte tolesnes vertes jai:

    - **Pavadinimas:** *Automatinis*
    - **Skaičiaus taisyklė:** *Automatinė*
    - **Formatas:** *V-\#\#*

    ![Įtraukite produkto versijos skaičiaus taisyklę.](media/version-number-rule.png "Įtraukite produkto versijos skaičiaus taisyklę")

### <a name="set-up-a-product-release-policy"></a>Nustatykite produkto išleidimo politiką

1. Eikite į **Inžinerijos keitimo valdymą &gt; Nustatymus &gt; Produkto leidimo politikos**.
1. Rinkitės **Naujas** tam, kad įtrauktumėte į leidimo politiką ir nustatytumėte tolesnes vertes jai:

    - **Pavadinimas:** *Komponentai*
    - **Aprašas:** *Komponentai*

1. „FastTab“ skirtuke **Bendra** nustatykite šias reikšmes:

    - **Produkto tipas:** *Prekė*
    - **Taikyti šablonus:** *Visada*
    - **Įjungta:** *Taip*

1. „FastTab“ **Visi produktai** rinkitės **Įtraukti** norėdami įtraukti eilutę tinklelyje ir nustatykite tolesnes vertes jai:

    - **Bendrovė:** *DEMF*
    - **Šablono leidimo produktas:** *D0006*

1. Rinkitės **Įtraukti** tam, kad įtrauktumėte kitą eilutę ir nustatytumėte tolesnes vertes jai:

    - **Bendrovės paskyrų ID:** *USMF*
    - **Šablono leidimo produktas:** *D0006*
    - **Gaukite KS:** Rinkitės šį žymimą laukelį.
    - **Kopijuokite KS tvirtinimą:** Rinkitės šį žymimą laukelį.
    - **Kopijuokite KS įjungimą:** Rinkitės šį žymimą laukelį.
    - **Gaukite maršrutą:** Rinkitės šį žymimą laukelį.
    - **Kopijuokite maršruto tvirtinimą:** Rinkitės šį žymimą laukelį.
    - **Kopijuokite įjungimo tvirtinimą:** Rinkitės šį žymimą laukelį.

    ![Įtraukite produkto išleidimo strategiją.](media/product-release-policy.png "Įtraukite produkto išleidimo politiką")

### <a name="set-up-an-engineering-product-category"></a>Nustatykite inžinerijos produkto kategoriją 

Inžinerinių produktų kategorijas pateikia pagrindą inžinerinių produktų kūrimui (tai yra, produktai su versijomis yra valdomi per inžinerijos keitimo valdymą). Norėdami nustatyti inžinerijos produktų kategorijas, atlikite šiuos žingsnius.

1. Eikite į **Inžinerijos keitimo valdymą &gt; Inžinerijos produkto kategorijų išsami informacija**.
1. Rinkitės **Naujas** tam, kad sukurtumėte kategoriją.
1. „FastTab“ **Išsami informacija** nustatykite šias vertes:

    - **Pavadinimas:** *Komponentai*
    - **Inžinerijos organizacija:** *DEMF*
    - **Produkto tipas:** *Prekė*
    - **Sekti versiją perlaidose:** *Taip*
    - **Produkto matmenų grupė:** *Versija*
    - **Produkto gyvavimo būsena kūrime:** *Operacinis*
    - **Versijos skaičiaus taisyklė:** *Automatinė*
    - **Vykdyti efektyvumą:** *Ne*
    - **Naudoti skaičiaus taisyklės nomenklatūrą:** *Ne*
    - **Naudoti pavadinimo taisyklės nomenklatūrą:** *Ne*
    - **Naudoti aprašo taisyklės nomenklatūrą:** *Ne*

1. „FastTab“ **Leidimo politika** nustatykite **Produkto leidimo politikos** laukelius į *Komponentai*.
1. Pasirinkite **Įrašyti**.

    ![Įtraukite inžinerijos produkto kategoriją.](media/product-category-details.png "Įtraukite inžinerijos produkto kategoriją")

### <a name="set-up-product-acceptance-conditions"></a>Nustatykite produkto priėmimo sąlygas

1. Naudokite įmonės parinkiklį dešinėje naršymo juostos pusėje, kad įjungtumėte *USMF* juridinį subjektą (bendrovę).
1. Eikite į **Inžinerijos keitimo valdymą &gt; Nustatymus &gt; Inžinerijos keitimo valdymo parametrai**.
1. Skirtuke **Leidimo valdymas** skyriuje **Produkto priėmimas** nustatykite **Produkto priėmimas** laukelį į *Rankinis*.

    ![Nustatykite produkto priėmimo sąlygas.](media/engineering-change-management-parameters.png "Nustatykite produkto priėmimo sąlygas")

## <a name="create-a-new-engineering-product"></a>Sukurkite naują inžinerijos produktą

Inžinerijos produktas yra produktas, kurio versija nustatoma ir jis valdomas per inžinerijos keitimo valdymą. Kitaip tariant, galite kontroliuoti keitimus per jo gyvavimą ir keisti informaciją, kuri bus įrašoma naudojant inžinerijos keitimo užsakymus. Norėdami sukurti inžinerijos produktus, atlikite šiuos žingsnius.

1. Įsitikinkite, kad esate inžinerinės organizacijos juridinio subjekto viduje (*DEMF* šiuo atveju). Naudokite įmonės parinkiklį dešinėje naršymo juostos pusėje, kaip būtina.
1. Atidarykite **Išleisti produktai** puslapį atlikdami vieną šių žingsnių:

    - Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**.
    - Eikite į **Inžinerijos keitimo valdymą &gt; Bendri &gt; Išleisti produktai**.

1. Veiksmų juostoje skirtuke **Produktas** grupėje **Naujas** pasirinkite **Inžinerijos produktas**.
1. Dialogo lange **Naujas produktas** nustatykite šias vertes:

    - **Inžinerijos produkto kategorija:** *Komponentai*
    - **Produkto numeris:** *Z0001*
    - **Produkto pavadinimas:** *Garsiakalbio rinkinys*

    ![Įtraukite inžinerijos produkto kategoriją.](media/new-product-dialog.png "Įtraukite inžinerijos produkto kategoriją")

    Atkreipkite dėmesį, kad **Versijos** laukelis yra automatiškai nustatomas naudojant produkto versijos skaičiaus taisyklę, kurią anksčiau nustatėte.

1. Pasirinkite **Gerai** tam, kad sukurtumėte produktą ir uždarytumėte teksto laukelį.
1. Išsamios informacijos puslapis naujam produktui atveriamas. Atkreipkite dėmesį, kad vertės yra užpildomos kai kuriems laukeliams, tokiems kaip **Talpinimo matmenų grupė**, **Sekimo matmenų grupė** ir (arba) **Prekės modelio grupė**. Šie laukeliai buvo automatiškai nustatyti dėl to, kad produktas išleistas *DEMF* juridiniame subjekte ir naudoja *Komponentų* produkto leidimo politiką *Komponentai* inžinerijos produkto kategoriją. Kadangi anksčiau naudojote prekę *D0006* kaip šabloną, kad nustatytumėte eilutę *DEMF* juridiniam subjektui, vertės užpildytos buvo paimtos iš prekės *D0006*.

    ![Patvirtinto produkto informacija.](media/product-details.png "Patvirtinto produkto informacija")

1. Tada veiksmų juostoje, skirtuke **Inžinierius** grupėje **Inžinerinių pakeitimų valdymas** grupėje, rinkitės **Inžinerinės versijos** tam, kad peržiūrėtumėte produkto versijas.

    ![Inžinerinės versijos.](media/engineering-versions-list.png "Inžinerinės versijos")

1. Puslapyje **Inžinerijos versijos** atkreipkite dėmesį, kad yra tik viena produkto versija ir ji įjungta.
1. Pasirinkite versiją, kad peržiūrėtumėte jos išsamią informaciją.

    ![Inžinerijos versijos išsami informacija.](media/engineering-version-details.png "Inžinerijos versijos išsami informacija")

1. Puslapio **Inžinerijos versija** „FastTab“ **Komplektavimo specifikacija** pasirinkite **Kurti KS**.
1. Teksto laukelyje **Kurti KS** nustatykite tolesnes vertes:

    - **KS numeris:** Z0001
    - **pavadinimas:** Garsiakalbio rinkinys
    - **Vieta:** 1

    ![KS kūrimas.](media/create-bom.png "KS kūrimas")

1. Rinkitės **Gerai** tam, kad įtrauktumėte KS ir uždarytumėte teksto laukelį.
1. „FastTab“ **Komplektavimo specifikacija** pasirinkite **Komplektavimo specifikacija**.
1. Puslapio **Komplektavimo specifikacija** „FastTab“ **Komplektavimo specifikacijos eilutės** įtraukite tris eilutes, kurių prekės numeriai yra *D0001*, *D0003*, ir *D0006*.

    ![KS eilučių įtraukimas.](media/bom.png "KS eilučių įtraukimas")

1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį.
1. Puslapio **Inžinerijos versija** „FastTab“ **Komplektavimo specifikacija** pasirinkite **Tvirtinti**.
1. Pasirodžiusiame dialogo lange pasirinkite **Gerai**.

    ![KS tvirtinimas.](media/approve-dialog.png "KS tvirtinimas")

1. Puslapyje **Inžinerijos versija** „FastTab“ **Komplektavimo specifikacija** rinkitės **Įjungti**.
1. Atkreipkite dėmesį, kad **Įjungtas** ir **Patvirtintas** žymimi laukeliai yra pasirinkti KS.

    ![Įjungtas ir patvirtintas KS.](media/approved-bom.png "Įjungtas ir patvirtintas KS")

1. Uždarykite puslapį.

## <a name="release-an-engineering-product-to-a-local-company"></a><a name="release"></a>Inžinerijos produkto leidimas į vietinę bendrovę

Produktas dabar buvo sukurtas inžinerijos skyriaus. Šiuo atveju produktas yra prototipas, kurį inžinerija sukūrė klientui. Kadangi klientas yra juridinio subjekto *USMF* klientas, produktas turi būti išleistas į jį.

1. Laikykite juridinį subjektą nustatytą į *DEMF*. (Naudokite įmonės parinkiklį dešinėje naršymo juostos pusėje, kaip būtina.)
1. Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**.
1. RInkitės produktą *Z0001*.
1. Veiksmų juostoje skirtuke **Produktas** , **Laikyti** grupėje, rinkitės **Leidžiamo produkto struktūra** kad atvertumėte **Leisti produktus** vedlį.
1. Puslapyje **Pasirinkite inžinerijos produktus išleidimu** rinkitės **Rinktis** žymimą laukelį produktui *Z0001*.

    ![Inžinerijos produktus išleidimui rodomi produktai.](media/select-eng-product-to-release.png "Inžinerijos produktus išleidimui rodomi produktai")

1. Pasirinkite **Leidimo išsami informacija**.
1. Puslapis pasirodo **Produkto leidimo išsami informacija** ir jame galite peržiūrėti išsamią produkto informaciją, kuris bus leidžiamas ir jo struktūrą. Atkreipkite dėmesį, kad **Siųsti KS** parinktis nustatyta į *Taip*. Dėl to, abu produktai *Z0001* ir jų vaikų prekės iš KS bus išleistos.

    Galite pasirinkti bet kurį vaiką prekę kairėje juostoje, kad peržiūrėtumėte išsamią informaciją. Jei bet kuri vaiko prekė turi KS, galite taip pat rinktis išleisti tos vaikų prekės KS.

    ![Leidžiamų produktų išsamios informacijos peržiūra.](media/product-release-details.png "Leidžiamų produktų išsamios informacijos peržiūra")

1. Užverkite puslapį, kad grįžtumėte į **Išleisti produktus** vedlį.
1. Rinkitės **Kitas** tam, kad atvertumėte **Pasirinkite inžinerijos produktus išleidimui** puslapį. Jei pasirinkote bet kurį standartinį (ne inžinerinį) produktą, jie pasirodys puslapyje. Pastebėkite, kad jums išleidžiant standartinį produktą pasirinkus  **Leisti produkto struktūrą**, jo KS ir maršrutas taip pat išleidžiami.

    ![Standartinio produktus išleidimui rodomi produktai.](media/select-std-product-to-release.png "Standartinio produktus išleidimui rodomi produktai")

1. Rinkitės **Kitas** tam, kad atvertumėte **Pasirinkite produkto variantai leidimui** puslapį. Šiam pavyzdžiui, nėra jokių variantų.
1. Rinkitės **Kitas** tam, kad atvertumėte **Pasirinkite įmonės** puslapį.
1. Pasirinkite įmones, kurioms produktas turi būti išleistas. Pavyzdžiui, pasirinkite žymimą laukelį **USMF**.

    ![Leidimo bendrovių pasirinkimas.](media/select-release-companies.png "Leidimo bendrovių pasirinkimas")

1. Rinkitės **Kitas** tam, kad atvertumėte **Tvirtinti pasirinkimą** puslapį.
1. Pasirinkite **Baigti**.

## <a name="review-and-accept-the-product-before-you-release-it-in-the-local-company"></a><a name="accept"></a>Peržiūrėti ir priimti produktą prieš jo leidimą į vietinę bendrovę

Inžinerijos skyrius dabar turi išleistą informaciją į vietines bendroves, kuriose produktas bus naudojamas. Šiam pavyzdžiui, vietinė įmonė yra *USMF*.

Kadangi nustatėte **Produkto priėmimo** laukelį į *Rankinis* puslapyje **Inžinerijos keitimo valdymo parametrai** įmonei *USMF* produktai turi būti rankiniu būdu priimti prieš jų leidimą į bendrovę. Kitaip tariant, jie turi būti peržiūrėti ir priimti prieš išleidimą.

Norėdami peržiūrėti produktą ir jį išleisti į *USMF* bendrovę, atlikite šiuos žingsnius.

1. Nustatykite juridinį subjektą į *USMF*. (Naudokite įmonės parinkiklį dešinėje naršymo juostos pusėje, kaip būtina.)
1. Eikite į **Inžinerijos keitimo valdymą &gt; Bendri &gt; Produkto leidimai &gt; Atverti produkto leidimus**.

    Puslapis **Atverti produkto leidimus** rodo produktą *Z0001*, kurio būsena yra *Laukia patvirtinimo*.

    ![Atidaryti produkto paleidimą.](media/open-product-releases.png "Atidaryti produkto paleidimą")

1. Rinkitės vertę **Produkto numerio** stulpelyje, kad atvertumėte **Produkto leidimo išsamios informacijos** puslapį. Atkreipkite dėmesį į tolesnę išsamią informaciją:

    - „FastTab“ **Bendri** rodo informaciją apie produkto leidimą, tokią kaip leidžianti bendrovė (*DEMF* šiuo atveju), leidimo saitas (*1*) ir leidimo saitas (*1*). Kadangi produktų paleidimo vedlyje **nenu** nurodėte gavimo svetainės, išleidžianti vietos vertė nukopijuojama į gavimo vietą.
    - „FastTab“ **Leidimo išsami informacija** rodo informaciją apie produktą ir jo leidimo versiją. Čia galite keisti nustatymus, tokius kaip efektyvumo datos.
    - „FastTab“ **Maršrutas** rodo produkto maršrutą. Nepaisant to, šiame pavyzdyje neišleidote jokių maršrutų.

    ![Produkto išleidimo informacija.](media/product-release-details-2.png "Produkto išleidimo informacija")

1. Jums pabaigus peržiūrėti informaciją, esate pasirengęs priimti produktą ir tokiu būtu jį išleisti į *USMF* bendrovę. Veiksmų juostoje rinkitės **Veiksmai &gt; Priimti**.
1. Produktas dabar išleistas į *USMF* bendrovę. Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Turite matyti prekę *Z0001*.

## <a name="use-the-product-in-transactions-in-the-local-company"></a>Naudokite produkto perlaidas vietinėje bendrovėje

Pagrindinių duomenų vadovas  *USMF* bendrovėje nori įsitikinti, kad produktas yra *Prototipo* būsenoje, kad įsitikintų, jog vartotojai bus įspėti, jei jie netyčia įtrauks jį į procesus, su kuriais jie dirba.

1. Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**.
1. Pasirinkite produktą *Z0001*, kad atvertumėte jo išsamios informacijos puslapį. (Tam, kad jį surastumėte naudokite filtrą.)
1. Veiksmų juostoje skirtuke **Inžinierius** grupėje **Inžinerinių keitimų valdymas** pasirinkite **Inžinerijos versijos**.
1. Puslapyje **Inžinerinės versijos** rinkitės versijos numerį *V-01* norėdami atverti jo išsamios informacijos puslapį.
1. Veiksmų juostoje skirtuke **Produkto** grupėje **Gyvavimo ciklo būsena** pasirinkite **Keisti gyvavimo ciklo būseną**.
1. Iškrentančiame teksto laukelyje **Keisti gyvavimo ciklo būseną** nustatykite **Būsenos** laukelį į *Prototipas* ir tada rinkitės **Gerai**.

    ![Gyvavimo ciklo būsenos keitimas.](media/change-lifecycle-state.png "Gyvavimo ciklo būsenos keitimas")

## <a name="add-the-engineering-product-to-a-sales-order"></a>Įtraukti inžinerinį produktą į prekybos užsakymą

Produktas dabar gali būti parduotas klientui. Siekiant įtraukti produktą į prekybos užsakymą, atlikite šiuos žingsnius.

1. Pasirinkite **Pardavimas ir rinkodara &gt; Pardavimo užsakymai &gt; Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Teksto laukelyje **Kurti prekybos užsakymą** nustatykite **Kliento paskyros** laukelį į *US-0002* ir tada rinkitės **Gerai**.
1. Naujas pardavimo užsakymas yra atidarytas. „FastTab“ **Prekybos užsakymo eilutės** įtraukite eilutę ir nustatykite **Prekės numerio** laukelį į *Z000*.
1. Veiksmų srityje pasirinkite **Įrašyti**.

    Gausite tolesnį įspėjimo pranešimą, kuris informuos jus, kad prekės būsena yra *Prototipas*. Nepaisant to, kadangi pranešimas tik įspėjamasis, prekybos užsakymas bus vis tiek sukurtas.

    ![Prekybos užsakymas inžinerijos produktui.](media/sales-order-eng-product.png "Prekybos užsakymas inžinerijos produktui")

## <a name="request-changes-in-the-engineering-product"></a>Prašykite pakeitimų inžinerijos produktui

Produktas buvo nusiųstas klientui, tačiau jis ne visiškai patenkintas ir pateikia atsiliepimą, kuris apima pagerinimo pasiūlymus. Klientui kalbant su pardavimo agentu telefonu, pastarasis gali paprašyti pakeitimų, kurių prašo klientas.

1. Pasirinkite **Pardavimas ir rinkodara &gt; Pardavimo užsakymai &gt; Visi pardavimo užsakymai**.
1. Suraskite ir atverkite prekybos užsakymą, kurį sukūrėte ankstesnėje praktikoje.
1. „FastTab“ **Prekybos užsakymo eilutės** rinkitės **Inžinerijos keitimo valdymas &gt; Nauja inžinerijos keitimo užklausa**.

    ![Inžinerijos keitimo užklausos kūrimas iš prekybos užsakymo.](media/sales-order-eng-change-request.png "Inžinerijos keitimo užklausos kūrimas iš prekybos užsakymo")

1. Užpildykite inžinerijos keitimo užklausą pagal kliento atsiliepimą. Šiam pavyzdžiui, nustatykite tolesnes vertes:

    - **Keisti užklausą:** *555*
    - **Pavadinimas:** *Z0001 kliento keitimas*
    - **Prioritetas:** *žemas*
    - **Kategorija:** nustatyti keitimą
    - **Sunkumas:** *Vidutinis*

1. „FastTab“ **Informacija** rinkitės **Naujas &gt; Pastaba** norėdami įtraukti pastabą į tinklelį.
1. Laukelyje **Aprašas** naujam pranešimui nurodykite, kad prekė *D0003* turi būti pašalinta iš KS. Jei turite įtraukti daugiau informacijos pastabai, galite įvesti tekstą **Pastabos** laukelyje.

    ![Inžinerinių pakeitimų užklausa.](media/eng-change-request.png "Inžinerinių pakeitimų užklausa")

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Atkreipkite dėmesį, kad prekė automatiškai įtraukiama į **Produktai** „FastTab“ ir kad šaltinis inžinerijos keitimo užsakymui (prekybos užsakymui) buvo įtrauktas į **Šaltinio** „FastTab“.

## <a name="make-changes-to-the-product-by-using-an-engineering-change-order"></a>Atlikite keitimus su produktu naudodami inžinerijos keitimo užsakymą

Prekybos agentas žino, kad produktas yra svarbus ir jis buvo sukurtas konkrečiai klientui. Dėl to, prekybos agentas paskambina inžinieriui *DEMF* bendrovėje siekiant pranešti jiems apie keitimo užklausą. Tokiu būdu, inžinierius gali pagreitinti procesą.

Inžinierius dabar peržiūri užklausą iš kliento ir sukuria keitimo užsakymą produktui.

1. Kadangi inžinierius dirba *DEMF* bendrovėje, nustatykite juridinį subjektą į *DEMF*. (Naudokite įmonės parinkiklį dešinėje naršymo juostos pusėje, kaip būtina.)
1. Eikite į **Inžinerinių pakeitimų valdymas &gt; Bendri &gt; Inžinerinių pakeitimų valdymas**.
1. Atverkite keitimo užklausą *555*.
1. Peržiūrėkite informaciją ir patvirtinkite keitimą. Veiksmų juostoje skirtuke **Keisti užklausą** grupėje **Keitimo būsenos** grupėje rinkitės **Tvirtinti**.
1. Eikite į **Inžinerinių pakeitimų valdymas &gt; Bendri &gt; Inžinerinių užsakymų pakeitimų**.
1. Veiksmų juostoje rinkitės **Naujas** tam, kad įtrauktumėte keitimo užsakymą ir nustatytumėte tolesnes vertes jam:

    - **Keisti užsakymą:** *555*
    - **Pavadinimas:** *Z0001 kliento keitimas*
    - **Kategorija:** *Kliento keitimas*
    - **Prioritetas:** *Žemas*
    - **Sunkumas:** *Vidutinis*

1. „FastTab“ **Paveikti produktai** rinkitės **Naujas &gt; Įtraukti esamą produktą** norėdami įtraukti eilutę tinklelyje ir nustatykite tolesnes vertes jai:

    - **Produktas:** *Z0001*
    - **Poveikis:** *Nauja versija*

    ![Inžinerijos keitimo užsakymo kūrimas.](media/eng-change-order.png "Inžinerijos keitimo užsakymo kūrimas")

1. Atkreipkite dėmesį, nes nustatėte **Poveikis** laukelį į *Nauja versija*, laukelis **Nauja versija** skirtuke **Išsami informacija** „FastTab“ **Produkto išsami informacija** rodo, koks naujos versijos numeris bus (*V-02* šiuo atveju).

    ![Išsami produkto informacija inžinerinių pakeitimų užsakymui.](media/eng-change-order-product-details.png "Išsami produkto informacija inžinerinių pakeitimų užsakymui")

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. „FastTab“ **Produkto išsami informacija** skirtuke **Komplektavimo specifikacija** pasirinkite **Eilutės** tam, kad atvertumėte KS produkto *Z0001* *V-01* versijai.

    ![Inžinerijos produkto KS eilutės.](media/eng-product-bom-lines.png "Inžinerijos produkto KS eilutės")

1. Parinkite eilutę prekės numeriui *D0003* ir tada veiksmų juostoje rinkitės **Šalinti**. Laukelio **Keisti tipą** vertė šiai eilutei keičiasi į *Naikinta*.
1. Veiksmų srityje pasirinkite **Įrašyti**.

    ![Pakeistos inžinerijos produkto KS eilutės.](media/eng-product-bom-lines-modified.png "Pakeistos inžinerijos produkto KS eilutės")

1. Uždarykite **KS eilutės** puslapį, kad grįžtumėte **Inžinerijos keitimo užsakymo** puslapį.
1. „FastTab“ **Išsami produkto informacija** skirtuke **Komplektavimo specifikacija** atkreipkite dėmesį, kad vertė **Keisti tipą** laukeliui KS *Z0001* dabar yra *Pakeista*.

    ![Inžinerijos pakeitimų užsakymas apimantis pakeistą KS.](media/eng-change-order-changed-bom.png "Inžinerijos pakeitimų užsakymas apimantis pakeistą KS")

    Užsakymas dabar turi būti patvirtintas prieš keitimų tvarkymą. Kai keitimai sutvarkyti, produktai yra naujinami su pakeitimais, kurie įtraukti į inžinerijos keitimo užsakymą. Šiame pavyzdyje, asmuo, kuris sukūrė inžinerijos keitimo užsakymą buvo nurodytas patvirtintojo.

1. Veiksmų juostoje skirtuke **Keisti užsakymą** grupėje **Keitimo būsenos** grupėje rinkitės **Tvirtinti**.
1. Rinkitės **Tvarkyti** norėdami atnaujinti produkto informaciją.

## <a name="release-the-changed-product"></a>Išleisti pakeistą produktą

Produktas dabar gali būti išleistas dar kartą į *USMF* bendrovę ir tada nusiųstas klientui. Norėdami išleisti produktą tiesiogiai iš inžinerijos keitimo užsakymo, atlikite šiuos veiksmus.

1. Atverkite inžinerijos keitimo užsakymą, kurį sukūrėte ankstesnėje praktikoje, jei jis dar nėra atvertas.
1. Veiksmų juostoje skirtuke **Keisti užsakymą** grupėje **Produkto leidimai** grupėje rinkitės **Ieškoti**.
1. Paieškos rezultatai rodo, kurių bendrovių paveikti produktai buvo išleisti. Užverti paieškos rezultatus.
1. Veiksmų juostoje **Keisti užsakymą** skirtuke **Produkto leidimai** grupėje rinkitės **Peržiūrėti** tam, kad atvertumėte **Leidimų** teksto laukelį, kuriame galite peržiūrėti ankstesnės paieškos rezultatus.
1. Pasirinkite visas bendroves, kurioms norite išleisti produktus.
1. Rinkitės **Gerai** tam, kad užvertumėte **Leidimų** teksto laukelį ir grįžtumėte į užsakymo keitimą.
1. Veiksmų juostoje, **Pokyčių užsakymas** skirtuke, grupėje **Produkto leidimai** rinkitės **Procesas** norėdami išleisti paveiktus produktus pasirinktoms bendrovėms. Kitu atveju, rinkitės **Leisti produkto struktūrą** tam, kad pradėtumėte leidimo procesą.

## <a name="complete-the-change-order"></a>Keitimo užsakymo baigimas

Kad keitimo užsakymą pažymėtumėte kaip atliktą (tai reiškia, kad nebereikia atlikti jokių tolesnių veiksmų), veiksmų srityje pasirinkite **Baigta**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
