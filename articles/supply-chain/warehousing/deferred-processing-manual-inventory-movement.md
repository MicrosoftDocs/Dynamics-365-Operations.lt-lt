---
title: Atidėtas atsargų perkėlimo neautomatinis apdorojimas
description: Šiame straipsnyje aprašoma, kaip naudoti atidėtą neautomatinį atsargų judėjimo "Microsoft" apdorojimą Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9acacaddbde22d05d85ab9e11cd1d6de62337a6a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336402"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Atidėtas atsargų perkėlimo neautomatinis apdorojimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti atidėtą neautomatinį atsargų judėjimo "Microsoft" apdorojimą Dynamics 365 Supply Chain Management.

Atidėta apdorojimo funkcija leidžia sandėlio darbuotojams atlikti kitus darbus, o padėjimo operacija apdorojama fone. Atidėtas tvarkymas yra naudingas, kai serveris gali turėti retą arba neplanuotą apdorojimo laiko padidėjimą, o didesnis apdorojimo laikas gali turėti įtakos darbuotojo produktyvumui. Atsargų *perkėlimo darbo tipas dabar įtrauktas į darbo* tipų, kuriuos palaiko ši priemonė, rinkinį.

Fono apdorojimas pasiektas naudojant funkciją Apdoroti [sandėlio programos](warehouse-app-events.md) įvykius.

## <a name="turn-on-this-feature-for-your-system"></a>Šios funkcijos įjungimas sistemoje

Norėdami naudoti šią funkciją, įjunkite toliau nurodytą funkcijas [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Turite įjungti juos šia tvarka:

1. *Darbo blokavimas organizacijos mastu*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.21, ši funkcija yra privaloma ir jos išjungti negalima.)
1. *Apdoroti sandėlio programos įvykius*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima.)
1. *Atidėtos padėjimo operacijos*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima.)
1. *Atidėtas rankinio atsargų perkėlimo operacijos apdorojimas*<br>(Kaip ir tiekimo grandinės valdymo versija 10.0.25, ši funkcija yra privaloma ir jos išjungti negalima.)

## <a name="configure-the-work-processing-policies"></a>Darbo apdorojimo strategijų konfigūravimas

Norėdami naudoti atidėtą apdorojimą, turite sukonfigūruoti ir naudoti darbo apdorojimo strategiją. Norint atidėti padėjimo apdorojimą, sandėlio darbo funkcija palaiko šiuos darbo tipus: Pardavimo [užsakymas](deferred-put.md) *Perkėlimo* užsakymo *išdavimas* ir *Papildymas*. Atidėtas *neautomatinio atsargų perkėlimo operacijos* priemonių apdorojimas prideda naują darbo tipą: atsargų *perkėlimas*.

Norėdami nustatyti tvarkymo politiką, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymą \> Nustatymai \> Darbas \> Darbo tvarkymo politikos**.
1. Įveskite pasirinktą esamą politiką sąraše ar sukurkite naują politiką pasirinkdami **Naujas** veiksmų juostoje. Kiekvienos strategijos antraštėje yra šie laukai:

    - **Darbo tvarkymo politikos pavadinimas** - Darbo tvarkymo politikos pavadinimas.
    - **Aprašas** - Darbo tvarkymo politikos aprašas. 

1. Apdorojimo **taisyklių** „FastTab" nustatykite taisyklių, kurios bus taikoma strategija, rinkinį. Naudokite tolesnius mygtukus įrankių juostoje, kad įtrauktumėte ar pašalintumėte taisykles. Nustatykite šiuos kiekvienos taisyklės laukus:

    - **Darbo užsakymo tipas** – pasirinkite darbo tipą, kurį strategija taiko.
    - **Operacija** – pasirinkite operaciją, kurią strategija naudojama apdoroti. Jei pasirinkote atsargų judėjimą darbo užsakymo tipo lauke, jums nereikia nustatyti šio lauko, nes išrinkimo operacijos ir padavimo operacijos apdorojamos *kaip* vienas **įvykis**.
    - **Darbo** apdorojimo metodas – pasirinkite metodą, naudojamą darbo eilutei apdoroti. Jei pasirenkate *Nedelsiant*, elgesys primena elgesį, kai eilučių apdorojimui nėra naudojamos jokios darbo apdorojimo strategijos. Jei pasirenkate *Atidėta*, sistema taikys atidėtą apdorojimą, kuris naudoja paketinę sistemą.
    - **Atidėta apdorojimo** ribinė vertė – jei šį lauką *nustatote kaip 0* (nulį), ribinės vertės nėra. Tokiu atveju, naudojamas apdorojimo metodas *Atidėtas*, jei įmanoma. Jei konkrečios ribinės reikšmės skaičiavimas yra žemesnis už ribinę reikšmę, naudojamas metodas *Nedelsiant*. Priešingu atveju naudojamas *atidėtasis* metodas, jei jį galima naudoti. Su pardavimu ir perkėlimu susijusiam darbui, ribinė reikšmė apskaičiuojama kaip susieto šaltinio įkėlimo eilučių, kurios apdorojamos darbui, skaičius. Papildymo darbams ribinė reikšmė apskaičiuojama kaip darbo eilučių, kurias papildo darbas, skaičius. Nustatydami ribinę reikšmę, pvz., *5*, pardavimams, kuriuose užtikrinate mažiau nei penkias pradinio šaltinio įkėlimo eilutes, nebus naudojamas atidėtas apdorojimas, tačiau jį naudos didesni darbai. Ribinė reikšmė taikoma tik tada, kai darbo **apdorojimo metodas nustatytas** laukelis nustatytas į *Atidėtas*.
    - **Atidėto apdorojimo** paketų grupė – nurodykite paketų grupę, kuri naudojama apdoroti. Jei lauke Darbo užsakymo tipas pasirinkote Atsargų perkėlimas, šio lauko nustatyti nereikia, nes apdorojimo sandėlio programos įvykių *dialogo* lange **pasirinkta** paketų **grupė**.

