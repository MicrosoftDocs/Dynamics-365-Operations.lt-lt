---
title: Pakankamų atsargų žurnalo naudojimas mažiausiam prekių padengimui atnaujinti
description: Šioje temoje aprašoma, kaip naudoti saugos atsargų žurnalą norint atnaujinti prekių atsargas, skaičiuojant minimalius padengimo pasiūlymus pagal retrospektyvias operacijas.
author: ChristianRytt
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 59e4959898cd961582e1ac1d2285c0c0867ee7af
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790985"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Pakankamų atsargų žurnalo naudojimas mažiausiam prekių padengimui atnaujinti

[!include [banner](../../includes/banner.md)]

Turimos atsargos nurodo papildomą atsargose laikomo prekės kiekį, siekiant sumažinti riziką, kad prekė išeis iš atsargų. Jei pardavimo užsakymai ateiti, kaip buferis naudojamos atsargos, tačiau tiekėjas negali atitikti kliento pageidaujamos siuntimo datos.

Šioje temoje aprašoma, kaip naudoti saugos atsargų žurnalą norint apskaičiuoti minimalius padengimo pasiūlymus, paremtus praeities operacijomis, ir tada atnaujinti prekės padengimą pasiūlymais.

## <a name="overview-of-minimum-coverage-usage"></a>Minimalaus padengimo naudojimo peržiūra

Kiekvienos prekės padengimo puslapyje **nustatytos atsargos, kurių reikia, kad būtų galima padengti** atsargas. Skirtingi papildymo tipai pateikiami skirtingais padengimo kodais. (Daugiau informacijos žr. [Prekių atsargų įvykdymo](safety-stock-replenishment.md) atsargos.) Tačiau visiems padengimo kodams naudojama kiekvienos prekės padengimo puslapio lauke Minimalus nustatyta vertė. Yra du pagrindiniai minimalaus lauko **naudojimo** būdai:

