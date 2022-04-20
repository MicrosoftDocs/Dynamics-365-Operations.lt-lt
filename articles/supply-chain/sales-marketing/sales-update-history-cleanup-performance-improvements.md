---
title: Planuoti pardavimo retrospektyvos duomenų valymą
description: Šioje temoje aprašoma, kaip padėti gerinti sistemos našumą, planuojant periodinę pardavimo atnaujinimo retrospektyvos valymo užduotį, kuri bus vykdoma įprastu intervalu.
author: myvakalo
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6c6c1e08d45f2a7d1e1267010b286111bad01a6c
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570400"
---
# <a name="schedule-sales-history-data-cleanup"></a>Planuoti pardavimo retrospektyvos duomenų valymą

[!include [banner](../includes/banner.md)]

"Microsoft Dynamics 365 Supply Chain Management " kaip standartinės operacijos dalį generuoja ir saugo vykdomo pardavimo retrospektyvos naujinimo duomenis. Laikui bėgant jūsų sistemoje gali kauptis daug pasenusių pardavimo retrospektyvos duomenų. Registruojant dokumentus, susijusius su pardavimo užsakymais, šie sukaupti duomenys gali sukelti našumo ir funkcinių problemų. (Šiuos dokumentus sudaro pardavimo užsakymų patvirtinimai, pardavimo važtaraščiai, pardavimo išrinkimo dokumentai ir SF). Todėl turite nustatyti ir suplanuoti pardavimų atnaujinimo retrospektyvos *periodinio valymo periodinę* užduotį, kad ji būtų vykdoma įprastu intervalu. Ši užduotis pašalins visus pardavimo retrospektyvos atnaujinimo duomenis, kurių prireiks.

Jei naudojate pardavimų atnaujinimo *retrospektyvos valymo* periodinę užduotį, *rekomenduojame* įgalinti pardavimo retrospektyvos valymo našumo patobulinimų funkciją, kuri padeda efektyviau vykdyti užduotį. (Neatsižvelgiant į tai, galite atlikti užduotį neįjungdami šios funkcijos.)

## <a name="turn-on-the-sales-history-cleanup-features"></a>Įjungti pardavimo retrospektyvos valymo priemones

Norėdami nustatyti *ir* naudoti pardavimo atnaujinimo retrospektyvos periodinio valymo periodinę užduotį su visomis šioje temoje aprašytomis funkcijomis, *·* *turite* įgalinti pardavimo retrospektyvos valymo našumo patobulinimus ir išvalyti pardavimo atnaujinimo retrospektyvą pagal funkcijų valdymo amžiaus funkcijas, kaip aprašyta toliau nurodytose poskyrėse.

### <a name="sales-history-cleanup-performance-improvements"></a>Pardavimo istorijos valymo našumo patobulinimai

Periodinis partinis darbas **Pardavimų retrospektyvos valymas** gali ilgai užtrukti, jei jis nedažnai vykdomas aplinkose, kuriose yra didelis pardavimų naujinimų kiekis. Tokiais atvejais *Pardavimo retrospektyvos valymo našumo patobulinimų* priemonė gali padėti sumažinti vykdymo trukmę ir padidinti patikimumą.

Priemonė pagerina esamą valymo užduotį šiais būdais:

- Ji išskaido išvalymą į paketus (pritaikymais galite keisti paketo dydį).
- Jis veiks daugiausia 2 valandas (pritaikymo metu galite keisti trukmę).
- Kai įmanoma, jis pritaiko svertą duomenų bazės galimybėms, kad valymo metu būtų sumažinti užrakinimų ginčai ir būtų išvengta operacinių lentelių prijungimo.

Įgalinus šią priemonę, **Pardavimo atnaujinimo retrospektyvos valymo** paketinė užduotis (**Pardavimo ir rinkodaros \> Periodinė užduotis \> Valymas \> Pardavimo atnaujinimo retrospektyvos valymas**) bus vykdoma taip, kaip buvo anksčiau, tačiau geresniu veikimu ir daugiausiai 2 valandoms. Tai reiškia, kad gali tekti paleisti kelis kartus, kad išvalytumėte visus duomenis per tam tikrą saugojimo laikotarpį.

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Pardavimai ir rinkodara*
- **Funkcijos pavadinimas:** *Pardavimo istorijos valymo našumo patobulinimai*

### <a name="clean-up-sales-update-history-based-on-age"></a>Valyti pardavimo naujinimo istoriją pagal terminą

