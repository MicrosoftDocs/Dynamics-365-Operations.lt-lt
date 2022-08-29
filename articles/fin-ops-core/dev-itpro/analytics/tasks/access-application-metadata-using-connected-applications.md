---
title: Prieiga prie programos metaduomenų naudojant prijungtas programas
description: Šiame straipsnyje atlikti veiksmai paaiškina, kaip reguliavimo konfigūracijos tarnybos vartotojas, naudodamas metaduomenis, gali sukurti naują elektroninio ataskaitų modelio konvertavimą.
author: kfend
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 1a935b96e247978fc2b2f9449d403c92bff35f17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267879"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Prieiga prie programos metaduomenų naudojant prijungtas programas

[!include [banner](../../includes/banner.md)]

Toliau paaiškinama, kaip reguliavimo konfigūracijos tarnybos (RCS) vartotojas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmenyje gali sukurti naują elektroninių ataskaitų (ER) modelio konvertavimą, naudodamas finansų ir operacijų metaduomenis. Programos metaduomenys bus pasiekiami tinkle naudojant programą, prijungtą prie RCS. Bus sukonfigūruotas ER modelio susiejimo pavyzdys, siekiant pasiekti užsienio prekybos operacijas. Norėdami atlikti šiuos veiksmus, RCS pirmiausia turite atlikti straipsnio veiksmus, [sukurkite konfigūracijos teikėjus ir pažymėkite juos kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md). Jei neatibaigėte šiame straipsnyje nurodytų veiksmų, [naudodami ER](access-application-metadata-er-configuration.md) konfigūraciją išeikite iš programos metaduomenų, [parsisiuntkite](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) elektroninių ataskaitų pavyzdžius ir įrašykite toliau nurodytas ER konfigūracijas: Užsienio prekybos metaduomenys.xml; Užsienio prekybos modelis.xml; Užsienio prekybos susiejimas.xml, tada atlikite procedūros veiksmus.

## <a name="prerequisites"></a>Būtinieji komponentai
1. Eikite į **Visos darbo sritys** > **Elektroninės ataskaitos**. 
2. Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md) veiksmus. 

## <a name="get-required-er-configurations"></a>Reikiamų ER konfigūracijų gavimas
1. Spustelėkite **Ataskaitų konfigūracijos**. 
2. Jei jau atlikote [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](access-application-metadata-er-configuration.md) procedūros veiksmus, jūs jau turite visas reikiamas ER konfigūracijas (užsienio prekybos metaduomenų, modelio ir susiejimo konfigūracijas) dabartiniame RCS egzemplioriuje. Galite praleisti visus kitus šios antrinės užduoties veiksmus. 
3. Spustelėkite **Keitimas**. 
4. Spustelėkite **Įkelti iš XML failo**. 
5. Spustelėkite **Naršyti** ir pasirinkite failą **Užsienio prekybos metaduomenys.xml**. 
6. Spustelėkite **Gerai**. 
7. Spustelėkite **Keitimas**. 
8. Spustelėkite **Įkelti iš XML failo**. 
9. Spustelėkite **Naršyti** ir pasirinkite failą **Užsienio prekybos modelis.xml**. 
10. Spustelėkite **Gerai**. 
11. Spustelėkite **Keitimas**. 
12. Spustelėkite **Įkelti iš XML failo**. 
13. Spustelėkite **Naršyti** ir pasirinkite failą **Užsienio prekybos susiejimas.xml**. 
14. Spustelėkite **Gerai**. 

