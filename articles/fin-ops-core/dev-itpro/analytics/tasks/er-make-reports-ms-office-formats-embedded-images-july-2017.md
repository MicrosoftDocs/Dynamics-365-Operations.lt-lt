---
title: Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas
description: Šioje temoje apibūdinama, kaip sukurti elektroninių ataskaitų kūrimo (ER) konfigūracijas, generuojančias elektroninius dokumentus „Excel” ir „Word” formatais, kuriuose yra įdėtųjų vaizdų.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944562"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Ataskaitų generavimo „Office“ formatu su įdėtaisiais vaizdais konfigūracijų kūrimas

[!include [banner](../../includes/banner.md)]

Norėdami atlikti šios procedūros veiksmus, pirmiausia atlikite procedūrą „ER: konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu.“ Šia procedūra paaiškinama, kaip kurti elektroninių ataskaitų (ER) konfigūracijas, norint generuoti „Microsoft Excel“ ar „Word“ dokumentą su įdėtaisiais vaizdais. Atlikdami šią procedūrą, kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Šiuos veiksmus galima atlikti naudojant USMF duomenų rinkinį. Ši procedūra sukurta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Prieš pradėdami, atsisiųskite ir įrašykite šiuos failus: 

| Aprašas                                          | Failo vardas                   |
|------------------------------------------------------|-----------------------------|
| ER duomenų modelio konfigūracija                          | [cheques.xml šablonas](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER formato konfigūracija                              | [Čekių spausdinimas formatas.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Įmonės logotipo vaizdas                                   | [Įmonės logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Parašo vaizdas                                      | [Parašo vaizdas.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternatyvus parašo vaizdas                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| „Microsoft Word“ mokėjimo čekių spausdinimo šablonas  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

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
