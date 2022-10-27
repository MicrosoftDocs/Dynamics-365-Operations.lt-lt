---
title: DK sudengimų automatizuojami
description: Šiame straipsnyje pateikiama informacija apie DK sudengimų automatų procesą.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2022
ms.locfileid: "9707763"
---
# <a name="automate-ledger-settlements"></a>DK sudengimų automatizuojami

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 10.0.31 **** finansų versijoje funkcijų valdymo darbo srityje galima rasti DK sudengimų automatinių **sudengimų proceso** priemonę. Dk sudengimų **automatinių sudengimų proceso priemonę** **galima įgalinti tik tada, jei įgalinta DK sudengimo ir uždarymo metų** pabaigos funkcijos supratimas.

DK sudengimas yra debeto ir kredito operacijų gretinimo DK procesas. Organizacijos, pasikartojančioje grafike atliekantys DK sudengimo operacijas, dabar gali automatizuoti procesą. Automatinio DK sudengimo proceso metu debeto ir kredito operacijos gali būti automatiškai sugretintos tik tada, jei jų sumos apskaitos valiuta yra vienodos.Pavyzdžiui, debeto suma, $1.00 gali būti automatiškai sugretinta su sf $1.00. Tačiau debeto vertė $1.00 negali būti automatiškai sugretinta su dviem kreditais, kiekvieno iš jų vertė $0.50. Dalinis DK operacijų sumų gretinimas nepalaikomas.

DK sudengimo automatizavimas apibrėžia šią informaciją:

- Paleidus DK sudengimą
- Kokie kriterijai naudojami norint sugretinti debetus ir kreditus, kuriuos galima sudengti automatiškai
- Kokia tvarka apdorojama DK sudengimo informacija

## <a name="define-the-occurrence-of-ledger-settlements"></a>Nustatyti DK sudengimų įvykį

DK sudengimo automatizavimas naudoja procesų automatizavimo sistemą. Skirtingi verslo procesai naudoja šią sistemą, kad nustatytų pasirinkto proceso įvykį. Norėdami sudengti DK, eikite į  **Sistemos administravimo \> nustatymo \> proceso automatizavimą** **arba DK DK \> nustatymo \> procesų automatizavimą**.

Pirmiausia pasirinkite parinktį Kurti **naują proceso automatizavimą** ir pasirinkite DK sudengimų ****. Tada vedlys padės jums nustatyti automatizavimą.

## <a name="general-page"></a>Puslapis „Bendra“

 **Vedlio** bendrajame puslapyje įveskite kuriamo DK sudengimo pasikartojimo pavadinimą. Pavyzdžiui, jei jūsų sutampantys debetai ir kreditai DK sudengti pirmadienį, įveskite aprašomąjį pavadinimą, pavyzdžiui, **LedgerSettle\_ Mon**. Pavadinimas, kurį įvedate, rodomas automatizavimo **taisyklės stulpelyje**, DK **sudengimų puslapyje** .

Likę puslapio parametrai yra bendri ir nurodo šios DK sudengimų versijos pasikartojimo trafaretą. Pavyzdžiui, jei įvykis yra pirmadienis, galite nurodyti, kad jis būtų paleidžiamas kas savaitę, o jūs galite pasirinkti, kad pirmadienis būtų savaitės diena, kai jis paleidžiamas. Taip pat galite įvesti ankstyvą grafiko laiką, pvz., 2.00 val. ryto, kad automatizuotas procesas būtų užbaigtas prieš prasidedant kitai darbo dienai. Rekomenduojame suplanuoti procesų automatizavimą, kad jis būtų atliekamas už įprastų darbo valandų. Tokiu būdu galite sumažinti savo apskaitos darbuotojų įtaką darbo dienos metu.

Daugiau informacijos apie kitus laukus, esančius bendrajame **puslapyje** , ieškokite proceso automatizavimo dokumentuose.

## <a name="ledger-settlements-match-criteria-page"></a>DK sudengimų gre nustatymo kriterijų puslapis

