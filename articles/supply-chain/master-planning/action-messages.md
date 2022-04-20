---
title: Veiksmų pranešimai
description: Veiksmo pranešimas yra sistemos sugeneruotas pasiūlymas keisti esamą suplanuotą arba patvirtintą tvarką.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570260"
---
# <a name="action-messages"></a>Veiksmų pranešimai

[!include [banner](../includes/banner.md)]

Veiksmo pranešimas yra sistemos sugeneruotas pasiūlymas keisti esamą suplanuotą, patvirtintą arba patvirtintą užsakymą.

Veiksmų pranešimai generuojami pakeitus reikalavimus, kai bendrojo planavimo metu atliekami skaičiavimai. Pavyzdžiui, siuntimo data arba kiekis pardavimo užsakyme pakeičiamas, kai jau sukūrėte pirkimo užsakymą, kad patenkintų to pardavimo užsakymo poreikį. Šiuo atveju bendrojo planavimo skaičiavimas generuoja vieną ar daugiau veiksmo pranešimų, siūlančių atnaujinti pirkimo užsakymą. Galite nuspręsti, ar atlikti siūlomus keitimus.

Galite nustatyti, kaip turi būti skaičiuojami padengimo grupės, kurią pridedate prie prekės, veiksmų pranešimai.

## <a name="select-action-messages"></a>Pasirinkite veiksmų pranešimus

**Padengimo grupių** puslapyje galite pasirinkti, kokius veiksmų pranešimus turi generuoti sistema ir kurioms padengimo grupėms ar prekėms pranešimai turi būti taikomi. Šioje lentelėje pateikiamas veiksmo pranešimas, kurį galite pasirinkti.

| Pranešimas | Aprašymas |
|---|---|
| Išankstinis | Jei reikia, sistema generuos veiksmų pranešimus, kad perkeltų užsakymus į ankstesnę datą. Lauke Išankstinės **maržos** galite nurodyti didžiausią dienų, kurios gali praeiti nuo gavimo iki išdavimo be išankstinio veiksmo, skaičių. |
| Atidėti | Sistema generuos veiksmų pranešimus, kurių reikia, kad užsakymai būtų perkelti į vėlesnę datą. Lauke Atidėta **marža** galite nurodyti maksimalų dienų, kurios gali praeiti nuo gavimo iki išdavimo be atidėjimo veiksmo, skaičių. |
| Mažinti | Sistema generuos veiksmų pranešimus, kai gamybos užsakymai, pirkimo užsakymai ir kitos gavimo operacijos turėtų būti sumažinos, kad nebūtų viršytas atsargų lygis. |
| Didinti | Sistema generuos veiksmų pranešimus, kai gamybos užsakymai, pirkimo užsakymai ir kitos gavimo operacijos turėtų būti padidintos, kad būtų išvengta atsargų trūkumo. |
| Išvestiniai veiksmai | Veiksmo pranešimai, sukurti gavimo operacijoms, bus išplatinti į bet kuriuos išvestinius reikalavimus ir gavimo operacijoms, kurios atitinka tuos reikalavimus, bus sugeneruoti būtini veiksmo pranešimai. |

Toliau pateikiamose dalyse pateikiami keli išsamūs scenarijai.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Padidinti ir sumažinti veiksmus su numatytuoju produkto užsakymo kiekiu

Prekės numatytųjų **užsakymo** parametrų puslapyje galite nustatyti mažiausią užsakymo kiekį, maksimalų užsakymo kiekį ir kelias vertes. Tada, kai ji siūlo veiksmus, sistema į šiuos parametrus atsižvelgia, kad pasiūlymai niekada nenusikels per daug.

Pavyzdžiui, turite prekę, kuri savo numatytųjų užsakymo parametrų **puslapyje turi šiuos** parametrus:

- **Mažiausias užsakymo kiekis:** *0*
- **Maksimalus užsakymo kiekis:** *90*
- **Keli:** *20*

