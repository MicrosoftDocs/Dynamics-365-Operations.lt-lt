---
title: "Saugos sąnaudų apskaitos analizės Power BI turinio nustatymas"
description: "Šioje temoje aiškinama, kaip jūs galite propaguoti prieigos lygį saugumo kaštų apskaitos eilutės lygio saugumo Microsoft Power BI. Šios funkcijos padeda užtikrinti, kad vartotojai mato tik Power BI duomenis, kad jie būtų suteikta galimybė naudotis."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Saugos sąnaudų apskaitos analizės Power BI turinio nustatymas

Šioje temoje aiškinama, kaip jūs galite propaguoti prieigos lygį saugumo kaštų apskaitos eilutės lygio saugumo Microsoft Power BI. Šios funkcijos padeda užtikrinti, kad vartotojai mato tik Power BI duomenis, kad jie būtų suteikta galimybė naudotis.

<a name="overview"></a>Apžvalga
--------

Pagal **išlaidų apskaitos analizė** Microsoft Power BI turinį naudoja Power BI eilutės lygio saugumo apriboti prieigą. Saugumas yra pagrįstas prieigos lygmens organizacijos hierarchiją, kuri nustatyta sąnaudų apskaitos parametrų. Daugiau informacijos apie su **sąnaudų apskaitos analizės** Power BI turinio, žr [sąnaudų apskaitos analizės Power BI turinys](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Sąranka
Platinti prieigos lygio sauga į Power BI, Power BI turinio savininkas turi atlikite šiuos veiksmus. **Pastaba:** paskelbęs kad **sąnaudų apskaitos analizės** Power BI turinys automatiškai tampa savininku. Tik savininkas nustatyti saugumo, Power BI. Be to, kol savininkas priduria kitas vartotojų PowerBI.com, niekas, išskyrus savininkas galite pamatyti bet kuriuos kitus duomenis į **sąnaudų apskaitos analizės** Power BI turinį.

1.  Publikuoti aprašų failą Power BI.
2.  Prisijungti prie PowerBI.com.
3.  Rasti kad duomenų į **sąnaudų apskaitos analizės** Power BI turinį.
4.  Atidarykite saugos puslapyje. 

    [![Darbo saugos puslapyje](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  Pagal **išlaidų objekto valdytojas** vaidmuo yra jau sukurta. Įtraukti kitų narių, kurie yra dalis sąnaudų apskaitos prieigos lygmens organizacijos hierarchiją. 

    [![Pridedant narius](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Vartotojai, kurie priskirti pagal **išlaidų objekto valdytojas** vaidmuo bus matyti tik tie duomenys, jie gali matyti, pagal apibrėžimą, sąnaudų apskaitos prieigos lygmens organizacijos hierarchiją. **Pastaba:** eilutės lygio saugumo plytelės taikoma ir ataskaitas Microsoft Dynamics 365 operacijoms, kurie įdėti iš Power BI.

## <a name="updating-security"></a>Atnaujinti apsaugos
Jei atnaujinimai yra pagaminti prieigos lygį saugumo kaštų apskaitos ir norite Power BI atspindėti šiuos naujinimus, turite atnaujinti įmonės parduotuvėje, **sąnaudų apskaitos analizės** Power BI turinį. Baigus objekto store atnaujinimas Dynamics 365 operacijoms, turite atnaujinti artefaktus, PowerBI.com. Daugiau informacijos apie tai, kaip padaryti įmonės parduotuvės atnaujinimas, žr [naujinimas subjektas parduotuvėje](power-bi-integration-entity-store.md#update-entity-store). Savininkas, **sąnaudų apskaitos analizės** Power BI turinys turi padaryti įmonės parduotuvė atnaujinti Jei naujiems vartotojams būtų suteikta prieiga prie organizacijos hierarchiją. Be to, savininkas turi pridėti naujų naudotojų prie to **išlaidų objekto valdytojas** vaidmenį PowerBI.com, taip kad eilutės lygio saugumo prašoma juos.

## <a name="disabling-security"></a>Išjungti saugos
Mes manome, kad jūsų organizacija nori apriboti prieigą prie duomenų. Jei dėl kokios nors priežasties, saugumo parametrai yra išjungti paleidus sąnaudų apskaitos, savininkas turi įtraukti vartotojus į su **kaina buhalteris** vaidmenį Power BI vietoj. Jei jūs pakeičiate saugos įgalintą būseną į išjungta, tai gera idėja, kad pašalinti vartotojų iš pagal **išlaidų objekto valdytojas** vaidmenį. Ir atvirkščiai, jei jūs iš naujo įgalinti saugos. Vartotojai gali priklausyti abiem vaidmenis. Bendra prieiga yra abu vaidmenis Sąjungos. Dėl to **sąnaudų apskaitos analizės** Power BI turinio, bendrą prieigą turintys vartotojai gali nevaržomai prieiti prie duomenų. Jei jūsų tikslas turi būti taikomas riboto patekimo, vartotojams turi būti priskirtas tik pagal **išlaidų objekto valdytojas** vaidmenį. Šios eilutės lygio saugos naujinimai įsigaliotų nedelsiant. Nukentėję vartotojai turėtų atnaujinti savo naršykles.

## <a name="additional-resources"></a>Papildomi ištekliai
Norėdami sužinoti daugiau apie Power BI eilutės lygio saugumo, pamatyti [valdyti saugumo modelio, Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


