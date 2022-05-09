---
title: Komercijos registravimo parametrai
description: Šioje temoje aprašomi parametrai, kurie yra specifiniai finansinių ir faktinių operacijų registravimui Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 1b49c893567d39f05e16cefee47407a424b7e139
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649181"
---
# <a name="commerce-posting-parameters"></a>Komercijos registravimo parametrai

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje aprašomi parametrai, kurie yra specifiniai finansinių ir faktinių operacijų registravimui Microsoft Dynamics 365 Commerce. "Commerce" registravimo parametrai yra "Commerce Headquarters" " **Retail" ir "Commerce \> Headquarters" nustatymo parametrų \> " \> Commerce Parameters Posting \> "**.

## <a name="periodic-discount-parameters"></a>Laikotarpio nuolaidos parametrai

Toliau esančioje lentelėje pateikiami periodinių nuolaidų parametrai, kurie yra specifiniai finansinių ir faktinių operacijų registravimui.

| Parametras | Aprašymas |
|-----------|-------------|
| Registruoti laikotarpio nuolaidą | Ši pasirinktis kontroliuoja, ar periodiniai pasiūlymai registruojami DK sąskaitose. Periodinės nuolaidos apima prekių rinkinių nuolaidas, kiekio nuolaidas ir nuolaidų pasiūlymus. Įgalinus šį parametrą, skyriuje Periodinės nuolaidos galima nustatyti **papildomus** laukus. |
| DK sąskaitos tipas | <p>Pasirinkite sąskaitos, kuri bus naudojama laikotarpio nuolaidoms registruoti, tipą:</p><ul><li>**Standartinis** – sistema šiame puslapyje naudoja su nuolaida susijusius laukus. Vietoj to ji naudoja sąskaitas, kurios nustatytos "**Commerce Headquarters**" registravimo puslapyje (**atsargų valdymo nustatymo registravimo \>\>\> registravimo formos).**</li><li>**Periodinis** – sistema naudoja "Commerce discount" sąskaitas, kurias šiame puslapyje nurodė su nuolaida susiję laukai. Jei pasirenkate šią pasirinktį, turite nurodyti kiekvieno pasiūlymo tipo DK (nuolaida, nuolaida ir gretinimas, kiekis ir ribinė vertė) DK sąskaitą. Kai nustatote kiekvieną nuolaidą, galite nurodyti sąskaitą. Kai nuolaidos sąskaitos registravimo priemonė naudojama nuolaidos nustatymo puslapyje, papildomas debeto įrašas ir kredito įrašas yra atliekami, norint perklasifikuoti nuolaidos registravimą iš komercijos nuolaidos DK sąskaitos į nuolaidos DK sąskaitą. Daugiau informacijos rasite Mažmeninės [prekybos nuolaidos](retail-discounts-overview.md).</li></ul> |
| Registruoti informacijos kodo nuolaidą | Ši pasirinktis nebenaudojama standartiniame "Commerce" sprendimas ir bus pasenusi. |
| Registruoti užsakymų laikotarpio nuolaidas | Ši pasirinktis valdo, ar klientų užsakymų ir skambučių centro užsakymų mažmeninės prekybos periodinės nuolaidos registruojamos DK. |

## <a name="inventory-update-parameters"></a>Atsargų atnaujinimo parametrai

Šioje lentelėje išvarditi atsargų atnaujinimo parametrai, kurie yra specifiniai finansinių ir faktinių operacijų registravimui.

| Parametras | Aprašymas |
|-----------|-------------|
| Naudoti numatytąjį paketo ID, kai nerasta paketo numerių | Ši pasirinktis valdo, ar prekėms, kurių paketas įgalintas, naudojamas numatytasis paketo ID, jei nerasta paketo numerių ir leidžiamos neigiamos atsargos. |
| Numatytasis paketo ID | Paketo numeris, naudotimas, jei nerasta prekių paketo numerių ir **įgalinamas parametras Naudoti numatytąjį paketo ID**, kai nerasta paketo numerių. |

