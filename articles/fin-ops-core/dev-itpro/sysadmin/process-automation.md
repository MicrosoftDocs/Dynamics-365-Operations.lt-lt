---
title: Proceso automatizavimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip procesų automatizavimas leidžia paprastą procesų, kurie bus paleisti paketinio apdorojimo serveryje, planavimą.
author: RyanCCarlson2
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: c0015b65f1ff00cfce19139cb8aaa248512d070b
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2022
ms.locfileid: "9114942"
---
# <a name="process-automation"></a>Procesų automatizavimas

[!include[banner](../includes/banner.md)]

Procesų automatizavimas leidžia paprastai suplanuoti procesus, kuriuos vykdys paketų serveris. Atnaujinto suplanuotų užduočių kalendoriaus rodinys leidžia galutiniams vartotojams peržiūrėti ir atlikti veiksmus su suplanuotomis ir pabaigtomis užduotimis.

## <a name="administration"></a>Administravimas

Visų procesų automatizavimų centrinis administravimo puslapis yra sistemos administravimo modulyje **Nustatymas** meniu. Šiame puslapyje bus išvardyti visi sistemoje nustatyti automatizuoti procesai (serija). Be to, leidžiama pridėti naujų procesų automatizavimus tiesiogiai iš šio puslapio. Nustačius seriją, galite valdyti kiekvieną šio sąrašo seriją. Galite pasirinkti redaguoti visą seriją, panaikinti ją, peržiūrėti visus įvykius sąrašo rodinyje arba išjungti seriją, jei norite, kad suplanuotos užduotys būtų pristabdytos kuriam laikui. 

Visi funkcijų valdyme neįjungti procesai nebus rodomi funkcijai esant išjungtai. Taip pat, procesų automatizavimo grafiko variklis nenustatys jokių įvykių ar fone vykstančių procesų išjungtai funkcijai. Funkcijos įjungimas įjungs visus suplanuotus įvykius ir anksčiau pradėtus fone vykstančius procesus neatidėliotinam vykdymui. Proceso automatizavimo planavimo sistema remiasi sistemos paketine užduotimi, apdoroti **apklausų sistemos automatizavimo** užduotį. Užduoties negalima pakeisti ar pakeisti bet kuriuo metu. Jei ši paketinė užduotis nepaleidusi arba jos būsena yra Klaida, **norėdami** iš naujo nustatyti paketinę užduotį pasirinkite Inicijuoti proceso automatizavimą. Taip iš naujo bus užtikrintas bet koks naujos automatizavimas, paleistas naudojant naujesnę programos versiją. 

## <a name="calendar-view"></a>Kalendoriaus rodinys

Vienas iš pagrindinių procesų automatizavimo privalumų yra galimybė peržiūrėti suplanuotas užduotis paprastajame kalendoriaus rodinyje.  Šis rodinys leidžia peržiūrėti visos savaitės užduotis vienu metu. Šį rodinį pamatysite dešinėje puslapio **Procesų automatizavimas** pusėje. Jis bus automatiškai užpildytas pasirinktų serijų suplanuotomis užduotimis. 

[![Apdoroti automatizavimo kalendorių.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Įvykių pakeitimai

Kiekvieną įvykį galima modifikuoti nedarant įtakos kitiems įvykiams, nustatytiems juos sukūrusios serijos. Suplanuotas užduotis galima redaguoti kalendoriaus rodinyje pasirenkant mygtuką **Peržiūrėti/redaguoti** ir **Įvykis**. Šis puslapis suteikia prieigą prie visų parametrų, rodomų serijos nustatymo vedlyje ir galimybę atlikti vienkartinius pasirinkto įvykio pakeitimus. Suplanuota užduotis gali būti išjungta pasirenkant mygtuką **Išjungti** kalendoriaus rodinyje.

## <a name="developer-documentation"></a>Kūrėjo dokumentacija

Procesų automatizavimo sistema leidžia programuotojams išplėsti proceso automatizavimo sistemą. [Procesų automatizavimo sistema](../process-automation/process-automation-framework.md) dokumentacijoje pateikta informacija apie tai, kaip galite sukurti pasirinktinius procesus, kurie yra vykdomi paketų serveryje, numatyti procesų automatizavimo vedlyje ir automatiškai atsirandantys kalendoriaus rodinyje.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
