---
title: Įplaukų pripažinimo perskirstymas – 4 scenarijus
description: Šioje temoje aptariamas perskirstymo scenarijus, kai iš esamo pardavimo užsakymo, kuriam išrašyta dalinė SF, pašalinama eilutė. Šis scenarijus pateikia tą patį rezultatą, nepaisant to, ar eilutė pašalinta iš pardavimo užsakymo ar nustatyta būsena Atšaukta.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 500c7817795448d7d9759c4ad7a1842df0a9bdc5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003286"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Įplaukų pripažinimo perskirstymas – 4 scenarijus

[!include [banner](../includes/banner.md)]

Šioje temoje aptariamas perskirstymo scenarijus, kai iš esamo pardavimo užsakymo, kuriam išrašyta dalinė SF, pašalinama eilutė. Šis scenarijus pateikia tą patį rezultatą, nepaisant to, ar eilutė pašalinta iš pardavimo užsakymo ar nustatyta būsena Atšaukta.

Šiam scenarijui parinktis **Perskirstant registruoti SF taisymus į Gautinas sumas** nustatoma į **Ne** skirtuke **Įplaukų pripažinimas** puslapyje **DK parametrai** (**Įplaukų pripažinimas \> Sąranka \> DK parametrai**).

[![Parinktis Registruoti SF taisymus į Gautinas sumas nustatyta į Ne](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Sukurtas kliento US\_SI\_0003 pardavimo užsakymas. Klientas perka nešiojamąjį kompiuterį (prekės numeris S0012), diegimo tarnybas (prekės numeris S0001) ir nešiojamojo kompiuterio palaikymo planą (prekės numeris S0008, „Ilgalaikė inžinerinė paslauga). Nešiojamojo kompiuterio ir diegimo paslaugų įplaukos atpažįstamos iš karto. Palaikymo plano įplaukos bus atidėtos ir atpažįstamos per 12 mėnesių, kaip nurodyta sutartyje apibrėžtame datų intervale.

[![Nešiojamojo kompiuterio, diegimo tarnybų ir palaikymo plano pardavimo užsakymo eilutės](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Pardavimo užsakymas patvirtinamas. Visoms trims prekėms nustatytas įplaukų vertės paskirstymas, todėl įplaukų vertė apskaičiuojama patvirtinus pardavimo užsakymą. Galite peržiūrėti įplaukas, kurios bus atpažintos, puslapyje **Įplaukų vertės paskirstymas** (puslapyje **Pardavimo užsakymas** veiksmų srities skirtuke **Valdymas** grupėje **Įplaukų pripažinimas** pasirinkite **Įplaukų vertės paskirstymas**). Nešiojamojo kompiuterio įplaukos bus užregistruotos Įplaukų sąskaitoje, kurios suma 995,84 $. Diegimo paslaugų įplaukos taip pat bus užregistruotos Įplaukų sąskaitoje, kurios suma 314,47 $. Palaikymo plano įplaukos bus užregistruotos atidėtų įplaukų sąskaitoje, kurios suma 188,69 $. Įplaukų verčių suma turi būti lygi eilučių, kurios nustatytos įplaukų vertės paskirstymui fiksuoti, sumai (1 499,00 $).

[![Įplaukų vertės paskirstymo puslapis](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Klientui išrašoma SF nešiojamajam kompiuteriui ir palaiko planui, tačiau ne diegimo paslaugoms. Toliau pateiktoje iliustracijoje rodomas apskaitos įrašas, užregistruotas SF.

[![Pardavimo užsakymo, kuriam išrašyta SF, apskaitos įrašas](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Apskaitos įrašas registruoja 1 276,94 $ gautinose sumose. Tačiau, kadangi ši SF yra dalinė SF, įplaukos arba atidėtos įplaukos ir mokestis nėra lygūs gautinai sumai. -14,47 $ skirtumas užregistruotas dalinės SF įplaukų kliringo sąskaitoje.

Taip pat sukuriamas įplaukų pripažinimo grafikas.

[![Dalinės SF įplaukų pripažinimo grafiko puslapis](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Vėliau klientas nusprendžia nepirkti diegimo paslaugų. Todėl ši eilutė pašalinama iš pardavimo užsakymo. Atkreipkite dėmesį, kad pardavimo užsakymo vėl patvirtinti negalima, nes pardavimo užsakyme lieka tik eilutės, kurioms išrašytos SF.

[![Pardavimo užsakymas pašalinus diegimo paslaugų eilutę](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Net jeigu pardavimo užsakymo patvirtinti negalima, jį galima perskirstyti. Pardavimo užsakyme pasirinkite **Perskirstyti vertę naujose užsakymo eilutėse**, kad atidarytumėte puslapį **Perskirstyti vertę naujose užsakymo eilutėse**. Pasirinkite dvi likusias pardavimo užsakymo eilutes, tada pasirinkite **Naujinti perskirstymą**. Stulpelyje **Perskirstyta suma** rodoma nauja kiekvienos likusios pardavimo užsakymo eilutės įplaukų vertė.

[![Naujos įplaukų vertės puslapyje Perskirstyti vertę naujose užsakymo eilutėse](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Tada pasirinkite **Numatomas kvitas**, kad būtų galima peržiūrėti apskaitos įrašus.

[![Apskaitos įrašai puslapyje Numatomas kvitas](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

Puslapyje **Numatomas kvitas** paskutinės penkios eilutės atšaukia pradinį apskaitos įrašą iš užregistruotos SF. Pirmosios keturios eilutės yra nauji apskaitos įrašai, registruojami SF. Svarbu suprasti, kad nauja SF nėra pateikiama klientui. Po perskirstymo klientas vis dar skolingas 1 276,94 $, t. y. sumą, kuri turi būti užregistruota gautinose sumose naujame apskaitos įraše. Naujos įplaukos arba atidėtos įplaukos ir mokesčiai sudaro 1 276,94 $. Todėl nereikia registruoti dalinės SF įplaukų kliringo sąskaitos.

Norėdami baigti perskirstymą, pasirinkite **Apdoroti**. Įvedama registravimo data. Atlikus perskirstymą puslapyje **Įplaukų vertės priskyrimas** rodomas dviejų likusių prekių kainos perskirstymas.

[![Likusių prekių vertės perskirstymas puslapyje Įplaukų vertės paskirstymas](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Įplaukų pripažinimo grafikas taip pat buvo atnaujintas remiantis nauja įplaukų perskirstymo verte. Pardavimo užsakyme atidarykite puslapį **Įplaukų pripažinimo grafikas**. Anksčiau buvo 13 prekės S0008 eilučių (šiai prekei buvo priskirtas 12 mėnesių grafikas). Dabar yra 39 eilutės: 13 pradinio grafiko eilučių, 13 atšaukimo grafiko eilučių ir 13 eilučių, kurios pagrįstos nauja įplaukų verte.

[![Atnaujintas įplaukų pripažinimo grafiko puslapis su 39 prekės S0008 eilutėmis](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Pasirinkus **Kvitas**, SF žurnale rodomas pradinis apskaitos įrašas. Norėdami peržiūrėti atšaukimo įrašą ir naują apskaitos įrašą iš pardavimo užsakymo, veiksmų srityje pasirinkite **Įplaukų koregavimai**, tada pasirinkite **Kvitas**.

Tada atidarykite puslapį **Visi klientai** (**Gautinos sumos \> Klientai \> Visi klientai**), pasirinkite klientą **US\_SI\_0003**, tada pasirinkite **Operacijos**. Puslapyje **Kliento operacijos** kartu su pradiniu apskaitos įrašu rodoma tik pradinė SF (000008). Parinktis **Perskirstant registruoti SF taisymus į Gautinas sumas** yra nustatyta į **Ne** puslapyje **DK parametrai**, todėl atnaujinama tik Didžioji knyga. Todėl atšaukimo ir atnaujintų apskaitos įrašai nerodomi. Atkreipkite dėmesį, kad rodomos įplaukų koregavimo operacijos, sukurtos [3 scenarijuje](rev-rec-reallocation-scenario-3.md).

[![Pradinis apskaitos įrašas puslapyje Kliento operacijos](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)
