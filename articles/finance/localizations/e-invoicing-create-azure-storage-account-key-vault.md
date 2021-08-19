---
title: „Azure” saugyklos abonemento ir raktų saugyklos kūrimas
description: Šioje temoje paaiškinama, kaip sukurti „Azure” saugyklos abonementą ir raktų saugyklą.
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a0fe265c75138f3ecfbf08de3c30b2c824463afc35414986e21c4a27bf84bb61
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770541"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>„Azure” saugyklos abonemento ir raktų saugyklos kūrimas

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami atlikti šioje temoje esančius veiksmus, turite įsitikinti, kad atliktos toliau nurodytos užduotys.

- Sukurti raktų saugyklos išteklius „Azure”. Daugiau informacijos žr. [Apie „Azure Key Vault”](/azure/key-vault/general/overview).
- Sukurti „Azure” saugyklos abonementą (didelių dvejetainių objektų saugykla). Daugiau informacijos žr. [„Azure” saugyklos abonemento priežiūra](/azure/storage/blobs/).

## <a name="overview"></a>Peržiūra

Šioje temoje galėsite atlikti du toliau pateiktus pagrindinius veiksmus.

- Nustatyti „Azure” saugyklos abonementą, kad būtų gautas saugyklos abonemento URI.
- Nustatyti raktų saugyklą, kad būtų saugomas saugyklos abonemento URI.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>„Azure” saugyklos abonemento nustatymas siekiant gauti saugyklos abonemento URI

1. Atidarykite saugyklos abonementą, kurį planuojate naudoti su elektroninių SF išrašymo priedu.
2. Eikite į **Didelio dvejetainio objekto paslauga** \> **Konteineriai** ir sukurkite naują konteinerį.
3. Įveskite konteinerio pavadinimą ir nustatykite lauką **Viešosios prieigos lygis** į **Privatus (ne anoniminė prieiga)**.
4. Atidarykite konteinerį ir eikite į **Parametrai \> Prieigos strategija**.
5. Pasirinkite **Įtraukti strategiją**, norėdami įtraukti saugomą prieigos strategiją.
6. Atitinkamai nustatykite laukus **Identifikatorius** ir **Teisės**. Lauke **Teisės** turite pasirinkti visas teises.

    ![Didelių dvejetainių objektų saugyklos teisių suteikimas.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Įveskite pradžios ir pabaigos datas. Galiojimo data turi būti data ateityje.
8. Pasirinkite **Gerai**, norėdami įrašyti strategiją, tada įrašykite konteinerio keitimus.
9. Grįžkite į saugyklos abonementą ir atidarykite **Saugyklos naršyklė (peržiūra)**.
10. Dešiniuoju pelės klavišu spustelėkite konteinerį ir pasirinkite **Gauti bendrai naudojamą prieigos parašą**.
11. Dialogo lange **Bendrai naudojamas prieigos parašas** kopijuokite ir išsaugokite reikšmę, esančią lauke **URI**. Ši reikšmė bus naudojama kitoje procedūroje ir bus vadinama *bendrai naudojamo prieigos parašo URI*.

    ![URI reikšmės pasirinkimas ir kopijavimas.](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Raktų saugyklos nustatymas siekiant saugoti saugyklos abonemento URI

1. Atidarykite raktų saugyklą, kurią planuojate naudoti su elektroninių SF išrašymo priedu.
2. Norėdami sukurti naują slaptąjį raktą, eikite į **Parametrai** \> **Slaptieji raktai** ir pasirinkite **Generuoti / importuoti**.
3. Puslapio **Sukurti slaptąjį raktą** lauke **Nusiuntimo parinktys** pasirinkite **Rankinis**.
4. Įveskite slaptojo rakto pavadinimą. Šis pavadinimas bus naudojamas paslaugos nustatymo metu „Regulatory Configuration Services” (RCS) ir bus nurodomas kaip *raktų saugyklos slaptojo rakto pavadinimas*.
5. Lauke **Reikšmė** pasirinkite **Bendrai naudojamo prieigos parašo URI** ir tada pasirinkite **Kurti**.
6. Nustatykite prieigos strategiją, kad elektroninių SF išrašymo priedui būtų galima suteikti tinkamą saugios prieigos prie jūsų sukurto slaptojo rakto lygį. Eikite į **Parametrai \> Prieigos strategija** ir pasirinkite **Įtraukti prieigos strategiją**.
7. Nustatykite operacijų **Gauti** ir **Išvardyti** slaptųjų raktų teises.

    ![Paslaugos prieigos suteikimas.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Nustatykite operacijų **Gauti** ir **Išvardyti** sertifikatų teises.

    ![Sertifikatų teisių suteikimas.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Laukelyje **Pasirinkti pagrindą** pasirinkite **Nieko nepasirinkta**.
10. Dialogo lange **Pagrindas** pasirinkite pagrindą, įtraukdami **El. SF išrašymo paslaugą**.
11. Pasirinkite **Įtraukti**, tada pasirinkite **Įrašyti „Key Vault” keitimus**.
12. Puslapyje **Apžvalga** nukopijuokite raktų saugyklos reikšmę **DNS pavadinimas**. Ši reikšmė bus naudojama paslaugos nustatymo metu RCS ir bus vadinama *raktų saugyklos URI*.

> [!NOTE]
> Norėdami gauti papildomos saugojimo sąskaitos saugos, sukonfigūruokite „Azure Defender for Storage".
> 
> Daugiau informacijos rasite [Įžanga į „Azure Defender for Storage“](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
