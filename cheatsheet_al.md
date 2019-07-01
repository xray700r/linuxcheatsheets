## Informacion i sistemit

#### uname -a
* Lloji i kernelit
* Hostname
* Versioni i kernelit
* Momentit e upgradit te fundit
* Arkitekturen
* Shiko man uname

#### cat /etc/os-release
* Shfaq informacione mbi instalimin aktual te OS

#### uptime
* Kohen aktuale
* Kohen qe ka kaluar nga reboot i fundit
* Sa perdorues jane aktualisht logged in
* Ngarkesen ne perqindje te sistemit ne 1, 5 dhe 15 minutat e kaluara

#### hostname
* Shfaq hostname te sistemit
* -i shfaq adresen ip
* shiko man hostname

#### last
* Tregon historikun e aksesit ne sistem nga perdoruesit
* reboot - tregon  historikun e reboot
* shiko man last

#### date
* Tregon oren dhe daten aktuale te sistemit
* -s STRING vendos daten e pershkruar nga STRING
* shiko man date per formatin

#### cal
* Tregon kalendarin per muajin aktual
* -n n tregon kalendarin per n muaj
* Shiko man cal per lloje te ndryshme kalendaresh dhe formatesh

#### neofetch
* Shfaq info te pergjithshme mbi sistemin
* perfshin disa nga informacionet e mesiperme
* instalohet nga paketa neofetch

## Informacione mbi Hardware

#### dmesg
* Shfaq mesazhet e kernelit

#### cat /proc/meminfo 
* Shfaq informacione per secilen berthame te procesorit

#### cat /proc/meminfo
* Shfaqe informacione per memorien RAM

#### free
* Shfaq memorien ram te perdorur, te lire, cache,  swap dhe te perdorshme
* -h tregon vlerat numerike ne format te lexueshem nga njeriu (GB, MB)
* -m tregon vlerat numerike ne MB
* -g tregon vlerat numerike ne GB

#### lspci -tv
* Shfaq nderfaqet pci te perdorura

#### lsusb -tv
* Shfaq nderfaqet usb te perdorura

#### hdparm
* nderfaqe kontrolli per pajisjet e memories
* -i /dev/sda informacion per diskun sda
* -y /dev/sda dergo sinjalin e fikjes per diskun sda
* -tT /dev/sda teston shkrimin dhe leximin mbi diskun sda
* shiko man hdparm, KUJDES: KOMANDE SHUME E RREZIKSHME

#### badblocks
* -s /dev/sda teston per blloqe te demtuara ne diskun sda

## Performanca dhe statistikat

#### top
* shfaq proceset normale
* htop eshte alternative interaktive

#### mpstat
* shfaq aktivitet aktuale te cdo berthame te procesorit

#### vmstat
* shfaq statistikat e memories virtuale qe nga ndezja

#### iostat
* shfaq statistikat e input output
* shiko man iostat per specifika

#### journalctl -xe
* shfaq mesazhet e sistemit init
* ekuivalenti i dmesg per userspace

#### tcpdump
* kap dhe shfaq paketat ne device dhe porten e dhene si argument
* psh: tcpdump -i eth0 'port 80' ose tcpdump -i eth0 

#### lsof
* shfaq filet e hapura
* merr si argument user, pajisje ose file dhe shfaq filet e hapura
mbi argumentin ose nga argumenti

#### df
* Tregon hapesiren boshe ne disqet e dhena si argument
* Nese nuk ka argument tregon hapesiren boshe per te gjitha disqet e montuara
* -h shfaq vlerat numerike ne menyre te lexueshme nga njeriu (MB, GB)
* shiko man df per specifikime

#### du
* Tregon hapesiren e zene nga file ose directory e dhene si argument
* -s per direktori tregon shumen e hapesires se zene per cdo file te saj
* -h shfaq vlerat numerike ne menyre te lexueshme nga njeriu (MB, GB)
* shiko man du per specifikime

#### watch
* ekzekuton nje komande ne interval te caktuar
* -n N - N percakton numrin e sekondave te intervalit

#### Informacion dhe menaxhim i perdoruesve

## whoami
* Shfaq emrin e userit

## id
* shfaq emrin dhe grupet ne te cila perket useri 
* shfaq informacionet dhe ne ekuivalentin e tyre uid/gid
* shiko man id per specifika

## who
* Shfaq terminalet e alokuara ne sistem,  perdoruesin e tyre, dhe kur jane alokuar

## w
* Shfaq perdoruesit e loguar dhe shell qe po perdorin

## groupadd
* krijon grup me emer si argumenti
* psh groupadd test krijon grup me emer test

## useradd
* krijon user
* -m krijon home directory me emrin e userit
* -c krijon koment per userin
* psh useradd -m -c 'TEST' user1 krijon nje user user1 me koment 'TEST' dhe home ne /home/user1

