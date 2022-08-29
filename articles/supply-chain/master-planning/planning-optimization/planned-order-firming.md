---
title: Galutinai suplanuoti užsakymai
description: Šiame straipsnyje paaiškinama, kaip patvirtinti suplanuotus užsakymus. Kai patvirtinami suplanuoti užsakymai, jie tampa faktiniais pirkimo užsakymais, perkėlimo užsakymais arba gamybos užsakymais.
author: t-benebo
ms.date: 08/09/2022
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7c8d5b7992c7955b9c5b1c7e773fdd467ccba6f9
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335352"
---
# <a name="firm-planned-orders"></a>Galutinai suplanuoti užsakymai

[!include [banner](../../includes/banner.md)]

Suplanuoti užsakymai *turi būti patvirtinti* (t. y. patvirtinti) kaip bendrojo planavimo proceso dalis. Kai patvirtinami suplanuoti užsakymai, jie tampa faktiniais pirkimo užsakymais, perkėlimo užsakymais arba gamybos užsakymais. Šie užsakymai taip pat vadinami *pateiktais* arba *atvirais užsakymais*.

Yra trys suplanuotų užsakymų virtimo metodai:

- **Neautomatinis** virtimas – sąraše pasirinkite konkrečius suplanuotus užsakymus ir pradėkite procesą rankiniu būdu.
- **Automatinis tvirtinimas – nurodykite numatytąją padengimo grupių, atskirų prekių ir prekių bei bendrojo planų** derinio tvirtinimo laiko ribas. Tada, vykdant bendrąjį planavimą, suplanuoti užsakymai bus automatiškai patvirtinti, jei užsakymo data patenka į nurodytą patvirtinti laiko ribas.
- **Patvirtinti užklausą** – apibrėžkite užklausą, kad pagal jų ypatybes pasirinktumėte suplanuotus užsakymus. Galite nustatyti paketinę užduotį, norėdami vykdyti užklausą ir galutinai suderinti užsakymus pagal reguliarų grafiką.

Šiame straipsnyje išsamiai aprašomas kiekvienas metodas.

## <a name="enable-the-features-that-are-described-in-this-article"></a><a name="enable-features"></a> Įgalinkite šiame straipsnyje aprašytas funkcijas

Dauguma suplanuoto užsakymo funkcijų yra galimos visuose standartiniuose „Microsoft Dynamics 365 Supply Chain Management“ diegimuose, naudojant „Planning Optimization“. Tačiau kai kurios šiame straipsnyje aprašomos funkcijos turi būti įjungtas funkcijų valdymas prieš naudojant jas.

### <a name="turn-parallelized-firming-of-planned-orders-on-or-off"></a>Įjungti arba išjungti suplanuotų užsakymų lygiagretųjį tvirtavimą

Lygiagretus tvirtinimo procesas padeda pagreitinti tvirtinimo procesą, lygiagrečiai jį keliose gijose. Šis būdas gali būti naudingas, kai daugelis suplanuotų užsakymų yra patvirtinti. Norint naudotis šia funkcija, jūsų sistemai *turi būti* įjungta lygiagretaus suplanuotų užsakymų tvirtinimo funkcija. 

Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymas 10.0.25 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.25 versiją, [...](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)*šią funkciją galite įjungti arba išjungti nueidami į Funkcijų valdymą ir ieškodami lygiagrečio suplanuotų užsakymų tvirtinimo* funkcijos.

### <a name="turn-planned-order-firming-with-filtering-on-or-off"></a>Įjungti arba išjungti suplanuoto užsakymo tvirtinimas filtruojant

