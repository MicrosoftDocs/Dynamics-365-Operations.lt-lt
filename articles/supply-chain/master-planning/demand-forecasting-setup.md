---
title: Poreikio prognozių nustatymas
description: Šiame straipsnyje aprašomos nustatymo užduotys, kurias turite atlikti, norėdami pasiruošti poreikio prognozei.
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10a211e0e20f22dfbfdb4923841808750b6ed71b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901008"
---
# <a name="demand-forecasting-setup"></a>Poreikio prognozių nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti poreikio prognozę.  

## <a name="item-allocation-keys"></a>Prekių paskirstymo raktai

Prekių paskirstymo raktai sudaro prekių grupes. Poreikio prognozė skaičiuojama pagal prekę ir jos dimensijas tik tada, jei prekė yra prekių paskirstymo rakto dalis. Ši taisyklė taikoma grupuoti didelius prekių numerius, kad poreikio prognozės būtų kuriamos greičiau. Prognozės kuriamos remiantis tik retrospektyviniais duomenimis.

Prekė ir jos dimensijos turi būti tik vieno prekių paskirstymo rakto dalis, jei prekių paskirstymo raktas naudojamas kuriant prognozę.

Norėdami sukurti prekių paskirstymo raktus ir į juos įtraukti atsargų vienetą (SKU), atlikite šiuos veiksmus.

1. Eikite į **Bendrasis planavimas \> Nustatymas \> Poreikio prognozė \> Prekės paskirstymo raktai**.
1. Sąrašo srityje pasirinkite prekių paskirstymo raktą arba veiksmų srityje **pasirinkite** Naujas, kad sukurtumėte naują. Naujo ar pasirinkto rakto antraštėje nustatykite šiuos laukus:

    - **Prekių paskirstymo** raktas – įveskite unikalų rakto pavadinimą.
    - **Pavadinimas** – įveskite aprašomąjį rakto pavadinimą.

1. Norėdami įtraukti prekes į pasirinktą prekių paskirstymo raktą arba pašalinti prekes, atlikite vieną iš šių veiksmų:

    - Norėdami pridėti **ar pašalinti prekes**, "FastTab" prekių **paskirstymo** **metu naudokite** įrankių juostos mygtukus Naujas ir Naikinti. Kiekvienoje eilutėje pasirinkite prekės numerį, tada, jei reikia, priskirkite dimensijų vertes kituose stulpeliuose. Pasirinkite **Rodyti dimensijas** įrankių juostoje, kad pakeistumėte tinklelyje rodomų dimensijų stulpelių rinkinį. (Vertė lauke **Procentų** stulpelio nepaisoma, kai generuojamos poreikio prognozės.)
    - Jei į raktą norite įtraukti daug elementų, norėdami atidaryti puslapį, kuriame galite rasti ir priskirti kelis elementus pasirinktam raktui, **pasirinkite** Priskirti elementus veiksmų srityje.

> [!IMPORTANT]
> Būkite atsargūs, kad į kiekvieną prekių paskirstymo raktą būtų įtrauktos tik atitinkamos prekės. Nereikalingos prekės gali padidinti išlaidas, kai naudojate „Microsoft Azure“ mašininį mokymą.

## <a name="intercompany-planning-groups"></a>Vidinės įmonės planavimo grupės

Poreikio prognozė gali generuoti kelių įmonių prognozes. Įmonės Dynamics 365 Supply Chain Management, kurios yra planuojamos kartu, yra sugrupuotos į tą pačią vidinės įmonės planavimo grupę. Norėdami nurodyti, pagal įmonę, į kuriuos prekių paskirstymo raktus reikia atsižvelgti poreikio prognozėje, susiekite prekių paskirstymo raktą su vidinės įmonės planavimo grupės nariu.

> [!IMPORTANT]
> Planavimo optimizavimas šiuo metu nepalaiko vidinės įmonės planavimo grupių. Norėdami atlikti vidinės įmonės planavimą, naudojantį planavimo optimizavimą, nustatykite bendrojo planavimo paketines užduotis, į kurias įtraukti visų susijusių įmonių esantys esantys planai.

Norėdami nustatyti savo vidinės įmonės planavimo grupes, atlikite šiuos veiksmus.

1. Pereikite prie **bendrojo planavimo \> nustatymo \> vidinės įmonės planavimo grupių**.
1. Pasirinkite planavimo grupę sąrašo srityje arba veiksmų srityje **pasirinkite** Nauja, kad sukurtumėte naują. Naujos ar pasirinktos grupės antraštėje nustatykite šiuos laukus:

    - **Pavadinimas** – įveskite unikalų planavimo grupės pavadinimą.
    - **Aprašymas** – įveskite trumpą planavimo grupės aprašymą.

1. Vidinės įmonės **planavimo grupės narių** "FastTab" naudokite įrankių juostos mygtukus, norėdami pridėti kiekvienos įmonės (juridinio subjekto), kuri turi būti grupės dalis, eilutę. Kiekvienai eilutei nustatykite šiuos laukus:

    - **Juridinis** subjektas – pasirinkite įmonės (juridinio subjekto), kuri yra pasirinktos grupės narys, pavadinimą.
    - **Planavimo seka** – priskirkite užsakymą, pagal kurį įmonė turėtų būti apdorota kitų įmonių atžvilgiu. Pirmiausia apdorojamos mažos vertės. Šis užsakymas gali būti svarbus, kai vienos įmonės poreikis veikia kitas įmones. Tokiais atvejais įmonė, tiekiančių poreikį, turi būti apdorota paskutinį kartą.
    - **Bendrasis planas** – pasirinkite dabartinės įmonės bendrąjį planą, kuris turi būti suaktyvintas.
    - **Automatinis kopijavimas į statinį** planą – pažymėkite šį žymės langelį, jei norite plano rezultatą nukopijuoti į statinį planą.
    - **Automatinis kopijavimas į dinaminį** planą – pažymėkite šį žymės langelį, jei norite kopijuoti plano rezultatą į dinaminį planą.

