---
title: Profilių paskelbimo apžvalga
description: Šiame straipsnyje paaiškinama, kaip registravimo profiliai naudojami visose Microsoft Dynamics 365 programėlėse.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7ef3be13e82ff3722fc81247b5cd581b0b571b0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876130"
---
# <a name="posting-profiles-overview"></a>Profilių paskelbimo apžvalga

Finansų ir operacijų programėlėse termino registravimo šablonuose aprašomos konfigūracijos, kurios kontroliuoja, kaip papildomos knygos sąskaitos konvertuojamos į pagrindines sąskaitas, *kad* jas būtų galima naudoti DK registruojamose operacijose. Pavyzdžiui, jie kontroliuoja, kaip klientas konvertuojamas į gautinų sumų pagrindinę sąskaitą, kai SF užregistruojama.

Kai kuriuose moduliuose ir priemonėse yra puslapis, kuriame yra žodžiai "registravimo šablonas" pavadinime (pvz., **Kliento registravimo šablonas** arba **Tiekėjo registravimo šablonas**). Be to, kai kurie moduliai turi kelias pasirinktis, skirtas operacijų, sugeneruotų iš papildomos knygos, DK registravimo konfigūravimui. Pavyzdžiui, gamybos kontrolės modulyje **galite** nustatyti registravimą pagal gamybos grupę, išteklius ar išteklių grupę.

Nepamirškite, kad daugelyje operacijų tipų yra alternatyva registravimo šablonams: registravimo aprašams. Norėdami klasifikuoti apskaitos įrašų pagrindines sąskaitas ir finansines dimensijas, palaikomuose dokumentuose galite naudoti registravimo aprašus, o ne registravimo šablonus. Jei planuojate naudoti biudžeto rezervavimus ar preliminarius biudžeto rezervavimus, apskaitos įrašų sąskaitoms nustatyti būtinas registravimo aprašas.

Prieš konfigūruodami registravimo šablonus, **registravimo** aprašus arba automatinių operacijų sąskaitų puslapį, turite sukonfigūruoti sąskaitų planą DK puslapyje, juridiniame subjekte, **kurį** norite konfigūruoti.

## <a name="posting-types"></a>Registravimo tipai

Finansų ir operacijų programėlių registravimo tipas naudojamas bendrai debeto arba kredito kategorijai nustatyti. Ši kategorija nepriklauso nuo pagrindinės DK sąskaitos. DK yra kiekvieno debeto arba kredito registravimo tipai.

Viename kvite gali būti vienas arba daugiau registravimo tipų. Pavyzdžiui, operacija **·** **·**, registruojama per bendrąjį žurnalą, kur sąskaita ir korespondentinė sąskaita nustatyta į DK, turi turėti ir debeto, ir kredito registravimo tipą DK žurnale. Priešingai, tiekėjo SF registravimo tipai bus keli. Šie registravimo tipai apims vieną tiekėjo balanso eilutę ir papildomas korespondentinio įrašo eilutes, pvz. **, DK žurnalą**.

Kvito operacijų puslapio skirtuke **Bendra** galite peržiūrėti **registravimo** tipo **lauką**.

> [!TIP]
> Galite naudoti personalizavimo **įrankių juostą**, norėdami pridėti **registravimo** tipo lauką į tinklelį **skirtuke Peržiūra**, arba jį perkelti. Tokiu būdu galite palengvinti prieigą prie šio lauko ir jį peržiūrėti, kai galėsite peržiūrėti kvitus.

## <a name="detail-settings-for-a-posting-profile"></a>Registravimo šablono informacijos parametrai 

Konfigūruodami registravimo šablonus, **sąskaitos** kodo laukas apibrėžia parametro lygį. Galimos šios pasirinktys: **Lentelė**, **Grupė** ir **Visi**. Gretinimas sustabdomas po pirmojo gretinimo ir užsakymas yra nuo tinkamiausio lygio iki mažiausiai konkretaus lygio. Nors kai **kuriais atvejais** sąskaitos kodo lauko pavadinimas gali šiek tiek skirtis, lauko veikimo būdas ir funkcija lieka tokie patys. Pavyzdžiui, atsargų registravimo šablonas apima lauką **Prekės kodas** ir Sąskaitos **kodo** lauką. Abiejų laukų vertės **yra Lentelė**,**Grupė** **ir** Visos.

**Jei** laukas Pagrindinė sąskaita neužpildytas registravimo šablonui, **o** pagrindinės sąskaitos nekonfigūravote automatinių operacijų puslapyje arba konkrečios modulio ar funkcijos puslapyje, registruojant operaciją, kuri naudoja registravimo tipą, bus rodomas klaidos pranešimas. Paprastai pranešimas bus "Registravimo tipo \[sąskaita\] nerasta".

