---
title: "Nukrypimų grupės"
description: "Šioje temoje aprašoma, kaip naudojamos srities Laikas ir buvimas darbe nukrypimų grupės."
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgFlexGroup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: e21a2de2f46c619f27eddad4d7cced260a90bbb8
ms.openlocfilehash: 20f317ff57fac25b5b5b0d702fe64845eb849e87
ms.contentlocale: lt-lt
ms.lasthandoff: 04/09/2018

---

# <a name="flex-groups"></a>Nukrypimų grupės

[!include[banner](../includes/banner.md)]

Pasinaudodamos kintamomis darbo valandomis įmonės gali sumažinti mokėjimus už viršvalandžius ir pasiūlyti darbuotojams papildomo laisvo laiko pertraukų metu, kai sumažėja darbo krūvis. Ši funkcija svarbi tuose segmentuose, kuriems, pavyzdžiui, būdingi sezoniniai darbo krūvio pokyčiai.

Naudodamiesi nukrypimų grupėmis galite nustatyti toliau nurodytas kintamų darbuotojo valandų taisykles ir principus.

- Nukrypimų reglamentavimo taisyklės
- Darbuotojo nukrypimo balanso skaičiavimo principas

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Nukrypimų grupių kintamų darbo valandų nustatymas

- Pasirinkite **Laikas ir buvimas darbe** \> **Sąranka** \> **Grupės** \> **Nukrypimų grupės** ir nustatykite kintamomis valandomis dirbančias nukrypimų grupes.

## <a name="associate-workers-with-flex-groups"></a>Darbuotojų susiejimas su nukrypimų grupėmis

- Pasirinkite **Laikas ir buvimas darbe** \> **Sąranka** \> **Laiko registracijos darbuotojai**.

## <a name="rules-for-flex-regulations"></a>Nukrypimų reglamentavimo taisyklės

Naudodamiesi nukrypimų reglamentavimo taisyklėmis galite nurodyti nukrypimo ribas arba minimalų ir maksimalų leidžiamą darbuotojo nukrypimo sąskaitos valandų skaičių. Nustatomos nukrypimo grupės nukrypimo ribos. Viršijus nukrypimo ribas galima pakoreguoti darbuotojo nukrypimo balansą ir užmokestį.

Viršijus leidžiamą minimalų darbuotojo nukrypimą (t. y. jei nukrypimo sąskaitos valandų skaičius yra mažesnis nei nurodytas minimalus skaičius) naudojantis toliau nurodytais būdais ir sukuriant nukrypimo taisyklę galima koreguoti darbuotojo nukrypimo balansą.

- Darbuotojo nukrypimo sąskaitą galima koreguoti iki nurodyto leidžiamo minimalaus skaičiaus, bet neatimant darbuotojo užmokesčio už tokį valandų skaičių, kad nukrypimo sąskaitoje esanti suma taptų mažesnė negu minimali leistina suma.
- Iš darbuotojo darbo užmokesčio gali būti atskaičiuojamas toks skaičius valandų, kad nukrypimo sąskaitoje esanti suma taptų mažesnė negu minimali leistina suma. Šis atskaitymas atliekamas sukuriant konkretaus mokėjimo tipo elementus, turinčius neigiamą arba teigiamą mokėjimo vienetą.

Viršijus leidžiamą minimalų darbuotojo nukrypimą naudojantis toliau nurodytais būdais ir sukuriant nukrypimo taisyklę galima koreguoti darbuotojo nukrypimo balansą.

- Darbuotojo nukrypimo sąskaitą galima koreguoti vėl nustatant nurodytą leidžiamą maksimalų skaičių, bet nekompensuojant darbuotojo užmokesčio už tokį valandų skaičių, kada darbuotojas dirbo ilgiau negu nurodytą maksimalų leidžiamą valandų skaičių.
- Valandų skaičių, kada darbuotojas dirbo ilgiau negu nurodytą maksimalų leidžiamą valandų skaičių, galima paversti užmokesčiu. Tai atliekama sukuriant konkretaus mokėjimo tipo elementus.

