---
title: Darbas su publikavimo grupėmis
description: Šioje temoje aprašoma publikavimo grupių funkcija „Microsoft Dynamics 365 Commerce“.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d757f34d3e16850e4f5de122f63b2b3342f612e49f07c7cf6585362999f03c02
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717677"
---
# <a name="work-with-publish-groups"></a>Darbas su publikavimo grupėmis

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma publikavimo grupių funkcija „Microsoft Dynamics 365 Commerce“.

„E-commerce“ svetainėse ištisus metus nuolat pateikiamas naujas turinys. Naujinimai dažnai pateikiami paketais svarbių el. prekybos įvykių metu, pvz., per šventes, sezonines rinkodaros kampanijas arba reklaminius paleidimus. Šiuose naujinimuose dažnai reikalaujama, kad svetainės turinio grupės (pavyzdžiui, puslapiai, vaizdai, fragmentai ir šablonai) būtų paruošiami, patvirtinami ir publikuojami tuo pačiu metu vienu veiksmu.

Galimybė grupuoti elementus į loginius rinkinius ir publikuoti elementus kartu, kai kiekvienam rinkiniui suteikiamas ciklas, suteikia daug privalumų svetainės autoriams. Programoje „Commerce“ šie loginiai rinkiniai vadinami publikavimo grupėmis. Jie leidžia svetainės autoriams sekti naujinimų rinkinius kaip savo konfigūruojamus, patikrinamus ir paskelbiamus objektus.

Autoriai gali peržiūrėti naujinimus, esančius paruoštoje publikavimo grupėje, nepaveikdami aktyvios svetainės ar kitų atskirų publikavimo grupių. Tada autoriai gali suplanuoti publikavimo veiksmą ir vienu metu publikuoti visus publikavimo grupės elementus aktyvioje svetainėje. Galimybė grupuoti, peržiūrėti ir planuoti publikavimo naujinimus yra svarbi daugeliui įmonės lygio bendrovių, kurios gauna dideles metines įplaukas vykstant su įvykiais susijusiems svetainės naujinimo etapams.

Įmonės gali patirti išlaidų dėl lėtų ar netinkamų turinio išvesčių, kurios nevyksta sklandžiai. Publikavimo grupės padeda užtikrinti, kad paleidimai būtų organizuojami, patvirtinami ir publikuojami laiku. Nesvarbu, ar paleidimai yra dideli, ar maži, publikavimo grupės pateikia vertingą įrankių rinkinį, kuris padeda autoriams organizuoti ir supaprastinti vykdomas svetainės naujinimo užduotis.

## <a name="when-to-use-publish-groups"></a>Kada naudojamos publikavimo grupės

Publikavimo grupes galite naudoti, kai turite paruošti ir publikuoti keletą dokumentų kartu. Pavyzdžiui, jei jūsų svetainėje turinys atnaujinamas kiekvieną sezoną, galite sukurti publikavimo grupes šiems sezoniniams rinkodaros pakeitimams. Jūsų „rudens sezono naujinimo“ publikavimo grupėje gali būti naujų sezoninių vaizdų, fragmentų su sezoniniais rinkodaros pranešimais, puslapių, kuriuose pateikiama sezoninių produktų rinkinių, arba kitų sezoninių svetainės naujinimų.

Publikavimo grupių privalumas yra tas, kad vienu metu galite paruošti keletą naujinimų. Pavyzdžiui, atnaujinus „rudens sezono naujinimo“ publikavimo grupę, netrukus gali būti pateikiamas tam tikro šventinio savaitgalio turinio naujinimas. Tokiu atveju galite paruošti „rudens sezono naujinimo“ publikavimo grupės turinį, kai ruošite vėlesnės „rudens šventės naujinimo“ publikavimo grupės turinį. Kiekvienoje publikavimo grupėje yra unikalus puslapių, vaizdų, fragmentų, šablonų ir t. t. rinkinys. Šias dvi publikavimo grupes galite paruošti, peržiūrėti ir patvirtinti atskirai, bet tuo pačiu metu. Tuomet galima suplanuoti, kad kiekviena publikavimo grupė būtų pateikiama svetainėje tam tikromis dienomis ir laiku.

## <a name="turn-on-the-publish-groups-feature"></a>Publikavimo grupių funkcijos įjungimas

Publikavimo grupių funkcija yra neprivaloma ir turi būti įjungta jūsų svetainėje.

