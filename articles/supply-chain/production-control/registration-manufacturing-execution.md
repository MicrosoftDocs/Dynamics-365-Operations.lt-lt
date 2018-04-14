---
title: Gamybos vykdymo registracija
description: "Šioje temoje paaiškinamos pagrindinės sąvokos ir terminai, kuriuos turite suprasti norėdami konfigūruoti ir naudoti gamybos vykdymą."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e5d4ee2fb1cd58107043939c3721fd857909f16b
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="registration-for-manufacturing-execution"></a>Gamybos vykdymo registracija

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje paaiškinamos pagrindinės sąvokos ir terminai, kuriuos turite suprasti norėdami konfigūruoti ir naudoti gamybos vykdymą. 

Gamybos vykdymas visų pirma yra skirtas naudoti gamyboms įmonėse. Darbuotojai gali registruoti gamybos užduotims atlikti sugaištamą laiką ir prekių suvartojimą naudodami puslapį **Užduoties registravimas**. Visos registracijos yra patvirtinamos ir vėliau perkeliamos į atitinkamus modulius. Nuolatinis registracijų patvirtinimas ir perkėlimas vadovams leidžia lengvai sekti faktines gamybos užsakymų išlaidas.

## <a name="manufacturing-execution-and-registration-terminology"></a>Gamybos vykdymo ir registravimo terminologija
Toliau pateiktoje lentelėje nurodyti terminai, susiję su gamybos vykdymu ir susijusiomis registravimo užduotimis.

| Semestras                          | aprašymas                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gamybos vykdymas       | Funkcija, naudojama laikui, medžiagų suvartojimui, išlaidoms gamybos užduotims, projektams ir netiesioginei veiklai registruoti. Registravimas atliekamas gamybos vykdymo registracijos kliente.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Užduočių sąrašas                      | Puslapyje **Užduoties registracija** darbuotojams rodomas sąrašas užduočių, kurias jie privalo atlikti naudodami konkretų išteklių, pvz., įrenginį. Darbuotojas gali registruoti kiekvieno užduočių sąraše esančio darbo ar užduoties laiką ir prekių suvartojimą.                                                                                                                                                                                                                                                                                                                                                                           |
| Užduočių grupavimas                  | Jei darbuotojas pradeda daugiau nei vieną užduotį vienu metu puslapyje **Užduoties registravimas**, tai vadinama užduočių grupavimu. Sugrupuotoms užduotims sugaištamą laiką galima paskirstyti atskiroms užduotims įvairiais būdais, naudojant paskirstymo raktus.                                                                                                                                                                                                                                                                                                                                                         |
| Vadovo / asistento registracijos | Darbuotojas gali užsiregistruoti prie ištekliaus kaip asistentas ir sukurti nedidelę komandą, kurioje keli darbuotojai dirba su tomis pačiomis gamybos užduotimis. Ištekliai, prie kurių darbuotojai yra prisijungę kaip asistentai, vadinami pagrindiniais. Tik vadovaujantieji ištekliai turi atlikti registracijas. Visi asistentai automatiškai gauna tas pačias registracijas. Jei, pavyzdžiui, įrenginys veikia kaip vadovas, prie to įrenginio kaip asistentai užsiregistravę darbuotojai gali atlikti registracijas puslapyje **Užduoties registracija** ir tas pačias registracijas gaus tiek įrenginys, tiek ir darbuotojai, prisijungę kaip asistentai. |
| Netiesioginė veikla             | Veikla ar užduotis, kuri tiesiogiai nesusijusi su gamybos užduotimi arba projektu, pvz., padalinio susitikimas, cecho valymo ar priežiūros darbai. Darbuotojai gali atlikti registraciją į netiesioginę veiklą tuo pačiu būdu, kaip registruodamiesi į gamybos užduotis ir projektus.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Registracijos gamybos vykdyme
Darbuotojai gali atlikti įvairių tipų gamybos vykdymo registracijas, kad atliktų gamybos užduočių metu atliekamą darbą. Atsižvelgiant į sistemos nustatymą, darbuotojai taip pat gali atlikti projekto veiklos ir neproduktyvių užduočių, pvz., pertraukų, neatvykimo ir netiesioginės veiklos, registraciją. Toliau nurodyti registracijos tipai:

