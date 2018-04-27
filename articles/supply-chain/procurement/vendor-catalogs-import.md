---
title: "Importuoti tiekėjų katalogus"
description: "Šioje temoje aprašomas tiekėjo katalogo duomenų importavimo procesas."
author: mkirknel
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: 
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: a56e6ea0a8470f205b1c74379c887c0cac85a6b4
ms.openlocfilehash: c290bcd4787144fb4dd4232c06d2fb9e1e67ca3e
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="import-vendor-catalogs"></a>Importuoti tiekėjų katalogus
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Tiekėjų katalogų importavimas

Naudojant „Microsoft Dynamics 365 for Finance and Operations“ pirkimo specialistai gali kurti ir tvarkyti katalogus, kuriuos įmonės darbuotojai gali naudoti užsakydami prekes ir paslaugas vidaus naudojimui. Norėdami sukurti įsigijimo katalogą, norimas darbuotojams siūlyti prekes ir paslaugas galite įtraukti importuodami produktų katalogo duomenis arba patys neautomatiškai įtraukdami produktų katalogo duomenis į bendrąjį produktą. 

Galite įkelti tiekėjo naudojantis „Microsoft Dynamics 365“ klientu pateiktus katalogo duomenis.

Tiekėjas produkto duomenis turi pateikti kaip katalogo techninės priežiūros užklausos (CRM) failą XML formatu. CMR faile turi būti pateikiama informacija apie tiekėjo jūsų įmonei tiekiamus produktus.

## <a name="import-vendor-catalog-data"></a>Importuoti tiekėjo katalogo duomenis

Norėdami importuoti tiekėjo katalogo duomenis, turite atlikti toliau nurodytas užduotis.

1.  Darbo srityje Duomenų valdymas, kurioje nurodėte savo duomenų išdėstymo taisykles, parenkite projektą. Pasirinkite **Duomenų valdymas**, po to pasirinkite **Nustatyti duomenų projektų vaidmenis**. 

2.  Nustatykite įsigijimo kategorijų hierarchiją ir priskirkite savo tiekėjus įsigijimo kategorijoms. Jei naudojate prekių kodus, įtraukite juos į įsigijimo kategorijas. Informacijos apie tai, kaip nustatyti įsigijimo kategorijų hierarchiją, ieškokite dalyje [Nustatyti įsigijimo kategorijų hierarchiją](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3.  Sukonfigūruokite katalogo importavimo tiekėją. Pasirinkite tiekėją, po to pasirinkite **Įsigijimas** > **Sąranka** > **Sukonfigūruoti katalogo importavimo tiekėją**.

4.  Sukonfigūruokite katalogo importavimo darbo eigą. Sukurkite CMR failo šabloną ir pasidalinkite juo su savo tiekėju.

5.  Norėdami sukurti tiekėjo katalogą, pasirinkite **Įsigijimas ir šaltinio pasirinkimas** \> **Bendra** \> **Katalogai** \> **Tiekėjo katalogai**. Iš tiekėjo gauti katalogo techninės priežiūros užklausos (CMR) failai grupuojami šiame kataloge. 

6.  Nusiųskite CMR failą.

7.  Peržiūrėkite, patvirtinkite arba atmeskite tiekėjo katalogo produktus. Produktai automatiškai priskiriami „Dynamics 365 for Finance and Operations“ įsigijimo kategorijoms. 
    
Patvirtinti produktai įtraukiami į bendrąjį produktą ir pateikiami pasirinktiems juridiniams subjektams. Į įsigijimo katalogą glima įtraukti tik patvirtintus produktus.

## <a name="generate-a-catalog-import-file-template"></a>Generuoti katalogo importavimo failo šabloną

Katalogo importavimo failo šablonas yra pramoninio standarto XSD failas, kurį galite naudoti kurdami CMR failą tiekėjo produktams. Jūs galite naudoti CMR failą, kad sukurtumėte naują katalogą, pakeistumėte esamą katalogą arba modifikuotumėte esamą katalogą.

1.  Pasirinkite **Įsigijimas ir šaltinio pasirinkimas** \> **Katalogai** \> **Tiekėjo katalogai** ir dukart spustelėkite katalogą, su kuriuo norite dirbti.

2.  Atsisiųskite dabartinio katalogo importavimo šabloną (XSD failas). Grupės **Susijusi informacija** skirtuko **Katalogai** srities **Veiksmų sritis** puslapyje **Katalogo atnaujinimas** spustelėkite **Kurti katalogo šabloną** ir pasirinkite **Įsigijimo kategorija**.

    -   Naudodamiesi parinktimi **Įsigijimo kategorija** galite kurti katalogo šabloną, kuriame nurodomos įsigijimų kategorijos, kuriose tiekėjas yra įgaliotas teikti produktus.

3. Dialogo lange **Įrašyti kaip** pasirinkite vietą, kurioje norite saugoti katalogo failų šabloną ir įrašykite failą.

Daugiau informacijos ir pavyzdžių rasite šiame tinklaraščio įraše: [„Dynamics AX“ tiekėjo katalogai](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).