### <a name="table-value"></a>Lentelės vertė

Lentelės **vertė** nurodo pagrindinį įrašą, susietą su registravimo šablonu. Kiekvienas lentelės įrašas turi konkrečią vertę. Jūs nurodote, kad vertė lauke, kuris yra po sąskaitos **kodo** lauko. Paprastai šis laukas būna pavadintas **Sąskaitos** arba **Sąskaitos/Grupės numeris**. Tikslus pavadinimas skiriasi, atsižvelgiant į lapą, kuriame jis rodomas.

Pavyzdžiui, jei dirbate su kliento registravimo šablonu, lentelės **vertė** nurodo konkretų klientą. Todėl jei lauke Sąskaitos **kodas** pasirenkate **Lentelė**, turite pasirinkti kliento numerį lauke **Sąskaitos/grupės** numeris.

**Lentelės** vertė nurodo tinkamiausią įrašo tipą. Sistema visada naudoja šią reikšmę, net jei sukonfigūravote kitą įrašą, **kuriame pasirinkta reikšmė** **Grupė** arba Viskas. Ši vertė taip pat nepaiso visų verčių, kurias automatinių operacijų puslapyje **sukūrėte kaip numatytąsias** vertes.

Patariame naudoti lentelės **vertę** kaip pirminį registravimo šablonų valdymo mechanizmą, nes gali kilti duomenų kokybės problemų, jei kiekvienam pagrindinių duomenų įrašui tvarkomas atskiras registravimo šablonas. Taip pat sunku prižiūrėti ir suderinti atskirą registravimo šabloną kiekvienam pagrindinių duomenų įrašui. Vietoj to šią vertę reikia naudoti norint tvarkyti išimtis jūsų registravimo šablonuose.

### <a name="group-value"></a>Grupės vertė

Grupės **vertė** nurodo grupavimo įrašą, kurį palaiko bendrasis įrašas, susijęs su registravimo šablonu. Kiekvienas grupės įrašas turi konkrečią vertę. Jūs nurodote, kad vertė lauke, kuris yra po sąskaitos **kodo** lauko. Paprastai šis laukas būna pavadintas **Sąskaitos** arba **Sąskaitos/Grupės numeris**. Tikslus pavadinimas skiriasi, atsižvelgiant į lapą, kuriame jis rodomas.

Pirmiausiai **grupės** vertei reikia sukonfigūruoti grupę ir susieti ją su vienu ar daugiau abonemento įrašų. Grupės **vertė** yra mažiau konkreti nei lentelės **vertė**, bet labiau konkreti nei **vertė** Viskas. Jei lentelės įrašas nesukonfigūruotas, sistema bando rasti grupės, kuriai priklauso įrašas, įrašą.

Pavyzdžiui, jei dirbate su kliento registravimo šablonu, **·** **o** lauke Sąskaitos kodas pasirenkate Grupė, **lauke Sąskaitos / grupės numeris turite pasirinkti klientų** grupę. Turite iš anksto nurodyti klientų grupes klientų **grupės** puslapyje, o jūs turite nurodyti klientų grupę, kai kuriate klientą.

Jei turite sekti kelias šio registravimo tipo pagrindines sąskaitas, rekomenduojame naudoti grupės **vertę**. Pavyzdžiui, turite tris gautinų sumų prekybos pagrindines sąskaitas: vieną – įprastus klientus, vieną darbuotojams ir kitą – vidinės įmonės pardavimui. Tokiu atveju rekomenduojame sukurti tris klientų grupes klientams segmentuoti. Tada susiekite kiekvieną klientų grupę su teisinga pagrindine sąskaita kliento registravimo šablone. Toliau pateikiamoje lentelėje šiame pavyzdyje pateikiamos trys klientų grupės.

| Klientų grupė | Vardas | Aprašymas |
|----------------|------|-------------|
| EXT | Išorinis klientas | Ši grupė naudojama visiems standartiniams išoriniams klientams. |
| EMP | Darbuotojai | Ši grupė naudojama visiems darbuotojams, kurie perka iš jūsų organizacijos. |
| INT | Vidinės įmonės pardavimas | Ši grupė naudojama visoms vidinės įmonės klientų sąskaitoms, kurios naudojamos integruojant pardavimo ir pirkimo užsakymus. |

Tada registravimo šablone bus nustatytos trys eilutės. Kiekvienoje eilutėje pasirinkite Grupės **vertę** ir susijusią pagrindinę sąskaitą.

