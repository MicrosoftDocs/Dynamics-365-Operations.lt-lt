---
title: Konteinerių pakavimas siuntimui
description: Šiame straipsnyje aprašomas pakavimo procesas, kuris leidžia tikrinti atsargų prekes ir pakuoti jas į konteinerius.
author: perlynne
ms.date: 7/13/2022
ms.topic: business-process
ms.search.form: WHSLocationType, WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup, WHSPack, WHSContainerTable,
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 118b1c79d23cd1b5044ede9aa9c469409cd22166
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708789"
---
# <a name="pack-containers-for-shipment"></a>Konteinerių pakavimas siuntimui

[!include [banner](../../includes/banner.md)]

Konteinerio pakavimo procesas leidžia tikrinti atsargų prekes ir pakuoti jas į konteinerius. Šio proceso metu sandėlio darbuotojai paprastai paima atsargų prekes iš buferio saugojimo sričių ir perkelia jas į pakavimo sritį. Ten keli sandėlio darbuotojai patikrina prekių kiekius ir tipus ir priskiria juos atitinkamiems konteinerių dydžiais. Visiškai supakuotas konteineris uždaromas ir perkeliamas į siuntos rampos sritį, kur jis paruoštas išsiųsti.

Konteineriai rodo faktines struktūras, kuriose yra supakuotos prekės, ir jūs galite sekti konteinerių informaciją sistemoje. Ši informacija gali būti naudinga planuojant transportavimą, ypač jei siuntimo išlaidas skaičiuojate pagal konteinerius. Prieš siųsdami galite peržiūrėti siuntoje naudojamų konteinerių skaičių, naudojamų konteinerių tipus ir faktines kiekvieno konteinerio dimensijas (pvz., bendrą tūrį ir svorį).

Keletas susijusių siuntimo sandėlio galimybių gali būti naudojamos su konteineriais. Daugiau informacijos ieškokite šiuose straipsniuose:

- [Bangos imas į konteinerius](wave-containerization.md)
- [Siunčiamas rūšiavimas](outbound-sorting.md)
- [Mažų siuntinių siuntimas](small-parcel-shipping.md)
- [Tvirtinimas ir perkėlimas](confirm-and-transfer.md)
- [Skirtingų pakavimo ir saugojimo dimensijų nustatymas](packing-vs-storage-dimensions.md)
- [Siunčiamų konteinerių pakavimo ir siuntų apdorojimo pakavimo darbas](packing-work.md)
- [Konteinerių pakavimas su sandėlio valdymo mobiliąją programa](warehouse-app-packing-containers.md)
- [Pavyzdis scenarijus – supakuoti konteinerius su sandėlio valdymo mobiliąją programa](warehouse-app-pack-containers-scenario.md)
- [Spausdinti konteinerių etiketes](print-container-labels.md)

## <a name="set-up-your-warehouse-to-use-manual-packing-operations"></a>Sandėlio, kad būtų galima naudoti pakavimo operacijas rankiniu būdu, nustatykite

Yra du pagrindiniai siuntimo operacijų tvarkymo būdai:

- **Bangos kūrimas ir apdorojimas** – darbuotojai išrinkti prekes pagal siunčiamo sandėlio darbą. Tada prekės padėti tiesiai į siuntimo vietą, kur jos paruoštos skubiam siuntimui. Informacijos, kaip nustatyti ir naudoti šį procesą, ieškokite bangos kūrimas [ir apdorojimas](wave-processing.md).
- **Rankinis pakavimas pakavimo** stotis – šio proceso metu tarp paėmimo ir siuntimo operacijų atliekama papildoma operacija. Užuot siųsdami atsargas į *durų siuntimo vietą*, darbuotojai padėti jas į *pakavimo vietą*. Tada jie valdo pakavimo procesą pakavimo stotis, **naudodami žiniatinklio** kliento pakavimo puslapį. Norėdami įgalinti šį procesą, turite sukonfigūruoti savo sistemą, kaip aprašyta šiame skyriuje.

### <a name="set-up-warehouse-locations-for-packing"></a>Nustatyti sandėlių vietas, skirtas pakavimui

Privalote turėti bent vieną pakavimo vietą, kurioje darbuotojai padės atsargų prekes, kad galėtų būti supakuoti konteineriuose. Daugiau informacijos apie sandėlio vietų kūrimo ieškokite Sandėlio, įjungto [WMS, vietų konfigūravimas](tasks\configure-locations-wms-enabled-warehouse.md). Toliau pateikti poskyriai aprašo, kaip sukurti ir nustatyti pakavimo vietas.

