---
title: Bangos kūrimas ir apdorojimas
description: Šioje temoje aprašoma, kaip kurti, apdoroti ir išleisti bangą, norint sukurti krovinio, siuntos, gamybos užsakymo arba „kanban“ užsakymo išrinkimo darbą.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, WHSParameters, whswavetablecreatenew, WHSWaveTable, WHSWaveAttributes, WHSKanbanWaveTable, WHSWaveTableListPage, WHSKanbanWaveTableListPage, WHSProdWaveTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 4bf47b15b668a37f12edb3dbb842d19655fac97a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019032"
---
# <a name="wave-creation-and-processing"></a>Bangos kūrimas ir apdorojimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip kurti, apdoroti ir išleisti bangą, norint sukurti krovinio, siuntos, gamybos užsakymo arba „kanban“ užsakymo išrinkimo darbą. Galite sukurti bangas šiems užsakymų tipams:

- **Pardavimo užsakymams** – naudokite siuntimo bangas, norėdami įtraukti eilučių iš pardavimo užsakymų. Kai pardavimo užsakymas išleidžiamas į sandėlį, pardavimo užsakymo eilutes galima įtraukti į bangą.
- **Gamybos užsakymams** – naudokite gamybos bangas, norėdami įtraukti eilučių iš produkto komplektavimo specifikacijos (KS).
- **„Kanban“ užsakymai** – „kanban“ bangos apima išrinkimo dokumento eilutes iš „kanban“ užsakymų.

Pardavimo užsakymų ir „kanban“ užsakymų atsargos turi būti rezervuotos prie išleidžiant užsakymą į sandėlį. Kitu atveju prekės arba paskirstymo eilutės negali būti apdorojamos bangoje. Tačiau gamybos užsakymai yra šiek tiek lankstesni. Gamybos užsakymams galite pasirinkti vieną iš šių parinkčių:

- Galite reikalauti, kad visos medžiagos būtų rezervuotos prieš užsakymą išleidžiant į sandėlį.
- Galite leisti, kad gamybos užsakymai būtų išleidžiami į sandėlį, net jeigu visos medžiagos negali būti rezervuotos. Jei pasirinksite šią parinktį, turėsite rankiniu būdu kartoti išleidimo į sandėlį procesą, kai taps pasiekiama papildomų medžiagų. Pavyzdžiui, tai naudinga, jei turite medžiagų, kurių reikia, kad galėtumėte pradėti gamybą, ir galite palaukti, kai taps pasiekiamos papildomos medžiagos.

Galite nurodyti,kurią iš šių gamybos užsakymo parinkčių naudoti pagal numatytuosius nustatymus naudodami lauką **Medžiagų rezervavimo poreikis**, esantį **Gamybos kontrolės parametrų** puslapyje. Tačiau, jei reikia, galite pakeisti kiekvieno gamybos užsakymo nustatymą. Daugiau informacijos rasite [Sandėlio parametrai bangos apdorojimui](wave-warehouse-parameters.md).

## <a name="create-and-process-a-wave"></a>Bangos kūrimas ir apdorojimas

Šioje diagramoje parodyta, kaip kuriamos, apdorojamos ir išleidžiamos siuntimo bangos. Skaičiai atitinka tolesnius šios temos skyrius.

![Bangos kūrimo procesas](media/wave-processing-diagram.png "Bangos kūrimo procesas")

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradedant, turi būti pasiekiamas bangos, kurią norite sukurti, tipo (siuntimo, gamybos arba „kanban”) bangos šablonas. Bangos šablonas nustato daug parametrų, kaip banga bus generuojama ir apdorojama, įskaitant tuos veiksmus, kuriuos reikia atlikti rankiniu būdu ir tuos, kurie atliekami automatiškai. Daugiau informacijos rasite [Bangos šablonai](wave-templates.md).

### <a name="create-a-wave"></a>Bangos kūrimas

