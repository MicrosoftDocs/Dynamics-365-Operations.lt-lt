---
title: Vartojimo paraiškos kūrimas
description: Šioje temoje aprašomas vartojimo paraiškos kūrimo procesas.
author: kamaybac
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e36ccd7b1c0b1902e3631379d71e681e533fa3a6103cc59a3ec65731c4e6326f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775608"
---
# <a name="create-a-requisition-for-consumption"></a>Vartojimo paraiškos kūrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašomas vartojimo paraiškos kūrimo procesas. Ji parodo skirtingus produktų paieškos įsigijimo kataloge būdus ir kaip įtraukti produktą, kurio nėra kataloge. Prieš pradėdami šią procedūrą, pirkimo strategiją numatytuoju paraiškos tipu turite nustatyti suvartojimą. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis. Procedūrą galima atlikti tik iš vartotojo profilio, kuris nustatytas kaip darbuotojo. Šią užduotį paprastai atlieka darbuotojas. Užduotis galėsite atlikti per darbuotojo saugos **Darbuotojas** vaidmenį arba, jei naudojate USMF, galite prisijungti kaip **Alicia**.


## <a name="create-a-new-requisition"></a>Kurti naują paraišką
1. Pasirinkite **Naršymo sritis > Moduliai > Įsigijimas ir šaltinio pasirinkimas > Pirkimo paraiškos > Mano paruoštos pirkimo paraiškos**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** suteikite paraiškai pavadinimą.
4. Lauke **Pageidaujama data** įveskite datą. Pagal numatytuosius nustatymus, pageidaujama data ir apskaitos data nukopijuojamos į pirkimo paraiškos eilutes. Jas galima keisti eilučių lygmeniu. Pareikalauta data – tai pageidaujama pristatymo data.  
5. Lauke **Apskaitos data** įveskite datą. Apskaitos data naudojama įrašant apskaitos įrašą didžiojoje knygoje bei tikrinant, ar yra biudžeto lėšų.  
6. Pasirinkite **Gerai**.
7. Lauke **„Priežastis“** pasirinkite parinktį išplečiamajame meniu. Pagal nustatytuosius parametrus, jūsų pasirinkta verslo pagrindimo priežastis rodoma pirkimo paraiškos eilutėse, bet galite ją pakeisti eilutės lygmeniu.  
8. Pasirinkite priežastį.
9. Laukelyje **išsami informacija** įveskite išsamesnį paraiškos pagrindimą.

## <a name="add-a-line-to-the-requisition"></a>Įtraukti eilutę į paraišką
1. Pasirinkite **Pridėti eilutę**. Pridėti eilutes į pirkimo paraišką galima dviem būdais. Jei jau žinote produkto numerį arba jau žinote, kad jums reikalingo produkto kataloge nėra, galite pridėti eilutę tiesiogiai, paspaudę **Pridėti eilutę**. Kitas būdas yra paspausti **Pridėti produktus**, kur galite naudoti paiešką ir filtravimą, kad rastumėte prekes produktų kataloge.    
2. Pasirinkite šabloną, kurį ką tik sukūrėte.
    - Prašytojas yra darbuotojas, kuris paprašė leisti rengti paraišką.   
    - Pagal numatytuosius nustatymus, paraišką rengiantis asmuo yra to prašęs darbuotojas. Norėdami parengti paraiškos eilutę kito darbuotojo vardu turėsite gauti leidimą. Jei tokius leidimus turite, tada šioje paieškoje bus rodomi kiti darbuotojai.  
3. Lauke **Prekės numeris** įveskite vertę. Prekes, iš kurių galite rinktis, riboja kategorijos prieigos strategija ir perkančio juridinio subjekto įsigijimo katalogas.   
4. Lauke **Kiekis** įveskite skaičių.