#### <a name="set-up-location-types-for-packing"></a>Nustatyti pakavimo vietų tipus

Turite nurodyti *pakavimo* vietų tipą. Vietų tipus galima naudoti kaip filtravimo parinktis, kad būtų galima kontroliuoti skirtingus sandėlio valdymo procesus. Kiekvienos vietos tipo pavadinimas paprastai apibūdina ką nors apie tai, kaip turėtų būti naudojamas tas vietos tipas. Čia nustatomas vietos tipas turi būti susietas su kiekviena vieta, naudojama pakavimo operacijoms.

Norėdami nustatyti vietos tipą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos tipai**.
1. Veiksmų srityje pasirinkite Naujas, kad **į** tinklelį įtraukumėte vietos tipą.
1. Nustatykite šiuos naujo vietos tipo laukus:

    - **Vietos** tipas – įveskite vietos tipo pavadinimą. Kiekvienas pavadinimas turi būti unikalus ir turi aprašyti ką nors apie tai, kaip turi būti naudojamas vietos tipas.
    - **Aprašymas** – įveskite trumpą vietos tipo aprašymą.

#### <a name="inform-the-system-about-the-packing-location-type"></a>Sistemos informacija apie pakavimo vietos tipą

Kai sukuriate vietos tipą, turite nustatyti, kad sistema pakavimo operacijoms būtų naudojamas kaip vietos tipas.

Norėdami nustatyti pakavimo operacijoms naudojamą vietos tipą, atlikite šiuos veiksmus.

1. Eiti į Sandėlio **valdymo nustatymas \> Sandėlio \> valdymo parametrai**
2. Skirtuko Bendra **skirtuko** Vietos tipai "FastTab" lauke Pakavimo vietos tipas nustatykite vietos tipą, **·** **kurį** naudosite pakavimo stotis nustatyti.

> [!NOTE]
> Jei atnaujinate Microsoft Dynamics AX iš versijos, *pakavimo* būsena buvo pašalinta iš siuntų ir krovinių, nes ji neveikė tinkamai ir sukėlė perteklinius duomenis. Todėl važtaraščio **puslapiuose** **esantys** pristatymai ir kroviniai yra pasenusi. Konteineriai, kuriuos reikia supakuoti, sekami vietos lygyje.
>
> Ankstesnėse versijose nurodėte **pakavimo vietą naudodami pakavimo vietos lauko šablono ID** **·** **·**, kuris yra sandėlio valdymo parametrų puslapio skirtuke Pakavimas, kad nurodydami vietos *šabloną.* Dabartinėje versijoje naudojate **lauką** **·** **Pakavimo vietos tipas, skirtuko Bendra puslapyje, sandėlio valdymo parametrų** *puslapyje*, kad nurodykite vietos tipą, kaip aprašyta šiame straipsnyje. Naujas laukas geriau sulygiuojamas su nustatymo vietų ir galutinių siuntimo vietų nustatymo procesu.
>
> **Nors pakavimo vietos laukui galite ir toliau naudoti seną šablono ID**, **rekomenduojame** pradėti naudoti naują pakavimo vietos tipo lauką, nes senas laukas galiausiai bus pasenęs.
>
> Jei išvalysite seno **pakavimo vietos lauko šablono** ID parametrą ir įrašysite puslapį, laukas bus visam laikui išjungtas. Diegimuose, kuriuose **pakavimo vietos lauko šablono** ID niekada nebuvo naudojamas, jis visada bus uždraustas. Išvalę pakavimo vietos **lauko šablono** ID parametrą, pakavimo vietai nustatyti ir identifikuoti naudokite šiame straipsnyje aprašytus parametrus.

#### <a name="set-up-location-profiles-for-packing-locations"></a>Nustatyti pakavimo vietų šablonus

Kiekvienas *vietos profilis* nustato informaciją ir taisykles, taikomas susijusioms vietas. Kadangi pakavimo operacijoms atlikti reikia bent vienos vietos, be vietos tipo, turite sukurti ir vietos šabloną. Kiekvieną profilį gali naudoti bet koks vietų skaičius. Norint sekti numerio lentelę reikia nustatyti pakuotei naudojamas vietas.

Norėdami nustatyti pakavimo vietos šabloną, atlikite šiuos veiksmus.

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Sandėlis \> Vietos profiliai**.
1. Pasirinkite esamą profilį iš sąrašo srities arba veiksmų srityje **pasirinkite** Naujas, kad sukurtumėte naują.
1. Naujo arba pasirinkto profilio antraštėje nustatykite šiuos laukus:

    - **Vietos šablono ID – įveskite unikalų profilio ID**.
    - **Pavadinimas** – įveskite aprašomąjį profilio pavadinimą.

