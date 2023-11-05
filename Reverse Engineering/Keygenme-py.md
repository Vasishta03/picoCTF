## Description
Description
[keygenme-trial.py]

## Approach
I opened the file using `cat keygenme-trial.py` and read the code.
- this part was looking off
  ```python
    key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
    key_part_dynamic1_trial = "xxxxxxxx"
    key_part_static2_trial = "}"
    key_full_template_trial = key_part_static1_trial + key_part_dynamic1_trial + key_part_static2_trial
  ```

- After reading the code completely i understood that, first part of the flag is "picoCTF{1n_7h3_|<3y_of_" and key is the same length as "picoCTF{1n_7h3_|<3y_of_xxxxxxxx}".
- The code is saying that there are 8 more if statements left to write in the function, and each if statement will check the value of the variable `x` against a different character in the string `45362718`.
  The code then uses a loop to iterate over the remaining characters in the string, and for each character, it sets the value of the variable `key[i]` to the corresponding character.
- I ran the following code in an online compiler
  ```python
  import hashlib
  username_trial = "PRITCHARD"
  bUsername_trial = b"PRITCHARD"

  key_part_static1_trial = "picoCTF{1n_7h3_|<3y_of_"
  key_part_dynamic1_trial = "xxxxxxxx"
  key_part_static2_trial = "}"
  key_full_template_trial = key_part_static1_trial + key_part_dynamic1_trial + key_part_static2_trial

  #I used bUsername_trial because enter_liscence used it as well but after testing afterwards, they output the same answer
  print(hashlib.sha256(bUsername_trial).hexdigest()[4]) 
  print(hashlib.sha256(bUsername_trial).hexdigest()[5])
  print(hashlib.sha256(bUsername_trial).hexdigest()[3])
  print(hashlib.sha256(bUsername_trial).hexdigest()[6])
  print(hashlib.sha256(bUsername_trial).hexdigest()[2])
  print(hashlib.sha256(bUsername_trial).hexdigest()[7])
  print(hashlib.sha256(bUsername_trial).hexdigest()[1])
  print(hashlib.sha256(bUsername_trial).hexdigest()[8])
  ```

The output is `54ef6292`

## Output
We can now complete the flag: `picoCTF{1n_7h3_|<3y_of_xxxxxxxx} --> picoCTF{1n_7h3_|<3y_of_54ef6292}`
so the flag is `picoCTF{1n_7h3_|<3y_of_54ef6292}`
