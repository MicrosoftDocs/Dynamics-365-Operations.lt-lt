---
title: Aptarnavimo užsakymų kūrimas rankiniu būdu
description: Galite aptarnavimo užsakymus kurti rankiniu būdu naudodami aptarnavimo sutartį arba naudodami formą **Aptarnavimo užsakymai**.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1fad4abcf39021f94db50c07a39803af31f85c2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578853"
---
# <a name="create-service-orders-manually"></a>Aptarnavimo užsakymų kūrimas rankiniu būdu    

[!include [banner](../includes/banner.md)]


Galite aptarnavimo užsakymus kurti rankiniu būdu naudodami aptarnavimo sutartį arba naudodami formą **Aptarnavimo užsakymai**. Taip pat galite kurti aptarnavimo užsakymą iš projekto.

> [!TIP]
> <P>Aptarnavimo užsakymams kurti galite naudoti automatizuotus procesus. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Rankinis aptarnavimo užsakymo kūrimas iš aptarnavimo sutarties

1.  Pasirinkite **Aptarnavimo valdymas** \> **Bendrasis** \> **Aptarnavimo sutartys** \> **Aptarnavimo sutartys**.

2.  Pasirinkite aptarnavimo sutartį arba sukurkite naują aptarnavimo sutartį.

3.  Pasirinkite skirtuką **Pristatyti** ir grupėje **Kurti** pasirinkite **Suplanuoti aptarnavimo užsakymai** norėdami atidaryti formą **Kurti aptarnavimo užsakymus**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>Neautomatinis aptarnavimo užsakymo kūrimas formoje Aptarnavimo užsakymai

1.  Pasirinkite **Aptarnavimo valdymas** \> **Bendra** \> **Aptarnavimo užsakymai** \> **Aptarnavimo užsakymai**.

2.  Pasirinkite **Nauja**, kad sukurtumėte naują paslaugų užsakymą.

3.  Sukurkite aptarnavimo užsakymo eilutes.

> [!NOTE]
> <P>Jei žymės langelis <STRONG>Leisti be aptarnavimo sutarties</STRONG> pažymėtas formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>, galite registruoti aptarnavimo užsakymo eilučių operacijas, nepridėdami aptarnavimo užsakymo prie aptarnavimo sutarties. Jei žymės langelis išvalytas, prieš registruodami aptarnavimo užsakymo eilutes prie projekto turite pridėti rankiniu būdu sukurtą aptarnavimo užsakymą.</P>

## <a name="create-a-service-order-from-a-project"></a>Aptarnavimo užsakymo kūrimas iš projekto

1.  Eikite į **Projektų valdymas ir apskaita** \> **Bendra** \> **Projektai** \> **Visi projektai**.

2.  Formoje **Projektai**, esančioje **Veiksmų sritis**, pasirinkite skirtuką **Valdyti** \> pasirinkite **Aptarnavimas** \> **Aptarnavimo užsakymai**.

3.  Vadovaukitės ankstesne aptarnavimo užsakymo kūrimo rankiniu būdu procedūra formoje **Aptarnavimo užsakymai**. Lauke **Projekto ID** rodoma projekto nuoroda.

> [!NOTE]
> <P>Jei žymės langelis <STRONG>Leisti be aptarnavimo sutarties</STRONG> pažymėtas formoje <STRONG>Aptarnavimo valdymo parametrai</STRONG>, galite registruoti aptarnavimo užsakymo eilučių operacijas, nepridėdami aptarnavimo užsakymo prie aptarnavimo sutarties. Jei žymės langelis išvalytas, prieš registruodami aptarnavimo užsakymo eilutes prie projekto turite pridėti rankiniu būdu sukurtą aptarnavimo užsakymą.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Aptarnavimo užsakymų kūrimas iš pardavimo užsakymo formos

Aptarnavimo užsakymą galima sukurti formoje **Pardavimo užsakymai** naudodami vedlį **Kurti naują aptarnavimo užsakymą pagal pardavimo užsakymą**.

1.  Eikite į **Pardavimas ir rinkodara** \> **Bendra** \> **Pardavimo užsakymai** \> **Visi pardavimo užsakymai**.

2.  Atidarykite reikalingą pardavimo užsakymą.

3.  Skirtuke **Pardavimo užsakymas** pasirinkę **Aptarnavimo užsakymas** paleiskite vedlį **Kurti naują aptarnavimo užsakymą, pagrįstą pardavimo užsakymu**.

4.  Pasirinkite **Tolesnis \>**, tuomet atlikite toliau nurodytus veiksmus puslapyje **Pasirinkite aptarnavimo užsakymo sutartį**:
    
      - Naudokite lauką **Aptarnavimo sutartis** aptarnavimo sutarčiai, su kuria naujasis aptarnavimo užsakymas turi būti susietas, pasirinkti.
    
      - (Pasirinktinai:) naudokite lauką **Projekto ID**, kad šį aptarnavimo užsakymą susietumėte su tam tikru projektu.

5.  Pasirinkite **Tolesnis \>**, tuomet atlikite toliau nurodytus veiksmus puslapyje **Kurti aptarnavimo užsakymą**:
    
      - Įveskite datą ir laiką, kad aptarnavimo skambutis prasidėtų lauke **Pageidaujamas aptarnavimo laikas**.
    
      - Pasirinktinai: jei reikia, tekstą galite modifikuoti lauke **Aprašas**. Pagal numatytuosius nustatymus, šiame lauke pateikiamas aptarnavimo sutarties aprašas, kurį pasirinkote ankstesniame puslapyje.
    
      - Lauke **Atsakingas** pasirinkite darbuotojo, kuris atsakingas už sutartį, ID ir jei žinote, kas tai yra, įveskite kliento pageidaujamo aptarnavimui atlikti techniko ID.
    
      - Lauke **Kontakto ID** pasirinkite kliento įmonės asmenį, su kuriuo bus susisiekta dėl aptarnavimo užsakymo.

6.  Pasirinkite **Tolesnis\>** ir pasirinkite **Baigti**.


## <a name="see-also"></a>Taip pat žiūrėkite

[Aptarnavimo užsakymai](service-orders.md)

[Automatinis aptarnavimo užsakymų kūrimas](create-service-orders-automatically.md)

[Aptarnavimo užsakymų kūrimas (klasės forma)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]