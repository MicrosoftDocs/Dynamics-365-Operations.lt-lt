---
title: Kilmės šalis / regionas
description: Daugelis organizacijų išduoda sertifikatus savo pardavėjams tam, kad užtikrintų, jog jų produktai atitiktų sertifikato standartus. Šie sertifikatai dažnai priklauso nuo kilmės šalies. Šiame skyriuje pateikiama informacija apie kilmės šalies savybes, kurios leidžia jums susieti gaminį su jo kilmės šalimi ir sekti gaminių sertifikatus.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895553"
---
# <a name="country-of-origin"></a>Kilmės šalis / regionas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Daugelis organizacijų išduoda sertifikatus savo pardavėjams tam, kad užtikrintų, jog jų produktai atitiktų sertifikato standartus. Šie sertifikatai dažnai priklauso nuo kilmės šalies. Kilmės šalies savybės leidžia jums susieti gaminį su jo kilmės šalimi ir sekti gaminių sertifikatus.

## <a name="turn-on-the-country-of-origin-feature"></a>Kilmės šalies funkcijos įjungimas

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti [funkcijos valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, norėdami sužinoti funkcijos būseną ir įjungti ją. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Produkto informacijos valdymas*
- **Funkcijos pavadinimas:** *Kilmės šalies tvarkymo funkcija*

## <a name="configure-source-and-destination-countries"></a>Konfigūruoti šaltinį ir paskirties šalis

Prieš jums išduodant sertifikatą gaminiui privalo susieti jį su jo paskirties šalimi ir kilmės šalimi.

1. Eikite į**Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Kilmės šalies taisyklės**.
2. Pasirinkite esančią šalies sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies sąranką.
3. Naujosios politikos antraštėje, nustatykite šias vertes:

    | Laukas | aprašymas |
    |---|---|
    | Prekės Nr. | Pasirinkite elemento gaminio numerį. |
    | Paskirties šalis | Pasirinkite šalį, į kurią siunčiate gaminį. |
    | Kilmės šalis | Pasirinkite šalį, iš kurios siunčiate gaminį. |

Šios sąrankos tikslas yra padėti jums sukurti medžiagų sąskaitos (BOM) ataskaitą, į kurią galite įtraukti kilmės šalį kiekvienai daliai, kuriai yra nustatytas šaltinis ir paskirties šalis. Ši sąskaita padės jums gauti bendrą paveikslėlį, kuriame matysite, iš kur ateina jūsų dalys ir kur jos eina.

## <a name="keep-track-of-vendor-certificates"></a>Sekite pardavėjų sertifikatus

Galite naudoti **Kilmės šalies pardavėjo sertifikatų** puslapį tam, kad sektumėte sertifikatus, kuriuos išduodate pardavėjams.

Privalote nuspręsti, kuriuos sertifikato dokumentus išduodate ir kaip apie juos pranešite klientams. Ši funkcija padeda jums sekti jūsų sertifikatus. Ji taip pat padeda jums pasirinkti, ar atitinkami sertifikato numeriai bus rodomi sąskaitose, pakavimo lapeliuose ir (arba) užsakymo patvirtinimuose.

Sertifikato informacijos nustatymui, atlikite šiuos žingsnius.

1. Eikite į**Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Pardavėjo kilmės šalies sertifikatai**.
2. Pasirinkite esančią sertifikato sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujo sertifikato sąranką.
3. Naujam ar pasirinktam sertifikatui nustatykite šiuose nustatymus.

    | Laukas | aprašymas |
    |---|---|
    | Tiekėjo kodas | Pasirinkite pardavėją, kuriam išdavėte sertifikatą. |
    | Prekės Nr. | Pasirinkite elementą, kuriam išdavėte sertifikatą. |
    | Šalis/regionas | Paskirties šalis ar regionas, kuriame privalote naudoti šį sertifikatą. |
    | Sertifikato numeris | Įveskite jūsų išduoto sertifikato identifikavimo numerį. |
    | Galioja | Pasirinkite pirmą datą, kai esamas sertifikatas galioja.|
    | Galiojimas | Pasirinkite paskutinę datą, kai esamas sertifikatas galioja. |
    | Atspausdinkite sąskaitą | Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale. |
    | Atspausdinkite pakavimo lipduką | Pasirinkite žymimą laukelį, kad atspausdintumėte pakavimo lipdukų numerį sąskaitose, kurios yra siunčiamos konkrečiai šaliai nurodytų duomenų intervale. |
    | Prekybos užsakymo spausdinimas | Pasirinkite žymimą laukelį, kad atspausdintumėte sertifikato numerį ar prekybos užsakymus, kurie yra siunčiami konkrečiai šaliai nurodytų duomenų intervale. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Įtraukite kilmės šalį į BOM ataskaitas

Kai sukuriate BOM ataskaitą, galite įtraukti kilmės šalį kiekvienai daliai, kurią nurodėte šaltinyje ir kilmės šalyse **Kilmės šalies taisyklės** puslapyje.

1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
1. Pasirinkite ar sukurkite produktą, kad atidarytumėte jo **Išleisto produkto informacija** puslapį.
1. Veiksmų juostoje, **Inžinierius** skirtuke, **BOM** grupėje, pasirinkite **Projektuotojas**.
1. Pasirodžiusiame puslapyje Veiksmų juostoje pasirinkite **BOM \> Spausdinti**.
1. **Medžiagų linijų sąskaitos** teksto lange nustatykite **Paskirties šalies** laukelį į paskirties šalį, kurią norite peržiūrėti savo ataskaitoje.
1. Pasirinkite **Gerai**.

Informaciją pateikianti ataskaita apie kiekvienos dalies kilmės šalį yra sukuriama ir rodoma. Čia pateikiamas ataskaitos pavyzdys.

![Kilmės šalies ataskaita](media/country-of-origin-report.png "Kilmės šalies ataskaita")