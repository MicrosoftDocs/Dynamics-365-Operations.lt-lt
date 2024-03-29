---
title: Statinių failų nusiuntimas ir pateikimas
description: Šiame straipsnyje aprašoma, kaip įkelti statinį Microsoft Dynamics 365 Commerce failą į svetainės generatorių ir kaip sukurti pasirinktinį URL ir failo pavadinimą, kurį galima naudoti norint prašyti to failo.
author: bicyclingfool
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8b30150d4187bbb0195bcb23960afe7389d56a5c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281945"
---
# <a name="upload-and-serve-static-files"></a>Statinių failų nusiuntimas ir pateikimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip įkelti statinį Microsoft Dynamics 365 Commerce failą į svetainės generatorių ir kaip sukurti pasirinktinį URL ir failo pavadinimą, kurį galima naudoti norint prašyti to failo.

Kai kurios trečiųjų šalių jungtys reikalauja, kad failas būtų patalpintas ir aptarnautas e-komercijos saite. Šios jungtys tikisi, kad failas bus grąžintas pagal užklausas į konkretų atšaukimo URL kelią ir failo pavadinimą. Todėl šiame straipsnyje paaiškinama, kaip įkelti ir naudoti statinį failą, kuriame yra vartotojo apibrėžtas URL Dynamics 365 Commerce ir failo vardas el. komercijos svetainėje.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Sukurkite saito URL, kuris grąžina statinį failą

Siekiant sukurti saito URL, kuris grąžina statinį failą „Commerce“ vietos kūrimo įtaise, vadovaukitės šiais žingsniais.

1. Eikite į savo vietos medijos biblioteką ir įkelkite failą, kuris turi būti aptarnaujamas pagal užklausas į jūsų nustatytą URL. Jei jau įkėlėte failą, galite praleisti šį žingsnį.
1. Eikite į **URL** savo saite.
1. Pasirinkite **Naujas \> Naujas URL**.
1. Teksto laukelyje **Naujas URL** rinkitės **Medijos bibliotekos turinys**.
1. Laukelyje **URL kelias** įveskite URL kelią. Įtraukti failo pavadinimą kelyje.
1. Pasirinkite **Toliau**. Medijos biblioteka yra atverta ir rodo visą medijos turinį pagal **Dokumento** tipą, kuris buvo įkeltas.
1. Pasirinkite failą, kuris turi būti rodomas užklausoms tame URL, kurį nustatėte žingsnyje 5.
1. Pasirinkite **Įrašyti**.

Dabar URL, kurį sukūrėte yra šablono būsenoje. Failas, į kurį veda URL, nebebus grąžinamas iki jums publikuojant URL. Prieš jums publikuojant URL, galite patvirtinti, kad būtų grąžinami tinkami duomenys.

## <a name="validate-and-publish-a-url"></a>Patvirtinti ir publikuoti URL

Siekiant patvirtinti URL prieš jo publikavimą, atlikite šiuos žingsnius.

1. Eikite į **URL** savo saite ir pasirinkite rodomą URL.
2. Ypatybių juostoje dešinėje, po **Redaguoti** mygtuką, pasirinkite tinkamą URL nuorodą. Naujame atvertame naršyklės lange turėtumėte matyti 404 klaidą.
3. Prikabinkite **?peržiūra=progrese** užklausos eilutę į URL (pavyzdžiui, `https://yoursite.com/callback.html?preview=inprogress`) ir iš naujo įkelkite puslapį. Failas, kurį įkėlėte į medijos biblioteką turi grįžti į atsakymą.

Jums patvirtinus URL, galite jį publikuoti.

1. Eikite į **URL** savo saite ir pasirinkite rodomą URL.
2. Pasirinkite **Publikuoti** komandos juostoje.

## <a name="update-the-file-that-a-url-points-to"></a>Naujinkite failą, į kurį veda URL

Po URL publikavimo, galite naujinti jį taip, kad jis rodytų į kitą failą. Kitu atveju, galite naujinti URL taip, kad jis vestų į kitą išteklių tipą kaip aprašyta kitame skyriuje. Pavyzdžiui, galite nurodyti URL į vidaus puslapį ar nukreipimą.

Norėdami naujinti failą, į kurį rodo URL, atlikite šiuos žingsnius.

1. Eikite į **URL** savo saite ir pasirinkite rodomą naujinama URL.
1. Ypatybių juostoje dešinėje rinkitės **Redaguoti**.
1. Skyriuje **URL priskyrimas**, rinkitės **Žingsnis 2** laukelį ir tada rinkitės naują dokumentą iš medijos bibliotekos.
1. Pasirinkite **Taikyti**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Naujinkite turinio tipą, į kurį veda URL

Galite taip pat naujinti URL taip, kad jis rodytų į kitą turinio tipą (išteklius), tokius kaip vidinį puslapį ar nukreipimą.

Norėdami naujinti turinio tipą, į kurį rodo URL, atlikite šiuos žingsnius.

1. Eikite į **URL** savo saite ir pasirinkite rodomą naujinama URL.
1. Ypatybių juostoje dešinėje rinkitės **Redaguoti**.
1. Skyriuje **URL priskyrimas**, **Žingsnis 1**, pasirinkite kitą turinio tipą.
1. Pasirinkite **Žingsnio 2** laukelį ir tada pasirinkite naują turinį.
1. Pasirinkite **Taikyti**.

## <a name="change-the-url-path"></a>Keiskite URL kelią

Sukūrus URL, jo kelio keisti nebepavyks. Jei privalote keisti URL kelią, kuris reikalingas failui ar kito tipo ištekliams, turite sukurti naują URL, sudaryti jo žemėlapį į esantį failą ar kitą išteklių ir tada nebepublikuoti bei panaikinti seną URL.

Norėdami keisti URL kelią, atlikite šiuos žingsnius.

1. Norėdami sukurti naują URL ir susieti jį su esamu failu ar kitais ištekliais, vadovaukitės instrukcijomis, [pateiktomis svetainės URL](#create-a-site-url-that-returns-a-static-file) sukurkite, kuris pateikia statinį failo skyrių anksčiau šiame straipsnyje.
1. Pasirinkite naują URL ir rinkitės **Publikuoti** komandos juostoje. Naujas URL yra publikuotas.
1. Norėdami nepublikuoti seno URL, pasirinkite jį ir tada rinkitės **Nepublikuoti** komandų juostoje. Dabar jei norite, galite panaikinti seną URL.

## <a name="additional-resources"></a>Papildomi ištekliai

[Skaitmeninio turto valdymo apžvalga](dam-overview.md)

[Vaizdų nusiuntimas](dam-upload-images.md)

[Vaizdo įrašų įkėlimas](dam-upload-video.md)

[Kitų nei vaizdo ir vaizdo įrašų failų nusiuntimas](dam-upload-files.md)

[Vaizdų apkarpymas](dam-crop-images.md)

[Vaizdų centro tinkinimas](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
