# sam

Descifrado de password de windows a partir de los archivos sam y system

ruta (c:\windows\system32\config\)

#1 Obtenemos los usuarios y passwords y guardamos en el archivo hashes.txt
samdump2 -o hashes.txt system.bak sam.bak

#2 Mediante un diccionario intentamos recuperar el password
hashcat -m 1000 -a 0 hashes.txt /usr/share/wordlists/rockyou.txt --show





