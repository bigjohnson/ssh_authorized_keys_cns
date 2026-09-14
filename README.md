
## Installazione chiave pubblica.
1. Levare tutte le carte sia contact che contactless da tutti i lettori smartcard.
3. Installa un lettore usb compatibile con la CNS, io uso un lettore ACS ACR38 bit4id.
4. Io ho una carta ACJ 2025 ed ho installato il software di gestione della carta preso dalla pagina del Sistema Tessera Sanitaria
5. Collegare il lettore alla porta usb e inserire la carta, nel mio lettore se la carta è inserita correttamente si accende un led verde.
6. Installare il programma putty-cac, che è una versione di putty che ha una modifica per gestire il Common Access Card.
7. Aprire un prompt di dos con il comando cmd.exe
8. Lanciare il comando certutil.exe -scinfo per leggere la carta.
9. Inserire il pin della carta quando richiesto.
10. Aprire il programma pageant.exe che fa parte del pacchetto putty.
11. Cliccare sul bottone Add CAPI_Cert
12. Deve uscire il certificato dela carta inserita, con il codice fiscale della persona intestataria della carta e l'ente emettitore, nel mio caso Regione Lombardia - CA Cittadini 2020.
13. Cliccare su OK.
14. Inserire il pin della carta.
15. Nella Pageant Key List viene aggiunta una linea con il certificato, che contiene anche il codice fiscale della persona intestataria della CNS.
16. Selezionare con il mouse la linea del certificato.
17. Premere sul bottone Copy To Clipboard.
18. Fare il login sulla macchina nella quale si vuole aggiungere la chiave pubblica nel file .ssh/authorized_keys
 
## Effettuare il login.
1. Collegare il lettore.
2. Inserire la carta.
3. Aprire un prompt di dos con il comando cmd.exe
4. Lanciare il comando certutil.exe -scinfo per leggere la carta.
5. Inserire il pin della carta quando richiesto.
6. Aprire pageant.exe.
7. Cliccare sul bottone Add CAPI_Cert
8. Deve uscire il certificato dela carta inserita, con il codice fiscale della persona intestataria della carta e l'ente emettitore, nel mio caso Regione Lombardia - CA Cittadini 2020.
9. Cliccare su OK.
10. Inserire il pin della carta.
11. Aprire putty.exe
12. Collegatevi al server nel quale avete inserito la chiave pubblica.
13. Inserire il pin della carta quendo richieto.
14. Compare il prompt della macchina.