## usermod
* modifikon user ekzistues
* -aG group user - shton userin user ne grupin group si grup sekondar
* -ag group user - shton userin user ne grupin group si grup primar

## Files dhe directories

#### ls
* liston filet ne direktorine e dhene si argument, default eshte direktoria aktuale
* -a liston filet e fshehura
* -l liston informacionin e plote
* -R liston nendirektorite ne menyre rekursive
* -d liston vete direktorine e dhene si argument, jo permbajtjen e saj

#### pwd
* shfaq direktorine aktuale
* -L shfaq adresen fizike te direktorise aktuale, pa marre parasysh linket simbolike

#### mkdir
* krijon nje direktori
* -p krijon te gjitha direktorite parent nqs nuk ekzistojne

#### rm
* fshin nje file
* -r fshin direktorine dhe permbajtjen e saj ne menyre rekursive
* -f nuk kerkon konfirmim
* -d fshin direktorine nqs eshte boshe

#### cp
* kopjon nje file
* psh cp file1 file2 - kopjon file1 ne file2
* -f mbishkruaj file nqs ekziston
* -r kopjon direktori

#### mv
* leviz nje file dhe ndryshoi emrin
* psh mv file1 file2 - file1 shnderrohet ne file2
* nese file2 ekziston dhe eshte direktori, file1 perfshihet ne te

#### ln
* krijon linke fizike ne filesystem
* linket fizike NUK mund te krijohen nga nje particion tek tjetri
* -s krijon linke simbolike, nuk vlen me nqs objekti fillestar fshihet
* linket simbolike MUND te krijohen nga nje particion tek tjetri

#### touch
* updaton nje file
* nqs file nuk ekziston krijohet

#### cat
* printon te dhenat e marra nga nje file (qe mund te jete dhe stdin) ne stdout

#### less
* program pager, thjeshteson leximit e fileve te medha

#### head
* shfaq 10 rreshtat e para te nje file duke perdorur programin pager default
* -n N - shfaq N rreshtat e para

#### tail
* shfaq 10 rreshtat e fundit te nje file duke perdorur programin pager default
* -n N - shfaq N rreshtat e fundit
* -f vazhdon lexon file nderkohe qe shkruhet

## Menaxhimi i proceseve

#### ps
* shfaq proceset ne sistem
* e shfaq te gjitha proceset
* f format i plote
* l format i gjate
* a shfaq proceset normale (qe lidhen me nje terminal ose jane krijuar nga perdoruesi)
* u shfaq proceset e perdoruesit
* x shfaq dhe proceset qe nuk jane krijuar nga nje TTY
* SHENIM: te gjithe argumentat e mesiperm mund te perdoren duke u bashkuar por sygjerohet
te mos perdoren me "-" perpara ne sistemet GNU/Linux

#### kill
* ndalon procesin e dhene si argument
* -N - N percakton llojin e sinjalit, shiko man kill
* nqs argumenti ka "%" perpara do te merret si pid relative e shellit ne perdorim
* psh kill %N ndalon procesin nr N ne background te shellit ndersa kill N ndalon procesin
me numer N ne sistem
* killall arg - ndalon te gjitha proceset qe i fillon emri me 'arg'

#### bg
* shfaq programet qe ndodhen ne background
* per te kaluar nje program ne background e therret me '&' ne fund (psh 'badblocks /dev/sda &') ose shtyp ctrl-Z nderkohe
qe po ekzekutohet.

#### fg
* nxjerr ne foreground programin e pare ne background
* merr argument %N ku nxjerr ne foreground programin e N't ne background

## Te drejat e aksesit mbi file

#### Formati Trwxrwxrwx
* T - mund te jete '-' per file ose d per directory, per opsione te tjera shih man ls
* rwx - read write execute, tregon cfare i lejohet grupimit te caktuar mbi kete file
* grupimi i pare i referohet userit pronar
* grupimi i dyte i referohet grupit pronar
* grupimi i trete i referohet perdoruesve te cilet nuk bejne pjese te grupimet e mesiperme

#### Formati NNN
* N e pare i referohet userit pronar
* N e dyte i referohet grupit pronar
* N e trete i referohet perdoruesve te cilet nuk bejne pjese te grupimet e mesiperme
* N mund te kete vlera nga 0 ne 7 ku 0 tregon se nuk ka te drejta dhe 7 se i ka te gjitha
* Per te plotesuar vleren e N pranohet konvencioni i tille:
	* read = 4
	* write = 2
	* execute = 1
* pra nqs nje user ka te drejta shkrimi dhe leximi por jo ekzekutimi vlera e N per te do te ishte
4+2 = 6

Per te ndryshuar menyrene aksesit perdoret komanda chmod
	chmod NNN file
Per te ndryshuar pronarin perdoret komanda chown
	chown user.group file

