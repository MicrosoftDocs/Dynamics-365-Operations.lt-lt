---
title: WVz., nauja ir pakeista Dynamics 365 Commerce 10.0.29 (2022 m. spalio mėn.)
description: Šiame straipsnyje aprašomos priemonės, kurios yra naujos arba pakeistos Microsoft Dynamics 365 Commerce 10.0.29.
author: josaw1
ms.date: 09/29/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0629228516d688abf4dcd4280d1ad676f8f35331
ms.sourcegitcommit: ce4e56d798281258479432ad821287a1cc8e26bf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2022
ms.locfileid: "9601577"
---
# <a name="whats-new-or-changed-in-dynamics-365-commerce-10029-october-2022"></a>Kas nauja ar pasikeitė „Dynamics 365 Commerce“ 10.0.29 versijoje (2022 m. spalio mėn.)

[!include [banner](../includes/banner.md)]


Šiame straipsnyje pateikiamos priemonės, kurios yra naujos arba pakeistos Microsoft Dynamics 365 Commerce versijoje 10.0.29. Ši versija turi versijos 10.0.1326 versiją ir yra pasiekiama šiame grafike:

- **Peržiūrėti leidimą:** 2022 m. rugpjūčio mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. rugsėjo mėn.
- **Bendras leidimo pasiekiamumas (automatinis naujinimas):** 2022 m. spalio mėn.

## <a name="features-included-in-this-release"></a>Funkcijos, įtrauktos į šį leidimą

Tolesnėje lentelėje pateiktos funkcijos, kuri yra šiame leidime. Mes galime atnaujinti šį straipsnį, kad būtų įtrauktos funkcijos, kurios buvo įtrauktos į versiją iš pradžių publikuous šį straipsnį.

