---
title: Įplaukų pripažinimo perskirstymas – 3 scenarijus
description: Šioje temoje aptariamas perskirstymo scenarijus, kai į esamą pardavimo užsakymą, kuriam išrašyta dalinė SF, įtraukiama nauja eilutė. Kai į sutartį įtraukiama nauja prekė, ją galima įtraukti į naują pardavimo užsakymą arba į esamą pardavimo užsakymą.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e4e0d89c094bd8dba9ff4560502035fa36ec453454a4e31596db8cfd3517c8e5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726163"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Įplaukų pripažinimo perskirstymas – 3 scenarijus

[!include [banner](../includes/banner.md)]

Šioje temoje aptariamas perskirstymo scenarijus, kai į esamą pardavimo užsakymą, kuriam išrašyta dalinė SF, įtraukiama nauja eilutė. Kai į sutartį įtraukiama nauja prekė, ją galima įtraukti į naują pardavimo užsakymą arba į esamą pardavimo užsakymą. Šis scenarijus taip pat rodo, kas vyksta, kai gautinos sumos atnaujinamos dėl perskirstymo.

Šiam scenarijui parinktis **Perskirstant registruoti SF taisymus į Gautinas sumas** nustatoma į **Taip** skirtuke **Įplaukų pripažinimas** puslapyje **DK parametrai** (**Įplaukų pripažinimas \> Sąranka \> DK parametrai**).

