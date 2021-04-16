---
title: ER dokumentų valdymo failų naudojimas formato išvestyse (3 dalis – formato kūrimas)
description: Šioje temoje aprašoma, kaip sukonfigūruoti elektroninių ataskaitų formatą, kad būtų galima naudoti dokumentų valdymo failus ER išvestyje. (3 dalis)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99a286b4e40ddeb7f4ff37c1ece3c678b26c838b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755015"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER dokumentų valdymo failų naudojimas formato išvestyse (3 dalis – formato kūrimas)

[!include [banner](../../includes/banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: dokumentų valdymo failų naudojimas formato išvestyse (2 dalis. Duomenų modelio išplėtimas)“.

Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]