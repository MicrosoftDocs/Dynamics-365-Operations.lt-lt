---
title: Akordeono modulis
description: Šiame straipsnyje aprašomi turimi moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: ec895476770f297825d6c88d0b0a5fef43a5c6ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279162"
---
# <a name="accordion-module"></a>Akordeono modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi turimi moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Akordeono moduliai yra į talpyklas panašūs moduliai, kurie naudojami organizuojant informaciją arba modulius puslapyje ir kurie suteikia sutraukiamus stalčius primenančią funkciją. Akordeono modulis gali būti naudojamas bet kuriame puslapyje.

Kiekviename akordeono modulyje galima įtraukti vieną ar daugiau akordeono elementų modulių. Kiekvienas akordeono elementų modulis vaizduoja sutraukiamą stalčių. Kiekviename akordeono elementų modulyje galima įtraukti vieną ar daugiau modulių. Modulių, kuriuos galima įtraukti į akordeono elementų modulį, tipų apribojimų nėra.

Toliau pateiktame paveikslėlyje parodytas akordeono modulio, kuris naudojamas parduotuvės dažnai užduodamų klausimų (DUK) puslapyje esančiai informacijai tvarkyti, pavyzdys.

![Akordeono modulio pavyzdys.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Akordeono modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Antraštė | Tekstas | Ši ypatybė nurodo pasirinktinę akordeono modulio teksto antraštę. |
| Išplėsti viską | **Teisinga** arba **Klaidinga** | Jei reikšmė nustatyta kaip **Teisinga**, išplėtimo / sutraukimo funkcija yra įjungta ir visi akordeono modulyje esantys elementai gali būti išplėsti ir sutraukti. |
| Sąveikos stilius | **Nepriklausoma** arba **Išplėsti tik vieną elementą** | Ši ypatybė apibrėžia akordeono elementų sąveikos stilių. Jei vertė nustatyta kaip **Nepriklausoma**, kiekvieną akordeono elementą galima atskirai išplėsti arba sutraukti. Jei reikšmė nustatyta kaip **Išplėsti tik vieną elementą**, vienu metu galima išplėsti tik vieną elementą. Išplėtus elementus, anksčiau išplėsti elementai yra sutraukiami. |

## <a name="accordion-item-module-properties"></a>Akordeono elementų modulio ypatybės

| Ypatybės pavadinimas | Reikšmės | aprašymas |
|----------------|--------|-------------|
| Kreipinys | Tekstas | Ši ypatybė nurodo akordeono elementų modulio pavadinimo tekstą. Pasirinkus pavadinimo sritį vartotojai gali išplėsti arba sutraukti sekciją. |
| Išplėsti pagal numatytuosius parametrus | **Teisinga** arba **Klaidinga** | Jei vertė nustatyta kaip **Teisinga**, pagal numatytąsias nuostatas akordeono elementas išskleidžiamas, kai puslapis įkeliamas. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Akordeono modulio įtraukimas į DUK puslapį

Norėdami į DUK puslapį įtraukti akordeono modulį ir nustatyti jo reikiamas ypatybes svetainių daryklėje, atlikite tolesnius veiksmus.

1. Eikite į **Puslapiai** ir naudokitės „Fabrikam“ rinkodaros šablonu (ar bet kokiu kitu šablonu be apribojimų), kad sukurtumėte naują puslapį su pavadinimu **Parduotuvės DUK**.
1. Numatytojo **puslapio** pagrindiniame atrinkinyje **pasirinkite** daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite modulį **Laukimas**, tada pasirinkite **Gerai**.
1. Akordeono modulio ypatybių srityje, šalia pieštuko simbolio, pasirinkite **Antraštė**.
1. Dialogo lange **Antraštė**, dalyje **Antraštės tekstas**, įveskite **Dažnai užduodami klausimai**. Tada pasirinkite **Gerai**.
1. Akordeono modulio ypatybių srityje pažymėkite žymės langelį **Rodyti „išplėsti viską“**, o tada laukelyje **Sąveikos stilius** pasirinkite **Nepriklausoma**.
1. Iš laiko **atminties** atminties pasirinkite daugtaškį (**...**), tada pasirinkite Pridėti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite prekių modulį **Laukimas**, tada pasirinkite **Gerai**.
1. Akordeono elementų modulio ypatybių srityje, dalyje **Pavadinimas**, įveskite pavadinimo tekstą (pavyzdžiui, **Kaip veikia grąžinimas?**).
1. Prekių laiko **atminties laiko** atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Pridėti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Teksto blokas**, tada – **Gerai**.
1. Teksto bloko modulio ypatybių srityje įveskite teksto pastraipą (pvz., **Grąžinimai turi būti apdorojami skambučių centre. Dėl grąžinimo skambinkite 1-800-FABRIKAM. Gaminiams taikoma 30 dienų grąžinimo strategija. Dėl grąžinimo reikia kreiptis per šį laikotarpį.**).
1. Vietoje **Akordeonas** pridėkite dar kelis akordeono elementų modulius. Kiekviename akordeono elementų modulyje pridėkite tekstinio bloko modulį, kuriame yra turinio.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Puslapyje bus rodomas akordeono modulis, kuriame yra jūsų įtrauktas turinys.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Skirtuko modulis](add-tab.md)

[Teksto bloko modulis](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
