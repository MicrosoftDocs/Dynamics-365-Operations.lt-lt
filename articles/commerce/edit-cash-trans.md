---
title: Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas
description: Šioje temoje aprašoma, kaip redaguoti ir tikrinti atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijas „Microsoft Dynamics 365 Commerce“.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: c809f379dbd6824542d0b1768cfbf44f37461f4c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010204"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a>Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip redaguoti ir tikrinti atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijas „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Apžvalga

„Dynamics 365 Commerce” klientai naudoja tiek pirmosios šalies elektroninio kasos aparato (EKA) programą, tiek trečiosios šalies EKA programas. Naudojant pirmosios šalies programą, parduotuvės operacijos iš kanalų perkeliamos į „Commerce“ būstinę atliekant paketinį vykdymą. Naudojant trečiosios šalies programas, operacijos perkeliamos į „Commerce“ būstinę integravimo būdu. Abiem atvejais perkėlus operacijas į „Commerce“ būstinę reikia atlikti vientisumo patikrą. Šio proceso metu atliekami keli operacijų tikrinimai ir tik sėkmingai patikrintos operacijos įtraukiamos į išrašą, kad jos galėtų būti užregistruotos „Commerce“ būstinėje.

Patikrinus „Commerce“ operacijos galėjo būti pripažintos netinkamomis dėl įvairių priežasčių. Nenuoseklius duomenis galėjo nulemti klaida integravimo kode arba EKA programoje. Arba nenuoseklius duomenis galėjo nulemti vartotojo klaida. Pavyzdžiui, vartotojas panaikina produktą po to, kai jis buvo sinchronizuotas su kanalu, arba vartotojas uždaro ataskaitinį laikotarpį neužregistruodamas to laikotarpio operacijų. Nors šios operacijos yra pažymimos ir neįtraukiamos į išrašus, jos gali sutrikdyti kliento kasdienį pardavimo registravimo finansų išrašuose procesą. Programoje „Commerce” galite redaguoti operacijas, kurios jas patikrinus pripažįstamos netinkamomis, išlaikydami visų pakeitimų auditą.

## <a name="edit-transactions"></a>Operacijų redagavimas

„Commerce” 10.0.5 versijoje atsiskaitymo grynaisiais operacijos, pvz., pardavimas ir grąžinimas, yra vienintelės operacijos, kurias galima redaguoti. Kliento užsakymų ir internetinių užsakymų redaguoti negalima. „Commerce“ 10.0.6 ir naujesnėse versijose taip pat galima redaguoti grynųjų pinigų valdymo operacijas.

Norėdami redaguoti operacijas „Commerce“ būstinėje, atlikite nurodytus veiksmus.

