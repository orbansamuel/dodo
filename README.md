# PDF Jegyzetkivonat Készítő

Ez a projekt egy tudományos cikk (PDF) magyar nyelvű jegyzeteit készíti el prezentáció készítéséhez.

## Fájlok

- `1-s2.0-S0168159123000679-main.pdf` - A feldolgozandó tudományos cikk
- `extract_notes.py` - A jegyzetkivonat készítő Python script
- `jegyzet_magyar.md` - A kész magyar nyelvű jegyzet (markdown formátum)
- `prezentacio_pelda.md` - Példa prezentáció a jegyzetekből (Marp formátum)

## Használat

### Jegyzet generálása

```bash
python3 extract_notes.py
```

A script automatikusan:
1. Beolvassa a PDF fájlt (`1-s2.0-S0168159123000679-main.pdf`)
2. Kivonatol belőle magyar nyelvű jegyzeteket
3. Strukturált markdown formátumban menti el (`jegyzet_magyar.md`)

### Kimenet

A generált `jegyzet_magyar.md` fájl tartalmazza:

- **Alapinformációk**: Cím, szerzők, kutatóhelyek
- **Kulcsszavak és témakörök**: A kutatás fő témái
- **Probléma és háttér**: A kutatás célja és kontextusa
- **Kísérlet leírása**: Állatok, módszerek, kezelések
- **Főbb eredmények**: Viselkedés, testhőmérséklet, tejtermelés
- **Gyakorlati következtetések**: Előnyök, kihívások, jóllét szempontok
- **Kulcsfontosságú üzenetek**: Prezentációhoz összefoglalva
- **Adatok**: Számszerű információk
- **Hivatkozási információ**: Publikációs adatok

## A tudományos cikk témája

A kutatás a **tejelő tehenek hőstressz-kezelését** vizsgálja Új-Zélandon:

- Hogyan lehet csökkenteni a tehenek hőterhelését nyáron?
- Fejési és etetési idők módosításának hatásai
- Viselkedés, testhőmérséklet, légzésszám változásai
- Tejtermelés és jóllét összefüggései

## Követelmények

```bash
pip install PyPDF2
```

## Prezentáció készítése

A `jegyzet_magyar.md` fájl használható:

1. **PowerPoint/Google Slides készítéséhez** - témakörönként külön diák
2. **Keynote prezentációhoz** - strukturált tartalom
3. **Markdown prezentációhoz** (pl. reveal.js, Marp) - közvetlenül használható
4. **Előadás jegyzetként** - minden fontos információ egy helyen

### Példa prezentáció

A `prezentacio_pelda.md` fájl egy kész prezentációs példát tartalmaz Marp formátumban.

**Marp használata:**
```bash
# Telepítés
npm install -g @marp-team/marp-cli

# PDF generálás
marp prezentacio_pelda.md -o prezentacio.pdf

# HTML generálás
marp prezentacio_pelda.md -o prezentacio.html

# Élő előnézet
marp -w prezentacio_pelda.md
```

### Javasolt prezentációs szerkezet

1. **Bevezető diák**: Probléma bemutatása
2. **Módszertan**: Kísérlet leírása
3. **Eredmények**: Főbb megállapítások
4. **Következtetések**: Gyakorlati alkalmazás
5. **Kulcsüzenetek**: 7 fő pont összefoglalva

## Megjegyzések

- A jegyzet **magyar nyelvű**, az eredeti angol cikk kulcsfontosságú információit tartalmazza
- **Nem fordítás**, hanem strukturált jegyzet prezentáció készítéséhez
- A markdown formátum könnyen szerkeszthető és konvertálható más formátumokba
