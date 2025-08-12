# LAB-4
tanggal 12 agustus 2025
# Command Line Interface [terminal] pada mikrotik
selain merimote mikrotik dengan mode GUI kita juga bisa dengan cara CLI Command Line Interface [terminal].  
Bisa di akses via winbox terminal, webfig terminal, putty, mikrotik pro untuk smartphone. 

cotoh :  
via winbox terminal
![y](tl.PNG) 

    untuk memulai configurasi tekan ctrl+c 
![y](tl1.PNG) 

# selanjutnya saya akan menuliskan beberapa perintah CLI dasar:  
1. jika kalian ingin memasukan ip-dhcp client maka commadnya:
   
        ip dhcp-client add interface=ether1 use-peer-dns=yes use-peer-ntp=yes add-default-route=yes disabled=no
   
3. mengganti identitas mikrotik:

       system identity set name=(RB-Blajar-Fuzi)
   
5. melihat interfaces:

        interface print
   
7. mengganti nama interfaces:

       interface set name=(ether1-ISP) ether1

8. melihat ip address:
  
        ip address print / ip ad pr
    
9. menambahkan ip address:

        ip address add address=10.10.10.1/24 interfaces=(ether2)
    
10. melihat Gateway:

        ip route print
    
11. menambahkan Gateway:

        ip route add gateway=10.10.2.1
    
12. melihat DNS:

        ip dns print

13. menambahkan DNS:

        ip dns set server=8.8.8.8(ip google) allow-remote-requests=yes
    
14. menambahkan perintah NAT:

        ip firewall nat add chain=srcnat action=masquerade out-interfaces=ether1-ISP

    
15. melihat configurasi NAT:

        ip firewall nat prnit
    
17. Membuat user baru dan password dengan hak akses full:

        user add name=fuzi group=full password=fuzi123
    
21. melihat user:

        user prnit
    
23. melihat lisensi

        system license prnit

    

   



