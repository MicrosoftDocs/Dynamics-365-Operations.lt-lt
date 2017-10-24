--- 
title: "Kurti vartojimo paraišką"
description: "Ši procedūra žingsnis po žingsnio supažindins su paraiškos kūrimo procesu."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07fe007005fcbbac1beecadb14dbd752376a0bd4
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-for-consumption"></a>Kurti vartojimo paraišką

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra žingsnis po žingsnio supažindins su paraiškos kūrimo procesu. Ji parodo skirtingus produktų paieškos įsigijimo kataloge būdus ir kaip įtraukti produktą, kurio nėra kataloge. Prieš pradėdami šią procedūrą, pirkimo strategiją numatytuoju paraiškos tipu turite nustatyti suvartojimą. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis. Procedūrą galima atlikti tik iš vartotojo profilio, kuris nustatytas kaip darbuotojo.  Šiią užduotį paprastai atlieka darbuotojas. Užduotis galėsite atlikti per darbuotojo saugos vaidmenį arba, jei naudojate USMF, galite prisijungti kaip Alicia.


## <a name="create-a-new-requisition"></a>Kurti naują paraišką
1. Pasirinkite Pirkimai ir tiekėjų parinkimas > Pirkimo paraiškos > Mano parengtos pirkimo paraiškos.
2. Spustelėkite Naujas.
3. Lauke „Pavadiniams“ suteikite paraiškai pavadinimą.
4. Lauke „Pageidaujama data“ įveskite datą.
    * Pagal numatytuosius nustatymus, pageidaujama data ir apskaitos data nukopijuojamos į pirkimo paraiškos eilutes. Jas galima keisti eilučių lygmeniu. Pareikalauta data – tai pageidaujama pristatymo data.  
5. Lauke „Apskaitos data“ įveskite datą.
    * Apskaitos data naudojama įrašant apskaitos įrašą didžiojoje knygoje bei tikrinant, ar yra biudžeto lėšų.  
6. Spustelėkite GERAI.
7. Lauke „Priežastis“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pagal nustatytuosius parametrus, jūsų pasirinkta verslo pagrindimo priežastis rodoma pirkimo paraiškos eilutėse, bet galite ją pakeisti eilutės lygmeniu.    
8. Sąraše raskite ir pasirinkite norimą įrašą.
9. Pasirinkti priežastį
10. Informacija lauke įveskite išsamesnį paraiškos pagrindimą

## <a name="add-a-line-to-the-requisition"></a>Įtraukti eilutę į paraišką
1. Spustelėkite Pridėti eilutę.
    * Pridėti eilutes į pirkimo paraišką galima dviem būdais. Jei jau žinote produkto numerį arba jau žinote, kad jums reikalingo produkto kataloge nėra, galite pridėti eilutę tiesiogiai, paspaudę „Įtraukti eilutę“. Kitas būdas yra paspausti „Pridėti produktus“, kur galite naudoti paiešką ir filtravimą, kad rastumėte prekes produktų kataloge.    
2. Spustelėkite eilutę, kurią ką tik sukūrėte.
    * Prašytojas yra darbuotojas, kuris paprašė leisti rengti paraišką.   
    * Pagal numatytuosius nustatymus, paraišką rengiantis asmuo yra to prašęs darbuotojas. Norėdami parengti paraiškos eilutę kito darbuotojo vardu turėsite gauti leidimą. Jei tokius leidimus turite, tada šioje paieškoje bus rodomi kiti darbuotojai.  
3. Lauke Prekės numeris surinkite reikšmę.
    * Prekes, iš kurių galite rinktis, riboja kategorijos prieigos strategija ir perkančio juridinio subjekto įsigijimo katalogas.   
4. Lauke Kiekis įveskite skaičių.

## <a name="add-more-products-to-the-requisition"></a>Įtraukti daugiau produktų į paraišką
1. Spustelėkite „Įtraukti produktus“.
    * Ši parinktis leidžia ieškoti produktų kataloge.    
2. Lauke „Rasti įsigijimo kategorijos mazgą“ įveskite pirmąją jūsų ieškomos kategorijos pavadinimo dalį, tada paspauskite „Įvesti“.
    * Pvz., įveskite „kompiut“.  
3. Naudokite InvokeDefaultButton sparčiuosius klavišus.
4. Naudokite filtrą pasirinktos kategorijos produktų sąrašui filtruoti.
5. Pasirinkite produkto kortelę, kurią norite įtraukti į paraišką.
6. Spustelėkite „Įtraukti į eilutes“.
7. Lauke Kiekis įveskite skaičių.
8. Lauke „Rasti įsigijimo kategorijos mazgą“ įveskite pirmąją jūsų ieškomos kategorijos pavadinimo dalį, tada paspauskite „Įvesti“.
    * Pvz., įveskite „žym“ (žymekliai).  
9. Naudokite InvokeDefaultButton sparčiuosius klavišus.
10. Spustelėkite „Įtraukti į eilutes produktą ne iš sąrašo“, kad pridėtumėte produktą, kurio nėra įsigijimo kataloge.
11. Lauke Produkto pavadinimas įveskite reikšmę.
12. Lauke „Vienetas“ įveskite reikšmę.
13. Spustelėkite Gerai.
14. Lauke „Prekės aprašas“ pridėkite produkto aprašą.
15. Lauke Kiekis įveskite skaičių.
16. Lauke Vieneto kaina įveskite skaičių.
    * Jei žinote konkretaus tiekėjo kainą (kurią pasirenkate tiekėjo sąskaitos lauke), tada galite įvesti šią kainą   
17. Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Kokie tiekėjai bus šiame lauke priklauso nuo pirkimo strategijų ir tiekėjo būsenos esamoje įsigijimo kategorijoje. Tiekėją galite pasirinkti ne tik čia – taip pat galite spustelėti mygtuką „Siūlyti tiekėją“.    
18. Sąrašo pasirinkite tiekėją, kurį norite naudoti.
19. Lauke „Išorinis prekės numeris“ įveskite reikšmę.
    * Tai yra produkto nuorodos numeris, kurį žino tiekėjas. Pvz., tai gali būti prekės numeris tiekėjo produktų kataloge.  
20. Spustelėkite GERAI.

## <a name="distribute-amounts"></a>Paskirstyti sumas
1. Spustelėkite Finansai.
2. Spustelėkite „Paskirstyti sumas“.
    * Šis procesas nurodo, kaip paskirstyti pirmos eilutės išlaidas 2 sąskaitoms. Tą taip pat galima atlikti vėliau, kai paraiška bus peržiūrima.  
3. Spustelėkite „Skaidyti“, kad sukurtumėte naują paskirstymo eilutę.
4. Lauke „DK sąskaita“ pasirinkite pirmą išlaidų centrą, kuris turėtų prisiimti dalį išlaidų.
5. Pasirinkite kitą paskirstymo eilutę.
6. Lauke „DK sąskaita“ nurodykite kitą išlaidų centrą.
7. Spustelėkite „Paskirstyti tolygiai“.
8. Uždarykite puslapį.

## <a name="view-line-details"></a>Peržiūrėti eilutės informaciją
1. Perjunkite dalies Išsami eilučių informacija išplėtimą.

## <a name="submit-the-requisition"></a>Pateikti paraišką
1. Spustelėkite „Darbo eiga“, kad atidarytumėte išplečiamąjį dialogo langą.
2. Spustelėkite Pateikti.
3. Uždarykite puslapį.
4. Lauke „Komentaras“ įveskite pastabą paraiškos tvirtintojui.
5. Spustelėkite Pateikti.
6. Uždarykite puslapį.
7. Atnaujinkite puslapį.


