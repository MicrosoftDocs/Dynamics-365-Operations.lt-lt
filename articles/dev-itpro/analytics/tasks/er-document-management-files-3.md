--- 
title: "Formato, kuris bus naudojamas dokumentų valdymo failuose naudojant formato išvestis, kūrimas"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: 6d5df842dbbf89f5df72c63919fc0bcbf811a09c
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-format-to-use-document-management-files-in-format-outputs"></a>Formato, kuris bus naudojamas dokumentų valdymo failuose naudojant formato išvestis, kūrimas

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (2 dalis: duomenų modelio išplėtimas)“.

Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="create-a-format-to-process-invoices"></a>Formato, skirto SF apdoroti, kūrimas
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Ataskaitų konfigūracijos.
3. Medyje išplėskite Kliento SF modelis.
4. Medyje pasirinkite dalį Customer invoice model\Customer invoice model (custom).
    * Sukursite formatą, kurį naudojant būtų generuojami el. laiškai su informacija apie visus failus, pridėtus prie pardavimo užsakymo, susijusio su elektroniniu būdu apdorojama SF.  
5. Spustelėdami Kurti konfigūraciją, atidarykite išplečiamąjį dialogo langą.
6. Lauke Naujas įveskite Formatas pagal duomenų modelį Kliento SF modelis (pasirinktinis).
7. Lauke Pavadinimas įveskite Elektroninės SF pranešimo pavyzdys.
    * Elektroninės SF pranešimo pavyzdys  
8. Lauke Duomenų modelio aprašas įveskite arba pasirinkite reikšmę.
    * InvoiceCustomer  
9. Spustelėkite Sukurti konfigūraciją.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Kurkite formatą, skirtą priedams į generuojamus pranešimą įvesti MIME formatu
1. Spustelėkite Konstruktorius.
2. Spustelėdami Įtraukti šakninį elementą atidarykite išplečiamąjį dialogo langą.
3. Medyje pasirinkite „XML \ Elementas“.
4. Lauke Pavadinimas įveskite SF.
    * PVM sąskaita faktūra  
5. Spustelėkite GERAI.
6. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
7. Medyje pasirinkite „XML \ Atributas“.
8. Lauke Pavadinimas įveskite SalesOrder.
    * SalesOrder  
9. Spustelėkite GERAI.
10. Spustelėkite Įtraukti atributą.
11. Lauke Pavadinimas įveskite InvoiceNumber.
    * InvoiceNumber  
12. Spustelėkite GERAI.
13. Spustelėkite Įtraukti atributą.
14. Lauke Pavadinimas įveskite InvoiceAmount.
    * InvoiceAmount  
15. Spustelėkite GERAI.
16. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
17. Medyje pasirinkite „XML \ Elementas“.
18. Lauke Pavadinimas įveskite EnclosedDocs.
    * EnclosedDocs  
19. Spustelėkite GERAI.
20. Medyje pasirinkite Invoice\EnclosedDocs.
21. Spustelėkite Įtraukti elementą.
22. Lauke Pavadinimas įveskite Dokumentas.
    * Dokumentas  
23. Spustelėkite GERAI.
24. Medyje pasirinkite Invoice\EnclosedDocs\Document.
25. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
26. Medyje pasirinkite „XML \ Atributas“.
27. Lauke Pavadinimas įveskite FileName.
    * FileName  
28. Spustelėkite GERAI.
29. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
30. Medyje pasirinkite „XML \ Elementas“.
31. Lauke Pavadinimas įveskite FileContent.
    * FileContent  
32. Spustelėkite GERAI.
33. Medyje pasirinkite Invoice\EnclosedDocs\Document\FileContent.
34. Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.
35. Medyje pasirinkite Text\Base64.
36. Spustelėkite GERAI.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Susiekite formato elementus su duomenų modeliu kaip duomenų šaltinį
1. Medyje pasirinkite Invoice\SalesOrder.
2. Spustelėkite skirtuką „Susiejimas“.
3. Medyje išplėskite „modelis‟.
4. Medyje pasirinkite model\Sales order number(SalesId).
5. Spustelėkite Susieti.
6. Medyje pasirinkite Invoice\InvoiceNumber.
7. Medyje išplėskite model\Base invoice(InvoiceBase).
8. Medyje pasirinkite model\Base invoice(InvoiceBase)\Invoice number(Id).
9. Spustelėkite Susieti.
10. Medyje pasirinkite Invoice\InvoiceAmount.
11. Medyje pasirinkite model\Base invoice(InvoiceBase)\Invoice amount(Amount).
12. Spustelėkite Susieti.
13. Medyje išplėskite model\Invoice attachments.
14. Medyje pasirinkite model\Invoice attachments\File content.
15. Medyje pasirinkite Invoice\EnclosedDocs\Document\FileContent\Base64.
16. Spustelėkite Susieti.
17. Medyje pasirinkite model\Invoice attachments\File name.
18. Medyje pasirinkite Invoice\EnclosedDocs\Document\FileName.
19. Spustelėkite Susieti.
20. Medyje pasirinkite model\Invoice attachments.
21. Medyje pasirinkite Invoice\EnclosedDocs\Document.
22. Spustelėkite Susieti.
23. Spustelėkite Įrašyti.
24. Uždarykite puslapį.


