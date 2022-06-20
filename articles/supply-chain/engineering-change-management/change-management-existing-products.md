---
title: Pakeitimų valdymo įjungimas esamiems produktams
description: Šiame straipsnyje paaiškinama, kaip įgalinti esamų produktų pakeitimų valdymą. Joje taip pat aprašomi atvejai, kuriais jūsų gebėjimas įjungti pakeitimų valdymą yra ribotas.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9f99529abebdf5490f158c6f0a7be4519449e9f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893474"
---
# <a name="enable-change-management-on-existing-products"></a>Pakeitimų valdymo įjungimas esamiems produktams

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip įgalinti esamų produktų pakeitimų valdymą. Joje taip pat aprašomi atvejai, kuriais jūsų gebėjimas įjungti pakeitimų valdymą yra ribotas.

Įgalinę esamo produkto pakeitimų valdymą, galite sukurti to produkto versijas ir sekti jo naudojimo metu atliktus keitimus. Todėl galite sekti šiuos pakeitimus naudodami keitimų užsakymus. Norėdami įgalinti pakeitimų valdymą, turite konvertuoti atitinkamus produktus į *inžinerijos prekes* (dar vadinamas inžinerijos produktais). Inžinerijos produktai – tai produktai, kurių versijos nustatomos ir kurie valdomi atliekant keitimų valdymą. Naudodamiesi vedliu pereisite per konvertavimo procesą.

## <a name="turn-this-feature-on-or-off"></a>Įjungti arba išjungti šią funkciją

Šiame straipsnyje aprašytos funkcijos reikalauja, kad jūsų *sistemoje būtų* *įjungtas* ir inžinerinio keitimo valdymas, ir esamų produktų keitimo valdymas. Išsamesnės informacijos apie šių funkcijų įjungimą ir išjungimą žr. Inžinerinių [pakeitimų valdymo peržiūra](product-engineering-overview.md).

## <a name="restrictions-and-limitations"></a>Suvaržymai ir apribojimai

Ne visus produktų tipus galima konvertuoti į visus kitus tipus. Taikomi šie suvaržymai ir apribojimai:

- Konvertuojant produktą į inžinerijos produktą, jis lieka *produktu*. Jis netampa *pagrindiniu produktu*.
- Kai konvertuojate bendrąjį produktą, kuris turi tam tikrą dimensijų rinkinį, tos dimensijos tvarkomos atlikus keitimą. Pavyzdžiui, jei konvertuojate bendrąjį produktą, kuris turi dydžio dimensiją, jis išlaikys dydžio dimensiją.

Todėl, jei turite išskirtąjį produktą, jį galite keisti tik į inžinerijos produktą, kuris operacijų metu neseka produkto dimensijos (t. y. jei versijos dimensija nėra naudojama). Daugiau informacijos apie šias problemas rasite likusiuose šio straipsnio skyriuose.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Pasirengimas konvertuoti sukuriant visas reikiamas inžinerijos produktų kategorijas

*Inžinerijos produktų kategorija* turi būti priskirta kiekvienam inžinerijos produktui. Šį priskyrimą padarysite paleisdami vedlį **Konvertavimas į inžinerinį produktą**. *Kad* būtų galima konvertuoti šiuos produktus, pirmiausia visiems atitinkamiems standartiniams produktams gali būti taikomos inžinerinių produktų kategorijos.

Inžinerijos produktų kategorija yra inžinerijos produkto kūrimo pagrindas, kuris apibrėžia numatytųjų verčių ir strategijų rinkinį. Inžinerijos atributai ir jų numatytosios reikšmės (apibrėžtos inžinerijos kategorijai) taip pat yra taikomos gaunamam inžinerijos produktui. Galite redaguoti atributo reikšmes ir (arba) įtraukti daugiau inžinerijos atributų į gaunamą produktą pagal poreikį.

