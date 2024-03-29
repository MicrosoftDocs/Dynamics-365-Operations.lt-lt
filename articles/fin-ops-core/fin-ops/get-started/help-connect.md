---
title: Finansų ir operacijų programėlių žinyno patirties konfigūravimas
description: Šiame straipsnyje pateikiama informacija apie kai kurių 365 programėlių Microsoft Dynamics žinyno sistemos komponentus.
author: edupont04
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: edupont
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.form: SystemParameters
ms.openlocfilehash: 75f3cc1b76b2a38d4004c4fa3f86a528a7eebc3f
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9538529"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių žinyno patirties konfigūravimas

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šiame straipsnyje rasite finansų ir operacijų programėlių žinyno sistemos komponentų, pvz., Microsoft Dynamics 365 finansų ir Dynamics 365 Supply Chain Management. Dynamics 365 Commerce Dynamics 365 Human Resources Straipsnyje taip pat paaiškinama, kaip susieti šiuos komponentus ir pateikiama pasirinktinio žinyno kūrimo proceso suvestinė.

## <a name="help-architecture"></a>Žinyno architektūra

Finansų ir operacijų programėlės apima abstrakčias peržiūras ir kitas temas, kurios publikuojamos [Microsoft Dynamics 365 dokumentų](/dynamics365/) svetainėje. Šį turinį galima pasiekti iš produkto srities **Žinynas**. Toliau esančiame paveikslėlyje pavaizduotos žinyno sistemos dalys.

[![Žinyno architektūra.](./media/help-architecture.png)](./media/help-architecture.png)

Produkto žinyno sistema priima straipsnius iš kitų prijungtų Microsoft Learn svetainių. Ji taip pat gauna užduočių vedlius, kurie saugomi verslo procesų modeliavimo įrankyje (BPM) portale „ Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="adding-task-guides"></a>Užduočių vedlių įtraukimas

> [!NOTE]
> Skirtukas **Užduočių vedliai** šiuo metu „Human Resources“ arba „Commerce“ nepasiekiamas. <!--We are currently working to enable this functionality in a future release.--> Tačiau darbo su „Human Resources“ pradžioje išlieka pasiekiami pagrindinių funkcijų užduočių vedliai. „Human Resources“ ir „Commerce“ procedūrinis žinynas taip pat pasiekiamas [„Microsoft Dynamics 365“ dokumentų](/dynamics365/) svetainėje.

Puslapyje **Sistemos parametrai** sistemos administratoriai gali konfigūruoti prieigą prie atitinkamų diegimui skirtų užduoties vedlių bibliotekų.

> [!NOTE]
> - Norėdami konfigūruoti žinyną, turite prisijungti naudodami paskyrą tame pačiame nuomotojuje, kuriame įdiegta programa.
> - LCS bibliotekos negalim prijungti iš programos egzemplioriaus, veikiančio vietiniame virtualiajame standžiajame diske (VHD).

[![Forma Sistemos parametrai su žinyno parametrais.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Norėdami konfigūruoti sprendimo užduoties vedlius, atlikite puslapyje **Sistemos parametrai** nurodytus veiksmus.

> [!IMPORTANT]
> Pirmą kartą atidarę skirtuką **Žinynas**, turite prisijungti prie „Lifecycle Services“. Būtinai pasirinkite formos viduryje pateiktą saitą, palaukite, kol prisijungsite, uždarykite dialogo langą, tada pasirinkite **Gerai**, kad patektumėte į puslapį **Sistemos parametrai**.
>
> [![Prisijungti prie LCS](./media/connect-to-lcs-crop-1024x365.png "Prisijunkite prie LCS.")](./media/connect-to-lcs-crop.png)

1. Pasirinkite, prie kurio „Lifecycle Services‟ projekto prisijungti.
2. Pasirinkite, iš kurių BPM bibliotekų (pasirinkto projekto) gauti užduočių įrašus.
3. Nustatykite BPM bibliotekų rodymo tvarką. Rodymo tvarka apibrėžia tvarką, kuria užduočių įrašai iš bibliotekų bus rodomi srityje **Žinynas**.

Atlikę šiuos veiksmus, galite atidaryti žinyno sritį **ir** pasirinkti skirtuką **Užduočių** vedliai. Dabar matysite užduočių instrukcijas, kurios taikomos puslapiui, kurį šiuo metu naudojate finansų ir operacijų programėlėse. Jei nerasite nė vieno užduočių vedlio, galite įvedę raktažodžius patikslinti iešką.

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

Finansinės ir operacijų programėlės retai naudojamos jų išeinant iš lango. Vietoj to sprendimas yra pritaikomas ir išplečiamas, kad atitiktų organizacijos poreikius. Taip pat galite tinkinti ir išplėsti žinyno funkcijas. Pavyzdžiui, pasirinktinį žinyną galite įtraukti į produkto sritį **Žinynas**.

„Microsoft“ pateikė priemonių rinkinį, kuris jums padės įdiegti ir prijungti pasirinktinį žinyną prie srities **Žinynas**. Informacijos, kaip sukonfigūruoti pasirinktinį žinyno sprendimą, kuris yra prijungtas prie srities **Žinynas**, žr. [Pasirinktinio žinyno apžvalga](../../dev-itpro/help/custom-help-overview.md).

Jei norite bendradarbiauti su „Microsoft“ įrankiais ir procesais, kad galėtumėte tinkinti žinyną, užpildykite formą apsilankę [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Taip pat žiūrėkite

[Žinyno sistema](help-overview.md)  
[Pasirinktinio žinyno apžvalga](../../dev-itpro/help/custom-help-overview.md)  
[Užduoties įrašymo ištekliai](../../dev-itpro/user-interface/task-recorder.md)  
[Dokumentų ar mokymų kūrimas naudojant užduočių įrašymo priemonę](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Pasirinktinio žinyno „GitHub“ saugykla](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
