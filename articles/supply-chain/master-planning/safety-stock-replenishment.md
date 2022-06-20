---
title: Prekių pakankamų atsargų pildymas
description: Šiame straipsnyje aptariamas nesamų atsargų įvykdyimas ir kaip nustatyti prekių atsargų kiekį.
author: t-benebo
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 70461ad1de94c984cb41e6b1d46af9e310a928d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887405"
---
# <a name="safety-stock-fulfillment-for-items"></a>Prekių pakankamų atsargų pildymas

[!include [banner](../includes/banner.md)]

Pakankamos atsargos nurodo papildomą prekės kiekį, laikomą atsargose siekiant sumažinti riziką, kad prekės nebus atsargose. Pakankamos atsargos yra naudojamas kaip buferinės atsargos tiems atvejams, kai gaunama pardavimo užsakymų ir tiekėjas negali pristatyti papildomų prekių kliento pageidaujamą siuntimo dieną. Kai pakankamos atsargos naudojamos pardavimo užsakymui įvykdyti, pakankamos atsargos bus sumažintos. Galite naudoti bendrojo planavimo funkciją, kad automatiškai atstatytumėte pakankamų atsargų lygį.

## <a name="set-up-safety-stock-levels-for-items"></a>Prekių pakankamų atsargų lygių nustatymas

Pakankamos atsargos nustatomos kaip prekių padengimo dalis puslapyje **Prekės apimtis** puslapyje skyriuje **Išleisti produktai \> Planas \> Padengimas**.

Lauke **Minimalus kiekis** įveskite minimalų prekės pakankamų atsargų kiekį lygį, kurį norite turėti. Vertė išreikšta atsargų vienetais. Jei paliksite lauką tuščią, numatytoji reikšmė bus nulinė. Šis laukas yra galimas sąraše **Padengimo kodas** pasirinkus **Laikotarpis**, **Poreikis** arba **Min. / maks.** Atsargų lygio apribojimas taikomas turimoms atsargoms, o tai reiškia, kad dėl rezervavimų ir žymėjimų gali būti vykdomas pakankamų atsargų papildymas prieš tai, kai faktinis kiekis būna mažesnis nei nurodytas minimalus lygis.

> [!NOTE]
> Norėdami apibrėžti lauką **Minimalus kiekis**, pirmiausia turite apibrėžti visas suplanuotas padengimo dimensijas. Tokiu būdu netinkamas įrašas nebus naudojamas bendrojo planavimo metu. Tokia situacija galima, jei, pvz., dimensijų grupė išplečiama įtraukiant papildomą suplanuotą padengimo dimensiją, kurios minimalus ir maksimalus atsargų kiekis dar nenurodytas.

Galite naudoti minimalius raktus, norėdami tvarkyti sezoninius poreikio svyravimus. Pavyzdžiui, galima sumažinti minimalų prekės atsargų lygį ne sezono metu ir palaipsniui kelti lygį kitais mėnesiais. Minimalų raktą galite kurti pasirinkdami **Bendrasis planavimas \> Sąranka \> Padengimas \> Minimalūs / maksimalūs raktai**. Minimalus raktas nurodomas norint koreguoti pakankamų atsargų lygį pagal sezonus puslapio **Prekės padengimas** lauke **Minimalus raktas**.

## <a name="example-minimum-key"></a>Pavyzdys: minimalus raktas

Toliau pateikiama procedūra yra pavyzdys, kuriame parodyta, kaip nustatyti minimalų raktą, kuris abonementų nuo padidėjusios sezoninio poreikio per atostogas ir vasaros mėnesius.

