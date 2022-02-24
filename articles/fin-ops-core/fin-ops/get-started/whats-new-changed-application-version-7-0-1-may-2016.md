---
title: Kas nauja ar pasikeitė „Dynamics AX“ 7.0.1 versijoje (2016 m. gegužės mėn.)
description: Šiame straipsnyje aprašomos naujos ir pakeistos 7.0.1 programos „Microsoft Dynamics AX“ versijoje veikiančios funkcijos. Ši versija buvo išleista 2016 m. gegužės mėn. ir jos versijos numeris yra 7.0.1265.23014.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 17067ff534e0e3f4636d7a307563128db55cf2ba
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797169"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a>Kas nauja ar pasikeitė „Dynamics AX“ 7.0.1 versijoje (2016 m. gegužės mėn.)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos naujos ir pakeistos 7.0.1 programos „Microsoft Dynamics AX“ versijoje veikiančios funkcijos. Ši versija buvo išleista 2016 m. gegužės mėn. ir jos versijos numeris yra 7.0.1265.23014.

## <a name="electronic-reporting-er"></a>Elektroninė ataskaita (ER)

| Ką galite daryti? | Kodėl tai svarbu? |
|------------------|------------------------|
| Sukonfigūruokite elektroninė perdavimo ataskaitų (ER) kūrimo apdorojimo laiko dialogo langą, kad vartotojai galėtų pasirinkti norimas finansines dimensijas. | Apdorojimo metu ER ataskaitos apdorojimo dialogo lange vartotojai gali pasirinkti kelias finansines dimensijas. Pasirinktų finansinių dimensijų išsami informacija bus rodoma sugeneruotame elektroniniame dokumente. |
| Kai kuriate ER ataskaitą, sukonfigūruokite prieigą prie kelių finansinių dimensijų, nustatydami vieną susiejimą su norimo duomenų šaltiniu. | Tą pačią ER ataskaitos konfigūraciją galima naudoti generuojant elektroninius dokumentus, kuriuose pateikiami operaciniai duomenys ir išsami informacija apie finansines dimensijas, nepriklausomai nuo vartotojo pasirinktų arba dabartiniam juridiniam subjektui ar egzemplioriui sukonfigūruotų finansinių dimensijų skaičiaus. |
| Konfigūruokite ER ataskaitą, kad jį duomenis įvestų į OPENXML darbalapio formatu sukurto elektroninio dokumento dinamiškai sugeneruotus stulpelius. | ER ataskaita gali įvesti duomenis į sugeneruotą OPENXML darbalapį horizontaliai pakeisdama stulpelius. Todėl pakartotinai naudojant tą pačią ER ataskaitos konfigūraciją galima generuoti elektroninius dokumentus, kurie turi skirtingą dinamiškai sugeneruotų stulpelių skaičių. |
| Konfigūruokite ER paskirties vietas, kad formato išeigos rezultatas būtų nukreiptas į konkrečią paskirties vietą: failą, el. pašto adresą arba archyvą („Microsoft SharePoint“ aplanką arba „Microsoft Azure“ saugyklą). | Anksčiau paleidžiant ER konfigūraciją pasirodydavo pranešimo langas, nurodantis vartotojui failą įrašyti arba atidaryti. Dabar kiekvienos formato konfigūracijos ir kiekvienos komponento paskirties vietą (aplanką arba failą) galite iš anksto sukonfigūruoti atskirai. Vartotojai, turintys reikiamas teises, paskirties vietos parametrus gali taip pat keisti apdorojimo metu. |

## <a name="pos--microsoft-dynamics-ax-retail"></a>EKA – „Microsoft Dynamics AX Retail“

| Ką galite daryti? | Kodėl tai svarbu? |
|------------------|------------------------|
| Naudokite naršyklę „Google Chrome“. | Dabar mažmenininkai debesies EKA gali paleisti naršyklėje „Chrome“ ir naudoti visas funkcijas, kurios yra debesies EKA „Microsoft Edge“ ir „Internet Explorer“ versijose. |

## <a name="financial-reporting"></a>Finansinės ataskaitos

