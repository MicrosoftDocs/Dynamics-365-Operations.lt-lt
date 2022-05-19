---
title: Įplaukų pripažinimo perskirstymas – 1 scenarijus
description: Šioje temoje aprašytas perskirstymo scenarijus, kai įvedami du pardavimo užsakymai, tačiau jie yra tik patvirtinti. Tas pats scenarijus duoda panašius rezultatus, jei daugiau nei dviejų pardavimo užsakymų būsena yra Patvirtinta.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cd094840e16a0ab19e234148e4ef40c454315d96
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725798"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Įplaukų pripažinimo perskirstymas – 1 scenarijus

[!include [banner](../includes/banner.md)]

Šioje temoje aprašytas perskirstymo scenarijus, kai įvedami du pardavimo užsakymai, tačiau jie yra tik patvirtinti. Tas pats scenarijus duoda panašius rezultatus, jei daugiau nei dviejų pardavimo užsakymų būsena yra Patvirtinta.

Šiam scenarijui parinktis **Perskirstant registruoti SF taisymus į Gautinas sumas** nustatoma į **Ne** skirtuke **Įplaukų pripažinimas** puslapyje **DK parametrai** (**Įplaukų pripažinimas \> Sąranka \> DK parametrai**).

[![Parinktis Registruoti SF taisymus į Gautinas sumas nustatyta į Ne.](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Sukurtas kliento US\_SI\_0003 pardavimo užsakymas. Klientas perka nešiojamąjį kompiuterį (prekės numeris S0012) ir palaikymo planą (prekės numeris S0008, „Ilgalaikė inžinerinė paslauga“). Nešiojamojo kompiuterio įplaukos atpažįstamos iš karto (nėra įplaukų atpažinimo grafiko). Palaikymo plano įplaukos bus atidėtos ir atpažįstamos per 12 mėnesių, kaip nurodyta sutartyje apibrėžtame datų intervale.

[![Nešiojamojo kompiuterio ir palaikymo plano pardavimo užsakymo eilutės.](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Pardavimo užsakymas patvirtinamas. Abiems prekėms nustatytas įplaukų vertės paskirstymas, todėl įplaukų vertė apskaičiuojama patvirtinus pardavimo užsakymą. Galite peržiūrėti įplaukas, kurios bus atpažintos, puslapyje **Įplaukų vertės paskirstymas** (puslapyje **Pardavimo užsakymas** veiksmų srities skirtuke **Valdymas** grupėje **Įplaukų pripažinimas** pasirinkite **Įplaukų vertės paskirstymas**). Nešiojamojo kompiuterio įplaukos bus užregistruotos Įplaukų sąskaitoje, kurios suma 1.008,01 $. Palaikymo plano įplaukos bus užregistruotos atidėtų įplaukų sąskaitoje, kurios suma 190,99 $. Įplaukų verčių suma turi būti lygi eilučių, kurios nustatytos įplaukų vertės paskirstymui fiksuoti, sumai (1 199,00 $).

[![Įplaukų vertės paskirstymo puslapis.](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Klientas pardavimo metu pasirinko nepirkti diegimo paslaugų (prekės numeris S0001), tačiau vėliau pakeitė savo nuomonę. Todėl įvedamas antras to paties kliento pardavimo užsakymas.

[![Diegimo paslaugų pardavimo užsakymo eilutė.](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Patvirtinamas antras pardavimo užsakymas. Šiame pardavimo užsakyme yra tik viena eilutė, todėl įplaukų vertės paskirstymas neatliekamas, kai patvirtinamas pardavimo užsakymas. Įplaukų vertės paskirstymas vykdomas tik tada, kai yra dvi ar daugiau unikalių prekių ir tos prekės nustatytos kaip įplaukų vertės paskirstymas.

Jei šis naujas pardavimo užsakymas yra vienintelis kliento sutarties pakeitimas, galima vykdyti perskirstymo procesą. Viename iš dviejų pardavimo užsakymų pasirinkite **Perskirstyti vertę naujose užsakymo eilutėse**, kad atidarytumėte puslapį **Perskirstyti vertę naujose užsakymo eilutėse**. Arba eikite į **Įplaukų pripažinimas \> Periodinės užduotys \> Perskirstyti vertę naujose užsakymo eilutėse**. Pasirinkite du pardavimo užsakymus ir atitinkamas pardavimo užsakymo eilutes, tada pasirinkite **Naujinti perskirstymą**. Stulpelyje **Perskirstyta suma** rodoma nauja kiekvienos pardavimo užsakymo eilutės įplaukų vertė.

[![Naujos įplaukų vertės puslapyje Perskirstyti vertę naujose užsakymo eilutėse.](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Jei pasirenkate **Numatytas kvitas**, nieko nerodoma, nes nebuvo užregistruota jokių SF.

Norėdami baigti perskirstymą, pasirinkite **Apdoroti**. Bus rodomas raginimas įvesti registravimo datą, net jeigu niekas neregistruojama. Kai perskirstymas bus baigtas, kiekvieno pardavimo užsakymo puslapyje **Įplaukų vertės paskirstymas** bus rodomas visų prekių, esančių abiejuose pardavimo užsakymuose, vertės paskirstymas. Kitaip tariant, į kiekvieno pardavimo užsakymo puslapį **Įplaukų vertės paskirstymas** bus įtraukta prekė, kurios nėra tame pardavimo užsakyme, nes ji yra tos pačios sutarties, tačiau kito pardavimo užsakymo, dalis.

> [!TIP]
> Norėdami pateikti kontekstą, kodėl šie papildomi elementai rodomi, į tinklelį galite įtraukti kitus stulpelius, pvz., **Perskirstymo ID** ir **Pardavimo užsakymas**.
> 
> [![Papildomi stulpeliai puslapyje Įplaukų vertės paskirstymai.](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
