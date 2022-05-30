Using assembly language in BSIM to simulate a beta cpu, implement a game that was coded in C language.
i.e translate C language to assembly.

More about the game: 
Try to guess the secret 4-digit number

Each guess is scored with a count of “bulls” and “cows”

If the digit is in the number and at the correct position, 1 bull is awarded
If the digit is in the number but at the wrong position, 1 cow is given

Once a digit in the secret has been used to score a digit in the guess (e.g: counted as bull) it won’t be used in the scoring for other digits in the guess (e.g: wont be double counted as cow)

The count of bulls should be determined BEFORE scoring any cows (in code)


![image](https://user-images.githubusercontent.com/68263531/170956186-66b78a96-d49f-45b4-81b8-c312695690fc.png)




![image](https://user-images.githubusercontent.com/68263531/170954629-f6882013-71fd-45fd-9838-dc3903e00435.png)
