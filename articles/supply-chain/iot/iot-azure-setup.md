---
title: IoT analizės papildiniui skirtų „Azure“ išteklių konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip sukurti ir konfigūruoti išteklius Microsoft Azure, kurių reikia ĮT įžvalgoms.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07c73ba9b7f718efdf2020b334f24d4212573c4a
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228609"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>IoT analizės papildiniui skirtų „Azure“ išteklių konfigūravimas

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Šiame straipsnyje paaiškinama, kaip sukurti ir konfigūruoti išteklius Microsoft Azure, kurių reikia ĮT įžvalgoms.

## <a name="create-azure-resources"></a>„Azure“ išteklių kūrimas

Norėdami sukurti „IoT Hub“, „Redis“ talpyklą ir raktų saugyklą, kurias galėtų pasiekti „Microsoft Dynamics 365 Supply Chain Management“, atlikite toliau nurodytus veiksmus.

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Patikrinimas, ar „Microsoft Dynamics ERP Microservices“ pirmosios šalies programos ID yra jūsų nuomotojuje

Norėdami patikrinti, ar „Microsoft Dynamics ERP Microservices“ pirmosios šalies programos ID yra jūsų nuomotojuje, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Azure“ portalo adresu <https://portal.azure.com>.
2. Eikite į **Azure Active Directory**.
3. Eikite į **Įmonės programos**.
4. Lauke **Programos tipas** pasirinkite **„Microsoft“ programos**.
5. Ieškos lauke įveskite **Microsoft Dynamics ERP Microservices**.
6. Patikrinkite, ar **Microsoft Dynamics ERP Microservices** yra sąraše. Kitų programų pavadinimai panašūs. Todėl įsitikinkite, kad radote tinkamą programą. Programos ID yra **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Jei programos sąraše nėra, turite ją įtraukti į savo nuomotoją.

    1. „Azure“ portalo įrankių juostoje pasirinkite mygtuką, kad atidarytumėte „Azure Cloud Shell“.
    2. Vykdykite komandą **Install-Module AzureAD**. Įveskite **Y**, kad įdiegtumėte modulį.
    3. Vykdykite komandą **Get-InstalledModule -Name "AzureAD"**, kad įsitikintumėte, jog modulis įdiegtas.
    4. Norėdami vykdyti autentifikavimą, vykdykite komandą **Connect-AzureAD -Confirm**.
    5. Vykdykite komandą **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

    Dabar galite pakartoti 1–6 veiksmus, kad patikrintumėte, jog programos ID yra jūsų nuomotojuje.

### <a name="create-a-key-vault-resource"></a>Raktų saugyklos išteklių kūrimas

Norėdami kurti raktų saugyklos išteklius, atlikite toliau nurodytus veiksmus.

1. „Azure“ portale, sukurkite arba eikite į išteklių grupę.
2. Pasirinkite **Įtraukti**.
3. Puslapio **Nauja** ieškos lauke įveskite **Raktų saugykla**. Paskui paspauskite **Kurti**.
4. Puslapyje **Raktų saugyklos kūrimas** esančiame lauke **Raktų saugyklos pavadinimas** įveskite pavadinimą.
5. Peržiūrėkite numatytąsias reikšmes, tada pasirinkite **Peržiūrėti ir sukurti**.
6. Pasirinkite **Kurti**.

Raktų saugykla sukuriama fone.

### <a name="create-an-iot-hub-resource"></a>„IoT Hub“ išteklių kūrimas

Norėdami kurti „IoT Hub“ išteklius, atlikite toliau nurodytus veiksmus.

1. Kurkite arba eikite į išteklių grupę.
2. Pasirinkite **Įtraukti**.
3. Puslapio **Nauja** ieškos lauke įveskite **„IoT Hub”**. Paskui paspauskite **Kurti**.
4. Lauke **„IoT Hub“ pavadinimas** įveskite pavadinimą.
5. Peržiūrėkite numatytąsias reikšmes, tada pasirinkite **Peržiūrėti ir sukurti**.
6. Pasirinkite **Kurti**.

„IoT Hub“ sukuriamas fone.

> [!NOTE]
> Rekomenduojame vienai aplinkai kurti tik vieną „IoT Hub“ išteklių.

### <a name="create-a-redis-cache-resource"></a>„Redis“ talpyklos išteklių kūrimas

Norėdami kurti „Redis“ talpyklos išteklius, atlikite toliau nurodytus veiksmus.

