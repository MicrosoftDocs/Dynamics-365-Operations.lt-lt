---
title: Sumų rodymo ataskaitose ir dokumentuose būdo naujinimas
description: Šiame straipsnyje pateikta informacija apie tai, kaip atnaujinti, kaip sumos rodomos ataskaitose ir kituose Estijos, Latvijos, Lietuvos, Lenkijos, Čekijos Respublika, Vengrijos ir Rusijos dokumentuose.
author: AdamTrukawka
ms.date: 01/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264254
ms.search.form: Currency
ms.openlocfilehash: f9ddb4e2616c858bf8d68e485b88bf4fb7d9d5c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273817"
---
# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a>Sumų rodymo ataskaitose ir dokumentuose būdo naujinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie tai, kaip atnaujinti, kaip sumos rodomos ataskaitose ir kituose Estijos, Latvijos, Lietuvos, Lenkijos, Čekijos Respublika, Vengrijos ir Rusijos dokumentuose.

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
   |       <strong>Giminė</strong>       |  Pasirinkite **Vyriška**, **Moteriška** arba **Neutrali**. Šis parametras gali turėti įtakos vietinės sumos linksniavimo, rodomo vietinės kalbos tekste grynųjų pinigų užsakyme, tekstui. Pavyzdžiui, **kai** nustatote valiutos EUR **lytį kaip Neuter**, suma 101 EUR *rašoma Čekų kalba grynųjų pinigų užsakyme kaip Jedno euras 01 cent*.  |

5. Pasirinkite **Įrašyti**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
