---
title: Elektroninių SF išrašymo „Azure“ išteklių nustatymas
description: Šiame straipsnyje pateikta proceso, kaip nustatyti išteklius elektroninių SF Microsoft Azure išrašymo procesui, apžvalga.
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c5b7b2ca4d7733fb1c75ded8798655699284fe1a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907735"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Elektroninių SF išrašymo „Azure“ išteklių nustatymas

[!include [banner](../includes/banner.md)]

Elektroninių SF išrašymo Microsoft Azure išteklių nustatymo procesas turi tris veiksmus. Pirmi du veiksmai " "Azure" kodo "Azure" portale kūrimas ir "Azure" saugyklos sąskaitos kūrimas "Azure" portale" yra privalomi. Trečiasis veiksmas "Ryšio konfigūravimas SharePoint " yra pasirinktinis.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Kurti "Azure" kodo saugyklą "Azure" portale

Sukurkite kodo "Azure" abonementą. Rekomenduojame sukurti atskirą elektroninio SF išrašymo raktų saugyklą, o jūs nejungitumėte paslapčių su kitomis programomis. Sukurkite tiek paslapčių ir sertifikatų, kiek jums reikia savo scenarijams elektroniniuose dokumentuose. Turite sukurti bent vieną slaptažodį, kad būtų saugomas "Azure" saugyklos sąskaitos, kurią sukursite kitame veiksme, bendrai naudojamos prieigos parašo (SAS) atpažinimo ženklas.

Informacijos, kaip atlikti šį veiksmą, rasite " [Azure" portalo "Azure" portalo "Azure" rakto saugyklos kūrimas](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>„Azure“ saugyklos paskyros kūrimas „Azure“ portale

Jūs turite visus elektroninius dokumentus ir rinkmenas, sugeneruotas elektroninių SF išrašymo tarnybos, arba įveskite tarnybą. Šie dokumentai ir rinkmenos saugomi "Azure" saugykloje, kurią sukuriate savo "Azure" abonemente. Tarnyba turės prieigą prie jūsų saugyklos abonemento, naudodama SAS atpažinimo ženklą, kuris paimtas iš jūsų rakto Vault slapto kodo.

Informacijos, kaip atlikti šį veiksmą, ieškokite " [Azure" saugyklos sąskaitos kūrimas "Azure" portale](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>„SharePoint“ ryšio konfigūravimas

Kai kuriuose scenarijuose gali reikėti įrašyti elektronines rinkmenas ir nuskaityti SharePoint jas iš SharePoint. Norėdami užtikrinti, kad elektroninių SF išrašymo tarnyba gali pasiekti savo SharePoint aplankus, sukonfigūruokite prieigą prie SharePoint.

Informacijos, kaip atlikti šį veiksmą, ieškokite Ryšio [konfigūravimas SharePoint](e-invoicing-create-sharepoint-connection.md).