1. Pagal numatytuosius parametrus, jei prekių paskirstymo raktai nėra priskirti vidinės įmonės planavimo grupės nariams, skaičiuojama visų prekių, priskirtų visiems prekių paskirstymo raktams iš visų įmonių, poreikio prognozė. Papildomos filtravimo pasirinktys, susijusios su įmonėmis **ir** prekių paskirstymo raktais, yra dialogo lange Generuoti pagrindinės statistinės prognozės prognozę (Bendrojo **planavimo \>\>\> poreikio prognozės generavimas pagrindinė statistinė prognozė**). Norėdami priskirti prekių paskirstymo raktus įmonei pasirinktoje vidinės įmonės planavimo grupėje, pasirinkite įmonę, **tada** vidinės įmonės planavimo grupės narių "FastTab" įrankių **juostoje** pasirinkite Prekių paskirstymo raktus.

> [!IMPORTANT]
> Būkite atsargūs ir įtraukite tik atitinkamus prekių paskirstymo raktus į kiekvieną vidinės įmonės planavimo grupę. Nereikalingos prekės gali padidinti išlaidas, kai naudojate "Azure" mašinos mokymą.

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a> Poreikio prognozės parametrų nustatymas

Naudokite puslapį **Poreikio prognozės parametrai**, norėdami nustatyti kelias pasirinktis, kurios kontroliuoja, kaip poreikio prognozė veikia jūsų sistemoje.

### <a name="open-the-demand-forecasting-parameters-page"></a>Atidarykite poreikio prognozės parametrų puslapį

Norėdami nustatyti poreikio prognozės parametrus, eikite į bendrojo **planavimo nustatymą \> Poreikio \> prognozės poreikio \> prognozės parametrai**. Kadangi vykdoma visų įmonių poreikio prognozė, sąranka yra visuotinė. Kitaip tariant, ji taikoma visiems juridiniams subjektams (įmonėms).

### <a name="general-settings"></a>Bendrieji parametrai

Naudokite poreikio **prognozės** parametrų **puslapio skirtuką Bendra,** norėdami nustatyti bendruosius poreikio prognozės parametrus.

#### <a name="demand-forecast-unit"></a>Poreikio prognozės vienetas

Poreikio prognozės generuoja prognozes, išreikštas kiekiais. Todėl lauke **Poreikio prognozės vienetas** reikia nurodyti matavimo vienetą, kuriuo prognozė turi būti išreikšta. Šis laukas nurodo vienetą, kuris bus naudojamas visose poreikio prognozėse, nepaisant įprastų kiekvieno produkto atsargų vienetų. Naudodami nuoseklią prognozės vienetą galite užtikrinti, kad telkimo ir procento paskirstymas būtų logiškas. Daugiau informacijos apie telkimą ir paskirstymo procentą žr. [Neautomatinis pagrindinės prognozės koregavimas](manual-adjustments-baseline-forecast.md).

Kiekvieno matavimo vieneto, kuris naudojamas SKU ir kuris įtrauktas į poreikio prognozę, atveju įsitikinkite, kad yra matavimo vieneto konvertavimo taisyklė ir bendrasis čia pasirenkate prognozės matavimo vienetas. Kai generuojate prognozę, užregistruojamas prekių, kurios neturi matavimo vienetų konvertavimo, sąrašas. Todėl nustatymą galima lengvai koreguoti. Daugiau informacijos apie matavimo vienetus ir apie tai, kaip iš jų konvertuoti, ieškokite [Valdyti matavimo vienetus](../pim/tasks/manage-unit-measure.md).

#### <a name="transaction-types"></a>Operacijų tipai

Norėdami pasirinkti operacijų tipus **, kurie** naudojami generuojant bazinę statistinę prognozę, naudokite "FastTab" operacijų tipų laukus.

Poreikio prognozę galima naudoti norint prognozuoti ir priklausomą poreikį, ir nepriklausomą poreikį. Pavyzdžiui, jei **·** *nustatyta tik pardavimo užsakymo parinktis Taip*, o visos prekės, į kurias atsižvelgiama prognozuojant poreikį, yra parduodamos prekės, sistema apskaičiuoja nepriklausomą poreikį. Tačiau į prekių paskirstymo raktus ir poreikio prognozes galima įtraukti kritinių subkomponentų. Šiuo atveju, jei gamybos eilutės **pasirinktis** nustatyta kaip *Taip*, apskaičiuojama priklausoma prognozė.

Galite nepaisyti vieno ar daugiau konkrečių prekių paskirstymo raktų operacijų tipų naudodami skirtuką **Prekių paskirstymo** raktai. Šis skirtukas pateikia panašius laukus.

#### <a name="choose-how-to-create-the-baseline-forecast"></a>Pasirinkite, kaip sukurti bazinę prognozę

Prognozės **generavimo** strategijos laukas leidžia pasirinkti metodą, kuris naudojamas bazinei prognozei sukurti. Galimi trys metodai:

- *Kopijuoti praeities poreikį* – kurti prognozes tik kopijuojant praeities duomenis.
- *"Azure" mašinos mokymosi paslauga* – naudokite prognozės modelį, kuriame naudojama "Azure" mašinos mokymosi paslauga. "Azure" mašinos mokymosi paslauga yra dabartinis mašinos mokymosi sprendimas "Azure". Todėl rekomenduojame jį naudoti, jei norite naudoti prognozės modelį.
- *"Azure" mašinos* mokymasis – naudokite prognozės modelį, kuris naudoja "Azure" mašinos mokymosi studiją (azure machine Learning Studio). "Azure Machine Learning Studio" ("azure") buvo pasenusi ir netrukus bus pašalinta iš "Azure". Todėl rekomenduojame pasirinkti " *Azure" mašinos mokymosi paslaugą*, jei pirmą kartą nustatote poreikio prognozę. Jei šiuo metu naudojate "Azure Machine Learning Studio" ("azure"), turite suplanuoti kaip galima greičiau pereiti prie "Azure" mašinos mokymosi paslaugos.

