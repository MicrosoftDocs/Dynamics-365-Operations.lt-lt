---
title: SF fiksavimo sprendimo susiejimo taisyklės
description: Šiame straipsnyje pateikiama informacija apie SF fiksavimo sprendimo susiejimo taisyklių nustatymą.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d06f7fd3ed946756e975d0706687c2d4acc93
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691009"
---
# <a name="invoice-capture-solution-mapping-rules"></a>SF fiksavimo sprendimo susiejimo taisyklės

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Susiejimo taisyklės suteikia pagrindinius pagrindinius duomenis iš Microsoft Dynamics 365 finansų arba įmonės išteklių planavimo (ERP) sistemos. Nustačius susiejimo taisykles, išvedamas informacija, kurios reikia kuriant tiekėjo SF finansuose. Kai naudojamos susiejimo taisyklės, mokėtinų sumų (AP) klerkas užuot neautomatiniu būdu užpildęs visas trūkstamų laukų vertes, patikrins būseną.

Yra keturi susiejimo taisyklių tipai:

- Juridinis subjektas
- Tiekėjo paskyra
- Elementas
- Išlaidų tipas

## <a name="manage-mapping-rules-by-using-the-app"></a>Tvarkyti susiejimo taisykles naudojant programą

Norėdami tvarkyti susiejimo taisykles naudodami programą, pasirinkite **Nustatymas**. Susiejimo **taisyklės nustatymo skirtuke** galimos keturios pasirinktys:

- Juridinis subjektas 
- Tiekėjo paskyra 
- Prekės susiejimas 
- Išlaidų tipas

Pvz., pasirenkate juridinio **subjekto susiejimo taisyklių parinktį**. Juridinio subjekto kodas bus identifikuotas naudojant įmonės pavadinimą, adresą ir mokesčių registracijos numerį. Taisyklės, kuri pavadinta **LE-USPM**, atveju, jei įmonės pavadinime yra tekstas "Contoso Robotics USA", juridinio subjekto kodas bus **USPM**.

Puslapyje rodomos visos aktyvios susiejimo taisyklės. Jei norite peržiūrėti neaktyvias susiejimo taisykles, pasirinkite Aktyvus susiejimo **juridinio** subjekto taisyklės, **tada pasirinkite Neaktyvaus susiejimo juridinio subjekto taisyklės**.

Toliau pateikiami veiksmai pasiekiami, kad būtų galima susieti taisykles.

### <a name="create-a-mapping-rule"></a>Susiejimo taisyklės kūrimas

Susiejimo taisyklei sukurti galite naudoti du metodus:

- Norėdami **sukurti naują** susiejimo taisyklę, pasirinkite Naujas. Tada įveskite susiejimo taisyklės informaciją. Kiekvieno **susiejimo** taisyklės tipo taisyklės pavadinimo vertė turi būti unikali.
- Jei pasirinksite esamą susiejimo taisyklę, bus galima **naudoti** mygtuką Kopijuoti. Pasirinkite ją, tada rodomame **dialogo** lange pasirinkite Gerai. Susiejimo taisyklė sukuriama d sukuriama dėsant pasirinktos taisyklės teisę.

### <a name="edit-a-mapping-rule"></a>Susiejimo taisyklės redagavimas

Norėdami redaguoti susiejimo taisyklę, pasirinkite lauką ir pakeiskite vertę.

### <a name="activatedeactivate-mapping-rules"></a>Aktyvinti / išjungti susiejimo taisykles

Norėdami išjungti vieną ar daugiau susiejimo taisyklių, pasirinkite jas aktyvaus **susiejimo taisyklių** puslapyje, tada pasirinkite **Išjungti**. Taisyklės perkeliamos iš aktyvių susiejimo **taisyklių puslapio** į neaktyvaus **susiejimo taisyklių** puslapį.

Taip pat norėdami suaktyvinti susiejimo taisykles, pasirinkite jas neaktyvaus **susiejimo taisyklių** puslapyje, tada pasirinkite **Aktyvinti**.

### <a name="remove-mapping-rules"></a>Pašalinti susiejimo taisykles

Norėdami pašalinti susiejimo taisykles, pasirinkite jas, tada – **Naikinti**.

### <a name="check-for-conflicts"></a>Tikrinti, ar yra nesuderinamumų

Jei dviejų **susiejimų** **taisyklių** juridinio subjekto ir tiekėjo sąskaitos vertės yra tokios pačios, **bet** skiriasi prekės pavadinimo reikšmės, bus aptiktas konfliktas, o susiejimo taisyklė nebus sukurta ar atnaujinta.

## <a name="importexport-mapping-rules-from-excel"></a>Importuoti / eksportuoti susiejimo taisykles iš Excel

"Excel" priedą galima naudoti norint tvarkyti paketo taisykles. Galimos toliau nurodytos parinktys:

- Atsisiųskite "Excel" šabloną.
- Eksportuoti į Excel.
- Importuoti iš Excel.

### <a name="download-an-excel-template"></a>"Excel" šablono atsisiuntimas

Norėdami atsisiųsti "Excel" šabloną, pasirinkite Atsisiųsti **šabloną**. Tada pasirinkite laukus, kuriuos norite įtraukti į šabloną.

### <a name="export-to-excel"></a>Eksportuoti į Excel

Galite eksportuoti dviem būdais:

- Pasirinkite Atidaryti **programoje "Excel Online",** kad atidarytumėte failą programoje "Excel". Tada galėsite redaguoti rinkmeną tinkle. Jums pabaigus, pasirinkite **Įrašyti**. Visi jūsų pakeitimai bus įrašyti susiejimo **taisyklės** puslapyje.
- Pasirinkite Atsisiųsti **darbalapį,** kad atsisiųstumėte "Excel" failą, kuriame yra susiejimo taisyklės. Tada galite redaguoti failą. Baigę pasirinkite Importuoti iš Excel, kad būtų **įkeltas** atnaujintas darbalapis.

### <a name="import-from-excel"></a>Importuoti iš Excel

1. Pasirinkite **Importuoti iš Excel,** kad importuokite duomenis iš XLSX failo. Taip pat galite importuoti iš kableliu atskirtų verčių (CSV) ar XML failų. Prieš importuodami turite nuspręsti, ar leidžiami dublikatai.
2. Pasirinkite **Peržiūros susiejimas**, kad peržiūrėtumėte atributų susiejimą ir nustatytumėte, ar jis teisingas. Galite modifikuoti susiejimo ryšį.
3. Baigę pasirinkite Baigti importavimą, kad **pradėtumėte** importuoti.
4. Galite pasirinkti Sekti **procesą,** kad būtų sekama importavimo proceso eiga.

    Importavimo būsena atnaujinama iš Baigti **į** **Išanalizuota**, tada į **Transformacija** ir galiausiai – į **Baigta**.

Kai importavimo procesas yra baigtas, rodoma sėkmės, dalinių trikčių, klaidų ir bendro apdoroto kiekio statistika.