## <a name="aggregation-parameters"></a>Telkimo parametrai

Toliau esančioje lentelėje pateikiami telkimo parametrai, specialūs registruojant finansines ir faktines operacijas.

| Parametras | Aprašymas |
|-----------|-------------|
| Pinigų įnešimas į kasą | Įgalinkite šį parametrą, norėdami sujungti visas operacijas registruojant išrašą ir sukurti atskirą eilutę registruoti, o ne atskirą kiekvieno numetimo eilutę. |
| Inkasavimas | Įgalinkite šį parametrą, norėdami sujungti visas operacijas registruojant išrašą ir sukurti atskirą eilutę registruoti, o ne atskirą kiekvieno numetimo eilutę. |
| Pardavimo operacijos | Įgalinkite šį parametrą, kad operacijos būtų konsoliduotos kaip operacijų išrašo registravimo proceso dalis. Rekomenduojame įgalinti šį parametrą. Anksčiau tai buvo kvito **operacijos**. |
| Grąžinimai netelkiami | Jei pažymėta ši pasirinktis, registruojant mažmeninės prekybos išrašą kiekviena grąžinimo operacija registruojama kaip atskiras pardavimo užsakymas. |

## <a name="batch-processing-parameters"></a>Paketinio vykdymo parametrai

Šioje lentelėje išvarditi paketinio vykdymo parametrai, kurie yra specifiniai finansinių ir faktinių operacijų registravimui.

| Parametras | Aprašymas |
|-----------|-------------|
| Didžiausias lygiagrečių išrašų skaičius | Šis laukas nurodo paketinių užduočių, kurios naudojamos keliems išrašams registruoti, skaičių. |
| Maksimalus gijų skaičius, skirtas vieno išrašo užsakymo apdorojimui | Šis laukas nurodo didžiausią gijų skaičių, kurį išrašo registravimo paketinė užduotis naudoja vieno išrašo pardavimo užsakymams kurti ir išrašyti SF. Bendras gijų, kurias naudoja išrašo **registravimo procesas, skaičius apskaičiuojamas dauginant šio parametro vertę iš parametro maksimalios lygiagretaus išrašo registravimo parametro** skaičiaus vertės. Jei šio parametro vertė per didelė, ji gali turėti neigiamos įtakos išrašo registravimo proceso našumui. |
| Didžiausias telkime įtrauktas operacijų eilučių skaičius | Šiame lauke nustatomas operacijos eilučių, įtrauktų į vieną sudėti operaciją prieš naujos operacijos sukuriant, skaičius. Sukauptos operacijos sukuriamos pagal skirtingus telkimo kriterijus, pvz., klientą, verslo datą arba finansines dimensijas. Įsidėmėkite, kad vienos operacijos eilutės nebus padalintos skirtingoms suvestinėms operacijoms. Todėl, remiantis tokiais koeficientais, kaip atskirų produktų skaičius, jungtinių operacijų eilučių skaičius gali būti šiek tiek didesnis ar mažesnis. |
| Didžiausias gijų, reikalingų parduotuvės operacijoms tikrinti, skaičius | Šiame lauke nustatomas maksimalus gijų, naudojamų operacijoms tikrinti, skaičius. Operacijų tikrinimas yra būtinas žingsnis, kuris turi įvykti prieš tai, kai operacijos galės būti pereitos į išrašus. Taip pat turite nustatyti dovanų **kortelės** produktą dovanų kortelės "FastTab **·** **", kuris yra "Commerce**" parametrų puslapio registravimo skirtuke, net jei organizacija ne naudoja dovanų kortelių. |

Šioje lentelėje išvardijamos ankstesnės lentelės rekomenduojamų parametrų vertės. Šias vertes reikėtų patikrinti ir pakeisti diegimo konfigūraciją bei prieinamą infrastruktūrą. Vertės, viršijančios rekomenduojamas vertes, gali neigiamai paveikti kitą paketinį apdorojimą ir turi būti patvirtintos.

