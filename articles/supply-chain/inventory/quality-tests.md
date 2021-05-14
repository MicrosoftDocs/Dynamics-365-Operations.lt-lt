---
title: Kokybės valdymo bandymai
description: Šioje temoje aprašoma, kaip sukurti bandymus, kuriuos galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b88011f486b6582db4727b85d021868899c6abe1
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956758"
---
# <a name="quality-management-tests"></a>Kokybės valdymo bandymai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti bandymus, kuriuos galima naudoti kokybės užsakymų „Microsoft Dynamics 365 Supply Chain Management“ bandymams.

Naudokite **Bandymų** puslapį atskiriems tikrinimams, kuriais nustatoma, ar produktai atitinka kokybės reikalavimus, nustatyti ir peržiūrėti. Bandymų grupei galite priskirti vieną arba kelis atskirus bandymus. Šiuo atveju taip pat nurodote konkretaus bandymo informaciją, pvz., priimtinas matavimo reikšmes. Matavimo vertės naudojamos kiekybės bandymams. Kokybinių bandymų metu naudojami bandymo kintamieji.

- Kiekybės bandymams **lauke Tipas nustatoma vertė** Sveikas *skaičius* arba *Trupmena*. Matavimo vienetas taip pat nurodomas. Kokybės specifikacijos ir bandymų rezultatai išreiškiami skaičiais.
- Kokybinių bandymų tipą turite **Tipo** laukelį nustatyti į *Pasirenkamas*. Kokybės bandymams reikia pateikti papildomos informacijos apie bandymų kintamąjį, kuris vertinamas ir jo sunumeruotas parinktis. Kokybės specifikacijos ir bandymų rezultatai išreiškiami atsižvelgiant į rezultatą.

Tikrinimo prietaisą taip pat galite pasirinktinai tikrinimo sričiai. Tačiau tikrinimo priemonėms nereikia kurti ir naudoti bandymų su kokybės užsakymais. Daugiau informacijos ieškokite Kokybės [valdymo tikrinimo](quality-test-instruments.md) priemonės.

Taip pat galite pasirinktinai nurodyti tikrinimo vienetą, norėdami nurodyti matavimo vienetą, į kurį įrašomi tikrinimo rezultatai. Pavyzdžiui, temperatūros tikrinimas gali apimti arba Farenheit, arba Ttsijaus laipsnių vienetą.

## <a name="example-of-a-test"></a>Bandymo pavyzdys

Gamybos įmonė atlieka du įsigytų medžiagų bandymus: kiekybinį bandymą dėl medžiagos kokybės ir kokybinį bandymą dėl pakuotės sugadinimo. Įmonė nurodo papildomos informacijos, susijusios su kokybės tikrinimu, pateikdama tikrinimo kintamąjį (pavyzdžiui, pažeista pakuotė) ir jo rezultatus. Įmonė naudoja **Bandymų grupių** puslapį, kad bandymų grupei priskirtų šiuos du bandymus ir nurodytų konkretaus bandymo informaciją. Tikrinimų grupė priskiriama kokybės užsakymui tam, kad įmonė galėtų pateikti dviejų tikrinimų rezultatų ataskaitą.

## <a name="create-a-test"></a>Kurti bandymą

Atlikite šiuos žingsnius, kad sukurtumėte bandymą.

1. Eikite į **Atsargų valdymas \> Sąranka \> Kokybės kontrolė \> Bandymai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Bandymo instrumentas** – įveskite unikalų tikrinimo prietaiso ID arba pavadinimą.
    - **Aprašas** – įveskite išsamų bandymo instrumento aprašą.
    - **Tipas** – pasirinkite rezultatų, kuriuos testas duoda, tipą. Kiekybės bandymams pasirinkite *Trupmena* *arba sveikasis skaičius*. Kokybinių bandymų atveju pasirinkite *Parinktį*.
    - **Tikrinimo prietaisas** – pasirinkite [tikrinimo](quality-test-instruments.md) prietaisą, kuris turi būti naudojamas bandymams.
    - **Vienetas** – Jei pasirinkote *Frakcija* ar *Sveikasis skaičius* lauke **Tipas** (tai yra, jei bandymas yra kokybės bandymas), pasirinkite matavimo vienetą, kuriuo turi būti įrašyti bandymo rezultatai.

1. Uždarykite puslapį.

> [!NOTE]
> Išsaugoę bandymą, tinklelyje nebegalite **redaguoti** lauko Tipas. Jei turite pakeisti tikrinimo rezultatų, kurie bus įrašyti patikrinti, tipą, veiksmų srityje **pasirinkite Keisti kokybės tikrinimo** tipą. Dialogo lange Keisti kokybės tikrinimo tipą nustatykite norimą lauko Naujas tipas tipą ir **pasirinkite** **Gerai**, **kad** uždarytumėte dialogo langą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo bandymo instrumentai](quality-test-instruments.md)
- [Kokybės valdymo bandymo grupės](quality-test-groups.md)
- [Kokybės valdymo bandymo kintamieji](quality-test-variables.md)
- [Kokybės susiejimai](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
