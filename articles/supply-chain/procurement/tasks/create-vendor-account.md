---
title: Tiekėjo sąskaitos kūrimas
description: Ši procedūra nurodo, kaip sukurti tiekėjo sąskaitą ir įtraukti adresą bei kontaktinę informaciją.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8cd2bb7b03c0415a5c5656f0e3ffada961973e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4434023"
---
# <a name="create-a-vendor-account"></a>Tiekėjo sąskaitos kūrimas

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip sukurti tiekėjo sąskaitą ir įtraukti adresą bei kontaktinę informaciją. Procedūra nenurodo, kaip užpildyti visus laukus, pirkimo ir finansiniais sumetimais. Jei norite apie šiuos laukus sužinoti daugiau, prašome perskaityti laukų aprašus. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis. Tiekėjų sąskaitas paprastai kuria profesionalūs už pirkimus ar gautinas sumas atsakingi darbuotojai.


## <a name="create-a-vendor-account"></a>Tiekėjo sąskaitos kūrimas
1. Eikite į **Naršymo sritis > Moduliai > Įsigijimas ir išteklių paskirstymas > Tiekėjai > Visi tiekėjai**.
2. Spustelėkite **Naujas**.
3. Lauke **Tiekėjo sąskaita** įveskite vertę.
    - Reikšmė gali būti įvesta automatiškai. Tokiu atveju šį veiksmą galite praleisti.  
    - Galite kurti tiekėjo sąskaitas asmeniui arba organizacijai. Nuo to priklausys, kuriuos laukus bus galima naudoti. Šiame pavyzdyje sukursime organizacijos tiekėjo sąskaitą.   
4. Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę. Jei jūsų tiekėjas jau yra jūsų sistemoje registruota šalis, galite jį pasirinkti išplečiamojo sąrašo lauke, o nauja tiekėjo sąskaita perims jau registruotą adresą ir kontaktinę informaciją.
5. Lauke **Grupė** įveskite arba pasirinkite reikšmę. Tiekėjų grupė skirta sugrupuoti tiekėjams, kuriems bendri bet kurie iš šių parametrų: mokėjimo sąlygos, sudengimo laikotarpis, atsargų registravimo DK sąskaitos – įskaitant PVM grupę, numatytosios DK sąskaitos, produktų filtravimo kodai arba tiekimo prognozės konfigūracija.
6. Lauke **Darbuotojų skaičius** įveskite skaičių.
7. Lauke **Organizacijos numeris** įveskite reikšmę.

## <a name="add-an-address"></a>Įtraukti adresą
1. Išplėskite skyrių **Adresai**.
2. Spustelėkite **Pridėti**.
3. Lauke **Tikslas** įveskite arba pasirinkite reikšmę. Galite pasirinkti vieną arba kelis tikslus. Jie naudojami norint pasirinkti tinkamą konkretaus tikslo adresą. Pavyzdžiui, jei tikslas yra „Sąskaita faktūra“, tas adresas bus naudojamas siunčiant sąskaitas faktūras.
4. Lauke **Pavadinimas arba aprašas** įveskite reikšmę.
5. Lauke **Šalis / regionas** įveskite arba pasirinkite reikšmę. Įveskite adreso informaciją. Nuo jūsų pasirinktos šalies / regiono priklausys jums rodomi laukai, atitinkantys šalies / regiono adreso formatą. 
6. Spustelėkite **Gerai**.

## <a name="add-contact-information"></a>Įtraukti kontaktinę informaciją
1. Išplėskite skyrių **Kontaktinė informacija**.
2. Spustelėkite **Pridėti**.
3. Lauke **Aprašo laukas** surinkite reikšmę.
4. Lauke **Tipas** pasirinkite parinktį.
5. Lauke **Kontaktinis numeris / adresas** įveskite reikšmę. Jei tai yra pirminis kontaktas, galite pažymėkite žymės langelį Pirminis.  
6. Spustelėkite **Įrašyti**.
7. Uždarykite puslapį.
8. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]