Nukrypimo balansą galite koreguoti toliau nurodytu metu.

- Kai algalapio duomenimis grįstas užmokesčio failas eksportuojamas naudojantis užduotimi **Perkelti darbo užmokestį**. Algalapop duomenys sukuriami iš puslapio **Patvirtinimas** perkėlus darbuotojo registraciją.
- Apdorojus užduotį **Koreguoti nukrypimo balansą**.

> [!NOTE]
> Nukrypimo taisyklės nesukuriamos atliekant kasdienį patvirtinimą ir puslapyje **Patvirtinimas** perkeliant darbuotojo registracijas.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Darbuotojo nukrypimo balanso skaičiavimo principas

Valandų, pagal kurias koreguojamas darbuotojo nukrypimo balansas, apskaičiavimo principą nustato nukrypimo grupė. Pasirinkite **Laikas ir buvimas darbe** \> **Sąranka** \> **Grupės** \> **Nukrypimų grupės**. 

Gali būti naudojami du toliau nurodyti principai.

- **Laikas** – darbuotojo kintamos valandos skaičiuojamos tik pagal užregistruotą darbuotojo dienos laiką. Apskaičiavus darbuotojo dienos registracijas dienos Nukrypimas+ ir Nukrypimas- valandų skaičius apskaičiuojamas pagal darbuotojo laiko šablone nurodytas zonas Nukrypimas+ ir Nukrypimas-.
- **Mokėjimo tipai** – kintamos darbuotojo valandos skaičiuojamos pagal darbuotojo mokėjimo sutartyje nurodytų Nukrypimas+ ir Nukrypimas- mokėjimo tipų uždarbius. Mokėjimo sutartis susieta su laiko registracijos darbuotoju. Jei, pavyzdžiui, vienoje ar keliose nukrypimo zonose norite padidinti darbuotojo nukrypimo sąskaitą tam tikru koeficientu, galbūt norėsite nukrypimo sąskaitas tvarkyti naudodamiesi mokėjimo tipais.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>1 scenarijus: darbuotojo darbo užmokesčio ir nukrypimo sąskaitos koregavimas, nes viršytas leistinas minimalus nukrypimas

Laisvu grafiku galinčio dirbti darbuotojo nukrypimo sąskaita neigiama.

- **Nukrypimo sąskaita:** -4

Darbuotojas susietas su nukrypimų grupe, kurioje naudojamos toliau nurodytos konfigūracijos.

- **Minimalus nukrypimas:** -0,5
- **Minimalaus mokėjimo tipas:** 1302
- **Mokėjimo tipo faktorius:** -1,00

Pagal skirtumą tarp darbuotojo nukrypimo sąskaitos ir leidžiamo jo minimalaus nukrypimo paaiškėja, kad 3,5 valandos viršytas leidžiamas minimalus darbuotojo nukrypimas.

Algalapio administratoriui paleidus užduotį **Perkelti į užmokestį** arba **Nukrypimo koregavimas** ir perkėlus darbuotojo užmokesčio duomenis atliekami toliau nurodyti koregavimai.

- Darbuotojo nukrypimo sąskaita pakoreguojama 3,5 valandomis. Todėl -4,0 valandų nukrypimo balansas pakoreguojamas pagal -0,5 valandos leidžiamą minimalų darbuotojo nukrypimą.
- Sukuriamas mokėjimo tipo 1302 mokėjimo elementas. Šio mokėjimo elemento mokėjimo vieneto suma -3,5 valandos ir ši suma bus atimta iš darbuotojo darbo užmokesčio. Tokiu atveju mokėjimo vienetas yra neigiamas skaičius, nes teigiamas 3,5 valandos koregavimas dauginamas iš nukrypimų grupėje nurodyto neigiamo mokėjimo tipo koeficiento -1,0. Šis mokėjimo elementas bus įtrauktas į užduoties **Perkelti į užmokestį** sukurtą mokėjimo failą.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>2 scenarijus: darbuotojo darbo užmokesčio ir nukrypimo sąskaitos koregavimas, nes viršytas leistinas maksimalus nukrypimas

