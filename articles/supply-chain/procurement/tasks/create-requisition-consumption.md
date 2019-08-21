---
title: Vartojimo paraiškos kūrimas
description: Šioje temoje aprašomas vartojimo paraiškos kūrimo procesas.
author: mkirknel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2948282d8b40f7d34ffbae072a195cf954ab6e2
ms.sourcegitcommit: 81e6eaa2178fda7f7d086ad978f4c891bc4ec10a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/10/2019
ms.locfileid: "1738909"
---
# <a name="create-a-requisition-for-consumption"></a>Vartojimo paraiškos kūrimas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje aprašomas vartojimo paraiškos kūrimo procesas. Ji parodo skirtingus produktų paiekos įsigijimo kataloge būdus ir kaip įtraukti produktą, kurio nėra kataloge. Prieš pradėdami šią procedūrą, pirkimo strategiją numatytuoju paraiškos tipu turite nustatyti suvartojimą. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis. Procedūrą galima atlikti tik iš vartotojo profilio, kuris nustatytas kaip darbuotojo. Šiią užduotį paprastai atlieka darbuotojas. Užduotis galėsite atlikti per darbuotojo saugos **Employee** vaidmenį arba, jei naudojate USMF, galite prisijungti kaip **Alicia**.


## <a name="create-a-new-requisition"></a>Kurti naują paraišką
1. Pasirinkite **Navigation pane > Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**
2. Pasirinkite **Naujas**.
3. Lauke **Name** suteikite paraiškai pavadinimą.
4. Lauke **Requested date** įveskite datą. Pagal numatytuosius nustatymus, pageidaujama data ir apskaitos data nukopijuojamos į pirkimo paraiškos eilutes. Jas galima keisti eilučių lygmeniu. Pareikalauta data – tai pageidaujama pristatymo data.  
5. Lauke **Accounting date** įveskite datą. Apskaitos data naudojama įrašant apskaitos įrašą didžiojoje knygoje bei tikrinant, ar yra biudžeto lėšų.  
6. Pasirinkite **Gerai**.
7. Lauke **„Priežastis“** pasirinkite parinktį išplečiamajame meniu. Pagal nustatytuosius parametrus, jūsų pasirinkta verslo pagrindimo priežastis rodoma pirkimo paraiškos eilutėse, bet galite ją pakeisti eilutės lygmeniu.  
8. Pasirinkti priežastį
9. Laukelyje **details** įveskite išsamesnį paraiškos pagrindimą

## <a name="add-a-line-to-the-requisition"></a>Įtraukti eilutę į paraišką
1. Pasirinkite **„Pridėti eilutę“**. Pridėti eilutes į pirkimo paraišką galima dviem būdais. Jei jau žinote produkto numerį arba jau žinote, kad jums reikalingo produkto kataloge nėra, galite pridėti eilutę tiesiogiai, paspaudę **Add line**. Kitas būdas yra paspausti **Add products**, kur galite naudoti paiešką ir filtravimą, kad rastumėte prekes produktų kataloge.    
2. Pasirinkite šabloną, kurį ką tik sukurėte.
    - Prašytojas yra darbuotojas, kuris paprašė leisti rengti paraišką.   
    - Pagal numatytuosius nustatymus, paraišką rengiantis asmuo yra to prašęs darbuotojas. Norėdami parengti paraiškos eilutę kito darbuotojo vardu turėsite gauti leidimą. Jei tokius leidimus turite, tada šioje paieškoje bus rodomi kiti darbuotojai.  
3. Lauke **Prekės numeris** įveskite vertę. Prekes, iš kurių galite rinktis, riboja kategorijos prieigos strategija ir perkančio juridinio subjekto įsigijimo katalogas.   
4. Lauke **Kiekis** įveskite skaičių.

## <a name="add-more-products-to-the-requisition"></a>Įtraukti daugiau produktų į paraišką
1. Pasirinkite **Add products**. Ši parinktis leidžia ieškoti produktų kataloge.    
2. Lauke **Find procurement category node** įveskite pirmąją jūsų ieškomos kategorijos pavadinimo dalį, tada paspauskite **Enter**. Pavyzdžiui, įveskite `comput`.  
3. Naudokite **„InvokeDefaultButton“** nuorodą.
4. Naudokite **Filter** pasirinktos kategorijos produktų sąrašui filtruoti.
5. Pasirinkite produkto kortelę, kurią norite įtraukti į paraišką.
6. Pasirinkite **Add to lines**.
7. Lauke **Kiekis** įveskite skaičių.
8. Lauke **Find procurement category node** įveskite pirmąją jūsų ieškomos kategorijos pavadinimo dalį, tada paspauskite **Enter**. Pavyzdžiui, įveskite `High` (žymekliai).  
9. Naudokite **„InvokeDefaultButton“** nuorodą.
10. Spustelėkite **Add unlisted product to lines**, kad pridėtumėte produktą, kurio nėra įsigijimo kataloge.
11. Lauke **Produkto gavimo kvitas** įveskite vertę.
12. Lauke **Unit** įveskite reikšmę.
13. Pasirinkite **Gerai**.
14. Lauke **Item description** pridėkite produkto aprašą.
15. Lauke **Kiekis** įveskite skaičių.
16. Lauke **Unit price** įveskite skaičių. Jei žinote konkretaus tiekėjo kainą (kurią pasirenkate tiekėjo sąskaitos lauke), tada galite įvesti šią kainą   
17. Lauke **Vendor account** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Kokie tiekėjai bus šiame lauke priklauso nuo pirkimo strategijų ir tiekėjo būsenos esamoje įsigijimo kategorijoje. Tiekėją galite pasirinkti ne tik čia – taip pat galite spustelėti mygtuką **Suggest vendor**.    
18. Sąrašo pasirinkite tiekėją, kurį norite naudoti.
19. Lauke **External item number** įveskite reikšmę. Tai yra produkto nuorodos numeris, kurį žino tiekėjas. Pvz., tai gali būti prekės numeris tiekėjo produktų kataloge.  
20. Pasirinkite **Gerai**.

## <a name="distribute-amounts"></a>Paskirstyti sumas
1. Pasirinkite **„Finansiniai“**.
2. Pasirinkite **Distribute amounts**. Šis procesas nurodo, kaip paskirstyti pirmos eilutės išlaidas 2 sąskaitoms. Tą taip pat galima atlikti vėliau, kai paraiška bus peržiūrima.  
3. Spustelėkite **Split**, kad sukurtumėte naują paskirstymo eilutę.
4. Lauke **Ledger account** pasirinkite pirmą išlaidų centrą, kuris turėtų prisiimti dalį išlaidų.
5. Pasirinkite kitą paskirstymo eilutę.
6. Lauke „DK sąskaita“ nurodykite kitą išlaidų centrą.
7. Pasirinkite **Distribute equally**.
8. Uždarykite puslapį.

## <a name="view-line-details"></a>Peržiūrėti eilutės informaciją
1. Perjunkite dalies **Line details** išplėtimą.

## <a name="submit-the-requisition"></a>Pateikti paraišką
1. Spustelėkite **Workflow**, kad atidarytumėte išplečiamąjį dialogo langą.
2. Pasirinkite **Pateikti**.
3. Uždarykite puslapį.
4. Įveskite pastabą paraiškos tvirtintojui lauke **Comment**.
5. Pasirinkite **Pateikti**.
6. Uždarykite puslapį.
7. Atnaujinkite puslapį.

