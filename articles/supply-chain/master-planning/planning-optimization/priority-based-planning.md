---
title: Prioritetu grindžiamas planavimas
description: Šiame straipsnyje aprašoma "Microsoft" prioritetu pagrįsta planavimo priemonė Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 1a952fe5734f01325842a8a130b9322eadc67951
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740598"
---
# <a name="priority-based-planning"></a>Prioritetu grindžiamas planavimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma "Microsoft" prioritetu pagrįsta planavimo priemonė Dynamics 365 Supply Chain Management. Ši funkcija įtraukia poreikio planavimo, kuris yra vienas [iš poreikio poreikių planavimo (DDMRP) žingsnio, palaikymą](ddmrp-overview.md). Prioritetinis planavimas įgalina sistemą generuoti suplanuotus užsakymus, paremtus planavimo prioritetais, o ne poreikio datomis.

Prioritetinis planavimas leidžia jums nustatyti papildymo užsakymų prioritetą siekiant užtikrinti, kad skubaus poreikio prioritetas būtų skubus, o ne toks svarbus poreikis. Pavyzdžiui, atsargų papildymo užsakymas bus laikomas prioritetu virš standartinio papildymo papildymo užsakymo. Sistema gali automatiškai išskaidyti didesnius užsakymus į atskirus mažesnius užsakymus, kai užsakymo eilutės grupuojami pagal prioritetą. Tada pirmiausia bus galima apdoroti visus didelio prioriteto užsakymus.

