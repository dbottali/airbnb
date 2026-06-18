# Airbnb Fondocassa Calculator

Pagina web statica per calcolare:

- payout Airbnb prima e dopo ritenuta;
- split 80/20 tra proprietario e property manager;
- ritenuta italiana configurabile;
- quota fondocassa generata dalla parte netta delle pulizie nel payout del PM;
- storico spese fondocassa con note;
- export CSV e backup/import JSON.

## Regola fondocassa

Formula usata:

```text
Fondocassa = Payout PM netto × Cleaning fee / Base lorda
```

dove:

```text
Base lorda = Accommodation + Cleaning fee
```

## Default

- Cleaning fee: 71 €
- PM: 20%
- Ritenuta Italia: 21%
- Fondocassa iniziale: 161 €

Tutto è modificabile dalla pagina.

## Come caricare su GitHub Pages

1. Crea una repository GitHub, per esempio `airbnb-fondocassa`.
2. Carica `index.html` nella root della repository.
3. Vai su `Settings` → `Pages`.
4. In `Build and deployment`, scegli:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Salva.
6. Dopo qualche minuto GitHub ti darà il link pubblico.

## Nota importante

Questa versione è statica: i dati vengono salvati nel browser con `localStorage`.

Questo significa che:
- tu puoi usare la pagina dal tuo browser e i dati restano lì;
- un collaboratore che apre la stessa pagina non vede automaticamente i tuoi dati;
- per condividere i dati devi usare `Export JSON` e `Import JSON`.

Per sincronizzazione vera tra più persone serve un backend, per esempio Google Sheets, Supabase o Firebase.
