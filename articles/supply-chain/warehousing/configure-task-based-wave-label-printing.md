---
title: Planuoti bangos žymos spausdinimą bangos vykdymo metu
description: Šioje temoje aprašoma, kaip nustatyti ir naudoti funkcijas, skirtas užduotimi pagrįstam bangos žymų spausdinimui.
author: MSFTGarm
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-obaranov
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 652e6fb3f586fc873ffabf2c741e5c99216931461f159a42f08f9922e756280f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735901"
---
# <a name="schedule-wave-label-printing-during-wave"></a>Planuoti bangos žymos spausdinimą bangos vykdymo metu

[!include [banner](../../includes/banner.md)]

Naudokite *Užduotimi pagrįstos bangos žymų spausdinimo* funkciją kaip jūsų bangos proceso dalį, kad būtų pagerintas efektyvumas, o sistema sukurtų bangos žymas ir darbą atskiromis užduotimis.

Bangos žymos spausdinimo konfigūravimas yra sudėtingas ir remiasi tikslia konfigūracija ir bendraisiais duomenimis. Neretai bangos žymos įrašų generavimas nepavyksta, o kai taip nutinka, sutrinka visas bangos apdorojimas. *Užduotimi pagrįsto bangos žymos spausdinimo* funkcija padeda išvengti pakartotinio darbo ir darbo eilučių kūrimo kiekvieną kartą, kai bangos žymė yra neteisingai išspausdinta.

Kai naudojate *Užduotimi pagrįstos bangos žymų spausdinimo* funkciją, sistema pirmiausia sukuria darbą ir darbo eilutes. Tada ji sukuria ir atspausdina bangos žymas. Galiausiai, jei bangos žymos sukurtos tinkamai, ji išleidžia darbą ir bangą išrinkimui.

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>Funkcijų valdyme įjunkite užduotimi pagrįstą bangos žymų spausdinimo funkciją

