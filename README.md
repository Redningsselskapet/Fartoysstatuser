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

| aarsak              | aarsak_id | Farge                                         |
|:------------------------ | ---- | --------------------------------------------- |
| Normal                   | ?    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` |
| Ledig på basen           | ?    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` |
| Ledig på oppdrag         | ?    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` |
| 30 min beredskap         | ?    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` |
| Forflytning              | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |
| Personell                | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |
| Teknisk planlagt         | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |
| Hviletid                 | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |
| Operasjonelt             | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |
| Kun SAR-oppdrag          | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |
| Teknisk uplanlagt        | ?    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |
| Forflytning              | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` |
| Personell                | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` |
| Teknisk planlagt         | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` |
| Operasjonelt             | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` |
| Hviletid                 | ?    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000` |

> **Ikke implementert ennå
>
> 
> RO viser ikke tekst, bare farge
> 
> CO viser tekst og farge



Eksempel på status visning fra CO:

![](https://github.com/Redningsselskapet/Fartoysstatuser/blob/Tonys-forslag/img/status-tony.PNG)
