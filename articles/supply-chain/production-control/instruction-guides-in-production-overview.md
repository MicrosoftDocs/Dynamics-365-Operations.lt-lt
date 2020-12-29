---
title: Mišrios realybės vadovų pateikimas į gamybą įtrauktiems darbuotojams
description: Šioje temoje paaiškinta, kaip susieti „Microsoft Dynamics 365 Supply Chain Management“ gamybos valdymo modulį su „Dynamics 365 Guides“.
author: cabeln
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 727a3bc50ea55259c7260a9d060dac59473ee3c1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645149"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Mišrios realybės vadovų pateikimas į gamybą įtrauktiems darbuotojams

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Į gamybos procesus įtrauktiems darbuotojams bus pateikiami atitinkamos instrukcijos, kurios bus rodomos tinkamu laiku, atsižvelgiant į atliekamą darbą. *Instrukcijos* taikomos kelioms darbo sritims, įskaitant surinkimą, aptarnavimą, operacijas, sertifikavimą ir saugą. Kalbant apie visas šios pagrindines verslo veiklas, pateikiamos mokymo instrukcijos gali padėti darbuotojams daugiau pasiekti ir geriau dirbti.

## <a name="introduction"></a>Įžanga

Instrukcijas galite pateikti skirtingais būdais. Viena efektyvi sistema, kurią galima naudoti iš karto, naudoja [„Dynamics 365 Guides“](https://dynamics.microsoft.com/mixed-reality/guides/).

„Dynamics 365 Guides“ gali padėti darbuotojams suteikdama galimybę mokytis. Galite apibrėžti standartinius procesus su nuosekliomis instrukcijomis, kurios padės jūsų darbuotojams naudoti reikalingus įrankius ir dalis bei suteiks informacijos darbuotojams, kaip naudoti šiuos įrankius realiose darbo situacijose.

Vadovus galite susieti su įvairiomis gamybos kontrolės sritimis, įskaitant toliau nurodytas:

- [Ištekliai](#resources)
- [Išteklių grupės](#resource-groups)
- [Patvirtinti produktai](#released-products)
- [Formulės](#formulas)
- [Formulės versijos](#formula-versions)
- [Komplektavimo specifikacijos (KS)](#bom)
- [KS versijos](#bom-versions)
- [Maršrutai](#routes)
- [Maršruto versijos](#route-versions)
- [Įprastų operacijų ryšiai](#route-operation-relations)

> [!NOTE]
> Taip pat vadovus galite susieti su turto valdymu. Išsamesnės informacijos apie šią parinktį žr. [„Dynamics 365 Supply Chain Management“ (turto valdymo) integravimas su „Dynamics 365 Guides“](../asset-management/asset-management-guides-integration.md).

Kai darbą atliekantis darbuotojas ceche pasirenka užduotį naudodamas „Supply Chain Management“, užduoties kortelėje darbuotojas gali matyti [susijusias instrukcijas](#logic). Darbuotojui pasirinkus konkrečią instrukciją, ekrane rodomas instrukcijos QR kodas. Tada darbuotojas naudodamas „HoloLens“ nuskaito QR kodą, kuris paleidžia „Guides“ ir rodo reikiamas instrukcijas.

Toliau esančiuose poskyriuose aprašyti keli pasirinkti scenarijai, kai pramonės įmonės, naudodamos „Guides“ gamybos instrukcijoms rodyti, gali siekti didžiausios vertės.

### <a name="assembly"></a>Surinkimas

![„Guides“ naudojimas surinkimo užduotims](media/instruction-guides-hero-assembly.png "„Guides“ naudojimas aptarnavimo užduotims")

Surinkimo operacijų instrukcijose darbuotojams nurodomi reikalingi įrankiai ir dalys bei kaip juos naudoti realiose darbo situacijose.

Gamybos vadovai gali kurti ir priskirti vadovus, pavyzdžiui, [gamybos maršrutams](routes-operations.md), [operacijų ryšiams](routes-operations.md#operation-relations) arba [komplektavimo specifikacijoms](bill-of-material-bom.md). Darbuotojai matys reikiamas instrukcijas, susijusias su atitinkama darbo patirtimi ceche.

### <a name="service"></a>Aptarnavimas

![„Guides“ naudojimas aptarnavimo užduotims](media/instruction-guides-hero-service.png "„Guides“ naudojimas aptarnavimo užduotims")

Teikite technikams instrukcijas darbo vietoje, kad nebereikėtų planuoti papildomų apsilankymų.

Aptarnavimo vadovai, pavyzdžiui, gali priskirti vadovus, padedančius atlikti kokybės vertinimo procedūras, konkretiems [produktams](../../commerce/product.md).

### <a name="quality"></a>Kokybė

![„Guides“ naudojimas kokybės užtikrinimo užduotims](media/instruction-guides-hero-quality.png "„Guides“ naudojimas kokybės užtikrinimo užduotims")

Diekite naujus procesus ir užtikrinkite didesnį nuoseklumą paversdami darbuotojo žinias į pakartotinai pritaikomą įrankį.

Kokybės užtikrinimo vadovai, pavyzdžiui, gali priskirti vadovus, padedančius atlikti kokybės vertinimo procedūras, [produktams](../../commerce/product.md).

### <a name="certifications"></a>Sertifikatai

![„Guides“ naudojimas su sertifikavimu susijusioms užduotims](media/instruction-guides-hero-certification.png "„Guides“ naudojimas su sertifikavimu susijusioms užduotims")

Užtikrinkite, kad kiekvienas darbuotojas atitiktų aukštus standartus, greitai identifikuodami darbuotojus ir vietas, kuriems reikia pagalbos.

### <a name="safety"></a>Sauga

![„Guides“ naudojimas darbo saugos instrukcijose](media/instruction-guides-hero-safety.png "„Guides“ naudojimas darbo saugos instrukcijose")

Pateikite instrukcijas, kaip vykdyti pavojingas procedūras, virtualiai prieš jas atliekant fizinėje aplinkoje. Taikant mišrios tikrovės koncepciją, darbuotojai gali susipažinti su pavojingomis procedūromis virtualiai.

Gamybos vadovai gali pateikti specialias pavojingų medžiagų tvarkymo arba atidaus tvarkymo procedūrų instrukcijas, priskirdami instrukcijas [produktams](../../commerce/product.md), [maršrutams](routes-operations.md) ir [operacijoms](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Darbo su instrukcijomis ir „Guides“ pradžia

Tam, kad būtų galima gauti instrukcijas vykdant gamybos procesą, „Supply Chain Management“ yra iš karto integruotas su „Dynamics 365 Guides“. Norint kurti, tvarkyti ir priskirti mišrios realybės instrukcijas gamybos ištekliams ir darbui, reikalingas licencijuotas ir įdiegtas „Guides“ programos egzempliorius.

### <a name="prerequisites"></a>Būtinieji komponentai

Tam, kad galėtumėte naudoti šią funkciją, jūsų sistemą turi sudaryti toliau nurodytos dalys.

- „Dynamics 365 Supply Chain Management“ 10.0.15 arba naujesnė versija
- [Dvigubas rašymas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) „Supply Chain Management“ programoms.
- [„Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution)“ 400.0.1.48 arba naujesnė versija

### <a name="turn-on-the-feature"></a>Funkcijos įjungimas

Tam, kad funkcija būtų prieinama jūsų sistemoje, turite aktyvinti jos konfigūracijos raktus. Tai atlikti reikia tik vieną kartą. Norinti tai padaryti, administratorius turi atlikti šiuos veiksmus:

1. Perjunkite savo sistemą į priežiūros režimą, kaip aprašyta [Priežiūros režimas](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
1. Išplėskite sritį **Mišrioji realybė** ir pasirinkite žymės langelį **Mišriosios realybės vadovas**.
1. Išplėskite sritį **Gamybos valdymas** ir pasirinkite žymės langelį **Gamybos instrukcijos**.
1. Išjunkite priežiūros režimą, kaip aprašyta [Priežiūros režimas](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Konfigūravimas, kaip vadovai bus rodomi ceche

Norėdami sukonfigūruoti, kaip vadovai bus rodomi ceche, eikite į **Mišrioji realybė \>Dynamics 365 Guides\>Konfigūruoti „Guides“ integravimą**.

![Vadovo integravimo gamybai konfigūravimas](media/instruction-guides-configure-integration.png "Vadovo integravimo gamybai konfigūravimas")

Užpildykite toliau nurodytus laukus:

- **„Microsoft Dataverse“ URL** - Nurodykite URL „Microsoft Dataverse“ aplinkai, kurioje kuriate savo „Guides“. Formatas yra „contoso.crm4.dynamics.com", kuriame pirmoji dalis URL dažniausiai pavadinta organizacijos vardu (tokiu kaip „contoso."), antroji dalis yra duomenų regiono jūsų aplinka (tokia kaip „crm4."), o paskutinė dalis - domenas (toks kaip „dynamics.com"). Vienas būdas surasti reikiamą URL yra eiti į [home.dynamics.com](https://home.dynamics.com/) ir tada atverti savo „Guides“ programą. Atvėrus „Guides“ programą, matysite URL adreso juostoje savo naršyklėje (imkite tik pagrindinį URL, kuris parodytas ankstesniame pavyzdyje). Ši vertė naudojama sudaryti adresus jūsų gairėse ir bus koduojama į QR kodus."
- **QR kodo dydis** – nurodykite sugeneruoto QR kodo dydį. Rekomenduojame pasirinkti dydį, kuris didžiąją ekrano dalį, bet ne didesnį. Įprastai tinkama reikšmė yra *15*.
- **QR kodo klaidų taisymo lygis** – nurodykite QR kodo detalumo lygį. Didesnis detalumas gali padėti užtikrinti didesnį kodo patikimumą, bet **QR kodo dydis** turi būti pakankamai didelis, kad būtų užtikrintas detalumo lygis, kurio reikia pasirinktam koregavimo lygiui.

> [!TIP]
> - QR kodai, kurie yra per dideli jūsų monitoriui, gali būti generuojami šiek tiek ilgiau, o po to jie bus sumažinami, kad atitiktų ekraną. Tai nesuteikia kokių nors pranašumų.
> - Esant per mažiems QR kodams, tam tikrose aplinkose „HoloLens“ gali nepavykti tinkamai nuskaityti kodo.
> - Rekomenduojame išbandyti kiekvieno įrenginio, kuris rodytis QR kodus „HoloLens“ vartotojams, parametrus. Pasirinkite parametrus, kurie užtikrintų pakankamą patikimumą cecho aplinkoje.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Peržiūrėkite visų vadovo priskyrimų apžvalgą

Norėdami peržiūrėti visų jūsų organizacijoje prieinamų vadovų sąrašą bei visų gamybos procesų ir išteklių priskyrimų sąrašą, naudokite puslapį **Visi vadovai“**. Norėdami atidaryti, eikite į **Mišrioji realybė \> Vadovai \> Visi vadovai**. Viršuje esančiame sąraše rodomi visi prienami vadovai, be to, norėdami filtruoti sąrašą, galite naudoti čia esantį lauką. Apačioje esančiame sąraše rodomi visi vadovo priskyrimai ir yra valdymui skirta įrankių juosta.

![Vadovų valdymas](media/instruction-guides-allguides.png "Vadovų valdymas")

Toliau esančiuose skyriuose aprašyti objektų tipai, kuriems galite priskirti vadovus. Kiekviename priskirtame vadove pateikiamos instrukcijos, kurios automatiškai pridedamos prie atitinkamų gamybos užduočių ir kurios bus pateikiamos ceche.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Vadovo susiejimas su ištekliu

Pridėkite vadovą prie [ištekliaus](operations-resources.md), kuris pateiks vadovą, atitinkamų gamybos užduočių kontekste.

### <a name="typical-scenario-using-resources"></a>Tipinis scenarijus naudojant išteklius

Pavyzdžiui, vadovą su bendrosiomis mašinų saugos arba darbo instrukcijomis galite pridėti prie mašinos tipo ištekliaus. Tada vadovas bus pasiekiamas kiekvienai mašina atliekamai užduočiai.

### <a name="add-a-guide-to-a-resource"></a>Vadovo pridėjimas prie ištekliaus

Norėdami pridėti vadovą prie ištekliaus:

1. Eikite į **Gamybos kontrolė \> Sąranka \> Ištekliai \> Ištekliai**.
1. Sąrašo srityje pasirinkite išteklių, kuriam norite priskirti vadovą.
1. Išplėskite „FastTab“ **Susiję vadovai**.
1. Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**. Nauja eilutė pridedama prie tinklelio.
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti. Jei yra daug vadovų, galite filtruoti sąrašą, kad surastumėte tą, kurio ieškote.
    ![Vadovų valdymas](media/instruction-guides-allguides.png "Vadovų valdymas")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Vadovo susiejimas su išteklių grupe

Jei vadovą naudojate mašinų grupių, gamybos linijų arba darbo elementų valdymui, jį galite įtraukti į [išteklių grupes](tasks/define-discrete-manufacturing-resource-group.md).

### <a name="typical-scenarios-using-resource-groups"></a>Tipiniai scenarijai naudojant išteklių grupes

**1 pavyzdys.** Sukonfigūravote išteklių grupę kelioms to paties modelio mašinoms. Užuot priskyrę atitinkamą darbo su mašinos modeliu instrukciją kiekvienam atitinkamam ištekliui, vadovą galite priskirti išteklių grupei, kuri atitinka mašinos modelį.

**2 pavyzdys.** Sukonfigūravote darbo elementų, kuriuose yra įvairių mašinų, išteklių grupę ir turite vadovą, kuris pateikia bendrąsias instrukcijas, kaip tvarkyti darbo elementą. Vadovas taikomas bet kokiai darbo elemento gamybos veiklai.

### <a name="add-a-guide-to-a-resource-group"></a>Vadovo įtraukimas į išteklių grupę

Norėdami įtraukti vadovą į išteklių grupę:

1. Eikite į **Gamybos kontrolė \> Sąranka \> Ištekliai \> Išteklių grupės**.
1. Sąrašo srityje pasirinkite išteklių grupę, kuriai norite priskirti vadovą.
1. Išplėskite „FastTab“ **Susiję vadovai**.
1. Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**. Nauja eilutė pridedama prie tinklelio.
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti. Jei yra daug vadovų, galite filtruoti sąrašą, kad surastumėte tą, kurio ieškote.
    ![Vadovo įtraukimas į išteklių grupę](media/instruction-guides-resourcegroup.png "Vadovo įtraukimas į išteklių grupę")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Vadovo susiejimas su išleistu produktu

Vadovą galite pridėti prie bet kurio [išleisto produkto](../pim/tasks/create-released-product-single-company.md).

### <a name="typical-scenario-using-released-products"></a>Įprastinis scenarijus naudojant išleistus produktus

Produktų lygio vadovai pateikia cecho darbuotojams darbo su konkrečiu išleistu produktu ar preke arba eksploatavimo instrukcijas.

### <a name="add-a-guide-to-a-released-product"></a>Vadovo pridėjimas prie išleisto produkto

Norėdami pridėti vadovą prie išleisto produkto:

1. Eikite į **Gamybos informacijos valdymas \> Produktai \> Išleisti produktai**.
1. Atidarykite produktą, kuriam norite priskirti vadovą.
1. Veiksmų srityje atidarykite skirtuką **Inžinierius** ir grupėje **Peržiūra** pasirinkite **Susiję vadovai**.
1. Atidaromas pasirinkto produkto puslapis **Susiję vadovai**.
1. Veiksmų srityje pasirinkite **Įtraukti** ir pridėkite naują eilutę prie tinklelio. 
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.
    ![Vadovo pridėjimas prie išleisto produkto](media/instruction-guides-ReleasedProduct-AddGuides.png "Vadovo pridėjimas prie išleisto produkto")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Vadovo susiejimas su formule

Vadovą galite pridėti prie bet kurios [formulės](bill-of-material-bom.md#formulas-co-products-and-by-products).

### <a name="typical-scenario-using-formulas"></a>Tipinis scenarijus naudojant formules
  
Formulės lygio vadovai teikia cecho darbuotojams darbo instrukcijas formulės arba recepto kontekste. Vadovus taip pat galima priskirti formulės versijoms.

> [!NOTE]
> Vadovus, susijusius su gamybos procesais, pagal formulę galite priskirti maršrutui, maršruto versijai ar maršruto operacijų ryšiams.  

> Šiuo metu vadovų negalima pridėti prie atskirų formulės eilučių.

### <a name="add-a-guide-to-a-formula"></a>Vadovo pridėjimas prie fromulės

Norėdami pridėti vadovą prie formulės:

1. Eikite į **Gamybos informacijos valdymas \> KS ir formulės \> Formulės**.
1. Atidarykite formulę, kuriai norite priskirti vadovą.
1. Atidarykite skirtuką **Antraštė**, esantį virš viršutinio „FastTab“.
1. Išplėskite „FastTab“ **Susiję vadovai**.
1. Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**. Nauja eilutė pridedama prie tinklelio.
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.
    ![Vadovo pridėjimas prie formulės](media/instruction-guides-Formula.png "Vadovo pridėjimas prie formulės")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Vadovo susiejimas su formulės versija

Vadovą galite pridėti prie bet kurios [formulės versijos](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Tipinis scenarijus naudojant formulės versijas

Prie atskirų formulės versijų pridėti vadovai teikia cecho darbuotojams instrukcijas, kurios yra susijusios su gamyba taikant atitinkamą formulės recepto versiją.

> [!TIP]
> Vadovus, susijusius su gamybos procesais, pagal formulės versiją galite priskirti maršrutui, maršruto versijai ar maršruto operacijų ryšiams.  

> [!NOTE]
> Šiuo metu vadovų negalima pridėti prie atskirų formulės eilučių.

### <a name="add-a-guide-to-a-formula-version"></a>Vadovo pridėjimas prie formulės versijos

Norėdami pridėti vadovą prie formulės versijos:

1. Eikite į **Gamybos informacijos valdymas \> KS ir formulės \> Formulės**.
1. Atidarykite formulę, prie kurios versijos norite priskirti vadovą.
1. Atidarykite skirtuką **Antraštė**, esantį virš viršutinio „FastTab“.
1. „FastTab“ **Formulės versijos** pasirinkite versiją, kuriai norite priskirti vadovą.
1. Įrankių juostoje **Formulės versijos** pasirinkite **Susiję vadovai**.
    ![Su pasirinkta formulės versija susijusių vadovų atidarymas](media/instruction-guides-FormulaVersion.png "Su pasirinkta formulės versija susijusių vadovų atidarymas")
1. Atidaromas formulės versijos puslapis **Susiję vadovai**.
1. Veiksmų srityje pasirinkite **Įtraukti** ir pridėkite naują eilutę prie tinklelio. 
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.
    ![Vadovo pridėjimas prie formulės versijos](media/instruction-guides-FormulaVersionAddGuide.png "Vadovo pridėjimas prie formulės versijos")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Vadovo susiejimas su KS

Vadovą galite įtraukti į bet kurią [komplektavimo specifikaciją](bill-of-material-bom.md) (KS).

### <a name="typical-scenario-using-bills-of-materials"></a>Įprastinis scenarijus naudojant komplektavimo specifikacijas

Prie KS pridėti vadovai teikia cecho darbuotojams instrukcijas, paaiškinančias, kaip ruošti ir dirbti su medžiaga iš KS. Vadovus taip pat galima priskirti KS versijoms.

> [!NOTE]
> Šiuo metu vadovų negalima pridėti prie atskirų KS eilučių.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Vadovo pridėjimas prie KS

Norėdami pridėti vadovą prie KS:

1. Eikite į **Gamybos informacijos valdymas \> KS ir formulės \> Komplektavimo specifikacijos**.
1. Atidarykite KS, kuriai norite priskirti vadovą.
1. Atidarykite skirtuką **Antraštė**, esantį virš viršutinio „FastTab“.
1. Išplėskite „FastTab“ **Susiję vadovai**.
1. Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**. Nauja eilutė pridedama prie tinklelio.
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.
    ![Vadovo pridėjimas prie KS](media/instruction-guides-BOM.png "Vadovo pridėjimas prie KS")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Vadovo susiejimas su KS versija

Vadovą galite įtraukti į bet kurią [komplektavimo specifikacijos versiją](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Įprastinis scenarijus naudojant komplektavimo specifikacijos versijas

Prie atskiros KS versijos pridėti vadovai teikia cecho darbuotojams instrukcijas, kurios paaiškina, kaip paruošti ir dirbti su KS medžiagos versija, kuri skiriasi nuo bendrosios KS ar kitų versijų.

> [!NOTE]
> Šiuo metu vadovų negalima pridėti prie atskirų KS eilučių.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Vadovo pridėjimas prie KS versijos

Norėdami pridėti vadovą prie KS versijos:

1. Eikite į **Gamybos informacijos valdymas \> KS ir formulės \> Komplektavimo specifikacijos**.
1. Atidarykite KS, prie kurios versijos norite priskirti vadovą.
1. Atidarykite skirtuką **Antraštė**, esantį virš viršutinio „FastTab“.
1. „FastTab“ **KS versijos** pasirinkite versiją, kuriai norite priskirti vadovą.
1. Įrankių juostoje **KS versijos** pasirinkite **Susiję vadovai**.
    ![Su pasirinkta KS versija susijusių vadovų atidarymas](media/instruction-guides-BOMVersion.png "Su pasirinkta KS versija susijusių vadovų atidarymas")
1. Atidaromas KS versijos puslapis **Susiję vadovai**.
1. Veiksmų srityje pasirinkite **Įtraukti** ir pridėkite naują eilutę prie tinklelio.
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.
    ![Vadovo pridėjimas prie KS versijos](media/instruction-guides-BOMVersionAddGuide.png "Vadovo pridėjimas prie KS versijos")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Vadovo susiejimas su maršrutu

Vadovą galite pridėti prie bet kurio [maršruto](routes-operations.md).

### <a name="typical-scenario-using-routes"></a>Tipinis scenarijus naudojant maršrutus

Maršrutai paprastai naudojami nurodyti, kaip tam tikras išleistas produktas turi būti gaminamas pagal KS arba KS versiją ir esant tam tikriems ištekliams arba išteklių grupėms.

Priskirkite vadovą maršrutui, kad pateiktumėte nuoseklias atitinkamo gamybos proceso instrukcijas.

### <a name="add-a-guide-to-a-route"></a>Vadovo pridėjimas prie maršruto

Norėdami pridėti vadovą prie maršruto:

1. Eikite į **Gamybos kontrolė \> Visi maršrutai**.
1. Atidarykite maršrutą, kuriam norite priskirti vadovą.
1. Išplėskite „FastTab“ **Susiję vadovai**.
1. Įrankių juostoje **Susiję vadovai** pasirinkite **Įtraukti**. Nauja eilutė pridedama prie tinklelio.
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.
    ![Vadovo pridėjimas prie maršruto](media/instruction-guides-Route.png "Vadovo pridėjimas prie maršruto")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Vadovo susiejimas su maršruto versija

Vadovą galite pridėti prie bet kurios [maršruto versijos](routes-operations.md#route-versions).

### <a name="typical-scenario-using-route-versions"></a>Tipinis scenarijus naudojant maršruto versijas

Maršrutų versijos paprastai naudojamos norint nurodyti gamybos procesų variantus pagal esamą maršrutą. Kiekvienai maršruto versijai galite priskirti skirtingus vadovus.

### <a name="add-a-guide-to-a-route-version"></a>Vadovo pridėjimas prie maršruto versijos

Norėdami pridėti vadovą prie maršruto versijos:

1. Eikite į **Gamybos kontrolė \> Visi maršrutai**.
1. Atidarykite maršrutą, kuriam norite priskirti vadovą.
1. „FastTab“ **Versijos** pasirinkite versiją, kuriai norite priskirti vadovą.
1. Įrankių juostoje **Versijos** pasirinkite **Susiję vadovai**.
    ![Su pasirinkta maršruto versija susijusių vadovų atidarymas](media/instruction-guides-RouteVersion.png "Su pasirinkta maršruto versija susijusių vadovų atidarymas")
1. Atidaromas KS versijos puslapis **Susiję vadovai**.
1. Veiksmų srityje pasirinkite **Įtraukti** ir pridėkite naują eilutę prie tinklelio.
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti.
    ![Vadovo pridėjimas prie maršruto versijos](media/instruction-guides-RouteVersionAddGuide.png "Vadovo pridėjimas prie maršruto versijos")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Vadovo susiejimas su maršruto operacijų ryšiu

Vadovą galite pridėti prie bet kurio [maršruto operacijų ryšio](routes-operations.md#operation-relations).

### <a name="typical-scenario-using-route-operation-relations"></a>Tipinis scenarijus naudojant maršruto operacijų ryšius

Operacijų ryšiai yra konkretus būdas, leidžiantis įtraukti rekomendacijas į produkto procesą ir susijusias operacijas. Galite nurodyti kiekvienos maršruto operacijos rekomendacijas bei nurodyti skirtingas rekomendacijas bet kuriam sukonfigūruotam maršruto ryšio kontekstui, pvz., konkrečioms prekėms, konfigūracijoms ir pan. Taip pat galite nurodyti, kuriems operacijos etapams taikomos rekomendacijos (pvz., nustatymas, eilių sudarymas, apdorojimas arba gabenimas).

> [!NOTE]
> Jei vadovus nurodysite keliams maršruto operacijų ryšiams, iš šių vadovų ceche sugeneruotai užduočiai bus rodomas tik vienas tiksliausio ryšio vadovas.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Vadovo pridėjimas prie maršruto operacijų ryšio

Norėdami pridėti vadovą prie maršruto operacijų ryšio:

1. Eikite į **Gamybos kontrolė \> Visi maršrutai**.
1. Atidarykite maršrutą, kuriam norite priskirti vadovą.
1. Veiksmų srityje atidarykite skirtuką **Maršrutas** ir grupėje **Tvarkyti** pasirinkite **Maršruto informacija**.
1. Atidaromas pasirinkto maršruto puslapis **Maršruto informacija**.
1. Viršutiniame tinklelyje pasirinkite operaciją, su kuria susijusias rekomendacijas norite teikti.
1. Apatiniame tinklelyje pasirinkite konkretų ryšį (arba bendrąjį ryšį **Visi**).
    ![Pasirinkite operaciją, o tada ryšį](media/instruction-guides-RouteOperationRelation.png "Pasirinkite operaciją, o tada ryšį")
1. Virš apatinio tinklelio atsidarykite skirtuką **Susiję vadovai**.  ![Skirtukas Susiję vadovai](media/instruction-guides-RouteOperationRelation-AddGuide.png "Skirtukas Susiję vadovai")
1. Apatinio tinklelio viršuje pasirinkite **Įtraukti**, kad į tinklelį įtrauktumėte naują liniją.
1. Naujoje eilutėje naudokite stulpelio **Pavadinimas** išskleidžiamąjį sąrašą, kad pasirinktumėte vadovą, kurį norite priskirti. Likusioje eilutės dalyje pažymėkite kiekvieno konteksto, kuriame turi būti prieinamas pasirinktas vadovas, žymės langelį.

> [!NOTE]
> Kiekvienam operacijos etapui galite pridėti vieną ar daugiau vadovų.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Vadovų pasirinkimas iš cecho vykdymo sąsajos

Kai darbuotojas atidaro užduočių sąrašą cecho vykdymo sąsajoje, „Supply Chain Management“ randa atitinkamus vadovus rodomoms užduotims. Norėdami peržiūrėti atitinkamus vadovus, naudokite mygtuką **Vadovai**.

![Vadovų mygtukas cecho vykdymo sąsajoje](media/instruction-guides-Shopfloor1.png "Vadovų mygtukas cecho vykdymo sąsajoje")

Tada pasiruoškite „HoloLens“ ir pasiekite atitinkamą vadovą nukreipdami į QR kodą ir suaktyvindami atitinkamą vadovą.

![QR kodas, skirtas prieigai prie vadovų naudojant „HoloLens“](media/instruction-guides-Shopfloor2.png "QR kodas, skirtas prieigai prie vadovų naudojant „HoloLens“")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Vadovų pasirinkimo logikos sprendimas

Vadovus galite pridėti vadovus prie šių gamybos duomenų:

- [Ištekliai](#resources)
- [Išteklių grupės](#resource-groups)
- [Patvirtinti produktai](#released-products)
- [Formulės](#formulas)
- [Formulės versijos](#formula-versions)
- [Komplektavimo specifikacijos (KS)](#bom)
- [KS versijos](#bom-versions)
- [Maršrutai](#routes)
- [Maršruto versijos](#route-versions)
- [Įprastų operacijų ryšiai](#route-operation-relations)

Kai „Supply Chain Management“ generuoja gamybos cecho užduotis, iš šių šaltinių surenkami atitinkami vadovai. Atkreipkite dėmesį į toliau pateiktas svarbias taisykles.

- Jei prie maršruto ar gamybos užsakymo pridedate KS versiją arba formulės versiją, tada užduotyje bus rodomi visi vadovai, pridėti prie šios versijos, ir vadovai, pridėti prie pirminės KS arba versijos formulės.
- Jei prie gamybos užsakymo pridedate maršruto versiją, tada užduotyje bus rodomi visi vadovai, pridėti prie šios versijos, ir vadovai, pridėti prie pirminio versijos maršruto.
- Jei nurodysite kelis maršruto operacijų ryšius, apimančius ryšį *Visi*, ir jiems priskirsite vadovus, užduotyje bus rodomi tik labiausiai specifinio ryšio vadovai.  

![Atitinkamų vadovų sprendimo diagrama](media/instruction-guides-Resolve.png "Atitinkamų vadovų sprendimo diagrama")