Norėdami įjungti svetainės publikavimo grupių funkciją „Commerce“ kūrimo įrankiuose, atlikite toliau nurodytus veiksmus.

1. Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.
1. Dalyje **Svetainės parametrai** pasirinkite **Funkcijos**.
1. Nustatykite parinkties **Publikavimo grupės** vertę **Įjungta**.

## <a name="create-a-publish-group"></a>Publikavimo grupės kūrimas

Norėdami sukurti svetainės publikavimo grupę „Commerce“ kūrimo įrankiuose, atlikite toliau nurodytus veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Publikavimo grupės**.
1. Komandų juostoje viršuje pasirinkite **Nauja**.
1. Dialogo lango **Publikavimo grupės kūrimas** dalyje **Publikavimo grupės pavadinimas** įveskite aprašomąjį pavadinimą. Tada pasirinkite **Gerai**.

## <a name="set-the-publish-group-authoring-context"></a>Publikavimo grupių kūrimo konteksto nustatymas

Programoje „Commerce“ numatytasis kūrimo kontekstas yra aktyvios svetainės kontekstas. Aktyvios svetainės kūrimo kontekstas yra numatytasis rodinys, kuriame galite peržiūrėti ir atlikti keitimus tiesiogiai svetainėje, nenaudodami publikavimo grupės. Jame rodomi publikuotos svetainės versijos naujausi tiesioginiai naujinimai. Jei konteksto valdiklyje, esančiame dalyje **Publikavimo grupės** kairiojoje naršymo srityje rodomas pavadinimas **Aktyvi svetainė**, dirbate aktyvios svetainės kūrimo kontekste. **Aktyvi svetainė** yra numatytasis konteksto valdiklio pavadinimas. Priešingu atveju konteksto valdiklyje rodomas publikavimo grupės pavadinimas.

Norėdami dirbti publikavimo grupėje, turite persijungti į publikavimo grupės kūrimo kontekstą. Norėdami nustatyti publikavimo grupės kontekstą, atlikite vieną iš toliau nurodytų veiksmų.

- Kairiojoje naršymo srityje pasirinkite konteksto valdiklį tiesiogiai dalyje **Publikavimo grupės**, tada pasirodžiusiame parinkčių sąraše pasirinkite publikavimo grupės pavadinimą. Konteksto valdiklio pavadinimas pakeičiamas ir jame rodomas publikavimo grupės pavadinimas.
- Kairiojoje naršymo srityje pasirinkite **Publikavimo grupės**, tada dalyje **Publikavimo grupės** pasirinkite publikavimo grupės pavadinimą. Konteksto valdiklio pavadinimas pakeičiamas ir jame rodomas publikavimo grupės pavadinimas.

Nustatę publikavimo grupės kūrimo kontekstą, dirbate tame publikavimo grupės kontekste, kai peržiūrite ir redaguojate svetainės turinį.

Norėdami grįžti į numatytąjį aktyvios svetainės kūrimo kontekstą, pasirinkite konteksto valdiklį, tada pasirinkite **Aktyvi svetainė**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Puslapių arba kitų elementų įtraukimas į publikavimo grupę

Pasirinkę publikavimo grupės kūrimo kontekstą, ir kai kairiojoje naršymo srityje esančiame konteksto valdiklyje rodomas jo pavadinimas, galite kurti turinį taip, kaip jį kuriate numatytajame aktyvios svetainės kontekste. Taip pat galite įtraukti esamų puslapių ar kitų elementų iš kitų publikavimo grupių arba iš aktyvios svetainės konteksto.

Norėdami nukopijuoti esamus puslapius į publikavimo grupę, atlikite toliau nurodytus veiksmus.

1. Pasirinkite kūrimo kontekstą, iš kurio kopijuosite, o tada kairiojoje naršymo srityje pasirinkite **Puslapiai**.
1. Pasirinkite puslapį, kurį norite įtraukti į publikavimo grupę.
1. Komandų juostoje pasirinkite **Kopijuoti į publikavimo grupę**.
1. Dialogo lange **Pasirinkti publikavimo grupę** pasirinkite publikavimo grupę, į kurią norite įtraukti puslapį, tada pasirinkite **Gerai**.

Atlikdami tuos pačius pagrindinius veiksmus, galite kurti pritaikytus produktų puslapius, URL, šablonus, maketus, fragmentus ir medijos bibliotekos išteklius arba įtraukti esamų šių tipų elementų į publikavimo grupę.

## <a name="validate-a-publish-group"></a>Publikavimo grupės patikrinimas

