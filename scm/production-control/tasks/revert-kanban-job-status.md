--- 
title: "Grąžinti „kanban“ užduoties būseną"
description: "Ši procedūra padeda grąžinti neteisingą „kanban“ užduoties būseną."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 00b6ae872e60a322c994420ab69236abef7fb312
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="revert-kanban-job-status"></a>Grąžinti „kanban“ užduoties būseną

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padeda grąžinti neteisingą „kanban“ užduoties būseną. Tai naudinga, jei mašinų operatorius atnaujina neteisingą užduotį arba netyčia nustato neteisingą būseną. Šios procedūros metu „kanban“ užduotis netyčia užregistruojama kaip paruošta ir jos būsena yra grąžinama. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF. Ši procedūra skirta parduotuvės prižiūrėtojui arba mašinų operatoriui, dirbančiam „lean manufacturing“ įmonėje.


## <a name="open-process-board-for-the-work-cell"></a>Atidaryti darbo elemento proceso informacijos sritį
1. Eikite į proceso užduočių „kanban“ sritį.
2. Lauke Darbo elementas įveskite arba pasirinkite reikšmę.
    * Pasirinkite 1260 darbo elementą.  

## <a name="prepare-kanban-job"></a>Paruošti „kanban“ užduotį
1. Spustelėkite „Parengti“.
    * Jei negalite spustelėti Paruošti, nes ši parinktis papilkinta, įsitikinkite, kad pasirinktos „kanban“ užduoties būsena Suplanuota, kurią nurodo tuščia „kanban“ piktograma. Jei parinkties Paruošti funkcija nepavyko, įsitikinkite, kad galima naudoti visas išrinkimo dokumento medžiagas.  
2. Sąraše pasirinkite paruoštą užduotį.
    * Pasirinkite pirmą ką tik paruoštą užduotį.  
    * Atkreipkite dėmesį, kad užduoties būsena yra Paruošta (tai nurodo trikampis „kanban“ piktogramos viduje).  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Grąžinti paruoštos „kanban“ užduoties būseną
1. Sąraše pažymėkite pasirinktą eilutę.
    * Pasirinkite pirmą paruoštą užduotį.  
2. Veiksmų srityje spustelėkite Gamyba.
3. Spustelėkite Grąžinti būseną.
    * Galite naudoti alternatyvią „kanban“ taisyklę, kai teisingi šie teiginiai: – abiejų taisyklių papildymo strategija yra ta pati;  - abiejų taisyklių gamybos eigos versija yra ta pati;  - abiejų taisyklių tiekiamas produktas yra tas pats;  - bet kokios abiejų taisyklių vėliausiai sukonfigūruotos „kanban“ taisyklių proceso pabaigos veiklos yra tos pačios;  - sukonfigūruotos tos pačios abiejų taisyklių pateiktos atsargų dimensijos;  - sandėliavimo vieneto būsena yra Nepriskirtas;  - įvykio „kanban“ konfigūracija yra pati.  
    * Įsitikinkite, kad naujoji būsena yra Suplanuota.  
4. Spustelėkite GERAI.
5. Sąraše atžymėkite pasirinktą eilutę.
    * Pasirinkite tą pačią užduotį.  
    * Atkreipkite dėmesį, kad „kanban“ užduoties būsena grąžinama į Suplanuota (tai nurodo tuščia „kanban“ piktograma).  


