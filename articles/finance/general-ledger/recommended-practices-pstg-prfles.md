---
title: Rekomenduojama šablonų registravimo praktika
description: Šiame straipsnyje aprašomos registravimo šablonų konfigūravimo rekomenduojamos praktikos.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb0e321f447b78b88c065e52bb7fad1c445e47b6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849908"
---
# <a name="recommended-practices-for-posting-profiles"></a>Rekomenduojama šablonų registravimo praktika

Yra keletas rekomenduojamų praktikų, kurių turėtumėte laikytis konfigūruodami registravimo šablonus visoje sistemoje. Šiame straipsnyje aprašomi skirtingi scenarijai ir atitinkama rekomenduojama praktika.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Įvedimo rankiniu būdu vėliavėlės nustatymas

Puslapyje Pagrindinės **sąskaitos** pažymėkite bet kurios **pagrindinės sąskaitos,** kuri naudojama registravimo šablone, žymės langelį Neleisti įvesti rankiniu būdu. Šis parametras neleidžia vartotojams neautomatiniu būdu registruoti žurnalo įrašo pagrindinėje sąskaitoje. Todėl tai padeda užtikrinti, kad papildomos knygos balansas lieka DK ir palengvina derinimo procesą.

Jei reikia sistemos kontroliuojamos ir automatiškai užregistruotos sąskaitos koregavimų, galite naudoti vieną iš šių būdų:

- Kurti antrinę pagrindinę sąskaitą, kurioje galima registruoti koregavimus. Tada, norėdami sugrupuoti ir sumuoti sąskaitas, savo finansinėse ataskaitose naudokite sąskaitą Bendra arba specialią eilutę.
- Atitinkamai papildomos knygos operacijas atšaukite, atlikite reikalingus pataisymus ir iš naujo užregistruoti operaciją naudodami tą pačią papildomos knygos informaciją.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Registravimo šablonų keitimas po operacijų egzistuoja

Jei po operacijų pakeisite registravimo šabloną, gali nepavykti suderinti, o jūsų antrinė knyga ir DK gali išeiti iš balanso. Apskritai, patariame nekeiskite registravimo **šablono** po to, kai egzistuoja operacija.

Jei reikia atlikti pakeitimus, norėdami užtikrinti sistemos vientisumą, naudokite šias gaires:

- Atlikite keitimus laikotarpio uždarymo metu.
- Atlikite pakeitimus, kai sistemoje nėra kitų operacijų.
- Prieš atlikę keitimus, patikrinkite DK ir suderinkite ją su papildomos knygos keitimus.
- Užregistruotos operacijos nėra atnaujinamos, jei keičiate registravimo šabloną. Atidžiai apsvarstykite, ar reikalaujama keiskite įrašus koreguojančių įrašų.
- Jei keičiate atsargų registravimo šablonus, apsvarstykite, kaip pakeitimai turės įtakos jūsų turimose atsargose ir DK balansams. Kai kurie pakeitimai gali reikalauti, kad atidarytų atsargas iki 0 (nulio), uždarytų atsargas ir tada atidarysite atsargas atgal po to, kai bus atlikti pakeitimai.
- Prieš pradėdami gamybą visada patikrinkite savo keitimus ne gamybos aplinkoje.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Duomenų bazės registravimo pakeitimų naudojimas audito šablonams atlikti

Apsvarstykite galimybę nustatyti kiekvieno registravimo šablono ir parametrų lentelių, kurios kontroliuoja registravimą, duomenų bazės registravimą. Tada, jei parametras arba profilis pakeičiamas, turite turėti visą audito įrašą apie tai, kokia vertė buvo pakeista, kas ją pakeitė, kada ji buvo pakeista ir kokia buvo ankstesnė vertė. Ši informacija gali būti svarbi derinimo proceso metu, o jūsų auditoriui gali reikėti patvirtinamųjų dokumentų.