| Ką galite daryti? | Kodėl tai svarbu? |
|------------------|------------------------|
| Atstatykite finansinių ataskaitų duomenų sritį. | Kai „Dynamics AX“ duomenų bazes perkeliate iš vienos aplinkos į kitą arba atliekate kitus esminius aplinkos pakeitimus, finansinių ataskaitų duomenų bazę gali tekti kurti iš naujo. Nuo šiol „Windows PowerShell“ scenarijus teikiamas duomenų bazei kurti iš naujo. |
| Daugiau nebegalite pasirinkti ataskaitų dizaino įrankio parinkčių, kurios negalioja. | Kelios ataskaitų kūrimo parinktys, kurios buvo naudojamos rinkoje esančiose „Management reporter“ versijose, šioje „Dynamics AX“ versijoje netaikomos. Šios parinktys buvo susijusios su finansinių ataskaitų kūrimu, išvedamais duomenimis ir susiejimu. Šios parinktys buvo pašalintos iš finansinių ataskaitų dizaino įrankio, kad vartotojai nedarytų klaidų. |

## <a name="financial-management"></a>Finansų valdymas

| Ką galite daryti? | Kodėl tai svarbu? |
|------------------|------------------------|
| Generuokite mokėtinų sumų mokėjimų teigiamo mokėjimo failus. | Galima generuoti teigiamo mokėjimo failus, kad bankai galėtų lengviau išvengti su čekiais susijusio sukčiavimo. |

## <a name="warehouse-and-production"></a>Sandėlis ir gamyba

<table>
<thead>
<tr>
<th>Ką galite daryti?</th>
<th>Kodėl tai svarbu?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nustatykite sandėlio darbo strategiją, kuri kontroliuoja produktų rinkinio darbo kūrimą konkrečiose vietose.</td>
<td>Sandėlio procesai ne visada apima darbą. Naudodami naująją sandėlio darbo strategiją, galite neleisti konkrečiose vietose kurti tam tikro produktų rinkinio žaliavų paėmimo ir pagamintų prekių padėjimo darbo.</td>
</tr>
<tr>
<td>Nurodykite, kad gamybos išeigos vieta nėra kontroliuojama pagal numerio lentelę.</td>
<td>Dabar galite nurodyti, kad produktų išeigos vieta nėra kontroliuojama pagal numerio lentelę. Pavyzdžiui, ši funkcija yra naudinga, kai pirminės gamybos užsakymas ataskaitą apie baigtas prekes pateikia tiesiai toje vietoje, kuri naudojama kaip tolesnio gamybos užsakymo gamybos išeigos vieta.</td>
</tr>
<tr>
<td>Teikite pagalbą KS, kuriose yra prekių, turinčių skirtingas tos pačios prekės produktų dimensijas.</td>
<td>Gamyboje naudodami vieną ar kelias produkto dimensijas, gali būti atvejų, kai jūs norėsite prekę gaminti pagal kitą tos pačios prekės variantą. Daugiau informacijos žr. <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">šiame tinklaraštyje</a>.</td>
</tr>
<tr>
<td>Gamybos užsakymai, kurių cikliškumo struktūros yra pirmame KS lygyje, nėra įtraukiamos į materialiųjų išteklių planavimo KS lygio skaičiavimą.</td>
<td>Produkto variantams priskirti teisingų KS lygių neįmanoma, jei pasirinkti gamybos užsakymai yra KS hierarchijos cikliškumo priežastis.</td>
</tr>
<tr>
<td>Apskaičiuokite atskirus materialiųjų išteklių planavimo ir išlaidų apskaičiavimo KS lygius.
<ul>
<li>Materialinių išteklių planavimo KS lygiai yra apskaičiuojami naujoje lentelėje <strong>ReqItemLevel</strong>. Baigti gamybos užsakymai į skaičiavimą neįtraukiami.</li>
<li>Gamybos išlaidų skaičiavimo KS lygiai yra apskaičiuojami lentelėje <strong>InventTable</strong>. Baigti gamybos užsakymai įtraukiami į skaičiavimą.</li>
</ul>
</td>
<td>
<ul>
<li>Vykdant materialiųjų išteklių planavimą, pvz., bendrojo planavimo plano planavimą ir išskleidimą, reikia perskaičiuoti tik materialiųjų išteklių planavime naudojamus KS lygius. Kitaip tariant, gamybos išlaidų skaičiavime naudojamų KS lygių skaičiuoti nereikia.</li>
<li>Vykdant išlaidų operacijas, pvz., atsargų uždarymą, reikia perskaičiuoti tik gamybos išlaidų skaičiavime naudojamus KS lygius.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildomi ištekliai

[Kas nauja ar pasikeitė „Finance and Operations“ pagrindiniame puslapyje](whats-new-changed.md)

[Nauji ar atnaujinti užduočių vedliai (2016 m. gegužės mėn.)](new-updated-task-guides-available-may-2016.md)
