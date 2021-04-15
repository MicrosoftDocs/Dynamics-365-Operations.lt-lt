---
title: Prekių saugojimo kainų palyginimo ataskaita
description: Sužinokite, kaip sugeneruoti prekių saugojimo kainų palyginimo ataskaitą, tada peržiūrėkite ir (arba) eksportuokite rezultatą.
author: AndersGirke
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage, InventItemPriceCompareStorageDetailsChart, InventItemPriceCompareStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a9e05dd582ed1bd2c242d3eeb77ca61203706e11
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813224"
---
# <a name="compare-item-prices-storage-report"></a>Prekių saugojimo kainų palyginimo ataskaita

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip vykdyti **Prekių saugojimo kainų palyginimo** ataskaitą ir nustatyti, kad rezultatas būtų prieinamas skaitmeniniu būdu kaip interaktyvus puslapis „Dynamics 365 Supply Chain Management“ arba kaip eksportuojamas dokumentas bet kuriuo iš kelių formatų.

Kai ataskaitą peržiūrite naršyklėje, stulpeliai ir kaupiamieji balansai yra dinamiškai koreguojami atsižvelgiant į jūsų sukonfigūruotą maketą. Galite surikiuoti rezultatus, filtruoti juos, detalizuoti duomenis ir daugiau.

Ataskaitų rezultatai saugomi duomenų objekte **Lyginti prekių kainas**, kuris leidžia filtruoti ir eksportuoti rezultatus kitu formatu, pvz., CSV arba „Microsoft Excel“.

Ataskaita **Palyginti prekių saugojimo kainas** naudinga tais atvejais, kai rezultatas pateikia daug eilučių. Pavyzdžiui, rezultate gausite daug eilučių, jei yra daugiau nei 40 000 prekių, kurių įkainojimo versijos kaina yra laukianti prekės kaina.

## <a name="enable-compare-item-prices-storage"></a>Prekių saugojimo kainų palyginimo įjungimas

Kad galėtumėte naudoti šią funkciją, turite ją įjungti savo sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įgalinti ją, jei reikia. Čia funkcija yra nurodyta kaip:

- **Modulis** – kaštų valdymas
- **Funkcijos pavadinimas** — lyginti prekių saugojimo kainą

## <a name="generate-a-compare-item-prices-storage-report"></a>Generuoti prekių saugojimo kainų palyginimo ataskaitą

Atlikite šiuos veiksmus, norėdami sugeneruoti ir išsaugoti ataskaitą **Palyginti prekių saugojimo kainas**:

1. Eikite į **Išlaidų valdymas > Užklausos ir ataskaitos > Iš anksto nustatytos savikainos ataskaitos > Palyginti prekių saugojimo kainas**.

1. Pasirinkite **Naujas**, kad būtų atverta sritis **Palyginti prekių kainas**. Nustatykite šias parinktis, apibrėžiančias, kurias kainas lyginti ataskaitoje:

    - „FastTab“ **Parametrai** suteikite ataskaitai unikalų **Pavadinimą** ir naudodami skyrių **Lyginti laukiančias kainas** ir **Lyginant naudotos kainos** laukus apibrėžkite, kurias kainas ir datas reikia lyginti.
    - „FastTab“ **Įtrauktini įrašai** nustatykite filtrus ir apribojimus, kad apibrėžtumėte, kuriuos duomenis reikia įtraukti į ataskaitą.
    - „FastTab“ **Vykdyti fone** nustatykite, kaip, kada ir kokiu dažnumu norite generuoti ataskaitą.
    > [!NOTE]
    > Ši ataskaita visada vykdoma kaip paketinės užduoties dalis.

1. Norėdami pritaikyti nustatymus ir uždaryti sritį, pasirinkite **Gerai**.

1. Sukūrus paketinę užduotį, ji bus įtraukta į puslapį **Palyginti prekių saugojimo kainas**. Gali reikėti atnaujinti puslapį, kad matytumėte ataskaitą.

## <a name="explore-the-compare-item-prices-storage-report"></a>Prekių saugojimo kainų palyginimo ataskaitos nagrinėjimas

Sukūrę ataskaitą galite ją peržiūrėti ir naršyti bet kuriuo metu:

1. Eikite į **Išlaidų valdymas > Užklausos ir ataskaitos > Iš anksto nustatytos savikainos ataskaitos > Palyginti prekių saugojimo kainas**.

1. Pasirinkti ataskaitą iš sąrašo.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Norėdami peržiūrėti ataskaitos rezultatus, pasirinkite **Peržiūra**.
    - Norėdami gauti išsamesnį ataskaitos rodinį, pasirinkite **Peržiūrėti informaciją**

