---
title: Redaguoti ir atlikti mažmeninės prekybos parduotuvės operacijų auditą
description: Šioje temoje aprašomos parduotuvės operacijų redagavimo ir audito funkcijos.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004394"
---
# <a name="edit-and-audit-retail-store-transactions"></a>Redaguoti ir atlikti mažmeninės prekybos parduotuvės operacijų auditą

[!include [banner](includes/banner.md)]



„Dynamics 365 Commerce” klientai naudoja pirmosios ir trečiosios šalies elektroninio kasos aparato (EKA) programas. Naudojant pirmosios šalies EKA programą, parduotuvės operacijos iš kanalų perkeliamos į būstinę atliekant paketinį vykdymą. Naudojant trečiosios šalies programas, operacijos perkeliamos į būstinę integravimo būdu. Abiem atvejais perkėlus operacijas į būstinę reikia įvykdyti vientisumo tikrinimo procesą, kurio metu atliekami keli operacijų tikrinimai, kad tik sėkmingai patvirtintos operacijos būtų įtraukiamos į išrašą, kuris bus registruojamas būstinėje. 

Patikrinus prekybos operacijos pripažįstamos netinkamomis dėl įvairių priežasčių. Pavyzdžiui, nenuoseklius duomenis galėjo nulemti klaida integravimo kode arba EKA programoje. Be to, tai gali nulemti ir vartotojo klaida, pvz., panaikintas su kanalu sinchronizuotas produktas arba uždarytas ataskaitinis laikotarpis neužregistravus to laikotarpio operacijų.

Nors šios operacijos yra pažymimos ir neįtraukiamos į išrašus, jos gali sutrikdyti kliento kasdienį pardavimo registravimo finansų išrašuose procesą.

Programoje „Commerce” galite redaguoti konkrečias operacijas, kurios jas patikrinus pripažįstamos netinkamomis, išlaikydami visų pakeitimų auditą. 

## <a name="edit-and-audit-transactions"></a>Redaguoti ir atlikti operacijų auditą

„Retail” versijoje 10.0.5 atsiskaitymo grynaisiais operacijos, pvz., pardavimas ir grąžinimas, yra vienintelės operacijos, kurias galima redaguoti. Kliento užsakymų ir internetinių užsakymų redagavimas nepalaikomas. „Retail” 10.0.6 ir naujesnėse versijose taip pat palaikomas grynųjų pinigų valdymo operacijų redagavimas.

1. Įdiekite „Dynamics Excel” papildinį.

2. Eikite į darbo sritį **Parduotuvės finansai**. Plytelėje **Operacijų tikrinimo klaidos** pateikiamas iš anksto filtruotas operacijų formos rodinys, kuriame pateikiami įrašai, neatitikę vienos ar daugiau tikrinimo taisyklių.
 
3. Atidarykite formą. Spustelėkite įrašą, kuris patikrinus pripažintas netinkamu, spustelėkite **„Office” papildinys**, tada spustelėkite **Redaguoti pasirinktą operaciją**. Atidaromas „Excel” failas, kuriame pateikiama išsami informacija apie pasirinktą operaciją, su šiais darbalapiais:

    - Eilutės: šiame darbalapyje pateikiama antraštė, produkto eilutės ir su operacija susiję duomenys.
    - Mokėjimai: šiame darbalapyje pateikiama išsami informacija apie operacijos mokėjimo eilutes.
    - Nuolaidos: šiame darbalapyje pateikiama su nuolaidomis susijusi informacija apie operaciją.
    - Mokesčiai: šiame darbalapyje pateikiama su mokesčiais susijusi informacija apie operaciją.
    - Išlaidos: šiame darbalapyje pateikiami su išlaidomis susiję duomenys apie operaciją.

4. „Excel” faile turite modifikuoti atitinkamus laukus ir tada įkelti duomenis atgal į būstinę naudodamiesi „Dynamics Excel” papildinio publikavimo funkcija. Publikavus pakeitimai bus rodomi sistemoje. Publikuojant vartotojo padaryti keitimai netikrinami.

5. Visą keitimų įrašų seką galima peržiūrėti spustelėjus **Peržiūrėti įrašo sekimą** antraštėje **Mažmeninės prekybos operacijos** (antraštės lygmens keitimai) ir atitinkamame skyriuje bei operacijų puslapio įraše. Pavyzdžiui, visi pakeitimai, susiję su pardavimo eilutėmis, bus matomi puslapyje **Pardavimo operacijos**, o su mokėjimais susiję pakeitimai bus matomi puslapyje **Mokėjimo operacijos** ir pan. Pakeitimams palaikoma audito informacija yra tokia, kaip pateikta toliau.

   - Pakeitimo data ir laikas
   - Laukas 
   - Sena vertė
   - Nauja vertė
   - Modifikavo

