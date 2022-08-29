---
title: Kasos aparato funkcionalumas Norvegijai
description: Šiame straipsnyje pateikta grynųjų pinigų registro funkcijų, kurios galimos Norvegijai Microsoft Dynamics 365 Commerce, apžvalga ir pateikiamos funkcijos nustatymo rekomendacijos.
author: EvgenyPopovMBS
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-10-31
ms.openlocfilehash: 30bd5ad8c1513c3d56cc4aa0a77b70fe38d31e0a
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346024"
---
# <a name="cash-register-functionality-for-norway"></a>Kasos aparato funkcionalumas Norvegijai

[!include[banner](../includes/banner.md)]

Šiame straipsnyje pateikta grynųjų pinigų registro funkcijų, kurios galimos Norvegijai, apžvalga Dynamics 365 Commerce. Taip pat pateikiami funkcijų nustatymo nurodymai. Funkcijas sudaro šios dalys:

- Bendrosiose kasos kasos įstaigose (EKA) priemonės, kurias gali naudoti klientai visose šalyse arba regionuose. Pavyzdžiai apima pasirinktį, kuri leidžia daugiau nei vieną kartą neleisti spausdinti kvito kopijos.
- Specifinės Norvegijos funkcijos, pavyzdžiui, pardavimo operacijų skaitmeniniai parašai.

## <a name="overview-of-cash-register-functionality-for-norway"></a>Norvegijos grynųjų pinigų registro funkcijų apžvalga

### <a name="common-pos-features"></a>Bendrosios EKA funkcijos

Norėdami sužinoti apie EKA priemones, kurios galimos klientams visose šalyse ar regionuose, žr. [žinyno išteklius Dynamics 365 Retail](../index.md).

Šios EKA lokalizavimo priemonės, kurios anksčiau buvo įdiegtos ir galimos klientams visose šalyse ar regionuose, dabar gali būti naudojamos konkrečiai Norvegijai:

- **Kvite spausdinti didelio šrifto teksto laukus.** Norėdami nurodyti, kad **didelis šrifto** dydis turi būti naudojamas kvito formato lauke, galite naudoti parametrą Šrifto dydis kvito formato konstruktoriuje. (Didelis šrifto dydis yra maždaug padvigubęs už įprastą šrifto dydį.) Pavyzdžiui, šį parametrą galite naudoti, jei ant kvito kopijos didelius simbolius norite spausdinti indikatorių "Kopijuoti".
- **Užregistruokite kvitų kopijų spausdinimą EKA audito įvykių žurnale.** EKA funkcijų **profilyje** galite naudoti parametrą Auditas, norėdami įgalinti kvitų kopijas spausdinti ir kitus EKA audito įvykius registruoti. Audito įvykiai registruojami kanalų duomenų bazėje ir būstinėje. Audito įvykius galite peržiūrėti audito **įvykių** puslapyje.
- **Neleiskite kvito kopiją spausdinti daugiau nei vieną kartą.** **Kai EKA** funkcijų profilyje įgalintas audito parametras, **teisės** Leisti spausdinti kvitų kopijų EKA kontroliuoja, ar galima spausdinti kvitų kopijas. Yra ir parinktis, leidžianti daugiau nei vieną kartą išvengti kvito kopijos spausdinimo.

Be to, Norvegijai buvo įdiegta ši EKA funkcija, bet ji prieinama klientams visose šalyse ar regionuose:

- **Užregistruokite papildomus įvykius EKA audito įvykių žurnale.** **Jei EKA** funkcijų šablone įgalintas audito parametras, EKA audito įvykių žurnale užregistruojami šie įvykiai:

    - Kainos tikrinimai
    - Mokesčių perrašymai
    - Eilutės kiekių koregavimai
    - Valo operacijas iš kanalų duomenų bazės

### <a name="norway-specific-pos-features"></a>Specifinė Norvegijos EKA priemonės

Šios Norvegijos EKA priemonės įgalintos, kai **ISO** kodo parametras EKA funkcijų profilyje nustatytas kaip **Ne**.

#### <a name="digital-signing-of-sales-transactions"></a>Skaitmeninis pardavimo operacijų pasirašymas

Kiekviena pardavimo operacija pasirašyta skaitmeniniu būdu. Parašas sukuriamas ir įrašomas EKA operacijų žurnale tuo pat metu, kai operacija baigiama. Parašas taip pat prieinamas žurnale, kuris eksportuojamas audito tikslais.

Pasirašomos tik pardavimo grynaisiais pinigais operacijos. Štai keletas operacijų, neįtrauktų į pasirašymo procesą, pavyzdžių:

