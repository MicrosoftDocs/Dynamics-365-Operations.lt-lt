---
title: Kreditų valdymo parametrų nustatymas
description: Šiame straipsnyje aprašomos pasirinktys, kurias galite naudoti norėdami konfigūruoti kredito valdymą, kad jis atitiktų jūsų verslo poreikius.
author: JodiChristiansen
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8955518e7b5c0200d3827c1c22b7d150a09be244
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799551"
---
# <a name="credit-management-parameters-setup"></a>Kreditų valdymo parametrų nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos pasirinktys, kurias galite naudoti norėdami konfigūruoti kredito valdymą, kad jis atitiktų jūsų verslo poreikius. Norėdami naudoti kreditų valdymo funkcijas, puslapyje **Kredito ir surinkimo parametrai** (**Kreditas ir surinkimas \> Nustatymas \> Kredito ir surinkimo parametrai**).

## <a name="credit-parameters"></a>Kreditų parametrai

Skyriuje **Kreditas** yra keturi „FastTab“, kur galite pakeisti parametrus, kontroliuojančius kreditų valdymą: **Kredito sulaikymas**, **Kreditų valdymo kontrolinis taškas**, **Kreditų valdymo statistika** ir **Kredito limitas**. Toliau esančiuose skyriuose aprašomi kiekvieno „FastTab“ parametrai.

### <a name="credit-holds"></a>Kredito sulaikymai

- Nustatykite **Leisti redaguoti prekybos užsakymų vertę po to, kai laikomas užsakymas yra paleidžiamas** parinktį į **Ne** tam, kad publikavimo taisyklės būtų dar kartą tikrinamos, jei prekybos užsakymo vertę (išplėsta kaina) buvo padidinta, nes prekybos užsakymas buvo paleistas iš laikomų sąrašo.
- Lauke **Atšauktų užsakymų priežastys** pasirinkite išleidimo priežastį, kuri bus naudojama pagal numatytuosius parametrus, kai pardavimo užsakymas, kuris buvo kreditų valdymo sulaikymų sąraše, yra atšaukiamas.
- Nustatykite parinktį **Patikrinti klientų kredito grupių kredito limitą** kaip **Taip**, kad galėtumėte patikrinti klientų kredito grupės kredito limitą, kai pardavimo užsakymas priklauso klientų kredito grupei. Bus patikrintas grupės kredito limitas; tada, jei jis pakankamas, bus patikrintas kliento kredito limitas.
- Nustatykite parinktį **Patikrinti kredito limitą, kai mokėjimo sąlygos padidinamos** kaip **Taip**, jei norite patikrinti mokėjimo sąlygų reitingus, kad nustatytumėte, ar pardavimo užsakymo mokėjimo sąlygos skiriasi nuo numatytųjų kliento mokėjimo sąlygų. Jeigu naujos mokėjimo sąlygos turi aukštesnį reitingą nei originalios mokėjimo sąlygos, užsakymas įtraukiamas į kreditų valdymo sulaikymo sąrašą.
- Nustatykite parinktį **Patikrinti kredito limitą, kai atsiskaitymo nuolaida padidinama** kaip **Taip**, jei norite patikrinti atsiskaitymo nuolaidos reitingus, kad nustatytumėte, ar pardavimo užsakymo mokėjimo nuolaida skiriasi nuo numatytosios kliento mokėjimo nuolaidos. Jeigu nauja mokėjimo nuolaida turi aukštesnį reitingą nei originali mokėjimo, užsakymas įtraukiamas į kreditų valdymo sulaikymo sąrašą.
- Lauke **Modifikuotų užsakymų išleidimo priežastis** pasirinkite išleidimo priežastį, kuri bus naudojama pagal numatytuosius parametrus, kai modifikuoti užsakymai automatiškai išleidžiami iš kreditų valdymo sulaikymo.
- Nustatykite parinktį **Ignoruoti kredito limito nebegaliojančią blokavimo taisyklė, kai galiojimo data yra tuščia** kaip **Taip**, kad galėtumėte valdyti taisyklės **Kredito limito galiojimas pasibaigęs** elgseną. Nustatykite pasirinktį kaip **Ne**, kad būtų blokuojamas užsakymas, kai galiojimo data yra tuščia.
- Sandėlio valdyme kroviniai gali būti kuriami pardavimo užsakymo įvedimo metu. Nustatykite parinktį **Pašalinti užblokuotas krovinio eilutes** kaip **Ne**, kad pardavimo užsakymo eilutės būtų sulaikytos, kai sulaikytas pardavimo užsakymo kreditas. Krovinio negalima apdoroti, kol sulaikytas pardavimo užsakymas. Nustatykite parinktį kaip **Taip**, kad pašalintumėte pardavimo užsakymo eilutes iš krovinio, kai sulaikytas pardavimo užsakymo kreditas. Tada krovinys gali būti apdorojamas.
- Pardavimo užsakymai gali būti automatiškai išleidžiami iš kreditų valdymo peržiūros. Lauke **Automatinio išleidimo priežastys**, pasirinkite išleidimo priežastį, kuri bus naudojama kaip numatytoji, kai automatiškai išleidžiami pardavimo užsakymai.
- Pardavimo užsakymai gali būti automatiškai išleidžiami iš kreditų valdymo peržiūros. Lauke **Automatinis išleidimas** pasirinkite **Be registravimo**, kad išleistumėte sulaikytą užsakymą. Turite rankiniu būdu vykdyti procesą, dėl kurio užsakymas yra sulaikytas. Pasirinkite **Su registravimu**, kad būtų užregistruotas užsakymas naudojant tą patį registravimo procesą, kuris buvo vykdomas, kai pardavimo užsakymas buvo sulaikytas.

