---
title: Užstrigusių paketinių užduočių nustatymas iš naujo
description: Šiame straipsnyje paaiškinama, kaip spręsti problemas naudojant paketines užduotis.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896024"
---
# <a name="reset-stuck-batch-jobs"></a>Užstrigusių paketinių užduočių nustatymas iš naujo


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Problema

Programoje gali kilti problemų dėl paketinių užduočių, kurios yra vykdymo arba atšaukimo būsenos „Microsoft Dynamics 365 Human Resources“ **ir nėra** **baigtos**.

## <a name="resolution"></a>Skiriamoji geba

Kai paketinės užduoties būsena yra Vykdoma arba Atšaukiama, galite grąžinti būseną **užduočiai** **atšaukti**. Atšaukę paketinę užduotį galite ją nustatyti iš naujo, nustatydami laukimo **būseną**. Tada jis bus paimtas dar kartą, kad būtų galima vykdyti kitame suplanuotame pakete.

1. Sistemos administravimo **darbo srityje pasirinkite puslapį** **Saitai ir pasirinkite** **Paketinės** užduotys.

2. Paketinių **užduočių sąrašo puslapyje pasirinkite** užduotį, kurią reikia nustatyti iš naujo.

3. Veiksmų juostelėje pasirinkite **Atšaukti ir** patvirtinkite veiksmą.

   > [!NOTE]
   > Veiksmas **Priverstinis atšaukimas** galimas tik tada, kai pasirinktos paketinės užduoties būsena yra **Vykdoma** arba **Atšaukiama** ir užduoties paketinio vykdymo arba atšaukimo procesai nėra vykdomi.

4. Veiksmų juostoje rinkitės **Keisti būseną**.

5. Puslapyje **Pasirinkti naują** būseną pasirinkite **Laukiama**, tada pasirinkite **Gerai**.

   ![Pasirinkti naują paketinės užduoties būseną.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Efektyvumo optimizavimas planuojant paketines užduotis po darbo valandų](hr-admin-troubleshooting-batch-jobs.md)<br>
[Efektyvumo optimizavimas naudojant automatinio valymo užduotis](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