## <a name="assign-the-work-creation-policy"></a>Priskirkite darbo kūrimo poltiką

Daugiau informacijos apie darbo kūrimo strategijos priskyrimą ieškokite Atidėtas [sandėlio darbo](deferred-put.md) apdorojimas.

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Sandėlio programos įvykių apdorojimo paketinės užduoties konfigūravimas

Norėdami naudoti *atidėtą neautomatinio atsargų perkėlimo operacijos proceso* apdorojimą, nustatykite suplanuotą paketinę užduotį.

1. Eikite į **Sandėlio valdymas \> Periodinės užduotys \> Apdoroti sandėlio programos įvykius**.
1. Dialogo lango **Tvarkymo sandėlio programos įvykių** „FastTab” **Paleisti fone** nustatykite parinktį **Paketinis vykdymas** į *Taip*.
1. Pasirinkite **Pasikartojimas** ir nustatykite vykdymo grafiką, kuris atitinka jūsų verslo poreikius.
1. Rinkitės **OK** kiekviename teksto laukelyje.

## <a name="inquire-about-the-warehouse-app-events"></a>Užklausos apie sandėlio programos įvykius

Sandėlio programos sugeneruotą įvykių eilę ir įvykio pranešimus, kuriamos programos, nuėję į **Sandėlio valdymas \> Užklausos ir ataskaitos \> Mobiliojo įrenginio žurnalai \> Sandėlio programos įvykiai**.

Atsargų *perkėlimo įvykio pranešimų būsena bus* Darbo *eilėje, kai jie bus sukurti pirmą* kartą. Ši būsena rodo, kad **Tvarkymo sandėlio programos įvykių** paketo darbas paims įvykio pranešimus ir juos sutvarkys. Kai Užbaigti perkėlimo užsakymą būsena atnaujinama į *Baigta* visi susiję įvykiai panaikinami iš eilės.

Visi atsargų *perkėlimo įvykiai* kaupiami po vieną vieno įvykio tipo ir sandėlio rinkinį.

Paketinė užduotis apdoros sandėlio programos įvykius pagal pasikartojimą, nustatytą dialogo lange Apdoroti **sandėlio programos** įvykius. Todėl, kol bus apdorotas pranešimas, sandėlio ID galėsite rasti lauke **Identifikatorius**.

Pranešimo informaciją sudaro perkėlimo informacija (pvz., „iš" ir „į" vietas).

Daugiau informacijos žr. [Sandėlio programos įvykių apdorojimas](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Mobiliojo įrenginio meniu konfigūravimas, kad būtų nepaisoma atidėto apdorojimo strategijos

Išsamesnės informacijos apie tai, kaip konfigūruoti mobiliojo įrenginio meniu, kad būtų praleista atidėtoji apdorojimo strategija, [ieškokite Atidėtas sandėlio darbo apdorojimas](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Poveikis uždaryto darbo datoms

Išsamesnės informacijos apie poveikį uždarytoms darbo datoms žr. [Atidėtas sandėlio darbo apdorojimas](deferred-put.md).

## <a name="additional-resources"></a>Papildomi ištekliai

- [Atidėtas sandėlio darbo apdorojimas](deferred-put.md)
- [Sandėlio programos įvykio apdorojimas](warehouse-app-events.md)
- [Mobiliųjų įrenginių nustatymas darbui sandėlyje](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