1. Pasirinkite **Bendrasis planavimas \> Sąranka \> Padengimas \> Minimalūs ar maksimalūs raktai**.
1. Pasirinkite **Naujas** jei norite sukurti minimumo ar maksimumo raktą.
1. **Minimalaus arba maksimalaus** rakto lauke įveskite rakto identifikatorių. Lauke **Pavadinimas** įveskite šablono raktą.
1. Nustatykite parinkt **Naudoti įsigaliojimo datą** kaip *Taip* ir palikite lauką **Galioja data tuščią** tam, kad raktas galiotų nuo pirmos šių metų dienos.

    > [!NOTE]
    > Naudojimo įsigaliojimo **datos ir galiojimo datos** ir **parametrų kombinacija** nurodo datą, nuo kurios galioja raktas.
    >
    > - Kai parinktis **Naudoti įsigaliojimo datą** nustatyta kaip *Ne*, raktas galioja nuo dabartinės datos arba sistemos datos.
    > - Kai **Naudoja galiojimo datos** parinktis nustatyta į *Taip*, raktą, kuris yra galiojantis nuo datos, kuris nustatyta **Galiojimo data** lauke.

1. Skyriuje **Laikotarpiai** sukurkite 12 eilučių ir nustatykite joms šias vertes:

    - **Keisti** – priskirkite kiekvienai eilutei unikalų numerį nuo 1 iki 12. Šis laukas nurodo didėjantį laiko vieneto, kurį nurodo laukas **Vienetas** pokyį.
    - **Vienetas** – pasirinkite mėnesius kiekvienai *eilutei*.
    - **Nuo datos**, **Iki datos** ir **Mėnuo** šie laukeliai yra nustatyti automatiškai, reminatis **Pokyčiu** ir **Vieneto** nustatymais. Mėnesio laikotarpiai prasideda nuo pirmos šių metų dienos.
    - Lauke **Faktorius** įveskite reikšmes, aprašytas toliau pateikiamoje lentelėje. Šis laukas nurodo koeficientą, iš kurio norite dauginti minimalias atsargas.

        | Eilutė (keitimas) | Koeficientas | Rezultatas |
        |---|---|---|
        | 1–3 | 1 | Minimalios atsargos priklauso nuo puslapyje **Prekės padengimas** nurodyto nustatymo, skirto sausio iki kovo mėnesiams. |
        | 4–5 | 2 | Minimalios balandžio–gegužės atsargos padauginamos iš koeficiento 2. |
        | 6–8 | 2.5 | Minimalios atsargos birželiui – rugpjūčiui padauginamos iš koeficiento 2,5. |
        | 9–12 | 1 | Minimalios atsargos grąžinamos į puslapyje **Prekės padengimas** nurodytą parametrą, skirtą rugsėjo–gruodžio mėnesiams. |

    Dabar jūsų nustatymai turi būti panašūs į šiame pavyzdyje pateikiamus parametrus.

    ![Minimalūs arba maksimalūs raktų laikotarpiai.](media/min-max-key-periods.png "Minimalūs arba maksimalūs raktų laikotarpiai")

> [!NOTE]
> Galite naudoti šį vedlį, jei norite kurti ar nustatyti minimalų/maksimalų raktą. Minimalių **arba maksimalių raktų** puslapyje veiksmų srityje pasirinkite **Vedlį,** kad atidarytumėte **minimalių/maksimalių raktų vedlį**. Vedlys padės jums pereiti po žingsnio, kaip kurti ir nustatyti minimalų/maksimalų raktą.

Jei padengimo kodas yra *Min/Maks.*, taip pat galite nurodyti maksimumą inventoriaus kokybę, kurią norite išlaikyti prekei. Reikšmė taip pat išreikšta atsargų vienetais. Kai numatomų turimų atsargų kiekis tampa mažesnis nei minimalus, bendrasis planavimas generuoja suplanuotą užsakymą, kad išpildytų visus atvirus poreikius, ir atstato atsargų kiekį iki nurodyto maksimalaus kiekio. Kaip prieš nustatydami lauką minimalus inventoriaus kiekis, turite nustatyti kitas suplanuotas aprėpties dimensijas prieš tai, kai nustatysite **Maksimalų** lauką.

## <a name="example-minmax-coverage-code"></a>Pavyzdys: min. / maks. padengimo kodas

Minimalus kiekis yra 10, o maksimalus – 15. Esamos turimos atsargos yra 4. Todėl minimalus kiekio poreikis yra 6. Tačiau, kadangi maksimalus kiekis yra 15, bendrasis planavimas generuoja suplanuotą 11 prekių užsakymą.

