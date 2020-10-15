# RS STATUSER

## Offisielle statuser (MDS)

- Disse statusene skrives fra RO og inn til MDS

- Eksponeres ut i alle feed'ene våre:  
  
  - https://skoytestasjonapi.rs.no/prefetch/getboats
  
  - https://skoytestasjonapi.rs.no/prefetch/getstations
  
  - https://skoytestasjonapi.rs.no/prefetch/iphone

- Brukes FRR, RS App.

| Navn              | Kode | Farge                                         |
| ----------------- | ---- | --------------------------------------------- |
| Operativ          | 0    | ![#33CC33](https://via.placeholder.com/15/33CC33/000000?text=+) `#33CC33`  | 
| 30 min beredskap  | 1    | ![#90ee90](https://via.placeholder.com/15/90ee90/000000?text=+) `#90ee90`  | 
| UAD               | 3    | ![#ff0000](https://via.placeholder.com/15/ff0000/000000?text=+) `#ff0000`  | 
| Kun SAR-oppdrag** | 5    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ff0000`  |

**Ikke implementer ennå



## ExtendedStates

- Status'ene settes i ro på bakgrunn av det som sendes inn fra kystradion.

- RO eksponerer dette ut, som igjen bakes inn i feed'en https://skoytestasjonapi.rs.no/prefetch/getboats under objectet extendedState.

- Brukes av RO gui, CO gui 

| Navn                     | Kode | Farge                                         | Fargekode |
|:------------------------ | ---- | --------------------------------------------- | --------- |
| Ledig, på basen/patrulje | 0    | ![#008000](https://via.placeholder.com/15/008000/000000?text=+) `#008000` |
| Kun SAR-oppdrag**        | 5    | ![#ffff00](https://via.placeholder.com/15/ffff00/000000?text=+) `#ffff00` |
| 30 min beredskap         | 1    | ![#90ee90](https://via.placeholder.com/15/90ee90/000000?text=+) `#90ee90` |
| UAD                      | 3    | ![#ff0000](https://via.placeholder.com/15/ff000/000000?text=+) `#ff0000` |
| På oppdrag**             | 4    | ![#ffd203](https://via.placeholder.com/15/ffd203/000000?text=+) `#ffd203` |



> **Ikke implementert ennå
> 
> **På oppdrag må/bør endre farge?
> 
> RO viser ikke tekst, bare farge
> 
> CO viser tekst og farge



Eksempel på status visning fra CO:

![](C:\Users\bernt\AppData\Roaming\marktext\images\2020-10-15-11-08-13-image.png)



Exempel på extendedState objekt i getboats feed:

```json
"extendedState": {
"StatusId": 0,
"StatusText": "Ledig, på basen/patrulje",
"ColorCode": "#008000"
}
```


