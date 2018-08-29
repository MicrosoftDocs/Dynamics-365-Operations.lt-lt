---
title: "Žinyno sistemos prijungimas"
description: "Šioje temoje aprašyti „Microsoft Dynamics 365 for Finance and Operations“ žinyno sistemos komponentai, apžvelgiama, kaip juos sujungti, ir pateikiama pasirinktinio žinyno kūrimo suvestinė."
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a1449d44149f328f780f02e798c5200595557474
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="connect-the-help-system"></a>Žinyno sistemos prijungimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi „Microsoft Dynamics 365 for Finance and Operations“ žinyno sistemos komponentai. Joje pateikiama apžvalga apie tai, kaip šiuos komponentus sujungti, ir pasirinktinio žinyno kūrimo suvestinė. 

## <a name="help-architecture"></a>Žinyno architektūra
Tolesnėje iliustracijoje rodomos „Finance and Operations‟ žinyno sistemos dalys. Vidinio žinyno sistema straipsnius ima iš „Finance and Operations‟ svetainės adresu https://docs.microsoft.com, o užduočių vadovus – iš „Lifecycle Services‟ (LCS) verslo procesų modeliavimo įrankio. 
> [!NOTE]
> Žvaigždute (\*) pažymėtos diagramoje išvardytos funkcijos yra planuojamos, bet dar neprieinamos. [![Žinyno architektūra](./media/help-architecture.png)](./media/help-architecture.png)


## <a name="connecting-the-help-system"></a>Žinyno sistemos prijungimas
> [!NOTE]
> Skirtukas **Užduočių vedliai** programose „Microsoft Dynamics 365 for Talent“ ir „Microsoft Dynamics 365 for Retail‟ šiuo metu nepasiekiamas. Šiuo metu dirbame, kad įgalintume šią funkciją būsimame leidime. Darbo su „Talent‟ pradžioje išlieka pasiekiami pagrindinių funkcijų užduočių gidai. „Retail“ ir „Talent“ procedūrinį žinyną taip pat galite rasti svetainėje docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)).


Naudodami puslapį **Sistemos parametrai**, sistemos administratoriai prijungia žinyno sistemos dalis diegti. [![Sistemos parametrų forma su žinyno parametrais](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Puslapyje **Sistemos parametrai** atlikite tolesnius veiksmus.

> [!IMPORTANT]
> Pirmą kartą atidarę skirtuką **Žinynas**, turite prisijungti prie „Lifecycle Services“. Būtinai spustelėkite formos viduryje pateiktą saitą, palaukite, kol prisijungsite, uždarykite dialogo langą ir tada spustelėkite **Gerai**, norėdami atidaryti puslapį **Sistemos parametrai**. [![Prisijungimas prie LCS](./media/connect-to-lcs-crop-1024x365.png "Prisijungimas prie LCS")](./media/connect-to-lcs-crop.png)

1.  Pasirinkite, prie kurio „Lifecycle Services‟ projekto prisijungti.
2.  Pasirinkite, iš kurių BPM bibliotekų (pasirinkto projekto) gauti užduočių įrašus.
    - Programoje „Finance and Operations“ norėdami pasiekti „Microsoft“ turinį, pasirinkite naujausią „Finance and Operations“ APQC bendrąją biblioteką. 
    - Programai „Retail“ biblioteką išleisime netolimoje ateityje. 
    - Jums nereikia pasirinkti bibliotekos „Talent“ atveju – ryšys su tinkama biblioteka jau sukurtas. 

3.  Nustatykite BPM bibliotekų rodymo tvarką. Taip nustatoma tvarka, kuria užduočių įrašai iš bibliotekų bus rodomi **Žinyno** srityje.

Atlikę šiuos veiksmus, galite atidaryti sritį **Žinynas** ir spustelėti skirtuką **Užduočių vedliai**. Matysite užduočių vedlius, taikomus „Finance and Operations“ puslapiui, kuriame dabar esate. Jei nerasite nė vieno užduočių vedlio, galite įvedę raktažodžius patikslinti iešką.

### <a name="showing-translated-task-guides"></a>Išverstų užduočių vedlių rodymas

Išversti užduočių vedliai pirmiausia buvo nusiųsti į APQC bendrąją biblioteką (2016 m. gegužės mėn.) ir darbo pradžios biblioteką. Norėdami „Finance and Operations“ peržiūrėti lokalizuotą užduočių vedlį, įsitikinkite, kad esate prisijungę prie gegužės mėn. bibliotekos. Ta kalba, kuria atskiram vartotojui rodomas užduočių vedlys, priklauso nuo kalbos parametrų, nustatytų dalyje **Parinktys** &gt; **Nuostatos**. 

> [!NOTE]
> Nors daug užduočių vedlių yra išversti, šiuo metu „Finance and Operations“ kliente nerodomi išversti užduočių vedlių pavadinimai. Be to, šiuo metu gegužės mėn. bibliotekoje galima rasti tik tuos išverstus užduočių vedlius, kurie buvo išleisti 2016 m. vasario mėnesį. Mes išleisime atnaujintą biblioteką su papildomais vertimais.
> -   Jei užduočių vedlys yra išverstas, atidarius tą užduočių vedlį visas užduočių vedlio tekstas bus rodomas jūsų pasirinkta kalba.
> -   Jei užduočių vedlys dar neišverstas, jį atidarius tik dalis užduočių vedlio teksto (valdiklių tekstas) bus rodoma jūsų pasirinkta kalba.

## <a name="creating-custom-help"></a>Pasirinktinio žinyno kūrimas
Kurdami užduočių įrašus, kurie atspindi jūsų diegimą, ir juos įrašydami į LCS verslo procesų biblioteką, galite sukurti pasirinktinį „Finance and Operations‟ ir „Retail“ žinyną. „Talent“ pasirinktinių užduočių vedlių sukurti negalima. 

Jei esate partneris ir biblioteką paaukštinsite iki įmonės bibliotekos bei įtrauksite ją į sprendimą, biblioteką galės naudoti jūsų klientai. Taip pat galite kopijuoti APQC suvienodintą visuotinę biblioteką ir tada savo kopiją atidaryti, iš jos atidaryti užduočių įrašus ir juos modifikuoti bei įrašus įrašyti su savo pakeitimais. Daugiau informacijos žr. temoje [Kaip sukurti užduoties įrašą ir jį naudoti kaip dokumentaciją ar mokymą](../../dev-itpro/user-interface/task-recorder.md).

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Pagalbos apžvalga](help-overview.md)

[Užduočių įrašymo priemonės apžvalga](../../dev-itpro/user-interface/task-recorder.md)

[Kaip kurti užduoties įrašą ir naudoti kaip dokumentus ar mokymą](../../dev-itpro/user-interface/task-recorder-training-docs.md)