1. Atsivėrus pasirinktam rodiniui galite atlikti toliau nurodytus veiksmus.

    - Pasirinkti beveik bet kurio stulpelio antraštę, kurio reikšmes norite rikiuoti arba filtruoti lentelėje, kaip tai darote su dauguma standartinių „Supply Chain Management“ formų. Įsidėmėkite, kad negalite rikiuoti arba filtruoti stulpelio **Grynasis kainos pokytis %**, nes tai yra apskaičiuotasis laukas.
    - Pasirinkite **Dimensijos rodinys**, kad būtų atidaryta sritis, kurioje galėtumėte pasirinkti, kurį dimensijos stulpelį įterpti į formą. Nustatykite **Įrašyti sąranką** kaip **Taip**, jei norite įrašyti šiuos parametrus, kad jie būtų išsaugoti, kai kitą kartą atidarysite ataskaitą. Norėdami pritaikyti nustatymus ir uždaryti pasirinkite **Gerai**.
    - Pasirinkite bet kurią formos eilutę ir pasirinkite **Peržiūrėti informaciją**, kad pamatytumėte daugiau informacijos apie pasirinktą prekę. Čia galėsite detalizuoti duomenis.
    - Pasirinkite bet kurią formos eilutę ir pasirinkite **Peržiūrėti palyginimo diagramą**, kad matytumėte interaktyvų grafinį rezultatų pateikimą, kaip jie susiję su pasirinkta preke. Šiuos rezultatus galite analizuoti pasirinkdami įvairius grafinius elementus diagramoje ir diagramos legendoje.
    - Pasirinkite bet kurią formos eilutę ir pasirinkite **Peržiūrėti skaičiavimo informaciją**, kad pamatytumėte daugiau informacijos apie skaičiavimus, susijusius su pasirinkta preke. Čia galėsite detalizuoti duomenis.

## <a name="export-the-compare-item-prices-storage-report"></a>Prekių saugojimo kainų palyginimo ataskaitos eksportavimas

Kiekviena sugeneruota ataskaita saugoma duomenų objekte **Palyginti prekių kainas**. Norėdami eksportuoti duomenis iš šio objekto bet kokiu palaikomu duomenų formatu, įskaitant CSV arba „Microsoft Excel“, galite naudoti standartines „Supply Chain Management“ duomenų tvarkymo funkcijas.

Toliau pateikiamas pavyzdys, kaip eksportuoti ataskaitą **Palyginti prekių saugojimo kainas**.

1. Eikite į **Sistemos administravimas > Darbo sritys > Duomenų valdymas**.

1. Pasirinkite mygtuką **Eksportuoti**, esantį skyriuje **Duomenų valdymas**.

1. Atidaromas puslapis **Eksportavimas**, kurį naudosite savo eksportavimo užduočiai nustatyti. Pirmiausia turite suteikti savo užduočiai **Grupės pavadinimą**.

1. Skyriuje **Pasirinkti objektai** pasirinkite **Įtraukti objektą**, kad būtų atidarytas dialogo langas, kuriame galite nustatyti šias pasirinktis:

    - **Objekto pavadinimas** – pasirinkite **Lyginti prekių kainas**.
    - **Paskirties duomenų formatas** – pasirinkite formatą, kuriuo norite eksportuoti.

1. Norėdami pridėti naują eilutę pasirinkite **Įtraukti**, tada pasirinkite **Uždaryti**, kad uždarytumėte dialogo langą.

1. Paprastai vienu metu eksportuojate vieną ataskaitą. Norėdami tai padaryti, eilutei, kurią ką tik įtraukėte į sritį **Užklausa**, nustatykite **Filtras**. Tai leis jums nurodyti, kurias ataskaitas iš objekto **Lyginti prekių kainas** norite įtraukti į eksportą. Nustatykite šias filtro pasirinktis vienai ataskaitai eksportuoti:

    - Skirtuke **Diapazonas** pasirinkite **Įtraukti**, kad įtrauktumėte naują eilutę.
    - Nustatykite **Lentelė** reikšmę kaip **Lyginti prekių kainas**.
    - Nustatykite **Išvestinė lentelė** reikšmę kaip **Lyginti prekių kainas**.
    - Nustatykite **Laukas** reikšmę kaip lauką, pagal kurį norite filtruoti. Paprastai naudosite **Vykdymo pavadinimas** arba **Vykdymo laikas**.
    - Nustatykite **Kriterijus** reikšmę kaip pasirinkto lauko, kurio norite ieškoti, reikšmę (arba ataskaitos pavadinimas, arba laikas, kada ataskaita buvo sugeneruota).
    - Jei reikia, įtraukite daugiau eilučių į lentelę **Diapazonas**, kol gausite tiksliai tokią unikalią ataskaitą, kokios reikėjo.

1. Norėdami išsaugoti nustatymus ir uždaryti pasirinkite **Gerai**.

1. Pasirinkite **Įrašyti**, kad įrašytumėte eksporto sąranką.

1. Atidarykite skirtuką **Eksportavimo parinktys** ir pasirinkite **Eksportuoti dabar**, kad būtų sugeneruotas eksporto failas.

1. Atidaromas puslapis **Vykdymo suvestinė**, kuriame galite matyti savo eksportavimo užduoties būseną ir eksportuotų objektų sąrašą. Pasirinkite objektą **Lyginti prekių kainas**, esantį srityje **Objekto apdorojimo būsena**, tada pasirinkite **Atsisiųsti failą**, kad atsisiųstumėte iš to objekto eksportuotus duomenis.

Norėdami gauti daugiau informacijos apie tai, kaip naudoti duomenų valdymo funkciją duomenims eksportuoti, žr. [Duomenų importavimo ir eksportavimo užduočių apžvalga](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]