1. „FastTab“ **Bendra** nustatykite toliau pateikiamus laukus.

    - **Vietos formatas** – pasirinkite dabartinės vietos formatą. Vietų formatai – tai pavadinimų sistema, naudojama kuriant unikalius ir nuoseklius skirtingų sandėlyje naudojamų vietos talpyklos pozicijų pavadinimus. Jei dar nėra reikia tipo, galite jį **sukurti nueiti į sandėlio valdymo nustatymo sandėlio \> vietos \>\> formatus**. Dėl išsamesnės informacijos, žr. [Konfigūruokite vietas WMS įjungtame sandėlyje](tasks/configure-locations-wms-enabled-warehouse.md).
    - **Vietos tipas** – pasirinkite vietos tipą, kuris **sandėlio** valdymo parametrų puslapyje nustatytas kaip pakavimo vietos tipas, kaip aprašyta anksčiau šiame straipsnyje.
    - **Naudoti numerio lentelės sekimą** – pakavimo vietų atveju nustatykite šią parinktį *kaip Taip*. Sistema turi sekti numerio lentelės NUMERIUS pakavimo vietose, kad galėtų valdyti pakavimo procesą.
    - **Leisti neigiamas atsargas** – pakavimo vietų atveju nustatykite šią pasirinktį kaip *Ne*.
    - **Leisti mišrias prekes** – pakavimo vietų atveju nustatykite šią pasirinktį kaip *Taip*. Šio parametro reikia todėl, kad daug skirtingų prekių numerių paprastai yra pateikiami į pakavimo vietas tuo pačiu metu.
    - **Leisti įvairių atsargų būsenas** – pakavimo vietose nustatykite šią pasirinktį kaip *Taip*. Šio parametro reikia todėl, kad prekės, kurių atsargų būsenos skiriasi, paprastai yra atvežios į pakavimo vietas tuo pačiu metu.
    - **Leisti įvairių atsargų paketus** – pakavimo vietose nustatykite šią pasirinktį kaip *Taip*. Ši pasirinktis automatiškai nustatoma kaip *Taip,* kai nustatyta **parinktis** Leisti mišrias prekes kaip *Taip*.

#### <a name="set-up-packing-locations"></a>Nustatyti pakuočių vietas

Privalote turėti bent vieną vietą *,* kur darbuotojai padės atsargų prekes, kurios turi būti supakuotos konteineriuose.

Norėdami įtraukti pakavimo vietą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Sandėlis \> Vietos**.
1. Veiksmų srityje pasirinkite Naujas, kad **įtraukumėte** vietą.
1. Nustatykite šiuos naujos vietos laukus:

    - **Sandėlis** – nurodyti sandėlį, kuriame turi būti pakavimo vieta.
    - **Vieta** – įveskite naujos vietos pavadinimą.
    - **Vietos šablono ID** – būtinai nurodykite ID, kurį sukūrėte ankstesniame skyriuje.

## <a name="set-up-the-packing-process"></a>Nustatyti pakavimo procesą

Šiame skyriuje aprašoma, kaip konfigūruoti parametrus, kurie įgalina pakavimo procesą ir leidžia darbuotojams pakuoti atsargas konteineriuose.

### <a name="set-up-container-packing-policies"></a><a name="packing-policy"></a>Nustatykite konteinerio pakavimo politiką

Kiekviena *konteinerio* pakavimo strategija apibrėžia, kaip turi būti apdorojamas konteineris. Kiekvieną kartą, kai sukuriate naują konteinerį, taip pat turėsite pasirinkti konteinerio pakavimo strategiją, kuri bus jai taikoma.

Norėdami nustatyti konteinerio pakavimo strategiją, atlikite toliau nurodytus veiksmus.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Talpyklos \> Talpyklos rūšiavimo politika**.
1. Pasirinkite esamą strategiją iš sąrašo srities arba veiksmų srityje **pasirinkite** Nauja, kad sukurtumėte naują.
1. Naujos arba pasirinktos strategijos antraštėje nustatykite tolesnius laukus.

    - **Konteinerio** pakavimo strategija – įveskite unikalų strategijos pavadinimą.
    - **Aprašas** – įveskite aprašomąjį strategijos pavadinimą.

