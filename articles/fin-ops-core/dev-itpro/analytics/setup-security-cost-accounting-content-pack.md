---
title: Kaštų apskaitos analizės „Power BI“ turinio apsaugos nustatymas
description: Šiame straipsnyje paaiškinama, kaip išplatinti prieigos lygio saugą kaštų apskaitoje į eilučių lygio saugą Microsoft Power BI.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.openlocfilehash: 9f019bec9c28602e31b43a8b3ab820f4a3a31ee8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267939"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Kaštų apskaitos analizės „Power BI“ turinio apsaugos nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip išplatinti prieigos lygio saugą kaštų apskaitoje į eilučių lygio saugą Microsoft Power BI. Ši funkcija padeda užtikrinti, kad vartotojai matys tik „Power BI“ duomenis, kuriems matyti prieiga yra suteikta.

## <a name="overview"></a>Peržiūra

„Microsoft Power BI“ turinys **Kaštų apskaitos analizė** naudoja „Power BI“ eilutės lygio saugą vartotojo prieigai apriboti. Sauga pagrįsta prieigos lygio organizacijos hierarchija, kuri nustatyta Kaštų apskaitos parametruose. Išsamesnės informacijos apie „Power BI“ turinį **Kaštų apskaitos analizė** žr. [„Power BI“ turinys Kaštų apskaitos analizė](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Sąranka
Norint paskirstyti prieigos lygio saugą „Power BI“, „Power BI“ turinio savininkas turi atlikti šiuos veiksmus.

> [!NOTE]
> „Power BI“ turinį **Kaštų apskaitos analizė** publikavęs vartotojas automatiškai tampa savininku. Tik savininkas gali nustatyti „Power BI“ saugą. Be to, kol savininkas neįtraukia kitų vartotojų į PowerBI.com, niekas, išskyrus savininką, negali matyti jokių duomenų „Power BI“ turinyje **Kaštų apskaitos analizė**.

1. Publikuokite apibrėžimo failą į „Power BI“.
2. Prisijunkite prie PowerBI.com.
3. Raskite „Power BI“ turinio **Kaštų apskaitos analizė** duomenų rinkinį.
4. Atidarykite saugos puslapį.

    ![Saugos puslapio atidarymas.](./media/CA-picture-1.png)

5. **Savikainos objekto valdiklis** vaidmuo jau sukurtas. Įtraukite kitų narių, kurie yra Kaštų apskaitos prieigos lygio organizacijos hierarchijos dalis.

    ![Narių įtraukimas.](./media/CA-picture-2.png)

Į **Savikainos objekto valdiklis** vaidmenį įtraukti vartotojai, matys tik tuos duomenis, kuriuos jiems leidžiama matyti, pagal apibrėžimą Kaštų apskaitos prieigos lygio organizacijos hierarchijoje.

> [!NOTE]
> Eilutės lygio sauga taikoma išklotinėms ir ataskaitoms, kurios įdėtos iš „Power BI“.

## <a name="updating-security"></a>Saugos atnaujinimas
Jei atliekama Kaštų apskaitos prieigos lygio saugos atnaujinimų, o jūs norite, kad „Power BI“ atspindėtų šiuos atnaujinimus, turime atnaujinti objekto parduotuvės „Power BI“ turinį **Kaštų apskaitos analizė**. Baigę naujinti objektų saugyklą, turite atnaujinti PowerBI.com artefaktus. Daugiau informacijos apie tai, kaip naujinti objekto parduotuvės saugą, žr. [„Power BI“ integravimas su objekto parduotuve](power-bi-integration-entity-store.md#update-entity-store). „Power BI“ turinio **Kaštų apskaitos analizė** savininkas taip pat turi atnaujinti objekto parduotuvę, jei naujiems vartotojams suteikiama prieiga prie organizacijos hierarchijos. Be to, savininkas turi įtraukti naujus vartotojus į **Savikainos objekto valdiklis** vaidmenį PowerBI.com, kad jiems būtų taikoma eilutės lygio sauga.

## <a name="disabling-security"></a>Saugos išjungimas
Laikome, kad jūsų organizacija nori apriboti duomenų prieigą. Jei dėl tam tikrų priežasčių vykdant Kaštų apskaitą saugos parametrai yra išjungti, savininkas turi įtraukti vartotojus į „Power BI“ **Išlaidų buhalteris**. Jei saugą pakeisite iš įgalintos būsenos į išjungtą būseną, pravartu pašalinti vartotojus iš vaidmens **Savikainos objekto valdiklis**. Ir atvirkščiai, jei saugą vėl įgalinsite. Vartotojai gali priklausyti abiems vaidmenims. Bendra prieiga yra abiejų vaidmenų jungtis. „Power BI“ turinio **Kaštų apskaitos analizė** atveju bendrą prieigą turintys vartotojai turi neribotą duomenų prieigą. Jei norite taikyti apribotą prieigą, vartotojus priskirkite tik vaidmeniui **Savikainos objekto valdiklis**. Šie eilutės lygio saugos naujinimai įsigalioja nedelsiant. Paveikti vartotojai turi atnaujinti savo naršykles.

## <a name="additional-resources"></a>Papildomi ištekliai
Norėdami daugiau sužinoti apie „Power BI“ eilutės lygio saugą žr. [Saugos valdymas savo modelyje „Power BI“](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
