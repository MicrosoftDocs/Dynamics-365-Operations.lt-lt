---
title: Sandėlio intervalas
description: Šioje temoje pateikiama informacija apie sandėlio intervalą. Sandėlio intervalas leidžia konsoliduoti poreikį pagal prekę ir matavimo vienetą iš užsakymų, kurių būsena yra Užsakytas, Rezervuotas arba Išleistas. Jis padeda sandėlio vadovams sumaniai planuoti paėmimų vietas dar prieš tai, kai jos išleidžia užsakymus į sandėlį ir sukuria paėmimų darbą.
author: mirzaab
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 36903bc7ce4164e42d191156b7d9e04bec84d4f6
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575152"
---
# <a name="warehouse-slotting"></a>Sandėlio intervalas

[!include [banner](../includes/banner.md)]

Keletas sandėlio vietų funkcijų yra prieinamos siekiant padėti sandėlio vadovams protingai planuoti paėmimo vietas prieš jiems paleidžiant užsakymus į sandėlį ir sukuriant paėmimo darbą.

*Sandėlio vietų funkcija* leidžia jums konsoliduoti poreikį pagal elementą ir matavimo vienetą iš užsakymų, kurie turi *Užsakyta*, *Rezervuota* ar *Išleista* būseną. Sugeneruota paklausa gali būti taikoma vietoms, kurios bus naudojamos paėmimui, atsižvelgiant į kiekį, vienetą, faktines dimensijas, fiksuotas vietas ir kita. Po to, kai buvo sukurtas intervalo planas, papildymo darbas gali būti sukurtas tam, kad būtų galima pasiekti reikiamą atsargų kiekį kiekvienoje vietoje.

*Sandėlio vietos užsakymų perdavimui* funkcija leidžia sandėlio vadovams papildyti paėmimo vietas priklausomai nuo poreikio perkelti užsakymus, kurie dar nėra paleisti į sandėlį. Tai užtikrina, kad paėmimo vietos apims visus vienetus, kurių reikia perduotiems užsakymams po jų paleidimo į sandėlį. Šiai funkcijai turite taip pat įjungti *Sandėlio vietų funkcijos* funkciją.

*Sandėlio vietų priskyrimo papildymo* funkcija įtraukia parinktį šablono eilutėms, kurios yra naudojamos *Sandėlio vietų funkcijos* funkcijos. Ši parinktis leidžia sistemai apgalvoti esamą turimą inventorių pagal tikslinę vietą. Dėl to, mažiau papildymų gali būti sukurta vienai vietai. *Sandėlio vietų priskyrimo papildymo* funkcijai turite taip pat įjungti *Sandėlio vietų funkcijos* funkciją. Ji gali būti pasirinktinai naudojama kartu su *Sandėlio vietų perduotiems užsakymams* funkcija.

## <a name="turn-on-the-warehouse-slotting-features"></a>Įjunkite sandėlio vietų funkcijas

Prieš tai, kai galėsite jas naudoti, jos turi būti įjungtos jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus tam, kad patikrintų funkcijų būseną ir įjungtų jas, jei to reikia. Įjunkite tolesnes funkcijas, kaip būtina:

- Sandėlio intervalo funkcija
- Sandėlio vietos perduotiems užsakymams

    > [!IMPORTANT]
    > Taigi *Sandėlio vietų funkcijos* funkcija turi būti įjungta prieš šią funkciją.

- Sandėlio vietų priskyrimo papildymai

    > [!IMPORTANT]
    > Taigi *Sandėlio vietų funkcijos* funkcija turi būti įjungta prieš šią funkciją.

## <a name="set-up-warehouse-slotting"></a>Sandėlio intervalo nustatymas

Norėdami naudoti sandėlio vietas, turite nustatyti tolesnius elementus savo sistemoje:

- Intervalo kūrimo matavimo vieneto pakopos
- Krypčių kodai
- Intervalo šablonai
- Vietos nurodymai

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a>Kurti matavimo vieneto pakopas intervalui

