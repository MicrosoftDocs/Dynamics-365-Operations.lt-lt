---
title: Tinkinti mokesčių konfigūracijas, skirtas bendrojo duomenų peržvalgai
description: Šioje temoje paaiškinama, kaip pritaikyti mokesčių konfigūracijas, norint išplėsti pagrindinių duomenų peržvalgos funkciją.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69541316ad4c6c4bb404ea142844ce596b5502b9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689134"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Tinkinti mokesčių konfigūracijas, skirtas bendrojo duomenų peržvalgai

[!include [banner](../includes/banner.md)]

Šioje temoje atlikite veiksmus, kaip pritaikyti mokesčių konfigūracijas, norint išplėsti pagrindinių duomenų peržvalgos funkciją.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Importuoti „Microsoft" pateiktą mokesčių konfigūraciją

1. Darbo srityje „Regulatory Configuration Service“ (RCS) **Elektroninių ataskaitų** pasirinkite **Microsoft** konfigūravimo teikėją.
2. Pasirinkite **Saugyklos**.
3. Pasirinkite **Visuotiniai ištekliai** ir pasirinkite **Atidaryti**.
4. Pasirinkite mokesčio konfigūraciją, **pvz., Mokesčių skaičiavimo konfigūraciją**, tada skirtuke **Versijos** pasirinkite versiją.
5. Pasirinkite **Importuoti**.

