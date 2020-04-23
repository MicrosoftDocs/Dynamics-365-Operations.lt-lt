---
title: Grąžinti „kanban“ užduoties būseną
description: Ši procedūra padeda grąžinti neteisingą „kanban“ užduoties būseną.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adf65175669d4cd5ec4cb431a7e1436ea3da83ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210515"
---
# <a name="revert-kanban-job-status"></a>Grąžinti „kanban“ užduoties būseną

[!include [banner](../../includes/banner.md)]

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

