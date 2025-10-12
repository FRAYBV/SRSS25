## Descripción
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.
Additional details will be available after launching your challenge instance.
## Solución
```
ssh -p 62467 ctf-player@saturn.picoctf.net
The authenticity of host '[saturn.picoctf.net]:62467 ([13.59.203.175]:62467)' can't be established.
ED25519 key fingerprint is SHA256:lMXKIC17ONzyUJx7ZYBY5VSwoxCz20uq5/Nm+IhXKew.
This host key is known by the following other names/addresses:
    ~/.ssh/known_hosts:1: [hashed name]
    ~/.ssh/known_hosts:2: [hashed name]
    ~/.ssh/known_hosts:5: [hashed name]
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[saturn.picoctf.net]:62467' (ED25519) to the list of known hosts.
ctf-player@saturn.picoctf.net's password:
Specialer$ echo *
abra ala sim
Specialer$ echo .* *
. .. .hushlogin .profile abra ala sim
Specialer$ echo .* */*
. .. .hushlogin .profile abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt
Specialer$ echo .* */* */.*
. .. .hushlogin .profile abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt abra/. abra/.. ala/. ala/.. sim/. sim/..
Specialer$ echo .* */* */.*
. .. .hushlogin .profile abra/cadabra.txt abra/cadaniel.txt ala/kazam.txt ala/mode.txt sim/city.txt sim/salabim.txt abra/. abra/.. ala/. ala/.. sim/. sim/..
Specialer$ echo "$(<abra/cadabra.txt)"
Nothing up my sleeve!
Specialer$ echo "$(<abra/cadaniel.txt)"
Yes, I did it! I really did it! I'm a true wizard!
Specialer$ echo "$(<ala/kazam.txt)"
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_811ae7e9}
```
## Notas adicionales

## Referencias