Jei prekių poreikis priklauso nuo sezono, gali tekti nustatyti skirtingus maksimalius lygius. Norėdami tai padaryti, turite nustatyti parametrą **Maksimalūs raktai** ir eikite į **Bendrasis planavimas \> Sąranka \> Padengimas \> Minimalūs/maksimalūs raktai**. Užpildykite lauką **Maksimalus raktas** puslapyje **Prekės padengimas**. Galite peržiūrėti informaciją apie pakankamų atsargų lygius, nurodytą naudojant minimalius raktus, puslapio **Prekės padengimas** skirtuke **Min. / maks.** Turite įsitikinti, kad tam tikrą laikotarpį mažiausia ir didžiausia reikšmės yra sinchronizuojamos.

## <a name="safety-stock-fulfillment"></a>Pakankamų atsargų pildymas

Parametras **Pripildyti minimalų kiekį** suteikia galimybę pasirinkti datą arba laikotarpį, per kurį atsargų lygis turi atitikti lauke **Minimalus kiekis** nustatytą kiekį. Šis laukas yra galimas sąraše **Padengimo kodas** pasirinkus **Laikotarpis**, **Poreikis** arba **Min. / maks.**

Jei naudojama parinktis **Minimalūs raktai**, pažymėkite žymės langelį **Minimalaus kiekio laikotarpiai**, jei norite pasiekti visų laikotarpių, kurie yra nustatyti minimaliame rakte, minimalų atsargų lygį. Jeigu žymės langelis yra išvalomas, minimalios atsargos yra pripildomos tik per esamą laikotarpį.

Toliau pateiktame scenarijuje parodyta, kaip šis parametras veikia ir kuo skiriasi jo reikšmės.

> [!NOTE]
> Visuose šio straipsnio pavyzdžiuose x ašyje vaizduojamos atsargos, y ašis reiškia dienas, juostos reiškia atsargų lygį, rodyklės reiškia operacijas, pvz., pardavimo užsakymo eilutes, pirkimo užsakymo eilutes arba suplanuotus užsakymus.

[![Įprastas saugos atsargų pildymo scenarijus.](media/Scenario1.png)](media/Scenario1.png)

Parametro **Užpildyti minimumą** reikšmės gali būti tokios:

### <a name="todays-date"></a>Šiandienos data

Nurodytas minimalus kiekis yra pasiektas bendrojo planavimo vykdymo dieną. Sistema bando pripildyti pakankamas atsargas iki ribos kuo greičiau, nors jis dėl gamybos laiko tai gali būti nerealu.

[![Šiandienos datos poreikis.](media/TodayReq.png)](media/TodayReq.png)

Šiandieną sukuriamas suplanuotas užsakymas P1, kad šią dieną turimų atsargų lygis viršytų pakankamų atsargų lygį. Pardavimo užsakymo eilutės S1–S3 toliau mažina atsargų lygį. Bendrasis planavimas sugeneruoja suplanuotus užsakymus P2–P4, kad atsargų lygis vėl būtų pripildytas iki pakankamų atsargų ribos po kiekvieno pardavimo užsakymo poreikio patenkinimo.

Kai **poreikio** padengimo kodas naudojamas, kuriami keli suplanuoti užsakymai. Tai visada patartina naudoti prekių ir medžiagų padengimo kodą **Laikotarpis** arba **Min. / maks.**, kai poreikis dažnai kinta, kad būtų galima grupuoti papildymus. Tolesnėje iliustracijoje parodytas padengimo kodo **Laikotarpis** pavyzdys.

[![Laikotarpis. Šiandienos data.](media/TodayPeriod.png)](media/TodayPeriod.png)

Tolesnėje iliustracijoje parodytas padengimo kodo **Min / Maks** pavyzdys.