Matavimo vienetų pakopos įgalina sugrupuoti kelis matavimo vienetus, kad juos būtų galima nustatyti. Pavyzdžiui, jei kelių dydžių dėžės paimamos iš tos pačios dėžių paėmimo srities, visiems dydžiams galima sukurti vieną pakopą. **Turi būti sukurta kiekvieno matavimo vieneto eilutė, kuri turėtų būti pakopos dalis.**

1. Eikite į **Sandėlio valdymas \>Nustatymas \>Papildymas \> Matavimo vienetų pakopų intervalas**.
1. Pasirinkite **Naujas**.
1. Antraštėje nustatykite šias vertes:

    - **Matavimo vieneto pakopa:** *EaBoxPl*
    - **Aprašymas:** *Kiekviena dėžės paletė*

1. Pasirinkite **Įrašyti**.
1. „FastTab“ skirtuke **Matavimo vienetai** pasirinkite **Nauja** eilutės įtraukimui į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Vienetas:** *Dėžė*
    - **Aprašymas** – palikite šį lauką tuščią. Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.
    - **Vieneto klasė:** *Kiekis*

1. Pasirinkite **Nauja**, kad įtrauktumėte antrą eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Vienetas:** *ea*
    - **Aprašymas** – palikite šį lauką tuščią. Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.
    - **Vieneto klasė:** *Kiekis*

1. Pasirinkite **Nauja**, kad įtrauktumėte trečią eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Vienetas:** *PL*
    - **Aprašymas** – palikite šį lauką tuščią. Jis bus užpildytas automatiškai, kai įrašysite pakeitimus.
    - **Vieneto klasė:** *Kiekis*

1. Pasirinkite **Įrašyti**, kad įrašytumėte pakopą.

### <a name="create-a-directive-code-for-slotting"></a>Kurti nurodymo kodą, skirtą intervalui

Turite pasirinkti nurodymo kodą, kuris turi būti susietas su šablonu.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Nurodymų kodai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. **Nurodymo kodas** lauke įveskite *Intervalas*.
1. **Nurodymo aprašymas** lauke įveskite *Intervalas*.

### <a name="set-up-slotting-templates"></a>Intervalo šablonų nustatymas

Kiekvienas intervalo šablonas kontroliuoja atsargų priskyrimui tam tikroms sandėlio vietoms. Kiekviename šablone turi būti eilutė kiekvieno intervalo specifikacijai. Norėdami nustatyti intervalo šablonus, naudokite šiame skyriuje nurodytas procedūras.

1. Pasirinkite **Sandėlio valdymas \> Nustatymas \> Papildymas \> Intervalo šablonai**.
1. Pasirinkite **Naujas**, kad sukurtumėte šabloną.

Toliau turite nustatyti šablono antraštę, intervalo specifikacijas ir vietos nurodymus, kaip paaiškinta šiuose poskyriuose. Vietos nustatymo perduotiems užsakymams atspindi nustatymą vietoms pardavimų užsakymuose, bet **Paklausos tipo** laukelis yra nustatytas *Perduoti užsakymus*, o ne *Pardavimo užsakymai*.

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a>Nustatykite antraštę pardavimo užsakymo vietos šablonui

1. Šablono antraštėje nustatykite šias vertes:

    - **Intervalo šablonas:** _61_
    - **Aprašas:** _61_
    - **Reikalaujamas tipas:** *Pardavimo užsakymas*

        > [!NOTE]
        > Šiuo metu *Pardavimo užsakymai* ir *Perdavimo užsakymai* yra tik palaikomi paklausos tipai. Galite pasirinkti *Perduoti užsakymus* tik jei *Sandėlio vietos perdavimo užsakymams* funkcija įjungta.

    - **Reikalaujama strategija:** _Užsakyta_

        Šiame lauke galimos vertės:

        - **Užsakyta** – Pardavimo užsakyme visas užsakytas kiekis turi būti laikomas paklausa.
        - **Rezervuota** – Rezervuoti (faktiniai ir užsakyti) pardavimo užsakymo eilutės kiekiai yra laikomi paklausa.
        - **Paleisti** – Paleistas kiekis turi būti nulemtas paklausos.

    - **Sandėlis:** _61_
    - **Leisti bangai reikalauti naudoti nerezervuotus kiekius:** _Taip_

Taip pat galite nurodyti užklausą, kuri susiaurina vertinamą paklausą.