### <a name="all-value"></a>Visos vertės

Vertė **Viskas** nurodo, kad parametrai taikomi visiems įrašams. Jei lauke Sąskaitos kodas **pasirenkate** **vertę** Viskas, **laukas Sąskaitos/** grupės numeris yra negalimas ir negalite pasirinkti konkretaus įrašo, kuris bus taikomas konfigūracijai.

Vertė **Viskas** yra mažiausiai konkreti vertė. Jis naudojamas tik tada, jei sistema negali rasti verčių **Lentelė arba** Grupė **atitikties**. Turite pasirinkti vertę **Viskas**, kai konkrečiam registravimo tipui turite tik vieną pagrindinę sąskaitą.

Pavyzdžiui, kai dirbate su kliento registravimo šablonu, jūsų nurodomos pagrindinės sąskaitos taikomos visiems kitiems klientams ir klientų grupėms, kurios neturi konkrečios lentelės (kliento) arba grupės (klientų grupės) įrašo.

### <a name="category"></a>Kategorija

Atsargų registravimo šablonuose yra papildoma vertė, konkreti pardavimo arba įsigijimo kategorijai. Ši vertė panaši į **lentelės** vertę, nes ji taikoma tik konkrečiai pardavimo ar įsigijimo kategorijai.

### <a name="default-value"></a>Numatytoji reikšmė

Jei registravimo šablone, kuriame nustatytas sąskaitos kodo laukas Kaip Visi, nesukursite registravimo tipo įrašo, **o** sistema neranda atitinkančio registravimo šablono įrašo, esančio grupės arba lentelės **reikšmei**, sistema atkurs numatytąją vertę, kuri gali būti nurodyta automatinės **operacijos** puslapio sąskaitose.**·** **·** Daugiau informacijos ieškokite Automatinių [operacijų sąskaitos.](accounts-for-auto-transactions.md)

## <a name="clearing-accounts"></a>Kliringo sąskaitos

Kliringo *sąskaita* dažnai naudojama apskaitoje. Kai kurie registravimo tipai Microsoft Dynamics 365 programėlėse yra kliringo sąskaitos. Kitaip tariant, užregistrus kitą operaciją, sąskaitos balansas išvalomas arba atšaukiamas. Pavyzdžiui, registruojant pirkimo užsakymo produkto gavimo kvitą, įvertintos produktų savikainos suma plius mokestis ir visi mokesčiai pirkimo užsakymo eilutėse registruojami į pirkimo kaupimo registravimo tipą kaip įsipareigojimai. Vėliau, kai išrašote pirkimo užsakymo SF, balansas atšaukiamas iš pirkimo kaupimo registravimo tipo ir perkeliamas į mokėtinų sumų prekybos sąskaitą.

## <a name="additional-resources"></a>Papildomi ištekliai

Daugelis "Dynamics 365 Finance" Dynamics 365 Supply Chain Management Dynamics 365 Commerce Dynamics 365 Project Operations modulių ir turi registravimo šabloną arba papildomas konfigūracijas, kurios kontroliuoja, kaip veikia registravimas į DK. Norėdami daugiau sužinoti apie registravimo šablonus ir registravimo kiekviename modulyje nustatymus, naudokite šias temas:

- [Automatinių operacijų sąskaitos](accounts-for-auto-transactions.md)
- [Mokėtinų sumų registravimas](accts-payble-posting.md)
- [Gautinų sąskaitų registravimas](accts-recvble-posting.md)
- [Turto nuomos registravimas](../asset-leasing/set-up-lease-posting-accts.md)
- Turto valdymo registravimas (netrukus)
- Grynųjų pinigų ir banko valdymas (netrukus)
- Valiutos kurso pasikeitimo registravimo sąskaitos (netrukus)
- Išlaidų valdymo registravimas (netrukus)
- [Ilgalaikio turto registravimo šablonas](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Vidinės įmonės apskaitos registravimas (netrukus)
- Atsargų registravimo šablonas (netrukus)
- [Įkainojimo registravimas](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Registravimo aprašų peržiūra](posting-definitions.md)
- Gamybos kontrolės registravimas (netrukus)
- Projektų valdymo ir apskaitos registravimas (netrukus)
- Aptarnavimo valdymo registravimas (netrukus)
- Mokesčių registravimas (netrukus)
- Laiko ir lankomumo registravimas (netrukus)
- Transportavimo valdymo registravimas (netrukus)
- Grąžinimo valdymo registravimo profiliai (netrukus)
