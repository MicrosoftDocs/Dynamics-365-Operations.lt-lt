--- 
title: "Duomenų modelio, skirto dokumentų valdymo failams naudoti ER išvestyje, išplėtimas"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8363dd2af728577175a620d7b645d90cea84803a
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="extend-data-models-to-use-document-management-files-in-er-output"></a>Duomenų modelio, skirto dokumentų valdymo failams naudoti ER išvestyje, išplėtimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas dokumentų valdymo failus (priedus) naudoti ER išvestyje. Šiuos veiksmus galima atlikti bet kurioje įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus užduočių vedlyje „ER: dokumentų valdymo failų naudojimas formato išvestyse (1 dalis: duomenų modelio ruošimas)“.

Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Duomenų modelio išplėtimas, kad jame būtų pateikti dokumentų valdymo failai
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Ataskaitų konfigūracijos.
3. Medyje išplėskite Kliento SF modelis.
4. Medyje pasirinkite dalį Customer invoice model\Customer invoice model (custom).
5. Spustelėkite Konstruktorius.
6. Medyje pasirinkite Customer invoice(InvoiceCustomer).
    * Išplėsime šį duomenų modelį, kad jame būtų rodomi visi failai, pridėti prie pardavimo užsakymo, kuris yra susijęs su elektroniniu būdu apdorojama SF.  
7. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
8. Lauke Pavadinimas, įveskite SF priedai.
    * SF priedai  
9. Lauke „Prekės tipas“ pasirinkite „Įrašų sąrašas“.
10. Spustelėkite Pridėti.
11. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
12. Lauke Pavadinimas įveskite Failo turinys.
    * Failo turinys  
13. Lauke Prekės tipas pasirinkite Konteineris.
14. Spustelėkite Pridėti.
15. Spustelėdami Naujas atidarykite išplečiamąjį dialogo langą.
16. Lauke Pavadinimas įveskite Failo vardas.
    * Failo vardas  
17. Lauke „Prekės tipas“ pasirinkite „Eilutė“.
18. Spustelėkite Pridėti.

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a>Naujų duomenų modelio elementų susiejimas su „Dynamics 365 for Finance and Operations“ duomenų šaltiniais
1. Spustelėkite „Susieti modelį su duomenų šaltiniu“.
2. Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Aprašas pagal reikšmę InvoiceCustomer.
    * InvoiceCustomer  
    * Susiesime naujo modelio elementus su tinkamais duomenų šaltiniais.  
3. Spustelėkite Konstruktorius.
4. Medyje pasirinkite SF priedai.
5. Medyje išplėskite SF priedai.
6. Medyje pasirinkite Invoice attachments\File name.
7. Spustelėkite Redaguoti.
8. Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Spustelėkite Įrašyti.
10. Uždarykite puslapį.
11. Medyje pasirinkite Invoice attachments\File content.
12. Spustelėkite Redaguoti.
13. Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.
16. Medyje pasirinkite SF priedai.
17. Spustelėkite Redaguoti.
18. Lauke Formulė įveskite CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Spustelėkite Įrašyti.
20. Uždarykite puslapį.
21. Spustelėkite Įrašyti.
22. Uždarykite puslapį.
23. Uždarykite puslapį.
24. Uždarykite puslapį.
25. Spustelėkite keisti būseną.
26. Spustelėkite Baigti.
27. Spustelėkite GERAI.


