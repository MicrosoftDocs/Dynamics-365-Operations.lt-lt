---
title: "Klientų kredito limitai"
description: "Šiame straipsnyje apžvelgiama, kaip programoje „Microsoft Dynamics 365 for Finance and Operations“ veikia kredito limitai."
author: omulvad
manager: AnnBe
ms.date: 09/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e00828ea24434da6dfd7443153b007ea728375f3
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="credit-limits-for-customers"></a>Klientų kredito limitai

[!include[banner](../includes/banner.md)]

Nustatę kredito limitą, galite nurodyti, kokią didžiausią kredito sumą galima suteikti klientams. Jei nurodytas kredito limitas, jis automatiškai patikrinamas vartotojui bandant atnaujinti dokumentą. Jei kredito limitas viršijamas, vartotojui rodomas pranešimas. Šiame straipsnyje apžvelgiama, kaip kredito limitai veikia, ir atsakoma į tolesnius klausimus.

-   Kokių dokumentų ir procesų kredito limitus galiu tikrinti?

-   Kur galiu sukonfigūruoti, kaip apskaičiuojamas kliento kredito likutis?

-   Kur naudojama informacija apie kliento kredito likutį?

-   Kur galiu nurodyti, ar, klientui suteikiant kreditą, klientą reikia identifikuoti, ir kredito limito sumą, kurią pasiekus klientą reikia identifikuoti?

-   Kur galiu nurodyti, ar, viršijus kredito limitą, rodyti įspėjimą arba klaidą?

-   Kaip nurodyti konkretaus kliento kredito limitą?

-   Kaip rankiniu būdu patikrinti pardavimo užsakymų kredito limitą?

**Kokių dokumentų ir procesų kredito limitus galiu tikrinti?**

Norėdami nurodyti, kurių dokumentų kredito limitus tikrinti, naudokite formą **Gautinų sumų parametrai**. Kad šioje formoje galėtumėte atlikti keitimus, turite būti saugos vaidmens Sistemos administratorius (-SYSADMIN-) narys. Galite tikrinti tolesnių dokumentų ir procesų kredito limitus.

-   Pardavimo užsakymų sąskaitos faktūros, jas registruojant

-   Pardavimo užsakymų važtaraščiai, juos naujinant

-   Pardavimo užsakymai, formoje **Pardavimo užsakymas** įtraukiant eilučių

-   Pardavimo užsakymai, kai jie kuriami naudojant tarnybą

-   Laisvos formos sąskaitos faktūros, jas registruojant

Kredito limitai automatiškai tikrinami, jei nustatyta kuri nors iš tolesnių parinkčių.

-   Formos **Gautinų sumų parametrai** laukas **Kredito limito tipas** nustatytas kitaip nei **Nėra**. Tikrinami visų klientų kredito limitai.

-   Formos **Gautinų sumų parametrai** laukas **Kredito limito tipas** nustatytas kaip **Nėra**, tačiau formoje **Klientai** prie kliento pasirinkta **Privalomas kredito limitas**. Tikrinami tik konkrečių klientų kredito limitai.

Norėdami tikrinti tolesnių dokumentų kredito limitus, turite nurodyti papildomus parametrus.

|    Dokumentas                                    |    Papildomas parametras                                                                                                             |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|    Laisvos formos sąskaita faktūra                         |    Formos Gautinų sumų parametrai srityje Kredito įvertinimas pasirinkite Tikrinti laisvos formos sąskaitos faktūros kredito limitą.     |
|    Pardavimo užsakymas (įvestas rankiniu būdu)            |    Formos Gautinų sumų parametrai srityje Kredito įvertinimas pasirinkite Tikrinti pardavimo užsakymo kredito limitą.           |
|    Pardavimo užsakymas (gautas elektroniniu būdu)     |    Formos Gautinų sumų parametrai srityje AIF pasirinkite Tikrinti pardavimo užsakymų kredito limitą.                     |

**Kur galiu sukonfigūruoti, kaip apskaičiuojamas kliento kredito likutis?**

Galite sukonfigūruoti, kad „Dynamics 365“ kliento kredito likutį apskaičiuotų bet kuriuo iš tolesnių būdų.

-   Kredito limitą lyginti su kliento balansu.

-   Kredito limitą lyginti su kliento balansu ir važtaraščio sumomis.

