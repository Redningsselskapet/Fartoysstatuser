# RS STATUSER - Mortens forslag

## Offisielle statuser (MDS)

- Disse statusene skrives fra RO og inn til MDS

- Eksponeres ut i feed'ene våre:  
  
  - https://skoytestasjonapi.rs.no/prefetch/getboats
  
  - https://skoytestasjonapi.rs.no/prefetch/getstations
  
  - https://skoytestasjonapi.rs.no/prefetch/iphone

- Brukes FRR, RS App.

| Navn              | Kode | Farge                                         |
| ----------------- | ---- | --------------------------------------------- |
| Operativ          | 0    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33`  | 
| 30 min beredskap  | 1    | ![#90ee90](https://via.placeholder.com/15/90ee90/000000?text=+) `#90ee90`  | 
| UAD               | 3    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000`  | 
| Kun SAR-oppdrag** | 5    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00`  |

>**Ikke implementert ennå

Eksempel på felter fra feed:
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


## ExtendedStates

- Status'ene settes i ro på bakgrunn av det som sendes inn fra kystradion.

- RO eksponerer dette ut, som igjen bakes inn i feed'en https://skoytestasjonapi.rs.no/prefetch/getboats under objectet extendedState.

- Brukes av RO gui, CO gui 

| Navn                     | Kode | Farge                                         |
|:------------------------ | ---- | --------------------------------------------- |
| Ledig, på basen/patrulje | 0    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33` |
| Kun SAR-oppdrag**        | 5    | ![#0066FF](https://via.placeholder.com/15/0066FF/000000?text=+) `#0066FF` |
| 30 min beredskap         | 1    | ![#ff9933](https://via.placeholder.com/15/ff9933/000000?text=+) `#ff9933` |
| UAD                      | 3    | ![#ff0000](https://via.placeholder.com/15/ff000/000000?text=+) `#ff0000` |
| På oppdrag               | 4    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |



> **Ikke implementert ennå
>
> 
> RO viser ikke tekst, bare farge
> 
> CO viser tekst og farge



Eksempel på status visning fra CO:

![](https://github.com/Redningsselskapet/Fartoysstatuser/blob/main/img/co.PNG)



Exempel på extendedState objekt i getboats feed:

```json
"extendedState": {
"StatusId": 0,
"StatusText": "Ledig, på basen/patrulje",
"ColorCode": "#008000"
}
```


