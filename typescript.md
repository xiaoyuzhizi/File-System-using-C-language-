# Step 1
Use the following command to build:
```
make
```

Start with
```
./BDS <DiskFileName> <#cylinders> <#sector per cylinder> <track-to-track delay><port=10356>
```
and
```
./BDC <DiskServerAddress> <port=10356>
```

For example, use
```
./BDS diskfile.txt 100 100 7 10356
./BDC 10356
```
A file named `diskfile.txt` will be created. Then use command and we can get corresponding output.
```
I
100 100
W 3 4 11 ABCDEFGHIJK
ABCDEFGHIJK
R 3 4
ABCDEFGHIJK
W 3 234 4 QWER              
Error: Invalid write parameters.
E
Bye!
```
you can also use
```
./BDS diskfile.txt 100 100 7 10356
./BDC_random 10356
```
A file named `diskfile.txt` will be created. Then use command and we can get corresponding output.
```
Request 0: I
100 100
Totally 100 cylinders, 100 sectors per cylinder.
Please input the number of R/W requests: 5
Request 1: W 21 85 256 9YVzztafqQH3IfiTOPzBEoOfXbGJq3KnPtMeNKi3rNWXT2GvI4Wciyg3zMCNDc0iwAl9bt0s6KfNDJ89DV9JhfCFP2ii59ppzymARcQLKTpbrlaU4ascdSHTLPZEOcRcA3Ah3hTDY6FfhDYaBgcFWJovmbXZeE1EvpKowrQjljoqMcqegsH1ZTmcU8ZWAOrW3Z8ogOxrVLHyMYAQe5H4OS4wQTjgvy2onZCtBZInzdJ9Z9P44nWG5O2JvbPQzG4
9YVzztafqQH3IfiTOPzBEoOfXbGJq3KnPtMeNKi3rNWXT2GvI4Wciyg3zMCNDc0iwAl9bt0s6KfNDJ89DV9JhfCFP2ii59ppzymARcQLKTpbrlaU4ascdSHTLPZEOcRcA3Ah3hTDY6FfhDYaBgcFWJovmbXZeE1EvpKowrQjljoqMcqegsH1ZTmcU8ZWAOrW3Z8ogOxrVLHyMYAQe5H4OS4wQTjgvy2onZCtBZInzdJ9Z9P44nWG5O2JvbPQzG4
Request 2: R 91 9

Request 3: W 38 98 256 z9FDGEqFkkxv43oGUXZTAFj4yTpRLaZ87vzEXQ77YvqTmCn4ndOOGXI4EWJdWzcRSBlFhjB6CPNMi0Hv1l9y6Gqyq0CcpCR513A7aZ3AFEcNsH8kQ6IMAY9QOzQ11xWQolNo8GOD8PerkdB177BvVAbyZPpOcavrj8DhDgJBTNQ3OfUJck4WK3kyIxcJvvYEupKXvjmcU16z6O89Y3VxU3VtqV0KhOeB3MmnTwpEnj3kY1hKS05DTQU7AKHHoK6
z9FDGEqFkkxv43oGUXZTAFj4yTpRLaZ87vzEXQ77YvqTmCn4ndOOGXI4EWJdWzcRSBlFhjB6CPNMi0Hv1l9y6Gqyq0CcpCR513A7aZ3AFEcNsH8kQ6IMAY9QOzQ11xWQolNo8GOD8PerkdB177BvVAbyZPpOcavrj8DhDgJBTNQ3OfUJck4WK3kyIxcJvvYEupKXvjmcU16z6O89Y3VxU3VtqV0KhOeB3MmnTwpEnj3kY1hKS05DTQU7AKHHoK6
Request 4: W 68 28 256 s6CGAOPrWBi3aZT5sAMcxaK5HWFD1PHiL9O9LrqxTxoTm5OCvoCTocMTYfkNURTuPxtqNIMu5YdfUPHf29We9yYXB6ymOiGrDXHgvhAo6BtOf0R5XE9W0VHsS6Cuc6LFTgKdm8riyJUDxBwl5v7UhDcXzChzyQ4hWCi8ByeX7YosqKDj5z3a23Vpt0ORGGXr95pytsloexHs7aC0xtZnlICEzgm3L7kK2y8kOhySC5bz4DnpUcD3L5w8aG1LDaj
s6CGAOPrWBi3aZT5sAMcxaK5HWFD1PHiL9O9LrqxTxoTm5OCvoCTocMTYfkNURTuPxtqNIMu5YdfUPHf29We9yYXB6ymOiGrDXHgvhAo6BtOf0R5XE9W0VHsS6Cuc6LFTgKdm8riyJUDxBwl5v7UhDcXzChzyQ4hWCi8ByeX7YosqKDj5z3a23Vpt0ORGGXr95pytsloexHs7aC0xtZnlICEzgm3L7kK2y8kOhySC5bz4DnpUcD3L5w8aG1LDaj
Request 5: W 88 67 256 Fak2SMVTbNkm33nwWWpiUnOJWfH5B3a43iWMUItTlE6evjyh5MoNX0mK6SDxLEpFMcfvKyeT0aYlhkraUDNItYipGLKhd0KO0P9ycbh0c5ahepiYSVwbHCpdeXlfLTTBxQZxS7nS0lZ4A5RiPbkmExqGkzLWgvlD9b0R6czWnnPMiuUXv2aZpotyL5iRotlnu95qbsbnFOZO8HztAxhNJA9kvh0HB9VT8O8847jAL6cJDB21X7DwyCFRKvn9u8S
Fak2SMVTbNkm33nwWWpiUnOJWfH5B3a43iWMUItTlE6evjyh5MoNX0mK6SDxLEpFMcfvKyeT0aYlhkraUDNItYipGLKhd0KO0P9ycbh0c5ahepiYSVwbHCpdeXlfLTTBxQZxS7nS0lZ4A5RiPbkmExqGkzLWgvlD9b0R6czWnnPMiuUXv2aZpotyL5iRotlnu95qbsbnFOZO8HztAxhNJA9kvh0HB9VT8O8847jAL6cJDB21X7DwyCFRKvn9u8S
Request 6: E
Bye!
```