| Funkcijos sritis | Funkcija | Daugiau informacijos | Įjungė   |
|---------|------------------|----------------|--------------| 
| B2B | [Įjungti pardavimo sutarties tarp kanalų palaikymą](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-b2b-sales-agreement-contract-based-pricing) | Ši funkcija leidžia verslo įmonių (B2B) pardavėjų organizacijoms naudoti pardavimo sutartis "Commerce Headquarters", kad būtų galima nustatyti sutartis dėl kainų savo pirkėjams. Kai B2B pirkėjų parduotuvės el. komercijos svetainėje, su sutartimi paremta kainodara, sukonfigūruota B2B pirkėjų organizacijai, automatiškai taikoma visam produkto su aptikimo, pirkimo ir tikrinimo būdui. | Funkcijų valdymas<p>*Palaikyti pardavimo sutartį visuose prekybos kanaluose* |
| Customer Service | [Įgalinti klientų aptarnavimą su "Dynamics 365" Klientų aptarnavimo tarnyba](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/chat-dynamics-365-commerce-omnichannel-customer-service) | Pirmos klasės klientų aptarnavimo patirtis yra labai svarbi teikiant vartotojams pritaikytą ir šiandieninę komercijos patirtį. Šiuo metu yra keletas "Commerce TouchPoint" taškų, pvz., faktinės parduotuvės, interneto kanalai ir socialinės kanalai. Vartotojai tikisi, kad visuose šiuose jutikliniuose taškuose bus pritaikyta palaikymo patirtis. Ši funkcija padeda padidinti krepšelio konvertavimą į pardavimą, padidinkite klientų aptarnavimo personalizavimą ir pagerinate klientų aptarnavimą, integruodami su "Dynamics 365" klientų aptarnavimo tarnyba. | Įgalino administratorius / asmenys |
| El. prekyba | Produktų palyginimo el. komercijoje palaikymas | Įgalinti pirkėjų grupes palyginti produktus visame kategorijų diapazone, kad jie patys galėtų priimti teisingą pirkimo sprendimą. Šią funkciją galima naudoti ir "verslas vartotojui" (B2C) ir B2B svetainėse. | Svetainės generatorius | 
| Dovanų kortelės | Mažmeninės prekybos dovanų kortelių lentelių palaikymas, kad būtų galima bendrai naudoti visos įmonės duomenis | "Dynamics Headquarters" palaiko galimybę įgalinti visų įmonių duomenų bendrinimą konkrečiose lentelėse Dynamics architektūroje. Šioje priemonėje nepalaikomi Dynamics 365 Commerce visų įmonių duomenys, skirti mažmeninės prekybos dovanų kortelių lentelėms. Todėl vienoje įmonėje dovanų kortelė dabar gali dubliuoti kitos aplinkos įmonės duomenis. Pakeitimai, atlikti kilmės įmonės dovanų kortelių lentelėje, bus bendrai naudojami dubliuotai įmonės dovanų kortelių lentelei. | Kūrėjai |
| Globalizacija | [Įjungti naujo "Commerce SDK" "Commerce" lokalizavimo priemones](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-commerce-localization-features-new-commerce-sdk) | Nauja funkcija leidžia naudojant priemonių valdymo sistemą arba parametrus įgalinti "Commerce Headquarters" "Commerce Localization" funkcijas. Dabar finansinio integravimo pavyzdžiai įtraukiami į naują "Commerce SDK" ir palaiko nepriklausomą pakuotę. Ši funkcija taip pat leidžia "Store Commerce" programėlę naudoti pagal visuotinės komercijos klientus.<p><p>Šiame leidime yra Komercijos lokalizavimo funkcijos [ir finansinio integravimo pavyzdžiai Austrijai,](../localizations/emea-aut-fi-sample.md) Čekijos [Respublikai, Prancūzijai,](../localizations/emea-cze-fi-sample.md)[...](../localizations/emea-fra-cash-registers.md)[Vokietijai,](../localizations/emea-deu-fi-sample.md) Italijai [,](../localizations/emea-ita-fpi-sample.md) Norvegijai [ir Lenkijai.](../localizations/emea-nor-cash-registers.md)[...](../localizations/emea-pol-fpi-sample.md) | Įgalino administratorius / asmenys |
| Neprisijungęs | [EKA autonominės duomenų bazės glaudinimas](../dev-itpro/implementation-considerations-offline.md#important-offline-features) | Ši nauja funkcija sumažina autonominės duomenų bazės dydžius, įgalindami automatizuoto indekso glaudinimą ne kanalo parduotuvės [valandomis](../dev-itpro/store-hours.md). | Funkcijų valdymas<p>*EKA autonominės duomenų bazės glaudinimas* |
| Našumas | Pašalinkite RTS priklausomybę "redaguoti klientą" scenarijams | Didelis pasiekiamumas ir didelis našumas yra numatytosios pardavimo (EKA) ir el. prekybos kanalų galimybės. Siekiant patenkinti šias lūkesčius, Dynamics 365 Commerce kanalams, redaguojant klientų informaciją, nebereikia pasitikti realiuoju laiku susijusiu ryšius su "Commerce Headquarters". Galimybė redaguoti asinchroninių ir nesinchroninių klientų klientų informaciją asinchroniškai gali padėti sumažinti realiuoju laiku išklydus į "Commerce Headquarters". | Įgalino administratorius / asmenys |

## <a name="feature-state-changes-in-this-release"></a>Šiame leidime yra funkcijų būsenos pakeitimai

Šioje lentelėje pateikiamos priemonės, kurios versijoje 10.0.29 tampa privalomomis arba pagal numatytuosius nustatymus. Visos šios priemonės bus automatiškai įjungtos jūsų sistemai, kai tik bus atnaujinta į 10.0.29 versiją. Privalomų priemonių išjungti negalima, tačiau pagal numatytuosius nustatymus įjungtas funkcijas vis tiek galima išjungti naudojant funkcijų [valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Lentelėje taip pat pateikiamos priemonės, kurios anksčiau buvo viešos peržiūros metu, bet kurios buvo pakeistos į bendrai pasiekiamas versijoje 10.0.29. Šis pakeitimas parodo, kad dabar šias priemones rekomenduojama naudoti gamybos aplinkose. Numatyta, kad šios priemonės išjungiamos, nebent pažymėta kitaip. Todėl, norėdami jas [įgalinti,](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) turite naudoti priemonių valdymą.

| Funkcija | Pavadinimas | Naujos funkcijos būsena |
| --- | --- | --- |
| BrazilRetailLocalizationFeature_BR |(Brazilija) Brazilijai būdinga „Commerce“ funkcija | Įjungta pagal numatytuosius parametrus |
| RetailAdvancedGTETaxAdjustmentFeature | (Indija) Taikyti apskaičiuotą mažmeninės prekybos operacijų GST „Retail POS“ esantiems mažmeninės prekybos išrašams | Įjungta pagal numatytuosius parametrus |
| RetailChronologicalInvoicePostingFeature_IT | (Italija) Įjungti mažmeninės prekybos sąskaitas faktūras, užregistruotas ne chronologine tvarka | Įjungta pagal numatytuosius parametrus |
| RetailDiscountWithoutTaxAdjustingFeature_MX | (Meksika) Nuolaidų koregavimas mažmeninės prekybos CFDI visuotinėje funkcijoje | Įjungta pagal numatytuosius parametrus |
| RetailFiscalIntegrationConfigurationEnhancementFeature | Finansinės integracijos techninio profilio perrašymai | Įjungta pagal numatytuosius parametrus |
| RetailFiscalIntegrationConnectorLocationFeature | Tiesioginė finansų integracija iš EKA registrų | Įjungta pagal numatytuosius parametrus |
| RetailFiscalIntegrationLocalStorageBackupEnableFeature | Finansinės integracijos vietinės saugyklos atsarginė kopija | Įjungta pagal numatytuosius parametrus |
| RetailFiscalIntegrationPostponeFiscalRegistrationFeature | Atidėtas dokumentų registravimas | Įjungta pagal numatytuosius parametrus |
| RetailFiscalIntegrationRegistrationProcessTerminalExceptionFeature | EKA registrų finansinės registracijos būsena | Įjungta pagal numatytuosius parametrus |
| RetailGSTInvoiceAddressTaxCalculationFeature_IN | (Indija) Apskaičiuoti GST pagal el. prekybos užsakymų sąskaitos faktūros adresą | Įjungta pagal numatytuosius parametrus |
| RetailInvoicesDefaultSalesDocumentStatusFeature_PL | (Lenkija) Numatytoji mažmeninės prekybos sąskaitų faktūrų pardavimo dokumento būsena | Įjungta pagal numatytuosius parametrus |
| RetailRecalculateRoundingOfTaxBaseAmountsFeature_MX | (Meksika) Mažmeninės prekybos CFDI visuotinės mokesčių bazės sumų apvalinimo funkcija programoje „Retail“. | Įjungta pagal numatytuosius parametrus |
| RetailSupplementaryInvoiceFeature | Įgalinti papildomas sąskaitas faktūras mažmeninės prekybos parduotuvėse atliktoms atsiskaitymo operacijoms grynaisiais pinigais | Įjungta pagal numatytuosius parametrus |
| RetailInventoryBufferAndInventoryLevelEnableFeature   |  Įgalinti atsargų buferius ir atsargų lygius    |  Įjungta pagal numatytuosius parametrus|
|RetailInboundOutboundInventoryValidationFeature|   Įjungti EKA gaunamų ir siunčiamų atsargų operacijos tikrinimą   |   Įjungta pagal numatytuosius parametrus   |
|  RetailInventoryChannelCalculationConsolidationFeature    |  Patobulinta el. prekybos kanalo atsargų skaičiavimo logika |   Įjungta pagal numatytuosius parametrus   |
|RetailInventoryAdjustmentsInPointOfSaleFeature|    Atsargų koregavimas elektroniniame kasos aparate   |  Įjungta pagal numatytuosius parametrus  |
| RetailMultiplePickupDeliveryModeFeature |  Kelių paėmimo pristatymo būdų palaikymas     |   Privalomas    |
|  RetailProductAvailabilityOptimizationFeature |   Optimizuotas produkto prieinamumo skaičiavimas  |  Privalomas |
|   RetailPricingDataManagerV2Feature   |   Pagerinti „Commerce“ kainodaros mechanizmo našumą |   Privalomas |
|  RetailPricingPreventUnintendedRecalculationFeature   | Apsaugoti nuo nenusilaikyto "Commerce" užsakymų kainų skaičiavimo    |  Privalomas  |
| RetailTeamsIntegration    |   Įjungti „Microsoft Teams“ integravimą| Privalomas   |  
| ConsumerEFDSyncProcessFeature_BR | (Brazilija) NFC–e sinchroninis apdorojimas | Įjungta pagal numatytuosius parametrus |
| RetailFiscalIntegrationInternalAndExternalServicesEnableFeature | Parama vidinėms ir išorinėms jungtims finansinės integracijos sistemoje | Privalomas |
| RetailTaxRegistrationIdEnableFeature_BR | (Brazilija) Ieškoti klientų „Retail POS” pagal mokesčių mokėtojo kodą | Privalomas |
| RetailTaxRegistrationIdEnableFeature_IN | (Indija) Ieškoti klientų „Retail POS” pagal mokesčių mokėtojo kodą | Privalomas |
| RetailTaxRegistrationIdEnableFeature_IT | (Italija) Klientų informacijos valdymas „Retail POS“ | Privalomas |
| RetailTaxRegistrationIdEnableFeature_PL | (Lenkija) Klientų informacijos valdymas „Retail POS“ | Privalomas |
| RetailUpdateReturnOriginalTransactionIdGlobalEnableFeature_IN | (Mažmeninės prekybos GST Indijai) Atnaujinti kredito pažymas su nuorodomis į pirmines sąskaitas faktūras | Privalomas |
| RetailUserDefinedCertificateProfileFeature | Vartotojo apibrėžti mažmeninės prekybos parduotuvių sertifikatų profiliai | Privalomas |
  

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finansų ir operacijų programėlių platformos naujinimai

„Microsoft Dynamics 365 Commerce“ 10.0.29 versijoje yra platformos naujinimų. Norėdami sužinoti daugiau, žr. [finansų ir operacijų programėlių 10.0.29 versijos (2022 m. spalio mėn.)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md) platformos naujinimus. 

### <a name="bug-fixes"></a>Klaidų ištaisymai

Norėdami gauti informacijos apie klaidos pataisas, įtrauktas į visus naujinimus, kurie yra 10.0.29 versijos dalis, prisiregistruokite prie ciklo tarnybų (LCS) [ir peržiūrėkite žinių bazės straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559&dbType=3&qc=ec3e3846199f5d3a27a0c4949e3902ffdbc87560f0cf928c4838b3bdd421633c). 

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
