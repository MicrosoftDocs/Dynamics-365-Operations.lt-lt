---
title: Įsigijimo tarp „Supply Chain Management” ir „Field Service” integracija
description: Šiame straipsnyje aprašoma, kaip dvigubo rašymo integravimas palaiko pirkimo užsakymo kūrimą ir atnaujinimus iš tiekimo grandinės valdymo ir laukų tarnybos.
author: RamaKrishnamoorthy
ms.date: 11/11/2020
ms.topic: article
audience: Application User
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d5a59365b3a524b8a5ec9e1e829fe181aa3d3660
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897150"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Įsigijimo tarp „Supply Chain Management” ir „Field Service” integracija

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

„Microsoft Dynamics 365 Supply Chain Management” leidžia naudotis patikimomis įsigijimo funkcijomis. „Dynamics 365 Field Service” siūlo panašias funkcijas, palaikančias pirkimo procesus, susietus su aptarnavimo procesu. Šių dviejų programėlių funkcijos integruojamos naudojant dvigubo rašymo funkciją, o gauti kryžminio naudojimo atvejai įgalinti lentelių susiejimuose, sprendimų logikoje, rodiniuose ir formose.

Ši integracija palaiko pirkimo užsakymų kūrimą ir, daugeliu atvejų, abiejų programėlių atnaujinimus. Tačiau „Supply Chain Management” kontroliuoja kainodarą, adresus ir produkto kvitą. Organizacijose, kurios naudoja ir „Field Service” ir „Supply Chain Management”, įgalinti keli galinga kryžminio naudojimo atvejai. Šie naudojimo atvejai įgalina įsigijimus inicijuoti ir sekti abiejose sistemose.

Toliau pateikta iliustracija rodo lenteles abiejose sistemose ir kaip jos susietos viena su kita. „Field Service” pirkimo užsakymai nurodo *sąskaita* eilutę, o tiekimo „Supply Chain Management” nurodo *tiekėjas* eilutę. Norint išspręsti integraciją, dvigubo rašymo funkcija naudoja nuorodą, kad susietų *tiekėjas* eilutes su *sąskaita* eilutėmis. Daugiau informacijos žr. [Integruotas tiekėjo šablonas](vendor-mapping.md).

