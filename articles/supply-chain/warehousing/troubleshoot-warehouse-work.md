---
title: Trikčių šalinimo sandėlio darbas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio darbu „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: b1814f7b23efda2cabdb7bfc7bea4de6e3d6ec2f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237064"
---
# <a name="troubleshoot-warehouse-work"></a>Trikčių šalinimo sandėlio darbas

[!include [banner](../includes/banner.md)]

Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio darbu „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Negaliu perkelti licencijos lentelių, kurių serijinio numerio elementai, kai tuščia problema ir tuščias gavimas yra leidžiami sekimo dimensijos grupėje.

### <a name="issue-description"></a>Problemos aprašas

Negalite perkelti licencijos lentelės naudodami **Perkėlimo** meniu elementą, jei serijinis numeris turi nustatymus *Tuščia problema leidžiama* ir *Tuščias kvitas leidžiamas* sekimo dimensijos grupėje ir jei esama kelių licencijos lentelių toje pačioje vietoje, kurių keletas turi serijinius numerius ir keletas neturi.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Ši triktis bus pataisyta pakeitimais, kurie yra patalpinti [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Šie pakeitimai padarys **Serijinio numerio** laukelį pasirenkamą, kai tuščias kvitas ir tuščia triktis yra leidžiami.

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Gaunu tolesnį klaidos pranešimą sandėlio pgramoje, kai apdoroju perkėlimus: „Inventoriaus savininkas %1 neleidžiamas šiame procese."

### <a name="issue-description"></a>Problemos aprašas

**Savininko** sekimo dimensijos trūksta, kai sandėlio programa naudojama siekiant atlikti perkėlimus. Įprastas inventoriaus perkelimo žurnalas iš „Supply Chain Management“ kliente ima dirbti kaip numatyta ir gali būti publikuotas tik jei **Savininko** dimensija užpildyta.

### <a name="issue-resolution"></a>Problemos paaiškinimas

„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą. Šiuo metu sandėlio valdymo procesas palaiko tik inventorių, kurį valdo juridinis asmuo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]