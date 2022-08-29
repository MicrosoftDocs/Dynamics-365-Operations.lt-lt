---
title: B2B el. komercijos svetainių SF valdymas
description: Šiame straipsnyje aprašomos SF valdymo Microsoft Dynamics 365 Commerce galimybės "verslas verslui" (B2B) el. komercijos žiniatinklio svetainėms.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: c1f3533eb711bf87fe226f5c61678b6939f35e13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274434"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>B2B el. komercijos svetainių SF valdymas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašomos SF valdymo Microsoft Dynamics 365 Commerce galimybės "verslas verslui" (B2B) el. komercijos žiniatinklio svetainėms.

Paprastai įmonės, apdorojančios B2B operacijas, priima užsakymus kliento kredite ir tada siunčia SF klientams po to, kai jie įvykdo užsakymą. Mokėjimo sąlygos apibrėžiamos klientams ir gali būti tam tikrų nuolaidų, kurios skatina klientus sumokėti laiku arba anksčiau. Siekiant padidinti tikimybę, kad mokėjimai bus gauti laiku, "B2B" el. komercijos svetainės leidžia klientams peržiūrėti visas SF. Klientas gali lengvai filtruoti SF, kad kartu su terminais būtų galima peržiūrėti apmokėtas, neapmokėtas ir iš dalies apmokėtas SF.

![SF puslapis B2B svetainėje.](../media/ViewInvoices.png)

> [!NOTE]
> Prisiregistravęs vartotojas gali peržiūrėti ir apmokėti tik savo SF. **·** **Jei** organizacijos sąskaita yra sukonfigūruota SF sąskaitos išplečiamajame meniu, esančiame kliento įrašo SF ir pristatymo "FastTab", esančiame "Commerce Headquarters", vartotojas galės peržiūrėti ir apmokėti organizacijos sąskaitos SF.

**B2B svetainės** SF puslapyje vartotojas gali pasirinkti neapmokėtą ar iš dalies apmokėtą SF, o tada pasirinkti mokėjimo **SF**. Pasirinkta SF įtraukta į krepšelį, ir vartotojas gali tęsti mokėjimą. Tada vartotojas gali nuspręsti, ar apmokėti visą SF sumą, ar dalinę sumą. Vartotojas negali naudoti laisvos formos sąskaitos mokėjimo būdo, kad galėtų mokėti už SF.

> [!NOTE]
> SF galima įtraukti į krepšelį, tik jei joje nėra prekių. Priešingai, prekes galima įtraukti į krepšelį, tik jei jame nėra SF. "Microsoft" planuoja pašalinti šį apribojimą būsimuose "Commerce" leidimuose.

![Krepšelio puslapis B2B svetainėje.](../media/PayInvoice.png)

**SF puslapyje** vartotojas taip pat gali pasirinkti Užklausą **SF, esančią** šalia SF. Tokiu būdu vartotojas gali prašyti išsamios informacijos apie SĄSKAITĄ faktūrą, išsiųstą registruotu el. pašto adresu.

![SF užklausos dialogo langas.](../media/RequestInvoice2.png)

Kai vartotojas reikalauja SF, užklausa perkeliama į **mano sąskaitos puslapio B2B** **užklausų skyrių**. Tada, **kai P-0001** **ir Sinchronizuoti užsakymų ir kanalo užklausų užduotis paleidžiamos "Commerce Headquarters", SF el. paštas paleidžiamas**, o B2B užklausos būsena pažymima kaip baigta.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
