---
title: Apie vidinės įmonės pirkimo ir pardavimo užsakymų kūrimą keliose įmonėse
description: Šioje temoje paaiškinama, kaip kurti vidinės įmonės pirkimo užsakymus arba pardavimo užsakymus keliose įmonėse
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5d756a82abb7e7b19080128353d863f29837fc5b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548419"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Apie vidinės įmonės pirkimo ir pardavimo užsakymų kūrimą keliose įmonėse

[!include [banner](../../includes/banner.md)]

„Microsoft Dynamics 365 Supply Chain Management“ nėra apribota tik laikyti vieną gamybos įmonę ir kelis pardavimo įmones. Vidinėje įmonėje visos įmonės gali būti nustatytos tiek kaip prekybos, tiek kaip gamybos įmonės.

Jei tą pačią prekę gali pristatyti kelios įmonės, galite laisvai rinktis, iš ko norite pirkti. Atnaujinimai apdorojami net ir tuo atveju, jei vienas pardavimo užsakymas tampa keliais pirkimo užsakymais.

Tokiu pat būdu galite automatiškai sukurti vieną vidinės įmonės pirkimo užsakymą, pradinį savo įmonės pardavimo užsakymą, o tada, sukurdami kelis vidinės įmonės pirkimo užsakymus, galite nurodyti, kad užsakymą vykdytų kelios vidinės įmonės tiekėjų įmonės. „Microsoft Dynamics 365 Supply Chain Management“ tiekėjų įmonėse automatiškai sukurs vidinės įmonės pardavimo užsakymus.

Norint tai atlikti, visos įmonės turi būti nustatytos kaip prekybiniai ryšiai. Tiekėjų įmonės turi būti nustatytos kaip vidinės įmonės tiekėjai ir jos turi „Microsoft Dynamics 365 Supply Chain Management“ būti pirminiai susijusios prekės tiekėjai. Pardavimo užsakymo **antraštės rodinyje**, turite pasirinkti **Automatiškai kurti vidinės įmonės užsakymus** laukelį ir **tiesioginio pristatymo** laukelį **Vidinės įmonės nustatymuose** „FastTab“. Tai numatytasis parametras.

Pardavimo eilutes galite kurti įprastu būdu. Kai įrašą paliekate, pasirodo pranešimas, informuojantis, kad buvo sukurti vidinės įmonės pirkimo ir pardavimo užsakymai. Pranešime taip pat pateikiami jų nauji užsakymai. Norėdami peržiūrėti vidinės įmonės pardavimo užsakymus, sukurtus jūsų tiekėjų įmonėse, atidarykite pradinį pardavimo užsakymą ir skirtuko **Bendra** skirtuke, **Susijusi informacija** grupė pasirinkite **Nuorodos**.

Atidarę tiekėjų vidinės įmonės pirkimo užsakymus pamatysite, kad „Microsoft Dynamics 365 Supply Chain Management“ automatiškai įveda kiekvieno tiekėjo pradinio pardavimo užsakymo numerį ir vidinės įmonės pardavimo užsakymo numerį.

Panašiai, atidarę tiekėjų vidinės įmonės pirkimo užsakymus pamatysite, kad „Microsoft Dynamics 365 Supply Chain Management“ automatiškai įveda kiekvieno tiekėjo pradinio pardavimo užsakymo numerį ir vidinės įmonės pirkimo užsakymo numerį.

> [!NOTE]
> Jei užsakymo prekės yra vienoje iš vidinės įmonės įmonių, tačiau jų nėra kitoje, programa „Microsoft Dynamics 365 Supply Chain Management“ sukuria vidinės įmonės užsakymus, skirtus tiekėjo įmonei, kurioje prekių yra, ir sustabdo kitai įmonei skirto užsakymo kūrimą. Kai taip atsitinka, yra rodomas pranešimas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
