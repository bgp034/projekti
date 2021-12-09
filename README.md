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

portit
/etc/ssh/sshd_config:
  file.managed:
    - source: salt://sshd/sshd_config
Myös kyseiseen tiedostoon pitäisi tehdä muutoksia.
