---
title: Klientų kreditų valdymo informacijos įtraukimas
description: Šioje temoje paaiškinama, kaip įtraukti klientų kreditų valdymo informaciją.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c8584c33b4f77b6d1f5a4dc0d62208b76b3ffa3
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2021
ms.locfileid: "7753975"
---
# <a name="add-credit-management-information-for-customers"></a>Klientų kreditų valdymo informacijos įtraukimas

[!include [banner](../includes/banner.md)]

Nustatę parametrus, kontroliuojančius kreditų valdymą, galite pridėti išsamesnę informaciją apie kiekvieną klientą. Ši išsami informacija valdo kreditų valdymo procesus ir suteikia papildomos informacijos, kuri padeda mokėjimų priežiūros komandai valdyti klientus.

## <a name="customer-information"></a>Kliento informacija

Galite įtraukti kliento išsamią informaciją į „FastTab“ **Kreditai ir mokėjimų priežiūra** puslapyje **Visi klientai** (**Gautinos sumos \> Klientai \> Visi klientai**).

1. Nustatykite parinktį **Neribotas kredito limito** kaip **taip**, jei klientui neturi būti taikomas limitas pagal jokį kredito limito tikrinimą.
2. Nustatykite parinktį **Pašalinti iš kreditų valdymo** kaip **Taip**, kad klientui nebūtų taikomi jokie veiksmai, kurie paprastai atsiranda kreditų valdymo procesuose.
3. Klientui parinkite kreditų valdymo grupę.
4. Norėdami apskaičiuoti kredito limitą kliento valiuta, lauke **Kredito limitas kliento valiuta** įveskite kliento kredito limitą. Kredito limitas įmonės valiuta bus konvertuotas naudojant valiutos kursus, apibrėžtus pagal kredito limito valiutos kurso tipą, kuris pasirinktas kreditų valdymo parametruose.
5. Lauke **Paskutinė peržiūros data** įveskite datą, kada kredito valdytojas paskutinį kartą peržiūrėjo kliento kredito limitą.
6. Lauke **Kita suplanuota peržiūros data** įveskite datą, kada suplanuota peržiūrėti ir naujinti kliento kreditą.
7. Lauke **Tinkamas kredito limitas** įveskite didžiausią kliento kredito limitą, kuris gali būti priskirtas klientui pagal šio kliento kredito istorijos peržiūrą. Tinkamas kredito limitas gali skirtis nuo kredito limito, kuris yra rodomas „FastTab“ **Kreditai ir mokėjimų priežiūra**.
8. Lauke **Tinkamo kredito limito valiuta** įveskite tinkamo kredito limito valiutą.
9. Lauke **Tinkamo kredito limito data** įveskite datą, kada tinkamas kreditas buvo sukurtas.
10. Lauke **Kredito sąskaitos būsena** įveskite kliento kredito sąskaitos būseną.
11. Lauke **Būsenos priežastis** įveskite priežastį, susieta su sąskaitos būsena.
12. Nustatykite parinktį **Su agentūra** kaip **Taip** kad nurodytumėte, kad klientas dabar priskirtas kredito agentūrai. Ši reikšmė skirta tik informacijai. Ji nenaudojama jokiame kreditų valdymo procese.
13. Nustatykite parinktį **Pavadinimas saugomas** kaip **Taip**, kad nurodytumėte, kad pavadinimas saugomas įmonei. Ši reikšmė skirta tik informacijai. Jis nenaudojamas jokiame kreditų valdymo procese.
14. Lauke **Verslo pradžios data** įveskite datą, kada klientas pirmą kartą pradėjo vykdyti verslą. Ši informacija naudojama, kai kuriami rizikos balai.
15. Lauke **Klientas nuo datos** įveskite datą, kada buvo apdorotos pirmos kliento operacijos. Ši informacija naudojama, kai kuriami rizikos balai.
16. Įveskite pastabas, kurias kredito komanda gali naudoti, kad galėtų toliau vertinti kliento kreditingumą.

Atkreipkite dėmesį, kad dalis informacijos, rodomos puslapyje **Klientas**, sukuriama kito proceso metu:

- Lauke **Kredito limito galiojimo data** rodoma data, kada baigiasi kredito limito galiojimas. Jei šio lauko nenustatote, kliento kredito limitas neturi galiojimo laiko.
- Lauke **Kredito limito data** rodoma kredito limito sukūrimo data. Šis laukas atnaujinamas, kai koreguojamas kredito limitas.
- Laikini kredito limitai perrašo kliento kredito limitą laikotarpiui. Jie naudojami vietoje kredito limito, norint apskaičiuoti bendrą kredito limitą. Ši informacija rodoma tik tada, jei yra aktyvus kredito limitas. Galite įtraukti laikinus kredito limitus naudodami kredito limito koregavimus.
- Lauke **Draudimas ir garantijos** rodoma bendra draudimo ir garantijų reikšmė, kuri gali padidinti kliento kredito limitą.
- Lauke **Bendras kredito limito** rodomas galutinis kliento kredito limitas. Bendras kredito limitas apima draudimą ir garantijas bei laikinus kredito limitus.