#### <a name="automatically-create-waves-based-on-warehouse-and-order-type"></a>Automatinis bangų kūrimas pagal sandėlio ir užsakymo tipus

Norėdami automatiškai sukurti bangas, nustatykite [Bangos šablonus](wave-templates.md), taikomus kiekvienam atitinkam užsakymo tipui ir sandėliui. Įsitikinkite, kad kiekvieno šablono **Automatizuoto bangos kūrimo** parinktis nustatyta į *Taip*.

#### <a name="manually-create-waves"></a>Bangos kūrimas rankiniu būdu

Norėdami sukurti bangą rankiniu būdu, atlikite toliau nurodytus veiksmus:

1. Įsitikinkite, kad atitinkami [Bangos šablonai](wave-templates.md) nėra nustatyti automatiškai kurti bangą sandėliui ir užsakymo tipams ten, kur norite kurti rankiniu būdu.
1. Priklausant nuo to, kokio tipo bangą norite sukurti, atlikite vieną šių veiksmų:

    - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Siuntimo bangos** \> **Visos bangos**. Veiksmų srityje pasirinkite **Banga**.
    - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Gamybos bangos** \> **Visos gamybos bangos**. Veiksmų srityje pasirinkite **Gamybos banga**.
    - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **„Kanban” bangos** \> **Visos „kanban” bangos**. Veiksmų srityje pasirinkite **Kurti bangą**.

1. Lauke **Aprašas** įveskite trumpą bangos aprašą. Jame turėtumėte nurodyti, ką apdorojate bangoje.

1. Lauke **Bangos šablono pavadinimas** pasirinkite norimo kurti bangos tipo bangos šabloną. Bangos šablone yra bangos metodų, kurie atliks veiksmus, pavyzdžiui, sukurs bangos darbą. Pavyzdžiui, siuntimo bangos šablone gali būti krovinių kūrimo, eilučių paskirstymo bangoms, papildymo ir bangos išrinkimo darbo kūrimo metodų.

1. Jei norite naudoti bangos atributus kaip papildomus bangos užklausos kriterijus, pasirinkite atributus laukuose **Bangos atributai**.

### <a name="specify-what-to-include-in-a-wave"></a>Nurodymas, ką įtraukti į bangą

Sukūrę bangą, esate pasiruošę į ją įtraukti turinį.

> [!NOTE]
> Jei reikia, eilutes į bangą galite įtraukti net po to, kai ji buvo apdorota, tačiau ji turi būti dar neišleista.

#### <a name="automatically-specify-what-to-include-in-a-wave"></a>Automatinis nurodymas, ką įtraukti į bangą

Norėdami automatiškai sukurti bangas, nustatykite [Bangos šablonus](wave-templates.md), taikomus kiekvienam atitinkam užsakymo tipui ir sandėliui. Įsitikinkite, kad kiekvieno šablono **Automatizuoto bangos kūrimo** parinktis nustatyta į *Taip*. Kitu atveju, jūsų šablonas gali automatiškai priskirti eilutes bet kuriai tinkamumo valdymo atvirai bangai, jei parinktis **Priskirti atviroms bangoms** nustatyta į *Taip*.

#### <a name="manually-specify-what-to-include-in-a-wave"></a>Neautomatinis nurodymas, ką įtraukti į bangą

Kai banga sukurta, tačiau dar neišleista, galite rankiniu būdu nurodyti, ką įtraukti į bangą. Norėdami įtraukti eilutes į bangą rankiniu būdu:

1. Atsižvelgdami į bangos, į kurią norite įtraukti eilučių, tipą, vieną iš šių veiksmų:

    - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Siuntimo bangos** \> **Visos bangos**. Veiksmų srityje pasirinkite **Banga**.
    - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Gamybos bangos** \> **Visos gamybos bangos**. Veiksmų srityje pasirinkite **Gamybos banga**.
    - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **„Kanban” bangos** \> **Visos „kanban” bangos**. Veiksmų srityje pasirinkite **Kurti bangą**.