Norėdami greitai peržiūrėti šią funkciją, žr. toliau nurodytą vaizdo įrašą: planavimo [optimizavimo palaikymas, skirtas prioritetui pagrįstam planavimui Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Įjungti prioritetinį planavimą savo sistemoje

Šią funkciją galėsite naudoti tik tada, kai ją įjungsite savo sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Bendrasis planavimas*
- **Funkcijos pavadinimas: prioritetinis** *MRP palaikymas, skirtas planavimo optimizavimui*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Kur ir kaip priskiriami planavimo prioritetai

*Planavimo prioriteto* informacija apie tiekimą ir poreikį yra prioriteto planavimo pagrindas. Planavimo prioritetas apibrėžia poreikio ar tiekimo eilutės svarbą. Bendrasis planavimas jį naudoja, kai **padengimo kodo** laukas nustatytas kaip *Prioritetas*.

Planavimo prioritetas paprastai yra skaičius nuo 0 (nulio) iki 100, o 0 reiškia aukščiausią svarbą. Jis rodomas ir nustatomas lauke **Planavimo prioritetas**. Šį lauką galite rasti šiuose puslapiuose: poreikio **prognozės** eilutės, **pardavimo** užsakymo informacija, **pirkimo** užsakymo informacija, **perkėlimo užsakymo** informacija ir suplanuoto **užsakymo informacija**.

Kai atitinkamos prekės arba padengimo grupės padengimo kodo laukas nustatytas kaip Prioritetas, bendrojo planavimo metu balansai su poreikiu apskaičiuojami naudojant poreikiu pagrįstą būdą, **o** kiekvieno išleisto produkto planavimo prioritetą jis apima vertes, kurios yra nustatytos laukams Minimalus, *·* **·** **Persamdyti** tašką ir Maksimalus prekių padengimo puslapyje.**·** **·**

> [!NOTE]
> Prioriteto *vertė* galima padengimo kodo **lauke tik** tada, kai įgalintas planavimo optimizavimas.

Susiję planavimo prioritetų *modeliai valdo planavimo* prioritetą ir padalina suplanuotus užsakymus pagal prioritetų diapazoną. Taip pat jos leidžia nustatyti numatytąsias planavimo prioriteto vertes kiekvienam tiekimo ar poreikio tipui ir apibrėžti prioriteto skaičiavimo metodą.

## <a name="types-of-priority-calculation-methods"></a>Prioriteto skaičiavimo metodų tipai

Kiekviename planavimo prioriteto modelyje yra **prioriteto skaičiavimo metodo parametras**, kuris valdo, kaip bendrasis planavimas prioritetas taikomas suplanuotams užsakymams. Galimos vertės yra didžiausio *atsargų kiekio procentas ir* Prioritetų *diapazonai*. *Prioritetų diapazonai* rodo išplėstinę didžiausio atsargų *kiekio procento metodo* versiją.

### <a name="percent-of-maximum-inventory-quantity"></a>Didžiausio atsargų kiekio procentas

Didžiausio atsargų *kiekio skaičiavimo metodo procente tiekimo prioritetų skaičiavimas suranda dabartines bendras turimas* *atsargas (grynasis srautas)* **kaip prekei nustatytos maksimalios atsargų kiekio vertės procentinę dalį.** Tada sukuriamas vienas kiekvienos prekės ir tiekėjo suplanuotas užsakymas (nebent skaidymo metu naudojamas maksimalus užsakymo kiekis). Užsakymo planavimo prioritetas skaičiuojamas kaip maksimalios procentinė dalis.

Naudojama ši formulė:

*Maksimali procentinė dalis* = (grynoji *srauto* padėtis × 100) ÷ *maksimalus atsargų kiekio vertė iš prekės padengimo*

Šioje formulėje *grynasis srautas* apskaičiuojamas taip:

*Grynojo srauto* = *padėtis –* + *turimos atsargų užsakymas* – *reikalavimus atitinkantis poreikis*

- *Užsakytas tiekimas* yra numatomas.
- *Reikalavimus atitinkantis* poreikis nurodo grynuosius poreikius, kurių poreikio data yra planavimo laiko ribose.

Vykdant bendrąjį planavimą, nauji suplanuoti užsakymai sukuriami, kai grynojo srauto padėtis yra mažesnė nei prekės užsakymo taškų kiekis. Suplanuoto užsakymo kiekis yra skirtumas tarp maksimalios **atsargų** kiekio vertės, nustatytos prekės lygyje, ir grynojo srauto pozicijos. Suplanuoto užsakymo prioritetas skaičiuojamas kaip didžiausio *atsargų kiekio vertės* grynojo **srauto pozicijos procentas**.

> [!NOTE]
> Apskaičiuotas prioritetas negali būti neigiamas, net jei poreikis viršija bendrą tiekimą. Jei poreikis viršija bendrą tiekimą, apskaičiuotas prioritetas nustatomas kaip 0 (nulis).

### <a name="priority-ranges"></a>Prioriteto diapazonai

Prioritetų *diapazonų* skaičiavimo metodas yra daugiau *išplėstas* nei didžiausio atsargų kiekio procento metodas ir yra sukonfigūruotas planavimo prioriteto modelio lygyje. Norint patenkinti prekės poreikį, gali būti sukurti keli nauji suplanuoti tiekimo užsakymai. Suplanuoto tiekimo prioritetai priklauso nuo verčių, kurios apibrėžtos puslapio **Planavimo prioriteto** **modeliai lauke Planavimo prioritetų diapazonų tinklelis**.

Šios papildomos taisyklės įsigalioja, kai Nustatytas **prioriteto skaičiavimo** metodo laukas Kaip *Prioriteto diapazonai*:

- Jei parinktis **Atsižvelgti į poreikio** prioritetą suplanuotam *prioriteto modeliui nustatyta kaip Taip*, prioritetas, nustatytas kiekvienoje poreikio eilutėje, apribos prioriteto diapazono rinkinį. Bet kurio naujo suplanuoto tiekimo užsakymo prioritetas nebus mažesnis nei poreikio prioritetas. Diapazono viršutinė vertė laikoma ribine verte, pagal kurią poreikio prioriteto vertė lyginama su. Jei poreikio prioritetas tiksliai yra viduryje tarp dviejų diapazonų viršutinių ribinių verčių, bus pasirinktas diapazonas, kuriame yra aukščiausias prioritetas (t. y. mažiausia prioriteto vertė).
- Jei **suplanuoto** *prioriteto* modelio laukas Suplanuoto užsakymo kūrimas nustatytas kaip Vienas tiekimas, kuriam taikomas aukščiausias prioritetas, bus sukurtas tik vienas tiekimas, kad būtų įvykdomas visas būdas iki didžiausio. Prioritetas bus nustatytas kaip pirmojo diapazono, kuris suaktyvins tiekimą, prioritetas.
- Jei nėra turimų atsargų, nėra tiekimo ir poreikio, bus naudojama planavimo prioriteto diapazonų tinklelio eilutė, **·** **·** *kurioje* lauko Nuo kiekio reikšmė yra Nulis.
- Jei yra poreikis, bet nėra turimų atsargų ar tikėtino tiekimo, bus naudojama planavimo prioritetų diapazonų tinklelio eilutė, **·** **·** *kurioje* lauko Nuo kiekio reikšmė nustatyta kaip Nulis arba Mažesnis.
- Kai diapazonas, į kurį vertinamas poreikis, poreikio prioriteto parinkties **Apsvarstyti poreikį parametras** vis tiek turės įtakos.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Skirtumai tarp tradicinio laiko juostos skaičiavimų ir prioritetu pagrįsto planavimo

Prioritetinis planavimas skiriasi nuo tradicinio laiko eilutės skaičiavimo šiais būdais:

- Visi reguliarūs išankstinio planavimo procesoriai vis dar veikia. Šie išankstiniai procesoriai apima patvirtintų suplanuotų užsakymų iškvietimą pagal pardavimo poreikį, pirkimo paraiškos konvertavimą ir rezervavimo logiką. Apdorojamas tik poreikis, kurių įvykdo šie išankstiniai procesoriai.
- Iškvietimo metu atsižvelgiama į visą tiekimą, nepaisant jo prioriteto. Šis tiekimas apima turimų atsargų, pateikto tiekimo ir neiškviestą patvirtintų suplanuotų užsakymų dalį.
- "Neigiamų dienų" poreikio negalima iškviesti prieš tiekimą per visą padengimo laiką.
- Kai tiekimas susietas su poreikiu, pirmiausia naudojamas tas tiekimas, kuris turi aukščiausią prioritetą (t. y. mažiausia prioriteto vertė). Laikoma, kad turimo atsargų tiekimo prioritetas lygus 0 (nuliui). Todėl jis bus suvartotas kaip pirmasis šaltinis.
- Naujos suplanuotos tiekimo eilutės bus sukurtos pagal įprastas minimalaus užsakymo dydžio, maksimalaus užsakymo dydžio, sudėtiaus kiekio ir t. t. taisykles.

## <a name="planning-priority-models"></a>Planavimo prioriteto modeliai

*Planavimo prioritetų modeliai* priskiriami padengimo grupėms ir valdo suplanuotų užsakymų planavimo prioritetą. Jie apibrėžia logiką, kuri nustato, kaip apskaičiuojama kiekvieno suplanuoto užsakymo planavimo prioriteto vertė ir kaip prioritetas priskiriamas suplanuotams užsakymams, tiekimo eilutėms ir poreikio eilutėms.

Norėdami dirbti su planavimo prioriteto modeliais, eikite į bendrojo **planavimo nustatymo \>\> planavimo prioritetų modelius**. Kaip anksčiau aptarta, vienas iš svarbiausių modelio parametrų yra Prioriteto **skaičiavimo metodo** vertė. Šis parametras valdo skaičiavimo metodą, kuris naudojamas, kai bendrasis planavimas priskiria prioriteto vertę suplanuotams užsakymams.

> [!NOTE]
> Planavimo prioritetų modeliai taikomi organizacijos mastu visiems juridiniams subjektams.

### <a name="coverage-group"></a>Padeng. grupė

Nustatykite naują padengimo grupę, kurią planuojate naudoti planuodami prioritetą, kaip aprašyta prekių [padengimo taisyklėse](../tasks/define-coverage-rules-items.md). Sukūrę padengimo grupę, nustatykite šiuos papildomus laukus:

- **Padengimo kodas** – pasirinkti *Prioritetą*, jei padengimo grupė naudos prioritetu pagrįstą planavimą.
- **Planavimo prioriteto** modelis – pasirinkite bet kurį visos organizacijos planavimo prioriteto modelį.

### <a name="item-coverage"></a>Prekės padengimas

Prekių padengimo parametrus nustatykite taip, kaip aprašyta padengimo [parametruose](../coverage-settings.md). Pagal numatytuosius nustatymus **, padengimo** kodo vertė, pasirinkta padengimo grupei, yra kopijuojama į prekės padengimo parametrus. Tačiau jei reikia, galite nepaisyti numatytosios vertės. Kai kuriais atvejais, padengimo **kodo** *laukas*, skirtas prekės padengimo įrašui, yra nustatytas kaip Planavimas, bet planavimo prioritetų modelis nėra nustatomas susijusiai padengimo grupei. Tokiais atvejais bet koks modelis, kurio prioriteto skaičiavimo metodo lauke nustatyta reikšmė Didžiausio atsargų kiekio procentas, **·** *·* **·** *o* laukas Suplanuoto užsakymo kūrimas yra nustatytas kaip Vienas tiekimas, kurio prioritetas labai svarbus, bus taikomas pagal numatytuosius nustatymus.

Nustatykite **padengimo kodo** lauką *Kaip Prioritetas,* kad prekės **padengimo parametruose** būtų galima naudoti lauką Užsakymo vieta. Šiame lauke įveskite užsakymo taškų kiekį, kurį sistema turi naudoti, kai nustato, kada pateikti suplanuotus **užsakymus**, kurių padengimo kodo vertė yra *Prioritetas*.

Užsakymo taškų kiekis dažnai skaičiuojamas kaip poreikis per gamybos laiką, pridėjus minimalią vertę (pakankamai atsargų). Ji turi būti reikšmė tarp minimalių ir **maksimalių** **verčių**.

Pavyzdžiui, laukus galite nustatyti tokiu būdu:

- **Mažiausia:** *10*
- **Užsakymo vieta:** *45*
- **Didžiausia:** *60*

Pavyzdžiui, užsakymo taškų kiekio pagrindas yra septynios dienos gamybos laikas, o vidutinis kasdienis naudojimas – 5. Todėl gamybos laiku poreikis yra 35. Tada pridedama bent 10 (šio kartotinio atsargų) vertė, kad būtų galima gauti 45 neįvykdyto užsakymo tašką. Naudojant šį nustatymą, bus pasiūlyta tiekti, kai projektuotas turimo atsargų lygis bus mažesnis nei 45. Užsakymo prioritetas bus paremtas planavimo prioriteto nustatymu.

### <a name="manage-planning-priority-models"></a>Tvarkyti planavimo prioritetų modelius

Dirbti su planavimo prioriteto modeliais. Atlikite šiuos veiksmus.

1. Pereikite prie bendrojo **planavimo nustatymo \>\> planavimo prioritetų modelių**.
1. Sąrašo srityje pasirinkite esamą modelį arba veiksmų srityje **pasirinkite** Naujas, kad sukurtumėte naują modelį.
1. Naujojo įrašo antraštėje nustatykite toliau pateiktus laukus:

    - **Pavadinimas** – įveskite modelio pavadinimą. Pavadinimas turi būti unikalus visuose jūsų organizacijos juridiniuose subjektuose.
    - **Aprašymas** – įveskite modelio aprašymą.
    - **Prioritetų skaičiavimo metodas** – pasirinkite vieną iš šių verčių:

        - *Prioritetų diapazonai* – pasirinkus šią reikšmę, tampa pasiekiamas **planavimo prioritetų diapazonų** tinklelis. Ten turite nustatyti keletą prioritetų diapazonų, kad būtų galima apibrėžti planavimo prioriteto vertę.
        - *Maksimalaus atsargų kiekio procentinė dalis* – skaičiuokite planavimo prioriteto vertę kaip procentinę dalį, remiantis planuotais atsargų kiekiais virš didžiausio atsargų kiekio.

    - **Suplanuoto užsakymo** kūrimas – šis laukas galimas, kai **lauke** Prioriteto skaičiavimo būdas nustatomas prioritetų *diapazonai*. Pasirinkite vieną iš šių reikšmių:

        - *Bendras tiekimas, kai prioritetas svarbus* – neskaidyti suplanuotų užsakymų pagal prioritetų diapazoną. Suplanuoto užsakymo planavimo prioritetas remiasi svarbiausiu prioritetų diapazonu (tai yra, mažiausia planavimo prioriteto verte).
        - *Skaidyti pagal prioriteto diapazonus* – išskaidyti poreikį į kelis suplanuotus užsakymus, remiantis planavimo prioritetų diapazonais. Atskirų suplanuotų užsakymų planavimo prioritetas nustatomas pagal susijusio planavimo prioritetų diapazono planavimo prioritetą.

    - **Apsvarstykite poreikio** prioritetą – nustatykite šią pasirinktį *kaip* Taip, jei norite apriboti naujo suplanuoto užsakymo, sukurto tiekimui, prioritetą. (Prioritetas nebus mažesnis nei susijusio poreikio prioritetas.) Jei nustatote šią pasirinktį *kaip* Ne, skaičiuojant tiekimo užsakymo prioritetą nebus atsižvelgiama į poreikio užsakymo prioritetą.

1. Jei Nustatote **Prioriteto skaičiavimo** *metodo lauką kaip Prioriteto diapazonus, naudokite mygtukus Įtraukti ir Pašalinti, esančius* **planavimo prioritetų diapazonų "FastTab",** **·** **jei** norite įtraukti ar pašalinti prioriteto diapazono eilutes, jei reikia. Jei yra kelios eilutės, o jūs įterpsite naują eilutę, planavimo prioritetas bus automatiškai nustatytas kaip pasirinktos eilutės ir aukščiau nurodytos eilutės vidurkis. Kiekvienai eilutei nustatykite šiuos laukus:

    - **Planavimo prioritetas** – įveskite bet kurią vertę nuo 0,00 iki 100,00. Ši vertė nurodo planavimo prioritetą, kuris naudojamas eilutėje. Mažiausia prioriteto vertė nurodo aukščiausią prioritetą. Priskiriama numatytoji vertė, tačiau, jei reikia, galite ją pakeisti. Ta pati **planavimo prioriteto** vertė negali būti naudojama daugiau nei vienam to paties planavimo prioriteto modelio planavimo prioritetų diapazonui.
    - **Aprašymas** – įveskite planavimo prioriteto diapazono aprašymą (pvz., *Pertvarkyti tašką iki maksimumo*).
    - **Nuo kiekio** – apatinė planavimo prioritetų diapazono riba. Ši vertė yra tik skaitoma ir yra paremta **ankstesnio** **planavimo** prioritetų diapazono kiekio Iki ir Procento nuo kiekio vertėmis.
    - **Kiekis Iki** – pasirinkite prekės padengimo lauką, kuris turi būti naudojamas norint nurodyti viršutinę diapazono ribą. Šios vertės yra palaikomos ir turės įtakos kito **diapazono** kiekio vertei Nuo:

        - *Nulis* – ši vertė rodo neigiamą diapazoną iki nulio (nuo *nulio iki* *nulio*). Eilutėms, kuriose pasirinkta ši vertė, kiekio **iki** kiekio procentas yra tik skaitomas ir visada nustatomas *100* procentų.
        - *Minimalus atsargų kiekis* – ši vertė rodo minimalią **prekės** vertę prekių padengimo **puslapyje**. Eilučių, kuriose pasirinkta ši vertė, **·** **lauke** Iki kiekio procentas galima redaguoti ir naudojama kito diapazono kiekio Nuo vertei nustatyti (pvz., *iki 80% minimalaus atsargų kiekio).*
        - *Pakartotinio užsakymo* vieta – ši vertė rodo **prekės užsakymo** taškų vertę prekių padengimo **puslapyje**. Eilutėse, kuriose pasirinkta ši vertė, **·** **kiekio** iki procentinės dalies laukas redaguojamas ir naudojamas nustatyti kiekio nuo vertę kitame diapazone (pvz., iki *80% neįvykdyto* skaičiaus).
        - *Maksimalus atsargų kiekis* – ši vertė rodo maksimalią **prekės** vertę prekių padengimo **puslapyje**. Jei pasirinkta ši vertė, **·** **eilučių** kiekio iki kiekio laukas yra redaguojamas ir naudojamas kito diapazono kiekiui Nuo nustatyti (pvz., *iki 80% minimalaus atsargų kiekio).*
        - *Neribotos* – ši vertė nurodo neribotą viršutinį diapazono lygį (neribotą *arba mažesnį iki* neriboto *·*). Eilutėms, kuriose pasirinkta ši vertė, kiekio **iki** kiekio procentas yra tik skaitomas ir visada nustatomas *100* procentų.

    - **Kiekio iki procentas** – įveskite procento vertę, kuri naudojama skaičiuojant viršutinę planavimo prioritetų diapazono ribą, **remiantis lauke Į kiekį pasirinkta** verte. Pavyzdžiui, **·** *jei* lauke Iki kiekio nustatyta minimalių atsargų kiekio reikšmė, **·** *o kiekio iki kiekio lauke nustatyta 50*, viršutinė riba bus 50 procentų minimalaus atsargų kiekio iš susijusios prekės padengimo.

1. Numatytuosiuose **planavimo prioriteto "FastTab" nustatykite laukus, kai reikia nurodyti numatytuosius** planavimo prioritetus kiekvienam tiekimo ar poreikio eilutės tipui (pardavimo užsakymui, pirkimo užsakymui, perkėlimo užsakymui arba poreikio prognozei). Gali būti įvestos tik teigiamos vertės.

## <a name="view-and-maintain-planning-priority"></a>Peržiūrėti ir prižiūrėti planavimo prioritetą

Planavimo prioritetas rodomas ir nustatomas lauke **Planavimo** prioritetas. Šį lauką galite rasti puslapiuose, kurie išvardyti šioje lentelėje. Prioritetas nustatomas kaip skaičius nuo 0 (nulio) iki 100, o 0 reiškia aukščiausią svarbą.

| Puslapis | Lauko vieta | Reikšmės šaltinis |
|---|---|---|
| Poreikio prognozės eilutės | <p>**Skirtukas** Prekė</p><p>(Pasirinkite eilutę viršutinėje dalyje ir pasirinkite **Skirtukas** Prekė.)</p> | Rankiniu būdu nustatoma numatytoji vertė arba vertė |
| Pardavimo užsakymo informacija | <p>**Eilutės** informacijos " **FastTab" pristatymo** skirtukas</p><p>(Pasirinkite eilutę lauke **Pardavimo užsakymo eilučių** "FastTab", tada eilutės informacijos **"** FastTab" pasirinkite skirtuką **Pristatymas**.)</p> | Neautomatiniu būdu nustatyta numatytoji vertė, vidinės įmonės vertė arba vertė |
| Pirkimo užsakymo informacija | <p>**Eilutės** informacijos " **FastTab" pristatymo** skirtukas</p><p>(Pasirinkite eilutę lauke **Pirkimo užsakymo eilučių** "FastTab", tada eilutės informacijos **"** FastTab" pasirinkite skirtuką **Pristatymas**.)</p> | Vertė, nustatoma patvirtinti iš suplanuotų užsakymų, vidinės įmonės vertės arba neautomatiniu būdu nustatytos vertės |
| Perkėlimo užsakymo informacija | <p>**Eilutės** informacijos " **FastTab" pristatymo** skirtukas</p><p>(Pasirinkite eilutę lauke **Perkėlimo užsakymo eilučių** "FastTab", tada eilutės informacijos **"** FastTab" pasirinkite skirtuką **Pristatymas**.)</p> | Vertė, nustatoma patvirtinti iš suplanuotų užsakymų arba vertės, nustatytos rankiniu būdu |
| Suplanuoto užsakymo informacija | **Bendra "** FastTab" | Vertė, skaičiuojama bendrojo planavimo metu arba neautomatiniu būdu nustatoma vertė |

### <a name="intercompany-trade"></a>Vidinės įmonės prekyba

Planavimo **prioriteto** vertė vidinės įmonės tiekimo ir poreikio eilutėse bendrai naudojama susietiems subjektams. Bet kurios pusės modifikavimas bus susietas užsakymo eilutėje.

Štai keletas pavyzdžių:

- Vartotojas pakeičia vidinės įmonės pardavimo užsakymo eilutės planavimo prioritetą nuo 20 iki 30. Šis pakeitimas rodomas susietame vidinės įmonės pirkimo užsakymo eilutėje.
- Vartotojas pakeičia vidinės įmonės pirkimo užsakymo eilutės planavimo prioritetą nuo 40 iki 50. Šis pakeitimas rodomas susieto vidinės įmonės pardavimo užsakymo eilutėje.
