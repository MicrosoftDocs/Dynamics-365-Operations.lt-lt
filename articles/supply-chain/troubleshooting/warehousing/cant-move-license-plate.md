---
title: Negalima perkelti numerio lentelės, jei leidžiamas tuščias išdavimas ir tuščias gavimas
description: Negalite perkelti numerio lentelės, jei serijinis numeris yra tuščias išdavimas ir tuščias gavimas. Jis bus fiksuotas, kad serijos numerio laukas būtų pasirinktinis.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0047f79aa417c8fc910447505f07963d014f54e7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477084"
---
# <a name="cant-move-license-plate-if-serial-number-has-blank-issue-and-blank-receipt-allowed"></a>Negalite perkelti numerio lentelės, jei serijinis numeris yra tuščias išdavimas ir tuščias gavimas.

## <a name="symptoms"></a>Požymiai

Negalite perkelti licencijos lentelės naudodami **Perkėlimo** meniu elementą, jei serijinis numeris turi nustatymus *Tuščia problema leidžiama* ir *Tuščias kvitas leidžiamas* sekimo dimensijos grupėje ir jei esama kelių licencijos lentelių toje pačioje vietoje, kurių keletas turi serijinius numerius ir keletas neturi.

## <a name="resolution"></a>Sprendimas

Ši triktis bus pataisyta pakeitimais, kurie yra patalpinti [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687). Šie pakeitimai padarys **Serijinio numerio** laukelį pasirenkamą, kai tuščias kvitas ir tuščia triktis yra leidžiami.