## Rrjeti

#### ifconfig
* -a Shfaq informacion per te gjitha nderfaqet e rrjetit
* shfaq informacionet per pajisjen e dhene si argument

#### ethtool
* kontrollon gjendjen e hardware dhe kernel per pajisjen e dhene si argument

#### ping
* dergon nje pakete ICMP drejt adreses se dhene si argument dhe pret pergjigje
* shiko man ping per specifika

#### whois
* shfaq informacion mbi pronarin e nje domain

#### dig
* shfaq informacion mbi DNS e nje domain
* -x reverse lookup

#### host
* shfaq DNS e nje domain

#### wget
* performon nje GET request tek adresa e dhene si argument (shumicen e rasteve shkarkohet si file)

#### netstat
* shfaq informacion per network sockets
* shiko man netstat per detaje

## Arkivat tar
```sh
tar cvf arkiva.tar /adresa/e/direktorise # Krijone nje arkive me emer arkiva.tar me direktorine e dhene
tar xvf arkiva.tar # ekstrakton permbajtjen e arkives ne direktorine aktuale
tar xvf arkiva.tar /file/ne/arkive ekstrakton vetem filen e dhen
```
#### Opsione shtese
* C vendos adresen ku behet ekstraktimi
* z ekstrakton arkiva gzip (.tar.gz), perdoret bashke me opsionin x dhe f
* j arkivon ne formatin bz2 (.tar.bz2) kur perdoret bashke me opsionin c dhe f
* j ekstrakton ne formatin bz2 (.tar.bz2) kur perdoret bashke me opsionin x dhe f


## Menaxhimi i paketave per sistemet e familjes Red Hat
```sh
yum whatprovides binary # Kerkon paketen qe ofron binarin binary
yum search package # Kerkon paketen me emrin package
yum install package # instalon paketen me emrin package
yum info package # jep informacione per paketen package
yum remove package # cinstalon paketen me emrin package
rpm -i /adrese/e/file.rpm # instalon pakete nga nje file rpm

# Istalim nga source, aplikohet ne cdo sistem nqs eshte
# pakete e vlefshme dhe nqs jane te instaluara te gjitha varesite
# Ne fillim shkarkohet source code nga github apo faqja e projektit
# supozojme se e kemi shkarkuar dhe e kemi ruajtur ne direktorine ./program
cd ./program
mkdir build
cd build
# Duhet lexuar me kujdes README e programit sepse ne disa raste
# Eshte e nevojshme te behet konfigurimi per sistemin e caktuar
../configure
make
sudo make install
```
## Menaxhimi i paketave per sistemet e familjes Debian
```sh
apt search package # Kerkon paketen me emrin package
apt install package # instalon paketen me emrin package
apt remove package # cinstalon paketen me emrin package
apt purge package # nuk ruan filet e konfigurimit te paketes pasi cinstalohet
dpkg -i /adrese/e/file.deb # instalon pakete nga nje file rpm
```

## Kerkimi i tekstit ne file
```sh
grep 'tekst' file # afishon te gjithe rreshtat qe permbajne stringun 'tekst' ne file
grep -r 'tekst' directory # afishon te gjithe rreshtat qe permbajne stringun 'tekst' ne cdo file ne direktorine directory
sed 's/abc/xyz/Ig' 'file.txt' # Kerko tekstin 'abc' brenda file.txt dhe zevendesoje me 'xyz'
awk -F':' '{print $1,$3,$4;}' /etc/passwd  # Printo kollonat 1 3 dhe 4 te ndara nga karakteri : ne file /etc/passwd
diff -c file1.txt file2.txt # Gjej ndryshimet midis fileve file1.txt dhe file2.txt ne kontekst (-c)
locate john # Gjej filet dhe direktorite me emer 'john'.
find /home/john -name 'down*' # Kerko per file ne /home/john qe fillojne me "down".
find /home -size +100M # Kerko per file me dimensione mbi 100MB ne /home
```

## SSH
```sh
ssh host # ben lidhje ssh me emrin e userit aktual ne adresen host
ssh user@host # ben lidhje ssh me emrin user ne adresen host
ssh -p PP user@host # ben lidhje ssh me emrin user ne adresen host ne porten PP
```

## Transferimi i fileve
```sh
scp file.txt host:/path/to/copy # ben kopje nepermjet ssh te nje filet file.txt tek adresa e specifikuar ne host
# scp suporton shumicen e opsioneve te cp si -r, -f etj
sftp -P PP user@host # ben lidhje ssh me emrin user tek adresa host me porten PP per te bere transferta interaktive filesh
rsync -a /home /backups/ # Sinkronizo /home ne /backups/home
rsync -avz /home 192.168.10.1:/backups/ # Sinkronizo files/directories midis sistemit local dhe direktorise backups ne server me IP 192.168.10.1
```