1. Skirtuke **Peržiūra** nustatykite šiuos laukus. Šie laukai leidžia nurodyti, kokių veiksmų reikia imtis, kai konteineris uždaromas, ar turi būti dirbama su darbo sukūrimu, ar ne, ir kada konteineris turėtų būti paleistas iš pakavimo vietos.

    - **Sandėlis** – pasirinkite sandėlį, kuriame taikoma pakavimo strategija.
    - **Galutinės siuntos numatytoji** vieta – uždarius nurodyti pageidaujamą konteinerio vietą. Šis laukas galimas tik tada, kai laukas **Konteinerio** išleidimo strategija nustatytas *kaip Galimas galutinėje siuntimo vietoje*.
    - **Numatytoji rūšiavimo vieta** – šis laukas naudojamas su [siuntimo rūšiavimo](outbound-sorting.md) pajėgumais.
    - **Svorio vienetas** – pasirinkite numatytąjį matavimo vienetą, kuris bus naudojamas uždarius konteinerį ir jį padarius. Paprastai šis matavimo vienetas yra matavimo vienetas, naudojamas svarstyklių pakavimo vietovėje. Šis laukas taikomas strategijai su darbo sukūrimu ar be jo.
    - **Konteinerio uždarymo** strategija – pasirinkite vieną iš šių pasirinkčių, norėdami nustatyti, kas turėtų būti įvyks uždarius konteinerį:

        - *Automatinis paleidimas* – konteineris bus paleistas iš pakavimo stoties ir bus suaktyvintas veiksmas, **nurodytas** lauke Konteinerio išleidimo strategija.
        - *Uždelstas* paleidimas – konteineris nebus iš karto paleistas iš pakavimo vietos. Sandėlio darbuotojas rankiniu būdu turi jį paleisti vėliau.
        - *Pasirinktinai* – kol darbuotojas uždaro konteinerį, jis galės pasirinkti, ar reikia paleisti konteinerį.

        Jei pakavimo stotis tvarko daugiausia vieną konteinerius, kurie pristatomi tiesiogiai klientams, tinkamiausias būdas yra iš karto išleisti konteinerius. Jei pakavimo stotis tvarko siuntas, kurias sudaro keli konteineriai arba lygūs padėklai, greičiausiai geriausia atidėti paleidimą, kol visa siunta ar padėklas bus supakuotas ir parengtas paimti.

    - **Konteinerio išleidimo** strategija – pasirinkite vieną iš šių pasirinkčių, norėdami nurodyti, kas turėtų būti, kai konteineris išleidžiamas iš pakavimo vietos:

        - *Padaryti pasiekiamas galutinėje siuntimo vietoje* – atnaujinkite konteinerį į galutinę siuntimo vietą. Jei pasirinksite šią pasirinktį, **galutinės** siuntos lauke nurodykite pageidaujamą konteinerio vietą po to, kai ji bus uždaryta.
        - *Kurti darbą, perkeliant konteinerį* iš pakavimo vietos – kurti darbą, perkeliant konteinerį iš pakavimo vietos į išdėstymo vietą arba tiesiai į durys. Norėdami nurodyti **darbo šabloną**, kurį reikia taikyti kuriant konteinerio darbą, naudokite lauką Darbo šablonas.
        - *Priskirti konteinerį siuntimo rūšiavimo* pozicijai – ši pasirinktis naudojama [su siuntimo rūšiavimo](outbound-sorting.md) galimybe.

        Daugeliu atvejų rekomenduojame sukurti darbą, į kurį perkeliate konteinerius, nes šis būdas geriau atspindi faktinius neautomatinius procesus sandėlyje. Tačiau paprastais scenarijais arba situacijose, kai pakavimo stotis yra tiesiai durų srityje, galima rinktis, kad konteineris būtų nedelsiant prieinamas galutinėje siuntimo vietoje.

    - **Darbo šablonas** – pasirinkite darbo šabloną, kuris turėtų būti taikomas kuriant konteinerio darbą. Šis laukas **galimas** *·* *tik tada, kai konteinerio išleidimo strategijos laukas nustatytas kaip Kurti darbą, kad būtų galima perkelti konteinerį iš pakavimo vietos ir susijusį su darbo užsakymo tipu, kuris vadinamas Supakuoto konteinerio paėmimu.* Daugiau informacijos ieškokite darbo šablonų [ir vietos nurodymuose](control-warehouse-location-directives.md).

    Atlikite likusius veiksmus, sukonfigūruosite parametrus, susijusius su *deklaracija*. Deklaracija yra konteinerio, konteinerio grupės arba siuntos svorio nurodymo procesas ir iš transportavimo tiekėjo gautas sekimo ID. Dynamics 365 Supply Chain Management nėra integruotas su išorinio transportavimo teikėjo sistemomis. Sandėlio darbuotojai turi spausdinti žymas, gautas iš transportavimo teikėjo, ir tada, baigę deklaracijos procedūrą, nuskaityti sekimo numerį.

    Dėl to, kad deklaracijos reikalavimai skiriasi nuo kliento iki kliento, ir netgi nuo siuntos iki siuntos, pakavimo strategijos leidžia lankstumo darbo eigoje. Konteinerių, konteinerių grupių ir siuntų deklaracijas galite nustatyti bet kokiu deriniu.

    Jei naudojate kelių lygių deklaracijos procedūrą, darbuotojai, prieš reikšdami susijusią konteinerių grupę, turi parodyti visus konteinerius, tada, prieš reikšdami susijusią siuntą, turi parodyti visas konteinerių grupes.

