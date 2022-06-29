---
title: Registruoti mokesčių sąskaitos apskaitos principu
description: Šiame straipsnyje pateikta išlaidų sąskaitos apskaitos principo peržiūra.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: c03109baaa341b25af70840b791ddf04f692fb1a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016571"
---
# <a name="post-to-charge-account-accounting-principle"></a>Registruoti mokesčių sąskaitos apskaitos principu

*Registravimas į sąskaitos* apskaitos principą leidžia kurti sąskaitas ir lengviau suderinti visus skirtumus, atsirandaus vieneto kainą tarp faktinio registravimo ir finansinio registravimo, nupirktų prekių netiesioginių išlaidų arba pirkimo užsakymo išlaidų.

Dvi mokėtinų sumų **mokesčių** kodų konfigūracijos puslapyje Mokesčių kodas (**\>\> Mokėtinų mokesčių nustatymo mokesčių kodas**) gali sukelti pirkimo užsakymo įtaką atsargų turto vertinimui:

- Mokesčių **kodams** *·* **·** *·*, kurių debeto tipo laukas nustatytas kaip Prekė, o kredito tipo laukas nustatytas kaip DK sąskaita, DK sąskaita, kuri pasirinkta kaip absorbavimo sąskaita, veikia kaip atsargų pokyčio sąskaita.
- Išlaidų **koduose** *·* **·** *, kurių debeto tipo laukas nustatytas kaip Prekė, o kredito tipo laukas nustatytas kaip Klientas/* Tiekėjas, išlaidos bus apskaiuotos kaip medžiagų išlaidos, o prekės atsargų pokyčio sąskaita bus naudojama.

## <a name="european-special-accounting-rule"></a>Europos specialioji apskaitos taisyklė

Europoje registrai į *sąskaitų apskaitos principus* dažnai naudojami, kad būtų įtraukta speciali apskaitos taisyklė. Pavyzdžiui, vienas iš šių metodų paprastai naudojamas atsargų pokyčiams sąskaitai pateikti:

- **Pardavimo metodo savikaina** – standartinė atsargų registravimo šablono konfigūracija palaiko šį metodą. Registruoti *mokesčių sąskaitos* apskaitos principu nebūtina.
- **Išlaidų metodo pobūdis** – mažesnės organizacijos dažnai naudoja šį metodą. Paprastai tai apima šiuos žingsnius:

    1. Prekių ar paslaugų gavimo metu išlaidos visiškai į išlaidos.
    2. Laikotarpio pabaigoje atliekamas ciklų skaičiavimas.
    3. Neautomatinis kiekio ir vertės koregavimas registruojamas atsargose. (Korespondentinė sąskaita yra atsargų pokyčio sąskaita, kuri kompensuoja išlaidas, užregistruotas 1 žingsnyje. Todėl atsargų vertės variacija matote tik šioje sąskaitoje.)

Registravimo *išlaidų sąskaitoje principas* leidžia visiškai automatizuoti du registravimus. Tokiu būdu galite pašalinti laikotarpio pabaigos koregavimo registravimą neautomatiniu būdu.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Įjungti paskelbį į sąskaitos apskaitos principą

Norėdami įjungti registrą *į sąskaitos apskaitos principą*, atlikite šiuos veiksmus.

1. Pasirinkite **Mokėtinos sumos \> Sąranka \> Mokėtinų sumų parametrai**.
2. SF skirtuko **SF** "**FastTab**" nustatykite DK pasirinktį **Registruoti kaip išlaidų sąskaitą** kaip *Taip*.
3. Uždarykite puslapį.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Būtinos sąlygos ir rekomenduojami parametrai, skirti registruoti mokesčių sąskaitos apskaitos principui

Jei planuojate atlikti pirkimo išlaidų ir atsargų variacijų sąskaitą, turi būti įdiegti šie būtinieji komponentai:

- Mokėtinų sumų **parametrų** **puslapio** SF skirtuke (**\>\> Mokėtinų sumų nustatymo mokėtinų sumų parametrai**) **parinktis** Registruoti į DK turi būti nustatyta kaip *Taip*.
- Prekių modelių **grupių puslapyje** (**Išlaidų \> valdymo atsargų apskaitos \>** strategijos nustatymas Prekių modelių grupės) *visos* šios pasirinktys turi būti nustatytos kaip Taip kiekvienai susijusiai modelių grupei, kurioje yra į pirkimo užsakymą įtrauktos prekės:

    - Registruoti faktines atsargas
    - Registruoti finansines atsargas
    - Sukaupti įsipareigojimus gavimo dokumente

- Įsigijimo ir **išlaidų** **parametrų** puslapio pristatymas (**\>\>** **Įsigijimas ir išlaidų nustatymo įsigijimo ir išlaidų parametrai) parinktis Generuoti** išlaidas gavimo kvite turi būti nustatyta kaip *Taip.*
- Atsargų apskaitos **skirtuko** puslapyje **Atsargų** ir sandėlio valdymo parametrai (**\>\> Atsargų valdymo nustatymas Atsargų ir sandėlio valdymo** parametrai) **parinktis** Registruoti važtaraštį DK turi būti nustatyta kaip *Taip.*
- Skirtuko Pirkimo **užsakymas registravimo puslapyje** **(** **\>\>\> Atsargų valdymo nustatymo registravimas) pagrindinės sąskaitos, kurios taikomos kiekvienai susijusiai prekei, turi būti nurodytos kiekvienam iš šių registravimo tipų:**

    - Pirkimo išlaidos, neišrašyta SF
    - Produkto pirkimo išlaidos
    - Atsargų nuokrypis

## <a name="example-scenario-1-change-in-unit-cost-price"></a>1 pavyzdis scenarijus: vieneto savikainos pokytis

Šiame pavyzdyje scenarijuje yra šios būtinosios sąlygos:

- "Pirmasis į, pirmasis iš" (FIFO) įkainojimo modelis

Toliau pateiktoje procedūroje pateikiamas pavyzdys, kuriame rodoma, kas atsitinka, kai pirkimo užsakyme keičiate vieneto savikainą.

1. Sukurkite pirkimo užsakymą, kai kiekis yra 1 prekė, kurios vieneto kaina 100,00.
2. Patvirtinkite pirkimo užsakymą.
3. Užregistruokite pirkimo užsakymo produkto gavimo kvitą.
4. Patikrinkite produkto gavimo kvitą. Šioje lentelėje rodomas kvito pavyzdys.

    | Registravimo tipas | Pagrindinė sąskaita | Pagrindinės sąskaitos pavadinimas | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Faktiškai/finansiškai? | Suma |
    |---|---|---|---|---|---|---|---|
    | Pirkimas, atsargų nuokrypis | 600170 | Atsargų pokyčio medžiagos | Išlaidos | Kreditas | Ne | Faktinis | -100.00 |
    | Gautų nusipirktų medžiagų savikaina | 140100 | Medžiagų atsargos | Turtas | Debetas | Taip | Faktinis | 100.00 |
    | Pirkimo išlaidos, neišrašyta SF | 600180 | Medžiagų gavimas | Išlaidos | Debetas | Taip | Faktinis | 100.00 |
    | Pirkimas, kaupimas | 200140 | Sukaupti pirkimai | Įsipareigojimai | Kreditas | Taip | Faktinis | -100.00 |

5. Užregistruokite pirkimo užsakymo, kuriame atnaujinta vieneto kaina 110,00, SF.
6. Patikrinkite SF kvitą. Šioje lentelėje rodomas kvito pavyzdys.

    | Registravimo tipas | Pagrindinė sąskaita | Pagrindinės sąskaitos pavadinimas | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Faktiškai/finansiškai? | Suma |
    |---|---|---|---|---|---|---|---|
    | Pirkimas, atsargų nuokrypis | 600170 | Atsargų pokyčio medžiagos | Išlaidos | Kreditas | Ne | Finansinis | -10.00 |
    | Gautų nusipirktų medžiagų savikaina | 140100 | Medžiagų atsargos | Turtas | Debetas | Taip | Finansinis | -100.00 |
    | Pirkimo išlaidos, neišrašyta SF | 600180 | Medžiagų gavimas | Išlaidos | Debetas | Taip | Finansinis | -100.00 |
    | Pirkimas, kaupimas | 200140 | Sukaupti pirkimai | Įsipareigojimai | Kreditas | Taip | Finansinis | 100.00 |
    | Nusipirktų medžiagų, kurioms išrašyta SF, savikaina | 140100 | Medžiagų atsargos | Turtas | Debetas | Ne | Finansinis | 110.00 |
    | Produkto pirkimo išlaidos | 600180 | Medžiagų gavimas | Išlaidos | Kreditas | Ne | Finansinis | 110.00 |
    | Tiekėjo balansas | 211000 | Mokėtinų sumų prekyba | Įsipareigojimai | Kreditas | Ne | Finansinis | -110.00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>2 pavyzdys: Pirkimo užsakymo išlaidos ir netiesioginės išlaidos

Šiame pavyzdyje scenarijuje yra šios būtinosios sąlygos:

- FIFO įkainojimo modelis
- **1 išlaidų kodas:** 10% debeto prekės ir kredito DK sąskaita
- **2 išlaidų kodas:** 10,00 proporcinės debeto prekės ir kredito klientas / tiekėjas
- **Netiesioginės išlaidos:** 2,00% pridėta prie pirkimo kainos

Toliau pateiktoje procedūroje pateikiamas pavyzdys, kuriame rodoma, kas atsitinka, kai į pirkimo užsakymą įtraukiami mokesčiai ir netiesioginės išlaidos.

1. Sukurkite pirkimo užsakymą, kai kiekis yra 1 prekė, kurios vieneto kaina 100,00.
2. Įtraukite vieną 10 procentų išlaidų kodą, kuris debetuos prekę ir kredituos DK.
3. Įtraukite vieną 10,00 išlaidų kodą, kuris debetuos prekę ir kredituos klientą /tiekėją.
4. Paskirstyti išlaidas pirkimo užsakymo eilutėms.
5. Patvirtinkite pirkimo užsakymą.
6. Užregistruokite pirkimo užsakymo produkto gavimo kvitą.
7. Patikrinkite produkto gavimo kvitą. Šioje lentelėje rodomas kvito pavyzdys.

    | Registravimo tipas | Pagrindinė sąskaita | Pagrindinės sąskaitos pavadinimas | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Faktinis arba finansinis | Suma |
    |---|---|---|---|---|---|---|---|
    | Pirkimas, atsargų nuokrypis | 600170 | Atsargų pokyčio medžiagos | Išlaidos | Kreditas | Ne | Faktinis | -110.00 |
    | Įvertintos netiesioginės įtrauktos išlaidos | 600520 | Netiesioginių išlaidų pereisite | Išlaidos | Kreditas | Taip | Faktinis | -2.40 |
    | Pirkimo frachtas | 600120 | Transportavimo/ transportavimo išlaidos | Išlaidos | Kreditas | Ne | Faktinis | -10.00 |
    | Gautų nusipirktų medžiagų savikaina | 140100 | Medžiagų atsargos | Turtas | Debetas | Taip | Faktinis | 122.40 |
    | Pirkimo išlaidos, neišrašyta SF | 600180 | Medžiagų gavimas | Išlaidos | Debetas | Taip | Faktinis | 110.00 |
    | Pirkimas, kaupimas | 200140 | Sukaupti pirkimai | Įsipareigojimai | Kreditas | Taip | Faktinis | -110.00 |

8. Registruokite pirkimo užsakymo SF.
9. Patikrinkite SF kvitą. Šioje lentelėje rodomas kvito pavyzdys.

    | Registravimo tipas | Pagrindinė sąskaita | Pagrindinės sąskaitos pavadinimas | Kodo tipas | Debetas/kreditas? | Tarpuskaitos sąskaita | Faktiškai/finansiškai? | Suma |
    |---|---|---|---|---|---|---|---|
    | Pirkimas, atsargų nuokrypis | 600170 | Atsargų pokyčio medžiagos | Išlaidos | Kreditas | Ne | Finansinis | 0,00 |
    | Įvertintos netiesioginės įtrauktos išlaidos | 600520 | Netiesioginių išlaidų pereisite | Išlaidos | Debetas | Taip | Finansinis | 2.40 |
    | Netiesioginės įtrauktos išlaidos | 600520 | Netiesioginių išlaidų pereisite | Išlaidos | Debetas | Ne | Finansinis | -2.40 |
    | Gautų nusipirktų medžiagų savikaina | 140100 | Medžiagų atsargos | Turtas | Kreditas | Taip | Finansinis | -110.00 |
    | Pirkimo išlaidos, neišrašyta SF | 600180 | Medžiagų gavimas | Išlaidos | Kreditas | Taip | Finansinis | -110.00 |
    | Pirkimas, kaupimas | 200140 | Sukaupti pirkimai | Įsipareigojimai | Debetas | Taip | Finansinis | 110.00 |
    | Nusipirktų medžiagų, kurioms išrašyta SF, savikaina | 140100 | Medžiagų atsargos | Turtas | Debetas | Ne | Finansinis | 110.00 |
    | Produkto pirkimo išlaidos | 600180 | Medžiagų gavimas | Išlaidos | Kreditas | Ne | Finansinis | 110.00 |
    | Tiekėjo balansas | 211000 | Mokėtinų sumų prekyba | Įsipareigojimai | Kreditas | Ne | Finansinis | -110.00 |