-   Kredito limitą lyginti su kliento balansu ir visomis pradėtomis operacijomis. Tai apima važtaraščio sumas ir pardavimo užsakymo sumas.

Informaciją, su kuria reikia lyginti kredito limitą, nurodykite naudodami formą **Gautinų sumų parametrai**. Kad šioje formoje galėtumėte atlikti keitimus, turite būti saugos vaidmens Sistemos administratorius (-SYSADMIN-) narys. Lauke **Kredito limito tipas** pasirinkite, ar reikia tikrinti kredito limitą, ir kokią informaciją apie operacijas įtraukti kredito limitą tikrinant. Pasirinkti iš šių pasirinkčių:

-   **Nėra** – kredito limitų netikrinti. Šios parinkties konkrečiam klientui galite netaikyti – formoje **Klientai** pažymėkite žymės langelį **Privalomas kredito limitas**. Tai padarius, kredito limitas tikrinamas pagal kliento balansą.

-   **Balansas** – kredito limitas tikrinamas pagal kliento balansą.

-   **Balansas + važtaraštis arba produkto gavimo kvitas** – kredito limitas tikrinamas pagal kliento balansą ir pristatymus.

-   **Balansas + visi** – Kredito limitas tikrinamas pagal kliento balansą, pristatymus ir atvirus užsakymus.

**Kur naudojama informacija apie kliento kredito likutį?**

