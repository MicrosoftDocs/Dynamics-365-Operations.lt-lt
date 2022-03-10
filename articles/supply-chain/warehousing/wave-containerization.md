---
title: Krovimas į konteinerius
description: Šioje temoje aprašyta, kaip automatizuoti krovinių krovimą į konteinerius. Automatizuotas krovimas į konteinerius sukuria konteinerius ir paėmimo darbą siuntoms, kai apdorojama banga.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9293beba6a251a670b918fecbb2315a5e94660b9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572270"
---
# <a name="containerization"></a>Krovimas į konteinerius

[!include [banner](../includes/banner.md)]

Šioje temoje aprašyta, kaip automatizuoti krovinių krovimą į konteinerius. Automatizuotas krovimas į konteinerius sukuria konteinerius ir paėmimo darbą siuntoms, kai apdorojama banga.

Norėdami nustatyti krovimą į konteinerius, turite sukurti šiuos elementus:

- **Konteinerio tipas** – apibrėžkite fizines konteinerių savybes. Naudokite konteinerių tipus atsargų prekėms pakuoti į konkretaus tipo ir dydžio pakuotes, pavyzdžiui, talpyklas ar padėklus.
- **Konteinerių grupės** – kurkite panašių konteinerių tipų grupes. Pavyzdžiui, vienai konteinerių grupei gali priklausyti panašių dydžio matmenų konteinerių tipai. Konteinerių grupėje nurodoma seka, kuria pakuojami konteineriai ir kiekvieno konteinerio užpildymo procentas.
- **Konteinerio kūrimo šablonas** – kurkite šablonus, apibrėžiančius krovimo į konteinerius taisykles. Pavyzdžiui, atsargų maišymo taisykles ir kitas pakavimo strategijas.
- **Bangos šablonai** – nustatykite vieną ar kelis bangos šablonus, kad sukurtumėte krovimo į konteinerius išrinkimo darbą.

## <a name="create-wave-templates-for-containerization"></a>Krovimo į konteinerius bangos šablonų kūrimas

Krovimui į konteinerius turite nustatyti vieną arba kelius siuntimo bangos šablonus. Bangos šablonai apima kriterijus, kurie lemia šiuos aspektus:

- Kaip apdoroti bangas. Tai galima atlikti tiek rankiniu, tiek automatiniu būdu.
- Kaip sukurti paėmimo darbą. Tai priklauso nuo bangos metodų. Bangos šablonas turi apimti **krovimo į konteinerius** metodą.
- Kaip sugretinti prekių arba paskirstymo eilutes su banga.

Daugiau informacijos rasite [Bangos šablonai](wave-templates.md).

## <a name="create-container-types"></a>Konteinerio tipų kūrimas

Naudokite konteinerių tipus kurti konteinerių aprašus, įskaitant didžiausias fizinio dydžio matmenų ir svorio pajėgumo reikšmes. Apdorojus krovimo į konteinerius bangą, sukuriami konteineriai pagal konteinerio tipo informaciją.

Norėdami nustatyti konteinerio tipą, atlikite šiuos veiksmus:

1. Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerio tipas**.
1. Pasirinkite **Naujas**, kad sukurtumėte naują konteinerio tipą.
1. Įveskite konteinerio tipo unikalųjį identifikatorių (ID) ir aprašą.
1. Lauke **Taros svoris** įveskite faktinį arba numatomą konteinerio svorį.
1. Lauke **Maksimalus svoris** įveskite didžiausią svorį, kuris gali tilpti konteineryje.
1. Laukuose **Maksimalus konteinerio tūris**, **Maksimalus konteinerio ilgis**, **Maksimalus konteinerio plotis** ir **Maksimalus konteinerio aukštis** nurodykite faktines konteinerio dimensijas.

    > [!NOTE]
    > Ilgio ir pločio vertes galima sukeisti vietomis. Tai reiškia, kad prireikus galite pasukti prekes horizontaliai, arba aplink ašį x. Pavyzdžiui, jei ilgis yra 2 pėdos, o plotis 1 pėda, galite pakeisti ilgį į 1 pėdą, o plotį į 2 pėdas. Atkreipkite dėmesį, kad tai netaikoma aukščio matmeniui. Negalite keisti aukščio vertės norėdami pasukti prekę vertikaliai.

