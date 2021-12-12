# projekti
Projekti Tero Karvisen palvelienhallinta kurssille https://terokarvinen.com/2021/configuration-management-systems-palvelinten-hallinta-ict4tn022-2021-autumn/. Projektissa aioin tehdä asentaa Nginxin ja tehdä testisivut sille ja tehdä siitä moduulin.

Teen projektin kahdella Debian 11 bullseye vagrant koneella jotka olen luonut virtualboxissa olevalle ubuntu 20.04 serverille. Vagrant koneet eivät ole uusia sillä en ole aikaisemmin asentanut Nginxiä niille.

Aloitin projektin asentamalla Nginxin manuaalisesti eli 'sudo apt-get install nginx'. Myös sivujen luonti ja konfigurointi tehdään aluksi käsin.

Aloitetaan luomaan hakemisto ja varmistamalla vaadittavat oikeudet.
'''
sudo mkdir /var/www/html/debian.lan
sudo chmod -R 755 /var/www/html/
'''
Seuraavaksi aletaan konfiguroimaan Nginxiä. Otin kopion alkuperäisestä testisivusta ja tein siihen muutoksia.
![image](https://user-images.githubusercontent.com/94476967/145728062-bc140e7a-e424-471a-b7f5-6236dc0bd00d.png)

Otin pois kaiken joka viittaa alkuperäiseen testisivuun ja muutin rootin ja palvelimen polun.

Tehtyäni tämän käynnistin nginxin uudelleen ja asensin 'curl' paketin jotta voin tarkistaa toimiiko se.
![image](https://user-images.githubusercontent.com/94476967/145728388-e9f52c3d-e75f-4f2c-b3dd-4a284ffdf9c4.png)

Totta kai koska vielä alkuperäinen sivu on olemassa niin se ottaa yhteyden siihen, elikkä poistin sen tiedoston komennolla 'sudo rm /etc/nginx/sites-enaled/default' ja poistin symboolisen linkin oman sivun ja testisivun väliltä.
![image](https://user-images.githubusercontent.com/94476967/145733951-a016813c-af6b-4fed-b6d8-06a23b40744f.png)
![image](https://user-images.githubusercontent.com/94476967/145734010-4ab26bca-2c8b-4428-a585-7d6a494aac8f.png)


Tässä kohtaa olin testannut samat muutokset copypastella ja välillä demoni toimi ja välillä ei joten luovutin ja vaihoin aihetta
Lähteinä käytin: https://stackoverflow.com/questions/51525710/nginx-failed-to-start-a-high-performance-web-server-and-a-reverse-proxy-server/51527784
https://ostechnix.com/how-to-setup-nginx-server-blocks-in-ubuntu-18-04-lts/