Informacija apie kliento balansą ir likusią kredito sumą apskaičiuojama bei saugoma kuriant skirstymo pagal terminus momentinę kopiją ir rodoma formoje **Mokėjimų priežiūra**. Kol nebus sukurta nauja skirstymo pagal terminus momentinė kopija, į sumas, rodomas formoje **Mokėjimų priežiūra**, gali būti įtrauktos ne visos operacijos. Norėdami gauti daugiau informacijos, žr. [Mokėjimų priežiūra ir kreditas modulyje Gautinos sumos](https://technet.microsoft.com/en-us/library/hh209221.aspx).

Atsižvelgiant į pasirinktus dokumentus, informacija apie kliento balansą ir likusią kredito sumą apskaičiuojama atnaujinant pardavimo užsakymus, važtaraščius ir kliento sąskaitas faktūras. Jei dokumento, su kuriuo dirbate, suma viršija kredito limitą, rodomas pranešimas.

**Kur galiu nurodyti, ar, klientui suteikiant kreditą, klientą reikia identifikuoti, ir kredito limitą, kurį pasiekus klientą reikia identifikuoti?**

Tai, ar reikia identifikuoti klientą, ir kredito limito sumą, kurią pasiekus reikia identifikuoti klientą, nurodykite naudodami formą **Gautinų sumų parametrai**.
Kad šioje formoje galėtumėte atlikti keitimus, turite būti saugos vaidmens Sistemos administratorius (-SYSADMIN-) narys.

|    Laukas                                    |    aprašymas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Reikia identifikuoti suteikiant kreditą     |    Pasirinkite reikiamą įvesti klientų, kuriems jūsų juridinis subjektas suteikia kreditą, identifikavimo tipą. Šiame lauke jūsų pasirenkama parinktis lemia, kada ir kokio tipo informaciją reikia įvesti formos Klientai laukuose Vyriausybės registras: Ne – nepaisant kliento kredito limito, vyriausybės išduotos identifikacijos nereikia.     Taip – jei kliento kredito limitas didesnis nei nulis arba lygus nuliui, reikia vyriausybės išduoto licencijos numerio arba kitokios vyriausybės išduotos identifikacijos.     Mažiausias limitas – jei kliento kredito limitas yra didesnis už limitą, įvestą šios formos lauke Limitas, arba yra jam lygus, reikia vyriausybės išduoto licencijos numerio arba kitokios vyriausybės išduotos identifikacijos.        |
|    Riba                                    |    Įveskite kredito limitą, kurį pasiekus iš klientų reikalaujama vyriausybės išduoto licencijos numerio arba kitų identifikavimo duomenų.    Pavyzdžiui, įveskite 2000, kad identifikavimo numeris, pvz., vairuotojo pažymėjimo numeris, būtų įvestas, kai kredito limitas 2000 arba didesnis.    Šį lauką galima naudoti, jei lauke Reikia identifikuoti suteikiant kreditą pasirinkote Mažiausias limitas.                                                                                                                                                                                                                                                                                                                                                                                                                                         |

**Kur galiu nurodyti, ar, viršijus kredito limitą, rodyti įspėjimą arba klaidą?**

Norėdami nurodyti, ar, viršijus kredito limitą, reikia rodyti įspėjimą arba klaidą, naudokite formą **Gautinų sumų parametrai**. Toks įspėjimas arba tokia klaida rodomi vartotojui įvedant arba registruojant informaciją, arba, jei dokumentus apdoroja elektroninė tarnyba, įspėjimas arba klaida įtraukiami į žurnalą. Kad šioje formoje galėtumėte atlikti keitimus, turite būti saugos vaidmens Sistemos administratorius (-SYSADMIN-) narys.

|    Laukas                                                               |    aprašymas                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    Pranešimas viršijus kredito limitą (srityje Kredito įvertinimas)     |    Pasirinkite, kaip vartotojams rodomi pranešimai apie viršijamus kredito limitus. Pasirinkite vieną iš šių parinkčių: Klaida – rodomas klaidos pranešimas. Paprastai sustabdoma dabartinė operacija ir, norint tęsti procesą, problema turi būti išspręsta.     Įspėjimas – rodomas įspėjimo pranešimas, tačiau procesą galima tęsti.                     |
|    Pranešimas viršijus kredito limitą (srityje AIF)               |    Pasirinkite, kaip pranešimai apie viršijamus kredito limitus pateikiami žurnale. Pasirinkite vieną iš šių parinkčių: Klaida – formoje Išimtys rodomas klaidos pranešimas ir dokumentas nebus apdorojamas tol, kol klaida nebus pašalinta.     Įspėjimas – formoje Išimtys rodomas įspėjimo pranešimas, tačiau procesą galima tęsti.        |

**Kaip nurodyti konkretaus kliento kredito limito sumą?**

Norėdami nurodyti konkretaus kliento kredito limito sumą, naudokite formą **Klientai**. Norėdami šioje formoje atlikti keitimus, turite būti saugos vaidmens, kuriam priskirta pareiga Tvarkyti kliento bendruosius duomenis (CustCustomersMaintain), narys.

1.  Spustelėkite **Gautinos sumos** \> **Bendra** \> **Klientai** \> **Visi klientai**. Dukart spustelėkite kliento sąskaitą.

2.  Formos **Klientai** veiksmų srityje spustelėkite **Redaguoti**.

3.  Lauke **Kredito limitas** įveskite valiutos sumą. Ši reikšmė turi būti didesnė už nulį (0) ir ji bus naudojama kaip kredito limito suma.

4.  Jei reikia, lauke **Vyriausybės registras** įveskite licencijos numerį arba kitus vyriausybės išduotus identifikavimo duomenis.

> [!NOTE]
> Formoje **Gautinų sumų parametrai** paprastai pasirenkamas kredito limito tipas. Tačiau, jei kredito limito tipas nustatytas kaip **Nėra**, norėdami kliento kredito limitą palyginti su kliento balansu, taip pat turite formoje **Klientai** pažymėti žymės langelį **Privalomas kredito limitas**. Norėdami gauti daugiau informacijos apie kredito limito tipus, žr. „Kokių dokumentų ir procesų kredito limitus galiu tikrinti?“ šioje temoje. 

**Kaip rankiniu būdu patikrinti pardavimo užsakymų kredito limitą?**

Kartais gali tekti rankiniu būdu patikrinti kliento kredito limitą. Pavyzdžiui, rankiniu būdu patikrinti kliento kredito limitą galite prieš pradėdami įvedinėti pardavimo užsakymą. Rankiniu būdu tikrinti kredito limitus galite naudodami formą **Pardavimo užsakymas**. Norėdami šioje formoje atlikti keitimus, turite būti saugos vaidmens, kuriam priskirta pareiga Tvarkyti pardavimo užsakymą (SalesOrderMaintain), narys.

1.  Spustelėkite **Pardavimas ir rinkodara** \> **Bendra** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**. Dukart spustelėkite pardavimo užsakymą.

2.  Formos **Pardavimo užsakymas** veiksmų srities skirtuke **Valdyti** spustelėkite **Tikrinti kredito limitą**.

