---
title: Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas
description: Šioje temoje apibūdinama, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, generuojančias elektroninius dokumentus „Excel” ir „Word” formatais, kuriuose yra įdėtųjų vaizdų.
author: NickSelin
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1bafc919d73c9e603935398563bb26e8fb277d3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751063"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas

[!include [banner](../../includes/banner.md)]

Norėdami atlikti šios procedūros veiksmus, pirmiausia atlikite procedūrą „ER: konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu.“ Šia procedūra paaiškinama, kaip kurti elektroninių ataskaitų (ER) konfigūracijas, norint generuoti „Microsoft Excel“ ar „Word“ dokumentą su įdėtaisiais vaizdais. Atlikdami šią procedūrą, kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį. Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Prieš pradėdami, atsisiųskite ir įrašykite žinyno temoje nurodytus failus [Įdėtieji vaizdai ir formos dokumentuose, kurie generuojami naudojant ER](../electronic-reporting-embed-images-shapes.md). Failai: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png ir Cheque template Word.docx.

## <a name="verify-prerequisites"></a>Būtinų sąlygų tikrinimas  
 1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.  
 2. Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros „Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu“ veiksmus.   
 3. Spustelėkite Ataskaitų konfigūracijos.  
 
## <a name="add-a-new-er-model-configuration"></a>Įtraukti naują ER modelio konfigūraciją  
 1. Užuot kūrę naują modelį, galite įkelti ankščiau įrašytą ER modelio konfigūracijos failą (Model for cheques.xml). Šiame faile yra mokėjimo čekių duomenų modelio pavyzdys ir duomenų modelio susiejimas su programos „Dynamics 365 for Operations“ duomenų komponentais.   
 2. Versijų FastTab spustelėkite Keitimas.   
 3. Spustelėkite Įkelti iš XML failo.  
 4. Spustelėkite Naršyti ir pasirinkite Model for cheques.xml.   
 5. Spustelėkite GERAI.  
 6. Įkeltas modelis bus naudojamas kaip duomenų informacijos šaltinis kuriant „Excel“ ir „Word“ dokumentus, kuriuose yra vaizdų.  

## <a name="add-a-new-er-format-configuration"></a>Įtraukite naują ER formato konfigūraciją  
 1. Užuot kūrę naują formatą, galite įkelti ankščiau įrašytą ER formato konfigūracijos failą (Cheques printing format.xml). Šiame faile yra formato maketo, skirto čekių spausdinimui naudojant iš anksto išspausdintą formą, pavyzdys ir šio formato susiejimas su duomenų modeliu „Model for cheques“.   
 2. Spustelėkite Keitimas.  
 3. Spustelėkite Įkelti iš XML failo.  
 4. Spustelėkite Naršyti ir pasirinkite failą Cheques printing format.xml.   
 5. Spustelėkite GERAI.  
 6. Medyje išplėskite „Model for cheques“.  
 7. Medyje pasirinkite „Model for cheques\Cheques printing format“.  
 8. Įkeltas formatas bus naudojamas kuriant „Excel“ ir „Word“ dokumentus, kuriuose yra vaizdų.   

## <a name="configure-er-user-parameters"></a>ER naudotojo parametrų konfigūravimas  
 1. Veiksmų srityje spustelėkite Konfigūracijos.  
 2. Spustelėkite Vartotojo parametrai.  
 3. Lauke Paleisti parametrus pasirinkite Taip.  
  Įjunkite žymę „Paleisti juodraštį“, kad galėtumėte paleisti pasirinkto formato juodraščio versiją, o ne baigtą versiją.  
 4. Spustelėkite GERAI.  

## <a name="configure-cash--bank-management-parameters"></a>Modulio Grynųjų pinigų ir banko valdymas parametrų konfigūravimas  
 1. Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.  
 2. Naudokite spartųjį filtrą, kad filtruotumėte lauką Banko sąskaita reikšme „USMF OPER‟.  
 3. Veiksmų srityje spustelėkite Nustatyti.  
 4. Spustelėkite Tikrinti.  
 5. Išplėskite skyrių Nustatymas.  
 6. Spustelėkite Redaguoti.  
 7. Lauke Įmonės logotipas pasirinkite Taip.  
 8. Spustelėkite Įmonės logotipas.  
 9. Spustelėkite Keisti.  
 10. Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Company logo.png.   
 11. Spustelėkite Įrašyti.  
 12. Uždarykite puslapį.  
 13. Išplėskite skyrių Parašas.  
 14. Lauke Spausdinti pirmą parašą pasirinkite Taip.  
 15. Spustelėkite Keisti.  
 16. Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Signature image.png.   
 17. Išplėskite skyrių Kopijos.  
 18. Lauke Vandenženklis pasirinkite parinktį.  
 19. Lauke Bendrasis eksporto elektroniniu būdu formatas pasirinkite Taip.  
 20. Pasirinkite konfigūraciją „Cheques printing form“.  
 21. Dabar pasirinktas ER formatas naudojamas spausdinant čekius.  
 22. Spustelėkite Pridėti.  
 23. Spustelėkite Naujas.  
 24. Spustelėkite Failas.  
 25. Spustelėkite Naršyti ir pasirinkite anksčiau atsisiųstą failą Signature image 2.png.   
 26. Uždarykite puslapį.  
 27. Uždarykite puslapį.  
 28. Uždarykite puslapį.  
 29. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.  
 30. Lauke Leisti kurti išankstinį pranešimą neaktyviuose banko koduose: pasirinkite Taip.  
 31. Spustelėkite Įrašyti.  
 32. Uždarykite puslapį.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]