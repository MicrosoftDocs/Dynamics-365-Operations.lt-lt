---
title: Užsakymo ieškos modulis
description: Šiame straipsnyje aprašomas užsakymo peržvalgos modulis ir paaiškinama, kaip jį konfigūruoti Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8c60ed0c334bf09916dd633302c6d813ea6f16b6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281460"
---
# <a name="order-lookup-module"></a>Užsakymo ieškos modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomas užsakymo peržvalgos modulis ir paaiškinama, kaip jį konfigūruoti Microsoft Dynamics 365 Commerce.

Užsakymų peržvalgos modulis pateikia formą, kurią klientai gali naudoti el. komercijos svetainėje pateiktiems užsakymams ieškoti. Jis naudojamas kaip svečio tikrinimo [funkcijos įgalinti užsakymo peržvalgą](order-lookup-guest.md) dalis. Užsakymo peržvalgos modulį galima naudoti norint peržiūrėti užsakymus, pateiktus per el. komercijos svetainę, mažmeninės prekybos elektroninį kasos punktą (EKA) arba skambučių centrą. Forma gali nuskaityti užsakymus, kuriuos pateikė ir svečių vartotojai, ir užregistruoti vartotojai.

Šioje iliustracijoje pateikiamas formos, kurią atvaizdavo užsakymo peržvalgos modulis, pavyzdys. Kai klientai užpildykite formą ir pasirinkite **Rasti užsakymą**, jie nukreipiami į užsakymo informacijos puslapį.

![Užsakymo peržvalgos modulio forma puslapyje.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Užsakymo ieškos modulio ypatybės

| Ypatybės pavadinimas     | Reikšmė     | Aprašas |
|-------------------|-----------|-------------|
| Antraštė           | Tekstas      | Antraštė, rodoma formos viršuje (pvz., "Rasti užsakymą"). |
| Raiškusis tekstas         | Raiškusis tekstas | Pasirinktinis aiškinamasis tekstas, rodomas po antrašte. |
| Užsakymo būsenos tipas | Išvardijimas      | <p>Pasirinkti informacijos, kurios bus pateikta formoje iš kliento, tipą kartu su užsakymo patvirtinimo ID. Šiuo metu palaikomos tolesnės vertės:</p><ul><li><b>El. paštas</b> – formoje bus laukas, kuriame klientai gali įvesti el. pašto adresą, kuris buvo naudojamas pateikiant užsakymą.</li><li><b>Nėra </b> – formoje nebus pateikta jokios informacijos, be užsakymo patvirtinimo ID.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Pridėkite užsakymo ieškos modulį prie puslapio

Užsakymo peržvalgos modulį galima pridėti prie bet kurio el. komercijos svetainės puslapio. Jei norite naudoti užsakymų peržvalgos modulį, kad įgalintumėte svečių tikrinimo užsakymo peržvalgą, būtinai įtraukite jį į puslapį, kuriame nereikalaujama, kad vartotojas būtų prisiregistravęs. Norint rasti puslapį reikia **prisiregistruoti?** „Commerce“ svetainės generatoriaus medžio rodinio parametras, pasirinkite **numatytąjį puslapį (būtinas)** ir žiūrėkite dešinios srities apačioje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įgalinti svečių išregistrų užsakymo peržvalgą](order-lookup-guest.md)

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
