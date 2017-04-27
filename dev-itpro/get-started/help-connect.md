---
title: "Žinyno sistemos prijungimas"
description: "Šioje temoje apibūdinami „Microsoft Dynamics 365 for Operations“ žinyno sistemos komponentai ir pateikiama informacija apie tai, kaip juos sujungti, bei pasirinktinio žinyno kūrimo suvestinė."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Žinyno sistemos prijungimas

Šioje temoje aprašomi „Microsoft Dynamics 365 for Operations“ žinyno sistemos komponentai. Joje pateikiama apžvalga apie tai, kaip šiuos komponentus sujungti, ir pasirinktinio žinyno kūrimo suvestinė. 

<a name="help-architecture"></a>Žinyno architektūra
-----------------

Tolesniame paveikslėlyje rodomos „Dynamics 365 for Operations‟ žinyno sistemos dalys. Vidinio žinyno sistema straipsnius ima iš „Dynamics 365 for Operations‟ svetainės adresu https://docs.microsoft.com, o užduočių vadovus – iš „Lifecycle Services‟ (LCS) verslo procesų modeliavimo įrankio. 
**Pastaba.** Su žvaigždute (\*) diagramoje išvardytos funkcijos yra planuojamos, bet dar neprieinamos. [![Žinyno architektūra](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Žinyno sistemos prijungimas
Naudodami puslapį **Sistemos parametrai**, sistemos administratoriai prijungia žinyno sistemos dalis diegti. [![Sistemos parametrų forma su žinyno parametrais](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Puslapyje **Sistemos parametrai** atlikite tolesnius veiksmus.

1.  **Svarbu:** pirmą kartą atidarę skirtuką **Žinynas**, turite prisijungti prie „Lifecycle Services“. Būtinai spustelėkite formos viduryje pateiktą saitą, palaukite, kol prisijungsite, uždarykite dialogo langą ir tada spustelėkite **Gerai**, norėdami atidaryti puslapį **Sistemos parametrai**. [![Prisijungimas prie LCS](./media/connect-to-lcs-crop-1024x365.png "Prisijungimas prie LCS")](./media/connect-to-lcs-crop.png)
2.  Pasirinkite, prie kurio „Lifecycle Services‟ projekto prisijungti.
3.  Pasirinkite, iš kurių BPM bibliotekų (pasirinkto projekto) gauti užduočių įrašus.
4.  Nustatykite BPM bibliotekų rodymo tvarką. Taip nustatoma tvarka, kuria užduočių įrašai iš bibliotekų bus rodomi **Žinyno** srityje.

Atlikę šiuos veiksmus, galite atidaryti **Žinyno** sritį ir spustelėti **Užduočių vadovų** skirtuką. Dabar matysite užduočių vedlius, taikomus tam puslapiui, kuriame „Dynamics 365 for Operations“ dabar esate. Jei nerasite nė vieno užduočių vedlio, galite įvedę raktažodžius patikslinti iešką.

### <a name="showing-translated-task-guides"></a>Išverstų užduočių vedlių rodymas

Išversti užduočių vedliai pirmiausia buvo nusiųsti į APQC bendrąją biblioteką (2016 m. gegužės mėn.) ir darbo pradžios biblioteką. Norėdami „Dynamics 365 for Operations“ peržiūrėti lokalizuotą užduočių vedlį, įsitikinkite, kad esate prisijungę prie gegužės mėn. bibliotekos. Ta kalba, kuria atskiram vartotojui rodomas užduočių vedlys, priklauso nuo kalbos parametrų, nustatytų dalyje **Parinktys** &gt; **Nuostatos**. **Pastaba.** Nors daug užduočių vedlių yra išversti, šiuo metu „Dynamics 365 for Operations“ kliente nerodomi išversti užduočių vedlių pavadinimai. Be to, šiuo metu gegužės mėn. bibliotekoje galima rasti tik tuos išverstus užduočių vedlius, kurie buvo išleisti 2016 m. vasario mėnesį. Mes išleisime atnaujintą biblioteką su papildomais vertimais.

-   Jei užduočių vedlys yra išverstas, atidarius tą užduočių vedlį visas užduočių vedlio tekstas bus rodomas jūsų pasirinkta kalba.
-   Jei užduočių vedlys dar neišverstas, jį atidarius tik dalis užduočių vedlio teksto (valdiklių tekstas) bus rodoma jūsų pasirinkta kalba.

## <a name="creating-custom-help"></a>Pasirinktinio žinyno kūrimas
Kurdami užduočių įrašus, kurie atspindi jūsų diegimą, ir juos įrašydami į LCS verslo procesų biblioteką, galite sukurti pasirinktinį „Dynamics 365 for Operations‟ žinyną. Jei esate partneris ir biblioteką paaukštinsite iki įmonės bibliotekos bei įtrauksite ją į sprendimą, biblioteką galės naudoti jūsų klientai. Taip pat galite kopijuoti APQC suvienodintą visuotinę biblioteką ir tada savo kopiją atidaryti, iš jos atidaryti užduočių įrašus ir juos modifikuoti bei įrašus įrašyti su savo pakeitimais. Daugiau informacijos žr. temoje [Kaip sukurti užduoties įrašą ir jį naudoti kaip dokumentaciją ar mokymą](../user-interface/task-recorder.md).

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Žinyno apžvalga](help-overview.md)

[Užduočių įrašymo priemonės apžvalga](../user-interface/task-recorder.md)

[Kaip kurti užduoties įrašą ir naudoti kaip dokumentus ar mokymą](../user-interface/task-recorder-training-docs.md)

[Naujų „Dynamics 365 for Operations“ mokymų bibliotekų kūrimas „Lifecycle Services“ naudojant užduočių įrašymo priemonę (išorinis saitas)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


