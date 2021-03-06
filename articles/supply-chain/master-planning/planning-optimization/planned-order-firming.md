---
title: Galutinai suplanuoti užsakymai
description: Šioje temoje paaiškinama, kaip patvirtinti suplanuotus užsakymus. Kai patvirtinami suplanuoti užsakymai, jie tampa faktiniais pirkimo užsakymais, perkėlimo užsakymais arba gamybos užsakymais.
author: ChristianRytt
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 2df579bfb820f871bfcc9c18bd8e5681cdf42447
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271213"
---
# <a name="firm-planned-orders"></a>Galutinai suplanuoti užsakymai

[!include [banner](../../includes/banner.md)]

Suplanuoti užsakymai *turi būti patvirtinti* (t. y. patvirtinti) kaip bendrojo planavimo proceso dalis. Kai patvirtinami suplanuoti užsakymai, jie tampa faktiniais pirkimo užsakymais, perkėlimo užsakymais arba gamybos užsakymais. Šie užsakymai taip pat vadinami *pateiktais* arba *atvirais užsakymais*.

Yra trys suplanuotų užsakymų virtimo metodai:

- **Neautomatinis** virtimas – sąraše pasirinkite konkrečius suplanuotus užsakymus ir pradėkite procesą rankiniu būdu.
- **Automatinis tvirtinimas – nurodykite numatytąją padengimo grupių, atskirų prekių ir prekių bei bendrojo planų** derinio tvirtinimo laiko ribas. Tada, vykdant bendrąjį planavimą, suplanuoti užsakymai bus automatiškai patvirtinti, jei užsakymo data patenka į nurodytą patvirtinti laiko ribas.
- **Patvirtinti užklausą** – apibrėžkite užklausą, kad pagal jų ypatybes pasirinktumėte suplanuotus užsakymus. Galite nustatyti paketinę užduotį, norėdami vykdyti užklausą ir galutinai suderinti užsakymus pagal reguliarų grafiką.

Šioje temoje išsamiai aprašomas kiekvienas metodas.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Įgalinkite šioje temoje aprašomas funkcijas

Dauguma suplanuoto užsakymo funkcijų yra galimos visuose standartiniuose „Microsoft Dynamics 365 Supply Chain Management“ diegimuose, naudojant „Planning Optimization“. Tačiau kai kurios šioje temoje aprašomos funkcijos turi būti įjungtos funkcijų valdymas prieš jas naudojant.

### <a name="enable-parallelized-firming-of-planned-orders"></a>Įjungti paralelų suplanuotų užsakymų pasirašymą

Lygiagretus tvirtinimo procesas padeda pagreitinti tvirtinimo procesą, lygiagrečiai jį keliose gijose. Šis būdas gali būti naudingas, kai daugelis suplanuotų užsakymų yra patvirtinti.

Norėdami, kad jūsų sistemoje šios funkcijos būtų galimos, eikite į Funkcijų [valdymas ir](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)įjunkite *suplanuotų užsakymų funkcijos lygiagretų* tvirtavimą.

### <a name="enable-planned-order-firming-with-filtering"></a>Įjungti suplanuoto užsakymo tvirtinimo naudojant filtravimą

Suplanuotų užsakymų virtimas naudojant filtravimą leidžia nurodyti loginius kriterijus, pagal kuriuos galima pasirinkti, kuriuos suplanuotus užsakymus patvirtinti. Taip pat galite peržiūrėti, kurie suplanuoti užsakymai buvo pasirinkti, vykdyti procesą fone ir / arba suplanuoti jį kaip paketinę užduotį.

Norėdami, kad jūsų sistemoje šios funkcijos būtų galimos, eikite į Funkcijų [valdymas ir](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)įjunkite *suplanuotų užsakymų funkcijos pasirašymą su filtravimu* tvirtavimą.

### <a name="enable-auto-firming-for-planning-optimization"></a>Įjungti automatinį planavimo optimizavimo patvirtinimą

Automatinis patvirtinimas leidžia patvirtinti (tai yra, išleisti) suplanuotus užsakymus kaip bendrojo planavimo dalį per laiko tvorą pasirašymui. Automatinis virtimas visada palaikomas planavimo variklis, sukurtas „Supply Chain Management“. Tačiau norėdami naudoti ją ir „Planning Optimization“, turite įjungti funkciją.