Laisvu grafiku galinčio dirbti darbuotojo nukrypimo sąskaita teigiama.

- **Nukrypimo sąskaita:** 6

Darbuotojas susietas su nukrypimų grupe, kurioje naudojamos toliau nurodytos konfigūracijos.

- **Maksimalus nukrypimas:** 2,0
- **Minimalaus mokėjimo tipas:** 1302
- **Mokėjimo tipo faktorius:** -1,0

Pagal skirtumą tarp darbuotojos nukrypimo sąskaitos ir leidžiamo jos maksimalaus nukrypimo paaiškėja, kad 4,0 valandomis viršytas leidžiamas minimalus darbuotojos nukrypimas.

Algalapio administratoriui paleidus užduotį **Perkelti į užmokestį** arba **Nukrypimo koregavimas** ir perkėlus darbuotojo užmokesčio duomenis atliekami toliau nurodyti koregavimai.

- Darbuotojo nukrypimo sąskaita pakoreguojama -4,0 valandomis. Todėl 6,0 valandų nukrypimo balansas pakoreguojamas pagal 2,0 valandų leidžiamą maksimalų darbuotojo nukrypimą.
- Sukuriamas mokėjimo tipo 1302 mokėjimo elementas. Šio mokėjimo elemento mokėjimo vieneto suma 4,0 valandos ir ši suma bus pridėta prie darbuotojo darbo užmokesčio. Tokiu atveju mokėjimo vienetas yra teigiamas skaičius, nes neigiamas 4,0 valandų koregavimas dauginamas iš nukrypimų grupėje nurodyto neigiamo mokėjimo tipo koeficiento -1,0. Šis mokėjimo elementas bus įtrauktas į užduoties **Perkelti į užmokestį** sukurtą mokėjimo failą.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>3 scenarijus: darbuotojo nukrypimo balanso tvarkymas pagal darbo užmokesčio tipus

Kaip jau paaiškinta pirmiau, nukrypimo sąskaitos gali būti tvarkomos pagal darbuotojo laiko šablone nurodytose laiko Nukrypimas+ ir Nukrypimas- zonose užsiregistruotą laiką arba pagal darbuotojo mokėjimo sutartyse nurodytus mokėjimo tipus. Jei naudojami mokėjimo tipai, darbuotojo nukrypimo sąskaita koreguojama pagal perkėlus darbuotojo registraciją iš puslapio **Patvirtinimas** sukuriamus mokėjimo elementus. Jei, pavyzdžiui, vienoje ar keliose nukrypimo zonose norite padidinti darbuotojo nukrypimo sąskaitą tam tikru koeficientu, galbūt norėsite nukrypimo sąskaitas tvarkyti naudodamiesi mokėjimo tipais.

Pagal šį scenarijų naudojamasi toliau nurodytu darbo dieną atitinkančiu nukrypimo šablonu.

| Šablono tipas  | Pradžios    | Pabaigoje      |
|---------------|----------|----------|
| Nukrypimas+         | 12:00 | 08:00 |
| Atėjimas į darbą      | 08:00 | 08:00 |
| Nukrypimas-         | 08:00 | 09:00 |
| Standartinis laikas | 09:00 | 11:30 |
| Apmokama pertrauka    | 11:30 | 12:00 |
| Nukrypimas-         | 12:00 | 04:00 |
| Išėjimas iš darbo     | 04:00 | 04:00 |
| Nukrypimas+         | 04:00 | 12:00 |

Tokiu atveju būtų geriau, jei darbuotojo nukrypimų balansą galėtumėte valdyti pagal mokėjimų tipus. Todėl turite nustatyti darbuotojo nukrypimo grupės srities **Pagal mokėjimo tipus** parinktį **Taip**.

Norėdami atsiskaityti už kintamas valandas, taip pat turite nurodyti naują mokėjimo tipą. Pagal šį scenarijų mokėjimo tipo pavadinimas **FlexCnt**.

| Mokėjimo tipas | aprašymas  |
|----------|--------------|
| FlexCnt  | Nukrypimo skaitiklis |

