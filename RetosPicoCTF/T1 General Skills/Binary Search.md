## Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/19/challenge.zip)

`ssh -p 55517 ctf-player@atlas.picoctf.net`Using the password `1db87a14`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
## Solución
```
mkdir bsh
FRAY30-picoctf@webshell:~$ cd bsh/
FRAY30-picoctf@webshell:~/bsh$ wget https://artifacts.picoctf.net/c_atlas/19/challenge.zip
--2025-11-03 05:22:12--  https://artifacts.picoctf.net/c_atlas/19/challenge.zip
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.72, 3.170.131.33, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.72|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1041 (1.0K) [application/octet-stream]
Saving to: 'challenge.zip'

challenge.zip     100%[===========>]   1.02K  --.-KB/s    in 0s      

2025-11-03 05:22:13 (340 MB/s) - 'challenge.zip' saved [1041/1041]

FRAY30-picoctf@webshell:~/bsh$ unzip challenge.zip 
Archive:  challenge.zip
   creating: home/ctf-player/drop-in/
  inflating: home/ctf-player/drop-in/guessing_game.sh  
FRAY30-picoctf@webshell:~/bsh$ cd home/ctf-player//drop-in/
FRAY30-picoctf@webshell:~/bsh/home/ctf-player/drop-in$ ls
guessing_game.sh
FRAY30-picoctf@webshell:~/bsh/home/ctf-player/drop-in$ cat guessing_game.sh 

            #!/bin/bash

            # Generate a random number between 1 and 1000
            target=$(( (RANDOM % 1000) + 1 ))

            echo "Welcome to the Binary Search Game!"
            echo "I'm thinking of a number between 1 and 1000."

            # Trap signals to prevent exiting
            trap 'echo "Exiting is not allowed."' INT
            trap '' SIGQUIT
            trap '' SIGTSTP

            # Limit the player to 10 guesses
            MAX_GUESSES=10
            guess_count=0

            while (( guess_count < MAX_GUESSES )); do
                read -p "Enter your guess: " guess

                if ! [[ "$guess" =~ ^[0-9]+$ ]]; then
                    echo "Please enter a valid number."
                    continue
                fi

                (( guess_count++ ))

                if (( guess < target )); then
                    echo "Higher! Try again."
                elif (( guess > target )); then
                    echo "Lower! Try again."
                else
                    echo "Congratulations! You guessed the correct number: $target"

                    # Retrieve the flag from the metadata file
                    flag=$(cat /challenge/metadata.json | jq -r '.flag')
                    echo "Here's your flag: $flag"
                    exit 0  # Exit with success code
                fi
            done

            # Player has exceeded maximum guesses
            echo "Sorry, you've exceeded the maximum number of guesses."
            exit 1  # Exit with error code to close the connection

            FRAY30-picoctf@webshell:~/bsh/home/ctf-player/drop-in$ 
FRAY30-picoctf@webshell:~/bsh/home/ctf-player/drop-in$ cd..
-bash: cd..: command not found
FRAY30-picoctf@webshell:~/bsh/home/ctf-player/drop-in$ cd 
FRAY30-picoctf@webshell:~$ 
FRAY30-picoctf@webshell:~$ cd home/ctf-player//drop-in/
-bash: cd: home/ctf-player//drop-in/: No such file or directory
FRAY30-picoctf@webshell:~$ cd bsh/
FRAY30-picoctf@webshell:~/bsh$ cd home/ctf-player//drop-in/
FRAY30-picoctf@webshell:~/bsh/home/ctf-player/drop-in$ cd ..
FRAY30-picoctf@webshell:~/bsh/home/ctf-player$ cd ..
FRAY30-picoctf@webshell:~/bsh/home$ cd ..
FRAY30-picoctf@webshell:~/bsh$ ssh -p 55517 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:55517 ([18.217.83.136]:55517)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? eyes
Warning: Permanently added '[atlas.picoctf.net]:55517' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 600
Lower! Try again.
Enter your guess: 500
Lower! Try again.
Enter your guess: 300
Higher! Try again.
Enter your guess: 400
Higher! Try again.
Enter your guess: 450
Higher! Try again.
Enter your guess: 480
Lower! Try again.
Enter your guess: 460
Higher! Try again.
Enter your guess: 470
Lower! Try again.
Enter your guess: 461
Higher! Try again.
Enter your guess: 462
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
FRAY30-picoctf@webshell:~/bsh$ ssh -p 55517 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 463
Higher! Try again.
Enter your guess: 464
Higher! Try again.
Enter your guess: 465
Higher! Try again.
Enter your guess: 466
Higher! Try again.
Enter your guess: 467
Higher! Try again.
Enter your guess: 468
Higher! Try again.
Enter your guess: 469
Higher! Try again.
Enter your guess: 500
Higher! Try again.
Enter your guess: 700
Higher! Try again.
Enter your guess: 800
Higher! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
FRAY30-picoctf@webshell:~/bsh$ ssh -p 55517 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 900
Higher! Try again.
Enter your guess: 990
Lower! Try again.
Enter your guess: 950
Lower! Try again.
Enter your guess: 901
Higher! Try again.
Enter your guess: 910
Higher! Try again.
Enter your guess: 920
Lower! Try again.
Enter your guess: 914
Higher! Try again.
Enter your guess: 918
Lower! Try again.
Enter your guess: 915
Congratulations! You guessed the correct number: 915
Here's your flag: picoCTF{g00d_gu355_1597707f}
```
## Notas adicionales

## Referencias
