---
title: Projekto išlaidų kaupimas pirkimo kvituose
description: Šioje temoje aprašoma, kaip sukauptas projekto išlaidas pirkimo kvituose galima sekti naudojant „Microsoft“ „Dynamics 365 Finance“.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 615e22234323e2235fba002c50f9ab9c230c021e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827895"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Projekto išlaidų kaupimas pirkimo kvituose

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukauptas projekto išlaidas pirkimo kvituose galima sekti naudojant „Microsoft“ „Dynamics 365 Finance“. 

Projekto SF dažnai gaunamos vėliau negu gaunamos prekės ir paslaugos, o tai gali turėti didelės įtakos pagrindiniams projekto efektyvumo indikatoriams (KPI). Svarbu turėti galimybę sekti šias finansinių ir projekto ataskaitų operacijas.

Tai pavaizduota toliau pateiktame scenarijaus pavyzdyje. 

„Contoso Consulting“ pradėjo naują debesies diegimo projektą. Sukuriamas pirkimo užsakymas pirkti kompiuterį projektui. Kompiuteris kainuos 1500 dol., o diegimo paslaugos kainuos 150 dol. Tiekėjas pristatė ir įdiegė kompiuterį, bet „Contoso Consulting“ sąskaitos faktūros dar negavo. Prieš pateikiant sąskaitą faktūrą projekto vadovas norėtų matyti sukauptas 1650 dol. vertės projekto išlaidas. Ši kaina taip pat turi būti nurodoma įmonės mėnesio pabaigos finansinėse ataskaitose. 

Pateikiant ataskaitas sukauptos išlaidos turi būti įrašomos finansiniu lygmeniu ir projekto lygmeniu. Gali būti sekamas prekės ir įsigijimo kategorijų produkto kvito finansinis naujinimas. 

Jeigu sekate prekių naujinimą, puslapyje **Mokėtinos sumos parametrai** pasirinkite parinktį **Registruoti produkto kvitus didžiojoje knygoje**.
[![Mokėtinų sumų parametrų puslapis](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Jeigu sekate įsigijimo kategorijų naujinimą, puslapyje **Kategorijos strategijos taisyklė** pasirinkite strategijas **Pirkimas**, o po to pasirinkite kiekvienos įsigijimo kategorijos parinktį **Kaupti pirkimo gavimo išlaidas**.
[![Kategorijos strategijos taisyklės puslapis](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Sąskaitos **Pirkimo išlaidos, kurioms neišrašyta SF** ir **Pirkimo kaupimas**, esančios dalyje **Registravimo nustatymas**, bus naudojamos registruojant su produkto kvitu susietus kvitus.

Naudodami tą patį scenarijų pažiūrėkime, kokią įtaką produkto kvito užregistravimas turės didžiajai knygai ir projekto informacijai. 

**1 veiksmas:** Sukurti ir patvirtinti naują projekto pirkimo užsakymą, kad jame būtų nurodyta 1500 dol. vertės kompiuterio pirkimo suma ir 150 dol. vertės diegimo paslaugos.
[![Naujo pirkimo užsakymo kūrimas](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Patvirtinus pirkimo užsakymą sukuriamos projekto fiksuotos savikainos operacijos. 
[![Operacijos sukurtos](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Fiksuotos savikainos operacijų lauke nustatomas lauko **Operacijos kilmė** parametras **Pirkimo užsakymas**. Sukūrus ir patvirtinus pirkimo užsakymą projekto operacijos nesukuriamos. 

**2 veiksmas:** Tiekiamos prekės, teikiamos paslaugos ir užregistruojamas produkto kvitas. 

Registruojant produkto kvitą sukuriamas ir užregistruojamas didžiosios knygos kvitas. Kvite nurodomas pirkimo išlaidų, sąskaitos, kuriai neišrašyta SF, ir kredito pirkimo kaupimo sąskaitos debetas. 
[![Kvitų operacijos](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Registruojant produkto kvitą bus naudojamas įsigijimo kategorijoms ir produktams skirtas registravimo nustatymas, o ne projekto kategorijoms skirtas registravimo nustatymas. Norint, kad būtų rodomas teisingas pirkimo kaupimų finansinis poveikis, šį nustatymą reikia sulygiuoti. 

Puslapyje **Įsigijimo kategorija** įsigijimo kategorijas galima susieti su projekto kategorijomis.
[![Įsigijimo kategorijos puslapis](./media/accruals7-1024x390.png)](./media/accruals7.png)

**3 veiksmas:** Kurti tiekėjo SF juodraštį. 

Registruojant produkto kvitą projekto informacija nepakeičiama. Kaip problemos apėjimo būdą tiekėjo sąskaitos faktūros juodraštį galite sukurti iš karto užregistravę pirkimo kvitą. Eikite į puslapį **Pirkimo užsakymas** &gt; **SF skirtukas** &gt; **Kurti** &gt; **Sąskaita faktūra**. Taip sukuriamas laukiančios SF dokumentas, kurį naudojant atnaujinama projekto informacija. 

Sukūrus tiekėjo SF juodraštį sukuriamos laukiančios projekto operacijos. 
[![Laukiančios projekto operacijos](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Puslapyje **Fiksuota savikaina** atliekant 1 veiksmą sukurti įrašai bus uždaryti ir bus sukurti nauji įrašai, kuriuose nurodomi iš laukiančios tiekėjo sąskaitos faktūros gauti išlaidų įsipareigojimai. Bus nustatyta fiksuotos savikainos lauko **Operacijos kilmė** parinktis **Tiekėjo SF**.
[![Fiksuotos savikainos puslapis](./media/accruals9-1024x200.png)](./media/accruals9.png)

Kol nebus gauta faktinė tiekėjo SF, tiekėjo SF ir toliau bus laukiančios būsenos.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]