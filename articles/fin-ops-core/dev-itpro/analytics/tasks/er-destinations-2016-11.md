---
title: 'ER: paskirties vietų konfigūravimas'
description: Šia procedūra rodoma, kaip nustatyti ir naudoti skirtingas elektroninių ataskaitų (ER) išvesties komponentų paskirties vietas, pvz., aplanką ar failą.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 78dbcb73b47223ba1fe2ea35ef7c7af09a98d5c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754967"
---
# <a name="er-configure-destinations"></a>ER: paskirties vietų konfigūravimas

[!include [banner](../../includes/banner.md)]

Šia procedūra rodoma, kaip nustatyti ir naudoti skirtingas elektroninių ataskaitų (ER) išvesties komponentų paskirties vietas, pvz., aplanką ar failą. Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF. Juridinio subjekto pagrindinio adreso šalis / regionas yra Vokietija, tačiau, atlikdami šią procedūrą, galite naudoti bet kokį juridinį subjektą. 

Šiame pavyzdyje naudojamas formatas yra ISO20022 Kredito perkėlimas, tačiau galite naudoti bet kokį formatą, kurį jau esate importavę. Atkreipkite dėmesį, kad ši procedūra yra vieno failo ir vienos paskirties vietos nustatymo pavyzdys. Daugiau informacijos apie elektroninių ataskaitų paskirties vietų valdymą galima rasti Dynamics 365 Finance žinyne.

1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Elektroninių ataskaitų paskirties vieta.
2. Spustelėkite Naujas, kad sukurtumėte naują formato paskirties vietų rinkinį.
3. Lauke Nuoroda pasirinkite formatą, kurio paskirties vietas norite konfigūruoti.
    * Jei neturite pasirenkamos reikšmės, tai reiškia, kad nesatę importavę jokių elektroninių ataskaitų formato konfigūracijų. Prieš nustatydami paskirties vietas turite importuoti formato konfigūraciją.  
4. Spustelėkite Nauja, kad sukurtumėte naują failų paskirties vietą.
    * Atkreipkite dėmesį, kad kiekvienam to paties formato išvesties komponentui galite sukurti vieną failų paskirties vietą, pvz., aplanką ar failą. Parametruose galėsite atskirai įjungti ir išjungti paskirties vietas.  
5. Lauke Pavadinimas įveskite patogų išvesties komponento pavadinimą.
    * Rekomenduojame naudoti prasmingus pavadinimus, pvz., „Mokėjimo failas" arba „Kontrolės ataskaita‟. Šie pavadinimai vartotojams bus pateikiami konfigūracijų vykdyklėje, kartu su paskirties vietų parametrais.  
6. Srityje Failo pavadinimas pasirinkite konkretaus formato failą arba aplanką.
7. Spustelėkite Parametrai.
8. Lauke Įjungta pasirinkite Taip.
    * Kiekviename skirtuke esančiu žymės langeliu Įjungta galima atskirai įjungti ir išjungti kiekvieną paskirties vietą. Šiame pavyzdyje įjungsite išvesties failo siuntimo el. pašto gavėjui, kai failas sugeneruojamas, funkciją.  
9. Spustelėkite Redaguoti, norėdami nustatyti el. pašto gavėjus.
10. Spustelėkite Pridėti.
11. Spustelėkite Spausdinimo valdymo el. paštas.
12. Lauke El. pašto šaltinis pasirinkite parinktį.
    * Galite pasirinkti skirtingus el. pašto šaltinio tipus, pvz., kliento arba tiekėjo tipą. Taip nurodomas argumento tipas, kurį pateiks el. pašto šaltinio sąskaitos formulė. El. pašto šaltinio sąskaitos formulėje, aprašytoje tolesniu veiksmu, bus galima susieti el. pašto šaltinį. Jei jūsų formulė pateiks tiekėjo sąskaitą, pasirinkite Tiekėjas. Jei naudojate ISO 20022 kredito perkėlimo konfigūracijos pavyzdį, naudokite Tiekėjas.  
13. Spustelėkite mygtuką El. pašto šaltinio susiejimas.
14. Srityje Formulė įveskite konkretaus dokumento nuorodą į šalies tipą, kurį pasirinkote anksčiau.
    * Užuot rinkę tekstą, galite surasti duomenų šaltinio mazgą, atitinkantį šalies sąskaitą, ir spustelėti mygtuką Įtraukti duomenų šaltinį, kad atnaujintumėte formulę. Pavyzdys: jei naudojate ISO 20022 kredito perkėlimo konfigūraciją, tiekėjo sąskaitą atitinkantis mazgas yra '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID. Priešingu atveju įveskite bet kokią eilutės reikšmę, pvz., „DE-001“, kad įrašytumėte formulę.  
15. Spustelėkite Įrašyti.
16. Uždarykite puslapį.
17. Spustelėkite Redaguoti, norėdami konfigūruoti šalies kontaktinę informaciją.
18. Lauke Pagrindinis kontaktas pasirinkite Taip.
    * Galite naudoti įvairias parinktis, norėdami nurodyti, koks šalies kontakto tipo turi būti naudojamas kaip šios paskirties el. pašto adresas. Šiame pavyzdyje naudojame pirminį kontaktą.  
19. Spustelėkite GERAI.
20. Spustelėkite GERAI.
21. Lauke „Tema“ įveskite reikšmę.
22. Spustelėkite GERAI.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]