---
title: Įplaukų pripažinimo perskirstymas – 2 scenarijus
description: Tema apima perskirstymo scenarijų, kai įvedami du pardavimo užsakymai, tada klientas įtraukia prekę į sutartį po to, kai SF išrašoma pirmam pardavimo užsakymui. Kai į sutartį įtraukiama nauja prekė, ją galima įtraukti į naują pardavimo užsakymą arba į esamą pardavimo užsakymą.
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
ms.openlocfilehash: 31a0b26fbf2383c90caaa8c1ea0e56ab5f377609
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814205"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Įplaukų pripažinimo perskirstymas – 2 scenarijus

[!include [banner](../includes/banner.md)]

Tema apima perskirstymo scenarijų, kai įvedami du pardavimo užsakymai, tada klientas įtraukia prekę į sutartį po to, kai SF išrašoma pirmam pardavimo užsakymui. Kai į sutartį įtraukiama nauja prekė, ją galima įtraukti į naują pardavimo užsakymą arba į esamą pardavimo užsakymą.

Šiam scenarijui parinktis **Perskirstant registruoti SF taisymus į Gautinas sumas** nustatoma į **Ne** skirtuke **Įplaukų pripažinimas** puslapyje **DK parametrai** (**Įplaukų pripažinimas \> Sąranka \> DK parametrai**).