Jei šios prekės kiekis yra 60, bendrasis planavimas sukurs suplanuotą pirkimo užsakymą, kurio kiekis – 60. Jei poreikis padidintas 30, bendrasis planavimas siūlys padidinimą 40, kadangi jis paisys 20 kartotinio ir dėl to niekada nebus per daug.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Užsakymų, susijusių su saugumo atsargomis, veiksmų pranešimai

Veiksmų pranešimuose, pateikiamuose užsakymams, kurie tiekia tiek laiko atsargas, niekada nebus siūloma mažinti kiekį, kuris bus mažesnis už kiekį, reikalingą norint gauti reikalingų atsargose. Kitaip tariant, jei yra užsakymas, kuris tiekia svarbias atsargas ir klientų poreikį, o poreikis sumažėja arba atšauktas, bendrasis planavimas pasiūlys sumažinti suplanuotą užsakymą pagal mažėjančią paklausą. Tačiau joje niekada nebus siūloma vertė, kuri būtų mažesnė už reikalingas laiko atsargas.

Sistema nesiųs atidėjimo veiksmų, kuriuos reikia atlikti norint tiekti reikiamas atsargas, nes laikoma, kad reikiamo laiko ir reikiamos datos reikia tiekti reikiamas atsargas.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Su KS susiję veiksmai paankstinti ir atidėti

Veiksmai, susiję su komplektavimo specifikacijos (KS) komponentais, turi būti taikomi prieš jų pirminių prekių veiksmus, nes gali būti paveikti tolesni užsakymai, susiję su aukštesnio lygio KS. Tada, norėdami perskaičiuoti ir pasiūlyti atitinkamus veiksmus, turite dar kartą vykdyti bendrąjį planavimą.

Pavyzdžiui, turite tokią situaciją:

- Galutinės prekės *FG,* kurios tipas *yra gamyba*, turi KS, kurioje yra *žaliavų RM*.
- Šiandienos data yra sausio 21 d.
- Esamas, pateiktas FG gamybos užsakymas *planuojamas* sausio 25 d.
- Siekiant palaikyti esamą gamybos užsakymą, bendrasis planavimas sukūrė suplanuotą būtinos žaliavų RM pirkimo *užsakymą*. Šio užsakymo poreikio data yra sausio 25 d.
- Šiandien sukurtas naujas *FG* pardavimo užsakymas. Jos poreikio data yra šiandien (sausio 21 d.).
- Sausio 21 d. uždaryta pristatyti *RM* kalendoriuje, tačiau sausio 22 d. atidaryta.

Vykdant bendrąjį planavimą, generuojami išankstinių veiksmų pranešimai, kurie siūlo perkelti aukštyn anksčiau suplanuotą gamybą, kad galėtumėte įvykdyti šiandienos užsakymą.

- Siekiant patenkinti naują poreikį, siūlo perkelti gamybos užsakymą FG iki *sausio* 21 d. (Šis pasiūlymas pasiūlomas neįrašant uždarytos datos *RM*.)
- Kadangi *RM* vis dar reikalingas gamybos užsakymui, jis siūlo pereiti prie suplanuoto pirkimo užsakymo. Tačiau šį kartą jis tikrina *RM kalendorių*. Todėl siūlo perkelti suplanuotą pirkimo užsakymą RM *į sausio* 22 d. (kadangi sausio 21 d. uždaryta).

Matote, reikiamos *žaliavų RM* dabar bus per vėlos suplanuotai FG *gamybai*. Todėl pirmiausia turite taikyti išankstinį veiksmą suplanuotam RM pirkimo užsakymui *, o* tada dar kartą vykdyti bendrąjį planavimą. Tuo metu bendrasis planavimas generuos naują veiksmo pranešimą, kuriame bus *siūloma perkelti gamybos užsakymą FG į sausio* 22 d.