Norėdami naudoti funkcijas, aprašytas šioje temoje, jos turi būti įjungtos jūsų sistemai. Naudokite darbo sritį [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte funkcijas pateikta tvarka:

1. *Bangos žymų spausdinimas* – ši funkcija būtina norint įgalinti bangos procesų metodą bangos žymų spausdinimui.
1. *Visos organizacijos darbo blokavimas* – ši funkcija reikalingas tiek rankiniam, tiek automatiniam suplanuoto darbo kūrimo konfigūravimui.
1. *Užduotimi pagrįstas bangos žymos spausdinimas* – ši funkcija reikalinga norint bangos žymos spausdinimą padalyti į atskirą operacijos aprėptį.

## <a name="manually-enable-the-new-wave-step-method"></a>Naujos bangos veiksmo metodo įgalinimas rankiniu būdu

Pirmiausia turite sukurti naują bangos veiksmo metodą ir įgalinti jį lygiagrečiam asinchroniniam užduoties apdorojimui.

1. Eikite į **Sandėlio valdymas \>Sąranka \> Bangos \> Bangos apdorojimo metodai**.
1. Veiksmų srityje pasirinkite **Pakartotinai generuoti metodą**. Atkreipkite dėmesį, kad *„waveLabelPrinting”* yra įtrauktas į bangos proceso metodų, kuriuos galite naudoti savo siuntimo bangos šablonuose, sąrašą.
1. Pasirinkite įrašą, kuriame laukas **Metodo pavadinimas** yra nustatytas į *„waveLabelPrinting”*, o tada veiksmų srityje pasirinkite **Užduoties konfigūracija**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Sandėlis** – pasirinkite sandėlį, kurį panaudosite darbo grafiko kūrimo apdorojimui. (Jei tikrinimo tikslais naudojate demonstracinius duomenis, galite pasirinkti *24* sandėlį. )
    - **Didžiausias paketinių užduočių skaičius** – Nurodykite maksimalų paketinių užduočių skaičių. Daugeliu atvejų vertė turi būti nuo *8* iki *16*. Tačiau patariame eksperimentuoti, kad surastumėte optimalius parametrus savo scenarijams.
    - **Bangos apdorojimo paketų grupė** – Pasirinkite paskirtą bangos apdorojimo paketų grupę, kad optimizuotumėte paketų eilės apdorojimą.

Dabar galite atnaujinti esamą bangos šabloną taip, kad jis naudotų *Bangos žymos spausdinimo* bangos apdorojimo metodą. Taip pat, galite sukurti naują bangos šabloną, kuris naudoja tą metodą.

1. Eikite į  **Sandėlio valdymas\>Nustatymas \> Bangos \> Bangų šablonai**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Sąrašo srityje pasirinkite bangos šabloną atnaujinimui. (Jei tikrinimo tikslais naudojate demonstracinius duomenis, galite pasirinkti *Numatytasis 24 siuntimas*. )
1. „FastTab” **Metodai** stulpelyje **Likę metodai** pasirinkite eilutę, kurioje laukas **Pavadinimas** nustatytas į *„waveLabelPrinting”*.
1. Pasirinkite **įtraukti** (dešinės rodyklės mygtukas), kad perkeltumėte pasirinktą eilutę į **Pasirinkti metodai** stulpelį.
1. Lauke **Bangos veiksmo kodas** įveskite bangos veiksmo kodą, kuris bus naudojamas bangos šablonui sujungti su bangos žymos šablonu.

## <a name="set-wave-task-processing-threshold-data"></a>Nustatykite bangos užduoties apdorojimo ribinės vertės duomenis

Pirmą kartą vykdant bangos procesą naudojant bet kokį užduotimi pagrįstą apdorojimą, sistema sukuria numatytuosius bangos užduoties apdorojimo ribinės vertės duomenis. Šie duomenys yra naudojami valdymui, nepriklausomai nuo to, ar bangos apdorojimas bus vykdomas asinchroniškai ir bus pagrįstas užduotimi, kad būtų galima apdoroti ir kurti bangos žymas lygiagrečiai.

Iš pradžių numatytieji duomenys naudoja *1* kaip ribinę mažiausio darbo ID skaičiaus („`MinimumWorkThresholdForLabelPrinting`”) vertę. Todėl, kai sistema apdoroja bangą, turinčią daugiau nei vieną darbo ID, ji naudos užduotimi pagrįstą bangos žymų apdorojimą atskiroje operacijoje. Galite rankiniu būdu įterpti ar atnaujinti šiuos duomenis „`WHSWaveTaskProcessingThresholdParameters`” lentelėje savo testavimo aplinkose. Norėdami pakeisti šį parametrą gamybos aplinkoje, turite kreiptis į „Microsoft“ palaikymo tarnybą ir pateikti užklausą naujinimui.

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>Bangos apdorojimo logikos pakeitimai, kai naudojamas užduotimi paremtas bangos žymos spausdinimas

Jei bangos žymos apdorojimas viršija bangos užduoties apdorojimo ribinę vertę, inicijuojamas užduotimi pagrįstas apdorojimas. Kito bangos apdorojimo metu, kuris atitinka bangos šabloną, bangos žymos spausdinimas bus vykdomas atskira *„ttsbegin”*/*„ttscommit”* operacija iškart po darbo sukūrimo. Jei darbo paleidimas (atblokavimas) sukonfigūruotas bangos šablone automatiniam vykdymui, jis įvyksta tik sėkmingai atlikus bangos žymos spausdinimo apdorojimą.

Jei bangos žymos generavimas nepavyksta (pavyzdžiui, jei darbo kiekio konvertavimas į bangos žymos kiekį nepavyksta ir įvyksta klaida), tik atitinkama operacija nepavyksta. Anksčiau sukurtas darbas lieka užšaldytas. Norėdami ištaisyti klaidas ir atspausdinti bangos žymas, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Tinklelyje pasirinkite atitinkamą bangą.
1. Veiksmų juostoje, **Bangos** skirtuke, **Spausdinimo** grupėje, pasirinkite **Bangos žymės**.
1. Vadovaukitės ekrane pateikiamomis instrukcijomis žymų nusiuntimui į spausdinimą.
1. Veiksmų srities skirtuko **Banga** grupėje **Banga** pasirinkite **Išleisti**, kad rankiniu būdu išleistumėte pasirinktos bangos darbą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Bangos žymos spausdinimas](configure-wave-label-printing.md)
- [Darbo kūrimo bangos metu planavimas](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
