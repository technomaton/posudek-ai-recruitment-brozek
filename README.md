# Regulatorní posudek: AI v recruitmentu — 642 kandidátů za 8 minut

> **Posudek k LinkedIn příspěvku:** [Pavel Brožek — „Za 8 minut jsem měl roztříděno 642 kandidátů"](https://www.linkedin.com/posts/brozekp_za-8-minut-jsem-m%C4%9Bl-rozt%C5%99%C3%ADd%C4%9Bno-642-kandid%C3%A1t%C5%AF-activity-7441803166980927488-X-ig)
>
> **Autor posudku:** Jaroslav Urbánek · TECHNOMATON, AI
>
> **Datum:** 23. března 2026

---

## Kontext

5 AI agentů (Claude Code) třídí 642 kandidátů z CSV exportu za 8 minut. Agenti analyzují JD, porovnávají kandidáty, provádí QA, hodnotí kariérní trajektorie a připravují personalizovaný outreach.

---

## 🔵 AI ACT (EU 2024/1689) — 7 porušení

### 1. Příloha III, bod 4a — High-risk klasifikace (nábor)

> *„systémy AI určené k použití za účelem náboru nebo výběru fyzických osob"*
> — Příloha III, bod 4a, str. 127–129

**Proč porušení:** Systém 5 agentů provádí přesně to, co Příloha III definuje jako high-risk — automatizovaný nábor a výběr kandidátů. Třídění 642 kandidátů do kategorií (A/B/C) je **CV screening s AI**, které je v textu přílohy explicitně zmíněno. Navíc agent č. 4 hodnotí kariérní trajektorie = **performance prediction**.

**Klíčový detail z čl. 6 odst. 3:** *„Bez ohledu na [výjimky] se systém AI uvedený v příloze III za vysoce rizikový považuje vždy, pokud provádí profilování fyzických osob."* — Třídění kandidátů je profilování, takže výjimka pro „přípravný úkon" (čl. 6 odst. 3 písm. d) **se neuplatní**.

**Sankce:** Až **15M EUR nebo 3% globálního obratu** (čl. 99).

---

### 2. Článek 9 — Chybějící systém řízení rizik

> *„Poskytovatelé vysoce rizikových systémů AI zavedou systém řízení rizik"*
> — Čl. 9, oddíl 2

**Proč porušení:** Autor neuvádí žádnou formu dokumentovaného risk managementu. U high-risk AI systému musí existovat kontinuální iterativní proces identifikace, analýzy a mitigace rizik — včetně rizika diskriminace a bias.

---

### 3. Článek 10 — Data governance (kvalita dat)

> *„Soubory tréninkových, validačních a testovacích dat podléhají příslušným postupům správy a řízení dat"*
> — Čl. 10, oddíl 2

**Proč porušení:** Autor sám přiznává problém s kvalitou dat: *„nekompletní data způsobila minimální klasifikaci top-tier kandidátů"*. To je přesně to, před čím čl. 10 chrání — systém musí mít data governance postupy zajišťující relevantnost, reprezentativnost a bezchybnost dat. CSV export bez validace tyto požadavky nesplňuje.

---

### 4. Článek 11 + Příloha IV — Chybějící technická dokumentace

> *„Technická dokumentace vysoce rizikového systému AI se vypracuje před uvedením tohoto systému na trh nebo do provozu"*
> — Čl. 11

**Proč porušení:** Neexistuje technická dokumentace popisující: zamýšlený účel systému, architekturu 5 agentů, použité prompty, limitace, výkonnostní metriky, bias testy. Příloha IV vyžaduje podrobný popis „logiky" AI systému, jeho schopností a omezení.

---

### 5. Článek 12 — Chybějící vedení záznamů (audit log)

> *„Vysoce rizikové systémy AI po dobu svého životního cyklu technicky umožňují automatické zaznamenávání událostí (protokoly)."*
> — Čl. 12 odst. 1

**Proč porušení:** Systém musí logovat: datum a čas každého použití, vstupní data, výstupy, identifikaci osob provádějících ověření výsledků. Bez audit logu nelze zpětně ověřit, jak AI rozhodla o konkrétním kandidátovi — a záznamy musí být uchovány **minimálně 5 let**.

---

### 6. Článek 26 odst. 11 + Článek 50 — Chybějící transparentnost vůči kandidátům

> *„Subjekty zavádějící vysoce rizikové systémy AI uvedené v příloze III, které přijímají rozhodnutí nebo pomáhají při přijímání rozhodnutí týkajících se fyzických osob, tyto fyzické osoby informují, že jsou vystaveny použití vysoce rizikového systému AI."*
> — Čl. 26 odst. 11

**Proč porušení:** 642 kandidátů s vysokou pravděpodobností neví, že jejich data zpracovávala AI. Čl. 26 odst. 11 **explicitně vyžaduje** informování dotčených osob — a to konkrétně v kontextu employment decisions dle Přílohy III.

---

### 7. Článek 4 — AI Literacy (JIŽ PLATÍ od 2.2.2025)

> *„Poskytovatelé systémů AI a subjekty zavádějící AI přijímají opatření, aby v co největší možné míře zajistili dostatečnou úroveň gramotnosti v oblasti AI u svých zaměstnanců"*
> — Čl. 4, str. 51

**Proč relevantní:** Toto ustanovení **již platí**. Autor demonstruje technickou zdatnost, ale AI gramotnost dle AI Act zahrnuje i povědomí o regulatorních rizicích a dopadech na dotčené osoby. Veřejný příspěvek bez zmínky o compliance naznačuje nedostatečnou gramotnost v regulatorní rovině.

---

## 🟢 GDPR (EU 2016/679) — 6 porušení

### 1. Článek 22 — Automatizované individuální rozhodování včetně profilování

> *„Subjekt údajů má právo nebýt předmětem žádného rozhodnutí založeného výhradně na automatizovaném zpracování, včetně profilování, které má pro něho právní účinky nebo se ho obdobným způsobem významně dotýká."*
> — Čl. 22 odst. 1, str. 46

**Proč porušení:** Třídění kandidátů do kategorií (A/B/C) je **profilování** dle definice v čl. 4 odst. 4 GDPR:

> *„profilováním" jakákoli forma automatizovaného zpracování osobních údajů spočívající v jejich použití k hodnocení některých osobních aspektů vztahujících se k fyzické osobě, zejména k rozboru nebo odhadu aspektů týkajících se jejího **pracovního výkonu**"*
> — Čl. 4 odst. 4, str. 33–35

Rozhodnutí o zařazení kandidáta do kategorie „top" vs. „vyřazen" má **významný dopad** na jeho šanci získat zaměstnání — tedy se ho „obdobným způsobem významně dotýká". Autor sice zmiňuje human oversight, ale popisuje 642 kandidátů za 8 minut — tempo, při kterém lidský přezkum jednotlivých rozhodnutí je **prakticky nemožný**.

I pokud by se uplatnila výjimka dle čl. 22 odst. 2 (smlouva, souhlas), správce musí zajistit minimálně **právo na lidský zásah, právo vyjádřit svůj názor a právo napadnout rozhodnutí** (čl. 22 odst. 3).

**Sankce:** Až **20M EUR nebo 4% obratu** (čl. 83 odst. 5).

---

### 2. Článek 35 — Chybějící DPIA (posouzení vlivu)

> *„Pokud je pravděpodobné, že určitý druh zpracování, zejména při využití nových technologií, bude [...] mít za následek vysoké riziko pro práva a svobody fyzických osob, provede správce před zpracováním posouzení vlivu"*
> — Čl. 35 odst. 1, str. 53–54

**Proč porušení:** Čl. 35 odst. 3 stanoví, kdy je DPIA **vždy povinný**:

> *„a) systematické a rozsáhlé vyhodnocování osobních aspektů týkajících se fyzických osob, které je založeno na automatizovaném zpracování, včetně profilování"*

