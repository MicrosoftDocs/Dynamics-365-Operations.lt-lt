---
title: „Dynamics 365 Commerce“ 10.0.31 išankstinė peržiūra (2023 m. vasaris)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos Microsoft Dynamics 365 Commerce 10.0.31.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: ed4325095163415d05a56128cb1f0334440fe0e5
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787532"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>„Dynamics 365 Commerce“ 10.0.31 išankstinė peržiūra (2023 m. vasaris)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikiamos priemonės, kurios yra naujos arba pakeistos Microsoft Dynamics 365 Commerce 10.0.31 versijoje. Ši versija turi versijos 10.0.1406 versiją ir yra pasiekiama šiame grafike:

- **Leidimo peržiūra:** 2022 m. spalio mėn.
- **Bendras leidimo prieinamumas (savaiminis naujinimas):** 2023 m. sausio mėnuo
- **Bendras leidimo prieinamumas (automatinis naujinimas):** 2023 m. vasario mėnuo

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Mes galime atnaujinti šį straipsnį, kad būtų įtrauktos funkcijos, kurios buvo įtrauktos į versiją iš pradžių publikuous šį straipsnį.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---|---|---|---|
| Klaidų kodai | "Commerce" pateikė standartines klaidų nuorodas, kurios turi būti įtrauktos į interneto kanalo tikrinimo klaidas, pateikiamas interneto pirkėjams.| [Tikrinimo modulio klaidų kodai](../checkout-module-error-codes.md)  | Įjungta pagal numatytuosius parametrus |
| Mokėjimai | [Įjungti Adyen Mokėjimo su "Dynamics 365" mokėjimo jungtį](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | El. komercijos klientai, naudojantys palaikomus įrenginius arba naršykles, gali naudoti Algalapio mokėjimo krepšelyje ir tikrinimo puslapius. | Programuotojo atsisakymas |
| Mokėjimai  |  "Commerce" įtraukė galimybę riboti vartotojų sąveiką su pasikartojančiais mokėjimo atpažinimo ženklus visoje "Commerce Headquarters" vartotojo sąsajoje. Mokėjimo formos, pavyzdžiui, **skambučių centro** pardavimo užsakymo puslapis, daugiau nerodo anksčiau naudotos kliento periodinio mokėjimo atpažinimo ženklo, kuris bus naudojamas naujoje operacijoje. Tik nustatyta failo kortelė įeis į "Commerce **Customer Payments** " ekraną arba sutartis su klientu apmokant pardavimo užsakymą, bus pristatyta skambučių centrui arba "Commerce Headquarters" vartotojams, vykdant naujos operacijos mokėjimą. | [Mokėjimo atpažinimo ženklo naudojimo apribojimas](../dev-itpro/limit-token-usage.md)  |  Funkcijų valdymas<p>*Apriboti mokėjimo atpažinimo ženklo naudojimą pagal užsakymo kontekstą*  |
| EKA | [Kurti pirkimo užsakymus iš EKA](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Patobulinta atsargų gavimo operacija, atliekama point of sale (EKA) programoje, kuri leidžia vartotojams kurti, redaguoti ir patvirtinti pirkimo užsakymo užklausas. |  Funkcijų valdymas<p>*Galimybė sukurti pirkimo užsakymo užklausą EKA*   |
| Turimos papildomos kalbos | Galimos keturios papildomos kalbos | Vartotojo pasirinkimus pageidaujamuose kalbų sąraše galima naudoti keturios naujos kalbos: Korėjos, Portugalos (Portugal), Vietnamo ir kinų (tradicinė). Norėdami pasirinkti šią pasirinktį, eikite į **Vartotojo pasirinkčių \> kalbos \> ir šalies / regiono nuostatą**. | Lokalizuotos nuostatos |  



## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Commerce“ 10.0.31 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.31 versijos platformos naujinimus (2023 m. vasario mėn.).](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md) 
  

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti informacijos apie klaidos pataisas, įtrauktas į visus naujinimus, kurie yra 10.0.31 versijos dalis, Microsoft Dynamics  [prisijunkite prie ciklo tarnybų ir peržiūrėkite žinių bazės straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>"Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 2 planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Patikrinkite ["Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 2 planas](/dynamics365-release-plan/2022wave2/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-commerce-features"></a>Pašalintos ir pasenusios "Commerce" funkcijos

Pašalintos [arba pasenusios straipsnio Dynamics 365 Commerce](removed-deprecated-features-commerce.md) funkcijos aprašo priemones, kurios buvo pašalintos arba pasenusios "Commerce".

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nerekomenduojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant bet kokią priemonę iš produkto, [Dynamics 365 Commerce](removed-deprecated-features-commerce.md) pranešimai dėl nušalinimo bus pereiti prie pašalintų arba pasenusių funkcijų 12 mėnesių prieš pašalinimą.


Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