# Step 2
```
make
./BDS <DiskFileName> <#cylinders> <#sectors per cylinder> <track-to-track delay> <port=10356>
./FS <DiskServerAddress> <BDSPort=10356> <FSPort=12356>
./FC <ServerAddr> <FSPort=12356>
```
For example, use
```
./BDS diskfile.txt 100 100 7 10356
./FS 10356 12356
./FC 12356
```
Then use command and we can get corresponding output.
```
f
formatted
ls
Current directory size: 0 bytes, last modified: Fri May 31 01:54:48 2024


mk f1
file created!
mkdir d1
file created!
ls
Current directory size: 552 bytes, last modified: Fri May 31 01:55:16 2024

f1      d1
cd d1
Directory changed
ls
Current directory size: 0 bytes, last modified: Fri May 31 01:55:16 2024


cd ..
Directory changed
ls
Current directory size: 552 bytes, last modified: Fri May 31 01:55:16 2024

f1      d1
rmdir d1
directory deleted
ls
Current directory size: 276 bytes, last modified: Fri May 31 01:56:02 2024

f1
rm f1
file deleted
ls
Current directory size: 0 bytes, last modified: Fri May 31 01:56:12 2024


mk f1
file created!
w f 5 hello
File not found
w f1 5 hello
file written
cat f1
hello
i f 10 6 iiihhh
File not found
i f1 10 6 iiihhh
file updated
cat f1
helloiiihhh
ls 
Current directory size: 287 bytes, last modified: Fri May 31 01:59:37 2024

f1
w f1 320 01234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789
file written
cat f1
01234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789
d f1 4 5
file updated
cat f1
012390123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789012345678901234567890123456789
```
# Step 3
```
cd step3
make
./BDS <DiskFileName> <#cylinders> <#sectors per cylinder> <track-to-track delay> <port=10356>
./FS <DiskServerAddress> <BDSPort=10356> <FSPort=12356>
./FC <ServerAddr> <FSPort=12356>
```
For example, use
```
./BDS diskfile.txt 100 100 7 10356
./FS 10356 12356
./FC 12356
```
Then use command and we can get corresponding output.
```
f
formatted
ls
Current directory size: 0 bytes, last modified: Fri May 31 02:11:43 2024


adduser yu 123
directory created!
login yu 123
Login successful
ls
Current directory size: 284 bytes, last modified: Fri May 31 02:11:58 2024

yu
cd yu
Directory changed
mk t
file created!
chmod t 0
Permissions updated
ls
Current directory size: 284 bytes, last modified: Fri May 31 02:12:34 2024

t
cd ..
Directory changed
logout
Logout successful
adduser zhang 789
directory created!
login zhang 78
Error: Authentication failed
login zhang 789
Login successful
cd yu
Directory changed
ls
Current directory size: 284 bytes, last modified: Fri May 31 02:12:34 2024


cd ..
Directory changed
ls
Current directory size: 852 bytes, last modified: Fri May 31 02:13:29 2024

yu      zhang
deluser zhang
directory deleted
ls
Current directory size: 568 bytes, last modified: Fri May 31 02:14:13 2024

yu
e
Bye!
```