Třídění 642 kandidátů AI systémem je **přesně** tento scénář — systematické, rozsáhlé, automatizované profilování osobních aspektů (pracovní výkon, kariérní trajektorie) s důsledky pro dotčené osoby.

**Sankce:** Až **10M EUR nebo 2% obratu** (čl. 83 odst. 4).

---

### 3. Článek 14 — Chybějící informační povinnost

> *„Pokud osobní údaje nebyly získány od subjektu údajů [...] poskytne správce subjektu údajů tyto informace: [...] skutečnost, že dochází k automatizovanému rozhodování, včetně profilování"*
> — Čl. 14 odst. 1 a 2 písm. f), str. 41–43

**Proč porušení:** Kandidátská data v CSV exportu nebyla získána přímo od kandidátů (byla stažena z ATS/databáze). Čl. 14 vyžaduje, aby správce kandidátům aktivně sdělil:
- totožnost správce a účely zpracování
- právní základ zpracování
- kategorie dotčených údajů
- **skutečnost, že dochází k profilování a smysluplné informace o použitém postupu**
- příjemce dat (Anthropic jako zpracovatel)

Informace musí být poskytnuta **nejpozději do 1 měsíce** od získání dat, nebo **při prvním kontaktu** s kandidátem (čl. 14 odst. 3).

---

### 4. Článek 28 — Chybějící DPA (Data Processing Agreement) s Anthropic

> *„Zpracování zpracovatelem se řídí smlouvou nebo jiným právním aktem [...] který stanovuje předmět a dobu trvání zpracování, povahu a účel zpracování"*
> — Čl. 28 odst. 3, str. 50

**Proč porušení:** Odesláním kandidátních dat (jméno, CV, kontakt, pracovní historie) do Claude API se Anthropic stává **zpracovatelem** osobních údajů. Bez platné DPA s Anthropic je toto zpracování v rozporu s čl. 28. DPA musí stanovit: jak Anthropic nakládá s daty, retention policy, sub-processors, právo auditu, a breach notification SLA.

