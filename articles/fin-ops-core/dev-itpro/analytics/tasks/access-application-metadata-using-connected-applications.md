---
title: Prieiga prie programos metaduomenų naudojant prijungtas programas
description: Šioje temoje pateikti veiksmai paaiškina, kaip „Regulatory configuration service“ vartotojas gali kurti naują elektroninės ataskaitos modelio susiejimą naudodamas metaduomenis.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457d5760fb704b7a93ce16c081b7c5e6d0ff19c1
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093335"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Prieiga prie programos metaduomenų naudojant prijungtas programas

[!include [banner](../../includes/banner.md)]

Toliau nurodyti veiksmai paaiškina, kaip „Regulatory configuration service“ (RCS) vartotojas, turintis sistemos administratoriaus arba elektroninės ataskaitos kūrėjo vaidmenį, gali kurti naują elektroninės ataskaitos (ER) modelio susiejimą naudodamas „Finance and Operations“ metaduomenis. Programos metaduomenys bus pasiekiami tinkle naudojant programą, prijungtą prie RCS. Bus sukonfigūruotas ER modelio susiejimo pavyzdys, siekiant pasiekti užsienio prekybos operacijas. Norint atlikti šiuos veiksmus, pirmiausia RCS reikia atlikti veiksmus, nurodytus temoje [Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais](er-configuration-provider-mark-it-active-2016-11.md). Jei neatlikote veiksmų, nurodytų temoje [Prieiga prie programos metaduomenų naudojant ER konfigūraciją](access-application-metadata-er-configuration.md), eikite į [Elektroninių ataskaitų pavyzdžių puslapis](https://go.microsoft.com/fwlink/?linkid=862266), atsisiųskite ir įrašykite šias ER konfigūracijas: Užsienio prekybos metaduomenys.xml; Užsienio prekybos modelis.xml; Užsienio prekybos susiejimas.xml, tada atlikite procedūros veiksmus.

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