Norėdami, kad jūsų sistemoje šios funkcijos būtų galimos, eikite į „Planning Optimization“ Funkcijų [valdymas ir](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) įjunkite *suplanuotų užsakymų funkcijos pasirašymą su filtravimu* tvirtavimą.

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
    - **Patvirtinti lygiagrečiai – ši pasirinktis galima tik jei jūsų sistemoje įjungta lygiagretaus suplanuotų užsakymų tvirtinimo funkcija ir jei pasirinkote du ar daugiau suplanuotų** [*užsakymų*](#enable-features) patvirtinti. Norėdami lygiagrečiai *vykdyti* tvirtinimo procesus, nustatykite jį Taip. Lygiagretus virtimas gali padėti pagerinti našumą.
    - **Siūlų skaičius** – Ši parinktis įmanoma tik, jei [*Lygiagretaus suplanuotų užsakymų tvirtinimo* funkcija](#enable-features) įjungta jūsų sistemoje ir pasirinkote **Lygiagretaus tvirtinimo** parinktį *Taip*. Įveskite gijų skaičių, naudoti naudingą tvirtinimo procesui paralelizuoti. Informacijos, kaip naudoti šią pasirinktį bendrojo planavimo metu, ieškokite [Bendrojo planavimo našumo](../master-planning-performance.md#number-of-threads) patobulinime.

        > [!NOTE]
        > Vertės **Gijų skaičius** nustatymas *0* (nulis) padidina bendrojo pagrindinio planavimo vykdymo laiką. Todėl rekomenduojame visuomet nustatyti reikšmę, kuri yra daugiau nei 0.

    - **Grupuoti pagal tiekėją – nustatykite šią pasirinktį kaip Taip, jei norite, kad tvirtintumėte** *sugrupuotumėte* suplanuotus pirkimo užsakymus ir sukurtumėte po vieną tiekėjo pirkimo užsakymą. Kitu atveju galite sukurti naują pirkimo užsakymą su viena eilute, skirta kiekvienam suplanuotam užsakymui.
    - **Grupuoti pagal pirkėjo grupę** – Pažymėkite šią parinktį į *Taip* kad būtų sudaryta suplanuotų prikimo užsakymų grupė, naudojama vienam pirkimo užsakymui su bendra tiekėjų ir pirkėjų grupe kurti. Jei norite naudoti šią pasirinktį, taip pat turite pažymėti parinktį **Grupuoti pagal tiekėją** į *Taip*.
    - **Grupuoti pagal pirkimo sutartį** – Nustatykite šią pasirinktį į *Taip*, jei norite sugrupuoti suplanuotus pirkimo užsakymus, kurių tiekėjas yra toks pats, kaip ir esamų pirkimo sutarčių, ir sukurti po vieną pirkimo užsakymą kiekvienai pirkimo sutarčiai. Ši parinktis įgalinama automatiškai, kai įgalinta **Grupuoti pagal tiekėją**. Tam, kad galėtumėte naudoti **Grupuoti pagal pirkimo sutartį**, **Rasti pirkimo sutartį** turi būti nustatyta į *Taip* puslapyje **Bendrojo planavimo parametrai**.
    - **Grupuoti pagal laikotarpį** (skyriuje **Pirkimo** užsakymai) – pasirinkite laikotarpį, pagal kurį norite grupuoti suplanuotus pirkimo užsakymus. Jei norite naudoti šią pasirinktį, taip pat turite pažymėti parinktį **Grupuoti pagal tiekėją**.
    - **Grupuoti pagal laikotarpį** (skyriuje **Perlaidos** užsakymai) – pasirinkite laikotarpį, pagal kurį norite grupuoti suplanuotus pirkimo užsakymus. Užsakymai bus sugrupuoti pagal vertes Iš **sandėlio** ir Į **sandėlį**.

    ![„FastTab“ tvirtinimo laukelio parametrai](./media/manual-firming.png "„FastTab“ tvirtinimo laukelio parametrai")

1. Dalyje **Vykdyti fone** „FastTab" nustatykite užduotį, kad ji būtų vykdoma paketiniu režimu ir (ar) nustatyti esamą grafiką. Tačiau, tai nėra svarbu nustatyti pasikartojantį planą, kai tai darote neautomatinį tvirtinį. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ [fono](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) užduočių tipams. Tačiau neautomatinis virtimas paketinė užduotis apdoros tik šiuo metu pasirinktus suplanuotus užsakymus. Jis nebus apdoros jokių užsakymų, kurie atitiktų filtrus, kurie šiuo metu taikomi puslapyje.
1. Pasirinkite **Gerai** tam, kad pritaikytumėte ir kurtumėte patvirtintus užsakymus.

## <a name="auto-firm-planned-orders"></a>Automatiškai patvirtinti suplanuoti užsakymai

Automatinis patvirtinimas leidžia patvirtinti (tai yra, išleisti) suplanuotus užsakymus kaip bendrojo planavimo dalį. Automatinis tvirtinimas – nurodykite numatytąją padengimo grupių, atskirų prekių ir prekių bei bendrojo planų derinio tvirtinimo laiko ribas. Tada, vykdant bendrąjį planavimą, suplanuoti užsakymai bus automatiškai patvirtinti, jei užsakymo data patenka į nurodytą patvirtinti laiko ribas. Suplanuoti užsakymai, sugeneruoti „Planning Optimization“ ir įtaisytos bendrojo planavimo operacijos, tvarko užsakymo datą (t. y. pradžios datą) kitaip.

> [!NOTE]
> Automatinis suplanuoto pirkimo užsakymų prekėms patvirtinimas vykdomas tik jei prekė yra susieta su tiekėju.
> 
> Patvirtinti išvestiniai užsakymai (subrangos pirkimo užsakymai) rodys būseną *Peržiūrima*, kai įgalintas atvejų keitimų sekimas.

> [!IMPORTANT]
> Prieš naudojant šiame skyriuje aprašytas funkciją naudojant „Planning Optimization“ jūsų sistemoje turi būti įjungta automatinio planavimo optimizavimo funkcijos patvirtinti, kaip aprašyta šios [*temos*](#enable-features) pradžioje. Automatinį tvirtinimas visada galima naudoti su įtaisytuoju bendrojo planavimo moduliu.

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
> Prieš naudojant šiame skyriuje aprašytas funkciją naudojant „Planning Optimization“ jūsų sistemoje turi būti įjungta automatinio suplanuotos optimizavimo funkcijos su filtravimupatvirtinti, kaip aprašyta šios [*temos*](#enable-features) pradžioje.

Norėdami patvirtinti suplanuotą užsakymą naudodami užklausa pagrįstą tvirtinto procesą, atlikite šiuos veiksmus.

1. Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Vykdyti \> Suplanuoto užsakymo tvirtinimas**.
1. Dialogo lange **Suplanuoto užsakymo** tvirtinimas, **parametrų** „FastTab", nustatykite pagrindines apdorojimo, žymėjimo ir grupavimo pasirinktis. Šios pasirinktys veikia taip pat, kaip ir **dialogo** lange tvirtimas. (Aprašymų žr. ankstesniame skyriuje.) Tada skyriuje **Planas** nustatykite šiuos unikalius laukus, kad jie būtų **unikalūs dialogo lange Suplanuoto užsakymo** tvirtimas:

    - **Planas** – pasirinkite bendrąjį planą, kuris turi būti taikomas tvirtintoje suplanuotus užsakymus, kuriuos rasite šioje užklausoje.
    - **Laiko tvoros dienų persiuntimo tvirtinimas** – Kiekviename plane galite pasirinkti, kaip tolimoje ateityje įvairūs poreikiai ir kiti veiksniai turi būti skaičiuojami bendrojo planavimo metu.
    - **Laiko tvoros dienų siuntimo atgal tvirtinimas** – Kiekviename plane galite pasirinkti, kaip tolimoje ateityje įvairūs poreikiai ir kiti veiksniai turi būti skaičiuojami bendrojo planavimo metu.

    ![„FastTab“ parametrai suplanuoto užsakymo tvirtinimo teksto laukelyje](./media/planned-order-firming-main-1.png "„FastTab“ tvirtinimo laukelio suplanuoto užsakymo parametrai")

1. Norėdami nurodyti, kurie įrašai turi būti įtraukti į užsakymą, pažymėkite mygtuką Filtras įrašuose, **kuriuos** norite **įtraukti** „FastTab". Atsiranda standartinis užklausos dialogo langas, kuriame galite nurodyti pasirinkimo kriterijus, rūšiavimo kriterijus ir jungtis. Šie laukai veikia kaip tik kitiems „Supply Chain Management“ fono užduočių tipams. Laukų informaciją galima tik skaityti ir vertes, susijusias su jūsų užklausa.

    ![Įrašai, įtrauktintys „FastTab" į suplanuoto užsakymo tvirtinto dialogo langą](./media/planned-order-firming-main-2.png "Įrašai, įtrauktintys „FastTab&quot; į suplanuoto užsakymo tvirtinto dialogo langą")

1. Pasirinkite **Peržiūra**, norėdami peržiūrėti jūsų tvirtinto užsakymo turinį, remiantis iki šiol nustatymais. Suplanuotų užsakymų, kurie bus patvirtinti, sąrašas rodomas kaip pranešimas. Jei reikia, galite koreguoti parametrus, kol peržiūroje bus rodomas reikiamas patvirtinti užsakymas.

    ![Tvirtinto užsakymo peržiūros pavyzdys](./media/planned-order-firming-preview.png "Tvirtinto užsakymo peržiūros pavyzdys")

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