- Išankstiniai mokėjimai (kliento sąskaitos depozitas)
- Pardavimo užsakymų išankstiniai mokėjimai (kliento užsakymo depozitas)
- Dovanų kortelės išdavimas
- Ne pardavimo operacijos (float entry, mokėjimo priemonės šalinimas ir taip toliau)

Pasirašyti duomenys yra teksto eilutė, kurią sudaro šie duomenų laukai. Duomenų laukai atskiriami kabliataškiais.

1. Ankstesnis to paties EKA parašas (pirmai \[**operacijai naudojamas nulis 0**\] .)
2. Operacijos data
3. Operacijos laikas
4. Nuoseklus pasirašytas operacijos numeris
5. Operacijos suma su mokesčiu
6. Operacijos suma be mokesčių

Skaitmeninio pasirašymo procese naudojamas RSA 1024 bitų raktas, kuris turi SHA-1 funkciją (RSA-SHA1-1024). Sertifikatas, įdiegtas "Commerce Scale Unit", naudojamas pasirašant. Unikalus sertifikato (pėdos atspaudo) identifikatorius įrašomas kartu su parašu.

Parašas saugomas parduotuvės duomenų bazėje ir būstinės (HQ) duomenų bazėje kartu su operacijų duomenimis. Galite peržiūrėti operacijos parašą ir operacijos duomenis, kurie buvo naudojami jį generuojant, **parduotuvės** operacijų puslapio "FastTab **" Iždo operacijos**.

#### <a name="receipts"></a>Kvitai

Norvegijos kvituose gali būti papildomos informacijos, kuri buvo įdiegta naudojant pasirinktinius laukus:

- **Kvito** pavadinimas – kvito formatui galima pridėti lauką prie kvito formato maketo, kad būtų galima identifikuoti kvito tipą. Pavyzdžiui, pardavimo kvite bus tekstas "Pardavimo kvitas".
- **Pasirašiusios operacijos sekos numeris** – nuoseklus pasirašytų operacijų numeris gali būti rodomas kvite, kad išspausdintas gavimas būtų susietas su skaitmeniniu parašu duomenų bazėje.
- **Bendrosios gavimo sumos** – pasirinktiniai kvitų bendrųjų sumų laukai neįtraukia pardavimo sumų iš bendrųjų operacijų sumų. Ne pardavimo sumos apima šių operacijų sumas:

    - Išankstiniai mokėjimai (kliento sąskaitos depozitas)
    - Pardavimo užsakymų išankstiniai mokėjimai (kliento užsakymo depozitas)
    - Dovanų kortelės išdavimas
    - Lėšų įtraukimas į dovanų kortelę

#### <a name="x-and-z-reports"></a>X ir Z ataskaitos

Informacija, įtraukta į X ir Z ataskaitas, pagrįsta Norvegijos reikalavimais. Pvz., bendrosios **pardavimo grynaisiais** pinigais sumos apima tik pardavimo grynaisiais operacijų sumas, bet neįeiti dovanų kortelės išdavimo operacijų ir išankstinių mokėjimų. Bendras pardavimas grynaisiais pinigais taip pat pateikiamas prekių grupei ir mokėjimo būdui. Be to, tvarkomos **ir spausdinamos** kaupiamosios **bendrosios bendrosios** pardavimo sumos ir bendrosios grąžinimo sumos.

#### <a name="saf-t-cash-register-audit-file"></a>PST-T kasos aparato audito failas

EKA operacijų žurnalą galite eksportuoti iš anksto nustatytu standartiniu audito failu – mokesčiai (-T) grynųjų pinigų registro formatu. Audito faile yra informacija apie organizaciją, susijusius pagrindinius duomenis (pvz., prekių grupes, prekes ir mokesčių kodus), grynųjų pinigų pardavimo operacijos duomenis kartu su šių operacijų parašais, ne pardavimo įvykių duomenis ir datų pabaigos ataskaitos duomenis.

Audito failą galima eksportuoti, kai:

- Vienai parduotuvei
- Visos parduotuvės
- Mokėjimo terminalui
- Visi terminalai

Taip pat galite siųsti ataskaitą iš vieno juridinio subjekto kito juridinio subjekto vardu. Tokiu atveju turite vykdyti eksportą iš veikiančių juridinių subjektų ir nurodyti ataskaitų juridinį subjektą kaip ataskaitos siuntėją.

VZ.-T kasos aparato formatas įdiegtas "Headquarters" naudojant elektronines [ataskaitas](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md). 

## <a name="setting-up-commerce-for-norway"></a>Norvegijos "Commerce" nustatymas

