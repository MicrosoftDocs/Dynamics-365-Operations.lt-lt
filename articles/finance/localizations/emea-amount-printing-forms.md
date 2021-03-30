---
title: Sumų rodymo ataskaitose ir dokumentuose būdo naujinimas
description: Šioje temoje pateikiama informacija apie tai, kaip naujinti sumų rodymą ataskaitose ir kituose dokumentuose, skirtuose Estijai, Latvijai, Lietuvai, Lenkijai, Čekijos Respublikai, Vengrijai, ir Rusijai.
author: anasyash
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Currency
audience: Application User
ms.reviewer: kfend
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 62e7b5146c142c8d3ce4a0e79f9698695216614d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209892"
---
# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Sumų rodymo ataskaitose ir dokumentuose būdo naujinimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie tai, kaip naujinti sumų rodymą ataskaitose ir kituose dokumentuose, skirtuose Estijai, Latvijai, Lietuvai, Lenkijai, Čekijos Respublikai, Vengrijai, ir Rusijai.

Jei pagrindinis juridinio subjekto adresas yra Estijoje,Latvijoje, Lietuvoje, Lenkijoje, Čekijos Respublikoje, Vengrijoje arba Rusijoje, galite nustatyti valiutos vienetų ir antrinių vienetų visus pavadinimus bei trumpus pavadinimus. Šiuos pavadinimus galima naudoti norint pakeisti sumų rodymo dokumentuose ir ataskaitose būdą. Pavyzdžiui, suma **100,20 LTL** gali būti rodoma kaip **100 litų ir 20 centų**.

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a>Valiutos vienetų ir antrinių vienetų visų pavadinimų bei trumpų pavadinimų nustatymas
Norėdami nustatyti valiutos vienetų ir antrinių vienetų visus pavadinimus bei trumpus pavadinimus, atlikite tolesnius veiksmus.

1. Atidarykite puslapį **Valiutos**.
2. Pasirinkite valiutą.
3. Veiksmų srityje pasirinkite **Linksniavimas**.
4. Norėdami įtraukti pilną ir trumpą kalbos pavadinimus, pasirinkite **Naujas** ir įveskite informaciją toliau nurodytuose laukuose.

   |             Laukas                                                           |                        aprašymas                                                                                                                                                                                                                                                |
   |------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |                       <strong>Kalba</strong>                        |                                                                                                               Pasirinkti šio teksto kalbą.                                                                                                                |
   |    <strong>Vienaskaitos vardininkas (laukų grupė Vienetų pavadinimas)</strong>    |                                                                                       Įveskite valiutos pavadinimą vienaskaitos forma. Pvz., valiutos litas vienaskaitos forma yra litas.                                                                                       |
   |     <strong>Daugiskaitos vardininkas (laukų grupė Vienetų pavadinimas)</strong>     | Įveskite valiutos pavadinimą daugiskaitos forma. Pavyzdžiui, įveskite litai. <strong>Pastaba</strong>: laukai <strong>Vienaskaitos kilmininkas</strong> ir <strong>Daugiskaitos kilmininkas</strong> rodomi atsižvelgiant į lauke <strong>Kalba</strong> pasirinktą kalbą. |
   | <strong>Laukas Vienaskaitos vardininkas (laukų grupė Dalių pavadinimas)</strong> |                                                                                                        Įveskite valiutos antrinio vieneto pavadinimą vienaskaitos forma.                                                                                                         |
   |     <strong>Daugiskaitos vardininkas (laukų grupė Dalių pavadinimas)</strong>     |                                                                                                         Įveskite valiutos antrinio vieneto pavadinimą daugiskaitos forma.                                                                                                          |
   |    <strong>Trumpas vienetų pavadinimas (laukų grupė Trumpas pavadinimas)</strong>    |                                                                                         Įveskite ISO kodą, kad identifikuotumėte valiutą. Pavyzdžiui, įveskite LTL identifikuoti litui..                                                                                         |
   |   <strong>Trumpas dalių pavadinimas (laukų grupė Trumpas pavadinimas)</strong>    |                                                                                               Įveskite valiutos antrinio vieneto nominaliąją vertę. Pavyzdžiui, įveskite centas.                                                                                               |
   |       <strong>Jungtukas „ir“ tarp vienetų ir dalių</strong>       |                                     Pažymėkite, jei norite spausdinti jungtuką „ir“ tarp valiutos vienetų ir vieneto dalių. Pvz., SF ir ataskaitose 100,20 LTL suma rodoma kaip 100 litų ir 20 centų.                                      |
   |       <strong>Giminė</strong>       |  Pasirinkite **Vyriška**, **Moteriška** arba **Neutrali**. Šis parametras gali turėti įtakos vietinės sumos linksniavimo, rodomo vietinės kalbos tekste grynųjų pinigų užsakyme, tekstui. Pavyzdžiui, nustatydami parametrą **Giminė** EUR valiutai į **Neutrali**, suma 1,01 EUR užrašoma grynųjų pinigų užsakyme čekų kalba kaip *„Edno euro 01 cent“*.  |

5. Pasirinkite **Įrašyti**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]