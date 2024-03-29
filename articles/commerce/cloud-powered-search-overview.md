---
title: Debesų technologija valdomos ieškos apžvalga
description: Šiame straipsnyje pateikta ieška debesyje Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273672"
---
# <a name="cloud-powered-search-overview"></a>Debesų technologija valdomos ieškos apžvalga

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikta ieška debesyje Microsoft Dynamics 365 Commerce.

Produktų aptinkamumas padeda užtikrinti, kad vartotojai galėtų greitai ir lengvai rasti produktus naršydami kategorijas, ieškodami bei filtruodami. Mažmenininkai turi galimybę surasti produktą ir naudoti pagrindinį kliento sąveikos įrankį kanaluose, kurie veikia naudojant debesų skalės vienetą (CSU), pvz., el. prekyba ir point of sale (EKA).

Klientai yra įpratę prie beveik momentinio interneto ieškos modulių atsako laiko, įmantrių el. prekybos svetainių, socialinės medijos programų, automatinių pasiūlymų, kurie rodomi vedant ieškos terminus, ypatybėmis pagrįsto naršymo ir paryškinimo. Jei klientai nepavyksta greitai rasti produkto, kurį jie ieško vienoje el. komercijos parduotuvėje, jie nepasitenką eiti į kitą el. komercijos parduotuvę.

"Commerce" leidžia aptikti debesyje galimus produktus, todėl mažmenininkai toliau gali padidinti vartotojo užlaikymo ir konvertavimo rodiklius kanaluose, kurie veikia CSU.

"Commerce Search" naudojimo patirtis pagerina pajėgumus, kurie padeda mažmenininkams pasiekti, kad produktai būtų lengviau atrasti. Tuo pat metu šios galimybės užtikrina el. prekybos srautui reikalingą keičiamumą ir našumą.

## <a name="browse-and-search"></a>Naršymas ir ieška

Ieškos aktualumas ir našumas yra pagrindiniai daugiakanalės platformos patirties veiksniai, nes produktų aptikimas pirmiausia priklauso nuo ieškos funkcijos informacijai gauti bei turiniui naršyti. Efektyvus naršymas ir ieška padeda padidinti konvertavimo rodiklį.

Toliau pateiktoje iliustracijoje parodytas įprastų naršymo ir ieškos funkcijų pavyzdys.

![Ieškos nukreipimo puslapis.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Ypatybėmis pagrįstas naršymas ir pasirinkimų suvestinė 

Ypatybėmis pagrįsto naršymo galimybė klientams padeda lengviau ieškoti turinio, nes leidžia filtruoti tikslinimo priemones, susietas su terminų rinkinio terminais. Klientui pasirinkus ir pritaikius tikslinimo priemones, rodoma pasirinkimų suvestinė. 

Naudodami ypatybėmis pagrįsto naršymo funkciją, skirtingiems terminų rinkinio terminams galite sukonfigūruoti skirtingas tikslinimo priemones, ir nereikia kurti papildomų puslapių. 

Toliau pateiktoje iliustracijoje parodytas pavyzdys, kai ieškant naudojama ypatybėmis pagrįsto naršymo funkcija.

![Pasirinkimų suvestinė.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Įtraukianti automatinio siūlymo funkcija

Dabartinė automatinė funkcija rodo raktažodžius, kurie suaktyvina ieškoti atitinkančio raktažodžio. Dėl naujų Komercijos patobulinimų klientai dažnai gali atrasti saitus su produktais prieš jiems įvedant.

"Commerce" taip pat palaiko raktažodžių atitikmenų funkcijas įvairiose kategorijose. Naudodami šias funkcijas klientai gali matyti sutampančių raktažodžių įvairiose kategorijose skaičių ir suaktyvinti raktažodžių iešką kitose kategorijose.

Toliau pateiktoje iliustracijoje parodytas pavyzdys, kuriame naudojama įtraukianti automatinio siūlymo funkcija.

![įtraukianti automatinio siūlymo funkcija.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Rūšiuoti

Rūšiavimo funkcijos leidžia klientams rūšiuoti, ieškoti ir naršyti kategorijų rezultatus bei patikslinti juos pagal, pvz., kainą, produkto pavadinimą ir produkto numerį. Jei jūsų aplinkoje [įgalinsite](product-recommendations.md) produkto rekomendacijas, klientai taip pat gali rūšiuoti rezultatus pagal išplėstinius rūšiavimo kriterijus, pvz., naują, geriausią pardavimą ir tendenciją.


> [!NOTE]
> Šios debesų kompiuterijos ieškos galimybės prieinamos 10.0.8 versijoje. Įsitikinkite, kad yra įrašas "ProductSearch.UseAzureSearch" ir "Commerce Parameters" nustatytas kaip "true" **> konfigūracijos parametrai**. 
![Konfigūracijos parametrai debesies aplinkos ieškoje.](./media/CloudPoweredSearchConfigurationParameters.png)
>Išplėstinės rūšiavimo pasirinktys, pvz., naujas, geriausias pardavimas ir tendencija, galimos su "Commerce SSK" versija 9.35+ Dynamics 365 Commerce ir 10.0.20 paleidimu.  


## <a name="additional-resources"></a>Papildomi ištekliai

[Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga](category-search-page-overview.md)

[Tvarkyti SEO metaduomenis](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