![Įsigijimo susiejimai.](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami integruoti „Supply Chain Management” su „Field Service”, turite įdiegti šiuos komponentus:

- „Field Service” 8.8.31.60 arba naujesnė versija, skirta išsamesnei pirkimo užsakymų integracijai
- „Supply Chain Management“ 10.0.14 ar naujesnė versija
- Dvigubo rašymas „OneFSSCM” sprendimui įvykdyti

## <a name="installation-guidelines"></a>Diegimo rekomendacijos

### <a name="prerequisites"></a>Būtinieji komponentai

- **Dvigubas rašymas** – norėdami sužinoti daugiau žr. [Dvigubo rašymo pagrindinis puslapis](dual-write-home-page.md#dual-write-setup).
- **„Dynamics 365 Field Service”** – Daugiau informacijos žr. [„Dynamics 365 Field Service” įdiegimas](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Kai jos yra įgalintos „Microsoft Dataverse”, dvigubo rašymo funkcija ir „Field Service” pateikia kelis sprendimų sluoksnius, praplečiančius aplinką naujais metaduomenimis, formomis, peržiūromis ir logika. Šie sprendimai gali būti įgalinti bet kokia tvarka, tačiau paprastai juos diegiate čia pateikiama tvarka:

1. **„Field Service Common”** – „Field Service Common” įdiegiama, kai aplinkoje įdiegta „Field Service”.
2. **„Field Service (Anchor)”** – „Field Service (Anchor)” yra įdiegiama, kai aplinkoje įdiegta „Field Service”. 
3. **„Supply Chain Management Extended”** – „Supply Chain Management Extended” yra automatiškai įdiegiama, kai aplinkoje įgalintas dvigubas rašymas. 
4. **„OneFSSCM” sprendimas** – „OneFSSCM” automatiškai įdiegiamas pagal tai, kuris sprendimas („Field Service” ar „Supply Chain Management”) yra įdiegtas paskutinis.

    - Jei „Field Service” jau įdiegta aplinkoje ir įgalinate dvigubo rašymo funkciją, kuri įdiegia tiekimo grandinės „Supply Chain Management Extended”, įdiegiama „OneFSSCM”.
    - Jei „Supply Chain Management Extended” jau įdiegta aplinkoje, įdiegiate „Field Service”, „OneFSSCM” taip pat yra įdiegiama.

## <a name="initial-synchronization"></a>Pirminis sinchronizavimas

Norėdami sukurti naujus pirkimo užsakymus ir dirbti su esamais pirkimo užsakymais, turite sinchronizuoti nuorodos duomenis tarp „Supply Chain Management” ir „Dataverse”. Naudokite pradinę rašymo funkciją, norėdami aptikti lentelių ryšius ir rasti lenteles, kurias turite įgalinti duotas schemai.

Turite sinchronizuoti šias lenteles:

- Produktų šablonai

    Kai paleidžiate pradinį įrašą, gaunate visą reikalingų lentelių sąrašą. Toliau pateikiami keletas šablonų pavyzdžių:

    - Visi produktai
    - Išleisti produktai V2
    - „Dataverse“ išleisti išskirtieji produktai

- Vietos
- Sandėliai
- Įsigijimo kategorijų šablonai

    Toliau pateikiami keletas šablonų pavyzdžių:

    - Įsigijimo kategorijos
    - Pro
    - Produktų kategorijų hierarchija
    - Produktų kategorijos priskyrimai

- Tiekėjų šablonai, pvz., Tiekėjas V2
- Kontaktinių asmenų šablonai, pvz., „Dataverse” Kontaktai V2
- Darbuotojų šablonai, pvz., darbuotojas

Lentelių sinchronizavimas užtikrina, kad visi dokumentai, esantys „Supply Chain Management”, (pirkimo užsakymai ir gavimo kvitai) yra pasiekiami „Dataverse”.

### <a name="account-and-vendor-tables"></a>Sąskaitų ir tiekėjų lentelės

„Field Service” pirkimo užsakymai priklauso nuo sąskaitų lentelės, kad būtų sekami tiekėjai. Todėl pirkimo „Dataverse” užsakymų lentelės naudoja sąskaitas tiekėjams sekti. Norint suderinti šį pagrindinį skirtumą, reikia suaktyvinti šias keturias darbo eigas, kad sąskaitos ir tiekėjai būtų sinchronizuoti: 

- Tiekėjų kūrimas lentelėje „Sąskaitos”
- Tiekėjų kūrimas lentelėje „Tiekėjai”
- Tiekėjų naujinimas lentelėje „Sąskaitos”
- Tiekėjų naujinimas lentelėje „Tiekėjai”

Jei įdiegtas „OneFSSCM”, nes įdiegti ir „Field Service” ir „Supply Chain Management Extended”, šios darbo eigos suaktyvintos automatiškai. Jei „Field Service” neįdiegta, bet norite integruoti pirkimo užsakymų lenteles „Dataverse”, turite suaktyvinti šias darbo eigas. Abiem atvejais, nebent prasidedate nuo pradžių, prieš kuriant pirkimo užsakymus gali tekti užtikrinti, kad visi tiekėjai „Dataverse” būtų sukurti kaip sąskaitos. Priešingu atveju gali kilti klaidų.

### <a name="initial-synchronization"></a>Pirminis sinchronizavimas

Kai visos būtinosios sąlygos yra, jei norite, kad esami pirkimo užsakymai ir produkto kvitai būtų pasiekiami abiejose sistemose, turite atlikti šių šablonų pradinę sinchronizaciją:

- Pirkimo užsakymo antraštė V2
- CDS pirkimo užsakymo eilutė
- CDS pirkimo užsakymo eilutės negalutinis naikinimas
- Pirkimo užsakymo kvitas
- Pirkimo užsakymo kvito produktas

## <a name="mappings-with-logic"></a>Susiejimai su logika

Įsigijimo integravimas išplečia produkto susiejimą tokia logika, kad užtikrintų, jog **„Field Service” produktų tipas** stulpelis būtų teisingai susietas su produktų lentele „Dataverse”:

- Jei **Produkto tipas** nustatytas į *Produktas* ir **Prekės modelio grupė, laikomas produktas** nustatytas *True*, **„Field Service” produkto tipas** nustatyta į *Atsargos*.
- Jei **Produkto tipas** nustatytas į *Produktas* ir **Prekės modelio grupė, laikomas produktas** nustatytas *False*, **„Field Service” produkto tipas** nustatyta į *Nėra sandėlyje*.
- Jei **Produkto tipas** nustatytas į *Paslauga*, **„Field Service” produkto tipas** nustatytas į *Paslauga*.

Be to, „Dataverse” pateikiama logika, pagal kurią tiekėjai susieti su susijusiais sąskaitomis. Ši logika nustato numatytąją sąskaitos faktūros tiekėjo paskyrą. Kuriant serveryje papildinio logika nustato numatytąją sąskaitos faktūros tiekėjo sąskaitą iš tiekėjo, susijusio su paskyra. Tiekėjas turi nuorodą į sąskaitos faktūros paskyrą, kuris naudojamas šiai vertei nustatyti.

## <a name="supported-scenarios"></a>Palaikomi scenarijai

- Pirkimo užsakymus gali kurti ir atnaujinti „Dataverse” vartotojai. Tačiau procesą ir duomenis kontroliuoja „Supply Chain Management”. „Supply Chain Management” pirkimų užsakymų stulpelių naujinimų apribojimai taikomi, kai naujinimai ateina iš „Field Service”. Pavyzdžiui, negalima atnaujinti pirkimo užsakymo, jei jis buvo baigtas. 
- Jei pirkimo užsakymas kontroliuojamas „Supply Chain Management”, „Field Service” vartotojas gali atnaujinti pirkimo užsakymą tik tada, kai „Supply Chain Management” patvirtinimo būsena yra *Juodraštis*.
- Tik keli stulpeliai yra tvarkomi „Supply Chain Management” ir jie negali būti atnaujinti „Field Service”. Norėdami sužinoti, kurių stulpelių negalima atnaujinti, peržiūrėkite produkto susiejimo lenteles. Siekiant paprastumo, dauguma šių stulpelių yra nustatyta tik skaityti „Dataverse” puslapiuose. 

    Pvz., kainos informacijos stulpeliai yra valdomi „Supply Chain Management”. „Supply Chain Management” turi prekybos sutarčių, kurios gali būti naudingos „Field Service”. stulpeliai, pvz., **Vieneto kaina**, **Nuolaida**, ir **Grynasis kiekis** ateina iš „Supply Chain Management”. Norėdami užtikrinti, kad kaina yra sinchronizuojama „Field Service”, turėtumėte naudoti **Sinchronizuoti** funkciją **Pirkimo užsakymas** ir **Pirkimo užsakymo produktas** puslapius „Dataverse”, kai pirkimo užsakymo duomenys yra įvesti. Daugiau informacijos žr. [„Dynamics 365 Supply Chain Management” įsigijimo duomenų sinchronizacija pagal poreikį](#sync-procurement).

- **Bendra suma** stulpelis yra prieinamas „Field Service”, nes nėra „Supply Chain Management” pirkimo užsakymo bendrosios sumos. „Supply Chain Management” bendrosios sumos apskaičiuojamos remiantis keliais parametrais, kurių nėra „Field Service”.
- Pirkimo užsakymo eilutes, kuriose nurodyta tik įsigijimo kategorija arba kurių nurodytas produktas yra nurodytas kaip *Paslauga* produkto tipo ar „Field Service” produkto tipo prekė, gali būti inicijuotos tik „Supply Chain Management”. Tada eilutės sinchronizuojamos su „Dataverse” ir yra matomos „Field Service”.
- Jei įdiegta tik „Field Service”, o ne „Supply Chain Management”, pirkimo užsakyme **Sandėlis** stulpelis yra būtinas. Tačiau, jei „Supply Chain Management” yra įdiegta, šis reikalavimas nėra būtinas, nes „Supply Chain Management” leidžia naudoti pirkimo užsakymo eilutes, kai tam tikrose situacijose nenurodytas sandėlis.
- Produktų kvitai (pirkimo užsakymo kvitai „Dataverse”) yra tvarkomi „Supply Chain Management” ir negali būti sukurti iš „Dataverse”, jei įdiegta „Supply Chain Management”. Produktų kvitai iš „Supply Chain Management” yra sinchronizuojami „Supply Chain Management” į „Dataverse”.
- Pristatymo išlaidos leidžiamos „Supply Chain Management”. „OneFSSCM” suteikia logikos, kad kai produkto kvito eilutė (arba pirkimo užsakymo kvito produktas „Dataverse”) yra sukuriamas ir atnaujinamas, atsargų žurnalo eilutė sukuriama „Dataverse” likusiam kiekiui, kuris yra užsakyme tam tikrais pristatymo perviršio atvejais, konfigūruoti.

## <a name="unsupported-scenarios"></a>Nepalaikomi scenarijai

- „Field Service” neleidžia įtraukti eilučių į atšauktą pirkimo užsakymą „Supply Chain Management”. Kaip problemos sprendimą galite pakeisti pirkimo užsakymo sistemos būseną „Field Service”, tada įtraukti naują eilutę į „Field Service” arba „Supply Chain Management”.
- Nors įsigijimo eilutės paveikia atsargų lygius abiejose sistemose, ši integracija užtikrina atsargų suderinamumą „Supply Chain Management” ir „Field Service”. Abu „Field Service” ir „Supply Chain Management” turi kitus procesus, atnaujinančius atsargų lygius. Šie procesai nepatenka į įsigijimo sritį.

## <a name="status-management"></a>Būsenos valdymas

„Field Service” pirkimo užsakymų būsenos skiriasi nuo „Supply Chain Management” būsenų.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>„Field Service” pirkimo užsakymo ir pirkimo užsakymo produktų būsenos

| Antraštė – sistemos būsena | Antraštė – patvirtinimo būsena | Prekės būsena |
|---|---|---|
| <ul><li>Juodraštis</li><li>Pateikta</li><li>Atšaukta</li><li>Gautas produktas</li><li>Išrašyta sąskaita</li></ul> | <ul><li>Null</li><li>Aprobuota</li><li>Atmestas</li></ul> | <ul><li>Laukia</li><li>Gauta</li><li>Atšaukta</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>„Supply Chain Management” pirkimo užsakymo ir pirkimo užsakymo eilučių būsenos

Eilučių patvirtinimo būsenos yra aktyvios tik tada, kai yra eilutės darbo eiga.

| Antraštė – dokumentų būsena | Antraštė – patvirtinimo būsena | Eilutės būsena | Eilutės patvirtinimo būsena |
|---|---|---|---|
| <ul><li>Atviras užsakymas (užlaikytas užsakymas)</li><li>Gauta</li><li>Išrašyta SF</li><li>Atšaukta</li></ul> | <ul><li>Juodraštis</li><li>Peržiūrima</li><li>Aprobuota</li><li>Atmestas</li><li>Išorinės peržiūros režime</li><li>Pritarta</li><li>Baigta</li></ul> | <ul><li>Atviras užsakymas (užlaikytas užsakymas)</li><li>Gauta</li><li>Išrašyta SF</li><li>Atšaukta</li></ul> | <ul><li>Nepateikta</li><li>Peržiūrima</li><li>Aprobuota</li><li>Atmestas</li></ul> |

Būsenos stulpeliams taikomos šios taisyklės:

- „Supply Chain Management” būsena negali būti atnaujinta „Field Service”. Tačiau kai kuriais atvejais būsena „Field Service” bus atnaujinta, kai bus pakeista „Supply Chain Management” pirkimo užsakymo būsena.
- Jei „Supply Chain Management” ketinama keisti pirkimo užsakymą, o pakeitimas apdorojamas, patvirtinimo būsena *Juodraštis* arba *Peržiūra*. Šiuo atveju „Field Service” patvirtinimo būsena bus nustatyta kaip *Null*.
- Jei pirkimo užsakymo patvirtinimo būsena yra „Supply Chain Management” nustatyta į *Patvirtinta*, *Išorinės peržiūros režime*, *Patvirtinta* arba *Baigta*, „Field Service” pirkimo užsakymo patvirtinimo būsena bus nustatyta į *Patvirtinta*.
- Jei pirkimo užsakymo patvirtinimo būsena yra „Supply Chain Management” yra nustatyta į *Atmesta*, „Field Service” pirkimo užsakymo patvirtinimo būsena bus nustatyta į *Atmesta*.
- Jei dokumento antraštės būsena „Supply Chain Management” yra pakeista į *Atviras užsakymas (užlaikytas užsakymas)*, ir „Field Service” pirkimo užsakymo būsena yra *Juodraštis* arba *Atšaukta*, „Field Service” pirkimo užsakymo būsena bus nustatyta į *Pateikta*.
- Jei dokumento antraštės būsena „Supply Chain Management” pakeista į *Atšaukta* ir nėra pirkimo užsakymo kvito produktų „Field Service” yra susieti su pirkimo užsakymu (per pirkimo užsakymo produktus), „Field Service” sistemos būsena yra nustatyta į *Atšaukta*.
- Jei pirkimo užsakymo eilutės būsena „Supply Chain Management” yra *Atšaukta*, pirkimo užsakymo produkto būsena „Field Service” yra nustatyta į *Atšaukta*. Be to, jei pirkimo užsakymo eilutės būsena „Supply Chain Management” yra pakeista iš *Atšaukta* į *Užlaikytas užsakymas* pirkimo užsakymo produkto prekės būsena yra „Field Service” nustatyta į *Laukiama*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Sinchronizavimas su „Supply Chain Management“ įsigijimo duomenimis pagal poreikį

„Supply Chain Management” pateikiami įsigijimo duomenys, kurie apima sutartis, nuolaidas ir kitus scenarijus, paremtus antriniais „Supply Chain Management” procesais. Įsigijimo mechanizmas naudoja sudėtingas taisykles nustatyti geriausią konkretaus pirkimo užsakymo kainą. Naudojant dvigubo rašymo būseną, duomenys ne visada sinchronizuojami dviejose aplinkose, ypač scenarijuose, kuriuose eilutė buvo sukurta arba atnaujinta iš „Dataverse” ir gali įgalinti paskesnius procesus „Supply Chain Management”.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Sinchronizavimas su „Supply Chain Management“ įsigijimo duomenimis

1. „Dataverse” eikite į **Atsargos \>Pirkimo užsakymas**.
2. Pasirinkite **Nauja**, kad sukurtumėte naują pirkimo užsakymą arba pasirinktumėte esamo pirkimo užsakymo eilutę.
3. Iš pirkimo užsakymo arba pirkimo užsakymo eilutės.
4. Veiksmų srityje pasirinkite **Sinchronizuoti**.

Visi stulpeliai iš „Dataverse” ir „Field Service”, kuriuos bendrina „Supply Chain Management”, yra sinchronizuojami.

Štai situacijos, kai galite naudoti **Sinchronizuoti** funkciją:

- Jei iš eilės atliksite keletą paskesnių tos pačios eilutės „Dataverse”, paleiskite **Sinchronizuoti** funkciją.
- Jei nesate tikri, ar pakeitimas gali būti antrasis paskesnis pakeitimas iš „Dataverse”, praverstų paleisti **Sinchronizuoti** funkciją.
- Jei gaunate klaidos pranešimą apie vertės atnaujinimą iš „Supply Chain Management”, paleiskite **Sinchronizuoti** funkciją ir pakartokite atnaujinimą „Dataverse”.

## <a name="cancelling-the-posting-process"></a>Skelbimo proceso atšaukimas

Jei produkto kvito skelbimo procesas yra atšaukiamas apdorojimo metu, tada dvigubo rašymo metu gali būti sukurta produkto kvito eilutė „Dataverse”, bet ne sukuriama produkto kvito eilutė „Supply Chain Management”. Taip atsitinka, nes dvigubo rašymo operacija nepalaiko paskirstytų operacijų.

## <a name="templates"></a>Šablonai

Šiuose šablonuose pateikiama informacija apie su įsigijimu susijusių dokumentų integravimą.

| Tiekimo grandinės valdymas | „Field service“ | aprašymas |
|---|---|---|
| [Pirkimo užsakymo antraštė V2](mapping-reference.md#183) | msdyn\_Purchaseorders | Šioje lentelėje yra stulpelių, kuriuose pateikiama pirkimo užsakymo antraštė. |
| [Pirkimo užsakymo eilutės objektas](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | Šioje lentelėje yra eilučių, kuriuose pateikiamos pirkimo užsakymo eilutės. Produkto numeris naudojamas sinchronizacijos metu. Identifikuoja produktą kaip atsargų saugojimo vienetą (SKU), įskaitant produktų dimensijas. Daugiau informacijos apie produkto integravimą su „Dataverse” žr. [Vientisa produkto patirtis](product-mapping.md). |
| [Produkto gavimo antraštė](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | Šioje lentelėje pateikiamos produkto kvito antraštės, kurios sukuriamos, kai produkto kvitas yra paskelbtas „Supply Chain Management”. |
| [Produkto gavimo eilutė](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | Šioje lentelėje pateikiamos produkto kvito eilutės, kurios sukuriamos, kai produkto kvitas yra paskelbtas „Supply Chain Management”. |
| [Pirkimo užsakymo eilutės negalutinai sunaikintas objektas](mapping-reference.md#182) | msdyn\_purchaseorderproducts | Šioje lentelėje pateikiama informacija apie pirkimo užsakymo eilutes, kurios yra negalutinai panaikintos. Pirkimo užsakymo eilutę, esančią „Supply Chain Management”, galima negalutinai panaikinti patvirtinus pirkimo užsakymą arba patvirtinus tada, kai pakeitimų valdymas yra įjungtas. Eilutė egzistuoja „Supply Chain Management” ir yra pažymėta kaip **Panaikinta**. Nes „Dataverse” nėra negalutinio panaikinimo funkcijos, todėl svarbu šią informaciją sinchronizuoti „Dataverse”. Tokiu būdu negalutinai panaikintos eilutės „Supply Chain Management” gali būti automatiškai panaikintos iš „Dataverse”. Šiuo atveju eilutės panaikinimo „Dataverse” logika yra pateikta „Supply Chain Management Extended”. |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
