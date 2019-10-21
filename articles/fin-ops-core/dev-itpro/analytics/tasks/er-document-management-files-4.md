---
title: Formato, skirto dokumentų valdymo failams naudoti ER išvestyje, taikymas
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų formatą, norėdamas dokumentų valdymo failus naudoti ER išvestyje.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8dc541af4d26b61ff9b90e08a8ca2c6a6bb8e70
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185019"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4-run-format"></a>ER: dokumentų valdymo failų naudojimas formato išvestyse (4 dalis: formato paleidimas)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (3 dalis: formato kūrimas)“.

Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Pridėkite reikiamus vienos SF pardavimo užsakymo priedus
1. Pasirinkite Gautinos sumos > Sąskaitos faktūros > Atidarytos klientų SF.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką SF reikšme CIV-000148.
    * CIV-000148  
3. Spustelėkite norėdami sekti pažymėtos SF saitą.
    * CIV-000148  
4. Spustelėkite, jei norite atidaryti lauke Pardavimo užsakymas esantį saitą.
    * 000148  
5. Lauke Eilutės arba antraštė pasirinkite parinktį Antraštė.
    * Pasirinkite Antraštė, norėdami nurodyti, kad tai bus priedų pridėjimo paskirties vieta.  
6. Spustelėkite Pridėti.
    * Įtraukite kelis failus kaip šio pardavimo užsakymo priedus. Naudokite dokumentų tipų, kuriuos palaiko dokumentų valdymas, failus (su failų plėtiniais DOCX, DPF, XML, JPG, ir pan.). Naršykite ir pasirinkite failus, kuriuos norite pridėti ir apdoroti su susijusia SF ER el. laiške.  
7. Spustelėkite Naujas.
8. Spustelėkite Failas.
9. Spustelėkite Naujas.
10. Spustelėkite Failas.
11. Uždarykite puslapį.
12. Uždarykite puslapį.
13. Uždarykite puslapį.
14. Uždarykite puslapį.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Paleiskite sukurtą pasirinktos SF ataskaitą
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite Kliento SF modelis.
3. Medyje išplėskite dalį Kliento SF modelis / kliento SF modelis (pasirinktinis).
4. Medyje pasirinkite Kliento SF modelis / kliento SF modelis (pasirinktinis) / elektroninės SF pranešimo pavyzdys.
5. Spustelėkite Vykdyti.
6. Išplėskite dalį Įtrauktini įrašai ().
7. Spustelėkite Filtras.
8. Pasirinkite kliento SF žurnalo eilutę ir lauką Pardavimo užsakymas.
9. Lauke Kriterijai įveskite 000148.
    * Kriterijų lauke Pardavimo užsakymas įveskite užsakymo numerį 000148.  
10. Spustelėkite GERAI.
11. Spustelėkite GERAI.
    * Peržiūrėkite sugeneruotą išvestį. Atkreipkite dėmesį, kad kiekvienam priedui sukuriamas vienas XML mazgas. Priedo turinys įvedamas į XML išvestį MIME (base64) teksto formatu.  
