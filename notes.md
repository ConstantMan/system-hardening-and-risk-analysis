# Net_Security 

# Commands List

`scp /home/host/Documents/.zshrc terminator@192...:/home/terminator` // sends files from host to machine 
<br>
`sudo apt-get update`  // Fetches the latest version of the package list from your distro's software repository
<br>
`timedatectl` // Timestamp
<br>
`sudo apt upgrade` // More aggressive update not recommended

<br>
`ip a // identifies every device` connected to the internet
<br>
`sudo apt autoremove` // Remove unwanted packages
<br>
`chch` // Change shell  (from bash to Zsh)
<br>
`cd /etc/netplan` // changes your current directory to the /etc/netplan directory. 
<br>
`sudo nano 00-installer-config.yaml` // will open the file named 00-installer-config.yaml located in the /etc/netplan directory using the Nano text editor with administrative privileges.
<br>
`sudo apt install openssh-server` // installs the OpenSSH server on your Ubuntu system. 
<br>
`sudo systemctl start` // This command starts the SSH service 
<br>
`sudo nano /etc/ssh/sshd_config` // Config sshd (server side) file
<br>
`sudo systemctl restart ssh` // Restart after saving changes
<br>
`sudo ufw enable`
<br>
`sudo ufw numbered`
<br>
`sudo ufw allow ssh`
<br>
`sudo ufw 
<br>
`dpkg -s` // command is used to query information about a specific installed package on a Debian-based system, such as Ubuntu. 
# Useful Links

https://upcloud.com/resources/tutorials/configure-iptables-ubuntu  //Iptables
<br>
https://www.tecmint.com/create-network-bridge-in-ubuntu/  //Bridging
<br>
https://linuxconfig.org/how-to-configure-static-ip-address-on-ubuntu-18-04-bionic-beaver-linux
<br>
https://support.cartika.com/portal/en/kb/articles/iptables-essentials#service-ssh
A3
Removed:Telnet (Remeber to mension it is insecure),snapd,rsynch,Plymouth
Γ1
/var/log/syslog-ng.log {
    weekly            # Rotate logs weekly
    missingok         # Ignore missing log files
    rotate 4          # Keep up to 4 rotated log files
    compress          # Compress rotated log files
    delaycompress     # Delay compression until the next rotation cycle
    notifempty        # Do not rotate if the log file is empty
    create 0644 root root  # Set permissions for new log files
}
# Steps per Stage

Stage A

A1
JUST DO IT!

A2
Δίνουμε στο VM την δίκη του IP με την ρύθμιση bridge
<br>
Επιλέγουμε -> Ecrypt the VM  group LUKS  (LUKS: standard hard drive encryption technology for major Linux systems including Ubuntu)
<br>
Passphrase -> {pass2024}
<br>
Name -> {terminator}
<br>
Server name -> {skynet}
<br>
Password -> {terminator2024}
<br>
Γράφουμε -> sudo apt update
<br>
Γράφουμε -> sudo apt upgrade
<br>
Γράφουμε -> ip a 
<br>
Γράφουμε -> sudo apt install openssh-server
<br>
Γράφουμε -> sudo nano /etc/netplan/static.yaml

NOTES
1. Remember configure route accesss
2. Remember to make login with keys instead of passwords
3.https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04
Warning: As of July 2022, an error will occur when you run the mysql_secure_installation script without some further configuration. The reason is that this script will attempt to set a password for the installation’s root MySQL account but, by default on Ubuntu installations, this account is not configured to connect using a password.

Βηματα που δεν εχουν γινει:
!!!!!!!!!!Επαληθεύστε την ακεραιότητα κα την αυθεντικότητα των πακέτων λογισμικού που
εγκαθιστάτε στο σύστημα σας ενεργοποιώντας GPG (GNU Privacy Guard) ελέγχους
στους διαχειριστές πακέτων λογισμικού όπως είναι ο apt, yum, dnf κλπ.
Β8. Ελέγξτε τακτικά τους λογαριασμούς χρηστών και τα δικαιώματα τους με εντολές
του συστήματος όπως "getent passwd" και "getent group", διασφαλίζοντας ότι δεν
υπάρχουν μη εξουσιοδοτημένοι λογαριασμοί.
Γ4.Ενημερωησ για αλλαγη αρχειου
Ε.
ΣΤ.
Check with LYnis for bonus stuff.

# Bonus
1. Cleaning Script
id konstantman
uid=1000(konstantman) gid=1000(konstantman) groups=1000(konstantman),998(wheel),996(audio),990(optical),987(storage),985(video),108(vboxusers)
2. SSh https://support.cartika.com/portal/en/kb/articles/iptables-essentials specific ips
3.Nmap on snapshot (DONE!!!!)
4.Επιλεξαμε τα security updates να γινονται αυτοματα ενω τα κανονικα να τα κανουμε χειροκινητα
5.Να προστεθεί να ελέγχονται οι προσπάθειες.

6.B5 unlimited storage admin
7. B5 quota not applied
8. B7 Beware we fucked up
9.Γ1 send messages to host
