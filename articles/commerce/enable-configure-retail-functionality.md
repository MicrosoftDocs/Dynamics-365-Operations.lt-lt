---
title: Pradinių duomenų inicijavimas naujose „Retail“ aplinkose
description: Šiame straipsnyje aprašyti duomenys, kurie kuriami „Dynamics 365 Commerce“ inicijavimo proceso metu.
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
ms.openlocfilehash: e2833c32d557ec3d2dc80808222d1d47860ce6ea
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023458"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Pradinių duomenų inicijavimas naujose „Retail“ aplinkose

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašyti duomenys, kurie kuriami „Dynamics 365 Commerce“ inicijavimo proceso metu.

Kai naudodami „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegiate sprendimą „Commerce“, turite inicijuoti „Commerce“ konfigūravimą ir sukurti pagrindinius konfigūravimo duomenis.

> [!IMPORTANT]
> Prieš inicijuodami „Commerce“ konfigūravimą, įsitikinkite, kad nurodėte visų juridinių subjektų, kuriuose nustatysite parduotuves, kalbą ir pašto adresą. Šį veiksmą reikia atlikti su visais juridiniais subjektais, kuriuose naudojate „Commerce“.

Norėdami inicijuoti „Commerce“ konfigūravimą, atlikite tolesnius veiksmus.

1. Paleiskite „Commerce“ klientą.
2. Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Būstinės sąranka** &gt; **Parametrai** &gt; **Prekybos parametrai**.
3. Spustelėkite **Inicijuoti**.

Inicijuojant sukuriami toliau pateikti numatytieji konfigūravimo duomenys.

- „Commerce“ duomenų apsikeitimo valdymo užduotys ir antrinės užduotys
- „Commerce“ kanalo schema
- „Commerce“ paskirstymo grafikai
- Numatytieji ekrano maketai, apimantys mygtukynus, vaizdus ir temas
- Laiko juostos informacija
- Elektroninio kasos aparato (EKA) operacijos
- EKA teisės
- Kanalo ataskaitos
- Atributo metaduomenys
- Objektų tikrinimo šablonai
- Paketinė užduotis, skirta „Commerce Data Exchange“ seansų retrospektyvai šalinti

Be to, įjungiama prisiregistravimo prie „Commerce“ duomenų bazės funkcija, susijusi su mokėjimo kortelių pramone (PCI).

> [!NOTE]
> „Commerce“ duomenų apsikeitimo valdymą galima konfigūruoti atskirai. Ši parinktis suteikia galimybę iš naujo nustatyti „Commerce“ duomenų apsikeitimo valdymo konfigūracijos numatytuosius parametrus.

Baigę inicijavimą turite sukonfigūruoti papildomus „Commerce“ duomenis. Štai keletas pavyzdžių:

- „Commerce“ parametrai
- „Commerce“ planuoklės parametrai
- „Commerce“ kanalai
- Registrai ir įrenginiai
- Asortimentai
