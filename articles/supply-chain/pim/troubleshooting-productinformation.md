---
title: Produkto informacijos trikties šalinimas
description: Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto informacija.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a05e9957363ef6a659e25ceba84a168507cd641a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841532"
---
# <a name="troubleshoot-product-information"></a>Produkto informacijos trikties šalinimas

Šioje temoje aprašoma, kaip ištaisyti bendras klaidas, su kuriomis galite dirbdami su produkto informacija.

## <a name="i-cant-delete-a-released-product"></a>Negaliu panaikinti išleisto produkto.

### <a name="issue-description"></a>Problemos aprašas

Galite panaikinti išleistą produktą ir visus jo variantus tik, jei išleistas produktas neturi jokių susijusių perlaidų.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Atlikite šiuos žingsnius, kad išleistumėte produktą ar pagrindinį produktą.

1. Užverkite visas perlaidas prekei.
1. Sumažinkite inventorių iki 0 (nulio).
1. Uždarykite inventorių.
1. Panaikinkite visus produkto variantus pagrindiniam produktui, kurį norite panaikinti.

## <a name="can-i-change-the-item-number-of-a-released-product"></a>Ar galiu keisti prekės skaičių išleistam gaminiui?

Daugeliu atvejų negalite redaguoti prekės skaičių išleistiems produktams, nes dėl tokio pokyčio duomenys taps užkrėsti. Galite redaguoti prekės skaičių tik, jei privalote ištaisyti užkrėstus duomenis, kurie kilo dėl anksčiau pervardyto pirminio išleisto produkto rakto, kaip paminėta sąraše [pašalintos ar negaliojančios funkcijos „Finance and Operations“ 10.0.0 su platformos naujinimu 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).

