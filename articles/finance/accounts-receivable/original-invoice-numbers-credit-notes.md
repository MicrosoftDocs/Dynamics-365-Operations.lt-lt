---
title: Nuorodos į originalias sąskaitas kredito pranešimuose
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir išspausdinti pradinius SF numerius susijusiose kredito pažymose.
author: mrolecki
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.search.form: ''
ms.openlocfilehash: f1f9ca3914aa02cc38ddfe9f8dd88eb7fc88fd4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281242"
---
# <a name="references-to-original-invoices-in-credit-notes"></a>Nuorodos į originalias sąskaitas kredito pranešimuose

[!include [banner](../includes/banner.md)]


Kai kuriose šalyse ir regionuose yra teisinis reikalavimas, kad spausdinti kredito pranešimai apimtų nuorodas į originalias sąskaitas. Šiame straipsnyje paaiškinama, kaip nustatyti ir išspausdinti pradinius SF numerius susijusiose kredito pažymose.

## <a name="prerequisites"></a>Būtinieji komponentai

- Darbo srityje **Funkcijų valdymas** įjunkite **Kredito sąskaitos išrašymo išdėstymas pardavimams ir projekto sąskaitos ataskaitoms** funkciją. Daugiau informacijos žr. [Funkcijų valdymo apžvalga](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Spausdintini reikiamų dokumentų formatai turi būti konfigūruojami spausdinimo valdyme.

Šiame straipsnyje aprašytos funkcijos taikomos toliau pateikties dokumentams:

**Gautinos sumos**

- Laisvos formos kredito pažyma
- Kliento kredito pažyma

**Projektų valdymas ir apskaita**

- Projekto kredito pažyma

## <a name="configure-accounts-receivable-parameters"></a>Konfigūruoti gautinų sąskaitų parametrus

Atlikite šiuos žingsnius, kad nustatytumėte parametrą, kuris valdo, ar nuorodos į originalias sąskaitas yra spausdinamos susijusiose kredito pažymose.

1. Eikite į **Gautinos sumos** \> **Nustatymai** \> **Gautinų sumų parametrai**.
2. Skirtuke **Naujiniai** „FastTab“ **Sąskaita** nustatykite **Taikyti kredito išrašymą sąskaitos išdėstymą į prekybos ir projekto sąskaitos ataskaitas** parinktį į **Taip**.

![Gautinų sąskaitų parametrų konfigūravimas.](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a>Nustatykite nuorodas į originalias sąskaitas

Naudokite tolesnes procedūras, kad nustatytumėte nuorodas į originalias sąskaitas pagal dokumento tipą.

### <a name="free-text-credit-note"></a>Laisvos formos kredito pažyma

1. Eikite į **Gautinos sumos** \> **Sąskaitos faktūros** \> **Visos laisvos formos SF**.
2. Kurkite naują kredito pažymą ar rinkitės esančią kredito pažymą.
3. Atidarykite sąskaitą.
4. Veiksmų juostoje **Sąskaitos** skirtuke, **Funkcijos** grupėje, rinkitės **Kredito sąskaitos išrašymas**.
5. Įveskite nuorodą į originalią sąskaitą ir rinkitės priežastį taisymui.

![Nustatykite nuorodą laisvo teksto sąskaitai.](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a>Kliento kredito pažyma

1. Eikite į **Gautinos sąskaitos** \> **Užsakymai** \> **Visi pardavimo užsakymai**.
2. Rinkitės ir atverkite išrašytą pardavimo užsakymą, kuris turi būti pataisytas.
3. Veiksmų juostoje **Parduoti** skirtuke, **kredito pažyma** grupėje, rinkitės **Kredito pažyma**.
4. Įveskite taisymo priežastį. Nuoroda į originalią sąskaitą sukuriama automatiškai.

![Nuorodos nustatymas prekybos užsakymui.](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a>Projekto kredito pažyma

1. Eikite į **Projekto valdymas ir apskaita** \> **Projekto sąskaitos** \> **Projekto sąskaitos**.
2. Rinkitės ir atverkite projekto sąskaitą, kuri turi būti pataisyta.
3. Veiksmų juostoje **Projekto sąskaitos** skirtuke, **Funkcijos** grupėje, rinkitės **Rinktis kredito pažymą**.
4. Rinkitės **Kredito sąskaita**.
5. Įveskite taisymo priežastį. Nuoroda į originalią sąskaitą sukuriama automatiškai.

![Nustatykite nuorodą laisvo projekto sąskaitai.](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a>Kredito pažymų spausdinimas

Spausdindami laisvą tekstą, klientą ir projekto kredito pažymą, jis apims nuorodą į originalią sąskaitą ir taisymo priežastį.

![Atspausdinta kredito pažyma.](media/credit-note-FTI.jpg)

> [!NOTE]
> Įsitikinkite, kad spausdinami dokumentų formatai yra tinkamai sukonfigūruoti remiantis prielaida, kad nuorodos į originalias sąskaitas bus atspausdintos.

## <a name="references-to-original-invoices-in-debit-notes"></a>Nuorodos į pradines SF debeto pažymose

Pagal numatytuosius nustatymus galima įvesti kredito pažymų nuorodas į originalias SF. Pavyzdžiui, galite įvesti nuorodas, kai pradinių SF neigiamų (mažėjančių) pataisymų metu.

Norėdami įvesti nuorodas, kai darote teigiamus (didėjančius) pradinių SF taisymus, turite įgalinti nuorodas į **pradines SF funkcijų valdymo darbo srityje debeto** funkciją **Funkcijų valdymas** darbo srityje.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