Naudojant *funkciją Valyti pardavimo naujinimo retrospektyvą* *pagal* amžiaus priemonę galima nurodyti didžiausią įrašų amžių, kuris bus naudojamas paleidus pardavimo atnaujinimo retrospektyvos valymo periodinę užduotį. Senesni įrašai bus panaikinti. Ši funkcija naudinga, kai nustatote, kad užduotis būtų vykdoma periodiškai, nes terminas visada apskaičiuojamas atsižvelgiant į užduoties vykdymo datą. Jei šios funkcijos nepasinaudosite, galite nustatyti tik seniausių įrašų, kuriuos norite saugoti, konkrečią datą.

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Pardavimai ir rinkodara*
- **Priemonės pavadinimas: valyti** *pardavimo naujinimo retrospektyvą pagal amžių*

## <a name="set-up-and-schedule-the-sales-history-cleanup-periodic-task"></a>Nustatyti ir planuoti pardavimo retrospektyvos valymo periodinę užduotį

Norėdami nustatyti ir suplanuoti pardavimo retrospektyvos *valymo periodinę* užduotį, atlikite šiuos veiksmus.

1. Analizuodami savo verslą turite nustatyti, kiek dienų turi išlaikyti istorinių pardavimo užsakymų registravimo duomenys. Paprastai rekomenduojame valymo užduotį vykdyti kas tris mėnesius, daugiausia kas šešis mėnesius.
1. Eiti į pardavimo **ir rinkodaros laikotarpio \> užduočių valymas \> pardavimo \> atnaujinimo retrospektyvos valymą**.
1. Dialogo lango **Valyti pardavimo atnaujinimo retrospektyvą** skirtuke **Parametrai** nustatykite šiuos laukus:

    - **Valyti** – norėdami nurodyti valytinos įrašų tipą pasirinkite vieną iš šių verčių:

        - **Įvykdyta** – naikinti tik visiškai apdorotus įrašus. Kadangi šiems įrašams galite naudoti daugiau informacijos, ši pasirinktis yra saugiausia.
        - **Įvykdyta ir klaidinga – naikinti ir** visiškai apdorotus įrašus, ir įrašus, kuriuose įvyko klaida. Ši pasirinktis yra dažniausiai naudojama. Galite patikrinti ir net pataisyti klaidingus įrašus, užuot automatiškai išvalę. Tačiau daugelis įmonių pasirenka išvalyti šiuos įrašus po mėnesio, nes tuo laiku jie tikriausiai nebeatitinka.
        - **Viskas** – naikinti įvykdytus, klaidingus ir laukiančius įrašus. Laukiančių įrašų galiojimo, bet jie dar nebuvo visiškai apdoroti. Daugeliu atvejų tikriausiai nenorite, kad jie būtų panaikinti automatiškai. Tačiau kai kuriais atvejais galite pasirinkti, kad jie būtų automatiškai panaikinti praėjus tam tikrai situacijai.

    - **Išlaikyti įrašus pagal** amžių – nurodyti, ar norite išvalyti įrašus pagal jų amžių dieną, kai užduotis vykdoma, arba panaikinti įrašus, sukurtus iki nustatytos datos. Jei valymą planuojate kaip pasikartojančią užduotį, *turite* nustatyti šią pasirinktį kaip Taip, nes amžius visada apskaičiuojamas pagal užduoties vykdymo datą.

        - Nustatykite šią pasirinktį *kaip Taip*, kad įgalintumėte lauką **Maksimalus** amžius. Naudokite šį lauką, norėdami nurodyti maksimalų įrašų amžių, kurį reikia išlaikyti kiekvieną kartą paleidus užduotį. Iki **lauko Sukurta** nepaisoma.
        - Norėdami įgalinti lauką Sukurta *iki*, nustatykite šią **pasirinktį** kaip Ne. Naudokite šį lauką norėdami nurodyti seniausią įrašų, kuriuos reikia išlaikyti paleidus užduotį, sukūrimo datą. Maksimalaus **amžiaus** lauko nepaisoma.

    - **Sukurta iki** – šis parametras taikomas tik tada, kai **pasirinktis** Išlaikyti įrašus pagal amžių nustatyta kaip *Ne*. Nurodykite seniausią įrašų sukūrimo datą, kurią reikia išlaikyti paleidus užduotį. Įrašai, sukurti iki šios datos, bus panaikinti.
    - **Maksimalus amžius** – šis parametras taikomas tik tada, kai **pasirinktis** Išlaikyti įrašus pagal amžių nustatyta kaip *Taip*. Nurodyti maksimalų įrašų amžių (dienomis), kurį reikia išlaikyti kiekvieną kartą paleidus užduotį. Senesni įrašai bus panaikinti.

1. Skirtuke **Vykdyti fone** FastTab nurodykite, kaip, kada ir kaip dažnai užduotis vykdoma. Naudokite šiuos parametrus grafikui, kurį nustatėte 1 žingsniu, įdiegti. Šie laukai veikia taip pat kaip ir kitų tipų paketinės [užduotys tiekimo](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) grandinės valdymo srityje.
1. Norėdami pritaikyti nustatymus ir uždaryti dialogo langą, pasirinkite **Gerai**.