[![Parinktis Registruoti SF taisymus į Gautinas sumas nustatyta į Ne](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Sukurtas kliento US\_SI\_0003 pardavimo užsakymas. Klientas perka diegimo paslaugas (prekės numeris S0001) ir nešiojamojo kompiuterio palaikymo planą (prekės numeris S0008), tačiau jis dar nepasirinko nešiojamojo kompiuterio. Diegimo paslaugų įplaukos bus atidėtos iki nešiojamojo kompiuterio įsigijimo datos. Palaikymo plano įplaukos bus atidėtos ir atpažįstamos per 12 mėnesių, kaip nurodyta sutartyje apibrėžtame datų intervale.

[![Diegimo paslaugų ir palaikymo plano pardavimo užsakymo eilutės](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Pardavimo užsakymas patvirtinamas. Abiems prekėms nustatytas įplaukų vertės paskirstymas, todėl įplaukų vertė apskaičiuojama patvirtinus pardavimo užsakymą. Galite peržiūrėti įplaukas, kurios bus atpažintos, puslapyje **Įplaukų vertės paskirstymas** (puslapyje **Pardavimo užsakymas** veiksmų srities skirtuke **Valdymas** grupėje **Įplaukų pripažinimas** pasirinkite **Įplaukų vertės paskirstymas**). Diegimo paslaugų įplaukos bus užregistruotos Atidėtų įplaukų sąskaitoje, kurios suma 250,00 $. Palaikymo plano įplaukos taip pat bus užregistruotos atidėtų įplaukų sąskaitoje, kurios suma 150,00 $. Įplaukų verčių suma turi būti lygi eilučių, kurios nustatytos įplaukų vertės paskirstymui fiksuoti, sumai (400,00 $).

[![Įplaukų vertės paskirstymo puslapis](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Pardavimo užsakymui išrašyta visa SF. Toliau pateiktoje iliustracijoje rodomas apskaitos įrašas, užregistruotas SF.

[![Pardavimo užsakymo, kuriam išrašyta visa SF, apskaitos įrašas](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Taip pat sukuriamas įplaukų pripažinimo grafikas, tačiau įplaukos dar nepripažįstamos.

[![Įplaukų pripažinimo grafiko puslapis](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Po kelių dienų klientas pasirenka nešiojamąjį kompiuterį. Įvedamas antras kliento pardavimo užsakymas.

[![Nešiojamojo kompiuterio pardavimo užsakymo eilutė](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Patvirtinamas antras pardavimo užsakymas. Šiame pardavimo užsakyme yra tik viena eilutė, todėl įplaukų vertės paskirstymas neatliekamas, kai patvirtinamas pardavimo užsakymas. Įplaukų vertės paskirstymas vykdomas tik tada, kai yra dvi ar daugiau unikalių prekių ir tos prekės nustatytos kaip įplaukų vertės paskirstymas.

Jei šis naujas pardavimo užsakymas yra vienintelis kliento sutarties pakeitimas, galima vykdyti perskirstymo procesą. Viename iš dviejų pardavimo užsakymų pasirinkite **Perskirstyti vertę naujose užsakymo eilutėse**, kad atidarytumėte puslapį **Perskirstyti vertę naujose užsakymo eilutėse**. Arba eikite į **Įplaukų pripažinimas \> Periodinės užduotys \> Perskirstyti vertę naujose užsakymo eilutėse**. Pasirinkite du pardavimo užsakymus ir atitinkamas pardavimo užsakymo eilutes, tada pasirinkite **Naujinti perskirstymą**. Stulpelyje **Perskirstyta suma** rodoma nauja kiekvienos pardavimo užsakymo eilutės įplaukų vertė.

[![Naujos įplaukų vertės puslapyje Perskirstyti vertę naujose užsakymo eilutėse](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Tada pasirinkite **Numatytas kvitas**, kad būtų galima peržiūrėti apskaitos įrašus, kurie bus registruojami tik DK. Puslapyje **DK parametrai** parinktis **Registruoti SF taisymus į Gautinas sumas** nustatyta į **Ne**, todėl apdorojant perskirstymą gautinos sumos nepasikeičia.

[![Apskaitos įrašai puslapyje Numatomas kvitas](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

Puslapyje **Numatomas kvitas** paskutinės trys eilutės atšaukia pradinį apskaitos įrašą iš užregistruotos SF. Pirmosios keturios sudaro naują apskaitos įrašą, kuris registruojamas SF. Svarbu suprasti, kad nauja SF nėra pateikiama klientui. Po perskirstymo klientas vis dar skolingas 426,00 $, t. y. sumą, kuri turi būti užregistruota gautinose sumose naujame apskaitos įraše. Korespondentinis mokestis ir atidėtos įplaukos sudaro 188,69 $ + 314,48 $ + 26,00 $ = 529,17 $. Dėl perskirstymo pasikeitė atidėtų įplaukų suma. -103,17 $ skirtumas užregistruotas dalinės SF įplaukų kliringo sąskaitoje. Šis balansas bus išvalytas, kai bus užregistruota antro pardavimo užsakymo, kuris buvo įtrauktas į perskirstymą, SF.

Norėdami baigti perskirstymą, pasirinkite **Apdoroti**. Bus rodomas raginimas įvesti registravimo datą, net jeigu niekas neregistruojama. Kai perskirstymas bus baigtas, kiekvieno pardavimo užsakymo puslapyje **Įplaukų vertės paskirstymas** bus rodomas visų prekių, esančių abiejuose pardavimo užsakymuose, vertės paskirstymas. Kitaip tariant, į kiekvieno pardavimo užsakymo puslapį **Įplaukų vertės paskirstymas** bus įtraukta prekė, kurios nėra tame pardavimo užsakyme, nes ji yra tos pačios sutarties, tačiau kito pardavimo užsakymo, dalis.

> [!TIP]
> Norėdami pateikti kontekstą, kodėl šie papildomi elementai rodomi, į tinklelį galite įtraukti kitus stulpelius, pvz., **Perskirstymo ID** ir **Pardavimo užsakymas**.
> 
> [![Papildomi stulpeliai puslapyje Įplaukų vertės paskirstymai](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

Pardavimo užsakyme 00036 įplaukų pripažinimo grafikas taip pat buvo atnaujintas remiantis nauja įplaukų perskirstymo verte. Šiame pardavimo užsakyme atidarykite puslapį **Įplaukų pripažinimo grafikas**. Anksčiau buvo 13 prekės S0008 eilučių (šiai prekei buvo priskirtas 12 mėnesių grafikas). Dabar yra 39 eilutės: 13 pradinio grafiko eilučių, 13 atšaukimo grafiko eilučių ir 13 eilučių, kurios pagrįstos nauja įplaukų verte.

[![Atnaujintas įplaukų pripažinimo grafiko puslapis su 39 prekės S0008 eilutėmis](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Anksčiau buvo dvi prekės S0001 eilutės, tačiau dabar yra šešios.

[![Atnaujintas įplaukų pripažinimo grafiko puslapis su šešiomis prekės S0001 eilutėmis](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Pardavimo užsakyme 000036 pasirinkus **Kvitas**, SF žurnale rodomas pradinis apskaitos įrašas. Norėdami peržiūrėti atšaukimo įrašą ir naują apskaitos įrašą iš pardavimo užsakymo, veiksmų srityje pasirinkite **Įplaukų koregavimai**, tada pasirinkite **Kvitas**.

[![Pardavimo užsakymas 000036](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Tada atidarykite puslapį **Visi klientai** (**Gautinos sumos \> Klientai \> Visi klientai**), pasirinkite klientą **US\_SI\_0003**, tada pasirinkite **Operacijos**. Bus rodoma atvira pardavimo užsakymo 000036 SF. Jei pasirenkate kvitą, matysite pradinį apskaitos įrašą, o ne naują apskaitos įrašą iš perskirstymo. Atšaukimo įrašo ir naujo apskaitos įrašo negalima peržiūrėti gautinose sumose.

Antram pardavimo užsakymui išrašoma SF. Bendra klientui pateikiama SF sudaro 1.099,00 $ + 71,44 $ mokestis = 1.170,44 $. Toliau pateiktoje iliustracijoje rodomas užregistruotas apskaitos įrašas.

[![Puslapis Kvito operacijos su užregistruotu apskaitos įrašu](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Kadangi įplaukų ir pardavimų suma didesnė nei 1.170,44 $, užregistruojamas -130,17 $ skirtumas. Ši suma išvalo balansą iš dalinės SF įplaukų kliringo sąskaitos. Tas balansas registruojamas naujame apskaitos įraše po perskirstymo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]