---
title: Konfigūruoti el. pašto kanalą
description: Šioje temoje paaiškinama, kaip konfigūruoti el. pašto kanalą, kad būtų galima gauti elektronines SF.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a5896a033212cf0f29f686eec0ab6fb3bc1d2a6
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371930"
---
# <a name="configure-an-email-channel"></a>Konfigūruoti el. pašto kanalą

[!include [banner](../includes/banner.md)]

Jei jūsų sukurta elektroninių SF išrašymo funkcija importuoja elektronines tiekėjo SF iš pridėtų failų, kurios gautos el. paštu, turėtumėte konfigūruoti el. pašto sąskaitos kanalą.

1. Reguliavimo konfigūracijos tarnybos (RCS) pasirinkite sukurtą elektroninių SF išrašymo priemonę. Įsitikinkite, kad pasirenkate versiją, kurios būsena **Juodraštis**.
2. Skirtuke **Nustatymai** pasirinkite **Įtraukti**.
3. Lauko Grupės **Naujas išplečiamajame** dialogo lange Kurti priemonių **nustatymą** pasirinkite pasirinktį Pasirinktinis **nustatymas**.
4. Lauko grupės **sąrankos** tipas pasirinkite duomenų kanalo **pasirinktį**.
5. Lauke Pasirinkti **duomenų kanalą** įveskite Gaunamą **el. laišką**.
6. Pasirinkite **Kurti**.
7. Pasirinkite sukurtą eilutę, tada pasirinkite **Redaguoti**.
8. Skirtuko Duomenų **kanalas** skyriuje Parametrai **nustatykite** šiuos reikalingus laukus.

    | Laukas                | Aprašymas |
    |----------------------|-------------|
    | Duomenų kanalas         | Įveskite unikalų pavadinimą duomenų kanalui identifikuoti. Pavadinime gali būti ne daugiau kaip 10 simbolių. Jis bus naudojamas kaip pritaikymo taisyklės ir susijusios programos ryšio proceso metu. |
    | Serverio adresas       | Įveskite el. pašto sąskaitos teikėjo serverio adresą. Pvz., teikėjo serverio adresas `https://outlook.live.com` yra imap-mail.outlook.com. |
    | Serverio prievadas          | Įveskite prievado, kurį naudoja el. pašto sąskaitos teikėjas, numerį. Pavyzdžiui, teikėjo serverio prievadas yra `https://outlook.live.com` 993. |
    | Vartotojo vardo slaptasis kodas     | Įveskite rakto Vault slaptojo Microsoft Azure vardo, kuriame yra el. pašto vartotojo sąskaitos ID, pavadinimą. Šį slaptažodį reikia sukurti rakto Vault ir nustatyti savo aptarnavimo aplinkoje. |
    | Vartotojo slaptažodžio slaptasis raktas | Įveskite rakto Vault slaptažodžio, kuriame yra el. pašto vartotojo abonemento slaptažodis, pavadinimą. |
    | Pasibaigė skirtasis laikas              | Maksimalus laiko limitas milisekunde (ms), kurį sistema turi laukti atsakymo. Numatytoji vertė – 10 000 ms (10 sekundžių). |
    | Pagrindinis aplankas          | Nurodykite el. laiško importavimo šaltinį arba aplanką, iš kurį tarnyba turi apdoroti el. laiškus. |
    | Archyvo aplankas       | Nurodykite aplanką, kuriame turi būti saugomi apdoroti el. laiškai. Jei šio aplanko nenu nurodysite, sistema jį sukurs automatiškai. |
    | Klaidų aplankas         | Nurodykite aplanką, į kurį sistema turi perkelti el. laiškus, jei apdorojimas nesėkmingas. Jei šio aplanko nenu nurodysite, sistema jį sukurs automatiškai. |
    | Maksimalus pranešimo dydis     | Įveskite maksimalų apdorojamo pranešimo dydį baitais. Numatytoji vertė yra 20,000,000 baitais. |
    | Maksimalus pranešimų skaičius   | Įvesti didžiausią skaičių pranešimų vienam veiksmui apdoroti. Jei nenorite apriboti pranešimų skaičiaus, **nustatykite vertę 0 (nuliui**). |
    | Filtras Nuo          | Įvesti eilutę, kad būtų galima filtruoti pagal siuntėjo adresą. Bus apdorojami tik el. laiškai, kuriuose siuntėjo adresas atitinka filtrą. Šis laukas nėra būtinas. Norėdami nurodyti kelis siuntėjo adresus, naudokite kabliataškius (;) kaip skyrikliai. |
    | Temos filtras       | Norėdami filtruoti pagal temą, įveskite eilutę. Bus apdorojami tik el. laiškai, kuriuose tema atitinka filtrą. Šis laukas nėra būtinas. Palaikoma paprasta šablono, pvz **\*smth\*.ext**, kai kiekviena žvaigždutė (\*) reiškia nulį arba daugiau bet kurio simbolio pasikartojimų. |
    | Datų filtras          | Nurodykite datą, iki kurios turi būti apibrėžtas maksimalus apdorojamų pranešimų terminas dienomis. Šis laukas nėra būtinas. Numatytoji vertė yra 30 dienų. |
    | Apdorojimo režimas      | <p>Pasirinkite vieną iš šių pasirinkčių norėdami nurodyti, ar visi el. laiško priedai gali būti apdorojami kartu, ar kiekvienas priedas turi būti apdorojamas atskirai:</p><ul><li><b>Pagal priedą</b> – naujas elektroninis dokumentas bus sukurtas kiekvienam el. laiško priedui. Pavyzdžiui, jei viename el. laiške yra keletas failų, kuriuose yra el. SF duomenų, kiekvienas failas sistemoje bus laikomas nauja el. SF.</li><li><b>El.</b> paštu – vienas priedas bus laikomas vienu priedus, o sistemoje bus sukurta viena elektroninė SF. Kitus priedus galima naudoti kaip palaikymo failus.</li></ul> |

9. **Priedų filtro skyriuje** pridėkite failų filtravimo informaciją. Bus apdoroti tik priedai, kurie atitinka nurodytą filtrą. Pavyzdžiui, **\*.xml filtruos** priedus, kurie turi .xml failo vardo plėtinį. Priedo pavadinimas naudojamas nustatymo metu „Dynamics 365 Finance“ arba „Dynamics 365 Supply Chain Management“ jo metu.

    - Jei ankstesniame veiksme **nustatote** apdorojimo **režimo** lauką Kaip el. laišką, čia galite įtraukti kelis filtrus. Pavadinimas identifikuos konkretų dokumentą.
    - Jei apdorojimo režimo **lauką** nustatote **kaip Priedą**, galite pridėti tik vieną filtrą.

10. Skirtuke **Taikymo taisyklės** peržiūrėkite ir atnaujinkite reikiamus kriterijus. Lauko Kanalas vertė **turi** būti lygi vertei, kurią įvedėte **8** žingsnyje duomenų kanalo lauke.
11. Pasirinkite **Išsaugoti** ir uždarykite puslapį.