1. Įdiekite [„Microsoft Dynamics Office Add-in“](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. „Commerce“ būstinėje atidarykite darbo sritį **Parduotuvės finansai**. Plytelėje **Operacijų tikrinimo klaidos** pateikiamas iš anksto filtruotas operacijų puslapio rodinys, kuriame pateikiami įrašai, neatitikę vienos ar daugiau tikrinimo taisyklių.
1. Atidarykite operacijų puslapį, pasirinkite įrašą, kuris patikrinus pripažintas netinkamu, pasirinkite **„Office“ papildinys** ir pasirinkite **Redaguoti pasirinktą operaciją**. Atidaromas „Excel“ failas, kuriame rodoma išsami pasirinktos operacijos informacija. Į šį failą įtraukti toliau pateikiami darbalapiai:

    - **Eilutės** – šiame darbalapyje pateikiama operacijos antraštė, produkto eilutės ir su operacija susiję duomenys.
    - **Mokėjimai** – šiame darbalapyje pateikiama išsami informacija apie operacijos mokėjimo eilutes.
    - **Nuolaidos** – šiame darbalapyje pateikiama su nuolaidomis susijusi informacija apie operaciją.
    - **Mokesčiai** – šiame darbalapyje pateikiama su mokesčiais susijusi informacija apie operaciją.
    - **Išlaidos** – šiame darbalapyje pateikiami su išlaidomis susiję duomenys apie operaciją.

1. „Excel” faile modifikuokite atitinkamus laukus ir tada įkelkite duomenis atgal į „Commerce“ būstinę naudodami „Dynamics Excel“ papildinio publikavimo funkciją. Publikavus duomenis, pakeitimai bus rodomi sistemoje. Publikuojant, vartotojo atlikti keitimai netikrinami.
1. Visą keitimų įrašų seką galima peržiūrėti pasirinkus **Peržiūrėti įrašo sekimą** antraštėje **Mažmeninės prekybos operacijos** (antraštės lygmens keitimai) ir atitinkamame skyriuje bei operacijų puslapio įraše. Pavyzdžiui, visi su pardavimo eilutėmis susiję pakeitimai bus rodomi puslapyje **Pardavimo operacijos**, o visi su mokėjimais susiję pakeitimai – puslapyje **Mokėjimo operacijos**. Pakeitimams palaikoma toliau pateikiama išsami audito informacija:

    - Pakeitimo data ir laikas
    - Laukas
    - Sena vertė
    - Nauja vertė
    - Modifikavo

1. Atlikę ir publikavę keitimus vykdykite parinktį **Patvirtinti parduotuvės operacijas**, kad patvirtintumėte, jog tie keitimai yra nuoseklūs ir tinkami.

> [!NOTE]
> Galite redaguoti tik tas operacijas, kurios patikrinus pripažintos netinkamomis. Jei norite redaguoti operaciją, kuri patikrinus pripažinta tinkama, operacijos tikrinimo būseną pakeiskite į **Klaida** arba **Nėra** ir tada publikuokite keitimą. Tada galite redaguoti antraštėje arba bet kuriuose kituose antriniuose operacijos įrašuose esančius duomenis ir publikuoti antraštę arba įrašus.

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a>Masinis operacijų, susietų su išrašu, redagavimas

„Commerce” 10.0.6 ir naujesnėse versijose palaikoma masinio operacijų redagavimo išrašo lygiu parinktis.

Norėdami masiškai redaguoti operacijas, susietas su išrašu „Commerce“ būstinėje, atlikite nurodytus veiksmus.

1. Atidarykite puslapį **Išrašai** ir pasirinkti išrašą, kuriame yra redaguotinos operacijos.
1. Pasirinkite mygtuką **Atidaryti naudojant „Microsoft Office“**.
1. Atsižvelgdami į tai, ką reikia redaguoti, pasirinkite vieną iš šių parinkčių:

    - **Redaguoti atsiskaitymo grynaisiais operacijas** – ši parinktis leidžia redaguoti visas atsiskaitymo grynaisiais operacijas, įtrauktas į išrašą. Prieinami šie „Excel” darbalapiai:

        - **Operacija** – šiame darbalapyje pateikiama visa pardavimo operacijų antraštės lygio informacija.
        - **Pardavimo operacija** – šiame darbalapyje pateikiama visa pardavimo operacijų eilutės lygio informacija.
        - **Mokėjimo operacijos** – šiame darbalapyje pateikiama visa pardavimo operacijų mokėjimo eilutės lygio informacija.
        - **Nuolaidų operacijos** – šiame darbalapyje pateikiama visa pardavimo operacijų nuolaidų eilutės lygio informacija.
        - **Mokesčių operacijos** – šiame darbalapyje pateikiama visa pardavimo operacijų mokesčių eilutės informacija.
        - **Išlaidų operacijos** – šiame darbalapyje pateikiama visa pardavimo operacijų išlaidų eilutės lygio informacija.

    - **Redaguoti grynųjų pinigų valdymo operacijas** – ši parinktis leidžia redaguoti visas grynųjų pinigų valdymo operacijas, įtrauktas į išrašą. Prieinami šie „Excel” darbalapiai:

        - **Operacija** – šiame darbalapyje pateikiama visa grynųjų pinigų valdymo operacijų antraštės lygio informacija.
        - **Bankinio mokėjimo priemonių operacijos** – šiame darbalapyje pateikiama visa informacija apie inkasavimo operacijas.
        - **Kasos mokėjimo priemonių operacijos** – šiame darbalapyje pateikiama visa informacija apie įnešimo į įmonės kasą operacijas.
        - **Mokėjimo priemonių deklaravimas** – šiame darbalapyje pateikiama visa informacija apie mokėjimo priemonių deklaravimo operacijas.
        - **Pajamų ir išlaidų operacija** – šiame darbalapyje pateikiama visa informacija apie pajamų ir išlaidų operacijų eilutes.
        - **Mokėjimo operacijos** – šiame darbalapyje pateikiama visa su mokėjimais susijusi operacijos **Apmokėti sąskaitą faktūrą** ir pajamų bei išlaidų operacijų informacija.

1. Redaguokite reikiamas operacijas.

    > [!NOTE]
    > Publikuojant masiškai redaguotas operacijas, tikrinimai nevykdomi. Turite užtikrinti, kad jūsų atlikti redagavimai ir darbalapiuose esantys duomenys yra tikslūs. Pavyzdžiui, jei norite pakeisti operacijos datą, kad galėtumėte valdyti scenarijus, kai atvirų operacijų ataskaitinis arba atsargų laikotarpis yra uždarytas, turite pakeisti datą visuose „Excel” darbalapiuose, kuriuose yra stulpelis **Verslo data**. Jei atlikę redagavimą norite operacijas patikrinti, galite pasirinkti parinktį **Pakartotinai tikrinti operaciją**, esančią puslapyje **Išrašai**. Prieš registruodami išrašą palaukite, kol tikrinimo užduotis bus baigta vykdyti.

1. Jei telkimas jau sugeneruotas, atidarykite puslapį **Sutelktos operacijos** ir pasirinkite **Iš naujo generuoti pardavimo užsakymo xml**.

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a>Masinis operacijų, nesusietų su išrašu, redagavimas

„Commerce“ 10.0.10 ir naujesnės versijos palaiko parinktį masiškai redaguoti operacijas, kurios patikrinus pripažįstamos netinkamomis, bet nėra susietos su išrašu.

Norėdami masiškai redaguoti operacijas, nesusietas su išrašu „Commerce“ būstinėje, atlikite nurodytus veiksmus.

1. Atidarykite puslapį **Visos parduotuvės** ir pasirinkti parduotuvę, kurios operacijos turi būti suredaguotos.
1. Pasirinkite mygtuką **Atidaryti naudojant „Microsoft Office“** ir tada pasirinkite **Redaguoti atsiskaitymo grynaisiais operacijas**.
1. Redaguokite reikalingas operacijos ir tada publikuokite jas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas](edit-order-trans.md)

[Mažmeninės prekybos operacijų finansinių dimensijų redagavimas](edit-financial-dim.md)

[„Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas](create-excel-edit.md)

[Laukų įtraukimas į „Excel“ darbaknygę norint redaguoti mažmeninės prekybos operacijas](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]