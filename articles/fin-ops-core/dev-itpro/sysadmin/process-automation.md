---
title: Procesų automatizavimas
description: Šioje temoje pateikiama informacija apie tai, kaip procesų automatizavimas leidžia paprastai suplanuoti procesus, kuriuos vykdys paketų serveris.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508190"
---
# <a name="process-automation"></a>Procesų automatizavimas

[!include[banner](../includes/banner.md)]

Procesų automatizavimas leidžia paprastai suplanuoti procesus, kuriuos vykdys paketų serveris. Atnaujinto suplanuotų užduočių kalendoriaus rodinys leidžia galutiniams vartotojams peržiūrėti ir atlikti veiksmus su suplanuotomis ir pabaigtomis užduotimis.

## <a name="administration"></a>Administravimas

Visų procesų automatizavimų centrinis administravimo puslapis yra sistemos administravimo modulyje **Nustatymas** meniu. Šiame puslapyje bus išvardyti visi sistemoje nustatyti automatizuoti procesai (serija). Be to, leidžiama pridėti naujų procesų automatizavimus tiesiogiai iš šio puslapio. Nustačius seriją, galite valdyti kiekvieną šio sąrašo seriją. Galite pasirinkti redaguoti visą seriją, panaikinti ją, peržiūrėti visus įvykius sąrašo rodinyje arba išjungti seriją, jei norite, kad suplanuotos užduotys būtų pristabdytos tam tikram laikotarpiui. 

## <a name="calendar-view"></a>Kalendoriaus rodinys 
Vienas iš pagrindinių procesų automatizavimo privalumų yra galimybė peržiūrėti suplanuotas užduotis paprastajame kalendoriaus rodinyje.  Šis rodinys leidžia peržiūrėti visos savaitės užduotis vienu metu. Šį rodinį pamatysite dešinėje puslapio **Procesų automatizavimas** pusėje. Jis bus automatiškai užpildytas pasirinktų serijų suplanuotomis užduotimis. 

[![Apdoroti automatizavimo kalendorių](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Įvykių pakeitimai
Kiekvieną įvykį galima modifikuoti nedarant įtakos kitiems įvykiams, nustatytiems juos sukūrusios serijos. Suplanuotas užduotis galima redaguoti kalendoriaus rodinyje pasirenkant mygtuką **Peržiūrėti/redaguoti** ir **Įvykis**. Tai suteikia prieigą prie visų parametrų, rodomų serijos nustatymo vedlyje ir galimybę atlikti vienkartinius pasirinkto įvykio pakeitimus. Suplanuota užduotis gali būti išjungta pasirenkant mygtuką **Išjungti** kalendoriaus rodinyje. 

## <a name="developer-documentation"></a>Kūrėjo dokumentacija 
Šiuo metu kuriama kūrėjo dokumentacija, leisianti kūrėjams išplėsti procesų automatizavimo sistemą. Šioje dokumentacijoje bus pateikta informacija apie tai, kaip galite sukurti pasirinktinius procesus, kurie yra vykdomi paketų serveryje, numatyti procesų automatizavimo vedlyje ir automatiškai atsirandantys kalendoriaus rodinyje.
