---
title: Mažmeninės prekybos hierarchijos
description: Šiame straipsnyje aprašytos „Dynamics 365 Commerce“ mažmeninės prekybos hierarchijos.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: cf8db2c828f99dfd4c220966e31894dcd6eda572
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023449"
---
# <a name="retail-hierarchies"></a>Mažmeninės prekybos hierarchijos

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos „Dynamics 365 Commerce“ hierarchijos.

Galite sukurti kategorijų hierarchiją, kad galėtumėte tvarkyti produktus, kuriuos parduodate per kanalus. Produktų klasifikavimui ar grupavimui galite naudoti produktų hierarchijas. Tada šiuos produktus galite naudoti produktų asortimentams ir klientų lojalumo programoms kurti. Taip pat galite priskirti produkto atributus ir ypatybes, priskirti kainų struktūrą, įtraukti produktus į produktų akcijas ir naudoti produktus ataskaitoms teikti. Galite sukurti vieną kategorijų hierarchiją, kad būtų pavaizduoti visi jūsų organizacijos produktai ir kategorijos, tada galite naudoti tą kategorijų hierarchiją kitiems tikslams. Arba galite sukurti kelias kategorijų hierarchijas specialiais tikslais, pvz., produktų akcijoms. Sukurdami produktų hierarchiją, turite priskirti kategorijos hierarchijos tipą, kad nustatytumėte kategorijų hierarchijos tikslą. Pavyzdžiui, kai naršote produktus pagal kategorijas internete arba elektroniniame kasos aparate (EKA), nurodomos tik tos produktų hierarchijos, kurioms priskirtas tipas **„Commerce“ naršymo hierarchija**.

## <a name="hierarchy-types"></a>Hierarchijos tipai

Toliau nurodytoje lentelėje pateikiami galimi kategorijų hierarchijų tipai ir bendra kiekvieno tipo funkcija.

| Kategorijų hierarchijos tipas       | Paskirtis |
|-------------------------------|---------|
| Produktų hierarchija      | Naudokite šį hierarchijos tipą, norėdami nurodyti bendrą savo organizacijos produktų hierarchiją. Šio tipo hierarchiją galite naudoti reklamavimo, kainų nustatymo ir akcijų, ataskaitų teikimo ir asortimento planavimo tikslais. Šiam hierarchijos tipui galima priskirti tik vieną produkto hierarchiją. |
| Papildoma hierarchija | Šį hierarchijos tipą naudokite bet kokioms papildomoms kategorijų hierarchijoms, kurias norite sukurti. Pvz., pavasarį vykdote maudymosi kostiumėlių akciją. Todėl maudymosi produktus įtraukiate į atskirą kategorijų hierarchiją ir akcijos kainas pritaikote skirtingoms produktų kategorijoms. |
| Naršymo hierarchija   | Naudokite šio tipo hierarchiją, norėdami grupuoti ir tvarkyti produktus į kategorijas, kad produktus būtų galima naršyti internete arba EKA. |

Naudodami kategorijų hierarchiją savo produktams struktūruoti, galite nustatyti ir prižiūrėti produkto atributus ir savybes kategorijos lygiu. Šie atributai ir ypatybės apima produktų dimensijų ir EKA parametrus. Visiems produktams, kuriuos priskiriate kategorijoms, automatiškai priskiriami jūsų nurodyti atributai ir ypatybės. Taip pat galite nukopijuoti bet kurio produkto ypatybių parametrus, norėdami vienu metu padidinti pasirinktos kategorijos produktų skaičių.