1. Konteinerio **deklaracijos "** FastTab" nustatykite šiuos laukus:

    - **Automatinė deklaracija uždarant konteinerį** – nustatykite šią parinktį *kaip Taip*, jei norite taikyti deklaracijos informaciją kaip konteinerio uždarymo proceso dalį. Jei nenaudojate transportavimo integravimo, informaciją reikia įrašyti rankiniu būdu.
    - **Konteinerio deklaracijos reikalavimai** – pasirinkite vieną iš šių parinkčių:

        - *Nėra* – deklaracijos procesas nebus naudojamas.
        - *Neautomatinis* – pakavimo darbo eiga reikš, kad turi pateikti. Sistema neleidžia uždaryti arba išleisti konteinerio, kol nebus užbaigtas deklaracija.
        - *Transportavimo valdymas* – deklaracija bus deklaracija atliekama naudojant transportavimo valdymo (TMS) tarifų sistemą. Kadangi norint naudoti šią parinktį reikia pasirinktinio programavimo, kad būtų pritaikytas konkretus transportavimo teikėjo variklis, jis neišeis iš dabartinės versijos lango.

    - **Spausdinti konteinerio turinį** – nustatykite šią pasirinktį *kaip Taip,* jei norite automatiškai spausdinti konteinerio turinio ataskaitą, kai konteineris užregistruojamas kaip uždarytas. Ataskaitą galima spausdinti ir pagal poreikį.

1. Konteinerių **grupės deklaracijos "** FastTab" lauke **Konteinerių grupės deklaracijos reikalavimai** pasirinkite vieną iš šių pasirinkčių:

    - *Nėra* – konteinerių grupės deklaracija nebus įtraukta kaip pakavimo darbo eigos reikalavimas.
    - *Neautomatinis* – konteinerių grupės deklaracija bus įtraukta kaip pakavimo darbo eigos reikalavimas. Visi konteineriai, įtraukti į grupę, turi būti uždaryti prieš tai, kai grupė gali būti pateikta deklaracija. Pasirinkite šią parinktį, jei jums reikia užpildyti kiekvienos konteinerių grupės, supakuotos pakavimo stotis, deklaracijas. Paprastai jūs pasirenkate šią pasirinktį, jei konteineriai yra supakuoti ant padėklo ir visas padėklas yra parodytas.

    > [!NOTE]
    > Dabartinė versija nepalaiko konteinerių grupių deklaracijos ataskaitų ir nėra konteinerių grupių TMS modulio palaikymo.

1. Siuntos deklaracijos **"** FastTab" nustatykite šiuos laukus:

    - **Siuntimo deklaracijos reikalavimai –** pasirinkite vieną iš šių pasirinkčių:

        - *Nėra* – siuntos deklaracija nebus įtraukta kaip pakavimo darbo eigos reikalavimas.
        - *Neautomatinis* – siuntos deklaracija bus įtraukta kaip pakavimo darbo eigos reikalavimas. Jokie siuntos konteineriai negali būti išleisti, kol nebus baigtas deklaracijos siuntimas.
        - *Transportavimo valdymas* – deklaracija bus deklaracija naudojant TMS tarifų sistemą. Kadangi norint naudoti šią parinktį reikia pasirinktinio programavimo, kad būtų pritaikytas konkretus transportavimo teikėjo variklis, jis neišeis iš dabartinės versijos lango.

        Siuntos deklaracija turi būti įgalinta, jei jums reikia užpildyti visos siuntos, kuri supakuota pakavimo stotyje, deklaracijas. Paprastai naudojama, kai reikia vienos konsoliduotos deklaracijos, net jei siuntą sudaro keli konteineriai ar konteinerių grupės.

    - **Spausdinti važtaraštį** – nustatykite šią pasirinktį *kaip* Taip, jei norite automatiškai spausdinti važtaraštį kaip siuntos deklaracijos dalį. Važtaraštį galima išspausdinti ir pagal poreikį.

