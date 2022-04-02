# youtube-as-text

TODO: 

- Youtube ta bulunan dinlenmesi gereken youtuberlar ozelinde uretmis olduklari videolarin speech recognizer ile text haline getirip, insanlarin 2* te dinletmek zorunda kalimamasi saglanmali. 
- Youtube icinden once sesler cikartilacak. Bu sesler kaydedilecek. Bu kayitlar ile speech recognation yapilacak. 
- Youtube video zamani recognized text'lerin icine gomulecek. (mesela bir texte sag tiklandiginda videonin ilgili ksimina gidilecek.)
- Giren kisilerin texleri fixleyebilme ozgurukleri olmali ve burada herkes herkesin editini gorup o editi degistirebilmeli. 
- Editler icine Video icinden foto cekeme ozelligi eklenmeli. Grfikler icin vs. (mesela texte sag tikla ve video bolumunu ifframe de ac. sonra foto cek'e bas ve gerekirse kare seklinde kirparak kaydet.)
- Edit ustune edit yapiplip git history mantigi isletilebilmeli. 
- Editler arasinda +1 -1 oy kullandirilarak en cok oy alanlar uste cikartilsin ve editleyip +1 alanlar odullendirilsin. 
- (Ileri ki asalamar icin kotu niyetli editterlar ve kotu niyetli puanlayicilar tespit edi)


Tecnical: 
- Speech recongize isleri bir Djangolu bir Python microservice icinde yapilabilir. 
- Speech recognation icin google service'i de ileride entegre edilebilir. (yeni microservice olarka)
- Bir next.js ile front yapilacak. 
