---
title: Numerio lentelės žymės spausdinimo įgalinimas
description: Šioje temoje aprašoma, kaip įjungti gabenimo konteinerio serijos kodo (SSCC) etiketės automatinį spausdinimą, pardavimo paėmimo darbo procese paėmus paskutinę prekę iš atsargų.
author: perlynne
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd79abfc1029c4e0ef41d0e9b0f33ff524f50e36b70cf4fa3ed50dcdc4cb7f03
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751677"
---
# <a name="enable-license-plate-label-printing"></a>Numerio lentelės žymės spausdinimo įgalinimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip įjungti gabenimo konteinerio serijos kodo (SSCC) etiketės automatinį spausdinimą, pardavimo paėmimo darbo procese paėmus paskutinę prekę iš atsargų. Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF. Jei ją vykdote naudodami savo duomenis, reikia nustatyti numerio lentelių numeraciją. Prieš pradėdami šią užduotį, turite nustatyti etikečių spausdintuvą. Pasirinkite Organizacijos administravimas > Nustatymas > Tinklo spausdintuvai. Srityje Veiksmas spustelėkite Parinktys ir tada spustelėkite mygtuką Atsisiųsti dokumento kelvados agento diegimo programą. Paleiskite diegimo programą ir prieš tęsdami procedūrą įsitikinkite, kad nustatyta veikiančio tinklo spausdintuvo parinktis Aktyvus.


## <a name="set-up-the-gs1-company-prefix"></a>Nustatyti GS1 įmonės prefiksą
1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Sandėlio valdymo parametrai**.
2. Lauke **GS1 įmonės prefiksas** įveskite 7 savo GS1 įmonės kodo skaitmenis.
3. Pasirinkite **Įrašyti**.
4. Uždarykite puslapį.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Nustatyti SSCC numerio lentelės numeraciją
1. Eikite į **naršymo sritį > Moduliai > Organizacijos administravimas > Numeracija > Numeracija**.
2. Lauke **Sritis** pažymėkite parinktį.
3. Lauke **Nuoroda** pažymėkite parinktį.
4. Lauke **Įmonė** įveskite reikšmę.
5. Išplėskite skyrių **Segmentai**.
6. Pasirinkite **Redaguoti**.
7. Lentelėje **Segmentai** pasirinkite pirmą eilutę
8. Pasirinkite **Šalinti**.
9. Pasirinkite **Šalinti**.
10. Pasirinkite **Įrašyti**.
11. Uždarykite puslapį.

## <a name="create-the-document-route-layout"></a>Kurti dokumento maršruto maketą
1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Dokumento maršruto planavimas > Dokumento maršruto planavimo maketai**. Įgalinti SSCC maketą.  
2. Pasirinkite **Naujas**.
3. Lauke **Maketo ID** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Pasirinkite **Įterpti teksto pabaigoje**.
6. Pasirinkite **Įrašyti**.
7. Uždarykite puslapį.

## <a name="set-up-the-document-routing"></a>Nustatyti dokumentų maršruto planavimą
1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Dokumento maršruto planavimas > Dokumento maršruto planavimas**.
2. Lauke **Darbo užsakymo tipas** pažymėkite parinktį.
3. Pasirinkite **Naujas**.
4. Lauke **Sandėlis** įveskite reikšmę.
5. Lauke **Pavadinimas** įveskite reikšmę.
6. Pasirinkite **Naujas**.
7. Lauke **Maketo ID** įveskite arba pasirinkite reikšmę.
8. Lauke **Pavadinimas** įveskite norimą naudoti spausdintuvo pavadinimą.
9. Pasirinkite **Įrašyti**.
10. Uždarykite puslapį.

## <a name="create-mobile-device-menu"></a>Kurti mobiliojo įrenginio meniu
1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai**.
2. Pasirinkite **Naujas**.
3. Lauke **Meniu elemento pavadinimas** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Režimas** pažymėkite parinktį.
6. Pasirinkite **Taip** lauke **Naudoti esamą darbą**.
7. Pasirinkite **Taip** lauke **Generuoti numerio lentelę**.
8. Išplėskite sekciją **Darbo klasės**.
9. Pasirinkite **Naujas**.
10. Lauke **Darbo klasės ID** įveskite reikšmę.
11. Pasirinkite **Įrašyti**.
12. Uždarykite puslapį.
13. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu**.
14. Medyje pasirinkite anksčiau sukurtą meniu elementą.
15. Pasirinkite **Redaguoti**.
16. Pasirinkę rodyklę, įtraukite meniu elementą į meniu.
17. Pasirinkite **Įrašyti**.
18. Uždarykite puslapį.

## <a name="update-a-work-template"></a>Naujinti darbo šabloną
1. Eikite į **Naršymo sritis > Moduliai > Sandėlio valdymas > Sąranka > Darbas > Darbo šablonai**.
2. Pasirinkite **Redaguoti**.
3. Pasirinkite **Naujas**.
4. Lauke **Darbo tipas** pasirinkite **Spausdinti**.
5. Lauke **Darbo klasės ID** įveskite arba pasirinkite reikšmę.
6. Pasirinkite **Perkelti aukštyn**.
7. Pasirinkite **Įrašyti**.
8. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]