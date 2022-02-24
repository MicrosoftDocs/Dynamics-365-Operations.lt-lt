---
ms.openlocfilehash: f6bf4b6c946ebc63d3d84140f762cd4b789deb03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459543"
---
Kopijuojant duomenų bazę iš vienos aplinkos į kitą, nukopijuota duomenų bazė taps visiškai funkcionali tik paleidus pakartotinio parengimo įrankį ir užtikrinus, kad visi „Commerce“ komponentai yra atnaujinti.

> [!IMPORTANT]
> Rekomenduojame paleisti šią procedūrą, nepaisant to, ar naudojate „Commerce“ komponentus, ar ne, nes „Commerce“ funkcijos įtrauktos į visas aplinkas. 

Prieš tęsdami turite įsitikinti, kad įvykdytos šios būtinosios sąlygos:
1. Jei naujinate į 2017 liepos mėn. leidimo versiją (taip pat vadinamą 7.2) 7.2.11792.56024, prieš paleisdami duomenų atnaujinimą toje aplinkoje, įdiekite programos X++ karštąsias pataisas paskirties aplinkoje. Tai užkirs kelią įvairioms duomenų atnaujinimo metu atsirandančioms klaidoms:

    - KB 4036156 – „Retail“ neesminis versijos atnaujinimas – „Nenustatyta varianto numerio seka.“ Šiame pataisų pakete taip pat yra KB 4035399 ir KB 4035751. Turėkite omenyje, kad norint naudoti šį paketą, reikia turėti mažiausiai „Platform Update 9“. Jei nesate tikri, įdiekite naujausius dvejetainius failus.
    
2. Jei atnaujinate iš „Microsoft Dynamics AX 2012“, prieš paleisdami duomenų atnaujinimą įdiekite šias programos X++ pataisas paskirties aplinkoje:
    - KB 4033183 – „Dynamics AX 2012 R2“ arba „Dynamics AX 2012 R3 Pre-CU8“ nemažmeninės prekybos versijos naujinimas nepavyksta dėl nerasto objekto dbo.RETAILTILLLAYOUTZONE.
    - KB 4040692 – „Dynamics AX 2012 R3 Microsoft Dynamics 365 for Operations“ 7.2 versijos naujinimas nepavyksta RetailSalesLine dublikato indekse SalesLineIdx.
    - KB 4035490 – veikimo triktis dėl GeneralJournalAccountEntry lauko MainAccount versijos naujinimo scenarijaus.


Atlikite šiuos veiksmus, norėdami paleisti aplinkos papildymo įrankį.

1. Bendrai naudojamo turto bibliotekoje pasirinkite **Programinės įrangos visuotinio diegimo paketą**.
2. Atsisiųskite aplinkos papildymo įrankį.
3. Projekto išteklių bibliotekoje pasirinkite **Programinės įrangos visuotinio diegimo paketą**.
4. Pasirinkite **Naujas**, kad sukurtumėte naują paketą.
5. Įveskite paketo pavadinimą ir aprašymą. Paketą galite pavadinti **Aplinkos papildymo įrankis**.
6. Įkelkite paketą, kurį atsisiuntėte anksčiau.
7. Tikslinės aplinkos puslapyje **Aplinkos informacija** pasirinkite **Tvarkyti** > **Taikyti naujinimus**.
8. Pasirinkite aplinkos papildymo įrankį, kurį įkėlėte anksčiau, tada pasirinkite **Taikyti**, kad pritaikytumėte paketą.
9. Stebėkite paketo visuotinio diegimo eigą. 

Daugiau informacijos apie tai, kaip taikyti įdiegiamą paketą, rasite [Visuotinai įdiegiamo paketo taikymas](../deployment/create-apply-deployable-package.md). Daugiau informacijos apie tai, kaip taikyti įdiegiamą paketą rankiniu būdu, rasite [Visuotinai įdiegiamo paketo diegimas](../deployment/install-deployable-package.md).