Kitas vedlio puslapis yra DK sudengimų **gre nustatymo kriterijų** puslapis. Jis naudojamas apibrėžti pagrindines sąskaitas, kurios yra įtrauktos į proceso automatizavimo įvykį, ir kriterijus, kurie naudojami debetams ir kreditams gretinimo nustatyti.

### <a name="account-selection"></a>Sąskaitos pasirinkimas

Rodomos pagrindinės sąskaitos, kurias anksčiau apibrėėte kaip juridinio subjekto DK sudengimo sąskaitas. (Pagrindines sąskaitas apibrėžiate kaip DK sudengimo sąskaitas **DK DK \> nustatymas DK \> parametrai DK sudengimas \>**.)

### <a name="main-account-and-posting-layer"></a>Pagrindinė sąskaita ir registravimo sluoksnis

Pagrindinės  **sąskaitos ir** registravimo **sluoksnio** vertės turi atitikti kriterijus. DK **debeto** operacijos **ir kredito** operacijos pagrindinės sąskaitos ir registravimo sluoksnių vertės turi būti lygios, kad automatinio DK sudengimo proceso metu būtų sugretintos.

### <a name="posting-type"></a>Registravimo tipas

Pasirinkti registravimo **tipo pasirinktį**, jei DK debeto ir kredito operacijų registravimo tipas turi būti toks pats, kad būtų galima sugretinti automatinio DK sudengimo proceso metu.

### <a name="financial-dimensions"></a>Finansinės dimensijos

Pasirinkite dimensijų **pasirinktį**, jei DK debeto ir kredito operacijose turi būti tos pačios finansinės dimensijos, kad jos būtų sugretintos automatinio DK sudengimo proceso metu. Kai ši pasirinktis pasirinkta, finansinių dimensijų reikšmių kriterijus reikia pasirinkti sąraše **Galimos finansinės dimensijos**. Galimose **finansinių** dimensijų sąraše nėra pagrindinės sąskaitos dimensijos, nes ji automatiškai būtina kaip gretavimo kriterijų dalis.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Peržiūrėti DK sudengimo automatizavimo rezultatus

Sukūrus DK sudengimo automatizavimo seriją, kiekvieno DK sudengimo pasikartojimai parodomi proceso automatizavimo savaitės rodinyje. Be to, rodoma kiekvieno įvykio būsena. Naudojamos šios būsenos:

- **Suplanuotas**  – automatizavimas suplanuotas, bet dar nėra paleistas.
- **Vykdomas –** automatizavimas šiuo metu vykdomas.
- **Klaida**  – automatizavimas vykdomas, bet įvyko klaida. Klaidas galite peržiūrėti pasirinkdami rezultatų **peržiūros** mygtuką.
- **Baigta**  – automatizavimas atliktas sėkmingai. Sudengimo rezultatus galite peržiūrėti DK sudengimų **puslapyje**.

Norėdami peržiūrėti gretinimo rezultatus, eikite į **DK periodinių užduočių \> DK \> sudengimą**. DK **sudengimų** puslapio automatizavimo **taisyklės lauke** rodomas automatizuoto DK sudengimo suplanuotos užduoties, kuri buvo naudojama operacijai sudengti, pavadinimas. Nesėkmingi sudengimo bandymai nebus atnaujinti automatizavimo **taisyklės** vertės. Jei neautomatiniu būdu atšauksite operaciją, kuri anksčiau buvo sėkmingai sudengta automatizavimo proceso metu, **bus pašalinta** automatizavimo taisyklės vertė.

Sugretintų **įrašų** sudengimo datos lauke rodoma data, kada buvo atliktas automatizavimo procesas.

## <a name="editing-a-ledger-settlement-automation"></a>DK sudengimo automatizavimo redagavimas

Procesų automatizavimo sistema leidžia redaguoti serijas ir atvejus, kurie sukurti DK sudengimo. Serijas galima redaguoti procesų automatizavimo puslapyje **arba proceso automatizavimo** kassavaitinio rodinio rodinyje. Pavyzdžiui, jei vadovas nusprendžia ATLIKTI DK sudengimą trečiadienį vietoj pirmadienio, **jis gali surasti įvykį savaitės rodinyje ir pasirinkti Peržiūrėti/Redaguoti – Serija**.

