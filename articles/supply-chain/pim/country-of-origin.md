---
title: Kilmės šalis / regionas
description: Daugelis organizacijų išduoda sertifikatus savo pardavėjams tam, kad užtikrintų, jog jų produktai atitiktų sertifikato standartus. Šie sertifikatai dažnai priklauso nuo kilmės šalies. Šiame straipsnyje pateikiama informacija apie kilmės šalį, kuri leidžia susieti produktą su jo kilmės šalimi ir sekti produkto sertifikatus.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 60d5a2067b8e3d311af89fb09cfa3b5c007db219
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882524"
---
# <a name="country-of-origin"></a>Kilmės šalis / regionas

[!include [banner](../includes/banner.md)]

Daugelis organizacijų išduoda sertifikatus savo pardavėjams tam, kad užtikrintų, jog jų produktai atitiktų sertifikato standartus. Šie sertifikatai dažnai priklauso nuo kilmės šalies. Kilmės šalies savybės leidžia jums susieti gaminį su jo kilmės šalimi ir sekti gaminių sertifikatus.

## <a name="turn-on-the-country-of-origin-feature"></a>Kilmės šalies funkcijos įjungimas

Kaip ir tiekimo grandinės valdymo versija 10.0.21 ši funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai gali naudotis funkcijų [valdymo puslapiu](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), norėdami patikrinti priemonės būseną ir, jei reikia, ją įgalinti arba išjungti. Čia funkcija yra nurodyta kaip:

- **Modulis:** *Produkto informacijos valdymas*
- **Funkcijos pavadinimas:** *Kilmės šalies tvarkymo funkcija*

## <a name="configure-source-and-destination-countries"></a>Konfigūruoti šaltinį ir paskirties šalis

Prieš jums išduodant sertifikatą gaminiui privalo susieti jį su jo paskirties šalimi ir kilmės šalimi.

1. Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Kilmės šalies taisyklės**.
2. Pasirinkite esančią šalies sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujos šalies sąranką.
3. Naujosios politikos antraštėje, nustatykite šias vertes:

    | Laukas | Aprašymas |
    |---|---|
    | Prekės numeris | Pasirinkite elemento gaminio numerį. |
    | Paskirties šalis | Pasirinkite šalį, į kurią siunčiate gaminį. |
    | Kilmės šalis | Pasirinkite šalį, iš kurios siunčiate gaminį. |

Šios sąrankos tikslas yra padėti jums sukurti medžiagų sąskaitos (BOM) ataskaitą, į kurią galite įtraukti kilmės šalį kiekvienai daliai, kuriai yra nustatytas šaltinis ir paskirties šalis. Ši sąskaita padės jums gauti bendrą paveikslėlį, kuriame matysite, iš kur ateina jūsų dalys ir kur jos eina.

## <a name="keep-track-of-vendor-certificates"></a>Sekite pardavėjų sertifikatus

Galite naudoti **Kilmės šalies pardavėjo sertifikatų** puslapį tam, kad sektumėte sertifikatus, kuriuos išduodate pardavėjams.

Privalote nuspręsti, kuriuos sertifikato dokumentus išduodate ir kaip apie juos pranešite klientams. Ši funkcija padeda jums sekti jūsų sertifikatus. Ji taip pat padeda jums pasirinkti, ar atitinkami sertifikato numeriai bus rodomi sąskaitose, pakavimo lapeliuose ir (arba) užsakymo patvirtinimuose.

Sertifikato informacijos nustatymui, atlikite šiuos žingsnius.

1. Eikite į **Gaminio informacijas tvarkymas \> Sąranka \> Gaminio atitiktis \> Kilmės šalis \> Pardavėjo kilmės šalies sertifikatai**.
2. Pasirinkite esančią sertifikato sąranką redagavimui arba pasirinkite **Naujas** veiksmų juostoje, kad sukurtumėte naujo sertifikato sąranką.
3. Naujam ar pasirinktam sertifikatui nustatykite šiuose nustatymus.

    | Laukas | aprašymas |
    |---|---|
    | Tiekėjo kodas | Pasirinkite pardavėją, kuriam išdavėte sertifikatą. |
    | Prekės numeris | Pasirinkite elementą, kuriam išdavėte sertifikatą. |
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
1. Veiksmų juostoje, **Inžinierius** skirtuke, **KS** grupėje, pasirinkite **Projektuotojas**.
1. Pasirodžiusiame puslapyje Veiksmų juostoje pasirinkite **BOM \> Spausdinti**.
1. **Medžiagų linijų sąskaitos** teksto lange nustatykite **Paskirties šalies** laukelį į paskirties šalį, kurią norite peržiūrėti savo ataskaitoje.
1. Pasirinkite **Gerai**.

Informaciją pateikianti ataskaita apie kiekvienos dalies kilmės šalį yra sukuriama ir rodoma. Čia pateikiamas ataskaitos pavyzdys.

![Kilmės šalies ataskaita.](media/country-of-origin-report.png "Kilmės šalies ataskaita")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]