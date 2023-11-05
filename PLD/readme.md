# EXDOS
### PLD equations
/* *************** INPUT PINS *********************/
PIN 1   = A20     ; /* A20 */ 
PIN 2   = A19     ; /* A19 */
PIN 3   = A18     ; /* A18 */ 
PIN 4   = A7      ; /* A7 */ 
PIN 5   = A6      ; /* A6 */ 
PIN 6   = A5      ; /* A5 */
PIN 7   = A4      ; /* A4 */ 
PIN 8   = A3      ; /* A3 */ 
PIN 9   = A2      ; /* A2 */ 
PIN 10  = A1      ; /* A1 */ 
PIN 11  = !IORQ   ; /* IORQ */ 
PIN 13  = !WR     ; /* WR */ 
PIN 14  = !RD     ; /* RD */ 
PIN 15  = !MREQ   ; /* MREQ */ 
PIN 21  = A21     ; /* A21 */ 

/* *************** OUTPUT PINS *********************/
PIN 16  = !WDCE   ; /* enable WD1772 */ 
PIN 17  = !RAMCS  ; /* enable RAM */ 
PIN 18  = !RDE    ; /* read from 244A */ 
PIN 19  = !RDB    ; /* buffered RD */ 
PIN 20  = !WRE    ; /* write to LS273 */ 
PIN 22  = !EXP    ; /* to Enterprise */ 
PIN 23  = !DE     ; /* enable LS245 */

/* *** RDB *** */
RDB     = RD;

/* *** ROMCE *** */
RAMCS   = MREQ & (RD # WR) & A19 & !A20 & !A21;

/* *** IOCE *** */
IOCE    = IORQ & (RD # WR) & A4 & !A5 & !A6 & !A7;

/* *** DE *** */
DE      = ROMCE $ IOCE;

/* *** WDCE *** */
WDCE    = IOCE & !A3;

/* *** EXP *** */
EXP     = DE;

/* *** WRE *** */
WRE     = WR & IOCE & A3;

/* *** RDE *** */
RDE     = RD & IOCE & A3;

/* end */