## <a name="register-a-connected-application"></a>Prijungtos programos užregistravimas
1. Uždarykite puslapį. 
2. Uždarykite puslapį. 
3. Eikite į **Visos darbo sritys** > **Elektroninės ataskaitos**. 
4. Spustelėkite **Prijungtos programos**. 
5. Įsitikinkite, kad sukonfigūruota programa yra „Azure“ ir pasiekiama esamam RCS vartotojui. Be to, esamas RCS vartotojas turi turėti prieigą prie pasirinktos programos ir turi būti užregistruotas kaip šios programos vartotojas, kuriam priskirtas vaidmuo suteikia teises pasiekti programos metaduomenis. 
6. Spustelėkite **Naujas**. 
7. Lauke **Pavadinimas** įveskite MyConnectedApp. 
8. Lauke **Programa** įveskite https:// mycompany.operations.dynamics.com. 
9. Lauke **Nuomotojas** įveskite mycompany.onmicrosoft.com. 
10. Spustelėkite **Įrašyti**. 
11. Kai tikrinate ryšį su sukonfigūruota programa, puslapyje **Prisijungti prie nuotolinės programos** spustelėkite saitą **Spustelėkite čia, kad prisijungtumėte prie pasirinktos nuotolinės programos**. 
12. Spustelėkite **Tikrinti ryšį**. 
13. Spustelėkite **Uždaryti**. 
14. Kai ryšio patikra atliekama sėkmingai, esamame tinklelyje atnaujinama sukonfigūruotos programos versijos ir nuomotojo informacija. 

## <a name="review-existing-model-mapping-configuration"></a>Esamo modelio susiejimo konfigūracijos peržiūra
1. Uždarykite puslapį. 
2. Spustelėkite **Ataskaitų konfigūracijos**. 
3. Medyje išplėskite **Užsienio prekybos modelis**. 
4. Medyje pasirinkite **Užsienio prekybos modelis\Užsienio prekybos susiejimas**. 
5. Išplėskite sekciją **Būtinieji komponentai**. 

    > [!NOTE]
    > Šiuo metu šis susiejimas nurodo metaduomenų konfigūraciją. Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys. 

6. Spustelėkite **Konstruktorius**. 
7. Spustelėkite **Konstruktorius**. 
8. Medyje pasirinkite **Dynamics 365 for Operations\Lentelės įrašai**. 
9. Spustelėkite **Įtraukti šakninį elementą**. 
10. Lauke **Lentelė** įveskite arba pasirinkite reikšmę. 

    > [!NOTE]
    > Šiuo metu šis susiejimas nurodo metaduomenų konfigūraciją. Kuriant šį modelio susiejimą bus siūlomi šios konfigūracijos programos metaduomenys. 

11. Spustelėkite **Atšaukti**. 
12. Uždarykite puslapį. 
13. Uždarykite puslapį. 

## <a name="assign-connected-application-to-model-mapping"></a>Prijungtos programos priskyrimas modelio susiejimui 
1. Spustelėkite **Redaguoti**. 
2. Pasirinkite programą **MyConnectedApp**. 

    > [!NOTE]
    > Šiuo metu šis susiejimas nurodo pasirinktos prijungtos programos metaduomenis. Kai tas pats susiejimas tuo pačiu metu nurodo metaduomenų konfigūraciją ir prijungtą programą, bus naudojami prijungtos programos metaduomenys. 

3. Spustelėkite **Konstruktorius**. 
4. Spustelėkite **Konstruktorius**. 
5. Medyje pasirinkite **Dynamics 365 for Operations\Lentelės įrašai**. 
6. Spustelėkite **Įtraukti šakninį elementą**. 
7. Lauke **Lentelė** įveskite arba pasirinkite reikšmę. 

    > [!NOTE]
    > Dabar siūlomos daugiau nei dvi programos lentelės, nes šis susiejimas naudoja visus prijungtos programos, kuri buvo priskirta, metaduomenis. 

8. Spustelėkite **Atšaukti**. 
9. Spustelėkite **Tikrinti**. 

    > [!NOTE]
    > Sėkmingai susiejome duomenų modelio elementus su duomenų šaltinių elementais, kurie aprašomi naudojant prijungtos programos, priskirtos šiam susiejimui, metaduomenis. 

10. Uždarykite puslapį. 
11. Uždarykite puslapį. 

Jei reikia įvertinti šio modelio susiejimą naudojant skirtingos programos versijos metaduomenis, užregistruokite kitą prijungtą programą, priskirkite ją šiam modelio susiejimui ir patikrinkite ją naudodami naujus metaduomenis.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

