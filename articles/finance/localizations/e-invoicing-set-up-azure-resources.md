---
title: Nustatyti "Azure" išteklius elektroninėms SF išrašyti
description: Šioje temoje pateikta proceso, kaip nustatyti išteklius elektroninių SF Microsoft Azure išrašymo metu, apžvalga.
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
ms.openlocfilehash: cb1fcddce1054aebf9ef70ba69eb7aca98093cbe
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371937"
---
# <a name="set-up-azure-resources-for-electronic-invoicing"></a>Nustatyti "Azure" išteklius elektroninėms SF išrašyti

[!include [banner](../includes/banner.md)]

Elektroninių SF išrašymo Microsoft Azure išteklių nustatymo procesas turi tris veiksmus. Pirmi du veiksmai " "Azure" kodo "Azure" portale kūrimas ir "Azure" saugyklos sąskaitos kūrimas "Azure" portale" yra privalomi. Trečiasis veiksmas "Ryšio konfigūravimas SharePoint " yra pasirinktinis.

## <a name="create-an-azure-key-vault-in-the-azure-portal"></a>Kurti "Azure" kodo saugyklą "Azure" portale

Sukurkite kodo "Azure" abonementą. Rekomenduojame sukurti atskirą elektroninio SF išrašymo raktų saugyklą, o jūs nejungitumėte paslapčių su kitomis programomis. Sukurkite tiek paslapčių ir sertifikatų, kiek jums reikia savo scenarijams elektroniniuose dokumentuose. Turite sukurti bent vieną slaptažodį, kad būtų saugomas "Azure" saugyklos sąskaitos, kurią sukursite kitame veiksme, bendrai naudojamos prieigos parašo (SAS) atpažinimo ženklas.

Informacijos, kaip atlikti šį veiksmą, rasite " [Azure" portalo "Azure" portalo "Azure" rakto saugyklos kūrimas](e-invoicing-create-azure-key-vault-azure-portal.md).

## <a name="create-an-azure-storage-account-in-the-azure-portal"></a>"Azure" saugyklos sąskaitos kūrimas "Azure" portale

Jūs turite visus elektroninius dokumentus ir rinkmenas, sugeneruotas elektroninių SF išrašymo tarnybos, arba įveskite tarnybą. Šie dokumentai ir rinkmenos saugomi "Azure" saugykloje, kurią sukuriate savo "Azure" abonemente. Tarnyba turės prieigą prie jūsų saugyklos abonemento, naudodama SAS atpažinimo ženklą, kuris paimtas iš jūsų rakto Vault slapto kodo.

Informacijos, kaip atlikti šį veiksmą, ieškokite " [Azure" saugyklos sąskaitos kūrimas "Azure" portale](e-invoicing-create-azure-storage-account-azure-portal.md).

## <a name="configure-a-sharepoint-connection"></a>Ryšio konfigūravimas SharePoint

Kai kuriuose scenarijuose gali reikėti įrašyti elektronines rinkmenas ir nuskaityti SharePoint jas iš SharePoint. Norėdami užtikrinti, kad elektroninių SF išrašymo tarnyba gali pasiekti savo SharePoint aplankus, sukonfigūruokite prieigą prie SharePoint.

Informacijos, kaip atlikti šį veiksmą, ieškokite Ryšio [konfigūravimas SharePoint](e-invoicing-create-sharepoint-connection.md).
