---
title: Nuomos žurnalo pavadinimų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti nuomos žurnalų pavadinimus. Nuomos žurnalų pavadinimai nurodo žurnalus, kuriuose įrašai, kilę iš turto nuomos, registruojami.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b9d8136ae4f960a586b9526751fc8bf6e7675c8d
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890755"
---
# <a name="set-up-lease-journal-names"></a>Nuomos žurnalo pavadinimų nustatymas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Nuomos žurnalų pavadinimai nurodo žurnalus, kuriuose turto nuomos operacijos registruojamos. Puslapio **Turto nuomos parametrai** laukuose **Pirminis pripažinimas** ir **Mėnesio žurnalo pavadinimas** bus rodomi tik tie žurnalų pavadinimai, kurie priskirti žurnalo tipui **Turto nuoma**. Lauke **SF žurnalo pavadinimas** galima priskirti tik žurnalo tipą **Tiekėjo SF įrašymas**.

Sistema užrakina tam tikrus finansinius laukus, kad išvengtų nuokrypių tarp operacijų ir grafikų. Kai kurie laukai, kurie yra užrakinti, apima **sąskaitą**, **sumas**, **finansines dimensijas**, **valiutą** ir **operacijos tipą**. Be to, žurnalo įrašų eilučių nebus galima įtraukti į žurnalo žurnalo įrašus, nes dėl to gali atsirasti nuokrypių tarp grafikų ir operacijų.


Norėdami konfigūruoti nuomos žurnalų pavadinimus, atlikite šiuos veiksmus.

1. Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.
2. Skirtuko **Bendra** lauke **Pirminio pripažinimo žurnalo pavadinimas** pasirinkite žurnalą. Visi pradiniai pripažinimo žurnalo įrašai bus registruojami į šį žurnalo pavadinimą.
3. Lauke **SF žurnalo pavadinimas** pasirinkite žurnalą. Jei nuomos knygos parinktis **Sumokėti tiekėjui** nustatyta į **Taip**, nuomos ir išlaidų apmokėjimo SF bus užregistruotos šiame žurnalo pavadinime.
4. Lauke **Nuomos žurnalo pavadinimas** pasirinkite žurnalą. Visi nusidėvėjimo, palūkanų ir trumpojo laikotarpio perklasifikavimo įrašai bus registruojami į šį žurnalo pavadinimą. Jei nuomos knygos parinktis **Sumokėti tiekėjui** nustatyta į **Ne**, nuomos mokėjimo ir išlaidų apmokėjimo įrašai bus taip pat užregistruoti šiame žurnalo pavadinime.
5. Lauke Nuomos **modifikavimo žurnalo** pavadinimas pasirinkite žurnalą. Nuomos koregavimo, atleidimo ir pablogėjimo operacijos bus registruojamos šiame žurnalo pavadinime. Jūsų pasirinktu žurnalo pavadinimui neturi būti priskirta darbo eiga arba patvirtinimas. Jei nuomos modifikavimo žurnalo pavadinimas nėra nustatytas, nuomos koregavimo, atleidimo ir pablogėjimo operacijos bus registruojamos žurnalo pavadinime, kuris pasirinktas nuomos **žurnalo pavadinimo** lauke. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
