---
title: Integruota didžioji knyga
description: Šioje temoje aprašomas didžiosios knygos duomenų integravimas tarp „Finance and Operations“ ir kitų „Dynamics 365“ programų, naudojant „Dataverse“.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e41d600464d707d01a0e319dd3cd343b04aa26b7
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782385"
---
# <a name="integrated-ledger"></a>Integruota didžioji knyga

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Verslo programoje didžiosios knygos duomenimis nustatoma pagrindinė sąranka, kaip įmonė vykdo veiklą. Pavyzdžiui, didžiosios knygos duomenimis nurodomi finansiniai metai, kurių įmonė laikosi, valiutos, kuriomis ji atlieka operacijas, ir naudojamos sąskaitos. Šioje temoje aprašomas šių pagrindinių finansinių duomenų integravimas.

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
