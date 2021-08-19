---
title: „National Motor Freight Classification“ (NMFC) kodai
description: Šioje temoje aprašoma, kaip dirbti su „National Motor Freight Classification“ (NMFC) kodais programoje „Microsoft Dynamics 365 Supply Chain Management“
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 8e6aac6b3a8b730b6adc5c3d4410b98c3e8d5090eac866c337ed1d03409ba765
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731156"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>„National Motor Freight Classification“ (NMFC) kodai

[!include [banner](../includes/banner.md)]

„National Motor Freight Classification“ (NMFC) kodai padeda klasifikuoti prekes, kurias galima siųsti. NMFC kodas yra priskyrimas, naudojamas prekių grupavimui. Tai leidžia transporto įmonėms įvertinti siuntos prekes klasifikuojant prekes pagal tokias aplinkybes, kaip sunkvežimio krovimas, krovinio pakrovimas, tvarkymą ir nebaigtumą. Prekės grupuojami į vieną iš 18 transportavimo klasių naudojant numerių diapazoną nuo 50 iki 500. Klasė, į kurią sugrupuota prekė, pagrįsta keturiomis transportavimo charakteristikomis: tankumu, krovimo galimybėmis, tvarkymu ir įsipareigojimais. Kartu šios charakteristikos nustato prekės transportavimo galimybes.

NMFC kodas susietas su kiekvienu mažesniu nei sunkvežimio krovinio (LTL) siuntos elementu. Pvz., nešiojamajam kompiuteriui gali būti priskirtas NMFC, kuris yra 2.5 klasė, o elektros įranga – 65 klasės NMFC.

Ši funkcija gali padėti darbuotojams naudoti NMFC kodus, klasifikuojant LTL siuntimo prekes. Štai keletas pavyzdžių:

- Jei jūsų įmonėje važtaraštyje (važtaraštis) pateikiamas transportavimo aprašymas, vežėjas tik šiek tiek žinoti, kas yra transportavimas. Transportavimas yra svarbus klasifikavimas, kadangi daugelis transportavimo įmonių visą verslo modelį pagrįsti savo siuntimo transportavimo tipais.
- Ši klasifikacija gali būti svarbi jūsų įmonei, nes ji naudojama nustatant dinio krovinio išlaidas.
- Jūsų įmonė gali nustatyti LTL logistikos ir transportavimo įmonės pelningumą.

Šioje temoje aprašoma, kaip dirbti su NMFC kodais „Microsoft Dynamics 365 Supply Chain Management“.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš kurdami NMFC kodus, turite nustatyti visas LTL transportavimo klases, kurios turi būti susietos su jomis. LTL transportavimo klasės nurodo prekių kategorijas, o NMFC kodai yra susiję su konkrečiomis prekėmis kiekvienoje iš 18 transportavimo klasių. Daugiau informacijos apie tai, kaip dirbti su LTL klasėmis, ieškokite mažiau nei [sunkvežimio krovinio (LTL)](ltl-class.md) klasės.

## <a name="create-an-nmfc-code"></a>NMFC kodo kūrimas

Norėdami sukurti NMFC kodą, atlikite toliau nurodytus veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Eikite į **Sandėlio valdymas \> Nustatymas \> Atsargos \> NMFC kodai**.
    - Eikite į **Gabenimo valdymas \> Nustatymai \> Gabenimo standartai \> NMFC kodai**.

1. Pasirinkite **Nauja**, kad sukurtumėte NMFC kodą. Tada nustatykite toliau nurodytus laukus.

    - Lauke **NMFC kodas** įveskite NMFC kodą prekės tipui.
    - **Pavadinimas** – Įveskite pavadinimą NMFC kodui.
    - **LTL klasė** – pasirinkite LTL klasę, susietą su NMFC kodu.
    - **Važtaraščio** sandėliavimo vienetas – nustatykite numatytąjį siuntos apdorojimo tipą.

## <a name="example-set-up-nmfc-codes"></a>Pavyzyds: Nustatykite NMFC kodus

Toliau pateikiamas pavyzdys rodo, kaip nustatyti dvi skirtingas NMFC kodai, kuriuos galima naudoti su skirtingais produktų tipais.

1. Eikite į **Sandėlio valdymas \> Nustatymas \> Atsargos \> NMFC kodai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **NMFC kodas:** *92.5*
    - **Pavadinimas:** *Kompiuteriai*
    - **LTL klasė:** *92,5*
    - **BOL sandėliavimo vienetas:** *vienetas*

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujoje eilutėje nustatykite šias reikšmes:

    - **NMFC kodas:** *125*
    - **Pavadinimas:** *telefonai*
    - **LTL klasė:** *125*
    - **BOL sandėliavimo vienetas:** *vienetas*

1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Mažiau nei sunkvežimio (LTL) krovinių klasės](ltl-class.md)
- [Važtaraščio kūrimas](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