Naudodami skirtuką Prekių paskirstymo raktai galite nepaisyti vieno ar daugiau konkrečių prekių paskirstymo raktų prognozės **generavimo** metodo. Šis skirtukas pateikia panašius laukus.

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>Visuotinai nepaisyti numatytųjų prognozės algoritmo parametrų

Numatytieji prognozės algoritmo parametrai ir vertės priskirtos puslapyje Poreikio prognozės parametrai **(Bendrojo** planavimo nustatymas **\> Poreikio prognozės \> poreikio prognozės parametrai \>).** Tačiau galite jų nepaisyti visuotinai, naudodami prognozės **algoritmo parametrus** "FastTab **·** **", kuris yra poreikio prognozės parametrų puslapio skirtuke** Bendra. (Taip pat galite jų nepaisyti dėl konkrečių paskirstymo raktų naudodami **Skirtukas Prekių** paskirstymo raktai poreikio **prognozės parametrų** puslapyje.)

Naudokite įrankių **juostos mygtukus** **Pridėti** arba šalinti, norėdami nustatyti reikiamą parametrų nepaisymo rinkinį. Lauke Pavadinimas pasirinkite kiekvieno parametro **vertę**, tada vertės **lauke įveskite tinkamą** vertę. Visų parametrų, kurių nėra čia, vertės bus įtrauktos iš poreikio prognozės **parametrų puslapio parametrų**. Daugiau informacijos apie tai, kaip naudoti standartinį parametrų rinkinį ir pasirinkti jų vertes, [ieškokite skyriuje Numatytieji parametrai ir poreikio prognozės modelių](#model-parameters) vertės.

### <a name="set-forecast-dimensions"></a>Prognozės dimensijų nustatymas

Prognozės dimensija nurodo nustatytą prognozės išsamumo lygį. Įmonės, svetainės ir prekių paskirstymo raktas yra būtinos prognozės dimensijos. Taip pat galite generuoti prognozes sandėlio, atsargų būsenos, klientų grupės, kliento sąskaitos, šalies/regiono, apskrities ir (arba) prekės lygyje bei visuose prekės dimensijų lygiuose. Norėdami pasirinkti **prognozės** dimensijų **rinkinį,** naudojamą generuojant poreikio prognozę, naudokite skirtuką Prognozės dimensijos puslapyje Poreikio prognozės parametrai.

Prognozės dimensijas bet kuriuo metu galite įtraukti į dimensijų, kurios naudojamos poreikio prognozei, sąrašą. Taip pat galite prognozės dimensijas iš sąrašo pašalinti. Tačiau įtraukus arba pašalinus prognozės dimensiją, neautomatiniai koregavimai bus panaikinti.

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>Nustatyti konkrečių prekių paskirstymo raktų nepaisymus

Ne visos prekės veikia vienodai iš poreikio prognozės perspektyvos. Todėl galite nustatyti paskirstymo raktas – konkrečius daugumai parametrų, kurie apibrėžti skirtuke **Bendra, perrašymus** . Išimtis yra poreikio prognozės vienetas. Norėdami nustatyti konkretaus prekių paskirstymo rakto nepaisymus, atlikite šiuos veiksmus.

1. Puslapyje Poreikio **prognozės** **parametrai**, skirtuke Prekių paskirstymo raktai, naudokite įrankių juostos mygtukus, norėdami pridėti prekių paskirstymo raktus į tinklelį kairėje, arba pašalinkite juos, jei reikia. Tada pasirinkite paskirstymo raktą, kurio nepaisymus norite nustatyti.
1. Operacijų tipų **"** FastTab" įgalinkite operacijų tipus, kuriuos norite naudoti produktų, kurie priklauso pasirinktam paskirstymo raktui, statistinei bazinei prognozei generuoti. Parametrai veikia taip pat, kaip ir skirtuke **Bendra**, tačiau jie taikomi tik pasirinktam prekių paskirstymo raktui. Visi čia bendrieji parametrai *(ir Taip* vertės *, ir Ne* vertės) panaikina visus skirtuke **Bendra** pateikiamus operacijų **tipų** parametrus.
1. Prognozės algoritmo **parametrų** "FastTab" pasirinkite prognozės generavimo strategiją ir prognozės algoritmo parametrų nepaisymus produktams, kurie priklauso pasirinktam paskirstymo raktui. Šie parametrai veikia tik tada, kai veikia skirtuke **Bendra**, bet jie taikomi tik pasirinktam prekių paskirstymo raktui. Naudokite įrankių **juostos mygtukus** **Pridėti** arba Šalinti, norėdami nustatyti reikiamą parametrų nepaisymo rinkinį. Lauke Pavadinimas pasirinkite kiekvieno parametro **vertę**, tada vertės **lauke įveskite tinkamą** vertę. Daugiau informacijos apie tai, kaip naudoti standartinį parametrų rinkinį ir pasirinkti jų vertes, [ieškokite skyriuje Numatytieji parametrai ir poreikio prognozės modelių](#model-parameters) vertės.

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>Nustatyti ryšį su "Azure" mašinos mokymosi paslauga

Norėdami nustatyti **ryšį su "Azure" mašinos** mokymosi paslauga, naudokite skirtuką "Azure" mašinos mokymosi paslauga. Šis sprendimas yra viena iš pagrindinės prognozės kūrimo pasirinkčių. Šie parametrai šiame skirtuke veikia tik tada, kai prognozės **generavimo strategijos** laukas nustatytas į " *Azure" mašinos mokymosi tarnybą*.

Norėdami gauti daugiau informacijos apie tai, kaip nustatyti "Azure" mašinos mokymosi paslaugą ir tada naudoti čia nustatytus parametrus, kad prie jos prisijungtų, [žr. "Azure" mašinos mokymosi paslaugos skyriaus nustatymas](#setup-amls).

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>Nustatyti ryšį su "Azure Machine Learning Studio" (azure machine learning Studio)

> [!IMPORTANT]
> "Azure Machine Learning Studio" ("azure Machine Learning Studio") pasenusi. Todėl "Azure" nebegalite sukurti naujų darbo sričių. Ją pakeitė "Azure" mašinos mokymosi tarnyba, kuri suteikia panašias funkcijas ir daugiau. Jei dar nenaudojate "Azure" mašinos mokymosi, turėtumėte pradėti naudoti "Azure" mašinos mokymosi tarnybą. Jei jau turite darbo sritį, kuri sukurta "Azure Machine Learning Studio" ("azure"), galite ją naudoti toliau, kol funkcija bus visiškai pašalinta iš "Azure". Tačiau rekomenduojame "Azure" mašinos mokymosi paslaugą atnaujinti kaip galima greičiau. Nors programa ir toliau įspės jus, kad "Azure Machine Learning Studio" (azure Machine Learning Studio) buvo pasenusi, prognozės rezultatas nebus paveiktas. Daugiau informacijos apie naują "Azure" mašinos mokymosi paslaugą ir kaip ją nustatyti, [žr. skyriuje "Azure" mašinos mokymo paslaugos(-ų) nustatyme](#setup-amls).
>
> Galite laisvai perjungti iš naujo naudodami naujus ir senus mašinos mokymosi sprendimus su tiekimo grandinės valdymu, kol liks galima senoji "Azure Machine Learning Studio" (paleisties) darbo sritis.

Jei jau turite esamą "Azure Machine Learning Studio" ("azure") darbo sritį, galite naudoti ją prognozėms generuoti prijungdami ją prie tiekimo grandinės valdymo. Šį ryšį galite užmegzti naudodami skirtuką " **Azure" mašinos mokymosi** funkciją, kurį rasite poreikio **prognozės parametrų** puslapyje. (Nustatymai šiame skirtuke veikia tik tada, kai **Prognozės generavimo** strategijos laukas nustatytas kaip " *Azure" mašinos mokymasis*.) Įveskite toliau nurodytą informaciją apie "Azure Machine Learning Studio" (mazgą) darbo sritį:

- Žiniatinklio tarnybos taikomojo programavimo sąsajos (API) raktas
- Žiniatinklio tarnybos galinio punkto URL
- „Azure“ saugyklos abonemento pavadinimas
- „Azure“ saugyklos abonemento raktas

> [!NOTE]
> „Azure“ saugyklos abonemento pavadinimas ir raktas yra privalomi tik tada, jei naudojate pasirinktinį saugyklos abonementą. Jei diegiate vietinę versiją, "Azure" turite turėti pasirinktinį saugojimo abonementą, kad įrenginio mokymosi programa galėtų pasiekti retrospektyvius duomenis.

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a> Poreikio prognozės modelių numatytieji parametrai ir vertės

Kai naudojate mašinų mokymą prognozės planavimo modeliams generuoti, jūs kontroliuojate įrenginių mokymosi pasirinktis nustatydami prognozavimo *algoritmo parametrų vertes*. Šios vertės siunčiamos iš tiekimo grandinės valdymo į "Azure" mašinos mokymą. Naudokite prognozavimo **algoritmo parametrų** puslapį, kad kontroly kurie verčių tipai turėtų būti pateikiami ir kurios vertės turi turėti.

Norėdami nustatyti numatytuosius parametrus ir vertes, naudojamas poreikio prognozės modeliams, eikite į bendrojo **planavimo nustatymo \>\> poreikio prognozavimo prognozavimo \> algoritmo parametrus**. Pateikiamas standartinis parametrų rinkinys. Kiekvienas parametras turi šiuos laukus:

- **Pavadinimas** – parametro pavadinimas, kurį naudoja "Azure". Paprastai šio pavadinimo keisti nereikia, nebent "Azure" mašinos mokymosi metu pritaikėte jo pritaikymą.
- **Aprašas** – bendras parametro pavadinimas. Šis pavadinimas naudojamas norint identifikuoti parametrą kitose sistemos vietose (pvz., poreikio **prognozės parametrų** puslapyje).
- **Reikšmė** – numatytoji parametro vertė. Vertė, kurią turėtumėte įvesti, priklauso nuo redaguojamo parametro. 
- **Paaiškinimas** – trumpas parametro aprašymas ir kaip jį naudoti. Paprastai šiame aprašyme pateikiama patarimas apie tinkamas vertės **lauko** vertes.

Šie parametrai pateikiami pagal numatytuosius nustatymus. (Jei kada nors turite grįžti į šį standartinį sąrašą, pasirinkite **Atkurti** veiksmų sritį.)

- **Patikimumo lygis procentais** – Patikimumo intervalą sudaro reikšmės, kurios nurodo tinkamus poreikio prognozės įvertinimus. 95 procentų patikimumo lygio procentas nurodo 5 procentų tikimybę, kad ateities poreikis nepateks į patikimumo intervalo diapazoną.
- **Force seasonality** – nurodo, ar priversti modelį naudoti tam tikrą sezoniškumo tipą. Šis parametras taikomas tik ARIMA ir ETS. Pasirinktys: *AUTOMATINIS (numatytasis),*, *NĖRA*, *PRIEDAS*, *DAUGKARTINIS*.
- **Prognozavimo modelis** – nurodo, kurį prognozės modelį naudoti. Pasirinktys: *ARIMA*, *ETS*, *STL*, *ETS+ARIMA*, *ETS+STL*, *VISI*. Norėdami pasirinkti modelį, tinkantį geriausiai, naudokite *VISUS*.
- **Didžiausia prognozuota vertė** – Nurodo didžiausią vertę, kurią reikia naudoti prognozėje. Formatas: +1E[n] arba skaitinė konstanta.
- **Mažiausia prognozuota vertė** – Nurodo mažiausią vertę, kurią reikia naudoti prognozėje. Formatas: ‑1E[n] arba skaitinė konstanta.
- **Trūkstamos vertės pakaitalai** – Nurodo, kaip užpildomos praeities duomenų spragos. Pasirinktys: *(skaitinė vertė)*, VIDUTINIS *·*, ANKSTESNIS *·*, *INTERALALIZINIS*, *INTERBANKINĖ POLINOMIJA*.
- **Trūkstamos vertės pakaitalų apimtis** – Nurodo, ar vertės keitimas taikomas tik kiekvienam atskiram duomenų diapazono detalumo atributui ar visam duomenų rinkiniui. Galimos šios datos intervalo, kurį sistema naudoja užpildydama praeities duomenų spragas, nustatymo pasirinktys:

    - *VISUOTINIS* – sistema naudoja visą visų detalumo atributų datų diapazoną.
    - *HISTORY_DATE_RANGE – sistema naudoja tam tikrą datų diapazoną, kuris apibrėžtas laukuose Nuo* **·** **·** **datos** ir Iki datos, esančiuose skyriuje Praeities laikotarpis, dialogo lange Generuoti bazinę statistinę prognozę.**·**
    - *GRANULARITY_ATTRIBUTE* – sistema naudoja šiuo metu apdoroto detalumo atributo datų diapazoną.

    > [!NOTE]
    > Detalumo atributas yra prognozės dimensijų, pagal kurias kuriama prognozė, derinys. Galite nustatyti prognozės dimensijas puslapyje **Poreikio prognozės parametrai**.

- **Užuomina apie sezoniškumą** – Jei naudojate sezoninius duomenis, pateikite prognozės modeliui užuominą, kad pagerintumėte prognozės tikslumą. Formatas – tai skaičius, nurodantis numerių rinkinius, kurių poreikio šablonas pasikartoja pats. Pavyzdžiui, įveskite *6 duomenims*, kurie pasikartoja kas šešis mėnesius.
- **Rinkinio dydžio procento tikrinimas** – Praeities duomenų procentas, kurį reikia naudoti kaip bandomąjį rinkinį skaičiuojant prognozės tikslumą.

Galite nepaisyti šių parametrų verčių nueidami prie bendrojo **planavimo nustatymo \> poreikio \> prognozės poreikio \> prognozavimo parametrų**. Poreikio **prognozės parametrų** puslapyje parametrų galite nepaisyti šiais būdais:

- Norėdami nepaisyti **parametrų** visuotinai, naudokite skirtuką Bendra.
- Naudokite skirtuką **Prekių paskirstymo raktai**, norėdami nepaisyti konkrečių prekių paskirstymo raktų parametrų. Konkretaus prekių paskirstymo rakto parametrai, kurių nepaisoma, veikia tik prekių, susijusių su tuo prekių paskirstymo raktu, prognozę.

> [!NOTE]
> Prognozavimo **algoritmo parametrų** puslapyje galite naudoti veiksmų srities mygtukus, pridėti parametrus į sąrašą arba pašalinti parametrus iš sąrašo. Tačiau dažniausiai turėtumėte nenaudoti šio požiūrio, nebent "Azure" mašinos mokymosi metu pritaikyto pritaikymo.

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a> Nustatyti "Azure" įrenginio mokymosi paslaugą

Tiekimo grandinės valdymas apskaičiuoja poreikio prognozes naudodamas "Azure" mašinos mokymosi paslaugą, kurią turite nustatyti ir paleisti savo "Azure" abonemente. Šiame skyriuje aprašoma, kaip nustatyti "Azure" mašinos mokymosi paslaugą "Azure" ir prijungti ją prie tiekimo grandinės valdymo aplinkos.

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>Funkcijų valdymo įjungti "Azure" įrenginio mokymosi paslaugą

Norėdami įjungti integravimą, prieš naudodami "Azure" mašinos mokymosi tarnybą poreikio prognozei atlikti turite įjungti tiekimo grandinės valdymo funkciją. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Bendrasis planavimas*
- **Funkcijos pavadinimas: "** *Azure" įrenginio mokymosi paslauga poreikio prognozei*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a> Nustatyti mašinos mokymą "Azure"

Norėdami įgalinti "Azure" naudoti įrenginio mokymą prognozėms apdoroti, šiuo tikslu turite nustatyti "Azure" mašinos mokymosi darbo sritį. Galite pasirinkti dvi pasirinktis:

- Norėdami nustatyti darbo sritį paleisdami "Microsoft" pateikiamą scenarijų, [vadovaukitės 1 parinkties instrukcijomis:](#ml-workspace-script) paleiskite scenarijų, kad būtų automatiškai nustatyta jūsų mašinos mokymosi darbo srities dalis, [tada pereikite prie "Azure"](#demand-forecast-parameters) mašinos mokymosi tarnybos ryšio parametrų nustatymo tiekimo grandinės valdymo skyriuje.
- Norėdami rankiniu būdu nustatyti savo darbo sritį, [vadovaukitės 2 parinkties instrukcijomis:](#ml-workspace-manual) rankiniu būdu nustatykite įrenginio mokymosi darbo srities skyrių ir [pereikite prie "Azure"](#demand-forecast-parameters) mašinos mokymosi tarnybos ryšio parametrų nustatymo tiekimo grandinės valdymo skyriuje. Ši pasirinktis užtrunka daugiau laiko, bet ji jums suteikia daugiau kontrolės.

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a> 1 parinktis: vykdyti scenarijų, kad būtų automatiškai nustatyta jūsų mašinos mokymosi darbo sritis

Šiame skyriuje aprašoma, kaip nustatyti jūsų mašinų mokymosi darbo sritį naudojant "Microsoft" pateiktą automatinį scenarijų. Jei norite, visus išteklius galite [nustatyti rankiniu būdu, vadovaukitės 2 pasirinkties instrukcijomis: rankiniu būdu nustatykite savo mašinų mokymo darbo srities](#ml-workspace-manual) skyrių. Jums nereikia atlikti abiejų pasirinkčių.

1. GitHub, atidarykite [Dynamics 365 Supply Chain Management poreikio prognozės naudojant "Azure"](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) mašinos mokymosi saugyklą (repo) šablonus ir atsisiųskite šiuos failus:

    - quick_setup.ps1
    - sampleInput.csv pavyzdys
    - SRC / parameters.py
    - src/api_trigger.s
    - SRC / run.py
    - src/REntryScript/forecast.r

1. Atidarykite "PowerShell" langą ir paleiskite **scenarijų quick_setup.ps1**, kurį atsisiuntėte atlikdami ankstesnį veiksmą. Vadovaukitės ekrane pateikiamais nurodymais. Scenarijus nustato reikiamą darbo sritį, saugyklą, numatytąją duomenų saugyklą ir apskaičiuoti išteklius. Tačiau jūs vis tiek turite sukurti reikalingas pardavimo galimybes, atlikdami likusius šios procedūros veiksmus. (Pardavimo galimybės suteikia būdą pradėti prognozavimo scenarijus nuo tiekimo grandinės valdymo.)
1. Į "Azure Machine Learning Studio" įkelkite 1 žingsniu atsisiųstą pavyzdžioInput.csv **failą** į konteinerį, *pavadintą demplan-azureml*. (quick_setup.ps1 scenarijus sukūrė šį konteinerį.) Šis failas yra būtinas norint paskelbti pardavimo galimybes ir sugeneruoti tikrinimo prognozę. Instrukcijų ieškokite nusiuntimo [bloko BLOB.](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob)
1. "Azure Machine Learning Studio" pasirinkite **Meniu**.
1. Failų struktūroje raskite **šią** vietą: vartotojai **/\[ dabartinis vartotojas\] / src**.
1. Įkelkite likusius keturis failus, kuriuos atsisiuntėte 1 žingsniu, į vietą, kurią rasite ankstesniame veiksme.
1. Pasirinkite ką **tik api_trigger.failą** ir paleiskite jį. Bus sukurta pardavimo galimybės, kurias galima įjungti naudojant API.
1. Jūsų darbo sritis dabar nustatyta. Praleisti į priekį iki ["Azure" mašinos mokymosi tarnybos ryšio parametrų nustatymo tiekimo grandinės valdymo](#demand-forecast-parameters) skyriuje.

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a> 2 parinktis: rankiniu būdu nustatykite savo įrenginio mokymosi darbo sritį

Šiame skyriuje aprašoma, kaip rankiniu būdu nustatyti savo įrenginio mokymosi darbo sritį. Turite atlikti šiame skyriuje aprašytas procedūras tik tada, jei nusprendėte ne vykdyti automatizuoto nustatymo scenarijaus, [kaip aprašyta 1 pasirinktyje: vykdykite scenarijų, norėdami nustatyti įrenginių mokymosi darbo srities](#ml-workspace-script) skyrių.

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a> 1 veiksmas: naujos darbo srities kūrimas

Norėdami sukurti naują mašinų mokymosi darbo sritį, naudokite nurodytą procedūrą.

1. Prisiregistruokite prie "Azure" portalo.
1. Atidarykite įrenginio **mokymosi tarnybą**.
1. Norėdami **atidaryti** vedlį Kurti, įrankių juostoje pasirinkite **Kurti**.
1. Baikite vedlio veiksmus, naudodami ekrane pateiktas instrukcijas. Dirbę atmeskite šiuos taškus:

    - Naudoti numatytuosius parametrus, nebent kiti šio sąrašo taškai rekomenduoja skirtingus parametrus.
    - Būtinai pasirinkite geografinį regioną, kuris atitinka regioną, kuriame įdiegtas tiekimo grandinės valdymo egzempliorius. Kitu atveju kai kurie jūsų duomenys gali peržengia regiono ribas. Norėdami gauti daugiau informacijos, toliau [šiame straipsnyje](#privacy) žr. privatumo pranešimą.
    - Naudokite paskirtus išteklius, pavyzdžiui, išteklių grupes, saugojimo sąskaitas, konteinerių registrus, "Azure" raktų saugyklą ir išteklius.
    - Vedlio **puslapyje Nustatyti "Azure" mašinos mokymosi** tarnybos ryšio parametrus turite nurodyti saugyklos sąskaitos pavadinimą. Naudokite sąskaitą, skirtą poreikio prognozei. Poreikio prognozės įvesties ir išeigos duomenys bus saugomi šioje saugojimo sąskaitoje.

Daugiau informacijos ieškokite Darbo [srities kūrimas](/azure/machine-learning/quickstart-create-resources#create-the-workspace).

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a> 2 žingsnis: saugojimo konfigūravimas

Norėdami nustatyti saugyklą, naudokite nurodytą procedūrą.

1. GitHub, atidarykite [Dynamics 365 Supply Chain Management poreikio prognozės naudojant "Azure"](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) mašinos mokymosi repo šablonus ir **atsisiųskite sampleInput.csv** failą.
1. Atidarykite saugojimo abonementą, kurį sukūrėte [1 žingsnyje: sukurkite naują darbo sritį](#create-workspace).
1. Norėdami sukurti konteinerį [, pavadintą](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) " *demplan-azureml", vadovaukitės instrukcijomis, pateiktomis kuriant konteinerį*.
1. Įkelkite **1 žingsniu atsisiųstą pavyzdžioInput.csv** failą į ką tik sukurtą konteinerį. Šis failas yra būtinas norint paskelbti pardavimo galimybes ir sugeneruoti tikrinimo prognozę. Instrukcijų ieškokite nusiuntimo [bloko BLOB.](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob)

##### <a name="step-3-configure-a-default-datastore"></a>3 žingsnis: numatytųjų duomenų saugyklos konfigūravimas

Norėdami nustatyti savo numatytuosius duomenų saugyklas, naudokite nurodytą procedūrą.

1. Programos "Azure Machine Learning Studio **" kompiuteryje pasirinkite Duomenų saugyklas**.
1. Sukurkite *naują "Azure BLOB* *" saugyklos tipo, kuris nurododemoplaną "azureml*" BLOB [saugyklos konteinerį, kurį sukūrėte 2 žingsnyje, duomenų saugyklą: konfigūruokite saugyklos](#config-storage) skyrių. (Jei naujos duomenų saugyklos autentifikavimo tipas yra *Sąskaitos raktas*, pateikite sukurtos saugojimo sąskaitos raktą. Instrukcijų ieškokite Valdyti saugojimo [sąskaitos prieigos raktus](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal).)
1. Padarykite naują duomenų parduotuvę numatytąja duomenų saugykla, atidarydami jos informaciją ir pasirinkdami **Nustatyti kaip numatytąją duomenų parduotuvę**.

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a> 4 žingsnis: išteklių konfigūravimas

Norėdami nustatyti skaičiuoti išteklius "Azure Machine Learning Studio", norėdami vykdyti prognozių generavimo scenarijus, naudokite nurodytą procedūrą.

1. Atidarykite įrenginių mokymosi darbo srities, kurią sukūrėte 1 veiksme [, informacijos puslapį: sukurkite naują darbo srities](#create-workspace) skyrių. Raskite **Studio žiniatinklio URL** reikšmę ir pasirinkite saitą, kad jį atidarytumėte.
1. Naršymo **srityje** pasirinkite Komponuoti.
1. Skirtuke **Apskaičiuoti egzempliorius pasirinkite** Naujas, kad **atidarytumėte** vedlį, kuris padės jums sukurti naują komponavimo egzempliorių. Vadovaukitės ekrane pateikiamais nurodymais. Komponavimo egzempliorius bus naudojamas kuriant poreikio prognozės pardavimo galimybes (jį galima panaikinti skelbiant pardavimo galimybes). Naudoti numatytuosius parametrus.
1. Skirtuke **Komponuoti klasterius** pasirinkite Naujas, **kad** atidarytumėte vedlį, kuris padės jums sukurti naują komponavimo klasterį. Vadovaukitės ekrane pateikiamais nurodymais. Šis klasteris bus naudojamas poreikio prognozėms generuoti. Jo parametrai daro įtaką našumui ir maksimaliam vykdymo lygiagretinimo lygiui. Nustatykite šiuos laukus, tačiau visiems kitiems laukams naudokite numatytuosius parametrus:

    - **Pavadinimas** – įveskite *e2ecpucluster*.
    - **Virtualiosios mašinos dydis** – koreguokite šį parametrą pagal duomenų, kuriuos tikitės naudoti kaip įvestį poreikio prognozei atlikti, kiekį. Mazgų skaičius neturi viršyti 11, nes vienas mazgas reikalingas poreikio prognozės generavimui paleisti ir didžiausias mazgų, kurie tada bus naudojami prognozei generuoti, skaičius yra 10. (Jūs taip pat nustatote mazgų skaičių parameters.py failo [5 žingsnis: sukurti pardavimo galimybių](#create-pipelines) skyrių.) Kiekviename mazge bus keletas darbuotojų procesų, kurie lygiagrečiai paleis prognozavimo scenarijus. Bendras jūsų užduoties darbuotojų procesų skaičius bus *branduolių, kuriuos mazgas turi* × skaičius *, skaičius*. Pavyzdžiui, *\_ jei jūsų komponuojamo klasterio tipas yra Standartinis D4* (aštuoni branduoliai) ir daugiausia 11 mazgų, `nodes_count`*o jei nustatyta vertė 10* parameters.py faile, veiksmingas lygiagretumo lygis yra 80.

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a> 5 žingsnis: pardavimo galimybių kūrimas

Pardavimo galimybės suteikia būdą pradėti prognozavimo scenarijus iš tiekimo grandinės valdymo. Norėdami sukurti reikalingas pardavimo galimybes, naudokite nurodytą procedūrą.

1. GitHub, atidarykite poreikio [prognozės Dynamics 365 Supply Chain Management naudojant "Azure"](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service) įrenginio mokymosi repo šablonus ir atsisiųskite šiuos failus:

    - SRC / parameters.py
    - src/api_trigger.s
    - SRC / run.py
    - src/REntryScript/forecast.r

1. "Azure Machine Learning Studio" pasirinkite **Meniu**.
1. Failų struktūroje raskite **šią** vietą: vartotojai **/\[ dabartinis vartotojas\] / src**.
1. Įkelkite keturis failus, kuriuos atsisiuntėte 1 žingsniu, į vietą, kurią rasite ankstesniame veiksme.
1. Atidarykite ir peržiūrėkite ką **tik parameters.py** įkeltą "Azure" failą. Įsitikinkite, kad `nodes_count` vertė [yra mažesnė nei vertė, kurią sukonfigūravote 4 žingsnyje nurodytai komponuoti klasteriui: dalyje Konfigūruoti išteklių naudojimą](#config-compute-resources). Jei vertė `nodes_count` didesnė nei komponuojame klasteryje esantis mazgų skaičius arba jis lygus, gali būti galima pradėti pardavimo galimybių paleidimą. Tačiau kol jis laukia reikalingų išteklių, jis nustos reaguoti. Daugiau informacijos apie mazgų skaičių ieškokite [4 žingsnyje: išteklių skaičiavimo konfigūravimas](#config-compute-resources).
1. Pasirinkite ką **tik api_trigger.failą** ir paleiskite jį. Bus sukurta pardavimo galimybės, kurias galima įjungti naudojant API.

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a> Nustatyti naują Active Directory programą

Norint autentifikuoti išteklius, skirtus poreikio prognozei naudojant tarnybos pagrindinius duomenis, reikalinga Active Directory programa. Todėl programa turi turėti žemiausią teisių lygį, kurio reikia prognozei generuoti.

1. Prisiregistruokite prie "Azure" portalo.
1. Registrkite naują prašymą nuomininkui Azure Active Directory (Azure AD). Norėdami gauti daugiau instrukcijų [, žr. portalą, kad sukurtumėte programą Azure AD ir aptarnavimo pagrindinį puslapį, galiį pasiekti išteklius](/azure/active-directory/develop/howto-create-service-principal-portal).
1. Pabaigę vedlį vadovaukitės ekrane pateikiamomis instrukcijomis. Naudoti numatytuosius parametrus.
1. Suteikite savo naujai Active Directory programai prieigą prie toliau nurodytų išteklių, kuriuos sukūrėte ["Azure](#ml-workspace) " skyriuje nustatyti mašinų mokymą. Norėdami gauti instrukcijų, žr. " [Azure" vaidmenų priskyrimą naudojant "Azure" portalą](/azure/role-based-access-control/role-assignments-portal?tabs=current). Šis veiksmas įgalins sistemą importuoti ir eksportuoti prognozavimo duomenis ir aktyvinti pardavimo galimybių paleidimą iš tiekimo grandinės valdymo.

    - Vaidmens vaidmuo įrenginio mokymosi darbo srityje
    - Paskirtos saugojimo sąskaitos vaidmens vaidmuo
    - Saugojimo BLOB duomenų vaidmens priskyrimo saugojimo sąskaitai

1. Sertifikatuose **> pasamdysite** sukurtos programos skyrių, sukurkite programos slapyme. Instrukcijų ieškokite Kliento [slapto failo pridėjimas](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret).
1. Pasižymėkite programos ID ir jo slaptą pastabą. Vėliau turėsite gauti išsamios šios programos informacijos, kai tiekimo grandinės valdymo **dalyje nustatysite** poreikio prognozės parametrų puslapį.

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a> Tiekimo grandinės valdymo dalyje nustatyti "Azure" įrenginio mokymosi tarnybos ryšio parametrus

Norėdami prijungti savo tiekimo grandinės valdymo aplinką prie įrenginio mokymosi paslaugos, kurią ką tik nustatėte "Azure", naudokite nurodytą procedūrą.

1. Prisijunkite prie „Supply Chain Management“.
1. Eikite į **bendrojo planavimo nustatymą \> Poreikio \> prognozės \> poreikio prognozės parametrai**.
1. Skirtuke **Bendra** įsitikinkite, kad prognozės generavimo **strategijos** laukas nustatytas į " *Azure" mašinos mokymosi tarnybą*.
1. Prekių paskirstymo **raktų** skirtuke įsitikinkite, kad prognozės generavimo strategijos laukas nustatytas į "Azure **" mašinos mokymosi paslaugą kiekvienam paskirstymo raktui,** *kuris* turi naudoti "Azure" mašinos mokymosi tarnybą poreikio prognozei.
1. Skirtuke **"Azure Machine Learning Service** " nustatykite šiuos laukus:

    - **Nuomininko ID – įveskite savo "Azure" nuomininko ID**. Tiekimo grandinės valdymas šį ID naudos autentifikuoti "Azure" mašinos mokymosi paslaugoje. Savo nuomininkų ID galite rasti " **Azure"** portalo Azure AD apžvalgos puslapyje.
    - **Tarnybos pagrindinis programos ID – įveskite programos, kurią sukūrėte** Active Directory programos skyriuje, [ID](#aad-app). Ši vertė naudojama norint įgalioti API užklausas "Azure" mašinos mokymosi tarnybai.
    - **Aptarnavimo sąrašas** – įveskite pagrindinį tarnybos programos slaptažodį programai, kurią sukūrėte [Active Directory programos skyriuje](#aad-app). Ši vertė naudojama siekiant gauti saugos rakto, kurį sukūrėte autorizuoti operacijoms pagal "Azure" saugyklą ir "Azure" mašinos kalbos darbo sritį, atpažinimo ženklą.
    - **Saugyklos sąskaitos pavadinimas** – įveskite "Azure" saugyklos sąskaitos pavadinimą, kurį nurodėte, kai "Azure" darbo srityje nurodėte sąrankos vedlį. (Daugiau informacijos ieškokite [Nustatykite mašinų mokymą "Azure"](#ml-workspace) skyriuje.)
    - **Pardavimo galimybių galinio punkto** adresas – įveskite "Azure" mašinos mokymosi tarnybos pardavimo galimybių REST galinio punkto URL. Pardavimo galimybes sukūrėte kaip paskutinį veiksmą, kai nustatote [mašinų mokymą "Azure"](#ml-workspace). Norėdami gauti pardavimo galimybių URL, prisijunkite prie "Azure" portalo, naršymo **metu pasirinkite** pardavimo galimybes. Skirtuke **Pardavimo galimybės** pasirinkite pardavimo galimybių galinį punktą, pavadintą **TriggerDemandForecastGeneration**. Tada nukopijuokite rodomą REST galinį punktą.

    ![Parametrai poreikio prognozės parametrų puslapio skirtuke "Azure" mašinos mokymosi tarnyba.](media/azure-ml-service-parameters.png "Poreikio prognozės parametrų puslapio skirtuko &quot;Azure&quot; mašinos mokymosi tarnyba parametrai")

## <a name="privacy-notice"></a><a name="privacy"></a>Privatumo pranešimas

*Kai pasirenkate "Azure*" mašinos mokymosi tarnybą kaip prognozės generavimo strategiją, tiekimo grandinės valdymas automatiškai siunčia savo kliento duomenis praeities poreikiui, pvz., sujungti kiekiai, produktų pavadinimai ir jų produktų dimensijos, siuntimo ir gavimo vietos, kliento identifikatoriai ir prognozės parametrai, į geografinį regioną, kuriame yra jūsų mašinos mokymosi darbo sritis ir yra susieta saugojimo sąskaita, ateities poreikio prognozavimo tikslu. "Azure" įrenginio mokymosi paslauga gali būti kitoje geografinėje regione nei geografinėje srityje, kurioje įdiegtas tiekimo grandinės valdymas. Kai kurie vartotojai gali kontroliuoti, ar ši funkcija įgalinta, pasirinkdami prognozės generavimo strategiją poreikio **prognozės parametrų** puslapyje.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Poreikio prognozavimo apžvalga](introduction-demand-forecasting.md)
- [Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)
- [Neautomatiniai pagrindinės prognozės koregavimai](manual-adjustments-baseline-forecast.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
