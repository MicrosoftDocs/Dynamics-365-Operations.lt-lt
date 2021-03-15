---
title: „Finance and Operations“ programų žinyno funkcijų konfigūravimas
description: Šioje temoje pateikiama informacija apie kai kurių „Microsoft Dynamics 365“ programų žinyno sistemos komponentus. Joje taip pat aiškinama, kaip sujungti šias programas, ir pateikiama pasirinktinio žinyno kūrimo proceso santrauka.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d000c3f801d382921a027c8ee259fd44ac5cdc80
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798285"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>„Finance and Operations“ programų žinyno funkcijų konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje rasite tokių „Finance and Operations“ programų, kaip „Microsoft Dynamics 365 Finance“, „Dynamics 365 Supply Chain Management“, „Dynamics 365 Commerce“ ir „Dynamics 365 Human Resources“, žinyno sistemos komponentų apžvalgą. Šioje temoje taip pat aiškinama, kaip sujungti šiuos komponentus, ir pateikiama pasirinktinio žinyno kūrimo proceso santrauka.

## <a name="help-architecture"></a>Žinyno architektūra

„Finance and Operations“ programose yra konceptualių apžvalgų ir kitų temų, kurios publikuojamos svetainėje [https://docs.microsoft.com/dynamics365](/dynamics365/). Šį turinį galima pasiekti iš produkto srities **Žinynas**. Toliau esančiame paveikslėlyje pavaizduotos žinyno sistemos dalys.

[![Žinyno architektūra](./media/help-architecture.png)](./media/help-architecture.png)

Produkto žinyno sistema gauna straipsnius iš docs.microsoft.com ir kitų prijungtų svetainių. Ji taip pat gauna užduočių vedlius, kurie saugomi verslo procesų modeliavimo įrankyje (BPM) portale „ Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="adding-task-guides"></a>Užduočių vedlių įtraukimas

> [!NOTE]
> Skirtukas **Užduočių vedliai** šiuo metu „Human Resources“ arba „Commerce“ nepasiekiamas. <!--We are currently working to enable this functionality in a future release.--> Tačiau darbo su „Human Resources“ pradžioje išlieka pasiekiami pagrindinių funkcijų užduočių vedliai. „Human Resources“ ir „Commerce“ procedūrinis žinynas taip pat pasiekiamas svetainėje [https://docs.microsoft.com/dynamics365](/dynamics365/).

Puslapyje **Sistemos parametrai** sistemos administratoriai gali konfigūruoti prieigą prie atitinkamų diegimui skirtų užduoties vedlių bibliotekų.

> [!NOTE]
> - Norėdami konfigūruoti žinyną, turite prisijungti naudodami paskyrą tame pačiame nuomotojuje, kuriame įdiegta programa.
> - LCS bibliotekos negalim prijungti iš programos egzemplioriaus, veikiančio vietiniame virtualiajame standžiajame diske (VHD).

[![Forma Sistemos parametrai su žinyno parametrais](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Norėdami konfigūruoti sprendimo užduoties vedlius, atlikite puslapyje **Sistemos parametrai** nurodytus veiksmus.

> [!IMPORTANT]
> Pirmą kartą atidarę skirtuką **Žinynas**, turite prisijungti prie „Lifecycle Services“. Būtinai pasirinkite formos viduryje pateiktą saitą, palaukite, kol prisijungsite, uždarykite dialogo langą, tada pasirinkite **Gerai**, kad patektumėte į puslapį **Sistemos parametrai**.
>
> [![Prisijungti prie LCS](./media/connect-to-lcs-crop-1024x365.png "Prisijungti prie LCS")](./media/connect-to-lcs-crop.png)

1. Pasirinkite, prie kurio „Lifecycle Services‟ projekto prisijungti.
2. Pasirinkite, iš kurių BPM bibliotekų (pasirinkto projekto) gauti užduočių įrašus.
3. Nustatykite BPM bibliotekų rodymo tvarką. Rodymo tvarka apibrėžia tvarką, kuria užduočių įrašai iš bibliotekų bus rodomi srityje **Žinynas**.

Atlikę šiuos veiksmus, galite atidaryti sritį **Žinynas** ir pasirinkti skirtuką **Užduočių vedliai**. Matysite užduočių vedlius, taikomus puslapiui, kuriame dabar esate „Finance and Operations“ programose. Jei nerasite nė vieno užduočių vedlio, galite įvedę raktažodžius patikslinti iešką.

### <a name="showing-translated-task-guides"></a>Išverstų užduočių vedlių rodymas

Išversti užduočių vedliai pirmiausia buvo išleisti APQC bendrojoje bibliotekoje (2016 m. gegužės mėn.) ir darbo pradžios bibliotekoje. Norėdami peržiūrėti lokalizuoto užduočių vedlio žinyną, įsitikinkite, kad jūsų „Dynamics 365“ sprendimas prijungtas prie 2016 m. gegužės mėn. bibliotekos. Vartotojai gali pakeisti kalbą, kuria rodomas užduočių vedlys: kalbos parametrai keičiami dalyje **Parinktys** &gt; **Nuostatos**.

> [!NOTE]
> Nors daug užduočių vedlių yra išversti, šiuo metu kliente nerodomi išversti užduočių vedlių pavadinimai. Be to, 2016 m. gegužės mėn. bibliotekoje pateikiami tik 2016 m. vasario mėnesį išleistų užduočių vedlių vertimai. „Microsoft“ išleis atnaujintą biblioteką, kurioje bus papildomų vertimų.
>
> - Jei užduočių vedlys yra išverstas, atidarius tą užduočių vedlį visas užduočių vedlio tekstas bus rodomas jūsų pasirinkta kalba.
> - Jei užduočių vedlys dar neišverstas, jį atidarius tik dalis užduočių vedlio teksto (valdiklių tekstas) bus rodoma jūsų pasirinkta kalba.

## <a name="adding-custom-help"></a>Pasirinktinio žinyno įtraukimas

Norėdami sukurti pasirinktinį žinyną galite naudoti užduočių vedlius arba pasirinktinio žinyno svetainę galite prijungti prie srities **Žinynas**.

### <a name="create-custom-help-by-using-task-guides"></a>Pasirinktinio žinyno kūrimas naudojant užduočių vedlius

Pasirinktinį palaikomų programų žinyną galite kurti kurdami užduočių įrašus, kurie atspindi jūsų diegimą, ir tada įrašydami juos į LCS verslo procesų biblioteką. Programoje „Human Resources“ pasirinktinių užduočių vedlių kurti negalite.

Jei esate partneris ir biblioteką paaukštinsite iki įmonės bibliotekos bei įtrauksite ją į sprendimą, biblioteką galės naudoti jūsų klientai. Taip pat galite sukurti APQC suvienodintos bibliotekos kopiją ir tada užduočių įrašus atidaryti kopijoje, juos redaguoti ir įrašyti savo pakeitimus. Daugiau informacijos žr. [Užduoties įrašymo ištekliai](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Pasirinktinio žinyno svetainės prijungimas

„Finance and Operations“ programos retai naudojamos savo parengtoje formoje. Vietoj to sprendimas yra pritaikomas ir išplečiamas, kad atitiktų organizacijos poreikius. Taip pat galite tinkinti ir išplėsti žinyno funkcijas. Pavyzdžiui, pasirinktinį žinyną galite įtraukti į produkto sritį **Žinynas**.

„Microsoft“ pateikė priemonių rinkinį, kuris jums padės įdiegti ir prijungti pasirinktinį žinyną prie srities **Žinynas**. Informacijos, kaip sukonfigūruoti pasirinktinį žinyno sprendimą, kuris yra prijungtas prie srities **Žinynas**, žr. [Pasirinktinio žinyno apžvalga](../../dev-itpro/help/custom-help-overview.md).

Jei norite bendradarbiauti su „Microsoft“ įrankiais ir procesais, kad galėtumėte tinkinti žinyną, užpildykite formą apsilankę [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Taip pat žiūrėkite

[Žinyno sistema](help-overview.md)  
[Pasirinktinio žinyno apžvalga](../../dev-itpro/help/custom-help-overview.md)  
[Užduoties įrašymo ištekliai](../../dev-itpro/user-interface/task-recorder.md)  
[Dokumentų ar mokymų kūrimas naudojant užduočių įrašymo priemonę](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Pasirinktinio žinyno „GitHub“ saugykla](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]