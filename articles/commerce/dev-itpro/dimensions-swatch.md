---
title: Konfigūruoti produkto dimensijų reikšmes, kad jos būtų rodomos kaip pavyzdžiai
description: Šioje temoje aprašoma, kaip konfigūruoti produkto dimensijų reikšmes kaip pavyzdžius „Microsoft Dynamics 365 Commerce” būstinėje.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.20 update
ms.openlocfilehash: 4ffbb6a162e87fd19cdb44224adc8c223ba8e903
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638299"
---
# <a name="configure-product-dimension-values-to-appear-as-swatches"></a>Konfigūruoti produkto dimensijų reikšmes, kad jos būtų rodomos kaip pavyzdžiai

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip konfigūruoti produkto dimensijų reikšmes kaip pavyzdžius „Microsoft Dynamics 365 Commerce” būstinėje. Daugiau informacijos apie produkto dimensijas rasite [Produkto dimensijos](../../supply-chain/pim/product-dimensions.md).

„Dynamics 365 Commerce” palaiko dydžio, stiliaus ir spalvos dimensijų naudojimą, kad būtų galima atspindėti produkto variantus. Produkto dimensijos turi draugiškus pavadinimus, rodomus produkto informacijos puslapiuose (PDP), kad būtų galima pasirinkti produkto variantus. Šių draugiškų pavadinimų pavyzdžiai yra „Mažas”, „Vidutinis” ir „Didelis” – dydžiams, o spalvoms – „Juoda” ir „Ruda”. Tačiau tuo atveju, jei produktas palaiko daugybę variantų, reikia kelių pasirinkimų kiekvienam produkto variantui peržiūrėti. Tačiau vartotojams gali būti lėta ir nuobodu naršyti bei rinktis produkto variantus.

Kai dimensijos yra rodomos kaip pavyzdžiai PDP puslapiuose, klientams pateikiamos produktų variantų vaizdinės peržiūros versijos. Jie gali lengvai naršyti didžiulį spalvų, raštų ir tekstūrų pasirinkimą, bei greitai peržiūrėti skirtingus produkto variantų derinius.

Dimensijų rodymo kaip pavyzdžių funkcija įgalina „Commerce” naudoti šešioliktainius („hex”) kodus ir vaizdus dimensijų rodymui kaip pavyzdžių. Be to, panašios dimensijos, pavyzdžiui, spalvos, gali būti sugrupuotos produktų sąrašo puslapiuose. Pavyzdžiui, klientas ieško mėlynos spalvos produktų. Jei įvairios mėlynos spalvos dimensijos reikšmės yra sugrupuojamos kartu, ieškos rezultatai rodys produktus, turinčius skirtingus mėlynos atspalvius. Dimensijos grupavimas žymiai pagerina produkto tikslinimo patirtį ir padeda klientams rasti daugiau produktų naudojant vieną produkto ieškos užklausą.

> [!NOTE]
> Dimensijų rodymo kaip pavyzdžių funkcija yra prieinama „Dynamics 365 Commerce“ 10.0.20 versijos leidime.

Toliau pateiktoje iliustracijoje rodomas pavyzdys, kuriame spalvos rodomos kaip pavyzdžiai „Commerce“ PDP puslapyje.

![Spalvų, rodomų kaip pavyzdžiai produkto informacijos puslapyje, pavyzdys.](../dev-itpro/media/swatch_pdp.png)

Toliau pateiktoje iliustracijoje rodomas pavyzdys, kuriame spalvos rodomos kaip pavyzdžiai „Commerce“ ieškos rezultatų sąrašo puslapyje.

![Spalvų, rodomų kaip pavyzdžiai ieškos rezultatų sąrašo puslapyje, pavyzdys.](../dev-itpro/media/swatch_searchresults.PNG)

## <a name="enable-the-display-dimensions-as-swatches-feature-in-commerce-headquarters"></a>Dimensijų rodymo kaip pavyzdžių funkcijos įgalinimas „Commerce“ būstinėje

