---
title: Perkėlimo užsakymo dokumentų mokesčių informacijos spausdinimas
description: Šiame straipsnyje paaiškinama, kaip mokesčių apskaičiavimo tarnybos nustatytą mokesčių informaciją galima išspausdinti perkėlimo užsakymo dokumentuose.
author: Kai-Cloud
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-10-12
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: ca7a610162c539a0ecd74cf9e663f08ea80a7e44
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855208"
---
# <a name="print-tax-information-on-transfer-order-documents"></a>Perkėlimo užsakymo dokumentų mokesčių informacijos spausdinimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip spausdinti mokesčių informaciją perkėlimo užsakymo dokumentuose. Galite spausdinti perkėlimo užsakymo pro forma SF dokumentą, skirtą atsargų perkėlimui, kuris laikomas vidiniu bendrijos tiekimu ir įsigijimais bendrijos viduje pagal Europos Sąjungos (ES) pridėtinės vertės mokesčio (PVM) nuostatus. 

Į perkėlimo užsakymo dokumentus įtraukiami šie su mokesčiais susiję duomenys:

- Atsargų perkėlimo pavadinimai ir siuntėjo bei gavėjo adresai
- Tiekėjo ir gavėjo mokesčių identifikavimo numeriai
- Tiekiamų prekių vieneto kaina ir apmokestinama suma
- Mokesčio kodas, mokesčio tarifas, mokesčio suma ir mokesčių direktyvos

Norėdami konfigūruoti šiuos duomenis, turite atlikti šiuos pagrindinius veiksmus.

1. [Įgalinkite ir nustatykite perkėlimo užsakymų mokesčių funkciją](tasks/Tax-feature-support-for-transfer-order.md).
2. [Kurkite ir nustatykite keletą juridinio subjekto mokesčio registracijos numerių](emea-multiple-vat-registration-numbers.md).
3. Nustatykite neapmokestinimo kodą, aprašymą, mokesčių direktyvas ir atspausdinkite kodą mokesčių koduose. Pavyzdžiui, Microsoft Dynamics trys mokesčių kodai sukuriami ir sinchronizuojami su "365 Finance": **NL-Exempt**, **BE-RC-21** ir **BE-RC+21**.

    1. „Finance” platformoje eikite į **Mokesčiai** \> **Nustatymas** \> **Pardavimo mokestis** \> **Pardavimo mokesčio atleidimo kodai**.
    2. Pasirinkite **Redaguoti** ir įveskite neapmokestinimo **EC** kodo aprašymą. Pvz., įveskite **Neapmokestinamos EC siuntos su mokesčio registracijos numeriu**.
    3. Nueikite į **Mokestis** \> **Netiesioginiai mokesčiai** \> **PVM** \> **PVM kodai**.
    4. Pasirinkite **BE-RC-21** mokesčių kodą, tada pasirinkite **Mokesčių direktyvos**.
    5. Pasirinkite **Naujas**.
    6. **Kalba** laukelyje pasirinkite **EN-US**. Tada į laukelį **Tekstas** įveskite **Dokumento dalis, perkeliant prekes pagal138 straipsnį. 2. c) ES PVM direktyvą 2006/112/EC**.
    7. Uždarykite puslapį.
    8. **Bendras** FastTab skirtuke laukelyje **Spausdinti** pasirinkite **PVM tarifą**.
    8. Pasirinkite **NL neapmokestinamo** mokesčio kodą ir tada **Bendras** FastTab skirtuke **Spausdinti** laukelyje pasirinkite **PVM tarifą**.

    > [!NOTE] 
    > Jei mokesčio kodui nėra taikomas neapmokestinimo kodo aprašymas arba mokesčių direktyvos, perkėlimo užsakymo dokumentuose spausdinamas mokesčio kodas, mokesčio tarifas ir neapmokestinimo aprašas nėra spausdinami.

## <a name="print-the-transfer-order---shipment-document"></a>Spausdinkite perkėlimo užsakymą – siuntimo dokumentas

Kai perkėlimas nusiunčiamas, atlikite šiuos veiksmus, norėdami atspausdinti perkėlimo užsakymą – siuntimo dokumentą.

1. Eikite į **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Perkėlimo užsakymai** \> **Siuntimas**.
2. Skirtuke **Parametrai** grupėje **Spausdinti** įgalinkite **Mokesčių informaciją**.
3. Skirtuke **Norimi įtraukti įrašai** pasirinkite **Filtras**, pasirinkite perkėlimo užsakymo numerį, tada pasirinkite **Gerai**.
4. Pasirinkite **Gerai** norėdami spausdinti perkėlimo užsakymą – siuntimo dokumentą.

## <a name="print-the-transfer-order---receipt-document"></a>Spausdinkite perkėlimo užsakymą – gavimo dokumentą

Kai perkėlimas gautas, atlikite šiuos veiksmus, norėdami atspausdinti perkėlimo užsakymą – gavimo dokumentą.

1. Eikite į **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Perkėlimo užsakymai** \> **Gavimas**.
2. Skirtuke **Parametrai** grupėje **Spausdinti** įgalinkite **Mokesčių informaciją**.
3. Skirtuke **Norimi įtraukti įrašai** pasirinkite **Filtras**, pasirinkite perkėlimo užsakymo numerį, tada pasirinkite **Gerai**.
4. Pasirinkite **Gerai** norėdami spausdinti perkėlimo užsakymą – gavimo dokumentą.

## <a name="print-the-transfer-overview-document"></a>Spausdinkite perkėlimo apžvalgos dokumentą

Norėdami atspausdinti perkėlimo peržiūros dokumentą, atlikite šiuos veiksmus.

> [!NOTE]
> Mokesčių informacija galima tik tada, kai perkėlimo užsakymas yra išsiųstas arba gautas.

1. Eikite į **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Perkėlimo užsakymai** \> **Perkėlimo apžvalga**.
2. Skirtuke **Parametrai** grupėje **Spausdinti** įgalinkite **Mokesčių informaciją**.
3. Skirtuke **Norimi įtraukti įrašai** pasirinkite **Filtras**, pasirinkite perkėlimo užsakymo numerį, tada pasirinkite **Gerai**.
4. Pasirinkite **Gerai** norėdami spausdinti perkėlimo apžvalgos dokumentą.

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
