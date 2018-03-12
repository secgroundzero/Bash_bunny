## bash bunny script for executing an HTA payload on x64 and x86 machines

1) Create the HTA payload using Cobalt Strike / Unicorn whatever and SharpShooter for evasion

'python SharpShooter.py  --dotnetver 2  --payload hta --rawscfile payload.bin --smuggle --output payload --template mcafee --stageless'

2) Place the script and the payload.hta in either the Switch1 or Switch2 folder of the Bash Bunny


### OPSEC considerations

- The script will attempt to run the HTA file twice. Once for x64 and once for x86
- the script uses mshta.exe. Adjust it according to your situation