1. Atributų laukuose pasirinkite konteinerio pasirinktinių atributų reikšmes. Atributai yra pasirinktinės reikšmės, naudojamos prekėms filtruoti arba rikiuoti pagal reikšmę, kuri kitu atveju nėra pasiekiama. Pavyzdžiui, jei norite supakuoti prekes konkrečiam klientui, galite sukurti kliento pavadinimo atributą. Atributus kurkite **Konteinerio atributai** puslapyje.

## <a name="create-container-groups"></a>Konteinerių grupių kūrimas

Galite nustatyti logines konteinerių tipų grupes. Kiekvienai grupei galite nurodyti, kokia seka pakuoti konteinerius ir kokį procentą turi užpildyti konteineriai. Pagal prekės dydžio dimensijas nustatoma, ar prekė tilps į konteinerį. Naudojamas konteineris, artimiausias prekės dydžio matmenims. Jei grupėje turite kelis konteinerių tipus, rekomenduojame išdėstyti seką pagal dydį, kad didžiausias konteineris sekoje būtų pirmas (Nr. 1), o mažiausias – paskutinis.

Norėdami nustatyti konteinerių grupę, atlikite šiuos veiksmus:

1. Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerių grupės**.
1. Pasirinkite **Naujas**, kad sukurtumėte konteinerių grupę.
1. Įveskite konteinerių grupės unikalųjį ID ir aprašą.
1. „FastTab“ skirtuke **Išsami informacija** pasirinkite **Nauja** konteinerio tipo įtraukimui į grupę.
1. Lauke **Konteinerio tipas** pasirinkite konteinerio tipą.
1. Pasirinkite **Perkelti aukštyn** arba **Perkelti žemyn**, kad nurodytumėte seką, kuria bus pakuojami konteinerių tipai.

## <a name="create-container-build-templates"></a>Konteinerio kūrimo šablonų sukūrimas

Galite nustatyti krovimo į konteinerius proceso taisykles, pavyzdžiui, atsargų maišymo taisykles ir kitas pakavimo strategijas. Pavyzdžiui, galite nustatyti taisyklę, kad darbuotojai negalėtų pakuoti paskirstymo eilučių, kurios atitinka skirtingų klientų pardavimo užsakymus, esančius tame pačiame konteineryje.

Norėdami nustatyti konteinerio kūrimo šabloną, atlikite šiuos veiksmus:

1. Eikite į **Sandėlio valdymas** \> **Nustatymas** \> **Konteineriai** \> **Konteinerio kūrimo šablonas**.
1. Sukurkite naują konteinerio kūrimo šabloną.
1. Laukuose **Konteinerio pavadinimas** ir **Sekos numeris** įveskite krovimo į konteinerius šablono pavadinimą ir užsakymą, suderintą su paskirstymo eilutėmis.

    > [!NOTE]
    > Sistema naudos pirmą šabloną, kurio paskirstymo eilutė atitinka užklausos kriterijus. Todėl į sąrašo viršų nustatykite šabloną su konkrečiausiais kriterijais. Kuo bendresni kriterijai, tuo labiau tikėtina, kad paskirstymo eilutė atitiks kriterijus. Dėl šios priežasties eilutės gali būti priskirtos netinkamam konteineriui. Jei reikia, galite pasirinkti **Perkelti aukštyn** arba **Perkelti žemyn**, kad pakeistumėte šablonų seką.