Redaguojant seką, jus paragins nurodyti, ar keisti visus esamus atvejus, ar tik naujus atvejus. Retrospektyviniai įvykiai, kurių būsena **jau yra** Baigta arba kurie baigėsi **** būsena Klaida, nebus keičiami.

Taip pat galite įtraukti naują įvykį arba pakeisti esamą įvykį. Pavyzdžiui, kitas DK sudengimo įvykis planuojamas vykdyti trečiadienį, sausio 1 d., tačiau ši data yra šventinė diena. Įvykį galite pakeisti procesų automatizavimo puslapyje **arba** proceso automatizavimo kassavaitinio rodinio rodinyje. Atidarytas puslapis, kuriame pateikiama grafiko informacija ir atitikimo kriterijai. Jame galite redaguoti suplanuotą laiką ir datą. Jei reikia pakeitimų, taip pat galite redaguoti gretapo kriterijus. 

Taip pat galite išjungti įvykį ar seką. Norėdami išjungti įvykį ir sustabdyti jo apdorojimą, pasirinkite jį proceso automatizavimo savaitės rodinyje, tada pasirinkite **Išjungti**. Galite išjungti seriją procesų **automatizavimo** puslapyje.

## <a name="security-for-ledger-settlement-automation"></a>DK atsiskaitymo automatizavimo sauga

**Prie** apskaitos vadovo ir apskaitos prižiūrėtojo vaidmenų pridėta pareiga Prižiūrėti DK sudengimų automatizavimo serijos parametrus, **o** DK sudengimų automatizavimo serijos parametrų peržiūros pareiga įtraukta į apskaitos, apskaitos vadovo ir apskaitos prižiūrėtojo vaidmenis DK sudengimo automatizavimo vaidmenims. Šios pareigos yra numatytieji saugos parametrai, tačiau juos galima keisti pagal jūsų organizacijos reikalavimus.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>DK parametrų nustatymas DK sudengimo automatizavimui

Įprastas **sudengimo** balanso laukas nurodo tvarką, pagal kurią bus apdorojamas automatinis DK sudengimas. Norėdami nustatyti arba peržiūrėti įprasto balanso sudengimo **vertę,** eikite į DK **nustatymas \> DK parametrus \>** ir pasirinkite skirtuką DK sudengimas **.**

Jei **pasirinktas** debetas, automatizuotas DK sudengimo procesas prasideda debeto pusėje ir ieško atitinkamų kreditų. Jei **pasirinktas** kreditas, automatizuotas DK sudengimo procesas prasideda kredito pusėje ir ieško atitinkamų debetų. Ši pasirinktis turi atspindėti įprastą pagrindinės sąskaitos balansą.

## <a name="processing-a-ledger-settlement-automation"></a>DK sudengimo automatizavimo apdorojimas

Paleidus automatizavimą, sistema pasirenka pagrindinių sąskaitų, nustatytų proceso automatizavimo serijai, DK operacijas. Ji užsakė operacijas pagal datą, naudodama datų diapazoną nuo finansinių metų pradžios iki proceso automatizavimo pradžios datos. Jis sugretinimas pagrįstas nurodytais grečių kriterijais. Reikia sudengti absoliučias debeto ir kredito apskaitos valiutos sumų vertes.

Kai pagrindinę sąskaitą apdorojo DK sudengimo automatizavimo įvykis, jos negalima parodyti DK **sudengimų** puslapyje. Turite palaukti, kol bus užbaigtas automatizavimo procesas. Rekomenduojame suplanuoti procesų automatizavimą, kuris būtų vykdomas ne darbo valandomis, kad būtų išvengta konfliktų.

Automatizavimo procesas apims visas operacijas, kurios atitinka kriterijus, išskyrus operacijas, **kurios DK sudengimų puslapyje pažymėtos sudengti** rankiniu būdu.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Operacijų, sudengtų automatizavimo procesu, atšaukimas

Galite atšaukti sudengimą, kuris buvo atliktas automatizuoto DK sudengimo proceso metu. Kai operacija, kuri buvo sudengta automatizavimo procesu, atšaukiama automatizavimo **taisyklės** vertė bus pašalinta.
