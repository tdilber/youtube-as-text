# youtube-as-text

TODO: 

- Youtube ta bulunan dinlenmesi gereken youtuberlar ozelinde uretmis olduklari videolarin speech recognizer ile text haline getirip, insanlarin 2* te dinletmek zorunda kalimamasi saglanmali. 
- Youtube icinden once sesler cikartilacak. Bu sesler kaydedilecek. Bu kayitlar ile speech recognation yapilacak. 
- Bir cumleyi gerekirse bu kaydetilen sesler uzerindne dinlenilebiliecek. (mouse select and listen tarzi mesela)
- Youtube video zamani recognized text'lerin icine gomulecek. (mesela bir texte sag tiklandiginda videonin ilgili ksimina gidilecek.)
- Giren kisilerin texleri fixleyebilme ozgurukleri olmali ve burada herkes herkesin editini gorup o editi degistirebilmeli. 
- Editler icine Video icinden foto cekeme ozelligi eklenmeli. Grfikler icin vs. (mesela texte sag tikla ve video bolumunu ifframe de ac. sonra foto cek'e bas ve gerekirse kare seklinde kirparak kaydet.)
- Edit ustune edit yapiplip git history mantigi isletilebilmeli. 
- Editler arasinda +1 -1 oy kullandirilarak en cok oy alanlar uste cikartilsin ve editleyip +1 alanlar odullendirilsin. 
- (Ileri ki asalamar icin kotu niyetli editterlar ve kotu niyetli puanlayicilar tespit edi)
- (Ileriki asamalarda belki chrome extension yazilabiir)


Tecnical: 
- Speech recongize isleri bir Djangolu bir Python microservice icinde yapilabilir. 
- Speech recognation icin google service'i de ileride entegre edilebilir. (yeni microservice olarka)
- Bir next.js ile front yapilacak. 
- Spring boot ile bir db ile bu Kullanici history islerini tutan moduler bir monolithc ile hizli bir dev sureci isletilebilir. 
- Resimleri ve ses kayitlarini kaydetmek icin bir s3 gibi bir file storage

DB Tables or Data models: 
User
Video
- id 
- youtube_id
- length
- read_count
VideoText
- video_id
- content
UserVideoVote
- user_id
- video_id
- video_text_id
- vote
VideoImage
VideoSound

Enpoints: 
- User login
- user register 
- forgot password

- post regognize video  [need autohorize]
- get video list
- get video by id (most voted and original regonized)
- get video by youtube id 
- post edit video [need autohorize]
- get video text history (sort by votes)
- get video sound by two part. 
- get video sound
- post video image [need autohorize]
- post vote video text (up down) [need autohorize]

Tecnical Challanges
- Bir video icersiinde her bir kelimenin kacinci saniyede oldugunu bulabilmek gerekiyor. (regonizer yapabiliyorsa cok iyi olacak)