> [!NOTE]
> Pagal numatytuosius „Dataverse“ nustatymus modelio susiejimas importuojamas. Jei konfigūracijos importavimo proceso metu gaunate perspėjimo pranešimus, įgalinkite virtualiuosius „Dataverse“ objektus. Daugiau informacijos žr. skyriuje [Įjunkite „Dataverse“ virtualūs objektai](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Sukurti tinkintą duomenų modelio konfigūraciją

1. Elektroninės ataskaitos **darbo srityje** pasirinkite Mokesčių konfigūracijas, tada pasirinkite norimą išplėsti duomenų **modelio konfigūraciją**. Pvz., pasirinkite **Mokesčių skaičiavimo duomenų modelį**.
2. Pasirinkite **Kurti konfigūraciją**.
3. Pasirinkite **Apmokestinamo dokumento modelį, išvestą iš pavadinimo: mokesčių skaičiavimo duomenų modelis, Microsoft**.
4. Lauke **Pavadinimas** įveskite **Tinkinimo duomenų modelis**.
5. Pasirinkite **Kurti konfigūraciją**.

## <a name="create-customized-reference-models"></a>Kurti pritaikytus nuorodų modelius

1. **Mokesčių konfigūracijos** puslapyje pasirinkite **Tinkinimo duomenų modelis** tada pasirinkite **Konstruktorius**.
2. Pasirinkite modulio daugtaškio mygtuką (**...**), tada pasirinkite **Nuorodos modelis** rodinys.

    [![Nuorodos modelis.](./media/pic2.png)](./media/pic2.png)

3. Kurti pritaikytus nuorodų modelis. Pritaikytas modelis yra šakninis modelis. Tinkinto objekto registro sąrašas. Pritaikytas laukas yra eilutės laukas, kurį norite naudoti peržvalgoje. Prireikus galite įtraukti daugiau laukelių kaip norite.
4. Pasirinkite modulio daugtaškio mygtuką (**...**), tada pasirinkite **Apmokestinamas dokumentas** rodinys.
5. Pasirinkite atributą, kurį norite susieti su pritaikytu nuorodos modeliu. Pvz., pasirinkite **Pritaikytas atributas**, tada atlikite šiuos veiksmus:

    1. Pasirinkite **Pasirinkti nuorodos modelį**.
    2. Pasirinkite **Pritaikytas modelis**, o tada – **Gerai**. Nuorodos modelio pavadinimas atnaujinamas pagal srities **rakto lauko** vertę.

        [![Pasirinkti nuorodos modelio dialogo langą.](./media/pic5.png)](./media/pic5.png)

    3. Pasirinkite **Įrašyti**, tada – **Užbaigti**.

## <a name="create-a-customized-model-mapping-configuration"></a>Sukurti tinkintą duomenų modelio susiejimo konfigūracija

1. Darbo srityje **Elektroninės ataskaitos** rinkitės **Mokesčių konfigūracijas**, ir tada rinkitės **Dataverse modelio susiejimas** konfigūracija.
2. Lauke **Numatytoji modelio susiejimo** laukelyje rinkitės **Ne**.
3. Pasirinkite **Kurti konfigūraciją**.
4. Pasirinkite **Apmokestinamo dokumento modelio susiejimą, išvestą iš pavadinimo: „Dataverse“ modelio susiejimas, Microsoft**.
5. Lauke **Pavadinimas** įveskite **Tinkinimo susiejimo modelis**.
6. Paskirties **modelio lauke** pasirinkite **tinkinimo duomenų modelio** duomenų modelį.
7. Pasirinkite **Kurti konfigūraciją**.

    [![Konfigūracijos išplečiamojo dialogo lango kūrimas.](./media/pic6.png)](./media/pic6.png)

8. Pasirinkite **inkinimo modelio susiejimas** ir nustatykite **Prijungta lauką** kaip ryšį, kuris buvo sukurtas 8 žingsniu, nustatyti pagrindinių [Nustatykite aplinkos pagrindinius duomenis apžvalgoje](tax-service-set-up-environment-master-data-lookup.md).
9. Nustatykite parinktį **Numatytasis modelių susiejimui** laukelį į **Taip**.

## <a name="create-customized-model-mappings"></a>Kurti pritaikytus modelio susiejimus

1. Puslapyje **Mokesčių konfigūracijos** rinkitės **tinkinimo modelio susiejimą**.
2. Pasirinkite **Kūrimo įrankis**, o tada – **Tinkinimo modelis**.

    [![Tinkinimo modelis.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Modelio susiejimo su objektu „Dataverse“ susiejimas

1. **Modelio susiejimo kūrimo įrankis** puslapyje pasirinkite **Tinkinimo modelis** tada pasirinkite **Konstruktorius**.
2. Medyje **Duomenų šaltinio** rinkitės **Dataverse lentelė**.
3. **Duomenų šaltiniai** skirtuke pasirinkite **Įtraukti šaknį**.
4. Laukelyje **Pavadinimas** rinkitės **Tinkinti Dataverse**.
5. Antrame lauke **Pavadinimas** pasirinkite objektą.
6. Pasirinkite **Gerai**.

    [![Lentelės duomenų šalšinio ypatybių dialogo langas.](./media/pic9.png)](./media/pic9.png)

7. Pasirinkite **Tinkintas Dataverse** ir **Tinkintas objektas** tada pasirinkite **Susieti**.

    [![Pritaikytas Dataverse ir Tinkintas objekto susiejimas.](./media/pic10.png)](./media/pic10.png)

8. Pasirinkite **Tinkintas Dataverse** ir **Tinkintas laukelis** rinkitės laukelį ir tada pasirinkite **Susieti**.

    [![Pritaikytas Dataverse ir Tinkintas laukelis susiejimas.](./media/pic11.png)](./media/pic11.png)

9. Pasirinkite **Įrašyti**, tada – **Užbaigti**.

## <a name="create-a-customized-tax-configuration"></a>Sukurti tinkintą mokesčių konfigūraciją

1. Darbo srityje **Elektroninės ataskaitos** rinkitės **Mokesčių konfigūracijas** ir tada rinkitės **Mokesčių skaičiavimo konfigūravimas**.
2. Pasirinkite **Kurti konfigūraciją**.
3. Pasirinkite **mokesčių tarnybos konfigūraciją, išvestą iš pavadinimo: mokesčių skaičiavimo konfigūracija, „Microsoft"**.
4. Lauke **Pavadinimas** įveskite **Tinkinimo konfigūravimas**.
5. Pasirinkite **Kurti konfigūraciją**.
6. Pasirinkite **Tinkinti konfigūravimas**, o tada – **Kūrimo įrankis**.
7. Paskirties **Duomenų modelio** lauke pasirinkite **tinkinimo duomenų modelio** duomenų modelį.
8. Lauke **Duomenų modelio** versija pasirinkite atitinkamą duomenų modelio versiją.

    [![Ypatybės sritis.](./media/pic13.png)](./media/pic13.png)

9. Pasirinkite **Baigti**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
