---
title: Įgalinti mokesčių skaičiavimo konfigūracijos pagrindinių duomenų peržvalgą
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir įgalinti mokesčių skaičiavimo pagrindinių duomenų peržvalgos funkciją.
author: kai-cloud
ms.date: 11/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d9c234781e55fbf7f29eec14666c939d5d60e2fb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879415"
---
# <a name="enable-master-data-lookup-for-tax-calculation-configuration"></a>Įgalinti mokesčių skaičiavimo konfigūracijos pagrindinių duomenų peržvalgą 

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti ir įgalinti mokesčių skaičiavimo pagrindinių duomenų peržvalgos funkciją. Išplečiamajame sąraše galima pasirinkti vertes mokesčių skaičiavimo konfigūracijoje **laukams**, pvz., Juridiniam subjektui, **Tiekėjo** sąskaitai, **Prekės** kodui ir **Pristatymo terminas**. Šios vertės yra iš susijusios Microsoft Dynamics 365 finansų aplinkos, naudojant duomenų Microsoft Dataverse šaltinį.

> [!NOTE] 
> Mokesčių skaičiavimo pagrindinių duomenų peržvalgos funkcija yra pasirinktinė funkcija. Jei išjungidami mokesčių tarnybos duomenų šaltinių **Dataverse** palaikymo funkciją reguliavimo konfigūracijos tarnyba (RCS), galite praleisti šiuos veiksmus. Tačiau šiuo atveju mokesčių skaičiavimo konfigūracijoje išplečiamasis sąrašas nebus galimas.

1. Nustatykite Microsoft Power Platform integravimą į Microsoft Dynamics Lifecycle Services (LCS). Daugiau informacijos rasite [„Microsoft Power Platform” integravimas – Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Atlikus šį veiksmą, Microsoft Power Platform aplinkos pavadinimas bus rodomas **Power Platform integravimo** skyriuje.
2. Eikite į [Microsoft Power Platform administravimo centrą](https://admin.powerplatform.microsoft.com/environments) ir pasirinkite aplinkos pavadinimą. Pateikiamas aplinkos URL.
3. Nustatykite "Dynamics 365" finansus ir Dataverse. Daugiau informacijos žr. [Gauti virtualaus objekto sprendimą](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) ir [Autentifikavimas ir autorizacija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
4. Nustatykite šiuos objektus. Daugiau informacijos žr. skyriuje [Įgalinti Microsoft Dataverse virtualius objektus](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCityEntity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity

5. Nustatyti „Regulatory Configuration Service“ (RCS) Atidarykite **Funkcijų valdymo** darbo sritį ir įjunkite šias funkcijas:

    - Elektroninių ataskaitų „Dataverse” duomenų šaltinių palaikymas
    - Mokesčių tarnybos „Dataverse“ duomenų šaltinių palaikymas
    - Globalizacijos funkcijos

6. Prisijunkite prie RCS naudodami nuomotojo administratoriaus paskyrą.
7. Eikite į **Elektroninėmis ataskaitos** > **Prijungtos programos**. 
8. Pasirinkite **Nauja** įrašui pridėti ir įveskite toliau nurodytą lauko informaciją. 

    - Lauke **Pavadinimas** įveskite pavadinimą.
    - Lauke **Tipas** pasirinkite **„Dataverse”**.
    - Lauke **Programa** įveskite savo „Dataverse” URL.
    - Lauke **Nuomotojas** įveskite savo nuomotoją.
    - Lauke **Pasirinktinis URL** įveskite savo „Dataverse” URL ir sujunkite jį su „/api/data/v9.1”.

9. Pasirinkite **Tikrinti ryšį** ir užbaikite ryšio procesą. 

    [![Mygtukas Tikrinti ryšį.](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. Eikite į **Elektroninės ataskaitos** > **Mokesčių konfigūracijos** ir importuokite mokesčių konfigūracijas iš [Mokesčių konfigūracijų](https://go.microsoft.com/fwlink/?linkid=2158352).

    [![Mokesčių konfigūracijų puslapis, Mokesčių duomenų modelio medis.](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. Eikite į **Apmokestinto dokumento modelio susiejimas** arba **„Dataverse” modelio susiejimas**, jeigu naudojate „Microsoft” konfigūraciją ir lauke **Prijungta programa** pasirinkite įrašą, kurį sukūrėte 7 veiksme.
12. Nustatykite **Numatytasis modelių susiejimui** į **Taip**.

    [![Modelio susiejimo puslapis.](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
