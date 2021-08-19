---
title: Akordeono modulis
description: Šioje temoje aprašomi akordeono moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fa2515a0cbc5b69a1a69e15ec9e1ba2739fa2fbeffb5b0eb22b49fd8cab18e6f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719532"
---
# <a name="accordion-module"></a>Akordeono modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi akordeono moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

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
1. **Numatytojo puslapio** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Akordeonas**, tada pasirinkite **Gerai**.
1. Akordeono modulio ypatybių srityje, šalia pieštuko simbolio, pasirinkite **Antraštė**.
1. Dialogo lange **Antraštė**, dalyje **Antraštės tekstas**, įveskite **Dažnai užduodami klausimai**. Tada pasirinkite **Gerai**.
1. Akordeono modulio ypatybių srityje pažymėkite žymės langelį **Rodyti „išplėsti viską“**, o tada laukelyje **Sąveikos stilius** pasirinkite **Nepriklausoma**.
1. Vietoje **Akordeonas** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Akordeono elementas**, tada pasirinkite **Gerai**.
1. Akordeono elementų modulio ypatybių srityje, dalyje **Pavadinimas**, įveskite pavadinimo tekstą (pavyzdžiui, **Kaip veikia grąžinimas?**).
1. Vietoje **Akordeono elementas** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Teksto blokas**, tada pasirinkite **Gerai**.
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