#### <a name="set-up-slotting-specifications-for-each-template"></a>Intervalo specifikacijų kiekvienam darbo šablonui nustatymas

Kiekvienam pardavimo užsakymo šablonui, kurį sukūrėte, atlikite šiuos žingsnius tam, kad įtrauktumėte eilutę kiekvienai vietos specifikacijai.

1. Norėdami sukurti naują šablono eilutę, „FastTab” skirtuke **Nauja** pasirinkite **Išsami intervalo šablono informacija**.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Seka:** _1_
    - **Aprašymas:** _Fiksuota vieta_
    - **Mažiausias kiekis:** _1_

        Šis laukas nurodo minimalų paklausos kiekį, kurio reikia eilutei.

    - **Maksimalus kiekis:** _1000000_

        Šis laukas nurodo maksimalų paklausos kiekį, kuris galioja eilutei.

    - **Vienetas:** lauką palikite tuščią.

        Šiame lauke apibrėžiamas matavimo vienetas, kurį nurodo minimalus ir maksimalus kiekis.

    - **Matavimo vieneto pakopa:** _EaBoxPl_

        Šis laukas nurodo paklausos matavimo vienetus, kurie galioja eilutei. (Norėdami gauti daugiau informacijos, žr. šios temos skyrių [Matavimo vienetų pakopos intervalui](#unit-tiers).)

    - **Priskirti intervalo kriterijus:** _Atsižvelgti į kiekį_

        Šiame lauke galimos vertės:

        - **Tarkime, kad tuščia** – Šioje sistemoje daroma prielaida, kad visos vietos iš paėmimo srities, yra tuščios ir nereiktų patikrinti šių vietų dėl atsargų.
        - **Atsižvelgti į kiekį** – Ši sistema patikrina visas vietas iš paėmimo srities dėl atsargų, ir turėtų praleisti visas vietas, kurios nėra tuščios.
        - **Apgalvota turimas** – Sistema turi tikrinti, ar bet kuri paskirties vieta turi neužrezervuotą kiekį vienetui pagal paklausos eilutę. Jei kiekis yra pakankamai didelis, kad atitiktų mažiausiai viena paklausos eilutės vienetą, sukurtas vietų plano įrašas yra sumažinamas esamu kiekiu. Pavyzdžiui, jei paklausa yra 10 atvejų ir vienas yra turimas, nustatyta paklausa bus devyni atvejai. Jei paklausa yra 10 atvejų ir vienas yra turimas, nustatyta paklausa bus 10 atvejų. Ši vertė yra prieinama tik, jei *Sandėlio vietų priskyrimo papildymų* funkcija įjungta.

    - **Nurodymo kodas:** _Intervalas_

        Šiame lauke apibrėžiama vietos nurodymas, kuri naudojamas papildymo darbo paėmimų vietai rasti.

    - **Perpildos vieta:** palikite šį lauką tuščią.

        Šis laukas nurodo vietą, į kurią yra įtrauktas atsargų kiekis, jei vietos negalima rasti, kai eilutė yra apdorojama.

    - **Leisti** _taip_

        Jei ši parinktis nustatyta kaip *Taip*, jei bet koks reikalavimas negali būti įvykdytas, perkėlimo darbas bus sukurtas, kad būtų galima paimti atsargas iš vietų, kuriose yra atsargų, tačiau kur niekas nebuvo paimta. Tada šablonas paleidžiamas iš naujo. Šiuo metu nepaisoma vietų atsargų. Ši funkcija veikia geriausiai, kai laukas **Priskirti intervalo kriterijų** nustatomas į _Atsižvelgti į kiekį_.

    - **Fiksuotos vietos naudojimas:** _Galima naudoti tik fiksuotas produkto vietas_

        Šiame lauke galimos vertės:

        - **Fiksuotos ir nefiksuotos vietos** – Sistema neapribojama naudoti tik fiksuotas vietas.
        - **Tik fiksuotos produkto vietos** – Sistema veikia tik tose vietose, kurios yra fiksuotos produkto vietos.
        - **Tik fiksuotos produkto varianto vietos** – Sistema veikia tik tose vietose, kurios yra fiksuotos produkto varianto vietos.

> [!NOTE]
> Jei vietos šablonas turi mažiausiai vieną eilutę, kurioje **Priskyrimo vietos kriterijaus** laukelis nustatytas į *Laikomas turimu*, leidimai nebėra leidžiami jokiai eilutei šablone.

1. Pasirinkite **Įrašyti**.
1. Pasirinkite **Naujas**, kad sukurtumėte antrą šablono eilutę.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Seka:** _2_
    - **Aprašymas:** _Kita_
    - **Minimalus kiekis:** _1_
    - **Maksimalus kiekis:** _1000000_
    - **Vienetas:** lauką palikite tuščią.
    - **Matavimo vieneto pakopa:** _EaBoxPl_
    - **Priskirti intervalo kriterijus:** _Atsižvelgti į kiekį_
    - **Nurodymo kodas:** _Intervalas_
    - **Perpildos vieta:** palikite šį lauką tuščią.
    - **Leisti** _taip_
    - **Fiksuotos vietos naudojimas:** _Fiksuotos ir nefiksuotos vietos_

    Antrojoje eilutėje,dabar bus nurodyti kriterijai, naudojami nustatyti, kokiose vietose gali būti padarytos tos eilutės paklausa.

1. Pasirinktie eilutę, kurios **Seka** yra nustatyta į *2*.
1. Pasirinkite **Redaguoti užklausą**.
1. Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Lentelė:** *Vietos*
    - **Išvestinė lentelė:** *Vietos*
    - **Laukas:** *Vietos profilio ID*
    - **Kriterijai:** lauke *Pick-06* (pasirinkite dvigubą pliuso ženklą \[**++**\], kad išplėstumėte sąrašą, tada pasirinkite *Pick-06* - *Paėmimo vieta 6*.)

1. Pasirinkite **Gerai**.

#### <a name="set-up-location-directives"></a>Nustatyti vietos nurodymus

Reikia nustatyti bent vieną vietos nurodymą, kad būtų palaikomi intervalo paėmimai. Naudokite šiame skyriuje nurodytas procedūras, kad nustatytumėte naują *papildymo vietos nurodymą*, skirtą paėmimams.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Vietų nurodymai**.
1. Kairinės srities lauke **Darbo užsakymo tipas** pasirinkite *Papildymas*.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujo vietos nurodymo antraštės lauke **Pavadinimas**, įveskite *61 intervalo paėmimas*.
1. Laukelyje **Sekos numeris** priimkite nustatytąją vertę.

##### <a name="configure-the-location-directives-fasttab"></a>Konfigūruokite vietų nurodymus „FastTab“ skirtuke

1. „FastTab“ skirtuke **Vietų nurodymai** nustatykite šias reikšmes: Priimkite numatytąsias vertes visuose kituose laukuose.

    - **Darbo tipas:** _Paėmimas_
    - **Vieta:** _6_
    - **Sandėlis:** _61_
    - **Nurodymo kodas:** _Intervalas_

1. Pasirinkite **Įrašyti,** kad būtų galima naudoti **Eilutės** „FastTab“ skirtuką.

##### <a name="configure-the-lines-fasttab"></a>Konfigūruoti „FastTab“ skirtuką Eilutės

1. „FastTab“ skirtuke **Eilutės** spustelėję **Nauja** sukursite naują eilutę.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Pradinis kiekis:** _0_
    - **Galutinis kiekis:** _1000000_

1. Priimkite nustatytąsias vertes likusiems laukeliams.
1. Pasirinkite **Įrašyti,** kad būtų galima naudoti **Vietos nurodymų veiksmų** „FastTab“ skirtuką.

##### <a name="configure-the-location-directive-actions-fasttab"></a>Konfigūruokite vietų nurodymų veiksmus „FastTab“ skirtuke

1. „FastTab“ skirtuke **Vietos nurodymo veiksmai** pasirinkite **Nauja** eilutės sukūrimui.
1. Naujoje eilutėje nustatykite šias reikšmes: Priimkite numatytąsias vertes visuose kituose laukuose.

    - **Sekos numeris:** Priimkite numatytąją vertę.
    - **Pavadinimas:** _Bulk_
    - **Strategija:** _Nėra_

1. Priimkite nustatytąsias vertes likusiems laukeliams.
1. Pasirinkite **Įrašyti**, kad būtų galima naudoti mygtuką **Redaguoti užklausą**.

##### <a name="edit-the-query"></a>Redaguoti užklausą

1. „FastTab“ **Vietos nurodymų veiksmai** pasirinkite **Redaguoti užklausą**.
1. Skirtuke **Diapazonas** pasirinkite **Pridėti**, kad įtrauktumėte naują eilutę į tinklelį.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **Lentelė:** *Vietos*
    - **Išvestinė lentelė:** *Vietos*
    - **Laukas:** *Zonos ID*
    - **Kriterijai:** *Bulk* (pasirinkite dvigubą pliuso ženklą \[**++**\] , kad išplėstumėte sąrašą, tada pasirinkite *Bulk*.)

1. Pasirinkite **Gerai**.

## <a name="scenario"></a>Scenarijus

### <a name="set-up-the-scenario"></a>Scenarijaus nustatymas

Šiame scenarijuje naudokite įtaisytuosius pavyzdžio duomenis ir kurkite šiame skyriuje aprašytus įrašus.

#### <a name="use-the-usmf-sample-data"></a>Naudoti USMF pavyzdinius duomenis

Norėdami dirbti pagal šį scenarijų, naudojant nurodytus įrašų ir reikšmių pavyzdžius, standartiniai [demonstraciniai duomenys](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) turi būti įdiegti Jūsų sistemoje. Be to, turite pasirinkti **USMF** juridinį asmenį prieš pradedant.

#### <a name="create-demand"></a>Kurti paklausą

Atlikite šiuos veiksmus, kad sukurtumėte paklausą, kuriai taikysite intervalą.

1. Pasirinkite **Pardavimas ir rinkodara \> Pardavimo užsakymai \> Visi pardavimo užsakymai**.
1. Pasirinkite **Naujas**, kad sukurtumėte pardavimo užsakymą.
1. Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite _US-007_.
1. Lauke **Sandėlis** pasirinkite _61_.
1. Pasirinkite **Gerai**.
1. Naujas pardavimo užsakymas yra atidarytas. Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekė:** _L0101_
    - **Kiekis:** _20_

1. Pasirinkite **Įtraukti eilutę** naujai eilutei įtraukti ir nustatykite šias reikšmes:

    - **Prekė:** _T0100_
    - **Kiekis:** _8_

1. Pasirinkite **Įrašyti**.
1. Pasirinkite **Naujas**, kad antrą pardavimo užsakymą.
1. Dialogo lango **Kurti pardavimo užsakymą** lauke **Kliento sąskaita** pasirinkite _US-008_.
1. Lauke **Sandėlis** pasirinkite _61_.
1. Naujas pardavimo užsakymas yra atidarytas. Jis apima naują tuščią eilutę **Pardavimo užsakymo eilučių** „FastTab“. Šioje eilutėje nustatykite šias reikšmes:

    - **Prekė:** _T0100_
    - **Kiekis:** _1_

1. Pasirinkite **Įrašyti**.

### <a name="walk-through-a-typical-slotting-scenario"></a>Naudokite įprastą intervalo scenarijų

Po to, kai yra visi būtini elementai, kaip aprašyta ankstesniame skyriuje, jūs esate pasirengę išbandyti šią funkciją dirbdami per kiekvieną šiame skyriuje esantį pratimą.

#### <a name="generate-demand"></a>Generuoti paklausą

1. Eikite į **Sandėlio valdymas \>Sąranka \> Papildymas \> Intervalo šablonai** ir pasirinkite norimą naudoti intervalo šabloną.
1. Veiksmų srityje spustelėkite **Generuoti paklausą**. Ši komanda įvertina visas paklausas, kurios yra sistemoje ir kurios atitinka intervalo šablono užklausą. Bendra visų užsakymų paklausa yra konsoliduojama po vieną kiekvieno kiekio/matavimo vieneto eilutę. Kai procesas baigiamas, atsiranda informacinis pranešimas.

#### <a name="slotting-demand"></a>Intervalo paklausa

Dėl to, kad yra intervalo šablono nustatymu, *Intervalo paklausa* parodo paklausos generavimo rezultatus.

- Veiksmų srityje pasirinkite **Intervalo paklausa** norėdami peržiūrėti rezultatus iš komandos **Generuoti paklausą**. Intervalo paklausos eilutės gali būti redaguojamas. Galite panaikinti eilutę, pridėti naują eilutę arba redaguoti eilutės informaciją.

> [!NOTE]
> Galite redaguoti paklausą neautomatiniu būdu arba galite ją importuoti iš išorinės sistemos naudodami duomenų valdymą. Neatsižvelgiant į tai, iš kur intervalo paklausa yra, ji bus naudojamas atliekant tolesnį veiksmą.

#### <a name="locate-demand"></a>Surasti paklausą

Kai paklausa sugeneruojama, turite naudoti komandą **Surasti paklausą,** kad būtų sugeneruotas *Intervalo planas*.

- Veiksmų srityje spustelėkite **Surasti paklausą**. Paleidžiamas intervalo procesas. Kai procesas baigiamas, atsiranda informacinis pranešimas.

#### <a name="slotting-plan"></a>Intervalo planas

Intervalo planas nurodo vietą, kurioje buvo priskirta kiekviena prekė/kiekis, buvo panaudota perpilda, buvo sukurtas padėjimo darbas ar naudota šablono eilutė. *Bet kokia paklausa, kurios negalima įvykdyti yra paryškintas raudonai.*

- Veiksmų srityje pasirinkite **Intervalo planas,** norėdami peržiūrėti rezultatus.

> [!NOTE]
> - **Sukurta paklausa**, **Nustatyti paklausą** ir **Vykdyti papildymą** procesai yra dabar vykdomi smėlio dėžėje. (Šie procesai yra prieinami iš veiksmų juostos **Vietų šablono** puslapyje.)
> - **Sukurta paklausa**, **Nustatyta paklausą** ir **Vykdyti papildymą** procesai turi užraktą siekiant užtikrinti, kad jie nebus paleisti vienu metu. Kitu atveju, naudojami duomenys gali būti panaikinti.
> - **Sukurta paklausa** ir **Nustatyta paklausai** procesai rodo įspėjimą, jei vykdymas nesukūrė įrašų arba jei įrašuose trūksta informacijos.
> - Jums pasirinkus **Vietų planas**, puslapis neturi **Naujas**, **Redaguoti** ar **Panaikinti** mygtukus veiksmų juostoje, nes duomenų šaltinio redaguoti nepavyksta.
> - Jums pasirinkus **Vykdyti papildymą**, sistema įjungia pasirinktą vietos šabloną ir procesus.

#### <a name="create-replenishment"></a>Sukurkite papildymą

Sukūrę planą, turite sukurti *Papildymo darbą*, pagrįstą planu.

- Veiksmų srityje pasirinkite **Vykdyti papildymą**. Kai procesas baigiamas, atsiranda informacinis pranešimas. Šis pranešimas nurodo antraščių, sukurtų darbo kūrimo ID, skaičių.

Vietos nurodymai, kurie bus naudojami, yra identifikuojami pagal nurodymo kodą, pateiktą kiekvienoje šablono eilutėje.

## <a name="tips"></a>Patarimai

### <a name="set-up-automatic-slotting"></a>Intervalo šablonų nustatymas

Po to, kai visi reikiami elementai yra, galite nustatyti automatinį valdymą, atlikdami šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Papildymas \> Atlikti intervalą**.
1. Nurodykite paleidžiančius veiksmus. Pasirinkite vieną ar daugiau iš šių intervalo veiksmų:

    - Generuoti paklausą
    - Surasti paklausą
    - Kurti papildymo darbą

    > [!NOTE]
    > Intervalo veiksmai yra progresyvūs. Jei norite pasirinkti *Surasti paklausą*, pirmiausia turite pasirinkti *Generuoti paklausą*.

1. Nurodyti naudotiną šabloną.
1. Jei norėsite, pakartojimas paleidžiamas automatiškai.

Norėdami atlikti scenarijų pratimus, **ne** nustatykite automatinio intervalo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]