---
title: "Platinti ir pildyti klausimyną"
description: "Šioje temoje aiškinama, kaip paskirstyti klausimynus, kurie kuriate, taip, kad jie yra asmuo arba grupė žmonių, kurie jas užbaigti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: 8e09c6b042d557e3b2d608fb5e278169fc3c1d88
ms.lasthandoff: 03/31/2017


---

# <a name="distribute-and-complete-a-questionnaire"></a>Platinti ir pildyti klausimyną

Šioje temoje aiškinama, kaip paskirstyti klausimynus, kurie kuriate, taip, kad jie yra asmuo arba grupė žmonių, kurie jas užbaigti. 

Platinti klausimyną galima keliais būdais.

-   Klausimyną pažymėkite kaip aktyvų. Tada klausimynas prieinamas visiems darbuotojams, nebent nustatyta klausimyno grupė, prie jo ribojanti prieigą.
-   Priskirkite klausimyno grupės teises. Tada klausimynas prieinamas visiems pasirinktos grupės nariams.
-   Kurkite suplanuotus atsakymų seansus. Tada klausimynas pasiekiamas tik tam tikram asmeniui.
-   Sukurkite grafiką. Tada klausimynas gali būti prieinamas keliems žmonėms.

## <a name="marking-a-questionnaire-as-active"></a>Klausimyno pažymėjimas kaip aktyvaus
Nustačius, **Active** lauko į **taip** ant į **klausimynus** puslapyje, jūs padaryti klausimynas skirtas visiems darbuotojams atlikti. Respondentai gali užpildyti klausimyną kelis kartus. Ši funkcija yra naudinga, jei norite rinkti nuolatinio grįžtamojo ryšio ištisus metus. Pavyzdžiui, galite sukurti klausimyną, kurį darbuotojai naudotų teikti atsiliepimams apie valgyklos pietų paslaugą.

## <a name="questionnaire-groups"></a>Klausimynų grupės
Galite nustatyti klausimyno grupes ir tada įtraukti respondentus, kuriems klausimynas turėtų būti išplatintas. 

Kurti klausimyno grupes galite tolesniuose puslapiuose.

-   **Klausimyno grupės** – pasirinktą klausimyną gali pildyti tik klausimyno grupės asmenys. Pavyzdžiui, jūsų tikslinė auditorija yra rangovai, todėl klausimyno grupę sukuriate konkrečiai tiems respondentams.
-   **Klausimyno grupės nariai** – į šias klausimyno grupes galite pridėti žmonių.

Priskirti klausimyną grupę į klausimyno klausimus, dėl to **klausimynus** spustelėkite **vartotojo teises**. Po klausimyno įrašomas kaip aktyvų, klausimyno grupės nariai gali užpildyti klausimyną. Ši funkcija yra naudinga, jei norite išbandyti klausimyną dėl pasirinktos grupės žmonių, prieš ją iškočiokite didesnei grupei, arba jei norite nukreipti klausimyno labai konkrečiai auditorijai.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Klausimyno suplanuoti atsakymų seansai
Suplanuoti atsakymų seansai yra klausimynai, kuriuos sukūrėte ir kuriems pasirinkote respondentus. 

**Pastaba.** Prieš nustatydami suplanuotus atsakymų seansus, turite sukurti klausimyną. 

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

Norėdami nustatyti klausimyno nuorodų tipus, naudokite **Nuorodų tipų** puslapį. Kiekvienos nuorodos tipas atitinka lentelę programoje Microsoft Dynamics 365 operacijoms. Kurdami klausimyno grafikus, galite nurodyti atskirus lentelės įrašus arba įrašų, su kuriais klausimynas bus susietas, intervalą. 

Pvz., jei pasirenkate Kursų lentelę, galite nuspręsti, kuriam konkrečiam kursui klausimynas bus skirtas. Kai nustatote Kursų lentelės nuorodą, **Kursų** puslapyje tampa prieinami kai kurie laukai ir mygtukai.

### <a name="questionnaire-schedules"></a>Klausimynų grafikai

