---
title: Importuoti tiekėjų katalogus
description: Šiame straipsnyje aprašomas procesas, kaip importuoti tiekėjo katalogo duomenis.
author: GalynaFedorova
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gfedorova
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 923715893b9f1c4b87d7bbb67e200f8cb8f92e6b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015561"
---
# <a name="import-vendor-catalogs"></a>Importuoti tiekėjų katalogus

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Tiekėjo katalogų importavimas

Naudojant „Dynamics 365 Supply Chain Management“, pirkimo specialistai gali kurti ir tvarkyti katalogus, kuriuos įmonės darbuotojai gali naudoti užsakydami prekes ir paslaugas vidaus naudojimui. Norėdami sukurti įsigijimo katalogą, norimas darbuotojams siūlyti prekes ir paslaugas galite įtraukti importuodami produktų katalogo duomenis arba patys neautomatiškai įtraukdami produktų katalogo duomenis į bendrąjį produktą. 

Galite įkelti tiekėjo naudojantis „Microsoft Dynamics 365“ klientu pateiktus katalogo duomenis.

Tiekėjas produkto duomenis turi pateikti kaip katalogo techninės priežiūros užklausos (CRM) failą XML formatu. CMR faile turi būti pateikiama informacija apie tiekėjo jūsų įmonei tiekiamus produktus.

## <a name="import-vendor-catalog-data"></a>Importuoti tiekėjo katalogo duomenis

Norėdami importuoti tiekėjo katalogo duomenis, turite atlikti toliau nurodytas užduotis.

1. Darbo srityje Duomenų valdymas, kurioje nurodėte savo duomenų išdėstymo taisykles, parenkite projektą. Pasirinkite **Duomenų valdymas**, po to pasirinkite **Nustatyti duomenų projektų vaidmenis**.

2. Nustatykite įsigijimo kategorijų hierarchiją ir priskirkite savo tiekėjus įsigijimo kategorijoms. Jei naudojate prekių kodus, įtraukite juos į įsigijimo kategorijas. Informacijos apie tai, kaip nustatyti įsigijimo kategorijų hierarchiją, ieškokite dalyje [Nustatyti įsigijimo kategorijų hierarchiją](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3. Sukonfigūruokite katalogo importavimo tiekėją. Pasirinkite tiekėją, po to pasirinkite **Įsigijimas** > **Sąranka** > **Sukonfigūruoti katalogo importavimo tiekėją**.

4. Sukonfigūruokite katalogo importavimo darbo eigą. Sukurkite CMR failo šabloną ir pasidalinkite juo su savo tiekėju.

5. Norėdami **sukurti tiekėjo katalogą, pasirinkite** \> **Įsigijimai** \> **ir pasirinkimas** Katalogai Tiekėjai. Iš tiekėjo gauti katalogo techninės priežiūros užklausos (CMR) failai grupuojami šiame kataloge.

6. Nusiųskite CMR failą.

7. Peržiūrėkite, patvirtinkite arba atmeskite tiekėjo katalogo produktus. Produktai automatiškai priskiriami įsigijimo kategorijoms. 

Patvirtinti produktai įtraukiami į bendrąjį produktą ir pateikiami pasirinktiems juridiniams subjektams. Į įsigijimo katalogą galima įtraukti tik patvirtintus produktus.

## <a name="generate-a-catalog-import-file-template"></a>Generuoti katalogo importavimo failo šabloną

Katalogo importavimo failo šablonas yra XSD failas, kurį galite naudoti kurdami CMR failą tiekėjo produktams. Jūs galite naudoti CMR failą, kad sukurtumėte naują katalogą, pakeistumėte esamą katalogą arba modifikuotumėte esamą katalogą.

1. Pasirinkite **Įsigijimas ir šaltinio pasirinkimas** \> **Katalogai** \> **Tiekėjo katalogai** ir dukart spustelėkite katalogą, su kuriuo norite dirbti.

2. Atsisiųskite dabartinio katalogo importavimo šabloną (XSD failas). Grupės **Susijusi informacija** skirtuko **Katalogai** srities **Veiksmų sritis** puslapyje **Katalogo atnaujinimas** spustelėkite **Kurti katalogo šabloną** ir pasirinkite **Įsigijimo kategorija**.

    - Naudodamiesi parinktimi **Įsigijimo kategorija** galite kurti katalogo šabloną, kuriame nurodomos įsigijimų kategorijos, kuriose tiekėjas yra įgaliotas teikti produktus.

3. Dialogo lange **Įrašyti kaip** pasirinkite vietą, kurioje norite saugoti katalogo failų šabloną ir įrašykite failą.

Daugiau informacijos ir pavyzdžių rasite šiame tinklaraščio įraše: [„Dynamics AX“ tiekėjo katalogai](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]