Norėdami įgalinti dimensijų rodymo kaip pavyzdžių funkciją „Commerce“ būstinėje, eikite į **Darbo sritys \> Funkcijos valdymas** ir įjunkite **Įgalinti vaizdo palaikymą produkto dimensijos reikšmėms** funkciją. Kai šios funkcijos vėliavėlė įjungta, kiekvienai dimensijai įtraukiami trys nauji laukai į atitinkamas lenteles „Commerce” būstinėje: **Šešioliktainis kodas**, **URL (vaizdams)** ir **Tikslinimo priemonės grupė**.

## <a name="configure-dimension-values-in-commerce-headquarters"></a>Dimensijos reikšmių konfigūravimas „Commerce” būstinėje

Dimensijų rodymo kaip pavyzdžių funkcija yra palaikoma dydžio, stiliaus ir spalvos dimensijoms. Šešioliktainio kodo ir vaizdo URL reikšmės atitinkamoms dimensijoms gali būti nurodytos „Commerce” būstinėje. Pagal numatytuosius nustatymus, jeigu šešioliktainio kodo ir vaizdo URL reikšmės nėra pateiktos dimensijai, sistema parodys dimensijos draugiško pavadinimo tekstą.

Konfigūravimas gali būti atliekamas bet kuriuo iš toliau pateiktu lygiu:

- **Dimensijos** – „Commerce” būstinėje atidarykite dimensijos puslapį ieškodami **Spalvos**, **Dydžio** arba **Stiliaus**. Kiekvieno puslapio tinklelyje pateikiamos dimensijų reikšmės. Galite valdyti rodymo tvarkos, šešioliktainio kodo ir vaizdo URL reikšmes. Toliau pateiktoje iliustracijoje rodoma pavyzdinė konfigūracija **Spalvų** puslapyje.

    ![Dimensijos konfigūracijos pavyzdys Spalvų puslapyje.](../dev-itpro/media/swatch_Color.PNG)

- **Dimensijų grupė** – „Dynamics 365 Commerce” platformoje galite naudoti **Tikslinimo priemonės grupės** ypatybę dimensijų grupių kūrimui. Jei dimensijų grupės yra apibrėžtos, atidarykite atitinkamą puslapį ieškodami **Spalvų grupės**, **Dydžių grupės** arba **Stilių grupės**. Dimensijos – „Commerce” būstinėje atidarykite dimensijos puslapį ieškodami Spalvos, Dydžio arba Stiliaus. Toliau pateiktoje iliustracijoje rodoma pavyzdinė konfigūracija **Spalvų grupių** puslapyje.

    ![Dimensijos konfigūracijos pavyzdys Spalvos grupių puslapyje.](../dev-itpro/media/swatch_colorGroup.PNG)

- **Produkto dimensija (produkto kūrimo metu)** – Kurdami naują produktą, galite naudoti **Produkto dimensijų** puslapį dimensijų reikšmių įvedimui. Esamiems produktams jau gali būti nustatyti **Šešioliktainio kodo**, **URL (vaizdams)** ir **Tikslinimo** laukai. Tačiau reikšmes galite keisti taip, kaip jums reikia. Toliau pateiktoje iliustracijoje rodoma pavyzdinė konfigūracija **Produkto dimensijų** puslapyje.

    ![Dimensijos konfigūracijos pavyzdys Produkto dimensijų puslapyje.](../dev-itpro/media/swatch_product_dimensions.PNG)

> [!NOTE]
> Šešioliktainio kodo ir vaizdo URL konfigūracijų procesas vyksta tuo pačiu principu, kuris yra naudojamas dimensijų rodymo tvarkos valdymui.

## <a name="configure-dimension-values-by-using-hex-codes"></a>Dimensijos reikšmių konfigūravimas naudojant šešioliktainius kodus

Daugeliui spalvos dimensijų turi būti pateikta šešioliktainio kodo spalvos reikšmė dimensijos puslapiuose „Commerce” būstinėje. Pavyzdžiui, juoda spalva turi turėti šešioliktainio kodo reikšmę **„#00000”**. Kai „Commerce” sugeneruoja svetainės puslapį, šešioliktainį kodą atvaizduoja spalvos pavyzdys.

Toliau pateiktoje iliustracijoje rodomas pavyzdys, kuriame spalvos dimensijos yra konfigūruojamos naudojant šešioliktainio kodo reikšmes.