Šiame skyriuje aprašomi Norvegijai tinkami ir rekomenduojami parametrai. Daugiau informacijos ieškokite žinyno [išteklių Dynamics 365 Retail](../index.md).

Norėdami naudoti Norvegijai brastos funkcijos, turite atlikti šias užduotis:

- Nustatykite **lauką Šalis/regionas** **KAIP NOR** (Norvegija) juridinio subjekto pirminiu adresu.
- Kiekvienos parduotuvės **, kuri yra** Norvegijoje **, ISO kodo lauką nustatykite kaip NO** (Norvegija) EKA funkcijų šablone.

Taip pat turite nurodyti šiuos Norvegijos parametrus.

### <a name="enable-features-for-norway"></a>Įjungti Norvegijos funkcijas

"Commerce Headquarters" funkcijų valdymo **darbo** srityje turite įgalinti šias funkcijas:

- (Norvegija) Įjungti papildomus audito įvykius EKA
- (Norvegija) Įjungti papildomą informaciją EKA dienos pabaigos ataskaitose

### <a name="set-up-the-legal-entity"></a>Nustatyti juridinį subjektą

Įsitikinkite, kad nurodytas juridinio subjekto pavadinimas. Šis vardas bus spausdinamas X ir Z ataskaitose.

Be to, banko sąskaitos **informacijos** "FastTab", lauke **Banko** kodas, nurodykite organizacijos numerį.

### <a name="set-up-value-added-tax-vat-per-norwegian-requirements"></a>Nustatyti pridėtinės vertės mokestį (PVM) pagal Norvegijos reikalavimus


Turite sukurti PVM kodus, PVM grupes ir prekės PVM grupes. Taip pat turite nustatyti produktų ir paslaugų PVM informaciją. Daugiau informacijos apie tai, kaip nustatyti ir naudoti PVM, ieškokite [PVM peržiūra.](../../finance/general-ledger/indirect-taxes-overview.md)

Taip pat turite nurodyti PVM grupes ir įgalinti parinktį **Kainos su PVM**, taikoma parduotuvėms, kurios yra Norvegijoje.

### <a name="set-up-functionality-profiles"></a>Funkcijų šablonų nustatymas

Turite įgalinti auditą ir nustatyti kvitų numeravimą.

### <a name="update-pos-permissions-groups-and-individual-permission-settings-for-store-workers"></a>Naujinti parduotuvės darbuotojų EKA teisių grupes ir atskirus teisių parametrus

Nustatykite **atitinkamą teisės spausdinti kvito** kopiją reikšmę:

- **Visada leisti** – operatorius gali kelis kartus spausdinti kvito kopiją.
- **Leisti tik vieną** kartą – operatorius gali kvito kopiją spausdinti tik vieną kartą.
- **Leisti tik vieną kartą, o tik jei HQ DB** galimas – operatorius gali kvito kopiją spausdinti tik vieną kartą, o tik jei HQ Commerce Data Exchange duomenų bazė pasiekiama per : "Real-time Service", kad sistema galėtų patikrinti, ar bet kurioje parduotuvėje anksčiau nebuvo išspausdintos kvito kopijos.
- **Niekada** – operatorius negali spausdinti kvito kopijos.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Konfigūruoti pasirinktinius laukus, kad juos būtų galima naudoti pardavimo kvitų kvitų formatuose

Kalbos teksto **puslapyje** pridėkite šiuos kvitų maketų pasirinktinių laukų žymių įrašus. Atkreipkite dėmesį **, kad** lentelėje **pateiktos kalbos ID,** **teksto ID** ir teksto vertės yra tik pavyzdžiai. Juos galite pakeisti, kad jie atitiktų jūsų poreikius.

| Kalbos ID | Tekstas                   | Teksto ID |
|-------------|------------------------|---------|
| lt       | Kvito pavadinimas          | 900011  |
| lt       | Ar yra dovanų kortelė           | 900012  |
| lt       | Iš viso (pardavimas)          | 900013  |
| lt       | Bendra mokesčių suma (pardavimas)      | 900014  |
| lt       | Iš viso su mokesčiais (pardavimas) | 900015  |
| lt       | Mokesčių suma (pardavimas)     | 900016  |
| lt       | Operacijos grynaisiais pinigais ID    | 900017  |

Pasirinktinių **laukų puslapyje** pridėkite šiuos įrašus prie kvitų maketų pasirinktinių laukų. Atkreipkite **dėmesį, kad antraštės teksto ID** reikšmės turi **atitikti teksto ID** vertes, kurias nurodėte kalbos **teksto** puslapyje.

