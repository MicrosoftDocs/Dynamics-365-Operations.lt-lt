---
title: "Pradinių duomenų inicijavimas „Retail“ aplinkoje"
description: "Šiame straipsnyje aprašyti duomenys, kurie kuriami „Microsoft Dynamics 365 for Operations“ versijos „Retail“ inicijavimo proceso metu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Pradinių duomenų inicijavimas „Retail“ aplinkoje

[!include[banner](includes/banner.md)]


Šiame straipsnyje aprašyti duomenys, kurie kuriami „Microsoft Dynamics 365 for Operations“ versijos „Retail“ inicijavimo proceso metu.

Kai naudodami „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegiate mažmeninės prekybos sprendimą, turite inicijuoti mažmeninės prekybos konfigūravimą ir sukurti pagrindinius konfigūravimo duomenis. **Svarbu:** prieš inicijuodami mažmeninės prekybos konfigūravimą, įsitikinkite, kad nurodėte visų juridinių subjektų, kuriuose nustatysite mažmeninės prekybos parduotuves, kalbą ir pašto adresą. Šį veiksmą reikia atlikti su visais juridiniais subjektais, kuriuose naudojate mažmeninėje prekyboje. Norėdami inicijuoti mažmeninės prekybos konfigūravimą, atlikite tolesnius veiksmus.

1.  Paleiskite „Dynamics 365 for Operations“ klientą.
2.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **„Headquarters“ sąranka** &gt; **Parametrai** &gt; **Mažmeninės prekybos parametrai**.
3.  Spustelėkite **Inicijuoti**.

Inicijuojant sukuriami toliau pateikti numatytieji konfigūravimo duomenys.

-   Duomenų apsikeitimo valdymo užduotys ir antrinės užduotys
-   Mažmeninės prekybos kanalo schema
-   Mažmeninės prekybos paskirstymo grafikai
-   Numatytieji ekrano maketai, apimantys mygtukynus, vaizdus ir temas
-   Laiko juostos informacija
-   Elektroninio kasos aparato (EKA) operacijos
-   EKA teisės
-   Kanalo ataskaitos
-   Atributo metaduomenys
-   Objektų tikrinimo šablonai
-   Paketinė užduotis, skirta „Commerce Data Exchange“ seansų retrospektyvai šalinti

Be to, įjungiama prisiregistravimo prie „Dynamics 365 for Operations“ duomenų bazės funkcija, susijusi su mokėjimo kortelių pramone (PCI). **Pastaba:** duomenų apsikeitimo valdymą galima konfigūruoti atskirai. Ši parinktis suteikia galimybę iš naujo nustatyti mažmeninės prekybos duomenų apsikeitimo valdymo konfigūracijos numatytuosius parametrus. Baigę inicijavimą turite sukonfigūruoti papildomus mažmeninės prekybos duomenis. Štai keletas pavyzdžių:

-   Mažmeninės prekybos parametrai
-   Duomenų apsikeitimo valdymo parametrai
-   Mažmeninės prekybos kanalai
-   Registrai ir įrenginiai
-   Asortimentai





