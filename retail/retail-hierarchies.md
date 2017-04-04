---
title: "Mažmeninės prekybos hierarchijos"
description: "Šiame straipsnyje aprašytos „Microsoft Dynamics AX“ mažmeninės prekybos hierarchijos."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5fed76e09ef2a64bc2aad2cf6ad7dcfa290acab1
ms.lasthandoff: 03/31/2017


---

# <a name="retail-hierarchies"></a>Mažmeninės prekybos hierarchijos

Šiame straipsnyje aprašytos „Microsoft Dynamics AX“ mažmeninės prekybos hierarchijos.

Galite sukurti mažmeninės prekybos kategorijų hierarchiją ir tvarkyti produktus, kuriuos parduodate mažmeninės prekybos kanalais. Mažmeninės prekybos produktų hierarchijas galite naudoti produktams suskirstyti į kategorijas ar grupuoti. Tada šiuos produktus galite naudoti produktų asortimentams ir klientų lojalumo programoms kurti. Taip pat galite priskirti produkto atributus ir ypatybes, priskirti kainų struktūrą, įtraukti produktus į produktų akcijas ir naudoti produktus ataskaitoms teikti. Galite sukurti vieną mažmeninės prekybos kategorijų hierarchiją, kuri nurodytų visus produktus ir kategorijas jūsų organizacijoje, o tada naudoti tą kategorijų hierarchiją keliais tikslais. Arba galite sukurti kelias mažmeninės prekybos kategorijų hierarchijas specialiais tikslais, pvz., produktų akcijoms. Kai sukuriate mažmeninės prekybos produktų hierarchiją, turite priskirti kategorijų hierarchijos tipą, kad nustatytumėte kategorijų hierarchijos paskirtį. Pavyzdžiui, tik produktų hierarchijos, kurioms priskirtas tipas **Mažmeninės prekybos naršymo hierarchija**, nurodomos, kai naršote produktus pagal kategoriją internete arba naudodami elektroninį kasos aparatą (EKA).

## <a name="retail-hierarchy-types"></a>Mažmeninės prekybos hierarchijų tipai
Tolesnėje lentelėje nurodyti galimi mažmeninės kategorijų hierarchijų tipai ir kiekvieno tipo bendroji paskirtis.

| Kategorijų hierarchijos tipas       | Paskirtis                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mažmeninės prekybos produkto hierarchija      | Naudokite šį hierarchijos tipą, norėdami nurodyti bendrą savo organizacijos produktų hierarchiją. Šio tipo hierarchiją galite naudoti reklamavimo, kainų nustatymo ir akcijų, ataskaitų teikimo ir asortimento planavimo tikslais. Tik vienai mažmeninės prekybos produktų hierarchijai galima priskirti šio tipo hierarchiją.                                       |
| Papildoma mažmeninės prekybos hierarchija | Naudokite šio tipo hierarchiją visoms papildomoms mažmeninės prekybos kategorijų hierarchijoms kurti. Pvz., pavasarį vykdote maudymosi kostiumėlių akciją. Todėl maudymosi produktus įtraukiate į atskirą kategorijų hierarchiją ir akcijos kainas pritaikote skirtingoms produktų kategorijoms. |
| Mažmeninės prekybos naršymo hierarchija   | Naudokite šio tipo hierarchiją, norėdami grupuoti ir tvarkyti produktus į kategorijas, kad produktus būtų galima naršyti internete arba EKA.                                                                                                                                                                                       |

Naudodami mažmeninės prekybos kategorijų hierarchiją savo produktus struktūrizuoti, galite nustatyti ir prižiūrėti produkto atributus ir ypatybes kategorijos lygiu. Šie atributai ir ypatybės apima produktų dimensijų ir EKA parametrus. Visiems produktams, kuriuos priskiriate kategorijoms, automatiškai priskiriami jūsų nurodyti atributai ir ypatybės. Taip pat galite nukopijuoti bet kurio produkto ypatybių parametrus, norėdami vienu metu padidinti pasirinktos kategorijos produktų skaičių.