Klausimyno tvarkaraščius galite sukurti kelis suplanuotų atsakymų seansus grupės vartotojams, pagal nuorodos tipą. Kurti tvarkaraštį su **klausimyną tvarkaraščių** puslapis. Pasirinkite planavimo tipas kategorizuoti tvarkaraštį ir taip pat nuorodos tipą, kuris turėtų būti naudojamas pateikti užklausą sistemą konkretiems vartotojams. Pavyzdžiui, jei nustatysite nuorodos tipą kursų lentelę, galite pasirinkti tam tikro kurso, su **nuoroda** srityje. 

Norėdami pasirinkti klausimyną ir kitus kriterijus, spustelėkite **Sąrankos informacija**. Pvz., nurodyti dėstytojo vardą ir pavardę kaip kriterijų, jei klausimynas yra instruktorius įvertinimas. Baigę įvesti sąrankos duomenis, sistema sugeneruoja suplanuotus atsakymų seansus vartotojams, kurie yra įtraukti į užklausą. 

Norėdami peržiūrėti grafiko atsakymų seansus, spustelėkite **Suplanuoti atsakymų seansai**. Tada galite rankiniu būdu kurti papildomų suplanuotų atsakymų seansų arba naikinti neatsakytus suplanuotus atsakymų seansus. 

Spustelėkite **funkcijos**&gt;**pradėti** pateikti klausimyno vartotojai, susijusių suplanuotų atsakymų seansus. Norėdami peržiūrėti užpildytus klausimyno atsakymus, spustelėkite **Atsakymai**. Neprivaloma: klausimyno grafikų nuostatas, suplanuotus atsakymų seansus ir atsakymus galite kopijuoti į naują klausimyno grafiką.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Respondentų informavimas apie jiems prieinamus klausimynus
Kai platinate klausimyną, turite informuoti respondentus, kad jiems prieinami klausimynai. 

**Pastaba:** respondentų turi būti vartotojams Microsoft Dynamics 365 operacijoms užpildyti anketą.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Respondentų informavimas apie suplanuotą atsakymų seansą

Jei naudojate suplanuotą atsakymų seansą, asmenį turite informuoti tiesiogiai, pvz., telefonu ar elektroniniu paštu.

### <a name="notifying-respondents-about-a-scheduling"></a>Respondentų informavimas apie planavimą

Naudodami puslapį **Klausimyno grafikai**, paruoškite ir nusiųskite el. laišką visiems respondentams, kurie priskirti klausimynui. El. laiško tekstą įveskite **Darbuotojų savitarnos dalies el. pašto** skirtuke. Pradėjus tvarkaraštyje, spustelėkite **funkcijos**&gt;**siųsti el. paštu** kurti ir siųsti laišką į respondentų. Respondentų galite prisijungti prie svetainės ir užpildyti klausimyną. 

**Pastaba.** Kad galėtumėte naudoti el. pašto funkcijas, **El. pašto parametrų** puslapyje jūsų IT administratorius turi įvesti el. pašto nuostatas.

## <a name="ending-a-scheduled-questionnaire"></a>Suplanuoto klausimyno baigimas
Galite pabaigti suplanuotą klausimyną, kai visi respondentai užbaigė jiems priskirtus klausimų seansus. Kai suplanuotas klausimynas baigtas, jo nuostatų į naują grafiką kopijuoti negalima. 

**Pastaba.** Jei vienas ar keli respondentai klausimyno neužpildė, bet jūs vis tiek norite užbaigti planavimą, pirmiausia **Suplanuoto atsakymų seanso** puslapyje turite iš sąrašo panaikinti tuos respondentus. Tada galite baigti grafiką.

## <a name="completing-questionnaires"></a>Klausimynų pildymas
Jums sukūrus ir išplatinus klausimyną, jį gali pildyti pasirinkti respondentai. Galite užpildyti klausimynus, kuriuos galite pasiekti iš dviejų vietų:

-   Naršymo srityje spustelėkite **klausimynus**&gt;**paskirstyti**&gt;**užpildyti anketą,**.
-   Darbuotojų savitarnoje spustelėkite **Pildytini klausimynai**.

Klausimynus galima padaryti prieinamus konkretiems naudotojams ar naudotojų grupėms arba visiems tinklo naudotojams.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Klausimynų kūrimas](design-questionnaires.md)

[Klausimynų naudojimas](questionnaires.md)

[Peržiūri ir klausimynų rezultatų](evaluate-questionnaire-results.md)


