--- 
title: "Formato, kuris bus naudojamas dokumentų valdymo failuose naudojant formato išvestis, paleidimas"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 554de60fb8d2b6cb03cac5dc8d01df98390ad844
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="run-format-to-use-document-management-files-in-format-outputs"></a>Formato, kuris bus naudojamas dokumentų valdymo failuose naudojant formato išvestis, paleidimas 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (3 dalis: formato kūrimas)“.

Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


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


