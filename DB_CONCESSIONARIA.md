# Database Concessionaria

## Entità: Automobile

**Nome tabella:** `AUTOMOBILI`

### Caratteristiche dell'entità

| Campo                            | Tipo          | Attributi                   | Note                                  |
| -------------------------------- | ------------- | --------------------------- | ------------------------------------- |
| **ID**                           | BIGINT        | PRIMARY KEY, AUTO_INCREMENT | Identificatore univoco                |
| **Casa_produttrice**             | VARCHAR(50)   | NOT NULL                    | Esempio: Fiat, BMW, Toyota            |
| **Modello**                      | VARCHAR(80)   | NOT NULL                    | Es. Panda, Serie 1                    |
| **Targa**                        | VARCHAR(8)    | NULL, UNIQUE                | Deve essere unica                     |
| **Altezza_CM**                   | SMALLINT      | NULL                        | Altezza in centimetri                 |
| **Lunghezza_CM**                 | SMALLINT      | NULL                        | Lunghezza in centimetri               |
| **Colore**                       | VARCHAR(40)   | NULL                        | Esempio: Rosso Ferrari                |
| **Classe_euro**                  | CHAR(6)       | NOT NULL                    | Valori 1-6                            |
| **Stato**                        | CHAR(5)       | NOT NULL                    | `nuova` o `usata`                     |
| **Km_percorsi**                  | MEDIUMINT     | NULL                        | Chilometri percorsi                   |
| **Motore**                       | VARCHAR(10)   | NOT NULL                    | Elettrico / benzina / diesel / ibrido |
| **Cambio**                       | VARCHAR(10)   | NULL                        | manuale / automatico                  |
| **Incidentata**                  | TINY INT(0/1) | NOT NULL                    | `si` o `no`                           |
| **Neopatentati**                 | TINY INT(0/1) | NULL                        | `si` o `no`                           |
| **Anno_immatricolazione**        | YEAR          | NOT NULL                    | Anno di immatricolazione              |
| **Data_ingresso_concessionaria** | DATE          | DATETIME NULL               | Data di ingresso nel concessionario   |

---

### Note:

- I campi `Incidentata` e `Neopatentati` sono booleani (`TRUE/FALSE`).
- `Data_ingresso_concessionaria` assume automaticamente la data corrente se non specificata.
- La combinazione `Casa_produttrice + Modello` potrebbe essere resa `UNIQUE`.
- Il campo `Casa_produttrice` accetta fino ad 80 caratteri per eventuali case giapponesi(alcune hanno nomi lunghi)