Jei norite galėti redaguoti prekės skaičius išleistiems produktams, [balsuokite už šią idėją idėjų portale](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a>Nustatytasis nuleidimo principas iš produkto nėra įvedamas į komplektavimo specifikacijos eilutę.

### <a name="issue-description"></a>Problemos aprašas

Jums įtraukus prekę į važtaraščio (KS) eilutę, sistema nenaudoti nustatytojo nuleidimo principo informacijos, kuri yra nustatyta prekei. Kitaip tariant, nuleidimo principas iš prekės nepasirodo **KS eilutės** puslapyje.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Jei nurodote nuleidimo principą KS eilutėje, jis bus taikomas tai KS eilutei. Nepaisant to, jei nuleidimo principas yra tuščias arba jis nėra nustatytas KS eilutėje, nuleidimo principas nustatytas prekėje bus vis tiek taikomas tai KS eilute, net jei jis nerodomas KS eilutėje.

Nustatytoji logika kitoms funkcijoms „Microsoft Dynamics 365 Supply Chain Management“ dažniausiai neveikia tokiu būdu. Nepaisant to, esamas elgesys negali būti pakeistas. Kitu atveju, kai kurie esantys tinkinimai pagrįsti juo gali sulūžti.

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a>Sistema leidžia man įrašyti dublikuotus brūkšninius kodus kitoms prekėms ar tai pačiai prekei su kitokiais matmenimis.

Sistema šiuo metu neįpareigoja rengti unikalių brūkšninių kodų ir šio apribojimo priedas sulaužytų keitimą. Dėl to „Microsoft“ turi įrodymų, kad kai kurie esančių klientų įdiegimai būtų šiuo keitimu pažeisti. Nepaisant to, atsižvelgsime į platesnį kūrimo pokytį siekiant įjungti šią funkciją ateityje.

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a>Gaunu tolesnį klaidos pranešimą kai redaguotu prekės įrašo šablonus: „Sandėlio vieta negali būti sukurta dėl to, kad prekė nelaikoma. Norėdami laikyti prekes, laikomo produkto parinktis susietos prekės modelio grupėje turi būti pasirinkta.“

### <a name="issue-description"></a>Problemos aprašas

Jei ši problema atsitinka jums reikia atlikti šiuos žingsnius, kad bandytumėte sukurti šabloną nelaikomai prekei.

1. Atverkite išleistą produktą, kuri nėra laikoma.
1. Veiksmų juostoje **Parinktys** skyriuje rinkitės **Įrašo informacija**.
1. Teksto laukelyje **Įrašo informacija** rinkitės **Įmonės sąskaitų šablonas**.

Tokiu atveju, gausite tolesnį klaidos pranešimą:

> Sandėlio vietos sukurti nepavyko dėl to, kad prekė nelaikoma. Norėdami laikyti prekes, laikomo produkto parinktis susietos prekės modelio grupėje turi būti pasirinkta.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Produkto šablonų sukūrimo procesui reikia papildomo produktu būdingos logikos. Dėl to, negalite naudoti bendro **Bendrovės sąskaitų šablono** mygtuko šiuo tikslu. Vietoje to, vadovaukitės šiais žingsniais.

1. Atverkite išleistą produktą.
1. Veiksmų juostoje skirtuke **Produktas** grupėje **Naujas** pasirinkite **Šablonas \> Kurti bendrintą šabloną**.

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a>Numatytasis pagalbos tekstas yra įtraukiamas į produkto atributus ir neįvedamas į išleistą produktą.

Aprašymas ir pagalbos tekstas yra įtraukiamas į produkto atributus nėra matomi ar įvedami pagal nutylėjimą išleistuose produktuose. Toks veikimo būdas yra numatytas.

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a>Numatytasis kiekis, kuris yra įvedamas skiriasi registruojant iš KS ir jo registravimo iš KS versijos metu.

### <a name="issue-description"></a>Problemos aprašas

Pagal nutylėjimą, jums įtraukus elementą į KS, kiekis nustatomas į 1 vietoje kiekio, kuris nustatytas **Min. užsakymo kiekio** laukelyje **Numatytieji užsakymo nustatymai** puslapyje pasirinktiems produktams. Nepaisant to, jums įtraukiant prekę iš KS versijos ir pasirinkus prekę ir variantą, kiekis įvestas pagal nutylėjimą atsižvelgia į minimalų kiekį, nustatytą numatytuose užsakymo nustatymuose konkretiems matmenims.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Tikimasi tokio elgesio. Nepaisant to, žinoma problema yra ta, kad logika skiriasi KS ir KS versijose. Nepaisant to, šis elgesys nepasikeis, nes keitimas gali veikti daug skirtingų kliento scenarijų.

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a>Išleisto produkto išsamioje informacijoje, negaliu keisti pridėtų paveikslėlių, kurie buvo įkelti iš produkto dokumento priedų duomenų objekto.

### <a name="issue-description"></a>Problemos aprašas

Ši problema gali atsitikti, kai pridedate paveikslėlį prie prekės naudodami *Produkto dokumento priedų* duomenų objektą. Tokiu atveju, prekės paveikslėlis rodomas prekei. Nepaisant to, jei pasirenkate **Keisti paveikslėlį**, įkeltų paveikslėlių sąraše nerodoma nieko. Taip pat, nerodoma jokių priedų prekei.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Objektas *EcoResProductDocumentAttachmentEntity* importuoja (*Produkto dokumento priedus*) dokumento priedus skirtus *produktams* , o ne *išleistiems produktams*. (Išleisti produktai žinomi ir kaip *prekės*.) Norėdami peržiūrėti priedus prekei **Išleisto produkto išsami informacija** puslapyje, privalote naudoti *EcoResReleasedProductDocumentAttachmentEntity* objektą (*Išleisto produkto dokumento priedai*) vietoje to.

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a>„Microsoft Flow“ jungtis rodo tolesnį klaidos pranešimą: „Naujinimas neleidžiamas laukeliui 'Produkto numeris'.“

### <a name="issue-description"></a>Problemos aprašas

Ši problema atsitinka kai bandote naujinti **Produkto skaičių** laukelį naudodami *Išleisti produktai* objektą V2 ir „Microsoft Flow“.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Tikimasi tokio elgesio. Galimybė redaguoti produkto skaičių išleistam produktui buvo panaikinta „Dynamics 365 Finance and Operations“ 10.0.0 su platformos naujiniu 24 siekiant apsisaugoti nuo duomenų sugadinimo. Atskirais atvejais, kai turite pataisyti sugadintus duomenis, kurie kilo dėl ankstesnio vardo pakeitimo pagrindinio rakto išleidimo produkto metu, galite prašyti „Microsoft Support“ laikinai panaikinti tokį apribojimą.

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a>Negaliu išleisti produkto varianto kitu juridiniu subjektu.

### <a name="issue-description"></a>Problemos aprašas

Jei bandote išleisti pagrindinį produktą be variantų, tuomet sukurkite variantus kiekviename juridiniame subjekte (įmonėje), kaip būtina, jūs negalėsite išleisti variantų naudodami variantų siūlymus. Taip pat negalėsite rankiniu būdu kurti variantų.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Toks veikimo būdas yra numatytas. Pagrindinio produkto ryšiai ir matmenys, kuriuos pagrindinis produktas gali paimti laikomi bendrintu lygiu. Dėl to, negalite kurti prieinamų matmenų bendrintam produktui konkrečiame juridiniame subjekte, kuriame tie matmenys išleisti ir tuomet kopijuoti proceso visuose juridiniuose subjektuose, kuriuose būtini matmenys. Vietoj to, turite keisti išleidimo procesą, kad jis prisiderintų prie nustatyto proceso.

Čia yra produktų išleidimo procesas.

1. Sukurkite bendrintą pagrindinį produktą ir matmenis, kuriuos galima išleisti į savo juridinius subjektus.
1. Išleiskite produktus į juridinius subjektus pagal naudojamo varianto siūlymus arba rankiniu būdu įtraukdami išleidžiamus derinius.

Kitu būdu, galite tiesiogiai kurti išleistą produktą.

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a>Išleidžiant variantą kitoje bendrovėje, gaunu šį klaidos pranešimą: „Produkto variantas su nurodytais matmenimis jau buvo sukurtas“.

### <a name="issue-description"></a>Problemos aprašas

Jei produkto variantas jau buvo išleistas bendrovėje A ir bandote jį išleisti į bendrovę B naudodami **Naują** mygtukas puslapyje **Išleisti produkto variantai**, gausite tolesnį klaidos pranešimą:

> Produkto variantas su nurodytomis dimensijomis jau sukurtas.

### <a name="issue-resolution"></a>Problemos paaiškinimas

Mygtukas **Naujas** puslapyje **Išleisto produkto variantai** sukuria variantą ir išleidžia jį į bendrovės kontekstą. Jei variantas jau buvo sukurtas, negalite naudoti **Naujas** mygtuko, kad išleistumėte jį į kitą bendrovę.

Norėdami ištaisyti šią problemą, atverkite **Pagrindinio produkto** puslapį ir rinkitės **Išleisti produktą** norėdami išleisti esantį variantą norimoje bendrovėje.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]