### <a name="credit-management-checkpoint"></a>Kredito valdymo kontrolinis taškas

Galite nustatyti laiką, kuris naudojamas tikrinti pardavimo užsakymus, turinčius problemų dėl kredito. „FastTab“ **Kreditų valdymo kontrolinis taškas** identifikuoja dokumentų registravimo procesus, kuriuos sudaro kreditų valdymo taisyklių apdorojimas. Taip pat galite patikrinti kredito taisykles, kai atliekate išankstinį registravimą arba visapusį pardavimo užsakymo registravimą. Pažymėkite žymės langelius, norėdami nurodyti registravimo procesus, kurie turėtų sulaikyti užsakymą, jei išdavimas randamas apdoroje kredito valdymo blokavimo taisykles.

Taip pat galite nurodyti atidėjimo dienų skaičių prieš dar kartą tikrinant kredito taisykles. Nors galite nurodyti, kad kreditų valdymo taisyklės gali būti patikrinamos registravimo metu, taisyklės nebus tikrinamos nurodytą atidėjimo dienų skaičių. Pavyzdžiui, jūs patvirtinate pardavimo užsakymą vieną dieną, ir nurodote dvi patvirtinimo veiksmo atidėjimo dienas. Šiuo atveju kredito taisyklės nebus tikrinamos kitame registravimo etape (pvz., važtaraščio kūrimas arba užsakymo SF išrašymas) iki keturių dienų. Keturių dienų arba po keturių dienų taisyklės bus patikrintos dar kartą, kai bus registruojama, o atidėjimo dienų skaičius bus pakeistas į vertę, nurodytą kitame registravimo kontroliniame taške.

Jei nenurodysite atidėjimo dienų skaičiaus, kredito taisyklės bus patikrintos kiekviename registravimo etape, kuris nustatytas kreditų valdymo taisyklių vykdymui. Jei pardavimo užsakymą išleisite be registravimo ir dar kartą vykdysite tą patį užsakymo apdorojimo veiksmą, kredito taisyklės vėl bus patikrintos. Pavyzdžiui, užsakymas sulaikytas po patvirtinimo, o jūs jį išleidžiate su arba be registravimo. Šiuo atveju užsakymas vėl bus sulaikytas, jei dar kartą patvirtinsite. Naudokite atidėjimo dienas, jei užsakymas turi būti perkeltas į kitą vykdymo veiksmą be pakartotinio sulaikymo.

> [!Note]
> Jei viename registravimo poste įvesta atidėjimo diena, visiems registruoti pažymėtims čekiams turi būti atidėjimo dienos.

