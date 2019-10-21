---
title: Pradinių duomenų inicijavimas naujose „Retail“ aplinkose
description: Šiame straipsnyje aprašyti duomenys, kurie kuriami „Dynamics 365 Retail“ inicijavimo proceso metu.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49b21d81437ebd7cc55076444ee71ae1143bfac0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025521"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Pradinių duomenų inicijavimas naujose „Retail“ aplinkose

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašyti duomenys, kurie kuriami „Dynamics 365 Retail“ inicijavimo proceso metu.

Kai naudodami „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegiate mažmeninės prekybos sprendimą, turite inicijuoti mažmeninės prekybos konfigūravimą ir sukurti pagrindinius konfigūravimo duomenis.

> [!IMPORTANT]
> Prieš inicijuodami mažmeninės prekybos konfigūravimą, įsitikinkite, kad nurodėte visų juridinių subjektų, kuriuose nustatysite mažmeninės prekybos parduotuves, kalbą ir pašto adresą. Šį veiksmą reikia atlikti su visais juridiniais subjektais, kuriuose naudojate mažmeninėje prekyboje.

Norėdami inicijuoti mažmeninės prekybos konfigūravimą, atlikite tolesnius veiksmus.

1. Paleiskite „Retail“ klientą.
2. Spustelėkite **Mažmeninė prekyba** &gt; **„Headquarters“ sąranka** &gt; **Parametrai** &gt; **Mažmeninės prekybos parametrai**.
3. Spustelėkite **Inicijuoti**.

Inicijuojant sukuriami toliau pateikti numatytieji konfigūravimo duomenys.

- Duomenų apsikeitimo valdymo užduotys ir antrinės užduotys
- Mažmeninės prekybos kanalo schema
- Mažmeninės prekybos paskirstymo grafikai
- Numatytieji ekrano maketai, apimantys mygtukynus, vaizdus ir temas
- Laiko juostos informacija
- Elektroninio kasos aparato (EKA) operacijos
- EKA teisės
- Kanalo ataskaitos
- Atributo metaduomenys
- Objektų tikrinimo šablonai
- Paketinė užduotis, skirta „Commerce Data Exchange“ seansų retrospektyvai šalinti

Be to, įjungiama prisiregistravimo prie „Retail“ duomenų bazės funkcija, susijusi su mokėjimo kortelių pramone (PCI).

> [!NOTE]
> Duomenų apsikeitimo valdymą galima konfigūruoti atskirai. Ši parinktis suteikia galimybę iš naujo nustatyti mažmeninės prekybos duomenų apsikeitimo valdymo konfigūracijos numatytuosius parametrus.

Baigę inicijavimą turite sukonfigūruoti papildomus mažmeninės prekybos duomenis. Štai keletas pavyzdžių:

- Mažmeninės prekybos parametrai
- Duomenų apsikeitimo valdymo parametrai
- Mažmeninės prekybos kanalai
- Registrai ir įrenginiai
- Asortimentai
