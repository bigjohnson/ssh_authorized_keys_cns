
## Installazione chiave pubblica.
1. Installa un lettore usb compatibile con la CNS, io uso un lettore ACS ACR38 bit4id.
2. Io ho una carta ACJ 2025 ed ho installato il software di gestione della carta preso dalla pagina del Sistema Tessera Sanitaria
3. Collegare il lettore alla porta usb e inserire la carta, nel mio lettore se la carta è inserita correttamente si accende un led verde.
4. Installare il programma putty-cac, che è una versione di putty che ha una modifica per gestire il Common Access Card.
5. Aprire un prompt di soc con il comando cmd.exe
6. Lanciare il comando certutil.exe -scinfo per leggere la carta.
7. Inserire il pin della carta quando richiesto.
8. Aprire il programma pageant.exe che fa parte del pacchetto putty.
9. Cliccare sul bottone Add CAPI_Cert
10. Deve uscire il certificato dela carta inserita, con il codice fiscale della persona intestataria della carta e l'ente emettitore, nel mio caso Regione Lombardia - CA Cittadini 2020.
11. Cliccare su OK.
12. Nella Pageant Key List viene aggiunta una linea con il certificato, che contiene anche il codice fiscale della persona intestataria della CNS.
13. Selezionare con il mouse la linea del certificato.
14. Premere sul bottone Copy To Clipboard.
15. Fare il login sulla macchina nella quale si vuole aggiungere la chiave pubblica e aggiungerla nel file .ssh/authorized_keys
 
## Effettuare il login.
2.  A questo punto per fare il login sulla macchina basta 
