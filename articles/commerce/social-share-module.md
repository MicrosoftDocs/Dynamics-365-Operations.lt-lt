---
title: „Social Share” modulis
description: Šioje temoje aprašomi „Social Share” moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0e7f30686894f9cf92257e99d95cc8b00f76f899
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234322"
---
# <a name="social-share-module"></a>Bendrinimo socialiniuose tinkluose modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi „Social Share” moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

„Social Share” moduliai leidžia vartotojams bendrinti „e-Commerce” svetainių puslapių URL socialiniuose tinkluose, pvz., „Facebook”, „Twitter”, „Pinterest” ir „LinkedIn”. Svetainių puslapių URL taip pat galima bendrinti el. paštu. „Social Share” moduliai dažniausiai naudojami produkto informacijos puslapiuose (PDP), siekiant padėti vartotojams bendrinti produkto informaciją.

Kiekvienas „Social Share” modulis yra „Social Share” elementų modulių konteineris. Kiekvienas „Social Share” elemento modulis gali būti sukonfigūruotas taip, kad nukreiptų konkrečią socialinės medijos svetainę. Integravimas su „Facebook”, „Twitter”, „Pinterest”, „LinkedIn” ir el. paštu palaikomas iš karto. Kai svetainės vartotojas pasirenka socialinio tinklo simbolį, paleidžiamas HTML „iFrame“ atitinkamai socialinės medijos svetainei. Naudodamas „iFrame” vartotojas gali prisijungti ir užregistruoti peržiūrėtą puslapio turinį.

Kiekviena socialinės medijos platforma gali sekti slapukus, todėl šis modulis reikalauja, kad svetainės vartotojai sutiktų su sutikimo naudoti slapukus pranešimu. Jei nesutinkama naudoti slapukus, modulis bus paslėptas puslapyje. Daugiau informacijos žr. [Slapukų atitiktis](cookie-compliance.md) .

Toliau pateiktoje iliustracijoje pabrėžiamas „Social Share” modulio, naudojamo produkto informacijos puslapyje, pavyzdys.

![„Social Share” modulio pavyzdys](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>„Social Share” modulio ypatybės

| Ypatybės pavadinimas             | Reikšmė                 | aprašymas |
|---------------------------|-----------------------|-------------|
| Antraštė                  | Tekstas | Ši ypatybė nurodo modulio antraštę. |
| Padėtis | **Vertikali** ar **Horizontali**  | Ši ypatybė apibrėžia socialinės medijos elementų maketo padėtį. |

## <a name="social-share-item-module-properties"></a>„Social Share” elementų modulio ypatybės
| Ypatybės pavadinimas             | Reikšmė                 | aprašymas |
|---------------------------|-----------------------|-------------|
| Socialinė medija              | **„Facebook”**, **„Twitter”**, **„Pinterest”**, **„LinkedIn”**, **„Mail“** | Išskleidžiamasis meniu, kuriame yra socialinės medijos platformų sąrašas. |
| Piktograma |Nuotrauka    | Tai bus atitinkamos socialinės medijos rodomas vaizdas. Geriausia būtų kiekvienos platformos vaizdo ieškoti socialinės medijos platformos SDK. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>„Social Share” modulio įtraukimas į pirkimo langelio modulį

Norėdami įtraukti „Social Share” modulį į pirkimo langelio modulį, atlikite toliau pateiktus veiksmus.

1. „Fabrikam” svetainėje pasirinkite **Puslapiai**, tada – puslapį **DefaultPDP**, kad būtų atidarytas produkto informacijos puslapis. 
1. Vietoje **Pirkimo langelis (būtina)** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **„Social Share”**, tada pasirinkite **Gerai**.
1. Vietoje **„Social Share”** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **SocialShare**, tada pasirinkite **Gerai**.
1. Modulio **SocialShare** ypatybių srities dalyje **Padėtis** pasirinkite **Horizontali**. Jei reikia, įtraukite antraštę.
1. Vietoje **SocialShare** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **SocialShareItem**, tada pasirinkite **Gerai**.
1. Modulio **SocialShareItem** ypatybių srities dalyje **Socialinė medija** pasirinkite **„Facebook”**.
1. Modulio **SocialShareItem** ypatybių srities dalyje **Piktograma** pasirinkite **+ Įtraukti vaizdą**.
1. Dialogo lange **Medijos parinkiklis** pasirinkite „Facebook” logotipo vaizdą, tada pasirinkite **Gerai**. Jei nėra „Facebook” logotipo vaizdo, pasirinkite **Įkelti naują medijos elementą**, kad įkeltumėte.
1. Įtraukite ir konfigūruokite papildomus modulius **SocialShareItem** pagal poreikį.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Puslapyje bus rodomas „Social Share” modulis.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Slapukų atitiktis](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]