1. Lauke **Konteinerių grupės ID** pasirinkite konteinerių grupę, iš kurios norite kurti konteinerius.
1. Lauke **Užklausos tipų pagrindimas** pasirinkite užklausos tipą, kuris lems, ką pakuoti ir kuo pagrįsti filtro užklausą. Galimos toliau nurodytos parinktys:

      - **Pardavimų paskirstymo eilutė** – pakuoti paskirstymo eilutes, sukurtas pardavimo užsakymams.
      - **Perkėlimo paskirstymo eilutė** – pakuoti paskirstymo eilutes, sukurtas perkėlimo užsakymams.
      - **Konteineris** – pakuoti konteinerį, kuris jau buvo sukurtas atliekant krovimo į konteinerius procesą. Pavyzdžiui, tai naudojama įdėjimo konteineriams.

        > [!NOTE]
        > Norėdami naudoti įdėjimo konteinerius, turite padaryti taip, kad būtų galima pakartoti krovimo į konteinerius metodą. Daugiau informacijos rasite [Bangos šablonai](wave-templates.md).

1. „FastTab“ skirtuko **Bendra** lauke **Bangos veiksmo kodas** įveskite bangos proceso metodo, kuris susieja konteinerio kūrimo šabloną su veiksmais bangos šablone, unikalųjį identifikatorių.
1. Pasirinkite žymės langelį **Leisti skaidyti paėmimus** tam, kad darbuotojai galėtų pakuoti darbo užsakymo prekes atskiruose konteineriuose. Tam reikia, kad visas kiekis tilptų konteineryje. Visada naudojamas didžiausias matavimo vienetas paskirstymo eilutėje.
1. Lauke **Pakuoti pagal vienetą** pasirinkite matavimo vienetą, kuris atitiks konteinerį. Pavyzdžiui, galite nurodyti, kad saugykla yra konteineris. Jeigu pakuojate pagal matavimo vienetą, negalite nurodyti ir konteinerių grupės, nes matavimo vienetas yra konteineris.
1. Lauke **Konteinerių pakavimo strategija** pasirinkite pakavimo strategiją, kurią naudosite. Galimos toliau nurodytos parinktys:

    > [!NOTE]
    > Strategija taikoma tik pardavimų ir perkėlimo paskirstymo eilutėms.

      - **Pakuoti į visus atvirus konteinerius** – sistema įvertina tai, ar paskirstymo eilutė tilps bet kuriame konteineryje, sukurtame krovimo į konteinerius ciklo metu.
      - **Pakuoti tik į dabartinį konteinerį** – sistema įvertina tik tai, ar paskirstymo eilutė tilps paskutiniame sukurtame konteineryje.

    Daugiau informacijos ir pavyzdžių, kurie parodo, kaip dirbti su konteinerio pakavimo strategijomis, ieškokite [Konteinerio pakavimo strategijos](container-packing-strategy-overview.md).

1. Norėdami nustatyti paskirstymo eilučių pakavimo konteineriuose taisykles, pasirinkite **Maišymo logikos skaidymas**. Pavyzdžiui, galite sukurti taisyklę, kuri leis darbuotojams pakuoti dviejų skirtingų prekių paskirstymo eilutes tame pačiame konteineryje. Norėdami apibrėžti maišymo taisyklę, atlikite šiuos veiksmus:

    1. Puslapyje **Maišymo logikos skaidymas** pasirinkite **Naujas**.
    1. Lauke **Lentelė** pasirinkite lentelę, kurioje yra laukas, naudojamas kaip maišymo logikos skaidymo kriterijus.
    1. Lauke **Lauko pasirinkimas** pasirinkite lauką, kuris bus naudojamas kaip maišymo logikos skaidymo kriterijus.
    1. Kartokite šiuos veiksmus, kol įtrauksite visus maišymo logikos skaidymo kriterijus.

    > [!NOTE]
    > Jei naudojate maišymo logiką, rekomenduojame rikiuoti pagal tuos pačius laukus filtro kriterijų užklausoje. Taip bus sukurta mažiau konteinerių.
