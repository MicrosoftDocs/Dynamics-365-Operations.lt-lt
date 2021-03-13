---
title: Klausimynų platinimas ir planavimas
description: Šiame straipsnyje paaiškinama, kaip platinti savo sukurtus klausimynus, kad jie būtų prieinami asmeniui ar grupei žmonių, kurie juos pildys.
author: andreabichsel
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25a53d921f8c0761ec931831810b484cfbd00718
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115757"
---
# <a name="distribute-and-schedule-questionnaires"></a>Klausimynų platinimas ir planavimas

Šiame straipsnyje paaiškinama, kaip platinti savo sukurtus klausimynus, kad jie būtų prieinami asmeniui ar grupei žmonių, kurie juos pildys. 

Platinti klausimyną galima keliais būdais.

-   Klausimyną pažymėkite kaip aktyvų. Tada klausimynas prieinamas visiems darbuotojams, nebent nustatyta klausimyno grupė, prie jo ribojanti prieigą.
-   Priskirkite klausimyno grupės teises. Tada klausimynas prieinamas visiems pasirinktos grupės nariams.
-   Kurkite suplanuotus atsakymų seansus. Tada klausimynas pasiekiamas tik tam tikram asmeniui.
-   Sukurkite grafiką. Tada klausimynas gali būti prieinamas keliems žmonėms.

## <a name="marking-a-questionnaire-as-active"></a>Klausimyno pažymėjimas kaip aktyvaus

Puslapio **Klausimynai** lauką **Aktyvus** nustačius į **Taip**, klausimyną gali pildyti visi darbuotojai. Respondentai klausimyną gali pildyti kelis kartus. Ši funkcija yra naudinga, jei norite atsiliepimus rinkti visus metus. Pavyzdžiui, galite sukurti klausimyną, kurį darbuotojai naudotų teikti atsiliepimams apie valgyklos pietų paslaugą.

## <a name="questionnaire-groups"></a>Klausimynų grupės

Galite nustatyti klausimyno grupes ir tada įtraukti respondentus, kuriems klausimynas turėtų būti išplatintas. 

Kurti klausimyno grupes galite tolesniuose puslapiuose.

-   **Klausimyno grupės** – pasirinktą klausimyną gali pildyti tik klausimyno grupės asmenys. Pavyzdžiui, jūsų tikslinė auditorija yra rangovai, todėl klausimyno grupę sukuriate konkrečiai tiems respondentams.
-   **Klausimyno grupės nariai** – į šias klausimyno grupes galite pridėti žmonių.

Norėdami klausimynui priskirti klausimyno grupę, puslapyje **Klausimynai** spustelėkite **Naudotojų teisės**. Klausimyną įrašius kaip aktyvų, jį gali pildyti klausimyno grupės nariai. Ši funkcija naudinga, norint klausimyną išbandyti su pasirinkta žmonių grupe ir tada jį naudoti su didesne grupe, arba norint klausimyną taikyti labai konkrečiai auditorijai.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Klausimyno suplanuoti atsakymų seansai

Suplanuoti atsakymų seansai yra klausimynai, kuriuos sukūrėte ir kuriems pasirinkote respondentus. 

> [!NOTE]
> Prieš nustatydami suplanuotus atsakymų seansus, turite sukurti klausimyną. 

Puslapyje **Suplanuotas atsakymų seansas** galite kurti suplanuotą atsakymų seansą kiekvienam darbuotojui. Puslapyje pateiktame sąraše rodomi visi suplanuoti klausimynai. 

Suplanuoti atsakymų seansai taip pat naudojami **Klausimyno grafikų** puslapyje, kuriame planuoti klausimynus galite keliems žmonėms.

-   Darbuotojai
-   Kurso dalyviai
-   Organizacijos vienetai

Kiekvienas asmuo atsakyti į klausimyną gali tik vieną kartą.

## <a name="scheduling-a-questionnaire"></a>Klausimyno planavimas

Neprivaloma: klausimyną planuoti galite keliems respondentams.

### <a name="planning-types"></a>Planavimo tipai

Jei suplanuotus atsakymų seansus norite planuoti keliems respondentams, reikalingi planavimo tipai. Planavimo tipai naudojami klasifikuoti klausimyno grafikams. Pavyzdžiui, planuoti klausimynus galite tolesniais tikslais.

-   Įvertinimas
-   Apklausa
-   Bandymai

Nurodyti klausimyno grafiko planavimo tipus galite **Klausimyno grafikų** puslapyje.

### <a name="reference-types-for-questionnaire"></a>Klausimyno nuorodų tipai

Nuorodų tipus galite naudoti norėdami įvesti kriterijus respondentams, kuriuos galbūt pasirinksite planuodami klausimyną. 

