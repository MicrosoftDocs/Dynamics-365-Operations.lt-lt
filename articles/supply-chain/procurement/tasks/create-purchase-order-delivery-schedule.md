---
title: Pirkimo užsakymo su pristatymo grafiku kūrimas
description: Šioje temoje aiškinama, kaip kurti pirkimo užsakymo pristatymo grafiką.
author: kamaybac
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchDeliverySchedule, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c965d686f7d8ee426d7ab09d107bfd2782c9fe40feaf8b9a6b5eca1f61cf7198
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725727"
---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a>Pirkimo užsakymo su pristatymo grafiku kūrimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip kurti pirkimo užsakymo pristatymo grafiką. Pristatymo grafikas naudojamas, kai užsakymo arba žurnalo kiekį pageidaujama pristatyti keliomis siuntomis. Šiame vedlyje pateikiamą pavyzdį galima naudoti demonstracinių duomenų įmonėje USMF. Paprastai šią procedūrą atlieka pirkimo agentas.

## <a name="create-a-delivery-schedule"></a>Pristatymo grafiko kūrimas
1. Naršymo srityje eikite į **„Moduliai“ > „Įsigijimas ir šaltiniai“ > „Pirkimo užsakymai“ > „Visi pirkimo užsakymai“**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **„Tiekėjo paskyra“** įveskite „`US-101`“.
4. Pasirinkite **Gerai**.
5. Lauke **„Prekės numeris“** įveskite „`M0001`“.
6. Lauke **„Kiekis“** įveskite „`10`“.
7. Pasirinkite **„Pirkimo užsakymo eilutė“**.
8. Pasirinkite **„Pristatymo grafikas“**.
- Puslapyje **„Pristatymo grafikas“** galima nurodyti siuntų, kurių visas užsakymo eilutės kiekis bus pristatytas iš tiekėjo, skaičių.  
- Pagal numatytąsias nuostatas sistema visą pradinės pirkimo eilutės kiekį ir kitą pristatymo informaciją kopijuoja į pirmąją pristatymo grafiko eilutę. Šiame pavyzdyje sukursime dviejų siuntų grafiką, antrosios siuntos datą paslinkdami per savaitę nuo pirmosios.  
9. Lauke **Kiekis** pakeiskite kiekį į `4`.
10. Pasirinkite **Naujas**.
11. Lauke **Kiekis** įveskite `6` kaip likusį kiekį.
- Lauke Pristatymo data pasirinkite datą, kuri yra viena savaite vėliau nei pirmosios pristatymo eilutės data.  
- Sekti visą kiekį, paskirstytą pristatymo grafiko eilutėms, galite pažvelgę į laukus **Iš viso** ir **Liko**. Kai likęs kiekis yra nulis, grafikui paskirstytas visas pradinės eilutės kiekis.  
12. Išplėskite skyrių **Išlaidų konvertavimas**.
- Ši parinktis suteikia galimybę kontroliuoti, kaip norite išlaidas paskirstyti pristatymo grafiko eilutėse. Jei pasirenkate **Kopijuoti bendras sumas**, pradinės užsakymo eilutės išlaidų suma kopijuojama į kiekvieną pristatymo eilutę. Parinktis **Paskirstyti į pristatymo eilutes** pradinės eilutės išlaidas padalija pagal kiekį kiekvienoje pristatymo eilutėje.  
13. Suskleiskite sekciją **Išlaidų konvertavimas**.
14. Pasirinkite **Gerai**.
- Pristatymo grafikas dabar yra pritaikytas užsakymui.  
- Pradinė užsakymo eilutė, dabar vadinama komercine eilute, konvertuota į užsakymo eilutę, kurioje yra keli pristatymai. Ji pažymėta atskira piktograma ir veikia kaip pristatymo eilučių antraštė.  
15. Pasirinkite antrąją užsakymo eilutę, kuri yra pirmoji iš dviejų pristatymo eilučių.
- Dvi naujosios eilutės, vadinamos pristatymo eilutėmis, sudaro vieną pristatymo grafiką. Užsakymas bus vykdomas pagal šias eilutes, o ne pradinę eilutę. Jei spausdinami tokie dokumentai kaip patvirtinimai, produktų gavimo kvitų žurnalai ar SF, rodomos tik pristatymo eilutės.  

## <a name="change-the-delivery-schedule"></a>Keisti pristatymo grafiką
Galite keisti pristatymo eilučių kiekį. Jei taip padarote, komercinė eilutė automatiškai atnaujinama į visą pristatymo eilučių kiekį.  
1. Pirmosios pristatymo eilutės lauko **Kiekis** reikšmę pakeiskite iš `4` į `5`.
2. Pasirinkite pirmąją užsakymo eilutę (komercinę eilutę).  
- Komercinės eilutės kiekis pakeistas į 11.  

## <a name="process-product-receipt-using-delivery-schedules"></a>Apdoroti produkto gavimą naudojant pristatymo grafikus
Pirkimo užsakymas turi būti patvirtintas, kad produkto gavimą būtų galima apdoroti. Šiame pavyzdyje gavimas užregistruojamas tiesiai pirkimo užsakyme. Gavimą taip pat buvo galima užregistruoti, kai prekės buvo pristatytos į sandėlį.  
1. Veiksmų srityje pasirinkite **Pirkimas**.
2. Pasirinkite **„Patvirtinti“**.
3. Veiksmų srityje pasirinkite **„Gauti“**.
4. Pasirinkite **„Produkto gavimo kvitas“**. Lauke **Produkto gavimo kvitas** įveskite bet kurią reikšmę.
- Šiame lauke įvedama nuoroda, kuri naudojama kaip produktų gavimo žurnalo kvitas.  
- Lauke **Kiekis** pasirinkite **Užsakytas kiekis**. Pasirinkus šią parinktį bus apdorojamas toks gavimo kiekis, kurį naudojant buvo sukurtos užsakymo eilutės.  
- Įsitikinkite, kad lauko **Spausdinti produkto gavimo kvitą** kvitą parinktis nustatyta kaip **Ne**. Šiame pavyzdyje spausdinti nereikia.  
5. Išplėskite skyrių **Eilutės**.
- Atkreipkite dėmesį, kad kuriamas dviejų pristatymo eilučių, o ne pradinės užsakymo eilutės produkto gavimo kvitas. Jei gavimas užregistruotas sandėlyje, jis bus taip pat užregistruotas pristatymo grafiko eilutėse.  
6. Sutraukite sekciją **Eilutės**.
7. Spustelėkite **Gerai**, kad registruotumėte gavimą.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]