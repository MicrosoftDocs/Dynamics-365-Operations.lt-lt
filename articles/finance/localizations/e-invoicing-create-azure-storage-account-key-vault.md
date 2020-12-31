---
title: „Azure” saugyklos abonemento ir raktų saugyklos kūrimas
description: Šioje temoje paaiškinama, kaip sukurti „Azure” saugyklos abonementą ir raktų saugyklą.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5a883011bbff6d82504497d739c07f1ada9e5f69
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/19/2020
ms.locfileid: "4446170"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>„Azure” saugyklos abonemento ir raktų saugyklos kūrimas

[!include [banner](../includes/banner.md)]



Elektroninių SF išrašymo priedo paslauga yra atsakinga už visų jūsų verslo duomenų saugojimą „Microsoft Azure” ištekliuose, kurie priklauso jūsų įmonei. Siekiant užtikrinti, kad paslauga veiktų tinkamai ir kad visus verslo duomenis, kurių reikia elektroninių SF išrašymo priedui ir kuriuos jis sugeneravo, galėtų pasiekti tik priedas, turite sukurti du pagrindinius toliau pateiktus „Azure” išteklius.

- „Azure” saugyklos abonementas (didelių dvejetainių objektų saugykla), skirtas elektroninėms SF saugoti
- „Azure” raktų saugykla, skirta sertifikatams ir saugyklos abonemento vieningajam išteklių identifikatoriui (URI) saugoti

> [!NOTE]
> Paskirti raktų saugyklos ištekliai ir kliento didelių dvejetainių objektų saugykla turi būti priskirti tik elektroninių SF išrašymo priedo naudojimui.

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami atlikti šioje temoje esančius veiksmus, turite įsitikinti, kad atliktos toliau nurodytos užduotys.

- Sukurti raktų saugyklos išteklius „Azure”. Daugiau informacijos žr. [Apie „Azure Key Vault”](https://docs.microsoft.com/azure/key-vault/general/overview).
- Sukurti „Azure” saugyklos abonementą (didelių dvejetainių objektų saugykla). Daugiau informacijos žr. [„Azure” saugyklos abonemento priežiūra](https://docs.microsoft.com/azure/storage/blobs/).

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

    ![Didelių dvejetainių objektų saugyklos teisių suteikimas](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Įveskite pradžios ir pabaigos datas. Galiojimo data turi būti data ateityje.
8. Pasirinkite **Gerai**, norėdami įrašyti strategiją, tada įrašykite konteinerio keitimus.
9. Grįžkite į saugyklos abonementą ir atidarykite **Saugyklos naršyklė (peržiūra)**.
10. Dešiniuoju pelės klavišu spustelėkite konteinerį ir pasirinkite **Gauti bendrai naudojamą prieigos parašą**.
11. Dialogo lange **Bendrai naudojamas prieigos parašas** kopijuokite ir išsaugokite reikšmę, esančią lauke **URI**. Ši reikšmė bus naudojama kitoje procedūroje ir bus vadinama *bendrai naudojamo prieigos parašo URI*.

    ![URI reikšmės pasirinkimas ir kopijavimas](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Raktų saugyklos nustatymas siekiant saugoti saugyklos abonemento URI

1. Atidarykite raktų saugyklą, kurią planuojate naudoti su elektroninių SF išrašymo priedu.
2. Norėdami sukurti naują slaptąjį raktą, eikite į **Parametrai** \> **Slaptieji raktai** ir pasirinkite **Generuoti / importuoti**.
3. Puslapio **Sukurti slaptąjį raktą** lauke **Nusiuntimo parinktys** pasirinkite **Rankinis**.
4. Įveskite slaptojo rakto pavadinimą. Šis pavadinimas bus naudojamas paslaugos nustatymo metu „Regulatory Configuration Services” (RCS) ir bus nurodomas kaip *raktų saugyklos slaptojo rakto pavadinimas*.
5. Lauke **Reikšmė** pasirinkite **Bendrai naudojamo prieigos parašo URI** ir tada pasirinkite **Kurti**.
6. Nustatykite prieigos strategiją, kad elektroninių SF išrašymo priedui būtų galima suteikti tinkamą saugios prieigos prie jūsų sukurto slaptojo rakto lygį. Eikite į **Parametrai \> Prieigos strategija** ir pasirinkite **Įtraukti prieigos strategiją**.
7. Nustatykite operacijų **Gauti** ir **Išvardyti** slaptųjų raktų teises.

    ![Paslaugos prieigos suteikimas](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Nustatykite operacijų **Gauti** ir **Išvardyti** sertifikatų teises.

    ![Sertifikatų teisių suteikimas](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Dialogo lange **Pagrindas** pasirinkite pagrindą, įtraukdami **Elektroninių SF išrašymo priedas**.
10. Pasirinkite **Įtraukti**, tada pasirinkite **Įrašyti „Key Vault” keitimus**.
11. Puslapyje **Apžvalga** nukopijuokite raktų saugyklos reikšmę **DNS pavadinimas**. Ši reikšmė bus naudojama paslaugos nustatymo metu RCS ir bus vadinama *raktų saugyklos URI*.