1. Pasirinkite bangą. Veiksmų srityje pasirinkite vieną iš šių:

      - **Prižiūrėti siuntimus**
      - **Tvarkyti gamybą**
      - **Tvarkyti „kanban“ užduoties išrinkimo dokumentus**

1. Viršutinėje lango dalyje pasirinkite eilutę, kurią norite įtraukti į bangą ir tada pasirinkite **Įtraukti į bangą**. Eilutė perkeliama į „FastTab“ skirtuką **Bangos eilutės**.

    Pakartokite šį veiksmą su kiekviena norima įtraukti eilute. Norėdami įtraukti visas eilutes, pasirinkite **Įtraukti visas**.

    > [!TIP]
    > Jei kuriate siuntos bangas, galite greitai rasti konkretų užsakymą lauke **Bangos filtro kodas** pasirinkdami pasirinktinį filtrą. Bangos filtro koduose yra siuntų užklausų kriterijų, sukurtų formoje **Bangos filtrai**. Šis laukas negalimas gamybos ir „kanban“ bangoms.
    > Žalia varnelė stulpelyje **Bangoje** nurodo, kad siunta įtraukta į bangą.

### <a name="process-the-wave-to-create-the-picking-work"></a>Bangos apdorojimas paėmimo darbo sukūrimui

Kai banga sukurta ir joje yra visos reikiamos eilutės, esate pasiruošę ją apdoroti, kad sukurtumėte atitinkamą paėmimo darbą.

#### <a name="automatically-process-a-wave"></a>Automatinis bangos apdorojimas

Norėdami automatiškai apdoroti bangą, nustatykite atitinkamus [Bangos šablonus](wave-templates.md) su reikiamomis automatinio apdorojimo parinktimis.

#### <a name="manually-process-a-wave"></a>Neautomatinis bangos apdorojimas

Apdoroti bangą galite tik tada, kai **Bangos būsena** yra *Sukurta*. Kai apdorosite bangą, **Bangos būsena** bus pakeista į *Sulaikyta*.

Norėdami rankiniu būdu apdoroti bangą, kuri turi visą reikiamą turinį, atlikite šiuos veiksmus:

1. Atsižvelgdami į norimos apdoroti bangos tipą, atlikite vieną iš šių veiksmų:

    - Pasirinkite **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Siuntimo bangos** \> **Visos bangos**. Veiksmų srityje pasirinkite **Banga**.
    - Pasirinkite **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Gamybos bangos** \> **Visos gamybos bangos**. Veiksmų srityje pasirinkite **Gamybos banga**.
    - Pasirinkite **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **„Kanban” bangos** \> **Visos „kanban” bangos**. Veiksmų srityje pasirinkite **Kurti bangą**.

1. Pasirinkite norimą apdoroti bangą. Veiksmų juostoje pasirinkite **Apdoroti**.

### <a name="release-the-wave-to-the-warehouse-to-start-picking-and-packing"></a>Išleiskite bangą į sandėlį, kad būtų pradėtas išrinkimas ir pakavimas

Norėdami išleisti bangą, prieš tai turite ją apdoroti. Kai išleidžiate bangą, sandėlyje tampa galimas išrinkimo darbas. Išleidę bangą, galite ją atšaukti ir įtraukti daugiau eilučių, tačiau negalite keisti eilučių.

#### <a name="automatically-release-a-wave"></a>Automatinis bangos išleidimas

Norėdami automatiškai apdoroti bangą, nustatykite atitinkamus [Bangos šablonus](wave-templates.md) su reikiamomis automatinio apdorojimo parinktimis.

#### <a name="manually-release-a-wave"></a>Neautomatinis bangos išleidimas

Norėdami išleisti bangą rankiniu būdu, atlikite toliau nurodytus veiksmus:

1. Atsižvelgdami į norimos išleisti bangos tipą, atlikite vieną iš šių veiksmų:

      - Pasirinkite **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Siuntimo bangos** \> **Visos bangos**. Veiksmų srityje pasirinkite **Banga**.
      - Pasirinkite **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Gamybos bangos** \> **Visos gamybos bangos**. Veiksmų srityje pasirinkite **Gamybos banga**.
      - Pasirinkite **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **„Kanban” bangos** \> **Visos „kanban” bangos**. Veiksmų srityje pasirinkite **Kurti bangą**.

1. Pasirinkite norimą išleisti bangą. Veiksmų srityje pasirinkite **Išleisti bangą**.

## <a name="containerize-a-wave"></a>Bangos krovimas į konteinerius

Automatizuotas krovimas į konteinerius sukuria konteinerius ir paėmimo darbą siuntoms, kai apdorojama banga. Išsamesnės informacijos apie tai, kaip jį nustatyti, ieškokite [Krovimas į konteinerius](wave-containerization.md).

## <a name="work-with-the-scheduled-work-creation"></a>Darbas su Suplanuoto darbo kūrimo funkcija

Kai *Suplanuoto darbo kūrimo* funkcija yra įjungta, bangos apdorojimas sukurs suplanuotą darbą, kuris galiausiai bus panaudotas naujo darbo kūrimo procese. Darbo kūrimo metu darbas bus užblokuotas, naudojant *Visos organizacijos darbo blokavimo* funkciją. Daugiau informacijos rasite [Suplanuoto darbo kūrimas bangos metu](configure-wave-schedule-work-creation.md).

Šiose struktūrinėse schemose parodyta, kaip bangos apdorojimo metu sukuriamas suplanuotas darbas.