[![Min./Maks. Šiandienos data.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Šiandienos data + pirkimo laikas

Nurodytas minimalus kiekis yra pasiektas bendrojo planavimo vykdymo dieną pridėjus pirkimo ar gamybos laiką. Įskaičiuojami visi laiko rezervai. Jei pasirašyta prekei skirta prekybos sutartis ir yra pažymėtas puslapio **Bendrojo planavimo parametrai** žymės langelis **Rasti prekybos sutartis**, pristatymo vykdymo laikas iš prekybos sutarties nėra įskaičiuojamas. Vykdymo laikas yra imamas iš prekės padengimo nustatymų arba iš prekės.

Šis pildymo režimas sukurs planus su mažiau vėlavimo atvejų ir mažiau suplanuotų užsakymų, nepriklausomai nustatytą prekės padengimo grupę.

Tolesnėje iliustracijoje parodytas plano rezultatus, jei padengimo kodas yra **Poreikis** arba **Laikotarpis**.

[![Poreikis ar Laikotarpis. Šiandienos data ir gamybos laikas.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

Tolesnėje iliustracijoje parodytas plano rezultatus, jei padengimo kodas yra **Min / Max**.

[![Min./Maks. Šiandienos data ir gamybos laikas.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>Pirmas išdavimas

Nurodytas minimalus kiekis yra pasiektas tą dieną, kai turimų atsargų kiekis yra mažesnis nei minimalus lygis, kaip pavaizduota tolesnėje iliustracijoje. Net jei turimų atsargų kiekis yra mažesnis už minimalų lygį tą dieną, kai paleidžiamas bendrasis planavimas, **Pirmasis išdavimas** nebandys jo padengti, kol nepasikeis poreikis.

Tolesnėje iliustracijoje parodytas padengimo kodo **Poreikis** pavyzdys.

[![Prekės planavimas naudojant padengimo kodą Poreikis ir pildymą Pirmasis išdavimas.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

Tolesnėje iliustracijoje parodytas padengimo kodo **Laikotarpis** pavyzdys.

[![Prekės planavimas naudojant padengimo kodą Laikotarpis ir pildymą Pirmasis išdavimas.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

Tolesnėje iliustracijoje parodytas padengimo kodo **Min / Maks** pavyzdys.

[![Prekės planavimas naudojant padengimo kodą MinMax ir pildymą Pirmasis išdavimas.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

Jei tą dieną, kai paleidžiamas bendrasis planavimas, turimų atsargų kiekis jau yra mažesnis nei pakankamų atsargų riba, parinktys **Šiandienos data** ir **Šiandienos data + įsigijimo laikas** suaktyvins papildymą iš karto. **Pirmasis išdavimas** lauks, kol yra pradėta kita prekės išdavimo operacija, pvz., pardavimo užsakymo ir KS eilutės poreikis, ir tada jis suaktyvins papildymą šios operacijos dieną.

Jei tą dieną, kai paleidžiamas bendrasis planavimas, turimų atsargų kiekis nėra mažesnis nei pakankamų atsargų riba, parinktys **Šiandienos data** ir **Pirmasis išdavimas** pateiks tokį patį rezultatą, kaip parodyta tolesnėje iliustracijoje.

[![Riboti negalima.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

Jei tą dieną, kai paleidžiamas bendrasis planavimas, turimų atsargų kiekis nėra mažesnis nei pakankamų atsargų riba, parinktis **Šiandienos data + pirkimo laikas** pateiks toliau nurodytą rezultatą, nes ji atidės pildymą iki įsigijimo gamybos laiko pabaigos.

![Įvykdymo atidėjimas iki įsigijimo vykdymo laiko pabaigos.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Padengimo laiko ribos

Nurodytas minimalus kiekis pasiekiamas per lauke **Padengimo laiko riba** nustatytą laikotarpį. Ši pasirinktis yra naudinga, kai bendrojo planavimo metu negalima turimų atsargų naudoti norint įvykdyti realius užsakymus, pvz., pardavimo arba perkėlimo užsakymus, kad būtų palaikytas pakankamų atsargų lygis. Tačiau būsimame leidime šis papildymo būdas nebebus reikalingas ir ši parinktis nebebus naudojama.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Tipo „pirmas baigė galioti – pirmas baigėsi“ (FEFO) prekių pakankamų atsargų papildymo planas

Bet kuriuo metu, atsargų gavimas su naujausia galiojimo data bus naudojamas pakankamoms atsargoms pildyti, kad FEFO („pirmas baigė galioti – pirmas baigėsi“) užsakyme būtų patenkintas realus poreikis, pvz., pardavimo arba KS eilučių.

Norėdami suprasti, kaip tai veikia, peržiūrėkite toliau pateikiamą pavyzdį.

[![FEFO scenarijus.](media/FEFOScenario.png)](media/FEFOScenario.png)

Paleidus planavimą, pirmasis pardavimo užsakymas bus padengtas iš esamų turimų atsargų ir papildomas pirkimo užsakymas bus padengtas naudojant likusį kiekį.

[![FEFO 1.](media/FEFO1.png)](media/FEFO1.png)

Suplanuotas užsakymas sukuriamas norint užtikrinti, kad turimų atsargų kiekis atstatomas iki pakankamų atsargų ribos.

[![FEFO 2.](media/FEFO2.png)](media/FEFO2.png)

Suplanavus antrąjį pardavimo užsakymą, šiam kiekiui padengti naudojamas anksčiau sukurtas suplanuotas užsakymas, padengiantis pakankamas atsargas. Todėl pakankamos atsargos yra nuolat pildomos.

[![FEFO 3.](media/FEFO3.png)](media/FEFO3.png)

Galiausiai, kitas suplanuotas užsakymas sukuriamas pakankamoms atsargoms padengti.

[![FEFO 4.](media/FEFO4.png)](media/FEFO4.png)

Visi paketai atitinkamai baigia galioti, o galiojimui pasibaigus suplanuoti užsakymai kuriami norint papildyti pakankamas atsargas.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Kaip bendrasis planavimas apdoroja pakankamų atsargų ribą

Pakankamos atsargos sistemoje sekamos kaip poreikio tipas – kaip pardavimo eilučių arba KS poreikiai. Pakankamų atsargų poreikio eilutę galite peržiūrėti puslapyje **Grynieji poreikiai**, jei iš stulpelio **Poreikio tipas** pašalinsite numatytąjį filtrą.

Pakankamų atsargų poreikio pildymo operacijos prioritetas sumažinamas, jei sistema nustato, kad dėl to vėluojama tenkinti realų poreikį, pvz., pardavimo eilutes, KS eilutes, perkėlimo poreikius arba poreikio prognozės eilutes. Priešingu atveju užtikrinimui, kad turimų atsargų kiekis yra didesnis nei pakankamų atsargų kiekis, skiriamas toks pat prioritetas kaip kitiems poreikio tipams. Taip užtikrinama, kad nevėluotų realios operacijos, ir padedama išvengti atvejų, kai pakankamos atsargos papildomos per daug arba per anksti.

Bendrojo planavimo padengimo etapo metu pakankamų atsargų papildymo prioritetas nebėra mažinamas. Turimas atsargas galima naudoti prieš bet kokį kitą poreikio tipą. Skaičiuojant atidėjimą, įtraukiama nauja logika atidėtų pardavimo eilučių, KS eilučių poreikiams ir visų kitų tipų poreikiui patikrinti, kad būtų nustatyta, ar jie gali pristatyti laiku, jei naudojamos pakankamos atsargos. Jei sistema nustato, kad atidėjimas gali būti sumažintas naudojant pakankamas atsargas, tada pradinis pardavimo eilučių arba KS eilučių padengimas bus pakeistas pakankamomis atsargomis, o sistema suaktyvins papildymą naudojant pakankamas atsargas.

Jei nenustatytas plano ar prekės atidėjimo skaičiavimas, tada pakankamų atsargų apribojimo prioritetas bus toks pat kaip bet kurio kito tipo poreikio prioritetas. Tai reiškia, kad yra turimų ir kitų atsargų rezervas prieš kitų tipų poreikį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Pakankamų atsargų žurnalo naudojimas mažiausiam prekių padengimui atnaujinti](safety-stock-journal.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