Norėdami nustatyti klausimyno nuorodų tipus, naudokite **Nuorodų tipų** puslapį. Kiekvienas nuorodos tipas atitinka lentelę programoje „Microsoft Dynamics 365 Finance“. Kurdami klausimyno grafikus, galite nurodyti atskirus lentelės įrašus arba įrašų, su kuriais klausimynas bus susietas, intervalą. 

Pvz., jei pasirenkate Kursų lentelę, galite nuspręsti, kuriam konkrečiam kursui klausimynas bus skirtas. Kai nustatote Kursų lentelės nuorodą, **Kursų** puslapyje tampa prieinami kai kurie laukai ir mygtukai.

### <a name="questionnaire-schedules"></a>Klausimynų grafikai

Klausimyno grafikus galite naudoti norėdami pagal nuorodos tipą naudotojų grupei generuoti kelis suplanuotus atsakymų seansus. Puslapyje **Klausimyno grafikai** sukurkite grafiką. Pasirinkite planavimo tipą grafikui kategorizuoti ir taip pat pasirinkite nuorodos tipą, kurį reikėtų naudoti sistemai teikiant užklausas apie konkrečius naudotojus. Pvz., jei nuorodos tipą nustatote į lentelė Kursai, **Nuorodos** lauke galite pasirinkti konkretų kursą. 

Norėdami pasirinkti klausimyną ir kitus kriterijus, spustelėkite **Sąrankos informacija**. Pavyzdžiui, jei klausimynas yra dėstytojo vertinimas, kaip kriterijų nurodykite dėstytojo vardą ir pavardę. Jums baigus įvesti sąrankos informaciją, sistema sugeneruoja suplanuotus atsakymų seansus, skirtus naudotojams, įtrauktiems į užklausą. 

Norėdami peržiūrėti grafiko atsakymų seansus, spustelėkite **Suplanuoti atsakymų seansai**. Tada galite rankiniu būdu kurti papildomų suplanuotų atsakymų seansų arba naikinti neatsakytus suplanuotus atsakymų seansus. 

Norėdami, kad klausimynas būtų pasiekiamas susijusių suplanuotų atsakymų seansų naudotojams, spustelėkite **Funkcijos** &gt; **Pradėti**. Norėdami peržiūrėti užpildytus klausimyno atsakymus, spustelėkite **Atsakymai**. Neprivaloma: klausimyno grafikų nuostatas, suplanuotus atsakymų seansus ir atsakymus galite kopijuoti į naują klausimyno grafiką.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Respondentų informavimas apie jiems prieinamus klausimynus
Kai platinate klausimyną, turite informuoti respondentus, kad jiems prieinami klausimynai. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Respondentų informavimas apie suplanuotą atsakymų seansą

Jei naudojate suplanuotą atsakymų seansą, asmenį turite informuoti tiesiogiai, pvz., telefonu ar elektroniniu paštu.

### <a name="notifying-respondents-about-a-scheduling"></a>Respondentų informavimas apie planavimą

Naudodami puslapį **Klausimyno grafikai**, paruoškite ir nusiųskite el. laišką visiems respondentams, kurie priskirti klausimynui. El. laiško tekstą įveskite skirtuke **Darbuotojų savitarnos el. paštas**. Kai grafikas pradėtas, spustelėkite **Funkcijos** &gt; **Siųsti el. laišką**, kad generuotumėte ir visiems respondentams nusiųstumėte el. laišką. Tada respondentai gali prisijungti prie svetainės ir pildyti klausimyną. 

> [!NOTE]
> Kad galėtumėte naudoti el. pašto funkcijas, puslapyje **El. pašto parametrai** jūsų IT administratorius turi įvesti el. pašto nuostatas.

## <a name="ending-a-scheduled-questionnaire"></a>Suplanuoto klausimyno baigimas

Galite pabaigti suplanuotą klausimyną, kai visi respondentai užbaigė jiems priskirtus klausimų seansus. Kai suplanuotas klausimynas baigtas, jo nuostatų į naują grafiką kopijuoti negalima. 

> [!NOTE]
>   Jei vienas ar keli respondentai klausimyno neužpildė, bet jūs vis tiek norite užbaigti planavimą, pirmiausia puslapyje **Planuojamas atsakymų seansas** turite iš sąrašo panaikinti tuos respondentus. Tada galite baigti grafiką.

## <a name="completing-questionnaires"></a>Klausimynų pildymas

Jums sukūrus ir išplatinus klausimyną, jį gali pildyti pasirinkti respondentai. Galite užpildyti klausimynus, kuriuos galite pasiekti iš dviejų vietų:

-   Naršymo srityje spustelėkite **Klausimynai** &gt; **Platinti** &gt; **Pildyti klausimyną**.
-   Darbuotojų savitarnoje spustelėkite **Pildytini klausimynai**.

Klausimynus galima padaryti prieinamus konkretiems naudotojams ar naudotojų grupėms arba visiems tinklo naudotojams.