| Parametras | Rekomenduojama vertė | Informacija |
|-----------|-------------------|---------|
| Maksimalus lygiagrečiai registruojamų išrašų skaičius | <p>Nustatykite šį parametrą kaip paketinių užduočių, kurias gali naudoti paketų grupė, vykdanti išrašo **užduotį,** skaičių.</p><p>**Bendroji taisyklė:** dauginkite programos objektų serverio (AOS) virtualiųjų serverių skaičių iš paketinių užduočių, kurios galimos AOS virtualiame serveryje, skaičiaus.</p> | Šis parametras netaikomas, kai įgalinta funkcija **Mažmeninės prekybos išrašai – Parduotuvei** skirtas tiekimas. |
| Maksimalus gijų skaičius, skirtas vieno išrašo užsakymo apdorojimui | Pradėti tikrinti vertes **4**. Paprastai vertė neturi viršyti **8**. | Šis parametras apibrėžia gijų, kurios naudojamos pardavimo užsakymams kurti ir registruoti, skaičių. Jis rodo gijų, kurias galima registruoti pagal išrašą, skaičių. |
| Didžiausias telkime įtrauktas operacijų eilučių skaičius | Pradėti tikrinti vertes **1000 vertei**. Atsižvelgiant į "Commerce Headquarters" konfigūraciją, mažesni užsakymai gali padidinti našumą. | Šis parametras nurodo eilučių, kurios registruojant išrašą įtraukiamos į kiekvieną pardavimo užsakymą, skaičių. Pasiekus šį skaičių eilutės bus padalinta į naują užsakymą. Pardavimo eilučių skaičius nėra tiksliai lygus jūsų nurodytas skaičius, nes skaidymo procesas vyksta pardavimo užsakymo lygiu. Neatsižvelgiant į tai, numeris bus arti numerio, kuris nustatytas. Šis parametras naudojamas generuoti mažmeninės prekybos operacijų, kurių klientas neturi įvardyto kliento, pardavimo užsakymus. |
| Didžiausias gijų, reikalingų parduotuvės operacijoms tikrinti, skaičius | Rekomenduojame nustatyti šį parametrą kaip **4** ir padidinti jį tik tada, jei nepasiekite priimtino našumo. Gijų, kurias naudoja šis procesas, skaičius negali viršyti procesorių, kurie galimi paketinio apdorojimo serveryje, skaičiaus. Jei gijų skaičius per didelis, gali būti paveiktas kitas paketinis apdorojimas. | Šis parametras valdo operacijų, kurias galima patikrinti vienu metu duotame parduotuvėje, skaičių. |

> [!NOTE]
> Visi su išrašo registravimu susiję nustatymai ir parametrai, kurie nurodyti mažmeninės prekybos parduotuvėse ir puslapyje **Prekybos parametrai** taikomi naudojantis patobulinta išrašo registravimo funkcija.

## <a name="invoice-parameters"></a>SF parametrai

Toliau esančioje lentelėje pateikiami SF parametrai, kurie yra specifiniai finansinių ir faktinių operacijų registravimui.

| Parametras | Aprašymas |
|-----------|-------------|
| Žurnalo pavadinimas | Mokėjimų žurnalo pavadinimas, naudojamas kuriant pardavimo užsakymo mokėjimų kliento mokėjimo žurnalus. Šis parametras taikomas visiems užsakymų mokėjimams, kurie užregistruoti naudoti elektroninį kasos kanalą (EKA), skambučių centrą ir el. komercijos kanalo užsakymus. |
| Abonemento pavadinimas | Mokėjimo sąskaitos pavadinimas. |
| Nustatyti dimensijų prioritetus pagal mokėjimo metodą | Įgalinus šią vėliavėlę, mokėjimo žurnalai suteikia prioritetą dimensijoms iš mokėjimo būdo, o ne dimensijoms iš parduotuvės. |
| Mokesčių skaičiavimo elgsena | Šis parametras nurodo veikimo būdą, kai pardavimo užsakymams, sukurtims registruojant išrašą, išrašoma SF:<ul><li>**Perskaičiuoti – skaičiuoti** mokesčius iš naujo.</li><li> **Neskaičiuoti iš naujo – naudokite** mokesčių sumas, apskaičiuotas EKA.</li></ul> |
| Žurnalo pavadinimas | Žurnalo pavadinimas, naudojamas kuriant grąžinimams kliento mokėjimų žurnalą. Šis parametras taikomas visiems užsakymų mokėjimams, kurie registruojami EKA, skambučių centre ir el. komercijos kanalo užsakymuose. |

