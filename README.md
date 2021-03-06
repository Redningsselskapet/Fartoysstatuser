# RS STATUSER - Slik det er i dag

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

>**Ikke implementert ennå - ligger på test

| aarsak              | aarsak_id | Farge                                         |
|:------------------------ | ---- | --------------------------------------------- |
| Ingen årsak              | 0    | N/A |
| Personell                | 1    | N/A |
| Teknisk planlagt         | 2    | N/A |
| Teknisk uplanlagt        | 3    | N/A |
| Forflytning              | 4    | N/A |
| Hviletid                 | 5    | N/A |
| Operasjonelt             | 6    | N/A |

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
| 30 min beredskap         | 1    | ![#FF9933](https://via.placeholder.com/15/FF9933/000000?text=+) `#FF9933` |
| UAD                      | 3    | ![#ff0000](https://via.placeholder.com/15/ff000/000000?text=+) `#ff0000` |
| På oppdrag               | 4    | ![#FFFF00](https://via.placeholder.com/15/FFFF00/000000?text=+) `#FFFF00` |



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
"StatusId": 3,
"StatusText": "UAD",
"ColorCode": "#ff0000"
}
```


