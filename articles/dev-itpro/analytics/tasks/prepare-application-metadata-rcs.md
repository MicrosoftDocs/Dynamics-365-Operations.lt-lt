---
title: Programos metaduomenų, kurie bus naudojami RCS, parengimas
description: Šios temos veiksmai paaiškina, kaip vartotojas gali kurti naują elektroninės ataskaitos (ER) konfigūraciją, kurioje yra programos „Finance and Operations“ metaduomenys, skirti ER modelio susiejimo konfigūracijoms kurti naudojant „Regulatory Configuration Service“ (RCS).
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1bd2298240fa789762a350e90888201c5a7ce45
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726988"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Programos metaduomenų, kurie bus naudojami RCS, parengimas
[!include [task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodyti veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigas einantis vartotojas gali kurti naują elektroninės ataskaitos (ER) konfigūraciją, kurioje yra „Microsoft Dynamics 365 for Finance and Operations“ programos metaduomenys, skirti ER modelio susiejimo konfigūracijoms kurti naudojant „Regulatory configuration service“ (RCS). Naudojantis šia konfigūracija sukuriamas ER modelio susiejimo konfigūracijos, naudojamos norint pasiekti užsienio prekybos operacijas, pavyzdys. Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Šiuos veiksmus galima atlikti bet kurioje įmonėje. Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md).

## <a name="prerequisites"></a>Būtinieji komponentai
1.  Eikite į **Organizacijos administravimas** > **Darbo sritys** > **Elektroninės ataskaitos**. 
2.  Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) veiksmus. 
3.  Spustelėkite **Metaduomenų konfigūracijos**. 
4.  Tarkime, kad naudojantis RCS sukuriamas programai „Finance and Operations“ skirtas sprendimas, kuris generuoja elektroninius dokumentus, kuriuose pateikiama informacija iš užsienio prekybos verslo srities. Norint susieti ER duomenų modelį su reikiamų duomenų šaltiniais, naudojantis RCS reikia turėti prieigą prie programos „Finance and Operations“ metaduomenų. Todėl, norėdami sukurti ER sprendimą, mes sukonfigūruojame naują ER metaduomenų konfigūraciją, kurioje yra visi metaduomenys, kurių šiuo metu reikia generuojant pasirinktos verslo srities ER ataskaitas. 

## <a name="add-metadata-configuration"></a>Metaduomenų konfigūracijos įtraukimas 
1.  Spustelėdami **Kurti konfigūraciją**, atidarykite išplečiamąjį dialogo langą. 
2.  Lauke **Pavadinimas** įveskite „Užsienio prekybos metaduomenys“. 
3.  Spustelėkite **Sukurti konfigūraciją**. 
4.  Spustelėkite **Konstruktorius**. 
5.  Spustelėkite **Pridėti**. 
  
> [!NOTE]
> Galite pasirinkti visus metaduomenis, skirtus visai programai arba pasirinktiems modeliams ar moduliams. Atminkite, kad šiuo atveju šie metaduomenys bus įtraukti automatiškai: įrašų lentelės, išvardijimai ir išplėstiniai duomenų tipai. Jei reikia papildomų metaduomenų tipų, juos reikia įtraukti rankiniu būdu. 
 
Siūlome tam tikrų su užsienio prekybos operacijomis susijusių metaduomenų, kai metaduomenų elementai pasirenkami rankiniu būdu. 
  
6.  Spustelėkite **Įtraukti duomenų šaltinį**. 
7.  Spustelėkite **Lentelės įrašai**. 
8.  Naudokite spartųjį filtrą, kad atfiltruotumėte lauką **Pavadinimas** pagal reikšmę „Intrastat“. 
9.  Pasirinkite **Intrastat** lentelės įrašą. 
10. Spustelėkite **Gerai**.
  
Įtraukėme metaduomenų informaciją apie „Intrastat“ įrašų lentelę. 
  
11. Medyje išplėskite **Lentelės įrašai „Intrastat“**\>**Ryšiai**. 
12. Medyje pasirinkite **Lentelės įrašai „Intrastat“**\>**Ryšiai\IntrastatCommodity (lentelės įrašai EcoResCategory)**.   
13. Spustelėkite **Įtraukti metaduomenis**. 
  
> [!NOTE]
> Metaduomenis apie reikalingus ryšius, skirtus pasirinktai įrašų lentelei, reikia įtraukti rankiniu būdu. 
  
16. Spustelėkite **Įtraukti duomenų šaltinį**. 
17. Spustelėkite **Išvardijimas**. 
18. Naudokite spartųjį filtrą, kad atfiltruotumėte lauką **Pavadinimas** pagal reikšmę „IntrastatDirection“. 
19. Pasirinkite įrašą **IntrastatDirection išvardijimas**. 
20. Spustelėkite **Gerai**. 
21. Spustelėkite **Įrašyti**.  
22. Uždarykite puslapį. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Metaduomenų konfigūracijos juodraštinės versijos užpildymas
1.  Spustelėkite **Keisti būseną**. 
2.  Spustelėkite **Baigta**. 
3.  Spustelėkite **Gerai**. 
4.  Pasirinkite baigtą versiją **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Baigtos metaduomenų konfigūracijos versijos eksportavimas iš programos XML formatu
1.  Spustelėkite **Keitimas**. 
2.  Spustelėkite **Eksportuoti kaip XML failą**. 
3.  Spustelėkite **Gerai**. 
    
Sukurta ERA metaduomenų konfigūracija įrašyta kaip XML failas, kurį galima importuoti į RCS ir naudoti „Finance and Operations“ kaip užsienio prekybos verslo srities metaduomenų šaltinį. Remdamiesi šia informacija, galime nurodyti susiejimą tarp programos metaduomenų ir ER duomenų modelio.