Po to atlikę toliau nurodytus veiksmus nustatykite mokėjimo tipą ir įtraukite naujo tipo mokėjimo eilutes į mokėjimo šabloną.

1. Pasirinkite **Laikas ir buvimas darbe** \> **Sąranka** \> **Grupės** \> **Nukrypimų grupės**, po to pasirinkite **Nauja**.
2. Laukuose **Nukrypimas+** ir **Nukrypimas-** nurodykite naują mokėjimo tipą **FlexCnt**.
3. Pasirinkite **Laikas ir buvimas darbe** \> **Sąranka** \> **Mokėjimo sutartys**, o po to pasirinkite **Sutarties eilutės**.
4. Įtraukite tris toliau nurodytas srities **Pirmadienis** šablono tipo **Nukrypimas+** eilutes.

    | Mokėjimo tipas | aprašymas  | Pradžios laikas | Pabaigos laikas  | Mažiausia | Didžiausia | Koeficientas |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Nukrypimo skaitiklis | 12:00  | 06:00 | 00,00   | 00,00   | 1,00   |
    | FlexCnt  | Nukrypimo skaitiklis | 06:00  | 12:00 | 00,00   | 02,00   | 1.50   |
    | FlexCnt  | Nukrypimo skaitiklis | 06:00  | 12:00 | 02,00   | 06,00   | 2,00   |

    > [!NOTE]
    > Kiekviena eilutė naudojama skirtingam laiko intervalui ir nurodyti skirtingi jų veiksniai. Kintamos valandos, kuriomis darbuotojas dirba laiko intervale, padauginamos iš tos eilutės koeficiento. Pvz., kai dirbama nuo 18:00 iki 20:00, šios darbo valandos padauginamos iš 1,50. Koeficientas nurodomas puslapio **Mokėjimo sutarties eilutės** skirtuko **Bendra** lauke **Koeficientas**.

Darbuotojas įveda toliau nurodytas dienos registracijas.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      |
|---------------------------|----------|----------|
| Atėjimas į darbą                  | 07:00 | 07:00 |
| Gamybos užduotis            | 07:00 | 09:00 |
| Išėjimas iš darbo                 | 09:00 | 09:00 |

Mokėtina suma apskaičiuojama puslapyje **Patvirtinimas** pagal darbuotojo registraciją. Apskaičiavę registraciją rezultatą galite matyti skirtuke **Laikas**. Pagal šį scenarijų jus domina toliau nurodyti laukai.

| Nukrypimas + | Nukrypimas - | Laikas  | Mokėjimo laikas |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13,50 | 08,00    |

Laiko Nukrypimas+ suma yra 6 valandos ir skaičiavimas paremtas nurodytomis laiko šablono nukrypimo zonomis. Šią sumą sudaro viena valanda laiko Nukrypimas+ nuo 07:00 iki 08:00 ir penkios valandos laiko Nukrypimas+ nuo 16:00 iki 21:00.

Perkėlę registracijas pastebėsite, kad laiko Nukrypimas+ suma pasikeis iš 6,0 valandų į 8,0 valandas.

| Nukrypimas + | Nukrypimas - | Laikas  | Mokėjimo laikas |
|--------|--------|-------|----------|
| 8,00   | 0,00   | 13,50 | 08,00    |

Šis pokytis įvyksta po perkėlimo, nes kintamos valandos buvo apskaičiuotos remiantis mokėjimo tipais, o ne laiku. Šioje lentelėje parodyta, kaip suskaičiuojamos aštuonios valandos.

| Iš     | Į       | Laikas | Koeficientas    | Nukrypimo sąskaita |
|----------|----------|------|-----------|--------------|
| 07:00 | 08:00 | 1    | 1         | 1            |
| 04:00 | 06:00 | 2    | 1         | 2            |
| 06:00 | 08:00 | 2    | 1.5       | 3            |
| 08:00 | 09:00 | 1    | 2         | 2            |
|          |          |      | **Bendroji suma** | **8**        |