[![Parinktis Registruoti SF taisymus į Gautinas sumas nustatyta į Taip.](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Sukurtas kliento US\_SI\_0003 pardavimo užsakymas. Klientas perka nešiojamąjį kompiuterį (prekės numeris S0012) ir palaikymo planą (prekės numeris S0008, „Ilgalaikė inžinerinė paslauga“). Nešiojamojo kompiuterio įplaukos atpažįstamos iš karto. Palaikymo plano įplaukos bus atidėtos ir atpažįstamos per 12 mėnesių, kaip nurodyta sutartyje apibrėžtame datų intervale.

[![Nešiojamojo kompiuterio ir palaikymo plano pardavimo užsakymo eilutės.](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Pardavimo užsakymas patvirtinamas. Abiems prekėms nustatytas įplaukų vertės paskirstymas, todėl įplaukų vertė apskaičiuojama patvirtinus pardavimo užsakymą. Galite peržiūrėti įplaukas, kurios bus atpažintos, puslapyje **Įplaukų vertės paskirstymas** (puslapyje **Pardavimo užsakymas** veiksmų srities skirtuke **Valdymas** grupėje **Įplaukų pripažinimas** pasirinkite **Įplaukų vertės paskirstymas**). Nešiojamojo kompiuterio įplaukos bus užregistruotos Įplaukų sąskaitoje, kurios suma 1 008,01 $. Palaikymo plano įplaukos bus užregistruotos atidėtų įplaukų sąskaitoje, kurios suma 190,99 $. Įplaukų verčių suma turi būti lygi eilučių, kurios nustatytos įplaukų vertės paskirstymui fiksuoti, sumai (1 199,00 $).

[![Įplaukų vertės paskirstymo puslapis.](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Pardavimo užsakymui išrašyta visa SF. Toliau pateiktoje iliustracijoje rodomas apskaitos įrašas, užregistruotas SF.

[![Pardavimo užsakymo, kuriam išrašyta visa SF, apskaitos įrašas.](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Taip pat sukuriamas įplaukų pripažinimo grafikas. Praėjus tam tikram laikui du mėnesiai atpažino palaikymo plano įplaukas.

[![Puslapis Įplaukų pripažinimo grafikas po dviejų mėnesių.](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

Šiuo metu klientas nusprendžia įtraukti diegimo paslaugas (prekės numeris S0001). Ši prekė įtraukiama į esamą pardavimo užsakymą. Klientas raginamas patvirtinti, kad nori modifikuoti pardavimo užsakymą, kuriam išrašyta visa SF, ir jis pasirenka **Taip**.

[![Pardavimo užsakymas įtraukus diegimo paslaugų eilutę.](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Jei ši nauja prekė yra vienintelis kliento sutarties pakeitimas, galima vykdyti perskirstymo procesą. Pardavimo užsakyme pasirinkite **Perskirstyti vertę naujose užsakymo eilutėse**, kad atidarytumėte puslapį **Perskirstyti vertę naujose užsakymo eilutėse**. Pasirinkite visas šio pardavimo užsakymo eilutes, tada pasirinkite **Naujinti perskirstymą**. Stulpelyje **Perskirstyta suma** rodoma nauja kiekvienos pardavimo užsakymo eilutės įplaukų vertė.

[![Naujos įplaukų vertės puslapyje Perskirstyti vertę naujose užsakymo eilutėse.](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Tada pasirinkite **Numatomas kvitas**, kad būtų galima peržiūrėti apskaitos įrašus. Parinktis **Registruoti SF taisymus į Gautinas sumas** yra nustatyta į **Taip** puslapyje **Didžiosios knygos parametrai**, todėl šie apskaitos įrašai bus registruojami didžiojoje knygoje naudojant kredito dokumentą, o gautinose sumose bus sukurta nauja SF.

[![Apskaitos įrašai puslapyje Numatomas kvitas.](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

Puslapyje **Numatomas kvitas** paskutinės keturios eilutės atšaukia pradinį apskaitos įrašą iš užregistruotos SF. Pirmosios penkios eilutės yra nauji apskaitos įrašai, registruojami SF. Svarbu suprasti, kad nauja SF nėra pateikiama klientui. Po perskirstymo klientas vis dar skolingas 1 276,94 $, t. y. sumą, kuri turi būti užregistruota gautinose sumose naujame apskaitos įraše. Korespondentinis mokestis ir įplaukos arba atidėtos įplaukos sudaro 995,83 $ + 188,69 $ + 77,94 $ = 1 262,46 $. Dėl perskirstymo pasikeitė įplaukų arba atidėtų įplaukų suma. -14,48 $ skirtumas užregistruotas dalinės SF įplaukų kliringo sąskaitoje. Šis balansas bus išvalytas, kai bus užregistruota naujos prekės, kuri buvo įtraukta į pardavimo užsakymą, SF.

Norėdami baigti perskirstymą, pasirinkite **Apdoroti**. Įvedama registravimo data. Atlikus perskirstymą puslapyje **Įplaukų vertės priskyrimas** rodomas visų trijų prekių kainos perskirstymas.

[![Visų trijų prekių vertės perskirstymas puslapyje Įplaukų vertės paskirstymas.](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Įplaukų pripažinimo grafikas taip pat buvo atnaujintas remiantis nauja įplaukų perskirstymo verte. Pardavimo užsakyme atidarykite puslapį **Įplaukų pripažinimo grafikas**. Anksčiau buvo 13 prekės S0008 eilučių (šiai prekei buvo priskirtas 12 mėnesių grafikas). Dabar yra 39 eilutės: 13 pradinio grafiko eilučių, 13 atšaukimo grafiko eilučių ir 13 eilučių, kurios pagrįstos nauja įplaukų verte.

[![Atnaujintas įplaukų pripažinimo grafiko puslapis su 39 prekės S0008 eilutėmis.](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Pasirinkus **Kvitas**, SF žurnale rodomas pradinis apskaitos įrašas. Norėdami peržiūrėti atšaukimo įrašą ir naują apskaitos įrašą iš pardavimo užsakymo, veiksmų srityje pasirinkite **Įplaukų koregavimai**, tada pasirinkite **Kvitas**.

Tada atidarykite puslapį **Visi klientai** (**Gautinos sumos \> Klientai \> Visi klientai**), pasirinkite klientą **US\_SI\_0003**, tada pasirinkite **Operacijos**. Puslapyje **Kliento operacijos** rodoma pradinė SF (000006), atšaukimo dokumentas (000006-1) ir nauja SF (000006-2). Pradinė SF ir atšaukimo dokumentas sudengiami vienas su kitu ir jų balansas lygus 0 (nuliui). Norėdami pamatyti poveikį DK, peržiūrėkite kiekvieno dokumento kvitą.

[![Pradinė SF, atšaukimo dokumentas ir nauja SF puslapyje Kliento operacijos.](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Vėl išrašoma pridėtos prekės pardavimo užsakymo SF. Bendra klientui pateikiama SF sudaro 300,00 $ + 19,50 $ mokestis = 319,50 $. Toliau pateiktoje iliustracijoje rodomas užregistruotas apskaitos įrašas.

[![Puslapis Kvito operacijos su užregistruotu apskaitos įrašu.](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Kadangi įplaukų ir pardavimų suma didesnė nei 319,50 $, užregistruojamas 14,48 $ skirtumas. Ši suma išvalo balansą iš dalinės SF įplaukų kliringo sąskaitos. Tas balansas buvo atnaujintas naujame apskaitos įraše, užregistruotame po perskirstymo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]