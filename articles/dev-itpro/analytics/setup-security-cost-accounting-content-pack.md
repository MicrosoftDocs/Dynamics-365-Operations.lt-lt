---
title: "Kaštų apskaitos analizės „Power BI“ turinio saugos nustatymas"
description: "Šioje temoje paaiškinta, kaip Kaštų apskaitoje galite išplatinti prieigos lygio saugą į eilutės lygio saugą in „Microsoft Power BI“. Ši funkcija padeda užtikrinti, kad vartotojai matys tik „Power BI“ duomenis, kuriems matyti prieiga yra suteikta."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 15d25274b02b0e9423fd4670b82c2e398316a1fa
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Kaštų apskaitos analizės „Power BI“ turinio saugos nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinta, kaip Kaštų apskaitoje galite išplatinti prieigos lygio saugą į eilutės lygio saugą in „Microsoft Power BI“. Ši funkcija padeda užtikrinti, kad vartotojai matys tik „Power BI“ duomenis, kuriems matyti prieiga yra suteikta.

<a name="overview"></a>Apžvalga
--------

**Kaštų apskaitos analizė** „Microsoft Power BI“ turinyje naudojama „Power BI“ eilutės lygio sauga vartotojo prieigai apriboti. Sauga pagrįsta prieigos lygio organizacijos hierarchija, kuri nustatyta Kaštų apskaitos parametruose. Išsamesnės informacijos apie **Kaštų apskaitos analizė** „Power BI“ turinį žr. [Kaštų apskaitos analizės „Power BI“ turinys](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Sąranka
Norint paskirstyti prieigos lygio saugą „Power BI“, „Power BI“ turinio savininkas turi atlikti šiuos veiksmus. **Pastaba:** **Kaštų apskaitos analizė** „Power BI“ turinį publikavęs vartotojas automatiškai tampa savininku. Tik savininkas gali nustatyti „Power BI“ saugą. Be to, kol savininkas neįtraukia kitų vartotojų į PowerBI.com, niekas, išskyrus savininką, negali matyti jokių duomenų **Kaštų apskaitos analizė** „Power BI“ turinyje.

1.  Publikuokite apibrėžimo failą į „Power BI“.
2.  Prisijunkite prie PowerBI.com.
3.  Raskite **Kaštų apskaitos analizė** „Power BI“ turinio duomenų rinkinį.
4.  Atidarykite saugos puslapį. 

    ![Saugos puslapio atidarymas](./media/CA-picture-1.png)

5.  **Savikainos objekto valdiklis** vaidmuo jau sukurtas. Įtraukite kitų narių, kurie yra Kaštų apskaitos prieigos lygio organizacijos hierarchijos dalis. 

    ![Narių įtraukimas](./media/CA-picture-2.png)

Į **Savikainos objekto valdiklis** vaidmenį įtraukti vartotojai, matys tik tuos duomenis, kuriuos jiems leidžiama matyti, pagal apibrėžimą Kaštų apskaitos prieigos lygio organizacijos hierarchijoje. **Pastaba:** eilutės lygio sauga taikoma išklotinėms ir ataskaitoms sprendime „Microsoft Dynamics 365 for Finance and Operations“, kurios įdėtos iš „Power BI“.

## <a name="updating-security"></a>Saugos atnaujinimas
Jei atliekama Kaštų apskaitos prieigos lygio saugos atnaujinimų, o jūs norite, kad „Power BI“ atspindėtų šiuos atnaujinimus, turime atnaujinti objekto parduotuvės **Kaštų apskaitos analizė** „Power BI“ turinį. Baigę naujinti objektų saugyklą iš „Finance and Operations“, turite atnaujinti PowerBI.com artefaktus. Išsamesnės informacijos apie tai, kaip atnaujinti objekto parduotuvės saugą, žr. [Objekto parduotuvės atnaujinimas](power-bi-integration-entity-store.md#update-entity-store). **Kaštų apskaitos analizė** „Power BI“ turinio savininkas taip pat turi atnaujinti objekto parduotuvę, jei naujiems vartotojams suteikiama prieiga prie organizacijos hierarchijos. Be to, savininkas turi įtraukti naujus vartotojus į **Savikainos objekto valdiklis** vaidmenį PowerBI.com, kad jiems būtų taikoma eilutės lygio sauga.

## <a name="disabling-security"></a>Saugos išjungimas
Laikome, kad jūsų organizacija nori apriboti duomenų prieigą. Jei dėl tam tikrų priežasčių vykdant Kaštų apskaitą saugos parametrai yra išjungti, savininkas turi įtraukti vartotojus į rolę **Išlaidų buhalteris** „Power BI“. Jei saugą pakeisite iš įgalintos būsenos į išjungtą būseną, pravartu pašalinti vartotojus iš vaidmens **Savikainos objekto valdiklis**. Ir atvirkščiai, jei saugą vėl įgalinsite. Vartotojai gali priklausyti abiems vaidmenims. Bendra prieiga yra abiejų vaidmenų jungtis. **Kaštų apskaitos analizės** „Power BI“ turinio atveju, bendrą prieigą turintys vartotojai turi neribotą duomenų prieigą. Jei norite taikyti apribotą prieigą, vartotojus priskirkite tik vaidmeniui **Savikainos objekto valdiklis**. Šie eilutės lygio saugos naujinimai įsigalioja nedelsiant. Paveikti vartotojai turi atnaujinti savo naršykles.

## <a name="additional-resources"></a>Papildomi ištekliai
Norėdami daugiau sužinoti apie „Power BI“ eilutės lygio saugą žr. [Saugos valdymas savo modelyje „Power BI“](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).




