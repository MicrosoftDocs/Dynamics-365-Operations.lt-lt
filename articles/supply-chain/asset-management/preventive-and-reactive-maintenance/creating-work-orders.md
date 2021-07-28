---
title: Darbo užsakymų kūrimas
description: Šioje temoje aiškinama, kaip sukurti darbo užsakymus turto valdyme.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: d2fe07790f64f7e7f672980f80a3e56804cefd66
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351542"
---
# <a name="creating-work-orders"></a>Darbo užsakymų kūrimas

[!include [banner](../../includes/banner.md)]

Suplanavus prevencines priežiūros užduotis, kitas žingsnis yra sukurti jų darbo užsakymą. Šį veiksmą atlikti galite naudodami vieną iš priežiūros grafikų. Suplanuotos užduotys priežiūros grafike gali turėti skirtingus nuorodos numerius, kaip apibūdinta šioje lentelėje.

| Nuorodos tipas | Aprašymas |
|---|---|
| Priežiūros planai | Prevencinės priežiūros užduotys, pagrįstos *Laikas* arba *Skaitiklis* priežiūros plano tipu. |
| Priežiūros ciklai | Prevencinės priežiūros užduotys, turinčios kelis turtus, kuriems reikia atlikti panašaus tipo priežiūrą. |
| Priežiūros užklausa | Rankiniu būdu sukurta turto priežiūros ar atkūrimo užklausa. Šią užklausą galima konvertuoti į darbo užsakymą. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Darbo užsakymų, remiantis jūsų priežiūros grafiku, kūrimas

Norėdami sukurti darbo užsakymus pagal jūsų priežiūros grafiką, atlikite šiuos veiksmus.

1. Atidarykite vieną iš šių puslapių, atsižvelgiant į tai, kaip norite pasirinkti jūsų darbo užsakymų grafiko elementus:

    - Visi priežiūros grafikai (**Turto valdymas \> Valdymo grafikas \> Visi priežiūros grafikai**)
    - Atviros priežiūros grafiko eilutės (**Turto valdymas \> Valdymo grafikas \> Atviros priežiūros grafiko eilutės**)
    - Atviri priežiūros grafiko telkiniai (**Turto valdymas \> Valdymo grafikas \> Atviri priežiūros grafiko telkiniai**)

1. Tinklelyje pažymėkite žymės langelį kiekvienai suplanuotai priežiūros užduočiai, kuriai norite sukurti darbo užsakymą. Tada veiksmų srityje pasirinkite **Darbo užsakymas**.

    Atsiranda **Kurti darbo užsakymus** dialogo langas. Lauke **Priežiūros prognozės valandos** rodomas bendras prognozuojamų valandų skaičius pasirinktoms eilutėms.

    ![Dialogo langas Kurti darbo užsakymus.](media/18-preventive-maintenance.png)

1. Skyriuje **Parametrai** nurodykite skaičių darbo užsakymų, kurie turi būti sukurti. Pasirinkite vieną iš toliau pateiktų pasirinkčių:

    - **Vienas darbo užsakymas vienai eilutei** – Kurkite vieną darbo užsakymą vienai priežiūros grafiko eilutei.
    - **Vienas darbo užsakymas pagal** – Kurkite darbo užsakymus, sugrupuotus pagal kitų parinkčių, kurios tampa galimos pasirinkus šią parinktį, nustatymus.

1. Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą, kuris bus naudojamas visiems jūsų kuriamiems darbo užsakymams.
1. Pasirinkite **Gerai** darbo užsakymų kūrimui pagal savo parametrus.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Darbo užsakymo eilučių, sukuriamų automatiškai priežiūros plano vykdymo metu, grupavimas

Ši funkcija leidžia jums nustatyti darbo užsakymo eilučių grupavimo pagal vieną darbo užsakymą taisykles, kai sistema yra nustatyta generuoti darbo užsakymus automatiškai, atsižvelgiant į priežiūros planą. Anksčiau automatiškai sugeneruotuose darbo užsakymuose galėjo būti tik viena eilutė. Tačiau dabar galite grupuoti darbo užsakymus pagal, pavyzdžiui, turtą, turto tipą ar funkcinę vietą. (Rankiniu būdu sugeneruotus darbo užsakymus tokiu būdų jau buvo galima grupuoti, kaip aprašyta ankstesniame šios temos skyriuje.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Automatiškai sugeneruotų darbo užsakymų grupavimo įgalinimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Turto valdymas*
- **Funkcijos pavadinimas:** *Taikyti darbo užsakymų grupavimo taisykles vykdant priežiūros planą*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Automatiškai sugeneruotų darbo užsakymų grupavimo nustatymas

Norėdami nustatyti automatiškai sugeneruotų darbo užsakymų grupavimą, atlikite šiuos veiksmus.

1. Eikite į **Turto valdymas \> Sąranka \> Prevencinė priežiūra \> Priežiūros planai**.
1. Kiekvienam planui, kuriame norite generuoti sugrupuotus darbo užsakymus, atlikite šiuos veiksmus:

    1. Pasirinkite planą iš sąrašo srities.
    1. „FastTab” **Eilutės** įsitikinkite, kad žymės langelis **Automatinis kūrimas** yra pažymėtas kiekvienoje eilutėje.

1. Eikite į **Turto valdymas \> Laikotarpio \> Prevencinė priežiūra \> Planuoti priežiūros planus**.
1. Dialogo lango **Planuoti priežiūros planus** skyriuje **Laikotarpis** nurodykite plano laiko perspektyvas (kaip toli žvelgti į ateitį ieškant suplanuotų priežiūros užduočių, kurioms generuoti darbą).
1. Nustatykite parinktį **Automatiškai kurti darbo užsakymą iš grafiko** į *Taip*.
1. Skyriuje **Darbo užsakymas** pasirinkite vieną iš šių parinkčių:

    - **Vienas darbo užsakymas vienai eilutei** – Kurkite vieną darbo užsakymą vienai priežiūros grafiko eilutei. (Ši parinktis suteikia tas pačias funkcijas, kurios galimos, kai išjungta *Taikyti darbo užsakymų grupavimo taisykles, kai vykdomas priežiūros planas* funkcija.)
    - **Vienas darbo užsakymas pagal** – Kurkite darbo užsakymus, sugrupuotus pagal kitų parinkčių, kurios tampa galimos pasirinkus šią parinktį, nustatymus.

1. Jei norite, kad parinktys būtų taikomos vykdant tik kai kuriuos jūsų priežiūros planus, „FastTab” **Įtrauktini įrašai** pridėkite tiek filtrų, kiek jums reikia, kaip ir kitose „Microsoft Dynamics 365 Supply Chain Management” paketinėse užduotyse.
1. „FastTab” **Vykdyti fone** nustatykite paketo ir planavimo parinktis taip, kaip jums reikia, kaip ir kitoms „Supply Chain Management” paketinėms užduotims.
1. Pasirinkite **Gerai** tam, kad būtų vykdomi ir (arba) suplanuoti pasirinkti priežiūros planai.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]