## <a name="statement-parameters"></a>Išrašo parametrai

Šioje lentelėje išvarditi išrašo parametrai, kurie yra specifiniai finansinių ir faktinių operacijų registravimui.

| Parametras | Aprašymas |
|-----------|-------------|
| Skaičiuojant rezervuoti atsargas | Įgalinus šį parametrą, išrašo skaičiavimas laikinai rezervuos atsargas, kol bus užregistruotas išrašas. Numatyta, kad šis parametras išjungtas, kad pagerintų išrašų skaičiavimo efektyvumą. Atnaujinta atsargų informacija gali būti skaičiuojama naudojant paketinę **užduotį Registruoti** atsargas. Atkreipkite dėmesį **, kad** paketinė užduotis Registruoti atsargas nebenaudojama, [kai](trickle-feed.md) mažmeninės prekybos operacijoms negalima kurti prekių tiektuvu pagrįstų užsakymų. |
| Reikia išjungti skaičiavimą | Ši vėliavėlė išjungia skaičiavimą registruojant "Commerce Headquarters". |
| Perskaičiuoti finansines dimensijas, suskaičiuoti pagal klaidą | Įgalinus šį parametrą, finansinės dimensijos gali būti perskaičiuotos vėlesniuose išrašų registravime, jei išrašo registravimas nepavyksta. |
| Naudoti parduotuvės, į kurią grąžintas užsakymas, finansinę dimensiją. | Kai šis parametras įgalintas, gali būti sukurti susieti grąžinimo pardavimo užsakymai, naudojantys finansines parduotuvės dimensijas, o ne pradinės operacijos finansines dimensijas. |
| Atsieti grąžinimus | Kai šis parametras įgalintas, išrašas gali sukurti neregistruoto pardavimo grąžinimus kaip nematomus grąžinimus. Numatyta, kad šis parametras uždraustas, todėl rekomenduojame jį palikti išjungtą. |
| Uždrausti apvalinimo skirtumo registravimą | Šis parametras išjungia apvalinimo skirtumo tarp operacijos mokėjimo ir bendrosios sumos registravimą mokėjimų apdorojimo metu. |
| Automatinis klientų indėlių padengimas | Įgalinus šį parametrą, kliento depozitai, užregistruoti registruojant mažmeninės prekybos išrašą, sudengami su kliento atviromis operacijomis. |
| Įjungti ir naudoti grynųjų pinigų valdymo derinimą naudojant EKA | Kai šis parametras įgalintas, grynųjų pinigų valdymo suderinimas atliekamas EKA, o vertės perduodamos į mažmeninės prekybos finansinės ataskaitos registravimą, kad būtų galima kurti išrašo eilutes. |
| DK kvito informacijos lygis | Šis parametras nustato EKA pasirinktų operacijų, įtrauktų į DK kvitą, išsamumo lygį. Operacijų tipai apima pajamas, išlaidas ir nuolaidas. Nuolaidų atveju šis parametras taikomas tik tada, kai laikotarpio nuolaidos sąskaitos numeris ir įprastos nuolaidos sąskaitos numeris nėra vienodi. Jei reikia daugiau informacijos, **suvestinė** yra rekomenduojama šių registravimus registruojant. Kai suminis registravimas nustatytas, **TransactionDiscountTrans.RecID** nebus įrašomas. Commerce 10.0.27 versijoje ši vėliavėlė buvo pervardyta ir perkelta. Anksčiau jis buvo pavadintas **Detalumo** lygiu ir buvo **atsargų atnaujinimo** skyriuje. |
