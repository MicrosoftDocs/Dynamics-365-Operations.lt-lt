---
title: "Potencialūs klientai ir grynieji pinigai"
description: "Temoje apžvelgiamas „Dynamics 365 for Finance and Operations, Enterprise edition“ ir „Dynamics 365 for Sales“ sprendimas Potencialūs klientai ir grynieji pinigai."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>Potencialūs klientai ir grynieji pinigai  

[!include[banner](../includes/banner.md)]

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją [Duomenų integravimas](/common-data-service/entity-reference/dynamics-365-integration) ir „Common Data Service“ (CDS) sinchronizuojami duomenys „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ ir „Dynamics 365 for Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus ir funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus. Sukūrus duomenų srautą tarp „Finance and Operations“ ir „Sales“ galima vykdyti pardavimo ir rinkodaros veiklas sprendime „Sales“ bei tvarkyti užsakymų įvykdymą naudojant atsargų valdymo funkciją sprendime „Finance and Operations“. 

Šiuo sprendimu integruojamos toliau nurodytos sritys. 

-   [„Sales“ sąskaitų tvarkymas ir sinchronizavimas su „Finance and Operations“](accounts-template-mapping.md)
-   [„Sales“ kontaktų tvarkymas ir sinchronizavimas su „Finance and Operations“](contacts-template-mapping.md)
-   [„Finance and Operations“ produktų tvarkymas ir sinchronizavimas su „Sales“](products-template-mapping.md)
-   [Pardavimo pasiūlymų kūrimas sprendime „Sales“ ir jų sinchronizavimas su „Finance and Operations“](sales-quotation-template-mapping.md)
-   [Pardavimo užsakymų kūrimas sprendime „Finance and Operations“ ir jų sinchronizavimas su „Sales“](sales-order-template-mapping.md)
-   [Pardavimo sąskaitų faktūrų kūrimas sprendime „Finance and Operations“ ir jų sinchronizavimas su „Sales“](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Sprendimui „Dynamics 365 for Finance and Operations, Enterprise edition“ taikomi sistemos reikalavimai

Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti tolesnius elementus.

- „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) su 8 platformos naujinimu (programa 7.2.11792.56024 su platforma 7.0.4565.16212)

- Dvi „Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) karštąsias pataisas.

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – įdiegus šią karštąją pataisą, galima naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymų eilutes sinchronizuoti su „Sales“.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – įdiegus šią karštąją pataisą, galima naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymus sinchronizuoti su „Sales“.
    
**Pastaba**. Turite įdiegti tik KB4036524, nes į įdiegtį įtraukti pakeitimai iš KB4036461.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Sprendimui „Dynamics 365 for Sales“ taikomi sistemos reikalavimai

Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti tolesnius elementus.

- „Dynamics 365 for Sales“ versija 1612 (8.2.1.207) (DB 8.2.1.207) (internetinė versija) arba naujesnė versija.
- Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai versija 1.14.0.0 (v14) arba naujesnė.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Sprendimui „Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai diegimas

- Iš „CustomerSource“ atsisiųskite [Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai paketo ZIP failą](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash).

- Įsitikinkite, kad ZIP failas yra atblokuotas, kad, diegdami sprendimo paketą, negautumėte klaidos pranešimo „Importavimo paketų nerasta“. Norėdami atblokuoti failą, atlikite tolesnius veiksmus.

    -  ZIP failą spustelėkite dešiniuoju pelės mygtuku.
    -  Pasirinkite **Ypatybės**, tada – **Atblokuoti**. 

- Išskleiskite ir paleiskite PackageDeployer.exe.

- Savo „Sales“ egzemplioriuje įdiekite sprendimą Potencialūs klientai ir grynieji pinigai.

    - Pasirinkite visuotinio diegimo tipą **„Office 365“**.
    - Pasirinkite **Rodyti išplėstines parinktis**.
    - Norėdami greitai įdiegti, pasirinkite **regioną**. Jei pasirenkate **Nežinau**, sistema ieško visų regionų ir įdiegti truks ilgiau.
    - Įveskite administratoriaus vartotojo, turinčio diegimo teises, **vartotojo vardą** ir **slaptažodį**.