## <a name="temporary-credit-limits"></a>Laikini kredito limitai

Laikini kredito limitai perrašo kliento kredito limitus apibrėžtam laikotarpiui. Galite įtraukti laikinus kredito limitus naudodami kredito limito koregavimus. Kredito limito koregavimai leidžia kreditų vadovams naujinti vieno kliento, klientų grupės arba visų klientų kreditų limitus ir galiojimo datas naudojant registravimo procesą.

Galite kurti kredito limitų koregavimų įrašus puslapyje **Kredito limito koregavimai** (**Kredito valdymas \> Kredito limito koregavimai \> Kredito limito koregavimai**).

## <a name="create-insurance-policies-and-guarantees"></a>Draudimo polisų ir garantijų kūrimas

Galite sukurti vieną ar daugiau draudimo polisų ir garantijų kiekvienam klientui. Tada galite naudoti juos, kad apskaičiuotumėte savo įmonės, kai ji teikia kreditus klientams, išlaikymą. Draudimo polisus ir garantijas taip pat galima įtraukti į kliento kredito limitą.

Galite kurti draudimo polisus ir garantijas puslapyje **Visi klientai** (**Gautinos sumos \> Klientai \> Visi klientai**). Pasirinkite klientą, tada veiksmų srities skirtuke **Kreditų valdymas** pasirinkite **Draudimas ir garantijos**.

> [!NOTE]
> Šioje procedūroje iš visuotinės adresų knygelės pasirenkate draudiką arba laiduotoją. Todėl prieš pradėdami šią procedūrą turite įsitikinti, kad draudikai ir laiduotojai buvo įtraukti į visuotinę adresų knygelę.

1. Lauke **identifikatorius** įveskite **Garantija** arba **Draudimas**.
2. Lauke **Garantijos / draudimo tipas** pasirinkite vieną iš anksčiau nustatytų garantijų arba draudimo tipų.
3. Lauke **Draudikas / laiduotojas** pasirinkite draudiką arba laiduotoją iš visuotinės adresų knygelės. 
4. Jei pasirinkote **Draudimas** lauke **Identifikatorius**, lauke **Poliso padengimo tipas** pasirinkite vieną iš anksčiau nustatytų padengimo tipų. Negalite pasirinkti garantijos poliso padengimo tipo.
5. Lauke **Identifikavimas** įveskite poliso ID. Šis ID paprastai yra poliso numeris.
6. Lauke **Įsigaliojimas** įveskite draudimo poliso arba garantijos pradžios datą.
7. Lauke **Galiojimas** įveskite datą, iki kada draudimo polisas arba garantija galioja.
8. Lauke **Vertė** įveskite draudimo poliso arba garantijos vertę. Ši vertė yra visa poliso vertė.
9. Lauke **Valiuta** įveskite poliso vertės valiutą. 
10. Lauke **Naujinti kredito limitą** nurodykite procentus nuo **0** iki **100**. Šis procentas bus taikomas poliso vertei, o gauta suma bus naudojama padidinti kredito limitą, kuris skaičiuojamas apskaičiuoti kredito limitą. Apskaičiuota vertė rodoma dalyje **Bendras kredito limitas, draudimas ir garantijos** „FastTab“ **Kreditai ir mokėjimų priežiūra** puslapyje **Klientai**.

    Toliau pateikiamas pavyzdys.

    - Kredito limitas (A) yra 100, 000.
    - Poliso vertė (B) yra 50 000.
    - **Atnaujinti kredito limitą** procentai (C) yra 50,00.
    
    Šiuo atveju faktinis kredito limitas yra 125 000 (= A + \[ B × C\]).

11. Pažymėkite žymės langelį **Įskaičiuota į išlaikymą**, kad sumažintumėte kredito limitą, kuris naudojamas kredito limito skaičiavimuose pagal poliso vertę. Jei šis žymės langelis yra pažymėtas, vertė, apskaičiuota, kai nurodytas **Atnaujinti kredito limitą** procentas, nebus naudojama skaičiuojant kredito limitą.

    Toliau pateikiamas pavyzdys.

    - Kredito limitas (A) yra 100, 000.
    - Poliso vertė (B) yra 50 000.
    - **Atnaujinti kredito limitą** procentai (C) yra 50,00.

    Šiuo atveju faktinis kredito limitas yra 125 000 (= A + \[ B × C\]).
    
    Tačiau, jei pažymėsite žymės langelį **įtrauktas į išlaikymą**, vertė **Atnaujinti kredito limitą**, lygi 50 000 (=50,00 procentų vertės 100 000), pašalinama, o išlaikymo vertė yra 75 000 (= A + \[ B × C\] – B).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