Daugiau informacijos ieškokite Duomenų bazės registravimo [konfigūravimas](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Naudokite šią lentelę kaip nuorodą į bendrus lentelių pavadinimus, kurie yra susiję su registravimo šablonais ir susijusiais registravimo parametrais.

| Puslapio pavadinimas | Naršymo kelias | Lentelės pavadinimas |
|-----------|-----------------|------------|
| Mokėtinų sumų parametrai | Mokėtinų sumų &gt; nustatymo &gt; mokėtinų sumų parametrai | VendParm |
| Tiekėjų registravimo šablonas | Mokėtinų sumų &gt; nustatymo &gt; tiekėjo registravimo šablonas | VendPosting |
| Išlaidų kodas | Mokėtinų &gt; sumų mokesčių nustatymo &gt; mokesčių kodas arba gautinų sumų &gt; mokesčių nustatymo &gt; mokesčių kodas | MarkupTable |
| Mokėjimo būdai | Mokėtinų &gt; sumų mokėjimo &gt; nustatymo mokėjimo būdai | VendPaymMode |
| Mokėjimo nuolaidos | Mokėtinų &gt; sumų mokėjimo nustatymas &gt; Mokėjimo nuolaidos arba Gautinų sumų &gt; mokėjimo nustatymas &gt; Mokėjimo nuolaidos | "CashDisc" |
| Mokėjimo mokestis (tiekėjas) | Mokėtinų sumų &gt; mokėjimo nustatymo &gt; mokėjimo mokestis | VendPaymFee |
| Gautinų sumų parametrai | Gautinų sumų &gt; nustatymo &gt; gautinų sumų parametrai | CustParm |
| Kliento registravimo šablonai | Gautinų sumų &gt; nustatymas &gt; Kliento registravimo šablonas | CustPosting |
| Mokėjimo būdai | Gautinų &gt; sumų mokėjimų nustatymo &gt; mokėjimo metodai | CustPaymMode |
| Mokėjimo mokestis (klientas) | Gautinų sumų &gt; mokėjimų nustatymo &gt; mokėjimo metodai | CustPaymFee |
| Turto nuomos parametrai | Turto parametrai, per &gt; kuriuos &gt; buvo nustatyti turto parametrai | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Banko kodai | Grynųjų pinigų ir banko valdymo &gt; banko sąskaitos &gt; banko sąskaitos | BankAccountsTable |
| Banko operacijų tipai | Grynųjų pinigų ir banko valdymo &gt; nustatymas &gt; Banko operacijų tipai | BankTransType |
| Pašalinimo taisyklės | Konsolidacijos &gt; nustatymo pašalinimo &gt; taisyklė | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Išlaidų kategorijos | Išlaidų valdymo &gt; nustatymas &gt; Bendrosios išlaidų &gt; kategorijos | ProjCategories |
| Ilgalaikio turto parametrai | Ilgalaikio turto &gt; nustatymas &gt; Ilgalaikio turto parametrai | AssetParameters |
| Ilgalaikio turto registravimo šablonai | Ilgalaikio turto &gt; nustatymas &gt; Ilgalaikio turto registravimo profiliai | AssetLedgerAccounts<br>AssetDisposalParameters |
| Valiutos kurso perkainojimo sąskaitos | DK valiutos &gt; kurso pasikeitimo &gt; sąskaitos | CurrencyLedgerGainLossAccount |
| Automatinių operacijų sąskaitos | DK registravimo &gt; nustatymo sąskaitos &gt; automatinėms operacijoms | LedgerSystemAccounts |
| Vidinių įmonių apskaita | DK registravimo &gt; nustatymas &gt; vidinės įmonės sąskaitoms | DKįmonė |
| Operacijos registravimo aprašai | DK registravimo &gt; nustatymas Operacijos &gt; registravimo aprašai | JournalizingDefinitionTrans |
| Registravimo aprašai | DK registravimo &gt; nustatymo registravimo &gt; aprašai | JournalizingDefintion |
| Registravimas (atsargos) | Atsargų valdymo nustatymo &gt;&gt; registravimas &gt; | InventPosting |
| Išlaidų tipo kodai | Įkainojimo &gt; įkainojimo nustatymas &gt; Išlaidų tipo kodai | ITMCostTypeTable |
| Ištekliai | Gamybos kontrolės &gt; nustatymo &gt; išteklių &gt; ištekliai | WrkCtrTable |
| Išteklių grupės | Gamybos kontrolės &gt; nustatymo &gt; išteklių &gt; išteklių grupės | WrkCtrResourceGroup |
| Gamybos grupės | Gamybos kontrolės &gt; nustatymo &gt; gamybos &gt; grupė | ProdGroup |
| Išlaidų kategorijos | Gamybos valdymo nustatymo &gt; maršrutų &gt; išlaidų &gt; kategorijos | ProjCategory |
| Projektų grupės | Projekto valdymo ir apskaitos nustatymo &gt; registravimo &gt;&gt; projektų grupės | ProjGroup |
| DK registravimo nustatymas (projektai) | Projekto valdymo ir apskaitos nustatymo &gt; registravimo &gt; DK &gt; registravimo nustatymas | ProjPosting |
| Numatytoji korespondentinė sąskaita, skirta išlaidoms | Projekto valdymo ir apskaitos nustatymo &gt; numatytųjų &gt; korespondentinių &gt; sąskaitų, susijusių su išlaidomis, registravimas | ProjDefaultOffsetSetup |
| Grąžinimų valdymo registravimo šablonai | Grąžinimo valdymo &gt; grąžinimo valdymo registravimo nustatymas Grąžinimo &gt; valdymo registravimo profiliai | TAMRebatePosting |
| DK registravimo grupė (mokestis) | Mokesčių &gt; nustatymo &gt; PVM DK &gt; registravimo grupė | TaxAccountGroup (mokesčių inspekcija) |

## <a name="changing-groups-after-transactions-exist"></a>Grupių keitimas, kai yra operacijų

Keisti grupių pagrindinius duomenis būkite atsargūs. Jei naudodami grupes apibrėžiate registravimo šablonus, bet kokie pagrindinio įrašo grupės pakeitimas gali turėti neigiamos įtakos galimybėms suderinti DK su papildomos knygos grupe. Pavyzdžiui, galite konfigūruoti pardavimo užsakymo įplaukų atsargų registravimo šabloną, kad kiekvienai prekių grupei būtų naudojama skirtinga įplaukų sąskaita. Jeigu pakeičiate prekių grupę, priskirtą prekei po operacijų, naujų operacijų įplaukos bus registruojamos atnaujintoje sąskaitoje. Tačiau bet kokios įplaukos, užregistruotos prieš pakeitimą, liks pradinėje sąskaitoje.

## <a name="testing-posting-profiles"></a>Registravimo šablonų tikrinimas

Prieš pradėdami vykti ir atlikę bet kokius registravimo šablonų ar susijusių parametrų pakeitimus ar papildymus, turite išbandyti kiekvieną scenarijų. Turite patikrinti kiekvieną registravimo tipą, kad būtų patikrinta, ar teisingai veikia registravimas. Tačiau rekomenduojamas būdas yra tikrinti kiekvieną registravimo šablono operaciją ir derinį.

Pvz., turite du klientų registravimo šablonus, kurių kiekvienas turi tris įrašus, bvz., klientų grupes. Tokiu atveju turėtumėte patikrinti kiekvieną operacijos tipą.

**Registravimo šablonus:**

- **GEN** – bendrasis registravimo šablonas, kuris turi vieną darbuotojų grupę, vieną – klientams, o kitą – vid grupei. Kiekviena grupė nurodo skirtingą gautinų sumų prekybos sąskaitą.
- **PRE** – išankstinio apmokėjimo registravimo šablonas, kuriame yra vienas visų išankstinių apmokėjimų, kurie nurodo kliento iš anksto apmokėtų sąskaitų įrašus, įrašas.

### <a name="testing-scenarios"></a>Scenarijų tikrinimas

- Laisvos formos SF, skirta darbuotojų grupės **klientui**, kuris naudoja **GEN** registravimo šabloną
- Darbuotojo grupės, kuri naudoja IŠANKSTINIo registravimo **šabloną**, kliento **laisvos** formos SF
- Klientų grupės, kuri naudoja GEN registravimo **šabloną**, pardavimo **užsakymo** SF
- Darbuotojų grupės, kuri naudoja IŠANKSTINIo registravimo **šabloną**, kliento **pardavimo** užsakymo SF
- Klientų mokėjimų žurnalas, skirtas darbuotojų grupės klientui **,** kuris naudoja **GEN** registravimo šabloną
- Klientų mokėjimų žurnalas, skirtas darbuotojų grupės klientui **,** kuris naudoja išankstinio **registravimo** šabloną

Pateiktame pavyzdyje pakartokite vieną tikrinimo scenarijų kiekvienai klientų grupei ir pakartokite kiekvieną tikrinimo scenarijų grupę kiekvienam papildomam operacijos tipui (pavyzdžiui, projekto SF ir aptarnavimo valdymui).

## <a name="reconciling-the-ledger-to-the-subledger"></a>DK suderinimas su papildomos knygos

DK turi būti suderinta su ant papildomos knygos kiekvieną laikotarpį. Daugelyje modulių yra nenaudo naudojamų ataskaitų, kurias galima naudoti norint padėti atlikti šį suderinimą. Tačiau, atsižvelgiant į jūsų vietinį reikalavimus, jums gali tekti kurti pasirinktines ataskaitas arba išplėsti esamas ataskaitas, kad jos atitiktų jūsų ataskaitų reikalavimus.

Rekomenduojame prieš tiesioginio galiojimo laikotarpį suderinti kiekvieną papildomos knygos sumą su DK. Taip pat rekomenduojame prieš pradedant pirminę versti visus atvirus balansus ir atviras operacijas. Kaip šio proceso dalį turite vykdyti visą suderinimą, kad užtikrinti balansų perkėlimą ir atvirų operacijų balansą naudojant senąsias sistemas ir kad visi papildomos knygos balansai kartu su DK būtų sukurti prieš sukūrus naujas operacijas.