### <a name="set-up-container-types"></a>Konteinerių tipų nustatymas

Rankinio pakavimo proceso metu konteineriai turi būti sukurti prieš pakuojant jas prekes. Kiekvienas konteineris turi būti pagrįstas konteinerio *tipu*, kuris nurodo maksimalų tūrį ir svorio konteinerio tūrį.

Norėdami sukurti konteinerio tipą, atlikite šiuos veiksmus.

1. Eiti į sandėlio **valdymo nustatymą Konteinerių \>\>\> tipai.**
1. Norėdami įtraukti konteinerio tipą, veiksmų **srityje** pasirinkite Naujas.
1. Nustatykite šiuos naujo konteinerio tipo laukus:

    - **Konteinerio tipo** kodas – įveskite unikalų konteinerio tipo ID.
    - **Aprašas** – įveskite naujo konteinerio tipo aprašymą.
    - **Taros svoris** – įveskite faktinį arba įvertintą konteinerio svorį.
    - **Maksimalus grynasis svoris** – įveskite maksimalų svorį, kurį gali išlaikyti konteineris.

1. Dalies Konteinerio **dimensijos** laukuose **Ilgis**, **Plotis**, **Aukštis** ir Tūris **įveskite** paties konteinerio faktines dimensijas.
1. Skyriuje Maksimalus **kiekis, laukuose** **Ilgis,** **Plotis,** **Aukštis ir Tūris** **įveskite maksimalias faktines dimensijas**, kurias gali tvarkyti konteineris.
1. Galite apibrėžti papildomus konteinerių tipų, susietų su kitomis operacijomis, kurios naudoja konteinerius, atributus. Daugiau informacijos ieškokite Imas į [konteinerius](wave-containerization.md).

> [!NOTE]
> Rankinio pakavimo proceso metu sistema naudoja tik lauko Maksimalus grynasis svoris vertę ir lauko Tūris vertę, **·** **·** **kuri nurodyta skyriuje Maksimalios** vertės.

### <a name="set-up-packing-profiles"></a>Pakavimo profilių nustatymas

*Pakavimo procesui* reikia pakavimo šablonų. Juos galima pasirinkti arba nustatyti pagal numatytuosius nustatymus, kai pakavimo puslapyje pradedama **pakavimo** operacija.