- Pažymėkite registravimo **žymės** langelį, norėdami vykdyti kredito valdymo taisykles, kai vykdomas eilutėje rodomas registravimo kontrolinis taškas. Jei nepasirinksite žymės langelio, taisyklės bus tikrinamos tik vieną kartą per visą registravimo procesą.
- Jei pažymėsite žymės **langelį** Registravimas, nurodykite atidėjimo dienų, kurios turi praeiti prieš vėl pažymint blokavimo taisykles, skaičių. Negalima įtraukti atidėjimo dienų, jei žymės **langelis** Registravimas yra išvalytas.
- Pažymėkite pro **forma žymės** langelį, norėdami vykdyti kredito valdymo taisykles, kai vykdomas pro forma registravimo kontrolinis taškas, rodomas eilutėje. Dauguma atvejų laukas **Registravimas** dialogo lange nustatytas kaip **Ne**, kuris atsiranda užregistravus pardavimo užsakymą.
- Jei pažymėsite žymės **langelį** Registravimas, nurodykite atidėjimo dienų, kurios turi praeiti prieš vėl pažymint blokavimo taisykles, skaičių. Negalima įtraukti atidėjimo dienų, jei žymės **langelis** Registravimas yra išvalytas.

### <a name="credit-management-statistics"></a>Kredito valdymo statistika

Kelios kreditų valdymo statistikos yra įtrauktos į „FactBox“ **Kliento kredito valdymo statistika** puslapyje **Klientas**. Turite nurodyti keletą verčių, kurių reikia norint apskaičiuoti šiuos statistinius duomenis. „FactBox“ **Kliento kredito valdymo statistika** įveskite mėnesių skaičių, kuris naudojamas skaičiuojant šias reikšmes:

1. Pardavimo neapmokėjimo laikas dienomis 1
2. Pardavimo neapmokėjimo laikas dienomis 2
3. Vidurkio balansas 1
4. Vidurkio balansas 2
5. Vidutinis kredito limitas %
6. Vidutinis buvimas %

### <a name="credit-limits"></a>Kredito limitai

- Kreditų valdyme kliento kredito limitas rodomas kliento valiuta. Turite nustatyti kredito limito valiutos kurso tipą kliento valiuta. Lauke **Kredito limito valiutos kurso tipas** pasirinkite valiutos kurso tipą, kuris turi būti naudojamas konvertuojant pirminį kredito limitą į kliento kredito limitą.
- Nustatykite parinktį **Leisti rankinį kredito limitų redagavimą** kaip **Ne**, kad vartotojai negalėtų redaguoti kredito limitų puslapyje **Klientas**. Jei ši parinktis nustatyta kaip **Ne**, kliento kredito limito pakeitimai gali būti atliekami tik registruojant kredito limito koregavimo operacijas.
- Nustatykite **pasirinktį Praleisti atsargų rezervavimus**  **kaip Taip,** jei norite, kad būtų nepaisoma atsargų rezervavimo, kai patikrinamos kredito valdymo blokavimo taisyklės. Šiuo atveju kiekiai bus patikrinti ir bus įgalinti tikrinimo taško atidėjimo laikotarpiai, neatsižvelgiant į atsargų rezervavimo kiekį.
- Kai įgalintas kredito valdymas, tik laisvos **formos** SF apdoroti naudojamas pranešimo parametras, kai viršijamas kredito limitas. Nors pranešimai vis dar pridedami prie pardavimo užsakymų, kai klientai viršija savo kredito limitą, jei tokie pranešimai neužblokuoja patvirtinimo, išrinkimo dokumentų ir važtaraščių spausdinimo ar SF registravimo.

    Numatyta, kad kredito valdymas įgalintas, bet galite jį išjungti. Įgalinus šį raktą, norėdami nustatyti, kada klientai viršija savo kredito limitą, naudojate kredito valdymo blokavimo taisykles ir kontrolinius taškus. Jei jis uždraustas, pranešimai, kurie pridedami prie pardavimo užsakymų, remiantis lauko Pranešimas parametru viršijus kredito limitą **, gali padėti nustatyti,** kada klientai viršija savo kredito limitą.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Numeracijos ir bendrinami numeracijos parametrai

Norint apdoroti kredito limito koregavimus, reikalingas žurnalo ID. Turite įtraukti kredito limito koregavimo numerį, kuris turi būti naudojamas žurnalo ID generavimui.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
