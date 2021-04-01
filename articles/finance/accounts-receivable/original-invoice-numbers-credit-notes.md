---
title: Nuorodos į originalias sąskaitas kredito pranešimuose
description: Šioje temoje paaiškinta, kaip nustatyti ir spausdinti originalių sąskaitų numerius susijusiuose kredito pranešimuose.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 04a4fc96cb7de60052b17e36c33ad5d5be322be4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207356"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Nuorodos į originalias sąskaitas kredito pranešimuose

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Kai kuriose šalyse ir regionuose yra teisinsi reikalvimas, kad spausdinti kredito pranešimai apimtų nuorodas į originalias sąskaitas. Šioje temoje paaiškinta, kaip nustatyti ir spausdinti originalių sąskaitų numerius susijusiuose kredito pranešimuose.

## <a name="prerequisites"></a>Būtinieji komponentai

- Darbo srtiyje **Funkcijų valdymas** įjunkite **Kredito sąskaitos išrašymo išdėstymas pardavimams ir projekto sąskaitos ataskaitoms** funkciją. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).
- Spausdintinti reikiamų dokumentų formatai turi būti konfigūruojami spausdinimo valdyme.

Šioje temoje aprašyta funkcija taikoma šiems dokumentams:

**Gautinos sumos**

- Laisvos formos kredito pažyma
- Kliento kredito pažyma

**Projektų valdymas ir apskaita**

- Projekto kredito pažyma

## <a name="configure-accounts-receivable-parameters"></a>Konfigūruoti gautinų sąskaitų parametrus

Atlikite šiuos žingsnius, kad nustatytumėte parametrą, kuris valdo, ar nuorodos į originalias sąskaitas yra spausdinamos susijusiose kredito pažymose.

1. Eikite į **Gautinos sumos** \> **Nustatymai** \> **Gautinų sumų parametrai**.
2. Skirtuke **Naujiniai** „FastTab“ **Sąskaita** nustatykite **Taikyti kredito išrašymą sąskaitos išdėstymą į prekybos ir projekto sąskaitos ataskaitas** parinktį į **Taip**.

![Gautinų sąskaitų parametrų konfigūravimas](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Nustatykite nuorodas į originalias sąskaitas

Naudokite tolesnes procedūras, kad nustatytumėte nuorodoas į originalias sąskaitas pagal dokumento tipą.

### <a name="free-text-credit-note"></a>Laisvos formos kredito pažyma

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Kurkite naują kredito pažymą ar rinkitės esančią kredito pažymą.
3. Atidarykite sąskaitą.
4. Veiksmų juostoje **Sąskaitos** skirtuke, **Funkcijos** grupėje, rinkitės **Kredito sąskaitos išrašymas**.
5. Įveskite nuorodą į originalią sąskaitą ir rinkiės priežastį taisymui.

![Nustatykite nuorodą laisvo teksto sąskaitai](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Kliento kredito pažyma

1. Eikite į **Gautinos sąskaitos** \> **Užsakymai** \> **Visi pardavimo užsakymai**.
2. Rinkitės ir atverkite išrašytą pardavimo užsakymą, kuris turi būti pataisytas.
3. Veiksmų juostoje **Parduoti** skirtuke, **kredito pažyma** grupėje, rinkitės **Kredito pažyma**.
4. Įveskite taisymo priežastį. Nuoroda į orignalią sąskaitą sukuriama automatiškai.

![Nuorodos nustatymas prekybos užsakymui](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projekto kredito pažyma

1. Eiktie į **Projekto valdymas ir apskaita** \> **Projekto sąskaitos** \> **Projekto sąskaitos**.
2. Rinkitės ir atverkite projekto sąskaitą, kuri turi būti pataisyta.
3. Veiksmų juostoje **Projekto sąskaitos** skirtuke, **Funkcijos** grupėje, rinkitės **Rinktis kredito pažymą**.
4. Rinkitės **Kredito sąskaita**.
5. Įveskite taisymo priežastį. Nuoroda į orignalią sąskaitą sukuriama automatiškai.

![Nustatykite nuorodą laisvo projekto sąskaitai](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Kredito pažymų spausdinimas

Spausdindami laisvą tekstą, klientą ir projekto kredito pažymą, jis apims nuorodą į originalią sąskaitą ir taisymo priežastį.

![Atspausdinta kredito pažyma](media/credit-note-FTI.jpg)

> [!NOTE]
> Įsitikinkite, kad spausdinami dokumentų formatai yra tinkamai sukonfigūruoti remiantis prielaida, kad nuorodos į originalias sąskaitas bus atspausdintos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]