Norėdami įsitikinti, kad įvykdytos visos publikavimo grupės turinio priklausomybės ir kad visi tikrinimai atlikti sėkmingai, paleiskite patikrinimą, kad nustatytumėte problemas, kurias būtina išspręsti prieš planuojant publikavimo veiksmą.

Norėdami patikrinti savo publikavimo grupę prieš ją suplanuodami, atlikite toliau nurodytus veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Publikavimo grupės**.
1. Pasirinkite tikrintiną publikavimo grupę.
1. Komandų juostoje pasirinkite **Tikrinti**.

Tikrinamas visas publikavimo grupės turinys. Visos problemos, dėl kurių nepavyksta sėkmingai publikuoti, rodomos viršutiniame dešiniajame kampe esančiame pranešimo lange.

> [!NOTE]
> Tikrinimas visada vykdomas automatiškai, kai suplanuojama publikavimo grupė. Tačiau komandų juostoje esantis mygtukas **Tikrinti** yra naudingas, nes jį paspaudus galima nustatyti problemas, kurias reikia išspręsti prieš bandant suplanuoti publikavimo grupės įgyvendinimą.

## <a name="schedule-a-publish-group-to-go-live"></a>Publikavimo grupės įgyvendinimo planavimas

Norėdami suplanuoti publikavimo grupės įgyvendinimą svetainėje, atlikite toliau nurodytus veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Publikavimo grupės**.
1. Dalyje **Publikavimo grupės** pasirinkite suplanuotiną publikavimo grupę.
1. Komandų juostoje pasirinkite **Redaguoti grafiką**. Rodomas dialogo langas **Redaguoti grafiką**.
1. Pasirinkite publikavimo grupės įgyvendinimo datą ir laiką, tada pasirinkite **Gerai**.

Norėdami atšaukti publikavimo grupės planavimą, atlikite tuos pačius veiksmus, bet pasirinkite **Atšaukti publikavimo grupės planavimą** dialogo lange **Redaguoti grafiką**.

> [!NOTE]
> Labai didelių publikavimo grupių publikavimas gali užtrukti minutę arba dvi, atėjus jų suplanuotam laikui. Atminkite, kad publikavimo veiksmas nėra momentinis ir kad mažesnės publikavimo grupės bus paskelbtos greičiau.

## <a name="publish-groups-faq"></a>DUK apie publikavimo grupes

**Kiek elementų gali būti publikavimo grupėje?**

Šiuo metu limitas yra 2 000 elementų vienoje publikavimo grupėje. Atminkite, kad labai didelių publikavimo grupių publikavimas gali užtrukti keletą minučių, atėjus jų suplanuotam laikui.

**Ar publikavimo grupės yra panašios į kodą „šakos“, naudojamą programinės įrangos kūrimo terminijoje?**

Ir taip, ir ne. Publikavimo grupes galima traktuoti kaip svetainės išsišakojimo versijas. Taip į jas žiūrint, jos veikia kaip šakos. Tačiau nėra suliejimo sąvokos atskirų elementų lygiu. Paskutinis publikuotas elementas perrašo ankstesnį ir naujausias publikavimo veiksmas visada pakeičia ankstesnius publikavimo veiksmus.

**Ar galiu suplanuoti, kad dvi publikavimo grupės būtų įgyvendinamos tuo pačiu metu?**

Nr. Dėl su našumu ir konfliktais susijusių priežasčių sistema privers jus padaryti mažiausiai penkių minučių pertraukas tarp suplanuotų publikavimo grupių.

**Ar galiu naudoti publikavimo grupes daugiakanalio sprendimo operacijų skyriaus elementams, pvz., nuolaidoms ir produktų naujinimams, planuoti?**

Šiuo metu publikavimo grupių funkcija palaiko tik svetainės turinį. Tačiau „Microsoft“ supranta, kad integravimas į operacijų skyriaus prekybos scenarijus gali būti vertingas koordinuojant ir automatizuojant daugiakanalio sprendimo kampanijos paleidimus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Turinio įtraukimo būdai](add-manage-content.md)

[Puslapio modelio žodynas](page-elements-overview.md)

[Dokumentų būsenos ir vykdymo ciklas](document-states-overview.md)

[Kelių kanalų bendrinimo funkcijos įjungimas ir naudojimas](cross-channel-sharing.md)

[Darbas su moduliais](work-with-modules.md)

[Darbas su fragmentais](work-with-fragments.md)

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Svetainės naršymo tinkinimas](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