---

### 5. Články 44–49 — Mezinárodní transfer osobních údajů

> *„Jakékoli předání osobních údajů [...] do třetí země [...] se uskuteční pouze tehdy, pokud [...] správce a zpracovatel dodrží podmínky stanovené v této kapitole"*
> — Čl. 44, str. 56

**Proč porušení:** Claude API zpracovává data na serverech mimo EU (Anthropic je US společnost). Transfer osobních údajů 642 kandidátů do třetí země vyžaduje buď:
- rozhodnutí Komise o přiměřenosti (EU-US DPF — nutno ověřit certifikaci Anthropic)
- standardní smluvní doložky (SCCs)
- nebo explicitní souhlas kandidátů (čl. 49)

Bez ověření mechanismu transferu je každé odeslání osobních údajů do Claude API **nelegálním transferem**.

---

### 6. Článek 5 odst. 1 písm. c) — Minimalizace údajů

> *„Osobní údaje musí být přiměřené, relevantní a omezené na nezbytný rozsah ve vztahu k účelům, pro které jsou zpracovávány"*
> — Čl. 5 odst. 1 písm. c)

**Proč porušení:** CSV export pravděpodobně obsahuje **veškerá data** z ATS — včetně údajů nepotřebných pro účel třídění (kontaktní údaje, poznámky, historické interakce). Odeslání kompletního CSV do AI bez předchozí anonymizace nebo redukce je rozpor s principem minimalizace. Měla by být odeslána pouze data nezbytná pro vyhodnocení vůči kritériím pozice.

---

## 🔴 NIS2 (EU 2022/2555) — Podmíněně relevantní

### Čl. 21 — Opatření pro řízení kybernetických rizik

**Relevance pouze pokud** je recruiter nebo jeho klient v sektoru essential/important entity. Pro individuálního recruitera typicky **nerelevantní**.

**Pokud by šlo o HR platformu jako službu:** Sdílení 642 CV přes API třetí strany bez řízení rizik dodavatelského řetězce (čl. 21 odst. 2 písm. d) by bylo porušením.

---

## 🟣 Data Act (EU 2023/2854) — Nerelevantní

Data Act reguluje přístup k datům generovaným IoT zařízeními a cloud switching. Na tento případ se **nevztahuje**.

---

## 🟠 DORA (EU 2022/2554) — Nerelevantní

DORA se vztahuje výhradně na finanční sektor. Recruitment **nespadá** do scope.

---

## Souhrnná tabulka porušení

| # | Regulace | Článek | Porušení | Závažnost | Sankce |
|---|----------|--------|----------|-----------|--------|
| 1 | 🔵 AI Act | Příloha III.4a + čl. 6 | High-risk systém bez compliance | 🔴 | 15M/3% |
| 2 | 🔵 AI Act | Čl. 9 | Chybějící risk management | 🔴 | 15M/3% |
| 3 | 🔵 AI Act | Čl. 10 | Nedostatečná data governance | 🟠 | 15M/3% |
| 4 | 🔵 AI Act | Čl. 11 + Příloha IV | Chybějící technická dokumentace | 🔴 | 15M/3% |
| 5 | 🔵 AI Act | Čl. 12 | Chybějící audit log | 🔴 | 15M/3% |
| 6 | 🔵 AI Act | Čl. 26/11 + 50 | Neinformování kandidátů o AI | 🔴 | 15M/3% |
| 7 | 🔵 AI Act | Čl. 4 | AI literacy (platí od 2.2.2025) | 🟡 | 15M/3% |
| 8 | 🟢 GDPR | Čl. 22 | Automatizované rozhodování | 🔴 | 20M/4% |
| 9 | 🟢 GDPR | Čl. 35 | Chybějící DPIA | 🔴 | 10M/2% |
| 10 | 🟢 GDPR | Čl. 14 | Chybějící informování kandidátů | 🟠 | 20M/4% |
| 11 | 🟢 GDPR | Čl. 28 | Chybějící DPA s Anthropic | 🟠 | 10M/2% |
| 12 | 🟢 GDPR | Čl. 44–49 | Nelegální mezinárodní transfer | 🔴 | 20M/4% |
| 13 | 🟢 GDPR | Čl. 5/1/c | Porušení minimalizace dat | 🟡 | 20M/4% |

**Celkem: 13 identifikovaných porušení** (7 AI Act, 6 GDPR)

---

📖 **Zdroje:** Regulation knowledge graph — přímé citace z legislativních textů EU 2024/1689 (AI Act) a EU 2016/679 (GDPR) s čísly stran.

⚠️ **Toto není právní rada. Pro závazný výklad konzultujte právníka specializovaného na AI regulaci a ochranu osobních údajů.**

---

*Posudek vypracován s využitím AI-Native Entry Framework™ regulation knowledge graph — TECHNOMATON*