| Vardas                            | Tipas    | Vaizdo aprašo teksto ID |
|---------------------------------|---------|-----------------|
| Gavimo pavadinimas                    | Gavimas | 900011          |
| IsGiftCard                      | Gavimas | 900012          |
| SalesTotalExt                   | Gavimas | 900013          |
| TaxTotalExt kodas                     | Gavimas | 900014          |
| TotalWithTaxExt                 | Gavimas | 900015          |
| AmountPerTaxExt                 | Gavimas | 900016          |
| CashTransactionSequentialNumber | Gavimas | 900017          |

> [!NOTE]
> Svarbu nurodyti teisingus pasirinktinius laukų pavadinimus, kaip pateikta pirmiau pateiktoje lentelėje. Neteisingas pasirinktinio lauko pavadinimas gali sukelti kvitų duomenų.

### <a name="configure-receipt-formats"></a>Kvitų formatų konfigūravimas

Pakeiskite visų reikalingų kvitų formatų lauko Spausdinti veikimo būdą **reikšmę** **į Visada spausdinti kvito** formate.

Kvitų formato dizaineryje į atitinkamus kvitų skyrius įtraukite šiuos pasirinktinius laukus. Nepamirškite, kad laukų pavadinimai atitinka ankstesniame skyriuje jūsų apibrėžtus kalbos tekstus.

1. Antraštės:

    - **Kvito** pavadinimas – šis laukas nurodo gavimo tipą.
    - **Grynųjų operacijos ID** – šiame lauke spausdinamas pasirašiusių grynųjų pinigų operacijų sekos numeris.

2. Eilutės:

    - **Yra dovanų kortelė** – šis laukas pažymi kvito eilutę kaip susijusią su dovanų kortelės išdavimu arba pridėjimu prie dovanų kortelės operacijos.

3. Poraštės:

    - **Bendroji suma (pardavimas)** – šiame lauke išspausdinta bendroji kvito grynųjų pinigų pardavimo suma. Į sumą neįtraukti mokesčiai. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
    - **Bendroji mokesčio suma** (pardavimas) – šiame lauke spausdinamas bendroji kvito mokesčių suma, skirta pardavimui grynaisiais pinigais. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
    - **Bendroji suma su mokesčiu (pardavimas)** – šiame lauke spausdinamas bendroji kvito pardavimo suma. Į sumą įtrauktas mokestis. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.
    - **Mokesčio suma (pardavimas)** – šiame lauke spausdinamas kvito mokesčių kiekis, skirtas grynųjų pinigų PVM kodui. Išankstiniai mokėjimai ir dovanų kortelių operacijos neįtraukiamos.

Daugiau informacijos apie tai, kaip dirbti su kvitų formatais, ieškokite [Gavimo kvitų formatų nustatymas ir kūrimas](../receipt-templates-printing.md).

### <a name="configure-the-saf-t-cash-register-export-format"></a>Konfigūruoti BŪTI-T grynųjų pinigų registro eksportavimo formatą

NEPAVYKO-T grynųjų pinigų registro konfigūraciją galima atsisiųsti iš Microsoft Dynamics ciklo tarnybų (LCS). Daugiau informacijos rasite Importuokite [elektroninių ataskaitų konfigūracijas](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-import-ger-configurations.md). Turite atsisiųsti šias konfigūracijas:

- **Mažmeninės prekybos kanalo data.version.1** – duomenų modelio konfigūravimas.
- **DMM "Retail" kanalo data.version.1.14** – duomenų modelio susiejimo konfigūracija.
- **NOVZ., Grynųjų pinigų registras.versija.1.20** – formato konfigūracija.

Importavote konfigūracijas, **·** **skirtuko** Elektroniniai dokumentai puslapyje Commerce Parameters, **laukeVZ-T Grynųjų pinigų registro eksportavimo formatas** pasirinkite importuotos formato konfigūracijos pavadinimą.

Taip pat turite susieti reikiamus pagrindinius duomenis su iš anksto nustatytaisVZ.-T standartiniais kodais. Daugiau informacijos ieškokite NORVEGIJOS mokesčių inspekcijos teikiameVZ-T kasos aparato dokumentuose. Norėdami sukurti susiejimą, turite nustatyti naują **YRA-T grynųjų pinigų registro kodo** lauką šiame puslapyje:

- Prekių grupės
- Mokėjimo būdai
- PVM kodai

### <a name="configure-channel-components"></a>Konfigūruoti kanalo komponentus

Norėdami įgalinti Specifinės Norvegijos funkcijas, turite sukonfigūruoti kanalo komponentus. Norėdami gauti daugiau informacijos, žr. [diegimo rekomendacijas](emea-nor-fi-deployment.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