![Darbo grafiko kūrimas](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Suplanuotas Darbas

Puslapyje **Suplanuoto darbo informacija** (**Sandėlio valdymas \> Darbas \> Suplanuoto darbo informacija**) rodoma informacija apie suplanuotą darbą, kuris iš pradžių yra sukuriamas bangos apdorojimo metu. Galimos šios **Apdorojimo būsenos** reikšmės:

- **Eilėje** – laukiama, kada suplanuotas darbas bus panaudotas darbui sukurti.
- **Užbaigta** – suplanuotas darbas buvo panaudotas darbui sukurti.
- **Nepavyko** – bangos apdorojimas nepavyko. Atkreipkite dėmesį, kad suplanuoto darbo būsena gali būti **Nepavyko** su susijusiu faktiniu darbu arba be jo. Kai faktinio darbo kūrimo procesas nepavyksta, faktinio darbo būsena lieka *Atšaukta*.

### <a name="batch-job-for-the-work-creation-process"></a>Paketinė užduotis darbo kūrimo procesui

Norėdami peržiūrėti paketines užduotis bangų apdorojimui pasirinkite **Paketines užduotis** veiksmų srityje, **Visos bangos** puslapyje.

Čia galite peržiūrėti visą paketinės užduoties informaciją apie kiekvieną paketinės užduoties ID.

## <a name="cancel-a-wave"></a>Bangos atšaukimas

Jei reikia, galite atšaukti apdorotą bangą. Norėdami atšaukti bangą ir sukurtą išrinkimo darbą, atlikite toliau nurodytus veiksmus:

1. Atsižvelgdami į norimos atšaukti bangos tipą, atlikite vieną iš šių veiksmų:

      - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Siuntimo bangos** \> **Visos bangos**.
      - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **Gamybos bangos** \> **Visos gamybos bangos**.
      - Eikite į **Sandėlio valdymas** \> **Bendra** \> **Bangos** \> **„Kanban” bangos** \> **Visos „kanban” bangos**.

1. Pasirinkite norimą atšaukti bangą. Veiksmų srities skirtuke **Darbas** pasirinkite **Atšaukti**.

## <a name="review-wave-batch-job-details"></a>Peržiūrėkite išsamią bangos paketinės užduoties informaciją

Naudokite puslapį **Išsami bangos paketinės užduoties informacija** norėdami patikrinti paketines užduotis ir su bet kuria banga susijusias užduotis. Tai ypač naudinga nepavykusios bangos trikčių diagnostikai. Be šios funkcijos, įprastai tik administratoriai turės prieigą prie paketinės užduoties informacijos. Puslapis **Išsami bangos paketinės užduoties informacija** gali būti padarytas prieinamu ne administratoriaus vartotojams ir pateikti paketinių ir susijusių užduočių rodinį „tik skaityti”.

### <a name="enable-the-wave-batch-job-details-page"></a>Puslapio Išsami bangos paketinės užduoties informacija įgalinimas

Jei jūsų sistemoje dar nėra puslapio **Išsami bangos paketinės užduoties informacija**, eikite į [Funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite *Išsamios bangos paketinės užduoties informacijos* funkciją.

### <a name="use-the-wave-batch-job-details-page"></a>Puslapio Išsami bangos paketinės užduoties informacija naudojimas

Puslapyje **Išsami bangos paketinės užduoties informacija** sujungiamos paketinės užduotys ir užduotys, leidžiančios jums ištirti visus bangos veiksmus, be naršymo pirmyn ir atgal tarp vienos paketinės užduoties ir paketinių užduočių sąrašo. Šis puslapis taip pat suteikia prieigą prie paketo žurnalo ir, jei turite reikiamas teises, pateikia saitą į **Paketinių užduočių** puslapį.

Norėdami atidaryti šį puslapį, pasirinkite bangą bet kuriame iš kelių skirtingų bangos puslapių ir tada veiksmų srityje pasirinkite **Išsami bangos paketinės užduoties informacija**.

## <a name="review-load-validation-and-error-messages"></a>Krovinio tikrinimo ir klaidų pranešimų peržiūra

Bangos apdorojimo metu sistema patikrina ir rodo kiekvienos krovinio eilutės būseną bangoje. Jei įspėjimų nėra, bus pereinama prie kito bangos veiksmo. Jei atsiranda įspėjimų, vietoj to, užbaigus tikrinti visą bangą, rodoma šį klaida:

> Bangoje rasta netinkamų krovinio eilučių. Prašom pašalinti netinkamas krovinio eilutes.

Tada prieš bandydami dar kartą, galėsite peržiūrėti kiekvienos krovinio eilutės bangoje galutinę būseną ir ištaisyti visus įspėjimus. Tai jums leidžia iškart išspręsti visus įspėjimus prieš pakartotinį bangos apdorojimą. (Ankstesniuose leidimuose sistema sustabdydavo bangos apdorojimą po pirmojo įspėjimo, tad būdavo galima pataisyti tik po vieną įspėjimą vienu metu.)

Būdas, kaip sistema rodo jūsų bangos apdorojimo būsenos pranešimus, priklauso nuo to, kaip nustatėte parinktį **Kurti bangos apdorojimo retrospektyvos žurnalą** puslapyje **Sandėlio valdymo parametrai**.

- Kai **Kurti bangos apdorojimo retrospektyvos žurnalą** nustatyta į *Ne*, krovinio eilutės būsenos pranešimai rodomi **Sistemos pranešime**.
- Kai **Kurti bangos apdorojimo retrospektyvos žurnalą** nustatyta į *Taip*, krovinio eilutės būsenos pranešimai rodomi **Bangos apdorojimo retrospektyvos žurnalo** puslapyje. Norėdami peržiūrėti žurnalą, eikite į **Sandėlio valdymas \> Siunčiamos bangos \> Bangų apdorojimo retrospektyvos žurnalas**.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Bangos apdorojimo konfigūravimo pavyzdys](tasks/configure-wave-processing.md)
- [Bangos šablonai](wave-templates.md)
- [Krovimas į konteinerius](wave-containerization.md)