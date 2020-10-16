# RS STATUSER - Tony's forslag

Tony's model:
- https://github.com/Redningsselskapet/Fartoysstatuser/blob/Tonys-forslag/Statuser.pdf

## Offisielle statuser (MDS)

- Disse statusene skrives fra RO og inn til MDS

- Eksponeres ut i feed'ene våre:  
  
  - https://skoytestasjonapi.rs.no/prefetch/getboats
  
  - https://skoytestasjonapi.rs.no/prefetch/getstations
  
  - https://skoytestasjonapi.rs.no/prefetch/iphone

- Brukes FRR, RS Safetrx.

| state_description              | state | Farge                                         
| ----------------- | ---- | --------------------------------------------- |
| Operativ          | 0    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33`  | 
| Redusert          | 1    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00`  | 
| UAD               | 3    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000`  | 


>**Ikke implementert ennå

Eksempel på felter fra feed (dagens feed):
```json
{
  "merknad": {},
  "aarsak": "Ingen årsak",
  "aarsak_id": "0",
  "forventet_tilbake": {},
  "state": "0",
  "state_description": "Operativ",
}
```


## Årsaker og understatuser

| aarsak              | aarsak_id | Farge                                         | Relatert til state |
|:------------------------ | ---- | --------------------------------------------- |--------------------|
| Normal                   | ?    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` | 0 |
| Ledig på basen           | ?    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` | 0 |
| Ledig på oppdrag         | ?    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` | 0 |
| 30 min beredskap         | ?    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` | 0 |
| Forflytning              | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` | 1 |
| Personell                | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` | 1 |
| Teknisk planlagt         | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` | 1 |
| Hviletid                 | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` | 1 |
| Operasjonelt             | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` | 1 |
| Kun SAR-oppdrag          | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` | 1 |
| Teknisk uplanlagt        | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` | 1 |
| Forflytning              | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` | 3 |
| Personell                | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` | 3 |
| Teknisk planlagt         | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` | 3 |
| Operasjonelt             | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` | 3 |
| Hviletid                 | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` | 3 |

> **Ikke implementert ennå
>
> 
> RO viser ikke tekst, bare farge
> 
> CO viser tekst og farge



Eksempel på status visning fra CO:

![](https://github.com/Redningsselskapet/Fartoysstatuser/blob/Tonys-forslag/img/status-tony.PNG)
