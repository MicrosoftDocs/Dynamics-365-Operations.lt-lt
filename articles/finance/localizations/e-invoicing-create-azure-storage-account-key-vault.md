---
title: „Azure” saugyklos abonemento ir raktų saugyklos kūrimas
description: Šiame straipsnyje paaiškinama, kaip sukurti "Azure" saugyklos sąskaitą ir kodo saugyklą.
author: gionoder
ms.date: 08/17/2021
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
ms.openlocfilehash: ae2f21e959e35690ca3d8bd09059cfbf679ab842
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907767"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a>„Azure” saugyklos abonemento ir raktų saugyklos kūrimas

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami šiame straipsnyje nurodytus veiksmus, įsitikinkite, kad buvo atlikta ši užduotis:

- Sukurti raktų saugyklos išteklius „Azure”. Daugiau informacijos žr. [Apie „Azure Key Vault”](/azure/key-vault/general/overview).
- Sukurti „Azure” saugyklos abonementą (didelių dvejetainių objektų saugykla). Daugiau informacijos žr. [„Azure” saugyklos abonemento priežiūra](/azure/storage/blobs/).

## <a name="overview"></a>Apžvalga

Šiame straipsnyje atlikite du pagrindinius veiksmus:

- Nustatyti „Azure” saugyklos abonementą, kad būtų gautas saugyklos abonemento URI.
- Nustatyti raktų saugyklą, kad būtų saugomas saugyklos abonemento URI.

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a>„Azure” saugyklos abonemento nustatymas siekiant gauti saugyklos abonemento URI

1. Atidarykite saugyklos abonementą, kurį planuojate naudoti su elektroninių SF išrašymo priedu.
2. Eikite į **Duomenų talpinimas** > **Talpyklos** ir kurkite naują talpyklą.
3. Įveskite konteinerio pavadinimą ir nustatykite lauką **Viešosios prieigos lygis** į **Privatus (ne anoniminė prieiga)**.
4. Atidarykite konteinerį ir eikite į **Parametrai** > **Prieigos strategija**.
5. Pasirinkite **Įtraukti strategiją**, norėdami įtraukti saugomą prieigos strategiją.
6. Atitinkamai nustatykite laukus **Identifikatorius** ir **Teisės**. Lauke **Teisės** turite pasirinkti visas teises.

    ![Didelių dvejetainių objektų saugyklos teisių suteikimas.](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. Įveskite pradžios ir pabaigos datas. Galiojimo data turi būti data ateityje.
8. Pasirinkite **Gerai**, norėdami įrašyti strategiją, tada įrašykite konteinerio keitimus.
9. Eikite į **Parametrų** > **bendrai naudojamos prieigos** atpažinimo ženklus ir nustatykite lauko vertes. 
10. Įveskite pradžios ir pabaigos datas. Galiojimo data turi būti data ateityje.
11. Teisių lauke **Teisės** rinkitės šias teises: **Skaityti**, **Įtraukti**, **Kurti**, **Rašyti**, **Naikinti**, ir **Sąrašą**. 
12. Pasirinkite **Generuoti SAS atpažinimo ženklą ir URL**.
13. Nukopijuokite ir saugokite reikšmę **BLOB SAS URL** lauke. Ši reikšmė bus naudojama kitoje procedūroje ir bus vadinama *bendrai naudojamo prieigos parašo URI*.

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a>Raktų saugyklos nustatymas siekiant saugoti saugyklos abonemento URI

1. Atidarykite raktų saugyklą, kurią planuojate naudoti su elektroninių SF išrašymo priedu.
2. Norėdami sukurti naują slaptąjį raktą, eikite į **Parametrai** \> **Slaptieji raktai** ir pasirinkite **Generuoti / importuoti**.
3. Puslapio **Sukurti slaptąjį raktą** lauke **Nusiuntimo parinktys** pasirinkite **Rankinis**.
4. Įveskite slaptojo rakto pavadinimą. Šis pavadinimas bus naudojamas paslaugos nustatymo metu „Regulatory Configuration Services” (RCS) ir bus nurodomas kaip *raktų saugyklos slaptojo rakto pavadinimas*.
5. Reikšmės **lauke** įveskite bendrai naudojamos prieigos parašo URI, kurį nukopijavote ankstesnėje procedūroje, tada pasirinkite **Kurti**.
6. Nustatykite prieigos strategiją, kad elektroninių SF išrašymo priedui būtų galima suteikti tinkamą saugios prieigos prie jūsų sukurto slaptojo rakto lygį. Eikite į **Parametrai \> Prieigos strategija** ir pasirinkite **Įtraukti prieigos strategiją**.
7. Nustatykite operacijų **Gauti** ir **Išvardyti** slaptųjų raktų teises.

    ![Paslaugos prieigos suteikimas.](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. Nustatykite operacijų **Gauti** ir **Išvardyti** sertifikatų teises.

    ![Sertifikatų teisių suteikimas.](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. Laukelyje **Pasirinkti pagrindą** pasirinkite **Nieko nepasirinkta**.
10. Dialogo lange **Pagrindas** pasirinkite pagrindą, įtraukdami **El. SF išrašymo paslaugą**.
11. Pasirinkite **Įtraukti**, tada pasirinkite **Įrašyti**.
12. Puslapyje **Apžvalga** nukopijuokite raktų saugyklos reikšmę **DNS pavadinimas**. Ši reikšmė bus naudojama paslaugos nustatymo metu RCS ir bus vadinama *raktų saugyklos URI*.

> [!NOTE]
> Norėdami gauti papildomos saugojimo sąskaitos saugos, sukonfigūruokite „Azure Defender for Storage".
> 
> Daugiau informacijos rasite [Įžanga į „Azure Defender for Storage“](/azure/security-center/defender-for-storage-introduction).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
