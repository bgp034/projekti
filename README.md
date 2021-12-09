# projekti
Projekti Tero Karvisen palvelienhallinta kurssille. Kaikki ei ole vielä päätettyä et tuleeko se lopulliseen mutta ainakin aluksi mietin tehdä jonkin moduulin jota voisi mahdollisesti luomaan toimivat työpisteet halutuilla sovelluksilla ja esimerkiksi avaamalla tietyt ssh-portit.

Aloitan tekemällä moduulin jolla asennetaan muutamia hyödyllisiä paketteja.
pkginstall:
  pkg.installed:
    - name: apache2
    - name: tree
    - name: nano
    - name: openssh-server
alias:
  cmd.run:
    - name: a2enmod alias
    
Portteja voisi myös avata ssh:ta varten  
![image](https://user-images.githubusercontent.com/94476967/145321288-8b28e3a5-0de9-45b5-9db9-cef1e93b5c38.png)
Myös tiedosto josta konffataan pitää tehdä