Norėdami nustatyti pakavimo profilį, atlikite šiuos veiksmus:

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Pakavimas \> Pakavimo profiliai**.
1. Pasirinkite esamą profilį iš sąrašo srities arba veiksmų srityje **pasirinkite** Naujas, kad sukurtumėte naują.
1. Naujo arba pasirinkto profilio antraštėje nustatykite šiuos laukus:

    - **Pakavimo šablono ID – įveskite trumpą profilio ID**.
    - **Aprašymas** – įvesti pakavimo šablono aprašymą.
    - **Konteinerio** pakavimo strategija – pasirinkite pakavimo strategiją, kuri taikoma profiliui. Norėdami gauti daugiau informacijos, žr [. šio straipsnio skyrių Nustatyti konteinerio](#packing-policy) pakavimo strategijas.
    - **Konteinerio ID režimas** – pasirinkite, ar kuriant konteinerį automatiškai generuoti konteinerio ID, ar jį reikia sukurti rankiniu būdu.
    - **Konteinerio tipas** – pasirinkite konteinerio tipą, kuris pagal numatytuosius nustatymus naudojamas kuriant naują konteinerį.
    - **Automatiškai kurti konteinerį** uždaržius konteinerį – pažymėkite šį žymės langelį, norėdami automatiškai sukurti naują konteinerį, jei ankstesnis konteineris uždarytas ir viena ar daugiau eilučių lieka dabartinėje siuntoje.

### <a name="set-up-warehouse-workers"></a>Nustatyti sandėlio darbuotojus

Kiekvienas vartotojas **arba** *·* *darbuotojas*, kuris pakuojami konteinerius naudojantis žiniatinklio kliento pakavimo puslapiu arba sandėlio valdymo mobiliosios programos pakavimo veiklos kodu, turi turėti vartotojo abonementą, susietą su darbuotojo / asmens įrašu, kuriam priskirtos būtinos saugos prieigos teisės. (Daugiau informacijos apie tai, kaip nustatyti vartotojus, žr. [Kurti naujus vartotojus](../../fin-ops-core/dev-itpro/sysadmin/tasks/create-new-users.md).)

Norėdami nustatyti pakavimo proceso darbuotojo */ asmens* įrašą, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio tvarkymas \> Sąranka \> Darbuotojai**.
1. Veiksmų srityje pasirinkite Naujas, kad **įtraukumėte** darbo vartotoją.
1. Nustatykite **lauke Darbuotojas** esantį darbuotojo įrašą, **kuris** apibrėžtas vartotojo, kuris užbaigs pakavimo procesą, personalo modulyje.
1. „FastTab“ **Profilis** nustatykite toliau pateikiamus laukus:

    - **Konteinerio pakavimo strategija** – pasirinkite konteinerio pakavimo strategiją, kuri nustato, kaip pakavimo vietos konteineriai turi būti apdorojami. Jūsų pasirinkta konteinerio pakavimo strategija bus iš anksto pasirinkta darbuotojui, kai jis atidaro pakavimo stotį. Daugiau informacijos rasite toliau pateikiamame žurnalo skelbime: patobulintos [pakavimo funkcijos](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pakavimo šablono ID** – pasirinkite pakavimo šablono ID, kuris apibrėžia pakavimo strategiją ir konteinerio parametrus, kuriuos reikia naudoti. Jei pasirinktas pakavimo šablono ID yra susietas su konteinerio pakavimo strategija, **šiame puslapyje negalėsite** keisti lauko Konteinerio pakavimo strategija parametro.

1. Numatytoje **pakavimo stoties "** FastTab" pasirinkite darbuotojui taikykite numatytąją vietą, sandėlį ir vietą.
1. Jei darbuotojas naudos sandėlio valdymo mobiliąją programą savo konteinerių pakavimo darbui tvarkyti ir užregistruoti, **·** "FastTab" Vartotojai nustatykite vieną ar daugiau sąskaitų, kurias darbuotojas gali naudoti prisiregistruojate prie programos. Daugiau informacijos ieškokite mobiliojo įrenginio [vartotojo abonementuose](mobile-device-work-users.md).

## <a name="example-scenario"></a><a name="scenario"></a>Pavyzdinis scenarijus

Šiame skyriuje pateikiamas pavyzdis scenarijus, rodantis, kaip sukurti užsakymą ir supakuoti prekes.

### <a name="make-sample-data-available"></a>Įgalinkite duomenų pavyzdį

Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/fin-ops/get-started/demo-data.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

Kaip gamybos sistemos priemonę galite naudoti šį scenarijų kaip nurodymus. Nepaisant to, tokiu atveju, turėsite pakeisti savo vertes kiekvienam šiame dokumente aprašytam nustatymui.

### <a name="sign-in-as-a-user-that-can-do-packing-work"></a>Prisiregistruokite kaip vartotojas, galiis atlikti pakavimo darbą

Prisijunkite prie tiekimo grandinės valdymo, naudodami vartotojo abonementą, turiį teises, būtinas konteineriams pakuoti. *VartotojoVz., Funderburk* yra įtrauktas kaip demonstracinių duomenų dalis ir turi reikiamas teises. Šis vartotojas turi vartotojo ID *administravimą*.

### <a name="create-a-sales-order-and-complete-the-work"></a>Pardavimo užsakymo kūrimas ir darbo užbaigti

Norėdami sukurti pardavimo užsakymą ir užbaigti darbą, kai užsakytos prekės perkeliamos į pakavimo stotį, atlikite šiuos veiksmus.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite *US-005*.
1. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.
1. Naujas pardavimo užsakymas yra atidarytas ir yra viena, tuščia pardavimo užsakymo **eilučių** "FastTab" eilutė. Nustatykite šias naujo užsakymo eilutės vertes:

    - **Prekės numeris:** *A0001*
    - **Kiekis:** *2*
    - **Vieta:** *6*
    - **Sandėlis:** *62*

1. Kol užsakymo eilutė vis dar pasirinkta, Pardavimo **užsakymo eilučių \> "** FastTab" įrankių **juostoje pasirinkite Atsargų rezervavimas**.
1. Veiksmų srities puslapyje **Rezervavimas** pasirinkite **Rezervuoti partiją** rezervuoti visam pasirinktos eilutės kiekiui sandėlyje.
1. Uždarykite **Rezervavimo** puslapį, kad sugrįžtumėte į pardavimo užsakymą.
1. Veiksmų srities skirtuke **Sandėlis** pasirinkite **Išleisti į sandėlį**.

    Pranešimas rodo užsakymo siuntimo ir bangos SF.

1. Kol užsakymo eilutė vis dar pasirinkta, Pardavimo **užsakymo** \> **eilučių "** FastTab" įrankių juostoje **pasirinkite Sandėlio darbo** informacija. Jei savo bangoms vykdyti naudojate paketinį apdorojimą, gali tekti palaukti trumpą laiką, kol bus sukurtas darbas.
1. **Darbo puslapio** veiksmų srities skirtuke Darbas **pasirinkite** Baigti **darbą**.
1. Darbo užbaigimo **puslapyje** nustatykite vartotojo **ID** lauką *62*.
1. Veiksmų srityje pasirinkite Tikrinti **darbą**.
1. Kai gaunate pranešimą, nurodantį, kad jūsų darbas galiojantis, pasirinkite Baigti darbą, **kad** užbaigtumėte atsargų prekių paėmimo procesą ir įdėdami jas *į packų* vietą.
1. Pasižymkite siuntos **ID vertę**, kuri rodoma viršutiniame tinklelyje rodomai darbui.

### <a name="pack-the-ordered-items-into-a-container"></a>Supakuoti užsakytas prekes į konteinerį

Atsargų prekės buvo atvežtos į pakavimo sritį ir paruoštos pakuoti į konteinerius. Norėdami sistemoje sukurti naują konteinerį ir jį supakuoti, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio tvarkymas \> Pakavimas ir dėjimas į talpyklas \> Pakavimas**.
1. Dialogo lange **Pasirinkite pakavimo stotį** nustatykite šias vertes:

    - **Vieta:** *6*
    - **Sandėlis:** *62*
    - **Vieta:** *Pakavimas*
    - **Pakuotės šablono ID:** *WH62*

1. Pasirinkite **Gerai**.
1. Pakavimo **puslapyje**, numerio **lentelės arba siuntos lauke**, įveskite siuntos ID, kurį pažymėjote anksčiau. Dabar turėtumėte matyti likusias nesupakuotas prekes " **FastTab" Atidaryti** eilutes.
1. Veiksmų srityje pasirinkite Naujas konteineris **, kad** sistemoje sukurtumėte konteinerį.
1. Naujo konteinerio **dialogo lango** ID nustatykite konteinerio tipo **lauką** SmallBox *·*.
1. Norėdami sukurti **konteinerį**, pasirinkite Gerai.
1. Pasirinkite **Gerai,** jei norite grįžti į **pack** puslapį. Atidarytų **konteinerių** "FastTab" dabar **rodo konteinerio, kurį sukūrėte, konteinerio ID** vertę.
1. Šiuo atveju supakuoti tik vieną iš dabar užsakytus prekių. Todėl prekių pakavimo **"** FastTab" nustatykite šias vertes:

    - **Kiekis:** *1.00*
    - **Identifikatorius:** *A0001*

    Nedelsiant pasirinkę identifikatoriaus **vertę**, puslapis **atnaujina eilutes Atidaryti** **ir** Visos eilutės "FastTab", kad parodytų, jog viena prekė yra supakuota. Dabar turėtumėte supakuoti vieną iš dviejų prekės *A0001 vienetų*.

1. Veiksmų juostoje pasirinkite **Uždaryti talpyklą**.
1. Dialogo lange **Uždaryti konteinerį** pasirinkite Gauti sistemos svorį, **kad** būtų užpildyta numatytoji bruto **svorio** vertė.
1. Pasirinkite Gerai **,** jei norite uždaryti konteinerį.

> [!TIP]
> Yra įvairių konteinerių peržiūros būdų, atsižvelgiant į kontekstą. Pavyzdžiui, pakuojant siuntą dažnai naudinga peržiūrėti konteinerius, kurie yra siuntos dalis, arba visus konteinerius, kurie faktiškai yra pakavimo vietovėje. **Pakavimo stoties** puslapyje yra mygtukai, kuriuos galima naudoti norint peržiūrėti visus atidarytus ir uždarytus konteinerius pakavimo stotis. Šie rodiniai neapriboti konkrečia siunta. Tai gali būti labai naudinga tais atvejais, kai vienas darbuotojas pakuoja konteinerį ir kai kitas darbuotojas rodo ir išleidžia konteinerį.
>
> Taip pat galima naudoti konsoliduotą visų konteinerių rodinį. Šis rodinys dažniausiai naudingas vartotojams, kurie dirba už vienos pakavimo vietos konteksto ribų. Norėdami jį pamatyti, eikite į sandėlio **valdymo pakavimo \> ir konteinerių pakavimo į konteinerius \>**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