- **Minimalus kiekis min. /** maks. – taikant šį būdą minimalus kiekis naudojamas kartu su min. / maks. logika. Jis taikomas, kai **lauke** Padengimo kodas nustatyta atitinkamos *prekės ar* padengimo grupės min./maks. Minimalus **·** kiekis rodo vidutinį kasdienį naudojimą, padaugintą iš prekės gamybos laiko.
- **Minimalus atsargų plano paskirties kiekis – šiuo požiūriu naudojamas minimalus kiekis, kad būtų nurodytas atsargų planas kartu** su poreikio prognozėmis. Jis taikomas, **kai lauke** Padengimo kodas nustatyta atitinkamos prekės *ar* *·* padengimo grupės poreikis Laikotarpis arba Poreikis. Minimalus kiekis reiškia atsargų planą, atspindintį norimą klientų aptarnavimo lygį, siekiant padėti sumažinti medžiagų kiekį, dalinius siuntus ir **·** pristatymo vykdymo laiką. Mažiausias kiekis atspindi pateiktos prekės prognozės tikslumo procentą. Tai nėra pageidaujama atsargų padėtis.

Minimali **·** vertė gali būti nustatyta trimis būdais:

- Rankiniu būdu prekių **padengimo** puslapyje
- Pagal duomenų valdymo sistemą (prekės *padengimo* duomenų objektai)
- Pagal saugos atsargų skaičiavimą, kurį atliko sandėlio valdymo žurnalai

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Skaičiuoti minimalią padengimą pagal retrospektyvą

Turimų atsargų žurnalai naudojami apskaičiuoti siūlomą minimalų kiekį remiantis retrospektyviu prekės naudojimu, minimaliais / maksimaliais tikslais arba atsargų plano tikslais. Retrospektyvinis naudojimas rodo visas išdavimo operacijas nurodytu laikotarpiu. Šios išdavimo operacijos apima pardavimo užsakymo operacijas ir atsargų koregavimus. Skaičiuojant taip pat identifikuojami siūlomo minimalaus kiekio poveikis atsargų vertei ir atsargų vertės pokytis lyginant su esamais minimaliais kiekiais.

Kiekviena saugos atsargų žurnalo eilutė rodo prekę ir jos padengimo dimensijas. Šios žurnalo eilutės sukuriamos ir rodomos puslapyje Saugos **atsargų žurnalo** eilutės **(Bendrojo planavimo bendrasis planavimas Vykdyti atsargų \>\>\>** apsaugą). Verslo procesas, naudojamas kaip reikiamos atsargų žurnalai apskaičiuoti mažiausią siūlomą kiekį, aprašytas toliau šioje temoje.

Planuotojas naudoja saugos atsargų žurnalą, kad apskaičiuotų pasiūlytų minimalių pasirinktų prekių kiekius, pagrįstus retrospektyvu, naudojimu pasirinktų laikotarpių metu. Jei reikia, siūlomų minimalių verčių galima nepaisyti rankiniu būdu, taip pat galite peržiūrėti galimą siūlomų minimalių parametrų įtaką atsargų vertei. Užregistrus žurnalą, automatiškai atnaujinami susiję minimalūs prekių padengimo kiekiai.

### <a name="create-a-new-safety-stock-journal-name"></a>Kurti naują pakankamų atsargų žurnalo pavadinimą

Prieš generuodami šio tipo žurnalą turite sukurti bent vieną šio tipo atsargų žurnalo pavadinimą. Paprastai galite naudoti kelis žurnalų pavadinimus, kad būtų galima atskirti savo laiko atsargų skaičiavimus.

1. Eikite į **bendrojo planavimo \>\> nustatymą, jei norite naudoti kaip atsargos žurnalo** pavadinimus.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujoje eilutėje nustatykite šiuos laukus:

    - **Pavadinimas** – įveskite trumpą žurnalo pavadinimą.
    - **Aprašymas** – įveskite žurnalo aprašymą.
    - **Privatus vartotojų grupės** – norėdami apriboti šio žurnalo pavadinimo auditoriją, pasirinkite vartotojų grupę.
    - **Užregistr pasirinkę naikinti eilutes – pažymėkite šį žymės langelį, jei norite išvalyti žurnalo eilutes** pagal numatytuosius nustatymus jas užregistruodami. Išvalykite, kad išsaugokite visas užregistruotas eilutes.

    Laukas **Žurnalo** tipas skirtas tik skaityti, jis iš anksto nustatytas kaip *Turi būti* atsargos.

1. Uždarykite puslapį.

### <a name="create-a-safety-stock-journal-and-lines"></a>Kurti saugos atsargų žurnalą ir eilutes

Šiuo veiksmu sukuriamas žurnalas ir automatiškai į jį įtraukiamos eilutės. Kiekviena eilutė identifikuoja prekę, jos padengimo dimensijas ir kelis apskaičiuotus kiekius iš naudojimo retrospektyvos. Apskaičiuoti kiekiai apima vidutinius kiekvienos prekės gamybos laiko kiekius, vidutinį mėnesio nuokrypį ir mėnesio standartinį nuokrypį.

#### <a name="automatically-generate-journal-lines"></a>Automatiškai generuoti žurnalo eilutes

Žurnalo eilutes galima generuoti automatiškai, tik jei nėra dabar rodomos žurnalo eilučių.

Norėdami automatiškai sugeneruoti žurnalo eilutes, atlikite šiuos veiksmus.

1. Pereikite prie bendrojo **planavimo Bendrojo planavimo Vykdyti saugos atsargų \>\>\>** skaičiavimą.
1. Veiksmų srityje pasirinkite **Naujas**. Sukuriamas naujas saugos atsargų žurnalas.
1. Žurnalo **antraštės informacijos** "FastTab" nustatykite šiuos laukus:

    - **Pavadinimas** – pasirinkite safety stock žurnalo pavadinimą, į kurį reikia įtraukti eilutę.
    - **Aprašymas** – numatytoji vertė yra pasirinkto žurnalo pavadinimo aprašymas. Tačiau galite redaguoti vertę taip, kaip jums reikia.
    - **Užregistr pasirinkę naikinti** eilutes – pažymėkite šį žymės langelį, jei norite išvalyti žurnalo eilutes jas užregistruodami. Išvalykite, kad išsaugokite visas užregistruotas eilutes. Parametras perimamas iš pasirinkto žurnalo pavadinimo.

    Žurnalo laukas skirtas tik skaityti, jis rodo **·** kuriamo ir prie kurio pridedate eilutes, ID numerį.

1. Žurnalo **eilučių** "FastTab" įrankių **juostoje pasirinkite Kurti** eilutes.
1. Dialogo lange **Kurti žurnalo eilutes siūlomam minimalių atsargų** lygiui nustatykite šiuos laukus:

    - **Pradžios data** – pasirinkite laikotarpio, kurį išdavimai turi būti įtraukti į skaičiavimą, pradžios datą.
    - **Pabaigos data** – pasirinkti laikotarpio, kurį išdavimai turi būti įtraukti į šį skaičiavimą, pabaigos datą. Turi būti bent du mėnesiai nuo pradžios iki pabaigos datų.
    - **Apskaičiuoti standartinį** nuokrypį – nustatykite šią *pasirinktį kaip Taip,* norėdami apskaičiuoti standartinį nuokrypį. Norėdami naudoti pasirinktį Naudoti aptarnavimo lygį, kai skaičiuojate pasiūlymą, turite nustatyti šią pasirinktį *·* Taip **·** (kaip aprašyta toliau šioje temoje).

1. **Įrašuose, į kuriuos įtraukiama** "FastTab", galite nustatyti filtrus ir apribojimus, siekiant apibrėžti, kurios prekės yra įtrauktos. (Pvz., galite filtruoti pagal **Padengimo** grupės vertė.) Pasirinkite **·** Filtrą, norėdami atidaryti standartinį užklausų doroklį dialogo langą, kuriame galite nurodyti pasirinkimo kriterijus, rūšiavimo kriterijus ir jungtis. Šie laukai veikia kaip ir kitų tipų "Microsoft" Dynamics 365 Supply Chain Management užklausose.
1. Dalyje **Vykdyti fone** "FastTab" pasirinkite, ar užduotį vykdyti paketiniu režimu ir (arba) nustatyti pasikartojančią grafiką. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Pasirinkite **Gerai**. Sukuriamos dimensijų, kuriose yra atsargų operacijų, eilutės.

#### <a name="manually-add-or-remove-journal-lines"></a>Rankiniu būdu įtraukti arba šalinti žurnalo eilutes

Žurnalo eilutes galima pridėti ir (arba) šalinti neautomatiniu būdu bet kuriuo metu (po eilučių generavimo arba po to). Naudokite šiuos žurnalo eilučių **"FastTab" įrankių juostos** mygtukus:

- **Naujas** – pridėti naują eilutę. Tada kiekviename stulpelyje įveskite vertę, norėdami nurodyti produktą, suskaičiuoti ir taikyti naują minimumą. Nėra rankiniu būdu pridėtų eilučių siūlomų minimalių skaičiavimų, todėl joms **nerodoma naujų** apskaičiuotų minimalių kiekio verčių. Todėl naujo minimalaus kiekio vertes **turite įvesti neautomatiniu** būdu. Tačiau vis dar galite peržiūrėti galimą naujos minimalios kiekio vertės poveikį atsargų vertei ir galimą atsargų pokaitą lyginant su dabar **·** nurodytu minimumu.
- **Naikinti** – naikinti pasirinktą eilutę.
- **Naikinti žurnalo** eilutes – naikinti visas žurnalo eilutes.

### <a name="calculate-a-proposal"></a>Pasiūlymo skaičiavimas

Šis veiksmas apskaičiuoja kiekvienai žurnalo eilutei siūlomą minimalų minimumą ir galimą eilutės poveikį atsargų vertei. (Siūlomas minimumas rodomas kaip **Apskaičiuota minimali** kiekio vertė.) Jei reikia, skaičiavimą galite atlikti kelis kartus. Skaičiuojant atnaujinama visų **žurnalo eilučių** apskaičiuota minimalaus kiekio vertė.

Rodomi skaičiavimai neturės įtakos faktinėms minimalioms kiekvieno produkto kiekio vertėms, kol veiksmų srityje **·** nepasirinkote Registruoti. Tuo metu kiekvienam **produktui bus** taikomos naujos minimalaus kiekio vertės.

1. Pereikite prie bendrojo **planavimo Bendrojo planavimo Vykdyti saugos atsargų \>\>\>** skaičiavimą.
1. Atidarykite žurnalą, jei norite skaičiuoti pasiūlymą. Arba sukurkite naują žurnalą, kaip anksčiau aprašyta šioje temoje.
1. Žurnalo **eilučių** "FastTab" įrankių **juostoje pasirinkite Skaičiuoti** pasiūlymą. (Jums nereikia pasirinkti jokių eilučių.)
1. Dialogo lange **Minimalių atsargų lygio pasiūlymo** skaičiavimas nustatykite šiuos laukus:

    - **Gamybos laiko metu naudoti vidutinį išdavimą – pasirinkite šią pasirinktį norėdami sugeneruoti apskaičiuotas mažiausias kiekio vertes pagal vidutinį** **·** išdavimą per nurodytą laikotarpį. Tada lauke **Dauginimo koeficientas įveskite vertę, kad pagal tai būtų** galima koreguoti rezultatą. Pavyzdžiui, įveskite 1,0, jei norite naudoti tikslų apskaičiuotą vidurkį, arba 1,1, jei norite pridėti *·* papildomą *·* 10 procentų buferį.
    - **Naudoti aptarnavimo** lygį – pasirinkite šią pasirinktį, jei norite skaičiuoti siūlomą minimalų kiekį pagal norimą aptarnavimo lygį. Tada lauke **Aptarnavimo** lygis pasirinkite norimą aptarnavimo lygį.
    - **Gamybos laiko** marža – įveskite vertę, norėdami pratęsti įprastą gamybos laiką (pvz., leisti administravimui).
    - **Naudokite apskaičiuotą minimalų kiekį kaip naują minimalų kiekį – nustatykite šią pasirinktį kaip Taip, jei norite automatiškai kopijuoti vertes iš apskaičiuoto minimalaus kiekio stulpelio į naujo minimalaus kiekio stulpelį, kai skaičiavimas** *·* **·** **·** baigtas. Jei nustatote šią *pasirinktį kaip* Ne, dabartinė minimalaus kiekio vertė bus **·** nukopijuota į **visų eilučių stulpelį Naujas minimalus** kiekis. Tada turėsite rankiniu būdu redaguoti naujas **minimalaus kiekio** vertes, kaip jums reikia.

1. Dalyje **Vykdyti fone** "FastTab" pasirinkite, ar užduotį vykdyti paketiniu režimu ir (arba) nustatyti pasikartojančią grafiką. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Pasirinkite **Gerai**. Skaičiavimo rezultatai rodomi žurnalo eilučių **·** **"FastTab" stulpelyje Apskaičiuotas minimalus** kiekis. Dabar vertės yra tik siūlomos vertės, kurios jūsų produktams dar nebuvo taikomos.

### <a name="update-minimum-quantity"></a>Naujinti mažiausią kiekį

Galite pasirinkti bet kurią eilutę, kuri yra saugos atsargų žurnale ir rankiniu būdu perrašyti lauko **Naujas minimalus** kiekis vertę.

1. Pereikite prie bendrojo **planavimo Bendrojo planavimo Vykdyti saugos atsargų \>\>\>** skaičiavimą.
1. Atidaryti žurnalą, kad būtų galima redaguoti. Arba sukurkite naują žurnalą, kaip aprašyta anksčiau.
1. Žurnalo **eilučių** FastTab, raskite koreguotinas eilutes ir tada redaguokite vertę stulpelyje Naujas minimalus **·** kiekis. Pavyzdžiui, galite nustatyti naujo **minimalaus kiekio** vertę, kad ji sutaptų su **apskaičiuota minimalia kiekio** verte. Jei apskaičiuota **minimali kiekio vertė yra** *0* (nulis), galite įvesti norimą būsimą vertę.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Registruoti naują mažiausią kiekį ir patikrinti rezultatą

Norėdami užregistruoti naują minimalų kiekį ir patikrinti rezultatą, atlikite šiuos veiksmus.

1. Pereikite prie bendrojo **planavimo Bendrojo planavimo Vykdyti saugos atsargų \>\>\>** skaičiavimą.
1. Atidarykite žurnalą, kuriam norite registruoti naujus minimalius kiekius. Arba sukurkite naują žurnalą, kaip aprašyta anksčiau.
1. Veiksmų srityje pasirinkite **Registruoti**.
1. Dialogo lange **Registruoti** žurnalą nustatykite reikiamą **visų registravimo klaidų perkėlimą į naują** žurnalo lauką. Tada pasirinkite **Gerai,** kad būtų galima registruoti žurnalą.
1. Jei pakeitėte naujo minimalaus kiekio vertę žurnalo eilučių "FastTab" eilutėje, galite patvirtinti **·** **·** pakeitimą, atlikite šiuos veiksmus:

    1. Redaguotos eilutės prekės numerio stulpelyje pasirinkite **·** saitą.
    1. Dialogo lange Produkto informacija pasirinkite saitą lauke Prekės **·** **numeris, kad** atidarytumėte susijusį išleisto produkto įrašą.
    1. Veiksmų srities skirtuko **Planas** grupėje **Padengimas** pasirinkite **Prekės padengimas**.
    1. Atkreipkite dėmesį, kad minimali vietos ir sandėlio vertė, kurią pakoreguojate naudodami užregistruotą saugos atsargų žurnalą, dabar buvo atnaujinta, kad **·** atitiktų jūsų redagavimą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Prekių pakankamų atsargų pildymas](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