![Dimensijos konfigūracijos, naudojančios šešioliktainius kodus, pavyzdys.](../dev-itpro/media/swatch_color_hexcode.png)

## <a name="configure-dimension-values-by-using-image-urls"></a>Dimensijų reikšmių konfigūravimas naudojant vaizdo URL

Kai kurios spalvos dimensijos atspindi raštus, o ne vientisas spalvas. Pavyzdžiui, spalvos dimensija gali būti apibrėžta kaip „leopardo.” Tokiais atvejais galite efektyviau atvaizduoti spalvos dimensijas, jei pavyzdžiams naudosite publikuotus vaizdus, o ne šešioliktainius kodus.

Turite įkelti kiekvieną vaizdą į „Commerce” svetainių daryklę ir jį publikuoti. Tada įveskite vaizdo URL publikuotam vaizdui atitinkamose dimensijos puslapiuose „Commerce” būstinėje. Jei dimensija buvo pasirinkta rodymui kaip pavyzdys, tačiau šešioliktainis kodas nėra apibrėžtas, „Commerce” atliks vaizdo peržvalgą, kai generuos puslapį. Jei vaizdo peržvalga nepavyksta, „Commerce” parodys dimensijos draugiško pavadinimo tekstą.

Toliau pateiktoje iliustracijoje rodomas pavyzdys, kuriame vaizdo URL yra naudojami konfigūracijai **Spalvų** puslapyje.

![Dimensijos konfigūracijos, naudojančios vaizdo URL, pavyzdys.](../dev-itpro/media/swatch_color_urls.PNG)

Galite naudoti laikmenos šabloną vaizdo URL apibrėžti taip pat, kaip ir galite jį naudoti produkto ir kategorijos vaizdams. Kai keliate vaizdus į svetainių daryklę, failo pavadinimo konvencijos ir failo keliai turi būti nuoseklūs.

Toliau pateiktoje iliustracijoje rodomas pavyzdys, kuriame vaizdo URL yra naudojami laikmenos šablono konfigūracijai.

![Laikmenos šablono konfigūracijos pavyzdys.](../dev-itpro/media/swatch_media_template.PNG)

## <a name="configure-dimension-values-by-using-both-hex-codes-and-image-urls"></a>Dimensijų reikšmių konfigūravimas naudojant tiek šešioliktainius kodus, tiek vaizdo URL

Daugelį spalvų dimensijų galite konfigūruoti tiek šešioliktainiais kodais, tiek vaizdo URL. „Commerce” generavimo atsarginė logika automatiškai ieškos šešioliktainio kodo arba vaizdo URL spalvos pavyzdžiui rodyti. Naudodami tiek šešioliktainius kodus, tiek vaizdo URL, spalvos dimensijoms konfigūruoti, padedate supaprastinti vaizdo valdymą, kai spalvų skaičius yra didžiulis.

Toliau pateiktoje iliustracijoje rodomas pavyzdys, kuriame tik šešioliktainiai kodai, tiek vaizdo URL yra naudojami konfigūracijai **Spalvų** puslapyje.

![Dimensijos konfigūracijos, naudojančios tiek šešioliktainius kodus, tiek vaizdo URL, pavyzdys.](../dev-itpro/media/swatch_color_hexandimage.png)

## <a name="configure-refiner-groups"></a>Tikslinimo priemonės grupių konfigūravimas

Kai apibrėžiate dimensijos reikšmės šešioliktainį kodą arba vaizdo URL, taip pat galite nurodyti **Tikslinimo priemonės grupės** lauko reikšmę. Šis laukas apibūdina dimensiją, kuri turėtų būti naudojama panašioms dimensijos reikšmėms grupuoti tikslinimo patirtyje.

