---
title: Integruota didžioji knyga
description: Šiame straipsnyje aprašomas DK duomenų integravimas tarp finansų ir operacijų bei kitų "Dynamics 365" programų naudojant Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e83d66f3f8c8927b9baaf99838a4e242e7e011dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847195"
---
# <a name="integrated-ledger"></a>Integruota didžioji knyga

[!include [banner](../../includes/banner.md)]



Verslo programoje didžiosios knygos duomenimis nustatoma pagrindinė sąranka, kaip įmonė vykdo veiklą. Pavyzdžiui, didžiosios knygos duomenimis nurodomi finansiniai metai, kurių įmonė laikosi, valiutos, kuriomis ji atlieka operacijas, ir naudojamos sąskaitos. Šiame straipsnyje aprašomas šių pagrindinių finansinių duomenų integravimas.

## <a name="templates"></a>Šablonai

Didžiosios knygos duomenis sudaro pagrindinių finansinių lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.

„Finance and operations” programos | „Customer engagement“ programos     | Aprašas
---------------------------------|----------------------------------|------------
[CDS valiutos kursai](mapping-reference.md#123) | „msdyn_currencyexchangerates” |
[Sąskaitų planas](mapping-reference.md#121) | „msdyn_chartofaccountses” |
[Valiutos](mapping-reference.md#218) | transactioncurrencies |
[Valiutos kurso valiutų pora](mapping-reference.md#122) | „msdyn_currencyexchangeratepairs” |
[Valiutos kurso tipas](mapping-reference.md#129) | „msdyn_exchangeratetypes” |
[Finansinės dimensijos formatas](mapping-reference.md#130) | „msdyn_financialdimensionformats” |
[Finansinės dimensijos](mapping-reference.md#128) | „msdyn_dimensionattributes” |
[Ataskaitinio kalendoriaus integravimo objektas](mapping-reference.md#132) | „msdyn_fiscalcalendars” |
[Ataskaitinis kalendorinis laikotarpis](mapping-reference.md#131) | „msdyn_fiscalcalendarperiods” |
[Ataskaitinių kalendorinių metų integravimo objektas](mapping-reference.md#133) | „msdyn_fiscalcalendaryears” |
[Ledger](mapping-reference.md#148) | „msdyn_ledgers” |
[Korespondentinė sąskaita, subsąskaita](mapping-reference.md#152) | „msdyn_mainaccounts” |
[Pagrindinių sąskaitų kategorijos](mapping-reference.md#151) | „msdyn_mainaccountcategories” |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