Inžinerinio produkto kategorija turi sutapti su produktu, kuriam jį galite priskirti. Pavyzdžiui, produkto tipas ir dimensijų grupė turi atitikti ir produktą, ir gamybos produktų kategoriją. Dėl daugiau informacijos apie inžinerijos duomenis, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).

> [!IMPORTANT]
> Vedlys **Konvertuoti į inžinerijos produktą** produktą gali konvertuoti tik į tokius inžinerijos produktus, kurių versija nėra sekama operacijose. Todėl parinktį **Operacijų sekimo versija** reikia nustatyti kaip *Ne* inžinerijos produktų kategorijoms, kurias kuriate esamiems produktams konvertuoti.

Informacijos apie inžinerijos produktų kategorijų kūrimą žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Konvertavimo į inžinerijos produktų vedlio paleidimas

Vedlys **Konvertuoti į inžinerijos produktą** padeda konvertuoti vieną ar kelis esamus produktus į inžinerijos produktus. Jis produktus konvertuoja į inžinerijos produktus (produktų versijas), kai versija operacijų metu nėra sekama (t. y. jei versijos dimensija nenaudojama). Baigus konvertuoti, produktus galima valdyti naudojant inžinerijos pakeitimų valdymą.

Konvertavimas yra nuolatinis. Todėl vėliau jo atšaukti negalėsite. 

Kiekvienas konvertuotas inžinerijos produktas ir toliau bus išleidžiamas tose pačiose įmonėse, kuriose buvo išleistas pradinis produktas. Tačiau inžinerinė komplektavimo specifikacija (KS) ir maršrutai toms įmonėms nėra automatiškai išleidžiami.

Norėdami paleisti vedlį **Konvertuoti į inžinerijos produktą** ir konvertuoti produktą į inžinerijos produktą, atlikite nurodytus veiksmus.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Tinklelyje pasirinkite žymės langelį kiekvienam produktui, kurį norite konvertuoti.
1. Veiksmų srityje, skirtuke **Inžinierius** grupėje **Inžinerinių pakeitimų valdymas** pasirinkite **Konvertuoti į inžinerijos produktą**, kad atidarytumėte vedlį.
1. Pirmasis vedlio puslapis yra **Sveiki!**. Jei dar nesate susipažinę su konvertavimo procesu, atidžiai perskaitykite šiame puslapyje pateikiamą informaciją. Kai būsite pasirengę tęsti, pasirinkite **Toliau**.
1. Puslapyje **Pasirinkti produktų, kuriuos norite konvertuoti, duomenis** rodomas kiekvienas produktas, kurį pasirinkote prieš atidarydami vedlį. Patikrinkite sąrašą. Naudodami įrankių juostos mygtukus **Naujas** ir **Trinti** pridėkite arba pašalinkite reikiamus produktus.
1. Norėdami kiekvienam pateiktam produktui priskirti numatytąsias vertes, naudokite šiuos tinklelio viršuje esančius laukelius. (Pasibaigus konvertavimui, galėsite keisti šias atskirų produktų vertes.) Numatytosios vertės nebus priskirtos produktams, kuriems jau priskirta atitinkama vertė.

    - **Numatytoji inžinerijos kategorija** – pasirinkite pirminę inžinerijos produkto kategoriją, kurią norite priskirti kiekvienam išvardytam produktui. Jūsų pasirinkta kategorija bus taikoma tik su ja suderinamiems produktams.
    - **Numatytoji versija** – įveskite pradinę produkto versiją, kurią norite priskirti kiekvienam pateiktam produktui. Kiekvienam inžinerijos produktui priskirta bent viena inžinerijos versija.
    - **Numatytoji ciklo būsena** – pasirinkite pradinę produkto ciklo būseną, kuri bus priskirta kiekvienam išvardytam produktui.
    - **Dabartinė KS bus inžinerijos produkto dalis** – pažymėkite šį žymės langelį, jei kiekvieno išvardytų produktų dabartinė KS turi būti naudojama kaip inžinerijos produkto KS.

    Daugiau informacijos apie produkto parametrus ieškokite kitame veiksme.

