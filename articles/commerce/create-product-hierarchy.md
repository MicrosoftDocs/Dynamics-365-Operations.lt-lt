---
title: Naujos produkto hierarchijos kūrimas
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ sukuti naują produkto hierarchiją.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 724ec2e5af7837d574298d662911cd9c6ee9e9f2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070426"
---
# <a name="create-a-new-product-hierarchy"></a>Naujos produkto hierarchijos kūrimas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ sukuti naują produkto hierarchiją.

## <a name="overview"></a>Peržiūrėti

„Dynamics 365 Commerce“ palaiko kelis mažmeninės prekybos kanalus. Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis). Kiekviename mažmeninės prekybos parduotuvės kanale gali būti naudojami savi mokėjimo būdai, kainų grupės, elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai. Prieš kurdami mažmeninės prekybos parduotuvės kanalą, turite nustatyti visus šiuos elementus. 

Prekybos produktų hierarchija naudojama norint nurodyti bendrą organizacijos produktų hierarchiją. Prekybos produktų hierarchiją galite naudoti reklamavimo, kainų nustatymo ir akcijų, ataskaitų teikimo ir asortimento planavimo tikslais. Vienai organizacijai galima priskirti tik vieną prekybos produktų hierarchiją.

## <a name="create-and-configure-a-product-hierarchy"></a>Produkto hierarchijos kūrimas ir konfigūravimas

Norėdami sukurti ir sukonfigūruoti prekybos produktų hierarchiją, atlikite tolesnius veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Produktai ir kategorijos \> Prekybos produktų hierarchija**.
1. Jei hierarchijos dar nėra, pasirinkę **Veiksmų sritis**, pasirinkite **Nauja**, norėdami sukurti hierarchijos šakninį katalogą.
1. Srityje **Bendra** atlikite tolesnius veiksmus.
    1. Langelyje **Pavadinimas** įveskite pavadinimą.
    1. Langelyje **Aprašas** įveskite aprašą.
    1. Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.
    1. Parinktyje **Aktyvusis** nustatykite **Taip**.

## <a name="add-hierarchy-nodes"></a>Hierarchijos mazgų įtraukimas

Norėdami įtraukti hierarchijos mazgų, atlikite tolesnius veiksmus.

1. Veiksmų srityje pasirinkite **Redaguoti kategorijų hierarchiją**.
1. Pasirinkite pirminį mazgą, į kurį norite įtraukti naują mazgą, tada pasirinkite **Naujas kategorijos mazgas**.
1. Skyriuje **Bendra** pateikite **Pavadinimas**, **Aprašas**, **Patogus pavadinimas** ir **Raktažodžiai**.
1. Srityje **Bendra** atlikite tolesnius veiksmus.
    1. Langelyje **Pavadinimas** įveskite pavadinimą.
    1. Langelyje **Aprašas** įveskite aprašą.
    1. Langelyje **Patogus pavadinimas** įveskite patogų pavadinimą.
    1. Langelyje **Raktažodžiai** įveskite atitinkamus raktažodžius.
    1. Langelyje **Rodymo tvarka** įveskite rodymo tvarkos numerį (nebūtina).
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Norėdami įtraukti papildomų mazgų, pakartokite pirmiau nurodytus veiksmus.

Toliau pateiktame vaizde parodytas naujo produkto hierarchijos mazgo kūrimas.

![Produkto hierarchijos kūrimas](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Kiti parametrai

Kategorijos atributų grupes taip pat galima priskirti kiekvienai grupei, jei reikia.  

## <a name="additional-resources"></a>Papildomi ištekliai

[prekybos hierarchijos](retail-hierarchies.md)

[Produktų kategorijų ir produktų valdymas ](category-management-product-creation.md)

[Prekybos objektų rūšiavimo tvarkos keitimas](custom-order-categories-nav-retail-prod-hierarchy.md)
