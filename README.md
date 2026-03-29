# Password-Ranker-Naruto-Version-
Talking about Digital Literacy, passwords are the most basic yet important thing for any digital literacy platform you visit. Creating a strong password sometimes  gets confusing, but, using this project...users can know their password's security rank in a fun way using anime (Naruto).

# My password's Shinobi Rank-
Academy Student: Very weak; needs more characters.
Genin: Basic security; add some numbers.
Chunin: Solid defense; add special symbols.
Hokage: Ultimate security! 

# Digital Literacy Lesson:
A Hokage level password should contain atleast 8 characters that can be both alphabets and numbers. It should also include atleast one symbol like hashtag, dollar sign, exclamatory mark, etc.

# python code execution:
python file: code.py

import re

def check_password_rank(password):
    # Digital Literacy: Checking for length, numbers, and symbols
    length_score = len(password) >= 8
    digit_score = any(char.isdigit() for char in password)
    symbol_score = bool(re.search(r"[!@#$%^&*(),.?\":{}|<>]", password))
    
    total_score = sum([length_score, digit_score, symbol_score])

    # Anime Ranking Logic
    if total_score == 0:
        return "Rank: Academy Student (Too Weak! A Genjutsu would break this.)"
    elif total_score == 1:
        return "Rank: Genin (Keep training! Add some numbers or symbols.)"
    elif total_score == 2:
        return "Rank: Chunin (Good! You're getting harder to track.)"
    else:
        return "Rank: Hokage (Legendary Security! Even the Akatsuki can't get in.)"

user_input = input("Enter a password to test your Shinobi Rank: ")
print(check_password_rank(user_input))