-   **Atėjimas į darbą / išėjimas iš darbo** (galima naudoti su laiku ir lankomumu) – darbuotojai nurodo, kada atvyksta į darbą ir kada išeina iš darbo eidami namo.
-   **Registracija į gamybos užduotis** – darbuotojai gali atlikti jo (jos) užduočių sąraše rodomų gamybos užduočių registraciją, pvz., registruoti užduoties pradėjimą ir pateikti užduoties grįžtamąjį ryšį. Darbuotojai gali pradėti kelias užduotis vienu metu. Tai vadinama užduočių grupavimu.
-   **Registracija į atsargas** – darbuotojai gali atlikti medžiagų, naudojamų ceche, bet tiesiogiai nesusijusių su gamybos užduotimis, registraciją. Pavyzdžiai apima tepalą, alyvas ar kitas medžiagas, kurios naudojamos įrangos veikimui užtikrinti. Registracija atliekama atsargų žurnale.
-   **Registracija į projektus** (galima naudoti su laiku ir lankomumu) – darbuotojai gali atlikti, pvz., projektų darbo pradžios ir pabaigos arba projekto veiklų, rodomų užduočių sąraše, registracijas.
-   **Projekto mokesčių ir projekto elementų registracija** (galima naudoti su laiku ir lankomumu) – darbuotojai gali registruoti su projektu susijusius mokesčius (išlaidas) projekto mokesčių žurnale, pvz., išlaidas už nuvažiuotą atstumą ar išlaidas mokesčiams už važiavimą per mokamus tiltus. Darbuotojai taip pat gali registruoti prekių suvartojimą projektuose. Tai atliekama projekto prekių žurnale.
-   **Registravimasis kito darbuotojo asistentu** – jei su gamybos užduotimi ar projektu kartu dirbs du ar daugiau darbuotojų, darbuotojas gali užsiregistruoti kaip įrenginio arba kito darbuotojo asistentas; tuomet pirmasis darbuotojas bus laikomas pagrindiniu (vadovu). Jei reikia, vadovas gali pasirinkti kitą darbuotoją kaip vadovą.
-   **Registruoti neatvykimą** (galima naudoti su laiku ir lankomumu) – darbuotojai gali registruoti laiką įvairiais nustatytais neatvykimo kodais. Neatvykimą galima nurodyti, jei darbuotojas atvyksta pavėlavęs, jei jis negali būti darbe darbo dienos metu arba išeina anksčiau nei numatyta, pagal standartinį darbo laiko šabloną.
-   **Registruoti pertraukas** (galima naudoti su laiku ir lankomumu) – per darbo dieną darbuotojai gali registruotis, kad jie palieka savo darbo vietą norėdami daryti pertrauką. Galima nustatyti kelių tipų pertraukas. Kai darbuotojas grįžta ir vėl užsiregistruoja, sistema užregistruoja, kad darbuotojas grįžo, ir pertraukos registracija sustabdoma.
-   **Registruoti netiesiogines veiklas** (galima naudoti su laiku ir lankomumu) – netiesioginės veiklos yra neproduktyvios veiklos, kurių darbuotojai gali imtis darbo dienos metu, pvz., padalinio susitikimas, komandos susitikimas arba ceche atliekama priežiūros užduotis. Darbuotojai gali registruoti nustatytą netiesioginę veiklą.
-   **Registruoti viršvalandžius** (galima naudoti su laiku ir lankomumu) – darbuotojai, kurių paprašyta dirbti ilgiau, gali pasirinkti, ar papildomą laiką registruoti kaip darbą laisvu grafiku, ar kaip viršvalandžius.





