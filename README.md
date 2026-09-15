# power-bi-lego-franchise-value-analysis
Power BI analysis of LEGO licensed sets, price per set, price per piece and the relationship between movie franchises, Box Office performance and LEGO pricing.

## LEGO, filmy i cena klocka – czy filmowe uniwersum wpływa na ceny LEGO?

Projekt analityczny wykonany w Power BI, którego celem jest zbadanie zależności pomiędzy filmowymi franczyzami a ofertą licencjonowanych zestawów LEGO.

Analiza obejmuje nie tylko ceny całych zestawów, ale również **cenę pojedynczego klocka (Price per Piece)**, liczbę elementów oraz różnice pomiędzy poszczególnymi franczyzami.

Dane dotyczące zestawów LEGO zostały połączone z danymi dotyczącymi wyników Box Office wybranych filmowych uniwersów. Pozwala to sprawdzić, **czy obecność i popularność filmowej franczyzy znajduje odzwierciedlenie w cenach oraz charakterystyce oferty LEGO**.

---

## Cel projektu

Główne pytanie analityczne:

> **Czy i w jakim stopniu obecność licencjonowanego uniwersum filmowego wpływa na ceny zestawów LEGO oraz cenę pojedynczego klocka?**

Dodatkowe pytania:

- Czy zestawy należące do różnych franczyz mają różną średnią cenę?
- Czy franczyza filmowa wpływa na `Price per Piece`?
- Czy większa liczba klocków oznacza proporcjonalnie wyższą cenę zestawu?
- Czy małe zestawy mogą charakteryzować się wysoką ceną pojedynczego klocka?
- Czy popularność franczyzy mierzona wynikami Box Office znajduje odzwierciedlenie w cenach LEGO?
- Czy poszczególne franczyzy mają różne strategie produktowe i cenowe?
- Czy zmiany w ofercie LEGO można powiązać z rozwojem popularności określonych filmowych uniwersów?

---

## Zakres analizy

Analiza obejmuje licencjonowane zestawy LEGO powiązane z 10 wybranymi franczyzami filmowymi:

- Star Wars
- Marvel
- Harry Potter
- Jurassic World
- DC Comics
- Toy Story
- Auta
- Śródziemie
- Piraci z Karaibów
- Indiana Jones

Analizowany okres obejmuje lata **1984–2024**.

Z analizy wyłączono oryginalne serie LEGO, takie jak:

- LEGO City
- LEGO Ninjago
- LEGO Creator

Dzięki temu analiza koncentruje się na zestawach związanych z licencjonowanymi franczyzami filmowymi.

---

## Dashboard

![LEGO Franchise Analysis](screenshots/overview.png)

Dashboard został zaprojektowany w stylistyce **Cinema Dark Mode**, nawiązującej do tematyki filmowej.

### Główne KPI

- **76.81 mld USD** – łączny Box Office analizowanych filmów
- **1 654 tys.** – liczba analizowanych zestawów / rekordów
- **59.46 USD** – średnia cena zestawu

Raport pozwala przechodzić od analizy całych franczyz i ich wyników Box Office do szczegółowej analizy cen zestawów oraz ceny pojedynczego klocka.

---

# Główne obszary analizy

## 1. Cena zestawu

Jednym z podstawowych elementów analizy jest średnia cena zestawów LEGO.

```DAX
Średnia_Cena_Zestawu =
AVERAGE(fact_Lego[Retail_Price_USD])