1. Peržiūrėkite kiekvieną tinklelyje nurodytą produktą ir įvertinkite, ar gerai jam priskiriamos numatytosios vertės. Peržiūrėkite šią kiekvienos eilutės informaciją ir nustatykite atitinkamus laukelius:

    - **Produkto numeris** – produkto numeris.
    - **Produkto pavadinimas** – produkto pavadinimas.
    - **Inžinerijos kategorija** – pasirinkite inžinerijos produkto kategoriją, kuriai turėtų priklausyti produktas jį konvertavus. Kiekvienam produktui turi būti skirta atitinkama kategorija, kaip paaiškinta ankstesniame šio straipsnio skyriuje. Kiekvienam produktui turite priskirti kategoriją.
    - **Versija** – įveskite pradinę produkto versiją, kurią norite priskirti kiekvienam konvertuotam produktui. Pavyzdžiui, galite pasirinkti skaičių, atitinkantį jau naudojamos numeracijos numerį. Kiekviena inžinerijos versija talpina su inžinerija susijusius duomenis, kurie konkretūs tai versijai. Dėl daugiau informacijos apie inžinerijos duomenis, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).
    - **Produkto ciklo būsena** – pasirinkite produkto ciklo būseną, kurioje produktas turėtų būti jį konvertavus. Produkto ciklo būsena leidžia kontroliuoti, kurios operacijos leidžiamos duotai inžinerijos versijai. Dėl daugiau informacijos, žr. [Produkto gyvavimo ciklo būsenos ir perlaidos](product-lifecycle-state-transactions.md).
    - **Turi KS** – pažymėtas žymės langelis rodo, kad produktas turi KS. Šio žymės langelio nustatymas gali padėti nuspręsti, kaip žymės langelį **Dabartinė KS bus inžinerinio produkto dalis**.
    - **Dabartinė KS bus inžinerijos produkto dalis** – pažymėkite šį žymės langelį, jei produkto dabartinė KS turi būti naudojama kaip inžinerijos produkto KS. Šią KS tvarkys inžinerinio keitimo valdymas. Jei nėra produkto KS arba jei norite rankiniu būdu kurti konvertuoto produkto KS vėliau, išvalykite šį žymės langelį.
    - **Yra klaidų** – pažymėtas žymės langelis rodo, kad produkto nustatyme yra viena ar daugiau klaidų. Pavyzdžiui, produkto tipas arba dimensijų grupė gali nesutapti su kategorija. Produktai, kuriuose yra klaidų, bus praleisti ir nebus konvertuoti.

1. Baigę įrankių juostoje pasirinkite **Tikrinti** ir patikrinkite produkto sąranką. Kiekvienos eilutės žymės langelis **Yra klaidų** bus atnaujintas taip, kad būtų rodoma produkto būsena. Koreguokite vertes, kol kiekviename produkte nebeliks klaidų.
1. Tinkamai nustatę visus produktus, norėdami tęsti pasirinkite **Toliau**.
1. Puslapyje **Patvirtinti pasirinkimą** rodomas produktų, kurių sąrankoje nėra klaidų ir kurie yra paruošti konvertavimui, skaičius. Jame taip pat rodomas produktų, kurie dėl klaidų bus praleisti, skaičius. Kad konvertavimą paleistumėte į paketinę užduotį, parinktį **Paleisti pakete** į *Taip*.
1. Pasirinkite **Baigti**, kad pritaikytumėte parametrus ir pradėtumėte konvertuoti produktus į inžinerinius produktus.

> [!NOTE]
> Jei sistema nustatyta taip, kad rankiniu būdu priimtų produktus prieš juos išleidžiant, kiekvieną konvertuotą produktą reikia priimti naudojant puslapį **Atviras produktų išleidimas**. Daugiau informacijos žr. [Peržiūrėti ir priimti produktą prieš jo leidimą į vietinę bendrovę](engineering-scenarios.md#accept).
