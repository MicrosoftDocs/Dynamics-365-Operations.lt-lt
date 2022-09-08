---
title: „Dynamics 365 Commerce“ peržiūra 10.0.30 (2022 m. lapkritis)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos Microsoft Dynamics 365 Commerce 10.0.30.
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405521"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>„Dynamics 365 Commerce“ peržiūra 10.0.30 (2022 m. lapkritis)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikiamos priemonės, kurios yra naujos arba pakeistos Microsoft Dynamics 365 Commerce 10.0.30 versijoje. Ši versija turi versijos 10.0.1362 versiją ir yra pasiekiama šiame grafike:

- **Peržiūros leidimas:** 2022 m. rugsėjo mėn.
- **Bendras leidimo pasiekiamumas (savaiminis naujinimas):** 2022 m. spalio mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. lapkričio mėn.

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Mes galime atnaujinti šį straipsnį, kad būtų įtrauktos funkcijos, kurios buvo įtrauktos į versiją iš pradžių publikuous šį straipsnį.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---------|------------------|----------------|--------------| 
| Klientų aptarnavimo tarnyba   | Susirašinėkite el. prekybos svetainėje naudodami bot Power Virtual Agents. | Ši funkcija leis el. komercijos svetainės vartotojams pasirinkti naudoti pokalbių Power Virtual Agents robotą palaikymo užklausoms. | Įgalino administruojami / asmenys, skirti galutiniams vartotojams |
| Įžvalgos  |  Srauto point of sale (EKA) naudojimo žinių apie įvykius jūsų sąskaitoje Application Insights. | [Prieiga prie žurnalų Application Insights](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  IT pro / programuotojo opt-in   |
|  Mokėjimai  | PayPal užsakymo palaikymas pasibaigus 29 dienų autorizavimo laikotarpiui. | Maksimalus PayPal autorizavimo laikotarpis yra 29 dienos, po kurio turi būti sugeneruotas naujas autorizavimo ir užsakymo ID. Kaip alternatyvą PayPal siūlo pasirinktį, pagal kurią užsakymą "PayPal" galima nurodyti kaip bendrą užsakymą, leidžiant kelis autorizavimus ir užuot generuous naują autorizavimo ir užsakymo ID per 29 dienas. | Konfigūruojant PayPal mokėjimo jungtį "Commerce Headquarters", **laukas OrderIntent buvo** įtrauktas ir gali turėti dvi vertes:<p><p>- **Autorizuoti** – ši konfigūracija yra numatytoji (jei laukas paliekamas tuščias, **Authorize** veiks kaip numatytasis). **OrderIntent konfigūruojamas** **taip**, kad autoriz būtų processing_instruction **PayPal** failo **NO_INSTRUCTION**. Užsakymas bus autorizuotas naudojant PayPal, o autorizavimo negalima modifikuoti, kai naudojama ši vertė.<p>- **Įrašyti** – kai **OrderIntent** reikšmė **nustatyta kaip Įrašyti**, ši processing_instruction **PayPal** **vertės ORDER_SAVED_EXPLICITLY.** Užsakymo nuorodos bus išsaugotos PayPal paslaugose, kai naudojama ši vertė.  |
| EKA prisijungimas  | [Įgalinti savitarnos diagnozės galimybes, skirtas prisijungti prie EKA](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Ši funkcija suteikia savitarnos paslaugos diagnozės galimybes kasos kanale (EKA) ir "Commerce Headquarters", kad darbuotojai ir vadybininkai galėtų greitai nustatyti ir išspręsti EKA prisijungimo problemų šaknies priežastis.<p><p>– trikties pranešimai, rodomi EKA prisijungimo ekrane, buvo patobulinta siekiant pateikti konkrečią šakninės priežasties informaciją, kuri gali padėti darbuotojams, naudojantiems EKA, suprasti, kas negerai, kad galėtų atlikti reikiamus veiksmus problemai išspręsti.<p>– tikrinimo registravimosi **funkciją** **galima** rasti "Commerce Headquarters" puslapyje Darbuotojai, kad EKA įrenginius nustačiusys parduotuvių vadovai galėtų imituoti EKA prisijungimą. Jei prisijungiama nesėkminga, ši funkcija pateikia neveikiančių trikčių diagnostikos vadovus, kad vadybininkai galėtų patikrinti susijusias konfigūracijas, išspręsti problemas ir patikrinti pataisas.  | Įjungta pagal numatytuosius parametrus |


## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

"Dynamics 365 Finance 10.0.30" apima platformos naujinimus. Norėdami sužinoti daugiau, žr. [10.0.30 finansų ir operacijų programėlių versijos platformos naujinimus](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti informacijos apie klaidos pataisas, įtrauktas į visus naujinimus, kurie yra 10.0.30 versijos dalis, prisijunkite prie ciklo tarnybų (LCS) [ir peržiūrėkite žinių bazės straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>"Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 2 planas

Norite sužinoti apie būsimas ir neseniai išleistas mūsų verslo programų ar platformos galimybes?

Patikrinkite ["Dynamics 365" ir pramonės debesys: 2022 išleidimo bangos 2 planas](/dynamics365-release-plan/2022wave2/). Visą išsamią informaciją užfiksavome viename dokumente, kurį galite naudoti planuodami.

### <a name="removed-and-deprecated-features"></a>Pašalintos ir pasenusios funkcijos

Pašalintos [arba pasenusios straipsnio Dynamics 365 Commerce](removed-deprecated-features-commerce.md) funkcijos aprašo priemones, kurios buvo pašalintos arba pasenusios "Commerce".

- *Pašalinta* funkcija nebėra įtraukta į produktą.
- *Nerekomenduojama* funkcija nebėra aktyviai tobulinama ir gali būti pašalinta iš būsimo naujinio.

Prieš pašalinant bet kokią priemonę iš produkto, [Dynamics 365 Commerce](removed-deprecated-features-commerce.md) pranešimai dėl nušalinimo bus pereiti prie pašalintų arba pasenusių funkcijų 12 mėnesių prieš pašalinimą.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, tai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