Pavyzdžiui, jei jūsų spalvos dimensijos reikšmės yra „mėlyna”, „languota mėlyna”, „šviesiai mėlyna” ir „tamsiai mėlyna”, kiekviena reikšmė yra susieta su skirtingu šešioliktainiu kodu arba vaizdo URL. Todėl kiekviena reikšmė atrodys kaip skirtinga spalva atitinkamų produktų PDP puslapiuose ir kortelėse. Tačiau jeigu susiejate visas tas spalvos dimensijos reikšmės su **Tikslinimo** reikšme **Mėlyna**, „mėlynų” produktų ieška sugeneruos sąrašo puslapio ieškos rezultatus produktams, kurių dimensijos spalvos reikšmės yra „mėlyna”, „languota mėlyna”, „šviesiai mėlyna” ir „tamsiai mėlyna”.

Toliau pateiktos iliustracijos pavyzdys atspindi ryšį tarp **Spalvos** ir **Tikslinimo priemonės grupės** ypatybių „Commerce” būstinėje.

![Tikslinimo priemonės grupių valdymo pavyzdys.](../dev-itpro/media/swatch_refiner_group.png)

## <a name="manage-images-in-commerce-site-builder"></a>Vaizdų valdymas „Commerce“ svetainės kūrimo priemonėje

Jei vaizdo URL yra panaudoti kuriai nors dimensijos reikšmei, atitinkami vaizdai turi būti įkelti į „Commerce” svetainių daryklę. Kiekvieno vaizdo vieta turi atitikti failo pavadinimą ir aplanko kelią, kurie yra apibrėžti vaizdui „Commerce” būstinėje. Vaizdų failai turi būti įkelti į atitinkamą vietų kategoriją svetainių daryklėje. Pavyzdžiui, spalvų vaizdai turi būti įkelti į **Spalvos** kategorijos aplanką. Daugiau informacijos apie tai, kaip įkelti vaizdus į svetainės kūrimo įrankį, rasite [Vaizdų įkėlimas](../dam-upload-images.md).

Toliau pateiktoje iliustracijoje rodomas pavyzdys, kuriame dialogo langas **Įkelti failus** yra naudojamas failams įkelti į svetainių daryklės medijos biblioteką. Pabrėžiamos galimos pasirinkti **Dydžio**, **Spalvos** ir **Stiliaus** kategorijos.

![Vaizdo failų kategorijų pavyzdys įkėlimo į svetainių daryklės medijos biblioteką metu.](../dev-itpro/media/swatch_sitebuilder.png)

## <a name="enable-swatch-display-on-e-commerce-site-pages"></a>Pavyzdžių rodymo el. prekybos puslapiuose įgalinimas

Tam, kad pavyzdžiai galėtų pasirodyti el. prekybos svetainės puslapiuose, kuriems reikia dimensijos pasirinkimo, pavyzdžiui, PDP ir sąrašų puslapiuose, turite sukonfigūruoti dimensijos svetainės parametrus „Commerce” būstinėje. Daugiau informacijos rasite [Svetainės parametrų taikymas dimensijoms](../dimension-settings.md).

Be to, turėtumėte įgalinti ypatybę **Įtraukti produkto atributus ieškos rezultatuose** ieškos rezultatų moduliams. Jei jūsų svetainė naudoja tinkintus kategorijos puslapius, turėtumėte atnaujinti ieškos rezultatų modulius, naudojamus tuose puslapiuose tam, kad ypatybė **Įtraukti produkto atributus ieškos rezultatuose** būtų įjungta. Daugiau informacijos rasite [Ieškos rezultatų modulis](../search-result-module.md).

## <a name="display-swatches-in-pos-and-other-channels"></a>Pavyzdžių rodymas EKA ir kituose kanaluose

„Commerce” šiuo metu neturi visiškai parengto diegimo, palaikančio pavyzdžių rodymą Elektroniniame kasos aparate (EKA) ir kituose kanaluose. Tačiau galite įdiegti pavyzdžio rodymo funkciją kaip plėtinį, dėl kurio kanalo API grąžina šešioliktainius kodus ir vaizdo URL, reikalingus pavyzdžių generavimui.

## <a name="additional-resources"></a>Papildomi ištekliai

[Ieškos rezultatų modulis](../search-result-module.md)

[Svetainės parametrų taikymas dimensijoms](../dimension-settings.md)

[Produktų dimensijos](../../supply-chain/pim/product-dimensions.md)

[Nusiųsti vaizdą](../dam-upload-images.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