## <a name="add-more-products-to-the-requisition"></a>Įtraukti daugiau produktų į paraišką
1. Pasirinkite **Įtraukti produktus**. Ši parinktis leidžia ieškoti produktų kataloge.    
2. Lauke **Rasti įsigijimo kategorijos mazgą** įveskite pirmąją jūsų ieškomos kategorijos pavadinimo dalį, tada paspauskite **Įvesti**. Pavyzdžiui, įveskite `comput`.  
3. Naudokite **InvokeDefaultButton** nuorodą.
4. Naudokite **Filtras** pasirinktos kategorijos produktų sąrašui filtruoti.
5. Pasirinkite produkto kortelę, kurią norite įtraukti į paraišką.
6. Pasirinkite **Įtraukti į eilutes**.
7. Lauke **Kiekis** įveskite skaičių.
8. Lauke **Rasti įsigijimo kategorijos mazgą** įveskite pirmąją jūsų ieškomos kategorijos pavadinimo dalį, tada paspauskite **Įvesti**. Pavyzdžiui, įveskite `High` (žymekliai).  
9. Naudokite **InvokeDefaultButton** nuorodą.
10. Spustelėkite **Įtraukti į eilutes produktą ne iš sąrašo**, kad pridėtumėte produktą, kurio nėra įsigijimo kataloge.
11. Lauke **Produkto pavadinimas** įveskite vertę.
12. Lauke **Vienetas** įveskite reikšmę.
13. Pasirinkite **Gerai**.
14. Lauke **Prekės aprašas** pridėkite produkto aprašą.
15. Lauke **Kiekis** įveskite skaičių.
16. Lauke **Vieneto kaina** įveskite skaičių. Jei žinote konkretaus tiekėjo kainą (kurią pasirenkate tiekėjo sąskaitos lauke), tada galite įvesti šią kainą.   
17. Lauke **Tiekėjo sąskaita** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Kokie tiekėjai bus šiame lauke priklauso nuo pirkimo strategijų ir tiekėjo būsenos esamoje įsigijimo kategorijoje. Tiekėją galite pasirinkti ne tik čia – taip pat galite spustelėti mygtuką **Siūlyti tiekėją**.    
18. Sąrašo pasirinkite tiekėją, kurį norite naudoti.
19. Lauke **Išorinis prekės numeris** įveskite reikšmę. Tai yra produkto nuorodos numeris, kurį žino tiekėjas. Pvz., tai gali būti prekės numeris tiekėjo produktų kataloge.  
20. Pasirinkite **Gerai**.

## <a name="distribute-amounts"></a>Paskirstyti sumas
1. Pasirinkite **Finansai**.
2. Pasirinkite **Peržiūrėti paskirstymo sumas**. Šis procesas nurodo, kaip paskirstyti pirmos eilutės išlaidas 2 sąskaitoms. Tą taip pat galima atlikti vėliau, kai paraiška bus peržiūrima.  
3. Spustelėkite **Skaidyti**, kad sukurtumėte naują paskirstymo eilutę.
4. Lauke **DK sąskaita** pasirinkite pirmą išlaidų centrą, kuris turėtų prisiimti dalį išlaidų.
5. Pasirinkite kitą paskirstymo eilutę.
6. Lauke „DK sąskaita“ nurodykite kitą išlaidų centrą.
7. Pasirinkite **Paskirstyti tolygiai**.
8. Uždarykite puslapį.

## <a name="view-line-details"></a>Peržiūrėti eilutės informaciją
1. Perjunkite dalies **Išsami eilučių informacija** išplėtimą.

## <a name="submit-the-requisition"></a>Pateikti paraišką
1. Pasirinkite **Darbo eiga**, kad atidarytumėte išplečiamąjį dialogo langą.
2. Pasirinkite **Pateikti**.
3. Uždarykite puslapį.
4. Įveskite pastabą paraiškos tvirtintojui lauke **Komentaras**.
5. Pasirinkite **Pateikti**.
6. Uždarykite puslapį.
7. Atnaujinkite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]