Suplanuotų užsakymų virtimas naudojant filtravimą leidžia nurodyti loginius kriterijus, pagal kuriuos galima pasirinkti, kuriuos suplanuotus užsakymus patvirtinti. Taip pat galite peržiūrėti, kurie suplanuoti užsakymai buvo pasirinkti, vykdyti procesą fone ir / arba suplanuoti jį kaip paketinę užduotį.

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.25, funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima. Jei jūsų versija senesnė nei 10.0.29, tada *·*[administratoriai](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gali įjungti arba išjungti šią funkciją ieškodami suplanuoto užsakymo tvirtinto su filtravimo priemone funkcijų valdymo darbo srityje.

### <a name="turn-auto-firming-for-planning-optimization-on-or-off"></a>Įjungti arba išjungti planavimo optimizavimo automatinį tvirtinimas

Automatinis patvirtinimas leidžia patvirtinti (tai yra, išleisti) suplanuotus užsakymus kaip bendrojo planavimo dalį per laiko tvorą pasirašymui. Automatinis virtimas visada palaikomas planavimo variklis, sukurtas „Supply Chain Management“. Tačiau norėdami naudoti ją ir „Planning Optimization“, turite įjungti funkciją.

Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Kaip ir tiekimo grandinės valdymo 10.0.29 ši funkcija yra privaloma ir jos išjungti negalima. Jei naudojate senesnę nei 10.0.29 versiją, [...](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)*šią* funkciją galite įjungti arba išjungti nueidami į funkcijų valdymą ir ieškodami automatinio planavimo optimizavimo funkcijos automatinio tvirtinimo.

## <a name="manually-firm-planned-orders"></a>Peržiūrėti suplanuotus užsakymus rankiniu būdu

Norėdami neautomatiniu būdu patvirtinti suplanuotus užsakymus, surandate ir pasirenkate suplanuotus užsakymus, kuriuos norite patvirtinti, ir tada neautomatiniu būdu pradėkite virtinimo procesą.

1. [Atidarykite bet kurį suplanuotų užsakymų sąrašo](approved-planned-order.md#view-planned-orders) puslapį.
1. Norėdami filtruoti ir rūšiuoti sąrašą, kad būtų galima rasti ieškomus suplanuotus užsakymus, naudokite lauką Filtras, Planuoti **lauką** ir **stulpelio** antraštę.
1. Pasirinkite kiekvieno suplanuoto užsakymo, kurį norite įtraukti, žymės langelį. Jei norite patvirtinti visus šiuo metu puslapyje išvardytus suplanuotus užsakymus (remiantis taikomais filtrais), praleiskite šį veiksmą.
1. Veiksmų srityje pasirinkite vieną iš šių mygtukų:

    - **Patvirtinti** – patvirtinti tik pasirinktus suplanuotus užsakymus.
    - **Patvirtinti viską – patvirtinti visus šiuo metu puslapyje išvardytus suplanuotus užsakymus (remiantis jūsų taikomais filtrais), nepaisant visų pasirinktų** žymės langelių. Ši pasirinktis gali būti naudinga, jei jūs norite patvirtinti daug suplanuotų užsakymų.

1. Dialogo lange **Tvirtinimas** „FastTab“ skirtuke **Parametrai** nustatykite šiuos laukelius. (Daugelis šių laukų reikšmes priima iš formos **Standartinis atnaujinimo** skirtukas bendrojo **planavimo parametrų** puslapyje.)

    - **Naujinti žymėjimą** – Pasirinkti tvirtinant patvirtintus užsakymus naudojamą atsargų žymėjimo strategiją.
    - **Stabdyti virtimą, jei įvyksta klaida – nustatykite šią pasirinktį kaip Taip, norėdami sustabdyti visų pasirinktų suplanuotų užsakymų tvirtavimą, jei** viename iš jų įvyksta *klaida*. Ši pasirinktis turi būti nustatyta kaip *Ne*, **jei lygiagretinimo** tvirtinimo parinktis nustatyta kaip *Taip*.
    - **Patvirtinti lygiagrečiai** – [*·*](#enable-features) ši pasirinktis galima tik jei jūsų sistemai įjungta lygiagreti suplanuotų užsakymų tvirtinimo funkcija ir jei pasirinkote du ar daugiau suplanuotų užsakymų patvirtinti. Norėdami lygiagrečiai *vykdyti* tvirtinimo procesus, nustatykite jį Taip. Lygiagretus virtimas gali padėti pagerinti našumą.
    - **Gijų skaičius –**[*ši* parinktis](#enable-features) galima tik jei jūsų sistemai įjungta funkcija Lygiagretus suplanuotų užsakymų virtimas ir **jei** nustatote parinktį Lygiagrečiai patvirtinti kaip *Taip.* Įveskite gijų skaičių, naudoti naudingą tvirtinimo procesui paralelizuoti. Informacijos, kaip naudoti šią pasirinktį bendrojo planavimo metu, ieškokite [Bendrojo planavimo našumo](../master-planning-performance.md#number-of-threads) patobulinime.

        > [!NOTE]
        > Vertės **Gijų skaičius** nustatymas *0* (nulis) padidina bendrojo pagrindinio planavimo vykdymo laiką. Todėl rekomenduojame visuomet nustatyti reikšmę, kuri yra daugiau nei 0.

    - **Grupuoti pagal tiekėją – nustatykite šią pasirinktį kaip Taip, jei norite, kad tvirtintumėte** *sugrupuotumėte* suplanuotus pirkimo užsakymus ir sukurtumėte po vieną tiekėjo pirkimo užsakymą. Kitu atveju galite sukurti naują pirkimo užsakymą su viena eilute, skirta kiekvienam suplanuotam užsakymui.
    - **Grupuoti pagal pirkėjo grupę** – Pažymėkite šią parinktį į *Taip* kad būtų sudaryta suplanuotų prikimo užsakymų grupė, naudojama vienam pirkimo užsakymui su bendra tiekėjų ir pirkėjų grupe kurti. Jei norite naudoti šią pasirinktį, taip pat turite pažymėti parinktį **Grupuoti pagal tiekėją** į *Taip*.
    - **Grupuoti pagal pirkimo sutartį** – Nustatykite šią pasirinktį į *Taip*, jei norite sugrupuoti suplanuotus pirkimo užsakymus, kurių tiekėjas yra toks pats, kaip ir esamų pirkimo sutarčių, ir sukurti po vieną pirkimo užsakymą kiekvienai pirkimo sutarčiai. Ši parinktis įgalinama automatiškai, kai įgalinta **Grupuoti pagal tiekėją**. Tam, kad galėtumėte naudoti **Grupuoti pagal pirkimo sutartį**, **Rasti pirkimo sutartį** turi būti nustatyta į *Taip* puslapyje **Bendrojo planavimo parametrai**.
    - **Grupuoti pagal laikotarpį** (skyriuje **Pirkimo** užsakymai) – pasirinkite laikotarpį, pagal kurį norite grupuoti suplanuotus pirkimo užsakymus. Jei norite naudoti šią pasirinktį, taip pat turite pažymėti parinktį **Grupuoti pagal tiekėją**.
    - **Grupuoti pagal laikotarpį** (skyriuje **Perlaidos** užsakymai) – pasirinkite laikotarpį, pagal kurį norite grupuoti suplanuotus pirkimo užsakymus. Užsakymai bus sugrupuoti pagal vertes Iš **sandėlio** ir Į **sandėlį**.

    > [!NOTE]
    > Dėl kiekvienos pasirinktys Grupuoti pagal sistema kiekvieną suplanuotą užsakymą konvertuoja į vieno pirkimo užsakymo eilutę, kuri atsiranda grupuojant.

    ![„FastTab“ tvirtinimo laukelio parametrai.](./media/manual-firming.png "„FastTab“ tvirtinimo laukelio parametrai")

1. Dalyje **Vykdyti fone** „FastTab" nustatykite užduotį, kad ji būtų vykdoma paketiniu režimu ir (ar) nustatyti esamą grafiką. Tačiau, tai nėra svarbu nustatyti pasikartojantį planą, kai tai darote neautomatinį tvirtinį. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams. Tačiau neautomatinis virtimas paketinė užduotis apdoros tik šiuo metu pasirinktus suplanuotus užsakymus. Jis nebus apdoros jokių užsakymų, kurie atitiktų filtrus, kurie šiuo metu taikomi puslapyje.
1. Pasirinkite **Gerai** tam, kad pritaikytumėte ir kurtumėte patvirtintus užsakymus.

## <a name="auto-firm-planned-orders"></a>Automatiškai patvirtinti suplanuoti užsakymai

Automatinis patvirtinimas leidžia patvirtinti (tai yra, išleisti) suplanuotus užsakymus kaip bendrojo planavimo dalį. Automatinis tvirtinimas – nurodykite numatytąją padengimo grupių, atskirų prekių ir prekių bei bendrojo planų derinio tvirtinimo laiko ribas. Tada, vykdant bendrąjį planavimą, suplanuoti užsakymai bus automatiškai patvirtinti, jei užsakymo data patenka į nurodytą patvirtinti laiko ribas. Suplanuoti užsakymai, sugeneruoti „Planning Optimization“ ir įtaisytos bendrojo planavimo operacijos, tvarko užsakymo datą (t. y. pradžios datą) kitaip.

> [!NOTE]
> Automatinis suplanuoto pirkimo užsakymų prekėms patvirtinimas vykdomas tik jei prekė yra susieta su tiekėju.
> 
> Patvirtinti išvestiniai užsakymai (subrangos pirkimo užsakymai) rodys būseną *Peržiūrima*, kai įgalintas atvejų keitimų sekimas.

> [!IMPORTANT]
> Prieš naudojant šiame skyriuje aprašytas funkciją naudojant planavimo optimizavimą, [*·*](#enable-features) jūsų sistemai turi būti įjungtas automatinis planavimo optimizavimo funkcijos tvirtinimas, kaip aprašyta šio straipsnio pradžioje. Automatinį tvirtinimas visada galima naudoti su įtaisytuoju bendrojo planavimo moduliu.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automatinis virtimas „Planning Optimization“ ir įtaisytuoju planavimo moduliu

Tiek „Planning Optimization“, tiek planavimo mechanizmą, kuris įdiegtas „Microsoft “, galima naudoti norint automatiškai patvirtinti planavimo užsakymus. Tačiau yra keletas svarbių skirtumų. Pavyzdžiui, jei „Planning Optimization“ naudoja užsakymo datą (tai yra, pradžios datą), kad nustatytų, kuriuos suplanuotus užsakymus patvirtinti, įdiegtas „Supply Chain Management“ mechanizmas naudoja poreikio datą (tai yra, pabaigos datą). Šioje lentelėje apibendrinami skirtumai.

| Funkcija | Planavimo optimizavimas | Įtaisytasis planavimo modulis |
|---|---|---|
| **Pagrindinė data** | Automatinis patvirtinimas pagrįstas užsakymo data (pradžios data). | Automatinis patvirtinimas pagrįstas poreikio data (pabaigos data). |
| **Gamybos laikas** | Kadangi užsakymo data (pradžios data) suaktyvina patvirtinimą, nebūtina atsižvelgti į gamybos laiką kaip patvirtinimo laiko ribos dalį. | Siekiant užtikrinti, kad užsakymai būtų patvirtinti laiku, patvirtinimo laiko riba turi būti ilgesnė už gamybos laiką. |
| **Šios savaitės užsakymai** | Jei norite patvirtinti visus užsakymus, kurie turi prasidėti šią savaitę, patvirtinimo laiko riba turi būti viena savaitė. | Jei norite patvirtinti visus užsakymus, kurie turi prasidėti šią savaitę, patvirtinimo laiko riba turi būti gamybos laikas ir viena savaitė. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Nustatyti automatinio tvirtinimo ir tvirtinto laiko ribas

Automatinį tvirtinimas įjungiamas priskiriant automatinio patvirtinimo laiko ribas atitinkamiems padengimo nustatymams, kaip toliau aprašyta šiame skyriuje. Jei automatinis virtimas neįjungtas jokioms padengimo nustatymams ar jei planavimas pradedamas konkrečiame puslapyje, pvz., išleisto produkto grynojo reikalavimų puslapyje, automatinio užbaigimo procesas **praleidžiamas**.

Automatinio nustatymo grupavimo ir žymėjimo pasirinktys turi savo vertes iš skirtuko **Standartinis** atnaujinimas, bendrojo **planavimo parametrų** puslapyje.

Automatinio tvirtinimo laiko ribas apibrėžia dienų, kurias įvedate tam tikrai padengimo sąrankai, skaičius. Galite įjungti automatinio patvirtinimo laiko ribą toliau nurodytais būdais.

- Norėdami nustatyti numatytąją patvirtinimo laiko ribą padengimo grupei, eikite į **Pagrindinis planavimas \> Sąranka \> Padengimas \> Padengimo grupės**, ir pasirinkite padengimo grupę. Tada „FastTab“ **Kita** lauke **Automatinio patvirtinimo laiko riba (dienos)** įveskite dienų skaičių.
- Norėdami perrašyti konkrečios prekės padengimo grupei nustatytas tvirtinto laiko ribas, eikite į Produkto informacijos **valdymas \> patvirtinti** produktai. Veiksmų juostoje pasirinkite **Planavimas**, tada pasirinkite **Prekių padengimas**. Tada skirtuke **Bendroji informacija** pasirinkite **Perrašyti laiko ribą** ir lauke **Automatinio patvirtinimo laiko riba (dienos)** įveskite dienų skaičių.
- Jei norite perrašyti patvirtinimo laiko ribą, nustatytą padengimo grupei ir konkretaus bendrojo plano prekės padengimui, eikite į  **Bendrasis planavimas \> Sąranka \> Bendrieji planai**, ir pasirinkite bendrąjį planą. Tada **Laiko tvoros dienomis** „FastTab“, nustatytas **Patvirtinimas** į *Taip* ir įveskite dienų skaičių.

Jei visas anksčiau paminėtas laiko ribas nustatote kaip 0 (nulį), automatiškai išjungiamas atitinkamų *padengtų* prekių automatinis tvirtinimas.

## <a name="firm-planned-orders-by-using-a-query"></a>Patvirtinti suplanuotus užsakymus naudojant užklausą

Užklausomis pagrįstas virtimas leidžia planuoti tvirtvirtį pagal iš anksto nustatytus kriterijus. Skirtingai nei automatinis tvirtinimas, užklausomis pagrįstas tvirtinimas leidžia automatiškai patvirtinti skirtingus užsakymų pogrupius skirtingu metu. Be to, galite naudoti neautomat operacijas arba automatizuotas operacijas, norėdami patvirtinti skirtingus suplanuotų užsakymų tipus. Taip pat galite peržiūrėti, kurie patvirtinti užsakymai pasirinkti pagal jūsų nustatymus. Todėl galite patvirtinti, kad pasirinkimas atitinka jūsų lūkesčius.

Automatinį tvirtinimas galimas derinti su užklausa pagrįstu tvirtintoja. Pvz., užklausose pagrįstame tvirtintoje užduotyje yra laiko riba į priekį, kuri yra ilgesni nei atitinkamos automatinio užbaigimo padengimo konfigūracijos laiko riba. Todėl, užklausose pagrįsta virtimo užduotis apdoros suplanuotus užsakymus prieš suaktyvinant automatinį tvirtavimą. Galite pasinaudoti tokiu veikimo būdu, jei norite planuoti konkrečių tiekėjų užsakymus kitaip nei kitų tiekėjų panašių produktų užsakymus.

> [!IMPORTANT]
> Prieš naudojant šiame skyriuje aprašytas priemones, [*·*](#enable-features) jūsų sistemai turi būti įjungtas suplanuoto užsakymo virtimas naudojant filtravimo priemonę, kaip aprašyta šio straipsnio pradžioje.

Norėdami patvirtinti suplanuotą užsakymą naudodami užklausa pagrįstą tvirtinto procesą, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Vykdyti \> Suplanuoto užsakymo tvirtinimas**.
1. Dialogo lange **Suplanuoto užsakymo** tvirtinimas, **parametrų** „FastTab", nustatykite pagrindines apdorojimo, žymėjimo ir grupavimo pasirinktis. Šios pasirinktys veikia taip pat, kaip ir **dialogo** lange tvirtimas. (Aprašymų žr. ankstesniame skyriuje.) Tada skyriuje **Planas** nustatykite šiuos unikalius laukus, kad jie būtų **unikalūs dialogo lange Suplanuoto užsakymo** tvirtimas:

    - **Planas** – pasirinkite bendrąjį planą, kuris turi būti taikomas tvirtintoje suplanuotus užsakymus, kuriuos rasite šioje užklausoje.
    - **Laiko tvoros dienų persiuntimo tvirtinimas** – Kiekviename plane galite pasirinkti, kaip tolimoje ateityje įvairūs poreikiai ir kiti veiksniai turi būti skaičiuojami bendrojo planavimo metu.
    - **Laiko tvoros dienų siuntimo atgal tvirtinimas** – Kiekviename plane galite pasirinkti, kaip tolimoje ateityje įvairūs poreikiai ir kiti veiksniai turi būti skaičiuojami bendrojo planavimo metu.

    ![„FastTab“ parametrai suplanuoto užsakymo tvirtinimo teksto laukelyje.](./media/planned-order-firming-main-1.png "„FastTab“ tvirtinimo laukelio suplanuoto užsakymo parametrai")

1. Norėdami nurodyti, kurie įrašai turi būti įtraukti į užsakymą, pažymėkite mygtuką Filtras įrašuose, **kuriuos** norite **įtraukti** „FastTab". Atsiranda standartinis užklausos dialogo langas, kuriame galite nurodyti pasirinkimo kriterijus, rūšiavimo kriterijus ir jungtis. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ fono užduočių tipams. Laukų informaciją galima tik skaityti ir vertes, susijusias su jūsų užklausa.

    ![Įrašai, įtrauktintys „FastTab" į suplanuoto užsakymo tvirtinto dialogo langą.](./media/planned-order-firming-main-2.png "Įrašai, įtrauktintys „FastTab&quot; į suplanuoto užsakymo tvirtinto dialogo langą")

1. Pasirinkite **Peržiūra**, norėdami peržiūrėti jūsų tvirtinto užsakymo turinį, remiantis iki šiol nustatymais. Suplanuotų užsakymų, kurie bus patvirtinti, sąrašas rodomas kaip pranešimas. Jei reikia, galite koreguoti parametrus, kol peržiūroje bus rodomas reikiamas patvirtinti užsakymas.

    ![Tvirtinto užsakymo peržiūros pavyzdys.](./media/planned-order-firming-preview.png "Tvirtinto užsakymo peržiūros pavyzdys")

    > [!WARNING]
    > Ši priemonė patvirtins visus suplanuotus užsakymus, kurie atitinka filtro kriterijus. Nekritinis suplanuotų užsakymų virtimas gali sukelti nereikalingų pirkimo, perkėlimo ir gamybos užsakymų skaičių. Prieš tęsdami visada naudokite **mygtuką** Peržiūra, norėdami patikrinti įrašus, kurie bus įtraukti.

1. Dalyje **Vykdyti fone** "FastTab" nustatykite užduotį, kad ji būtų vykdoma paketiniu režimu ir (ar) nustatyti esamą grafiką. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams.
1. Pasirinkite **Gerai** tam, kad pritaikytumėte ir kurtumėte patvirtintus užsakymus.

## <a name="track-firmed-orders"></a>Sekti patvirtinti užsakymus

Norėdami sekti suplanuotą užsakymą, kuris buvo patvirtinti, atlikite šiuos veiksmus.

1. [Atidarykite bet kurį suplanuotų užsakymų sąrašo](approved-planned-order.md#view-planned-orders) puslapį.
1. Atidaryti ar pasirinkti suplanuotą užsakymą, kurį norite sekti.
1. Veiksmų juostoje **Rodinys** skirtukas, grupėje **Peržiūrėte**, pasirinkite **Tvirtinimo istorija**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
