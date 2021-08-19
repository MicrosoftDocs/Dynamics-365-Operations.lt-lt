---
title: Grąžinti „kanban“ užduoties būseną
description: Ši procedūra padeda grąžinti neteisingą „kanban“ užduoties būseną.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef6d77aae52dc81bb1b34acc74d4174a7dfe0482f3af5123f93688244cf50f9f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728536"
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
    * Galite naudoti alternatyvią „kanban“ taisyklę, kai teisingi šie teiginiai: – abiejų taisyklių papildymo strategija yra ta pati;  - abiejų taisyklių gamybos eigos versija yra ta pati;  - abiejų taisyklių tiekiamas produktas yra tas pats;  - bet kokios abiejų taisyklių vėliausiai sukonfigūruotos „kanban“ taisyklių proceso pabaigos veiklos yra tos pačios;  - sukonfigūruotos tos pačios abiejų taisyklių pateiktos atsargų dimensijos;  - Sandėliavimo vieneto būsena yra Nepriskirta;  - įvykio „kanban“ konfigūracija yra pati.  
    * Įsitikinkite, kad naujoji būsena yra Suplanuota.  
4. Spustelėkite GERAI.
5. Sąraše atžymėkite pasirinktą eilutę.
    * Pasirinkite tą pačią užduotį.  
    * Atkreipkite dėmesį, kad „kanban“ užduoties būsena grąžinama į Suplanuota (tai nurodo tuščia „kanban“ piktograma).  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]