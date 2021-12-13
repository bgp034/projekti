Projekti Tero Karvisen  kurssille https://terokarvinen.com/2021/configuration-management-systems-palvelinten-hallinta-ict4tn022-2021-autumn/. Projektissa aioin tehdä asentaa apachen ja tehdä testisivut sille ja tehdä siitä moduulin joka loisi sivut myös uusille käyttäjille.

Teen projektin Ubuntu 20.04 server virtuaalikoneella joka on virtualboxissa ja siinä on salt master ja minion. Aioin eka testata manuaalisesti sitten tehdä moduulin.

Aluksi luon '/etc/skel/' hakemistoon uuden index.html tiedoston jolla varmistan että uusi käyttäjä saa tiedoston. 
![image](https://user-images.githubusercontent.com/94476967/145738142-74f18150-b9a6-431a-a304-fb0192c1b83e.png)

![image](https://user-images.githubusercontent.com/94476967/145738439-9d0631cb-dc11-42e7-9dd4-11378b4135e5.png)

toimi.

Sitten päätin alkaa automatisoimaan.

![image](https://user-images.githubusercontent.com/94476967/145738763-8fde29c4-4832-4ea7-a35b-42ae6b07576e.png)





![image](https://user-images.githubusercontent.com/94476967/145740019-0835f5ac-76a4-485d-8b88-8cae17bdd4a6.png)
