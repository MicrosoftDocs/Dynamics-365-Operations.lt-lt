---
title: NF-e XML failų kaip priedų perkėlimas
description: Šiame straipsnyje paaiškinama, kaip perkelti NF-e XML Microsoft Dynamics failus iš savo 365 finansų ar duomenų Dynamics 365 Supply Chain Management bazės ir padaryti juos prieinamus kaip priedus.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ce9061896759efeb8e8960e84656d5fc1f0616ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877903"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>NF-e XML failų kaip priedų perkėlimas

[!include [banner](../includes/banner.md)] 


Kai išduodami elektroniniai finansiniai dokumentai (NF-e), XML Microsoft Dynamics failai sukuriami ir saugomi 365 finansų ir duomenų Dynamics 365 Supply Chain Management bazėse. Brazilijos lokalizavimo metu, norėdami **atlaisvinti duomenų bazės vietą, kurią naudos tie XML failai, galite naudoti NF-e XML** perkėlimo kaip priedo priemonę.

Tam tikro datų diapazono ir finansinio subjekto atveju funkcija perkelia NF-e XML failus iš jūsų finansų arba tiekimo grandinės valdymo duomenų bazės į BLOB saugyklą iš "Azure" abonemento. Šis perkėlimas leidžia failus naudoti tik kaip priedus. Kai XML failai sėkmingai perkeliami į BLOB saugyklą, pradiniai failai panaikinami iš finansų arba tiekimo grandinės valdymo duomenų bazės. Todėl duomenų bazės tarpas, kurį naudoja šie failai, yra išleidžiamas.

Norėdami įgalinti NF-e **XML perkėlimo kaip priedo priemonę, atlikite šiuos** veiksmus.

1. Finansų arba tiekimo grandinės valdymo srityje atidarykite **funkcijų valdymo** darbo sritį.
2. Skirtuke **Visi** ieškokite ir pasirinkite **NF-e XML, perkelti kaip priedo** priemonę.
3. Pasirinkite **Įjungti dabar**.

Norėdami PERKELTI NF-e XML failus kaip priedus, atlikite šiuos veiksmus.

1. Eiti į gautinų **sumų** \> **finansinius dokumentus Elektroniniai** \> **finansiniai** \> **dokumentai Perkelkite NF-e XML kaip priedus.**
2. Laukuose **Nuo datos** ir **Iki** datos pasirinkite pradžios ir pabaigos datas.
3. Lauke Finansinio **personalo ID** pasirinkite vertę.
4. Pasirinkite **Gerai**.

> [!IMPORTANT]
> Šio proceso negalima atšaukiama. Kai perkeliate NF-e XML failus, vartotojai gali juos peržiūrėti **tik** finansinio dokumento puslapio **viršuje pasirinkdami** Priedai.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
