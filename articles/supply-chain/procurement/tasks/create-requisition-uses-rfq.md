---
title: Paraiškos, kurioje naudojamas RFQ, kūrimas
description: Šioje temoje aiškinama, kaip įtraukti kainos ir tiekėjo informaciją į pirkimo paraišką iš RFQ proceso.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05ff98b5fd95fa345d344e54d9116c73434e5de5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018901"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Paraiškos, kurioje naudojamas RFQ, kūrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip įtraukti kainos ir tiekėjo informaciją į pirkimo paraišką iš RFQ proceso. Šiame vedlyje pateiktą pavyzdį galite naudoti demonstracinių duomenų įmonėje USMF, o norėdami atlikti visus veiksmus turite būti prisijungęs kaip Administratorius. Paprastai šio vedlio užduotis atlieka įsigijimo specialistai.


## <a name="create-a-requisition"></a>Kurti paraišką
1. Naršymo srityje eikite į **Moduliai > Įsigijimas ir išteklių paskirstymas > Pirkimo paraiškos > Mano parengtos pirkimo paraiškos**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite reikšmę.
4. Lauke **Pageidaujama data** įveskite datą.
5. Lauke **Apskaitos data** įveskite datą.
6. Pasirinkite **Gerai**.
7. Lauke **Priežastis** įveskite arba pažymėkite reikšmę.
8. Pasirinkite **Pridėti eilutę**.
9. Lauke **Įsigijimo kategorija** pažymėkite kategoriją medyje, tada pažymėkite **Gerai**.
10. Lauke **Produkto pavadinimas** įveskite vertę.
11. Lauke **Kiekis** įveskite skaičių.
12. Lauke **Vienetas** įveskite arba pasirinkite reikšmę.
13. Pasirinkite **Įrašyti**.
14. Pasirinkite **Darbo eiga**, kad atidarytumėte išplečiamąjį dialogo langą.
15. Pasirinkite **Pateikti**.
16. Uždarykite puslapį.
17. Pasirinkite **Pateikti**.

## <a name="reassign-a-workflow-task"></a>Iš naujo priskirti darbo eigos užduotį
Kitos užduoties metu kuriamas RFQ, siekiant gauti tiekėjų kainų pasiūlymus už produktą. USMF demonstraciniuose duomenyse paraiškos darbo eiga nustatoma naudojant taisyklę, pagal kurią RFQ kūrimo užduotis priskiriama konkrečiam darbuotojui, jei nėra pasirinktas tiekėjas arba jei eilutės vieneto kaina yra 0. Norėdami toliau vykdyti šio vedlio užduotis, tą užduotį turite priskirti kitam vartotojui (sau). Tai galite atlikti tik jei esate prisijungęs kaip Administratorius.  

1. Pasirinkite **Darbo eiga**, kad atidarytumėte išplečiamąjį dialogo langą.
2. Pažymėkite **Žiūrėti istoriją**.
3. Atnaujinkite puslapį.
4. Išplėskite skyrių **Sekimo išsami informacija**.
5. Medyje pažymėkite eilutę, kuri prasideda „Eilutės darbo eiga suaktyvinta“.
6. Pažymėkite **Žiūrėti darbo eigos išsamią informaciją**.
7. Išplėskite skyrių **Darbo elementai**.
8. Pažymėkite **Priskirti iš naujo**.
9. Lauke **Vartotojas** pažymėkite **Administratorius**.
10. Pažymėkite **Priskirti iš naujo**.
11. Uždarykite du puslapius.

## <a name="create-an-rfq"></a>Kurti RFQ

1. Atnaujinkite puslapį.
2. Pažymėkite **Prašyti kainos**.
3. Lauke **Juridinio asmens pirkimas** pažymėkite **USMF**. Turite pasirinkti tokį patį juridinį subjektą, koks nurodytas paraiškos eilutėje.  
4. Sąraše pažymėkite pasirinktą eilutę. Jei pirkimo paraiškoje yra kelios eilutės, pasirinkite visas eilutes, kurias norite įtraukti į RFQ.  
5. Pasirinkite **Gerai**.
6. Atnaujinkite puslapį.
7. Įsitikinkite, kad „FactBox“ yra atidarytas, tada išplėskite skyrių **Susiję dokumentai**.
8. Pažymėkite saitą lauke **Prašyti kainos**, kad atidarytumėte ką tik sukurtą RFQ.
9. Pažymėkite **Antraštė**.
10. Pasirinkite **Įtraukti**.
11. Lauke **Tiekėjo paskyra** įveskite arba pasirinkite reikšmę.
12. Pasirinkite **Įtraukti**.
13. Lauke **Tiekėjo paskyra** įveskite arba pasirinkite reikšmę.
14. Pažymėkite **Siųsti**.
15. Pasirinkite **Gerai**.
16. Pažymėkite **Įvesti atsakymą**.
17. Veiksmų srityje pasirinkite **Atsakymas**.
18. Pažymėkite **Kopijuoti duomenis į atsakymą**. Tokiu būdu iš RFQ į atsakymą nukopijuojami duomenys, pvz., kiekis ir datos.  
19. Lauke **Vieneto kaina** įveskite skaičių. Tai yra kaina, gauta iš tiekėjo. Galbūt taip pat norėsite įvesti papildomą tiekėjo informaciją.  
20. Pasirinkite **Patvirtinti**.
21. Pasirinkite **Gerai**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Patikrinti, ar tiekėjas ir kaina perkelti į paraišką
1. Uždarykite puslapį.
2. Pasirinkite **Eilutės**.
3. Pažymėkite **Susijusi informacija**.
4. Pažymėkite **Pirkimo paraiška**.
5. Pasirinkite eilutę, kuri buvo perkelta į RFQ. Patikrinkite, ar kaina ir tiekėjas nukopijuoti į paraišką.  
6. Pasirinkite **Darbo eiga**, kad atidarytumėte išplečiamąjį dialogo langą.
7. Pasirinkite Baigti.
8. Pasirinkite puslapį.
9. Pasirinkite Baigti.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]