---
title: Skubus papildymas
description: Šioje temoje aprašoma, kaip galite naudoti skubų papildymą, norėdami papildyti atsargas, kai vietos nurodymui nepavyksta paskirstyti atsargų.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 15a3cc4c50e49a50c354834761425cd107c23a9d79677e022cb1d339bb48c918
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741937"
---
# <a name="immediate-replenishment"></a>Skubus papildymas

[!include [banner](../includes/banner.md)]

Skubus papildymas suteikia galimybę skubiai papildyti atsargas, kai vietos nurodymo eilutei nepavyksta paskirstyti atsargų. Papildymas pagrįstas viena vietos nurodymo sąrankos eilute. Jei nėra atsargų, pateikiamų matavimo vienetu, kuris nurodytas toje eilutėje, to matavimo vieneto papildymas pradedamas iš karto.

Skubus papildymas suteikia alternatyvą metodui, kurį naudojant atsargų paskirstymas pagrįstas didesniu vietos nurodymo eilučių skaičiumi, o poreikis sumuojamas paskirstymo pabaigoje ir papildomas naudojant matavimo vienetą, kuris nurodytas vietos nurodymo paskutinėje eilutėje.

Skubaus papildymo naudojimo nauda yra ta, kad papildymą galima apriboti specialiais vienetais, o kiekį galima nukreipti į tam tikras vietas.

## <a name="business-scenario"></a>Verslo scenarijus

Pavyzdžiui, turite sandėlį, kuriame nustatytos atskiros paėmimo sritys, skirtos matavimo vienetams „dėžė“ ir „vnt.“. Norite optimizuoti išrinkimo procesą paimdami kiek įmanoma daugiau dėžių ir tada paimdami visą likusį kiekį, kuris yra mažesnis nei dėžėje telpantis kiekis, iš srities „vnt.“.

Tokiu atveju galite naudoti skubų papildymą. Vietos nurodyme galite nustatyti skubų dėžių papildymą, kad poreikio papildymas būtų naudojamas iš karto, kai pritrūksta dėžių, kurias galima paimti poreikio kiekiui patenkinti. Tokiu būdu optimizuosite išrinkimo procesą, kad paėmimas apimtų kiek įmanoma daugiau dėžių. Skubus papildymas sukurs dėžių papildymą ir poreikis bus patenkintas, o kiekiai bus paimami naudojant matavimo vienetą „vnt.“. Kitaip tariant, iš srities „vnt.“ bus paimti tik kiekiai, kuriuos reikia paimti iš srities „vnt.“ (t. y. kiekiai, kurie yra mažesni nei viena dėžė). Jei srityje „vnt.“ pasireikš trūkumas, galėsite paimti tiek tik įmanoma dėžių iš viso poreikio. Tada likę kiekiai bus paimti iš srities „vnt.“.

## <a name="where-it-applies"></a>Kai taikoma

Skubus papildymas naudojamas vykdant bangą, jei nepavyksta paskirstyti vietos nurodymo eilutės, kuriai priskirtas papildymo šablonas.

## <a name="set-up-immediate-replenishment"></a>Skubaus papildymo nustatymas

- Pasirinkite **Sandėlio valdymas** \> **Sąranka** \> **Vietos nurodymai**, tada skirtuko **Eilutės** sąraše **Skubaus papildymo šablonas** pasirinkite bangos poreikio papildymo šabloną.

Papildymo šablonas taikomas, jei vietos nurodymo eilutei nepavyksta paskirstyti kiekio naudojant nurodytą matavimo vienetą.

## <a name="troubleshooting"></a>Trikčių šalinimas

Jei vietos nurodymo eilutėje pasirenkamas skubus papildymas, bet nesugeneruojamas joks papildymo darbas, kai naudojate tos vietos nurodymo eilutės poreikio papildymo šablonus, būtina atlikti du pagrindinius veiksmus.

- Įsitikinkite, kad taikomas poreikio papildymo šablonas nustatytas naudoti teisingus tipo **Papildymas** vietos šablonus ir darbo šablonus.
- Įsitikinkite, kad turimų atsargų pakanka vietose, kuriose poreikio papildymo šablonas ieško turimų papildymo atsargų.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]