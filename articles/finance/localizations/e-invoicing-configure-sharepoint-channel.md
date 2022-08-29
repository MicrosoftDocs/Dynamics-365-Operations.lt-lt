---
title: „SharePoint“ kanalo konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti "Microsoft" kanalą SharePoint gaunaoms elektroninėms SF apdoroti.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 92eaa357c6d72cc637d4ce353702e5d41ecf4338
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272311"
---
# <a name="configure-a-sharepoint-channel"></a>„SharePoint“ kanalo konfigūravimas

[!include [banner](../includes/banner.md)]

Norėdami konfigūruoti "Microsoft SharePoint " kanalą gaunamiems dokumentams apdoroti, atlikite veiksmus, aprašytus dalyje [Konfigūruoti SharePoint ryšį](e-invoicing-create-sharepoint-connection.md).

Tada galite naudoti kanalą SharePoint, norėdami importuoti elektronines tiekėjo SF iš failų, saugomų jūsų aplankuose SharePoint.

1. Savo svetainėje SharePoint sukurkite šiuos aplankus:

    - **Pagrindinis aplankas** – aplankas, iš kurį tarnyba apdoros failus.
    - **Archyvo** aplankas – aplankas, kuriame bus saugomi apdoroti failai.
    - **Klaidų aplankas** – aplankas, į kurį sistema perkels failus, jei apdorojimas nesėkmingas.

2. Reguliavimo konfigūracijos tarnybos (RCS) pasirinkite sukurtą elektroninių SF išrašymo priemonę. Įsitikinkite, kad pasirenkate versiją, kurios būsena **Juodraštis**.
3. Skirtuke **Nustatymai** pasirinkite **Įtraukti**.
4. Lauko Grupės **Naujas išplečiamajame** dialogo lange Kurti priemonių **nustatymą** pasirinkite pasirinktį Pasirinktinis **nustatymas**.
5. Lauko grupės **sąrankos** tipas pasirinkite duomenų kanalo **pasirinktį**.
6. **Lauke Pasirinkti duomenų kanalą** pasirinkite **SharePoint aplanką**.
7. Pasirinkite **Kurti**.
8. Pasirinkite sukurtą eilutę, tada pasirinkite **Redaguoti**.
9. Skirtuko Duomenų **kanalas** skyriuje Parametrai **nustatykite** šiuos reikalingus laukus.

    | Laukas                 | Aprašymas |
    |-----------------------|-------------|
    | Duomenų kanalas          | Įveskite unikalų pavadinimą duomenų kanalui identifikuoti. Pavadinime gali būti ne daugiau kaip 10 simbolių. Jis bus naudojamas kaip tinkamumo taisyklės ir susijusios programos ryšio proceso metu. |
    | „SharePoint“ adresas    | SharePoint Įveskite URL. Pavyzdžiui, įveskite `<domain>.sharepoint.com`. |
    | Programos ID        | Įveskite "Azure Key Vault" slaptojo kodo, kuriame yra vartotojo sąskaitos SharePoint ID, pavadinimą. Šį slaptažodį reikia sukurti rakto Vault ir nustatyti savo aptarnavimo aplinkoje. Reikšmė yra programos **(kliento) ID** vertė iš ryšio konfigūruoti [SharePoint](e-invoicing-create-sharepoint-connection.md). |
    | Programos slapta informacija    | Įveskite rakto Vault slaptažodžio, kuriame yra vartotojo abonemento slaptažodis SharePoint, pavadinimą. Reikšmė yra programos registracijos **slaptos vertės iš** ryšio konfigūravimo [SharePoint](e-invoicing-create-sharepoint-connection.md). |
    | Svetainės pavadinimas             | Įveskite svetainės SharePoint pavadinimą. |
    | Dokumentų bibliotekos pavadinimas | Įveskite dokumentų bibliotekos SharePoint pavadinimą. |
    | Pasibaigė skirtasis laikas               | Įveskite maksimalų laiką milisekunde (ms), kurį sistema turi laukti atsakymo. Numatytoji vertė – 10 000 ms (10 sekundžių). |
    | Pagrindinis aplankas           | Nurodykite failo importavimo šaltinį ar aplanką, iš kurį tarnyba turi apdoroti failus. |
    | Archyvo aplankas        | Nurodykite aplanką, kuriame turi būti saugomi apdoroti failai. |
    | Klaidų aplankas          | Nurodykite aplanką, į kurį sistema turi perkelti failus, jei apdorojimas nesėkmingas. |
    | Maksimalus failo dydis         | Įveskite maksimalų apdorojamo failo dydį baitais. Numatytoji vertė yra 20,000,000 baitais. |
    | Maks. failų skaičius      | Įveskite didžiausią skaičių failų vienam veiksmui atlikti. Jei nenorite apriboti failų skaičiaus, **nustatykite vertę 0** (nuliui). |
    | Failo filtras           | Norėdami filtruoti pagal failo vardą, įveskite eilutę. Šis laukas nėra būtinas. Palaikoma paprasta šablono, pvz **\*smth\*.ext**, kai kiekviena žvaigždutė (\*) reiškia nulį arba daugiau bet kurio simbolio pasikartojimų. Pvz., įveskite **\*.pdf norėdami** sukonfigūruoti kanalą, kad būtų perskaityti PDF failai. |
    | Pasirinktinis failo vardas      | Įveskite kliento pasirinktinio failo vardą. |

10. Skirtuke **Taikymo taisyklės** peržiūrėkite ir atnaujinkite reikiamus kriterijus. Lauko Kanalas vertė **turi** būti lygi ankstesnio veiksmo lauke **Duomenų kanalas** įvestai vertei.
11. Pasirinkite **Išsaugoti** ir uždarykite puslapį.