1. Kurkite arba eikite į išteklių grupę.
2. Pasirinkite **Įtraukti**.
3. Puslapio **Nauja** ieškos lauke įveskite **„Azure“ talpykla, skirta „Redis“**. Paskui paspauskite **Kurti**.
4. Tada lauke **DNS pavadinimas** įveskite pavadinimą.
5. Peržiūrėkite numatytąsias reikšmes, tada pasirinkite **Kurti**.

„Redis“ talpykla sukuriama fone.

> [!NOTE]
> Rekomenduojame vienai aplinkai kurti tik vieną „Redis“ talpyklą.

Dabar sukurti visi ištekliai.

## <a name="configure-the-azure-resources"></a>„Azure“ išteklių konfigūravimas

### <a name="configure-the-iot-hub"></a>„IoT Hub“ konfigūravimas

Norėdami konfigūruoti „IoT Hub“, atlikite toliau nurodytus veiksmus.

1. Savo ištekliuose pasirinkite „IoT Hub“ išteklius.
2. Kairiojoje naršymo srityje pasirinkite **Įtaisytieji galiniai punktai**.
3. Dalyje **Vartotojų grupės** įklijuokite toliau nurodytas vartotojų grupes. Šios vartotojų grupės atitinka parengtus naudoti scenarijus.

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Raktų saugyklos konfigūravimas

Norėdami konfigūruoti raktų saugyklą, atlikite toliau nurodytus veiksmus.

1. Savo ištekliuose pasirinkite raktų saugyklos išteklių.
2. Kairiojoje naršymo srityje pasirinkite **Prieigos strategijos**.
3. Pasirinkite **Įtraukti prieigos strategiją**.
4. Puslapyje **Įtraukti prieigos strategiją** esančiame lauke **Slaptos teisės** pasirinkite **Gauti** ir **Sąrašas**.
5. Spustelėkite **Pasirinkti pagrindinę**.
6. Dialogo lange **Pagrindinis** suraskite ir pasirinkite **„Microsoft Dynamics ERP Microservices”**. Tada pasirinkite **Pasirinkti**.
7. Pasirinkite **Įtraukti**.
8. Pasirinkite **Įrašyti**.

Dabar programa turi prieigą prie slaptųjų raktų, esančių raktų saugykloje.

### <a name="save-the-iot-hub-connection-string-secret"></a>„IoT Hub“ ryšio eilutės slaptojo rakto įrašymas

Norėdami įrašyti „IoT Hub“ ryšio eilutės slaptąjį raktą, atlikite toliau nurodytus veiksmus.

1. Savo ištekliuose pasirinkite „IoT Hub“ išteklius.
2. Kairiojoje naršymo srityje pasirinkite **Įtaisytieji galiniai punktai**.
3. Kopijuokite reikšmę, esančią lauke **Su „Event Hub“ suderinamas galinis punktas**.
4. Eikite į raktų saugyklos išteklius.
5. Kairiojoje naršymo srityje pasirinkite **Slaptieji raktai**.
6. Pasirinkite **Generuoti / importuoti**.
7. Tada lauke **Pavadinimas** įveskite pavadinimą.
8. Lauke **Reikšmė** įklijuokite anksčiau nukopijuotą galinio punkto reikšmę.
9. Pasirinkite **Kurti**.

### <a name="save-the-redis-cache-connection-string-secret"></a>„Redis“ talpyklos ryšio eilutės slaptojo rakto įrašymas

Norėdami įrašyti „Redis“ talpyklos ryšio eilutės slaptąjį raktą, atlikite toliau nurodytus veiksmus.

1. Savo ištekliuose pasirinkite „Redis“ talpyklos išteklių.
2. Pasirinkite **Prieigos raktai**.
3. Nukopijuokite lauke **Pagrindinė ryšio eilutė** esančią reikšmę.
4. Eikite į raktų saugyklos išteklius.
5. Kairiojoje naršymo srityje pasirinkite **Slaptieji raktai**.
6. Pasirinkite **Generuoti / importuoti**.
7. Tada lauke **Pavadinimas** įveskite pavadinimą.
8. Lauke **Reikšmė** įklijuokite anksčiau nukopijuotą ryšio eilutę.
9. Pasirinkite **Kurti**.

> [!NOTE]
> Atnaujindami vieną iš ryšio eilučių, taip pat turite atnaujinti slaptųjų raktų reikšmes.

Dabar baigėte rengti reikiamus „Azure“ išteklius. Kitas veiksmas – [portale „Microsoft Dynamics Lifecycle Services“ (LCS) įdiegti IoT analizės papildinį](iot-lcs-setup.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