6. Atlikę keitimus ir publikavę dar kartą vykdykite parinktį **Patvirtinti parduotuvės operacijas**, kad patvirtintumėte, jog atlikti keitimai yra nuoseklūs ir tinkami.

> [!NOTE]
> Galite redaguoti tik tas operacijas, kurios neišlaikė patvirtinimo. Jei norite redaguoti operacijas, kurios išlaikė patikrinimą, operacijos, kurią norite pakeisti, būseną pakeiskite į **Klaida** arba **Nėra**, tuomet galėsite ją redaguoti. 


## <a name="bulk-edit-transactions"></a>Masinis operacijų redagavimas

„Retail” 10.0.6 ir naujesnėse versijose palaikoma masinio operacijų redagavimo išrašo lygiu parinktis. 

1. Norėdami atidaryti išrašą, kuriame pateikiamos norimos modifikuoti operacijos, naudokite „Excel” papildinį ir atlikite pirmiau pateiktus 1–3 veiksmus.

2. Pasirinkite vieną iš toliau pateiktų parinkčių.

    - **Redaguoti atsiskaitymo grynaisiais operacijas**. Ši pasirinktis leidžia redaguoti visas atsiskaitymo grynaisiais operacijas, įtrauktas į išrašą. Prieinami šie „Excel” darbalapiai.
    
       - **Operacija**: šiame darbalapyje pateikiama visa pardavimo operacijų antraštės lygio informacija.
       - **Pardavimo operacija**: šiame darbalapyje pateikiama visa pardavimo operacijų eilučių lygio informacija.
       - **Mokėjimo operacijos**: šiame darbalapyje pateikiama visa pardavimo operacijų mokėjimo eilučių lygio informacija.
       - **Nuolaidų operacijos**: šiame darbalapyje pateikiama visa pardavimo operacijų nuolaidų eilučių lygio informacija.
       - **Mokesčių operacijos**: šiame darbalapyje pateikiama visa pardavimo operacijų mokesčių eilučių informacija.
       - **Išlaidų operacijos**: šiame darbalapyje pateikiama visa pardavimo operacijų išlaidų eilučių lygio informacija.

    - **Redaguoti grynųjų pinigų valdymo operacijas**. Ši parinktis leidžia redaguoti visas grynųjų pinigų valdymo operacijas, įtrauktas į išrašą. Prieinami šie „Excel” darbalapiai.
     
       - **Operacija**: šiame darbalapyje pateikiama visa grynųjų pinigų valdymo operacijų antraštės lygio informacija.
       - **Bankinio mokėjimo priemonių operacijos**: šiame darbalapyje pateikiama visa informacija apie inkasavimo operacijas.
       - **Kasos mokėjimo priemonių operacijos**: šiame darbalapyje pateikiama visa informacija apie įnešimo į įmonės kasą operacijas.
       - **Mokėjimo priemonių deklaravimas**: šiame darbalapyje pateikiama visa informacija apie mokėjimo priemonių deklaravimo operacijas.
       - **Pajamų ir išlaidų operacija** – šiame darbalapyje pateikiama visa informacija apie pajamų ir išlaidų operacijų eilutes.
       - **Mokėjimo operacijos** – šiame darbalapyje pateikiama visa su mokėjimais susijusi operacijos **Apmokėti sąskaitą faktūrą** ir pajamų bei išlaidų operacijų informacija.

3.  Publikuojant masinio redagavimo operacijas, tikrinimai nevykdomi. Turite užtikrinti, kad jūsų atliktos redakcijos ir darbalapiuose esantys duomenys yra tikslūs. Pavyzdžiui, jei norite pakeisti operacijos datą, kad galėtumėte valdyti scenarijus, kai atvirų operacijų fiskalinis arba atsargų laikotarpis yra uždarytas, turite pakeisti datą visuose „Excel” darbalapiuose, kuriuose yra stulpelis **Verslo data**. Jei atlikę redakcijas norite operacijas patikrinti, galite naudoti parinktį **Pakartotinai tikrinti operaciją**, esančią puslapyje **Išrašai**.