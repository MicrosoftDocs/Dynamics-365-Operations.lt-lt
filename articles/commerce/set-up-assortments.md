---
title: Asortimento nustatymas
description: Šiame straipsnyje aprašyta, kas yra asortimentas ir paaiškinta, kaip asortimentus nustatyti sprendime „Dynamics 365 Commerce“.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d61addbc4eac691351c2d8cac013c9d94bd900e9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264605"
---
# <a name="set-up-assortments"></a>Asortimentų nustatymas

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašyta, kas yra asortimentas ir paaiškinta, kaip asortimentus nustatyti sprendime „Dynamics 365 Commerce“.

Asortimentas yra susijusių produktų, kuriuos priskiriate prekybos kanalui, pvz., plytos ir skiedinys sandėlyje arba internetinėje parduotuvėje, rinkinys. Asortimentą galite naudoti identifikuoti produktams, kurie yra kiekvienoje parduotuvėje. Galite naudoti asortimentą identifikuoti produktus, kurie yra kiekvienoje parduotuvėje. Asortimente gali būti produktų kategorijos. Todėl visi konkrečiai kategorijai priskirti produktai yra įtraukti į asortimentą. Asortimentas taip pat gali apimti konkrečius produktus ir konkrečius produktų variantus. Kurdami asortimentą, tuo pat metu galite priskirti tūkstančius produktų savo kanalams, bet kartu ir visus derinius, kurių reikia jūsų parduotuvėms. Galite nustatyti tiek produktų asortimente, kiek jums reikia. Kiekvieną produktą galima įtraukti į vieną ar daugiau asortimentų, o kiekvieną asortimentą galima priskirti vienam ar keliems kanalams. Pavyzdžiui, nustatykite vieną asortimentą, kuris apima bazinį produktų rinkinį. Šį asortimentą gauna visos parduotuvės. Tada nustatykite kitą asortimentą, kuris apima tik didelę sporto įrangą. Šį asortimentą gauna tik didesnės parduotuvės. Toliau pateikiamoje diagramoje parodyta, kaip priskirti produktus asortimentui ir kaip asortimentus priskirti kanalams.

![Prekių asortimento ryšiai](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš sukurdami asortimentą ir priskirdami jį prekybos kanalui, turite atlikti nurodytas užduotis.

| Užduotis                              | Aprašymas |
|-----------------------------------|-------------|
| Kanalo nustatymas.          | Kanalai skirti plytų ir skiedinio parduotuvei, internetinei parduotuvei arba internetinei prekyvietei. Turite sukurti bent vieną kanalą ir sukonfigūruoti parduotuvės parinktis. Asortimentai priskiriami parduotuvėms, kad būtų galima identifikuoti parduotuvės produktus. |
| Sukurkite organizacijos hierarchiją. | Sukūrę savo organizacijos prekybos kanalą, turite sukonfigūruoti organizacijos hierarchiją, kuri atitinka jūsų kanalo organizacinę struktūrą. Organizacijos hierarchiją galima naudoti asortimentams, prekių papildymui ir ataskaitoms. Pridėdami savo kanalus į organizacijos hierarchiją, galite priskirti asortimentus parduotuvių grupėms. Užuot priskyrus asortimentą atskirai kiekvienai parduotuvei, galite priskirti asortimentą aukšto lygio organizacijos mazgui. Tada, kaskart pridedant naują kanalą į aukšto lygio organizacijos mazgą, kanalas automatiškai gauna visus asortimentus, kurie buvo priskirti aukštesnio lygio organizacijos mazgui. Asortimentus galite priskirti tik tiems kanalams, kurie yra įtraukti į organizacijos hierarchiją, kuri yra priskirta **Prekybos asortimento** tikslu. |
| Nustatykite produktus.                  | Prieš įtraukdami produktus į asortimentą, turite įtraukti juos programoje „Commerce“. Produktus galite pridėti rankiniu būdu arba importuoti iš tiekėjo. Pridėję produktus, turite išleisti juos juridiniam asmeniui. Jūsų kanaluose gali būti tik juridiniam asmeniui išleisti produktai. Produktus, kurie dar neišleisti juridiniam asmeniui, galima pridėti prie asortimento ir asortimentą galima patvirtinti. Tačiau kol produktai bus išleisti juridiniam asmeniui, jų negalima pateikti į kanalus. |
| Nustatykite kategorijos hierarchiją.      | Kurdami savo prekybos produktus, juos grupuoti ir suskirstyti galite naudodami kategorijų hierarchijos funkciją. Galite sukurti vieną pagrindinę hierarchiją visų produktų, kuriuos platinate savo kanalais, grupavimui ir skirstymui. Taip pat galite kurti atskiras, papildomas kategorijų hierarchijas grupuoti arba skirstyti savo produktus specialiais tikslais, pavyzdžiui, akcijoms arba asortimentams. Naudodami kategorijų hierarchijas, galite priskirti visus produktus, tam tikrai kategorijai į asortimentą. Bet kurie produktai, kurie pridedami į asortimente esančią kategoriją, yra automatiškai įtraukiami į asortimentą. Tada kitą kartą paleidžiant prekybos asortimentą, šie produktai bus prieinami kanaluose, kuriems yra priskirtas asortimentas. |

## <a name="setting-up-an-assortment"></a>Asortimento nustatymas

Baigę skirstyti, galite sukurti asortimentą ir priskirti jį savo kanalams. Norėdami sudaryti asortimentą, turite atlikti toliau nurodytas užduotis.

1. Sukurkite naują asortimentą arba nukopijuokite esamą asortimentą.
2. Pasirinkite kanalus arba aukšto lygio kanalų grupes, kurioms taikomas asortimentas.
3. Pridėti produktų kategorijas, atskirus produktus ar produktų variantus į asortimentą. Galite įtraukti visus produktus į tam tikrą kategoriją arba pašalinti pasirinktus produktus iš kategorijos, kuri yra įtraukta į asortimentą.
4. Paskelbkite asortimentą. Paskelbus asortimentą, automatiškai paleidžiama asortimento planuoklė. Šis procesas generuoja produktų sąrašą. Baigus procesą, produktai tampa prieinami kanaluose, kuriems yra priskirtas asortimentas. Jei daromi paskelbto asortimento pakeitimai arba keičiami kanalai, kuriems priskirtas asortimentas, jis turi būti atnaujintas. Norėdami atnaujinti asortimentą po pakeitimų, galite paleisti asortimento planuoklę kaip paketinę užduotį.


[!INCLUDE[footer-include](../includes/footer-banner.md)]